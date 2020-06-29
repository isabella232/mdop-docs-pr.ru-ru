---
title: Требования к системе при работе с Application Virtualization
description: Требования к системе при работе с Application Virtualization
author: dansimp
ms.assetid: a2798dd9-168e-45eb-8103-e12e128fae7c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c160a7532b521bb41570b419b22b9e7daaec2987
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819519"
---
# Требования к системе при работе с Application Virtualization


В этой статье описаны минимальные требования к оборудованию и программному обеспечению для сервера управления Microsoft Application Virtualization (App-V) и потокового сервера.

## Управление виртуализацией приложений и потоковые серверы


В следующем списке приведены минимальные рекомендуемые требования к оборудованию и программному обеспечению для сервера управления App-V и потокового сервера App-V.

### Требования к оборудованию

-   Процессор — Intel Pentium III, 1 ГГц

-   ОЗУ (512 МБ)

-   Место на диске — 200 МБАЙТ свободного места на жестком диске, не включая каталог содержимого

### Требования к программному обеспечению

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows server2003</p></td>
<td align="left"><p>Стандартный выпуск</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows server2003</p></td>
<td align="left"><p>Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows server2003 R2</p></td>
<td align="left"><p>Стандартный выпуск</p></td>
<td align="left"><p>Нет пакета обновления или пакета обновления 2 (SP2)</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows server2003 R2</p></td>
<td align="left"><p>Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p>Нет пакета обновления или пакета обновления 2 (SP2)</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ относится только к App-V 4,5 SP1 и SP2.

## Хранилище данных


В следующем списке приведены минимальные рекомендуемые требования к оборудованию и программному обеспечению для компьютера, который используется при установке хранилища данных на отдельном сервере. Хранилище данных является обязательным только для сервера управления виртуализацией приложений.

### Требования к оборудованию

-   Процессор – процессор Intel Pentium III, 850 МГц

-   ОЗУ (512 МБ)

-   Место на диске — 200 МБАЙТ свободного места на жестком диске

### Требования к программному обеспечению

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows server2003</p></td>
<td align="left"><p>Стандартный выпуск</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows server2003</p></td>
<td align="left"><p>Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows server2003 R2</p></td>
<td align="left"><p>Стандартный выпуск</p></td>
<td align="left"><p>Нет пакета обновления или пакета обновления 2 (SP2)</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows server2003 R2</p></td>
<td align="left"><p>Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p>Нет пакета обновления или пакета обновления 2 (SP2)</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ относится только к App-V 4,5 SP1 и SP2.

-   Database (Microsoft SQL Server2000 SP3a или SP4, SQL Server2005 SP1, SP2 или SP3 или SQL Server2008, без пакета обновления или пакета обновления 1 или SQL Server2008 R2 (32-разрядная или 64-разр.)

-   Компоненты доступа к данным Microsoft — MDAC 2,7

-   Контроллер домена — Доменные службы Active Directory или основной контроллер домена Windows NT 4.0 (PDC) в качестве центра централизованной проверки подлинности.

## Веб-служба управления


В следующем списке приведены минимальные рекомендуемые требования к оборудованию и программному обеспечению для веб-службы управления виртуализацией приложений, установленной на отдельном компьютере.

### Требования к оборудованию

-   Процессор – процессор Intel Pentium III, 800 МГц

-   ОЗУ — 256 МБ

-   Место на диске — 50 МБАЙТ свободного места на жестком диске

### Требования к программному обеспечению

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows server2003</p></td>
<td align="left"><p>Стандартный выпуск</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows server2003</p></td>
<td align="left"><p>Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows server2003 R2</p></td>
<td align="left"><p>Стандартный выпуск</p></td>
<td align="left"><p>Нет пакета обновления или пакета обновления 2 (SP2)</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows server2003 R2</p></td>
<td align="left"><p>Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p>Нет пакета обновления или пакета обновления 2 (SP2)</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ относится только к App-V 4,5 SP1 и SP2.

-   Информационные службы Интернета (IIS) 6,0, настроенные с помощью Microsoft ASP.NET, IIS 7

-   Microsoft .NET Framework 2.0

## Консоль управления


В следующем списке приведены минимальные рекомендуемые требования к оборудованию и программному обеспечению для консоли управления виртуализацией приложений при установке на отдельном компьютере.

### Требования к оборудованию

-   Процессор – процессор Intel Pentium III, 450 МГц

-   ОЗУ — 256 МБ

-   Место на диске — 200 МБАЙТ свободного места на жестком диске

### Требования к программному обеспечению

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Профессиональный выпуск</p></td>
<td align="left"><p>SP2 или 3 (SP3)</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Бизнес, Корпоративная или максимальная выпускная версия</p></td>
<td align="left"><p>Пакет обновления, пакет обновления 1 (SP1) или пакет обновления 2 (SP2)</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Профессиональная, Корпоративная или Максимальная версия</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows server2003</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p>Нет пакета обновления или пакета обновления 2 (SP2)</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ относится только к App-V 4,5 SP1 и SP2.

-   Консоль управления (MMC) 3.0 или более поздней версии

-   Microsoft .NET Framework 2.0 (минимум)

    **Важно!**  Минимальным требованием является .NET Framework 2,0 с пакетом обновления 2 (SP2), если необходимо установить исправление App-V KB980850 или последующие исправления App-V на компьютере, на котором запущена консоль управления App-V.

     

## Статьи по теме


[Требования клиента Application Virtualization к оборудованию и программному обеспечению](application-virtualization-client-hardware-and-software-requirements.md)

[Требования программы Application Virtualization Sequencer к оборудованию и программному обеспечению](application-virtualization-sequencer-hardware-and-software-requirements.md)

[Настройка серверов для развертывания на основе сервера](how-to-configure-servers-for-server-based-deployment.md)

[Установка серверов и компонентов системы](how-to-install-the-servers-and-system-components.md)

[Обновление серверов и компонентов системы](how-to-upgrade-the-servers-and-system-components.md)

 

 





