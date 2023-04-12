# Инструкция по развёртыванию на Windows 10

* Установить Docker для Windows [https://www.docker.com/](https://www.docker.com/)
* Запустить Docker на компьютере
* Запустить терминал _Powershell_
* Клонировать репозиторий с файлом _compose.yml_

```
git clone https://github.com/d-poletavkin/osscore-otester-docker.git
```

* Перейти в директорию _osscore-otester-docker_

```
cd osscore-otester-docker
```

* Запустить развёртывание командой `docker-compose up`

```
docker-compose up
```

* Приложение появится в браузере на странице [http://localhost:](http://localhost:8000)4200
* Проверить работу можно загрузив в приложение файл, скачанный по ссылке ниже

{% file src="../../../../.gitbook/assets/яндекс-расписания-api-тест.yml" %}
