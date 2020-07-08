---
title: Управление группами соединений на отдельном компьютере с помощью PowerShell
description: Управление группами соединений на отдельном компьютере с помощью PowerShell
author: dansimp
ms.assetid: b73ae74d-8a6f-4bb3-b1f2-0067c7bd5212
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 32dd4f9c5ad1ba4ae9e25246d5ec52a6363ef303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813925"
---
# Управление группами соединений на отдельном компьютере с помощью PowerShell


Группа соединений App-V позволяет запускать все виртуальные приложения как определенные наборы пакетов в одной виртуальной среде. Например, вы можете виртуализировать приложение и его подключаемые модули с помощью отдельных пакетов, но запускать их вместе в одной группе подключения.

XML-файл группы подключения определяет группу подключений, которая выполняется на компьютере, на котором установлен клиент App-V. Сведения о XML-файле группы подключения и его настройке можно найти [в разделе о файле группы подключения](about-the-connection-group-file.md).

В этой статье описаны следующие процедуры:

-   [Добавление и публикация пакетов App-V в группе "подключение"](#bkmk-add-pub-pkgs-in-cg)

-   [Добавление и включение группы соединений в клиенте App-V](#bkmk-add-enable-cg-on-clt)

-   [Включение и отключение группы подключений для определенного пользователя](#bkmk-enable-cg-for-user-poshtopic)

-   [Разрешение только администраторам поддержки групп подключений](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a>**Добавление и публикация пакетов App-V в группе "подключение"**

1.  Чтобы добавить пакеты App-V 5,0 и опубликовать их на компьютер с клиентом App-V, введите следующую команду:

    Add-AppvClientPackage — path c:\\tmpstore\\quartfin.AppV | Publish-AppvClientPackage

2.  Повторите **действия 1** для каждого пакета в группе подключение.

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**Добавление и включение группы соединений в клиенте App-V**

1.  Чтобы добавить группу подключения, введите следующую команду:

    Add-AppvClientConnectionGroup — Path c:\\tmpstore\\financ.xml

2.  Включите группу соединения, введя следующую команду:

    Enable-AppvClientConnectionGroup-Name "Financial Applications"

    Если на целевом компьютере выполняются любые виртуальные приложения, которые находятся в пакетах, они будут выполняться внутри виртуальной среды группы подключения и будут доступны для всех виртуальных приложений в других пакетах в группе подключения.

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**Включение и отключение группы подключений для определенного пользователя**

1.  Ознакомьтесь с описанием и требованиями к параметрам.

    -   Этот параметр позволяет администратору включать или отключать группу подключений для определенного пользователя.

    -   Чтобы использовать этот параметр, необходимо воспользоваться пакетом обновления 2 (SP2) для App-V 5,0 или более поздней версии.

    -   Вы можете запустить этот командлет из сеанса пользователя или администратора.

    -   Для использования параметра необходимо войти в систему с помощью учетных данных администратора.

    -   Конечный пользователь должен войти в систему.

    -   Необходимо указать идентификатор безопасности (SID) конечного пользователя.

2.  Используйте указанные ниже командлеты и добавьте необязательный параметр **–** код, где **-** то есть идентификатор безопасности конечного пользователя (SID).

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Командлет</th>
    <th align="left">Примеры:</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Enable-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Enable-AppVClientConnectionGroup "ConnectionGroupA" — в чем заключается S-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Disable-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Disable-AppVClientConnectionGroup "ConnectionGroupA" — в чем заключается S-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**Разрешение только администраторам поддержки групп подключений**

1.  Ознакомьтесь с описанием и требованием для использования этого командлета:

    -   Используйте этот командлет и параметр, чтобы настроить клиент App-V таким образом, чтобы он мог включать или отключать группы подключения только для администраторов (конечных пользователей).

    -   Для использования этого командлета необходимо использовать по крайней мере App-V 5,0 с пакетом обновления 3 (SP3).

2.  Выполните следующий командлет и параметр:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Командлет</th>
    <th align="left">Параметры и значения</th>
    <th align="left">Пример.</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Set-AppvClientConfiguration</p></td>
    <td align="left"><p>–RequirePublishAsAdmin</p>
    <ul>
    <li><p>0 – ложь</p></li>
    <li><p>1 — истина</p></li>
    </ul></td>
    <td align="left"><p>Set-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
    </tr>
    </tbody>
    </table>

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.0](operations-for-app-v-50.md)

[Администрирование App-V с помощью PowerShell](administering-app-v-by-using-powershell.md)

 

 





