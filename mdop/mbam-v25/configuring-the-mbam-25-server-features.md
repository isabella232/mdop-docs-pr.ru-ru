---
title: Настройка компонентов сервера MBAM 2.5 Server
description: Настройка компонентов сервера MBAM 2.5 Server
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823059"
---
# Настройка компонентов сервера MBAM 2.5 Server


Используйте эти сведения в качестве начального места для настройки функций администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5 после [установки серверного программного обеспечения MBAM 2,5](installing-the-mbam-25-server-software.md). Для настройки MBAM можно использовать два способа:

-   Мастер настройки сервера MBAM

-   Командлеты Windows PowerShell

## Прежде чем приступить к настройке функций сервера MBAM


Прежде чем приступить к настройке функций сервера MBAM, ознакомьтесь с приведенными ниже инструкциями и выполните следующие действия.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Шаг</th>
<th align="left">Где найти инструкции</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Изучите рекомендованную архитектуру для MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Высокоуровневая архитектура для MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Проверка поддерживаемых конфигураций для MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Поддерживаемые конфигурации MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Заполните необходимые условия на каждом сервере.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Установка программного обеспечения сервера MBAM на каждый сервер, на котором будет настроена функция сервера MBAM.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Установка программного обеспечения MBAM 2.5 Server</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ознакомьтесь с требованиями для настройки функций сервера MBAM с помощью Windows PowerShell (если вы используете этот метод для настройки MBAM функций сервера).</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>

 

## Инструкции по настройке функций сервера MBAM


В каждой строке в следующей таблице описаны возможности, которые будут настраиваться на отдельном сервере в соответствии с рекомендованной [высокоуровневой архитектурой для MBAM 2,5](high-level-architecture-for-mbam-25.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Устанавливаемые компоненты</th>
<th align="left">Где найти инструкции</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Настройте базы данных.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Настройка баз данных MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Настройте отчеты.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Настройка отчетов MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Настройте веб-приложения.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Настройка веб-приложений MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Настройка интеграции System Center Configuration Manager (если применимо).</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Настройка интеграции System Center Configuration Manager с MBAM 2.5</a></p></td>
</tr>
</tbody>
</table>

 

Список событий, посвященных настройке компонентов сервера MBAM, можно найти в разделе [журналы событий сервера](server-event-logs.md).



## Статьи по теме


Настройка компонентов сервера MBAM 2.5 Server
 

 
## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




