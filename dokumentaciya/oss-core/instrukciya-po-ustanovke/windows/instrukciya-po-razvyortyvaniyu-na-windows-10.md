# Инструкция по развёртыванию на Windows 10

* Установить Docker для Windows [https://www.docker.com/](https://www.docker.com/)
* Запустить Docker на компьютере
* Запустить терминал _Powershell_
* Клонировать репозиторий с файлом _docker-compose.yml_

```
git clone https://github.com/basesource-isk/osscore-docker-compose-file.git
```

* Перейти в директорию _osscore-docker-compose-file_

```
cd osscore-docker-compose-file
```

* Запустить развёртывание командой `docker-compose up`

```
docker-compose up
```

* Приложение появится в браузере на странице [http://localhost:8000](http://localhost:8000)
* Проверить работу можно нажав кнопку **Тест** или загрузив в приложение файл, скачанный по ссылке ниже

{% file src="../.gitbook/assets/яндекс-расписания-api-тест.yml" %}
