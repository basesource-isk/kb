# Инструкция по развёртыванию на Windows 10

* Установить Docker для Windows [https://www.docker.com/](https://www.docker.com/)
* Установить Git если не установлен [https://git-scm.com/download/win](https://git-scm.com/download/win)
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
* При запросе логина и пароля ввести следующие учётные данные

```
admin
```

```
osscore123@
```

* Проверить работу можно загрузив в приложение файл, скачанный по ссылке ниже

{% file src="../../../../.gitbook/assets/яндекс-расписания-api-тест.yml" %}
