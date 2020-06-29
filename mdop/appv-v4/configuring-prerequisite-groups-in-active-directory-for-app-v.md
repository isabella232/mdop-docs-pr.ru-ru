---
title: Настройка необходимых групп в Active Directory для App-V
description: Настройка необходимых групп в Active Directory для App-V
author: dansimp
ms.assetid: 0010d534-46c0-44a3-b5c1-621b4d5e2c31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa1ab6393dee20203b715311d4e1dfdc4c22c679
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821862"
---
# Настройка необходимых групп в Active Directory для App-V


Перед установкой сервера управления Microsoft Application Virtualization (App-V) необходимо создать в Active Directory следующие объекты. Приложение App-V использует группы Active Directory для управления доступом к приложениям и административными функциями. Эти группы будут использоваться в процессе установки сервера и при публикации приложений.

## Настройка предварительных групп в службе каталогов Active Directory для виртуализации приложений


В этой таблице перечислены группы Active Directory, необходимые для установки приложения App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Объект</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Организационное подразделение (OU)</p></td>
<td align="left"><p>Создайте подразделение в службе каталогов Active Directory для конкретных групп, необходимых для App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Административная группа App-V</p></td>
<td align="left"><p>Во время установки сервера управления App-V необходимо выбрать группу Active Directory, которая будет использоваться в качестве группы администраторов App-V для управления административным доступом к консоли управления. Создайте группу безопасности для администраторов App-V и добавьте в эту группу всех пользователей, которые должны использовать консоль управления. Вы не можете создать эту группу непосредственно из установщика сервера управления App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Группа пользователей App-V</p></td>
<td align="left"><p>Для App-V требуется, чтобы все учетные записи пользователей, которые обращаются к функциям App-V, были членами политики поставщика, связанной с одной группой, для общего доступа к платформе. Использование существующей группы; Например, пользователи домена, если все пользователи должны иметь доступ к приложению App-V, или создать новую группу.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Группы приложений</p></td>
<td align="left"><p>App-V связывает право на использование отдельного приложения с группой Active Directory. Создавайте группы Active Directory для каждого приложения и назначайте пользователей этим группам, чтобы управлять доступом пользователей к приложениям.</p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Требования при развертывании Application Virtualization](application-virtualization-deployment-requirements.md)

[Настройка Windows Server 2008 для серверов App-V Management Server](how-to-configure-windows-server-2008-for-app-v-management-servers.md)

 

 





