---
title: Контрольный список подготовки к установке App-V
description: Контрольный список подготовки к установке App-V
author: dansimp
ms.assetid: 3af609b1-2c09-4edb-b083-b913b6d5e8c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 70e71d3dea02daeadedb4cff78c58302ac743dda
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819789"
---
# Контрольный список подготовки к установке App-V


Приведенный ниже контрольный список предназначен для того, чтобы создать высокоуровневый список элементов, которые необходимо принять, и ознакомиться с действиями, которые необходимо выполнить перед установкой серверов Microsoft Application Virtualization (App-V).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Шаг</th>
<th align="left">Справочные материалы</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Убедитесь в том, что ваша вычислительная среда соответствует поддерживаемым настройкам для App-V.</p></td>
<td align="left"><p><a href="application-virtualization-deployment-requirements.md" data-raw-source="[Application Virtualization Deployment Requirements](application-virtualization-deployment-requirements.md)">Требования при развертывании Application Virtualization</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Настройте необходимые группы и учетные записи Active Directory.</p></td>
<td align="left"><p><a href="configuring-prerequisite-groups-in-active-directory-for-app-v.md" data-raw-source="[Configuring Prerequisite Groups in Active Directory for App-V](configuring-prerequisite-groups-in-active-directory-for-app-v.md)">Настройка необходимых групп в Active Directory для App-V</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Настройте параметры информационных служб Интернета (IIS) на сервере, на котором запущены службы IIS.</p></td>
<td align="left"><p><a href="how-to-configure-windows-server-2008-for-app-v-management-servers.md" data-raw-source="[How to Configure Windows Server 2008 for App-V Management Servers](how-to-configure-windows-server-2008-for-app-v-management-servers.md)">Настройка Windows Server 2008 для серверов App-V Management Server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Настройте сервер, на котором выполняются службы IIS, как доверенный для делегирования.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Это необходимо только в том случае, если установка сервера управления App-V выполняется с помощью распределенной архитектуры системы, то есть при установке консоли управления App-V, веб-службы управления и базы данных на разных компьютерах.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-configure-the-server-to-be-trusted-for-delegation.md" data-raw-source="[How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)">Настройка сервера для разрешения делегирования</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Установите Microsoft SQL Server 2008.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="[Install SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=181924)">Установите SQL Server 2008 </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924"> https://go.microsoft.com/fwlink/?LinkId=181924 </a> ).</p></td>
</tr>
</tbody>
</table>



## Статьи по теме


[Контрольные списки развертывания и обновления Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

[Контрольный список установки App-V](app-v-installation-checklist.md)









