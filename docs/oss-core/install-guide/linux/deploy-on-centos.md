# Инструкция по развёртыванию на CentOS 7

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
sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-Linux-x86_64" -o /usr/local/bin/docker-compose
```

```
sudo chmod +x /usr/local/bin/docker-compose
```

```
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

* Проверить, корректно ли установился _docker-compose_

```
sudo docker-compose -v
```

* Установить _git_ если не установлен

```
sudo yum install -y git
```

* Запустить docker

```
sudo systemctl start docker
```

* Клонировать репозиторий с файлом _compose.yml_

```
sudo git clone https://github.com/d-poletavkin/osscore-otester-docker.git
```

* Перейти в директорию osscore-otester-docker

```
sudo cd osscore-otester-docker
```

* Запустить развёртывание командой `docker-compose up`

```
sudo docker-compose up
```

* Приложение появится в браузере на странице

```
http://[ip-адрес]:4200
```

* При запросе логина и пароля ввести следующие учётные данные

```
admin
```

```
osscore123@
```

Проверить работу можно загрузив в приложение файл, скачанный по ссылке ниже

{% file src="../../../../.gitbook/assets/яндекс-расписания-api-test.yml" %}
