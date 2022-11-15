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

Запустить docker

```
sudo systemctl start docker
```

Запустить развёртывание

```
docker run -p 8000:8000 osscore/osscore
```

Приложение появится в браузере на странице

```
http://[ip-адрес]:8000
```

Проверить работу можно загрузив в приложение файл, скачанный по ссылке ниже

{% file src=".gitbook/assets/яндекс-расписания-api-тест.yml" %}

Или просто нажав кнопку **Тест**
