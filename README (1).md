# Инструкция по развёртыванию на Linux CentOS 7

Установить docker

```
sudo yum install -y yum-utils
```

```
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```

```
sudo yum install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

Установить docker-compose

```
yum install -y docker-compose
```

Запустить docker

```
sudo systemctl start docker
```

Установить git

```
yum install -y git
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
http://[ip-адрес]:8000
```

Проверить работу можно загрузив в приложение файл, скачанный по ссылке ниже

{% file src=".gitbook/assets/яндекс-расписания-api-тест.yml" %}

Или просто нажав кнопку **Тест**
