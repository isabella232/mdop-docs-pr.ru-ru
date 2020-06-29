---
title: Загрузка командлетов PowerShell и получение справки по командлетам
description: Загрузка командлетов PowerShell и получение справки по командлетам
author: dansimp
ms.assetid: b6ae5460-2c3a-4030-b132-394d9d5a541e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 32b5bb26331f204acffbf96ea119ac4209c3cd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813949"
---
# Загрузка командлетов PowerShell и получение справки по командлетам


В этой статье рассказывается, как это делать.

-   [Требования для использования командлетов PowerShell](#bkmk-reqs-using-posh)

-   [Загрузка командлетов PowerShell](#bkmk-load-cmdlets)

-   [Вызов справки по командлетам PowerShell](#bkmk-get-cmdlet-help)

-   [Отображение справки для командлета PowerShell](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a>Требования для использования командлетов PowerShell


Ознакомьтесь с приведенными ниже требованиями для использования командлетов PowerShell App-V:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Требование</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Пользователи могут запускать командлеты App-V Server только в том случае, если вы предоставляете им доступ с помощью одного из указанных ниже способов.</p></td>
<td align="left"><ul>
<li><p><strong>При развертывании и настройке сервера App-V выполните указанные </strong> ниже действия.</p>
<p>Укажите группу Active Directory или отдельного пользователя, у которого есть разрешения на управление средой App-V. Узнайте <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> , как развернуть сервер App-V 5,1 </a> .</p></li>
<li><p><strong>После того как вы развернули сервер App-V, </strong> выполните указанные ниже действия.</p>
<p>Добавьте дополнительную группу или пользователя Active Directory с помощью консоли управления App-V. Узнайте <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console51.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)"> , как добавить или удалить администратора с помощью консоли управления </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Командлеты, для которых требуется Командная строка с повышенными привилегиями</p></td>
<td align="left"><ul>
<li><p>Add-AppvClientPackage</p></li>
<li><p>Remove-AppvClientPackage</p></li>
<li><p>Set-AppvClientConfiguration</p></li>
<li><p>Add-AppvClientConnectionGroup</p></li>
<li><p>Remove-AppvClientConnectionGroup</p></li>
<li><p>Add-AppvPublishingServer</p></li>
<li><p>Remove-AppvPublishingServer</p></li>
<li><p>Send-AppvClientReport</p></li>
<li><p>Set-AppvClientMode</p></li>
<li><p>Set-AppvClientPackage</p></li>
<li><p>Set-AppvPublishingServer</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Командлеты, с помощью которых можно запускать конечные пользователи, если не настроить для них необходимость в командной строке с повышенными привилегиями.</p></td>
<td align="left"><ul>
<li><p>Publish-AppvClientPackage</p></li>
<li><p>Отмена публикации — AppvClientPackage</p></li>
</ul>
<p>Чтобы настроить эти командлеты для использования командной строки с повышенными привилегиями, воспользуйтесь одним из указанных ниже способов.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Метод</th>
<th align="left">Дополнительные ресурсы</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Запустите <strong> командлет Set-AppvClientConfiguration </strong> с <strong> параметром-RequirePublishAsAdmin </strong> .</p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg)">Управление группами соединений на отдельном компьютере с помощью PowerShell</a></p></li>
<li><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">Управление пакетами App-V 5.1, работающими на автономном компьютере, с помощью PowerShell</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Включите параметр групповой политики "требуется публикация от имени администратора" для клиентов App-V.</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-51.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md)">Публикация пакета с помощью консоли управления</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a>Загрузка командлетов PowerShell

Чтобы загрузить модули командлетов PowerShell, выполните указанные ниже действия.

1.  Откройте Windows PowerShell или интегрированную среду сценариев Windows PowerShell (ISE).

2.  Чтобы загрузить командлеты для нужного модуля, введите одну из следующих команд:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Компонент App-V</th>
<th align="left">Команда для ввода</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Сервер App-V</p></td>
<td align="left"><p>Import-Module AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Секвенсор App-V</p></td>
<td align="left"><p>Import-Module AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Клиент App-V</p></td>
<td align="left"><p>Import-Module AppvClient</p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-get-cmdlet-help"></a>Вызов справки по командлетам PowerShell
Начиная с версии App-V 5,0 с пакетом обновления 3 (SP3), Справка по командлетам доступна в двух форматах:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Формат</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Как загружаемый модуль</p></td>
<td align="left"><p>Чтобы скачать последнюю справку после загрузки модуля командлета, выполните указанные ниже действия.</p>
<ol>
<li><p>Откройте Windows PowerShell или интегрированную среду сценариев Windows PowerShell (ISE).</p></li>
<li><p>Чтобы загрузить командлеты для нужного модуля, введите одну из следующих команд:</p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Компонент App-V</th>
<th align="left">Команда для ввода</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Сервер App-V</p></td>
<td align="left"><p>Update-Help-Module AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Секвенсор App-V</p></td>
<td align="left"><p>Update-Help-Module AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Клиент App-V</p></td>
<td align="left"><p>Update-Help-Module AppvClient</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>На веб-страницах TechNet</p></td>
<td align="left"><p>Ознакомьтесь с разделом App-V в разделе <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> Автоматизация пакета оптимизации рабочей среды Microsoft для Windows PowerShell </a> .</p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-display-help-cmdlet"></a>Отображение справки для командлета PowerShell
Чтобы отобразить справку для определенного командлета PowerShell, выполните указанные ниже действия.

1.  Откройте Windows PowerShell или интегрированную среду сценариев Windows PowerShell (ISE).

2.  Введите **командлет Get-Help** &lt; *cmdlet* &gt; , например **Get-Help Publish-AppvClientPackage**.

**У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





