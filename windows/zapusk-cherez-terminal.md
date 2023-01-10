# Запуск через терминал

Приложением можно пользоваться загружая файл с адресами проверок через терминал _<mark style="background-color:orange;">Powershell</mark>_. Для этого воспользуемся командой `Invoke-WebRequest`с параметром `-Infile`

````powershell
```powershell
function upload_file {
    param (
        $file_path
    )
    $boundary = [System.Guid]::NewGuid().ToString()
    $FilePath = "$file_path"
    $TheFile = [System.IO.File]::ReadAllBytes($FilePath)
    $TheFileContent = [System.Text.Encoding]::GetEncoding('iso-8859-1').GetString($TheFile)

    $LF = "`r`n"
    $bodyLines = (
        "--$boundary",
        "Content-Disposition: form-data; name=`"Description`"$LF",
        "This is a file I'm uploading",
        "--$boundary",
        "Content-Disposition: form-data; name=`"file`"; filename=`"file.json`"",
        "Content-Type: application/json$LF",
        $TheFileContent,
        "--$boundary--$LF"
    ) -join $LF

    Invoke-RestMethod 'http://localhost:8000/api-rest-api/' -Method POST -ContentType "multipart/form-data; boundary=`"$boundary`"" -Body $bodyLines
}
```
````
