# Инструкция по развёртыванию на Windows 10

Установить Docker для Windows [https://www.docker.com/](https://www.docker.com/)

Запустить Docker на компьютере

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

Приложение появится в браузере на странице [http://localhost:8000](http://localhost:8000)

Проверить работу можно загрузив в приложение файл, скачанный по ссылке ниже

{% file src="../.gitbook/assets/яндекс-расписания-api-тест.yml" %}

Или просто нажав кнопку **Тест**
