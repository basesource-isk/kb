# Запуск через терминал

Приложением можно пользоваться загружая файл с адресами проверок через терминал _<mark style="background-color:orange;">Powershell</mark>_. Для этого воспользуемся командой `Invoke-WebRequest`с параметром `-Infile`

```
Invoke-RestMethod -Uri http://localhost:8000 -Method Post -InFile "tests/test.yml" -UseDefaultCredentials
```
