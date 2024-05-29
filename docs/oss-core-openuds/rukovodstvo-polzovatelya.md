# Руководство пользователя

### Общие данные <a href="#obshie-dannye" id="obshie-dannye"></a>

OSS Core OpenUDS предназначен для виртуализации рабочего стола пользователя.

С помощью специализированного ПО на рабочем месте пользователь может удаленно подключиться в систему, получая доступ ко всем программам, приложениям и данным.

### Инструкция по подключению <a href="#instrukciya-po-podklyucheniyu" id="instrukciya-po-podklyucheniyu"></a>

#### Подготовка к работе <a href="#podgotovka-k-rabote" id="podgotovka-k-rabote"></a>

Скачайте дистрибутивы и установите следующее ПО:

**Virt-Viewer**

Данный дистрибутив размещен в личном кабинете. _Каталог загрузок -> Дистрибутивы -> Tools -> Virt-viewer_

**Usb-Dk** Данный дистрибутив размещен в личном кабинете. _Каталог загрузок -> Дистрибутивы -> Tools -> Usb-dk_

**UDS Client** Данный дистрибутив размещен на портале брокера VDI. _Загрузить его можно, перейдя на соответствующую вкладку._

![](https://kb.pvhostvm.ru/\~gitbook/image?url=https%3A%2F%2F2603182569-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-M6-oafU4c2bTrhoNggH%252Fuploads%252F3GxlngkJUfNOKm7kS6mx%252Fimage.png%3Falt%3Dmedia%26token%3D1da52728-e08d-425b-91f1-6eab34ad284e\&width=768\&dpr=4\&quality=100\&sign=cf6284a12cbef50bd52558344b30bb52487c7ecc47ec023d45565ab9395a2311)карт

**Рис.1 Раздел UDS Client**

#### Вход в систему <a href="#vkhod-v-sistemu" id="vkhod-v-sistemu"></a>

Для входа в систему выполните следующие шаги: 1. Откройте в браузере адрес VDI-портала; 2. В открывшуюся форму введите логин, пароль и предоставленный аутентификатор.

![](https://kb.pvhostvm.ru/\~gitbook/image?url=https%3A%2F%2F2603182569-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-M6-oafU4c2bTrhoNggH%252Fuploads%252FMscxEm7iGVRV0V7Bo06b%252Fimage.png%3Falt%3Dmedia%26token%3D0c6935bc-a2d4-4bd2-b36e-1658e53e167b\&width=768\&dpr=4\&quality=100\&sign=6b09005884ceb9f8048a10b2fd1de51be81dcb2cf66fbc0a1f3c4b706ffe3783)карт

**Рис.2 Форма для авторизации**

1.  Выберите нужный сервис и нажмите на иконку для открытия сессии.

    ![](https://kb.pvhostvm.ru/\~gitbook/image?url=https%3A%2F%2F2603182569-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-M6-oafU4c2bTrhoNggH%252Fuploads%252FntKheJwjJyxp2Izf4SyA%252Fimage.png%3Falt%3Dmedia%26token%3Df1dcd6e1-1d89-46ce-b19d-ab5634f14c47\&width=768\&dpr=4\&quality=100\&sign=8a8f4c700196d1b87d0ae0ff9e7d2bb147a38fa99b491f8232c9b836af06b760)

**Рис.3 Перечень сервисов**

После открытия сессии может потребовать еще раз ввести пароль

![](https://kb.pvhostvm.ru/\~gitbook/image?url=https%3A%2F%2F2603182569-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-M6-oafU4c2bTrhoNggH%252Fuploads%252FyWG4tuZwckt1PQPSj99l%252Flogin.jpg%3Falt%3Dmedia%26token%3D362ea368-86e2-4e85-8e3a-31489d0e9387\&width=768\&dpr=4\&quality=100\&sign=d40816084841845531ac524a52342e6d5c060ada6138ce90887340df9b386738)

**Рис.4 Вход в систему**

Если необходимо подключить в сессию USB-устройство с локальной машины, выполните следующие шаги: 1. В окне с открытой сессией выберите пункт меню: Файл → USB Device Selection;

![](https://kb.pvhostvm.ru/\~gitbook/image?url=https%3A%2F%2F2603182569-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-M6-oafU4c2bTrhoNggH%252Fuploads%252F9PWCrdLkxWE8vm1QiDXX%252Fsession.jpg%3Falt%3Dmedia%26token%3D566b9320-f9ed-40d2-86dc-ae1d4c9bfae1\&width=768\&dpr=4\&quality=100\&sign=f64e179ccc8fd015d83af2927048d040bffcab2c3469335dd2ce561d2654611f)

**Рис.5 Окно с открытой сессией**

1. Отметьте нужное устройство в появившемся списке;

![](https://kb.pvhostvm.ru/\~gitbook/image?url=https%3A%2F%2F2603182569-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-legacy-files%2Fo%2Fassets%252F-M6-oafU4c2bTrhoNggH%252Fsync%252F84ba39f80cf88ce19415f24c4aa91887e949b5ef.png%3Fgeneration%3D1588079040185981%26alt%3Dmedia\&width=768\&dpr=4\&quality=100\&sign=ded58df1701da42b2ac9cfa24a39bf9a8f56b4f8963e3b832cb2f941b24d2a43)карт

**Рис.6 Выбор USB-устройства**

1. Закройте список и дождитесь подключения устройства в сессию.





