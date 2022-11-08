---
description: Инструкция по развёртыванию приложения
---

# OSS Core

Скачиваем docker-compose в каталог /usr/local/bin/

```
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.25.3/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

Делаем файл исполняемым и создаем симлинк

```
$ sudo chmod +x /usr/local/bin/docker-compose
$ sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

Клонируем репозиторий с приложением

```
https://github.com/basesource-isk/osscore.git
```

Переходим в директорию osscore

```
cd osscore
```

Запускаем развёртывание

```
docker-compose up
```

Переходим в браузере на страницу приложения

```
http://0.0.0.0:8000
```

