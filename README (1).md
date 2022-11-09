# Инструкция по развёртыванию на Linux CentOS 7

Скачать docker-compose в каталог /usr/local/bin/

```
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.25.3/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

Сделать файл исполняемым и создаем симлинк

```
$ sudo chmod +x /usr/local/bin/docker-compose
$ sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

Клонировать репозиторий с приложением

```
git clone https://github.com/basesource-isk/osscore.git
```

Перейти в директорию osscore

```
cd osscore
```

Запустить развёртывание

```
docker-compose up
```

Приложение появится в браузере на странице

```
http://0.0.0.0:8000
```

