---
title: Контрольный список пост-установки App-V
description: Контрольный список пост-установки App-V
author: dansimp
ms.assetid: 74db297e-a744-4287-bcc6-0e096ca8b57a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79728bd2043076b20eb37ba0b1fa6f834a0d94bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819802"
---
# Контрольный список пост-установки App-V


В приведенном ниже контрольном списке представлен высокоуровневый список элементов, которые необходимо учитывать и описаны действия, которые необходимо выполнить после установки сервера управления Microsoft Application Virtualization (App-V), потокового сервера App-V и настольного клиента App-V.

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
<td align="left"><p>Создание исключений брандмауэра для серверного сервера управления App-V или служб потокового сервера.</p></td>
<td align="left"><p><a href="configuring-the-firewall-for-the-app-v-servers.md" data-raw-source="[Configuring the Firewall for the App-V Servers](configuring-the-firewall-for-the-app-v-servers.md)">Настройка брандмауэра для серверов App-V Server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Убедитесь, что система App-V работает правильно, публикуя, проstreaming и проверяя приложение по умолчанию.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-the-default-application.md" data-raw-source="[How to Install and Configure the Default Application](how-to-install-and-configure-the-default-application.md)">Установка и настройка приложения по умолчанию</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Настройте клиент App-V на использование потокового сервера App-V или другого сервера для потоковой передачи данных с помощью <strong> </strong> параметров APPLICATIONSOURCEROOT, <strong> IconSourceRoot </strong> и <strong> OSDSourceRoot </strong> .</p></td>
<td align="left"><p><a href="how-to-configure-the-client-for-application-package-retrieval.md" data-raw-source="[How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md)">Настройка клиента для получения пакетов приложений</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Узнайте, как использовать файл. msi для упорядоченных пакетов приложений для автономного развертывания.</p></td>
<td align="left"><p><a href="how-to-publish-a-virtual-application-on-the-client.md" data-raw-source="[How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md)">Публикация виртуального приложения на клиенте</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Необязательно Настройте зеркальное отображение базы данных SQL Server для базы данных App-V.</p></td>
<td align="left"><p><a href="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md" data-raw-source="[How to Configure Microsoft SQL Server Mirroring Support for App-V](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)">Настройка поддержки зеркального отображения Microsoft SQL Server для App-V</a></p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Контрольные списки развертывания и обновления Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





