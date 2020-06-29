---
title: Контрольный список установки App-V
description: Контрольный список установки App-V
author: dansimp
ms.assetid: b17efaab-cd6d-4c30-beb7-c6e7c9c87657
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d6d83ac465a7e48dd35bd2fe966c3c51be24c96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819812"
---
# Контрольный список установки App-V


Приведенный ниже контрольный список предназначен для создания высокоуровневого списка элементов, которые необходимо учитывать, и подробно описанных действий, которые необходимо предпринять, чтобы установить серверы Microsoft Application Virtualization (App-V).

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
<td align="left"><p>Установите сервер управления App-V. Если вы устанавливаете веб-службу управления, консоль управления или хранилище данных на разных серверах, вы можете воспользоваться параметром выборочной установки.</p></td>
<td align="left"><p><a href="how-to-install-application-virtualization-management-server.md" data-raw-source="[How to Install Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)">Установка сервера Application Virtualization Management Server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Установите веб-службу управления App-V. (Опционально ¹)</p></td>
<td align="left"><p><a href="how-to-install-the-management-web-service.md" data-raw-source="[How to Install the Management Web Service](how-to-install-the-management-web-service.md)">Установка веб-службы управления</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Установите консоль управления App-V. (Опционально ¹)</p></td>
<td align="left"><p><a href="how-to-install-the-management-console.md" data-raw-source="[How to Install the Management Console](how-to-install-the-management-console.md)">Установка консоли управления</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Установите хранилище данных App-V. (Опционально ¹)</p></td>
<td align="left"><p><a href="how-to-install-a-database.md" data-raw-source="[How to Install a Database](how-to-install-a-database.md)">Установка базы данных</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Установите клиент App-V.</p></td>
<td align="left"><p><a href="how-to-manually-install-the-application-virtualization-client.md" data-raw-source="[How to Manually Install the Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)">Установка клиента Application Virtualization Client вручную</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Установка секвенсора App-V.</p></td>
<td align="left"><p><a href="how-to-install-the-application-virtualization-sequencer.md" data-raw-source="[How to Install the Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md)">Установка программы Application Virtualization Sequencer</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Установите потоковый сервер App-V. (Это необязательно и требуется только при установке потокового сервера).</p></td>
<td align="left"><p><a href="how-to-install-the-application-virtualization-streaming-server.md" data-raw-source="[How to Install the Application Virtualization Streaming Server](how-to-install-the-application-virtualization-streaming-server.md)">Установка сервера потоковой передачи Application Virtualization Streaming Server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Создавайте каталоги содержимого на серверах, которые будут использоваться для потоковой передачи приложений на компьютеры пользователей.</p></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">Настройка серверов Application Virtualization Management Server</a></p>
<p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)">Настройка серверов Application Virtualization Streaming Server</a></p>
<p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)">Настройка сервера для служб IIS</a></p>
<p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)">Настройка файлового сервера</a></p></td>
</tr>
</tbody>
</table>

 

¹ этот параметр требуется только в том случае, если вы устанавливаете веб-службу управления App-V, консоль управления или хранилище данных на другом компьютере.

## Статьи по теме


[Контрольные списки развертывания и обновления Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

[Контрольный список пост-установки App-V](app-v-postinstallation-checklist.md)

 

 





