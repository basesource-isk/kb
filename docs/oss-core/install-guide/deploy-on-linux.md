# Развёртывание на Linux

Инструкция для установки на операционную систему семейства Linux.

Рекомендуется для выполнения в среде ОС Centos 7, однако на других версиях Linux последовательность установки аналогичная.

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
cd osscore-otester-docker
```

* Запустить развёртывание командой `docker-compose up`

```
sudo docker-compose up
```

* Процесс развёртывания может занять около 2 минут. По окончанию в терминале появляется надпись `otester-client | Compiled Successfully`

После запуска интерфейс приложения будет доступен через браузер по адресу: `http://<IP-адрес или имя виртуальной машины>:4200`.

Для дальнейшей работы с приложением обратитесь к [руководству пользователя](../user-guide.md).
