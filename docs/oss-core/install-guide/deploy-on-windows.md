# Развёртывание на Windows

Инструкция для установки на операционную систему семейства Windows.

Рекомендуется для выполнения в среде ОС Windows 10, однако на других версиях Windows последовательность установки аналогичная.

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

* Процесс развёртывания может занять около 2 минут. По окончанию в терминале появляется надпись `otester-client | Compiled Successfully`

После запуска интерфейс приложения будет доступен через браузер по адресу: `http://<IP-адрес или имя виртуальной машины>:4200`.

Для дальнейшей работы с приложением обратитесь к [руководству пользователя](../user-guide.md).
