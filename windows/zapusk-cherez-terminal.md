# Запуск через терминал

Приложением можно пользоваться загружая файл с адресами проверок через терминал _<mark style="background-color:orange;">Powershell</mark>_. Для этого скопируйте функцию ниже в терминал. Обратите внимание на строку `http://localhost:8000/api-rest-api/` - если вместо порта 8000 используется какой-либо другой, то нужно указать действительное значение

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

И запустите указав в качестве параметра путь к файлу с текстом скрипта проверок:

<pre><code>upload_file "[<a data-footnote-ref href="#user-content-fn-1">Пример: C:/NewFolder/test.yml</a>]"
</code></pre>

[^1]: Здесь указывается абсолютный путь к файлу с расширением .yml с текстом скрипта проверок
