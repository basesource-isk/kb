# Руководство по установке и настройке

Компоненты OSS Core HOSTVM VDI поставляются в виде готовых виртуальных машин. Вы можете скачать их из каталога загрузок, доступного в [личном кабинете](https://lk.pvhostvm.ru/).

Ознакомьтесь с [системными требованиями](https://kb.pvhostvm.ru/hostvm-vdi/hostvm-vdi-installation-guide/requirements) для виртуальных машин OSS Core HOSTVM VDI.

В каталоге загрузок образы виртуальных машин расположены в директории `HOSTVM-VDI/`, для загрузки доступны следующие версии:

`HOSTVM-VDI/beta` - версия ПО, находящаяся в режиме бета-тестирования;

`HOSTVM-VDI/stable` - текущий стабильный релиз(-ы);

`HOSTVM-VDI/legacy` - предыдущий стабильный релиз(-ы).

#### Компоненты OSS Core HOSTVM VDI <a href="#mandatory" id="mandatory"></a>

**OSS Core HOSTVM VDI Брокер**: брокер подключений, требуется во всех вариантах развертывания.

Предоставляет функционал портала пользователя и портала администратора системы, обеспечивает жизненный цикл виртуальных рабочих столов и приложений, взаимодействие с гипервизорами и другими сервис-провайдерами.

Для импорта и настройки воспользуйтесь [инструкцией](https://kb.pvhostvm.ru/hostvm-vdi/hostvm-vdi-installation-guide/hostvm-vdi-ova-install).

#### Дополнительные компоненты <a href="#optional" id="optional"></a>

**OSS Core HOSTVM VDI Шлюз**: шлюз для предоставления защищенных подключений и HTML5 доступа к сервисам.

Используйте данный компонент, если вам требуется обеспечить защищенный доступ пользователей к сервисам VDI из WAN, и/или возможность подключения через HTML5.

Для импорта и настройки воспользуйтесь [инструкцией](https://kb.pvhostvm.ru/hostvm-vdi/hostvm-vdi-installation-guide/tunneler-appliance-deploy).

**OSS Core HOSTVM VDI Сервер БД**: сервер базы данных брокера подключений.

Используйте данный компонент, если вам требуется выделенный сервер БД брокера вместо встроенного в составе брокера, например как часть отказоустойчивой конфигурации, в случае отсутствия собственного сервера БД в инфраструктуре.

Для импорта и настройки воспользуйтесь [инструкцией](https://kb.pvhostvm.ru/hostvm-vdi/hostvm-vdi-installation-guide/vdi-db).

**OSS Core HOSTVM VDI Балансировщик** - обеспечивает балансировку подключений к брокерам и шлюзам HOSTVM VDI при развертывании отказоустойчивой конфигурации.

Для импорта и настройки воспользуйтесь [инструкцией](https://kb.pvhostvm.ru/hostvm-vdi/hostvm-vdi-installation-guide/haproxy).

#### Дальнейшая настройка <a href="#dalneishaya-nastroika" id="dalneishaya-nastroika"></a>

Для дальнейшей настройки системы обратитесь к [руководству администратора](https://kb.pvhostvm.ru/hostvm-vdi/hostvm-vdi-admin-guide).

#### Перечень изменений <a href="#perechen-izmenenii" id="perechen-izmenenii"></a>

С перечнем изменений и исправлений вы можете ознакомиться в [статье](https://kb.pvhostvm.ru/hostvm-vdi/hostvm-vdi-installation-guide/changelog).

#### Компоненты OSS Core HOSTVM <a href="#mandatory" id="mandatory"></a>

Более подробно ознакомиться с платформой можно по ссылке: [О платформе ](https://kb.pvhostvm.ru/hostvm/installation-guide/datasheet)Ознакомиться с системными требованиями HOSTVM node и HOSTVM Manager можно по ссылке: [Системные требования ](https://kb.pvhostvm.ru/hostvm/installation-guide/requirements)

Дистрибутивы для установки HOSTVM node находятся в [Личном кабинете](https://lk.pvhostvm.ru/) в директории HOSTVM, для загрузки доступны следующие версии:&#x20;

`HOSTVM/beta` - версия ПО, находящаяся в режиме бета-тестирования;&#x20;

`HOSTVM/stable` - текущий стабильный релиз(-ы);&#x20;

`HOSTVM/legacy` - предыдущий стабильный релиз(-ы).&#x20;

Дистрибутивы, имеющие в названии "offline" используются в условиях отсутствия подключения к Интернету и/или при использовании прокси (актуально для версий 4.3, 4.4). Для версии 4.5.\* образ hostvm-node-ng-installer используется для установки гипервизора (HOSTVM node), образ hostvm-node-ng-installer-local-repo используется для последующей установки HOSTVM Manager.&#x20;

Гостевые инструменты находятся в директории Misc/Guest tools, ссылка на инструкцию по установке: [Установка гостевых агентов и драйверов в Windows ](https://kb.pvhostvm.ru/hostvm/rukovodstvo-po-administrirovaniyu/vm/gostevye-agenty-hostvm-instrumenty-i-draivery/ustanovka-gostevykh-agentov-i-draiverov-v-windows)Сценарий импорта виртуальных машин находится в директории Misc/VM Convert&#x20;

Для конвертации и импорта виртуальных машин из других сред виртуализации воспользуйтесь инструкцией: [Конвертация, импорт виртуальных машин](https://kb.pvhostvm.ru/hostvm/installation-guide/konvertaciya-import-virtualnykh-mashin)&#x20;

Для установки HOSTVM node и HOSTVM Manager воспользуйтесь [Руководством по установке и настройке ](https://kb.pvhostvm.ru/hostvm/installation-guide)

Для дальнейшей настройки системы обратитесь к [Руководству по администрированию](https://kb.pvhostvm.ru/hostvm/rukovodstvo-po-administrirovaniyu)
