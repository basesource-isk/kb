# Руководство администратора

Для использования приложения вам потребуется составить один или несколько файлов с тестами. В качестве формата для файлов используется YAML.

Структура файла представляет собой набор параметров вида `ключ: значение`. Основные параметры должны быть указаны в каждом файле, параметры модуля задаются в зависимости от типа тестирования.

На данный момент в приложении доступны 3 модуля:

* `rest_api`: для взаимодействия с REST API тестируемого сервиса;
* `html`: для web тестов;
* `bash`: для использования командной оболочки.

## Основные параметры <a href="#global-keys" id="global-keys"></a>

<table><thead><tr><th width="192">Ключ</th><th>Описание</th></tr></thead><tbody><tr><td><code>name</code></td><td>Необязательное поле. Произвольное имя файла с тестами</td></tr><tr><td><code>module</code></td><td>Тип тестирования, поддерживается 3 значения: <code>rest_api</code>, <code>bash</code>, <code>html</code></td></tr><tr><td><code>server_ip</code></td><td>IP-адрес тестируемого сервиса.</td></tr><tr><td><code>alias</code></td><td>Необязательное поле. При загрузке файла в приложение заданное значение будет отображено в столбце <code>Псевдоним</code>.</td></tr><tr><td><code>authentication</code></td><td>Необязательное поле. Учетные данные для аутентификации</td></tr></tbody></table>

### Модуль rest\_api <a href="#rest-api-keys" id="rest-api-keys"></a>

<table><thead><tr><th width="191">Ключ</th><th>Описание</th></tr></thead><tbody><tr><td><code>base url</code></td><td>Точка входа API.</td></tr><tr><td><code>urls</code></td><td>Запросы к ресурсам API.</td></tr></tbody></table>

### Модуль html <a href="#html-keys" id="html-keys"></a>

<table><thead><tr><th width="200">Ключ</th><th>Описание</th></tr></thead><tbody><tr><td><code>base url</code></td><td>Базовый URL сервиса.</td></tr><tr><td><code>pages</code></td><td>Перечень URL и параметров для тестирования.</td></tr></tbody></table>

### Модуль bash <a href="#shell-keys" id="shell-keys"></a>

<table><thead><tr><th width="193">Ключ</th><th>Описание</th></tr></thead><tbody><tr><td><code>commands</code></td><td>Набор выполняемых команд оболочки и проверок результата выполнения.</td></tr></tbody></table>

## Описание параметров <a href="#reference" id="reference"></a>

### `alias`

Необязательное поле. При загрузке файла в приложение заданное значение будет отображено в столбце `Псевдоним`.

Тип параметра: Основной.

Пример:

```yaml
alias: "Псевдоним теста"
```

### `authentication`

Учетные данные для аутентификации.

Тип параметра: Основной.

Поддерживает следующие подпараметры:

* `authentication:auth`
* `authentication:login`
* `authentication:username`
* `authentication:password`

#### `authentication:auth`

Позволяет указать тип аутентификации, если на конечном сервисе доступно несколько способов (например: внутренняя база данных, LDAP, Radius и т.д.).

Тип параметра: `html`, `rest_api`

Пример:

```yaml
authentication:
  auth: internal
```

#### `authentication:login`

Имя учетной записи.

Тип параметра: `bash`, `html`

Пример для модуля `html`:

```yaml
authentication:
  login: user
```

Для модуля `bash` указывается в формате `пользователь@адрес_сервиса`:

```yaml
authentication:
  login: user@10.1.1.10
```

#### `authentication:username`

Имя учетной записи.

Тип параметра: `rest_api`

Пример:

```yaml
authentication:
  username: user
```

#### `authentication:password`

Пароль учетной записи.

Тип параметра: `bash`, `html`, `rest_api`

Пример:

```yaml
authentication:
  password: password
```

### `base url`

URL для доступа к тестируемому сервису.

Тип параметра: `html`, `rest_api`

Для модуля `html` указывается базовый URL сервиса:

```yaml
base url: https://10.1.1.10/
```

Для модуля `rest_api` указывается точка входа API:

```yaml
base url: https://10.1.1.10/rest/
```

### `commands`

Набор выполняемых команд оболочки и проверок результата выполнения, каждый элемент передается в виде списка значений.

Тип параметра: `bash`

Список передаваемых значений:

* `command`: выполняемая команда оболочки;
* `expect_contains`: строка, которую должен содержать результат выполнения команды. Если параметр пуст, результат проверки всегда будет успешным. Регистр символов при проверке игнорируется.

Пример:

```yaml
commands:
  - command: uname 
    expect_contains: linux
  - command: systemctl status tomcat9.service
    expect_contains: active (running)
```

### `module`

Тип используемого для тестирования модуля приложения.

Тип параметра: Основной.

Возможные значения параметра:

* `rest_api`
* `bash`
* `html`

Пример:

```yaml
module: rest_api
```

### `name`

Произвольное имя файла с тестами.

Тип параметра: Основной.

Пример:

```yaml
name: "Стандартный тест rest-api на сервере 10.1.1.10"
```

### `pages`

Перечень URL и параметров для тестирования, каждый элемент передается в виде списка значений.

Тип параметра: `html`

Список передаваемых значений:

* `url`: путь к тестируемой странице, полный URL формируется добавлением этого значения к параметру `base url`;
* `method`: метод поиска веб-элемента, возможные значения: `id`, `name`, `xpath`, `linktext`, `tag`, `class`, `css`;
* `value`: значение для поиска, используется для всех методов поиска кроме `linktext`;
* `text`: текст ссылки для поиска, используется с методом `linktext`;
* `click`: нажатие на веб-элемент, возможные значения: `false` или `true`.

Расшифровка значений `method`:

* `id`: поиск веб-элемента по атрибуту id;
* `name`: поиск веб-элемента по атрибуту name;
* `xpath`: поиск веб-элемента по XPath;
* `linktext`: поиск гиперссылки по тексту (частичное совпадение);
* `tag`: поиск веб-элемента по HTML-тегу;
* `class`: поиск веб-элемента по атрибуту class;
* `css`: поиск веб-элемента с использованием синтаксиса CSS selector.

Пример:

```yaml
pages:
  - url: page/login
    method: tag
    value: body
    text: 
    click: false
```

### `server_ip`

IP-адрес тестируемого сервиса.

Тип параметра: Основной.

Пример:

```yaml
server_ip: '10.1.1.10'
```

### `urls`

Запросы к ресурсам API, каждый элемент передается в виде списка значений.

Тип параметра: `rest_api`

Список передаваемых значений:

* `url`: ресурс API, полный URL формируется добавлением этого значения к параметру `base url`;
* `method`: метод HTTP, возможные значения: `get`, `put`, `post`, `delete`;
* `body`: набор данных, передаваемых в запросе, в формате `ключ: значение`, определяются API тестируемого сервиса;
* `details`: необязательное поле, позволяет выполнять запросы к вложенным элементам, если ресурс является коллекцией. Каждый элемент передается в виде списка значений `url`, `method`, `body`.

Пример:

```yaml
urls:
  - url: api-endpoint1/
    method: post
    body:
      key1: value1
      key2: value2
  - url: api-endpoint2/
    method: put
    body:
      key1: value1
      key2: value2
    details:
      - url: detail/
        method: put
        body:
          key1: value1
```

