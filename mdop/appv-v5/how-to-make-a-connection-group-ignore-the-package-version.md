---
title: Настройка игнорирования версии пакета группой соединений
description: Настройка игнорирования версии пакета группой соединений
author: dansimp
ms.assetid: 6ebc1bff-d190-4f4c-a6da-e09a4cca7874
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b64d1938419aef184c5df667bf71b8157de0450a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813960"
---
# Настройка игнорирования версии пакета группой соединений


Microsoft Application Virtualization (App-V) 5,0 с пакетом обновления 3 (SP3) позволяет настроить группу подключений для использования любой версии пакета, которая упрощает обновление пакета и сокращает количество групп соединений, которые необходимо создать.

Чтобы обновить пакет в более ранних версиях App-V, необходимо выполнить несколько действий, включая отключение группы подключения и изменение XML-файла определения группы подключения.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Описание задачи с помощью App-V 5,0 SP3</th>
<th align="left">Выполнение задачи с помощью App-V 5,0 с пакетом обновления 3 (SP3)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Вы можете настроить группу подключений таким образом, чтобы она принимала любую версию пакета, которая позволяет обновлять пакет без необходимости отключить группу подключения.</p>
<p><strong>Как работает эта функция:</strong></p>
<ul>
<li><p>Если группа подключений имеет доступ к нескольким версиям пакета, используется новейшая версия.</p></li>
<li><p>Если группа подключения содержит необязательный пакет с неверной версией, пакет игнорируется и не блокирует создание виртуальной среды группы подключения.</p></li>
<li><p>Если группа подключения содержит необязательный пакет с неверной версией, виртуальная среда группы подключения не может быть создана.</p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Метод</th>
<th align="left">Действия</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Сервер App-V Server — консоль управления</p></td>
<td align="left"><ol>
<li><p>На консоли управления выберите пункт <strong> пакеты для </strong> &gt; <strong> групп соединений </strong> .</p></li>
<li><p>Выберите нужную группу подключений в библиотеке групп соединений.</p></li>
<li><p>Нажмите кнопку <strong> изменить </strong> в области подключенные пакеты.</p></li>
<li><p>Установите флажок <strong> использовать любую версию </strong> рядом с названием пакета и нажмите кнопку <strong> применить </strong> .</p></li>
</ol>
<p>Дополнительные сведения о добавлении и обновлении пакетов можно найти <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)"> в разделе Добавление и обновление пакетов с помощью консоли управления </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Клиент App-V на отдельном компьютере</p></td>
<td align="left"><ol>
<li><p>Создайте XML-документ группы подключения.</p></li>
<li><p>Чтобы обновить пакет, задайте <strong> </strong> для атрибутау Tag пакета <strong> VersionID </strong> звездочку ( <strong>*</strong> ).</p></li>
<li><p>С помощью следующего командлета добавьте группу подключения и укажите путь к XML-документу группы подключения.</p>
<p><strong>Add-AppvClientConnectionGroup</strong></p></li>
<li><p>При обновлении пакета используйте следующие командлеты, чтобы удалить старый пакет, добавить обновленный пакет и опубликовать обновленный пакет.</p>
<ul>
<li><p>RemoveAppvClientPackage</p></li>
<li><p>Add-AppvClientPackage</p></li>
<li><p>Publish-AppvClientPackage</p></li>
</ul></li>
</ol>
<p>Дополнительные сведения см. в следующих разделах:</p>
<ul>
<li><p>Пример XML-файла, <strong> XML-файла группы подключения с дополнительными пакетами </strong> , в этом разделе: <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"> использование необязательных пакетов в группах соединений</a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">Управление пакетами App-V 5.0, работающими на автономном компьютере, с помощью PowerShell</a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## Статьи по теме


[Управление связывающими группами](managing-connection-groups.md)

 

 





