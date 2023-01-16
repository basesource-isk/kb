# Инструкция по развёртыванию на Linux CentOS 7

* Установить docker

```
sudo yum install -y yum-utils
```

```
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```

```
sudo yum install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

* Установить _docker-compose_

```
curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-Linux-x86_64" -o /usr/local/bin/docker-compose
```

```
chmod +x /usr/local/bin/docker-compose
```

* Проверить, корректно ли установился _docker-compose_

```
docker-compose -v
```

* Установить _git_ если не установлен

```
sudo yum install -y git
```

* Запустить docker

```
sudo systemctl start docker
```

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

* Приложение появится в браузере на странице

```
http://[ip-адрес]:8000
```

Проверить работу можно нажав кнопку **Тест** или **** загрузив в приложение файл, скачанный по ссылке ниже

{% file src="../.gitbook/assets/яндекс-расписания-api-тест.yml" %}
