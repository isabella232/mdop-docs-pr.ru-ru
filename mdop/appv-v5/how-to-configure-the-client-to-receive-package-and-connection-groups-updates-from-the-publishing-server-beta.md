---
title: Настройка клиента для получения обновлений пакетов и групп соединений с сервера публикации
description: Настройка клиента для получения обновлений пакетов и групп соединений с сервера публикации
author: dansimp
ms.assetid: f5dfd96d-4b63-468c-8d93-9dfdf47c28fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e9df1f8b324430449d8d1dd3624d9f1157968a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814389"
---
# Настройка клиента для получения обновлений пакетов и групп соединений с сервера публикации


Развертывание пакетов и групп соединений с помощью сервера публикаций App-V 5,0 является полезным, так как он поддерживает единую точку управления и высокую масштабируемость.

Чтобы настроить клиент App-V 5,0 для получения обновлений с сервера публикаций, выполните указанные ниже действия.

**Примечание**  Для следующих процедур сервер управления установлен на компьютере с именем **MyMgmtSrv**, а сервер публикаций установлен на компьютере с именем **MyPubSrv**.

 

**Настройка клиента App-V 5,0 для получения обновлений с сервера публикаций**

1.  Разверните сервер управления App-V 5,0 и серверы публикации и добавьте необходимые пакеты и группы подключений. Дополнительные сведения о добавлении пакетов и групп подключений можно найти [в разделе Добавление и обновление пакетов с помощью консоли управления](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) и [Создание группы подключения](how-to-create-a-connection-group.md).

2.  Чтобы открыть консоль управления, щелкните указанную ниже ссылку, откройте браузер и введите указанные ниже команды. http://MyMgmtSrv/AppvManagement/Console.html в веб-браузере, а также для импорта, публикации и обслуживания всех пакетов и групп подключений, которые будут необходимы для определенного набора пользователей.

3.  На компьютере, на котором запущен клиент App-V 5,0, откройте командную команду PowerShell с повышенными привилегиями, выполнив следующую команду:

    **Add-AppvPublishingServer-Name ABC-URL http://MyPubSrv/AppvPublishing**

    Эта команда позволяет настроить указанный сервер публикаций. Результат должен выглядеть примерно следующим образом:

    ID: 1

    SetByGroupPolicy: false

    Name (имя): ABC

    URL-адрес: http://MyPubSrv/AppvPublishing

    GlobalRefreshEnabled: false

    GlobalRefreshOnLogon: false

    GlobalRefreshInterval: 0

    GlobalRefreshIntervalUnit: Day

    UserRefreshEnabled: true

    UserRefreshOnLogon: true

    UserRefreshInterval: 0

    UserRefreshIntervalUnit: Day

    Возвращенный идентификатор — в данном случае 1

4.  На компьютере, на котором запущен клиент App-V 5,0, откройте командную строка PowerShell и введите следующую команду:

    **Sync-AppvPublishingServer-ServerId 1**

    Команда будет запрашивать сервер публикаций для пакетов и групп подключений, которые необходимо добавить или удалить для этого конкретного клиента на основании данных о разобслуживаниях пакетов и групп подключений, настроенных на сервере управления.

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.0](operations-for-app-v-50.md)

 

 





