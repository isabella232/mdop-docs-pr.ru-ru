---
title: Поддерживаемые конфигурации App-V 5.0 с пакетом обновления 3 (SP3)
description: Поддерживаемые конфигурации App-V 5.0 с пакетом обновления 3 (SP3)
author: dansimp
ms.assetid: 08ced79a-0ed3-43c3-82e7-de01c1f33e81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b5a8858c703add3dc84c7eed4f62aa97e60ec9b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814792"
---
# Поддерживаемые конфигурации App-V 5.0 с пакетом обновления 3 (SP3)


В этой статье указаны требования для установки и запуска Microsoft Application Virtualization (App-V) 5,0 SP3 в среде.

## Требования к системе для App-V Server


В этом разделе перечислены требования к операционной системе и оборудованию для всех серверных компонентов App-V.

### Неподдерживаемые сценарии сервера App-V 5,0 SP3

Сервер App-V 5,0 с пакетом обновления 3 (SP3) не поддерживает указанные ниже сценарии.

-   Развертывание на компьютере, на котором запущен Microsoft Windows Server Core.

-   Развертывание на компьютере, на котором установлена предыдущая версия App-V 5,0 SP3. Вы можете установить приложение App-V 5,0 SP3 рядом с сервером App-V 4.5 облегченного потокового сервера (LWS). Развертывание App-V на стороне с сервером (серверная служба управления виртуализацией приложений для App-V 4,5) не поддерживается.

-   Развертывание на компьютере, на котором запущен Microsoft SQL Server, Экспресс-выпуск.

-   Удаленное развертывание базы данных сервера управления или базы данных отчетов. Вы должны запустить установщик прямо на компьютере, на котором установлен Microsoft SQL Server.

-   Развертывание на контроллере домена.

-   Короткие пути. Если вы планируете использовать короткий путь, вы должны создать новый том.

### Требования к операционной системе для сервера управления

В таблице ниже перечислены операционные системы, которые поддерживаются в установке сервера управления App-V 5,0 SP3.

**Примечание**  Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления. Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975). Дополнительные сведения о [политике поддержки жизненного цикла поддержки Майкрософт приведены в разделе вопросы и ответы](https://go.microsoft.com/fwlink/p/?LinkId=31976) .

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>

 

**Важно!**  Развертывание роли сервера управления на компьютере с включенным удаленным доступом к рабочему столу не поддерживается.

 

### <a href="" id="management-server-hardware-requirements-"></a>Требования к оборудованию сервера управления

-   Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор

-   ОЗУ — 1 ГБ ОЗУ (64-разр.)

-   Место на диске — 200 МБАЙТ свободного места на жестком диске, не включая каталог содержимого

### Требования к базам данных сервера управления

В следующей таблице перечислены версии SQL Server, которые поддерживаются при установке App-V 5,0 с пакетом обновления 3 (SP3).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Версия SQL Server</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>ОБНОВЛЕНИЙ</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
</tbody>
</table>

 

### Требования к операционной системе сервера публикаций

В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера App-V 5,0 с пакетом обновления 3 (SP3).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="publishing-server-hardware-requirements-"></a>Требования к оборудованию сервера публикаций

Приложение App-V не добавляет никаких дополнительных требований за пределы Windows Server.

-   Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор

-   ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)

-   Место на диске — 200 МБАЙТ свободного места на жестком диске, не включая каталог содержимого

### Требования к операционной системе сервера отчетов

В таблице ниже перечислены операционные системы, которые поддерживаются в установке сервера отчетов App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="reporting-server-hardware-requirements-"></a>Требования к оборудованию сервера отчетов

Приложение App-V не добавляет никаких дополнительных требований за пределы Windows Server.

-   Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор

-   ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)

-   Место на диске — 200 МБАЙТ свободного места на жестком диске

### Требования к базам данных сервера отчетов

В следующей таблице перечислены версии SQL Server, которые поддерживаются при установке приложения Database-V 5,0 с базой данных для создания отчетов.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Версия SQL Server</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>ОБНОВЛЕНИЙ</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a>Требования к системе для клиента App-V


В таблице ниже перечислены операционные системы, которые поддерживаются при установке клиента App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
</tbody>
</table>

 

Следующие сценарии установки клиента App-V не поддерживаются, за исключением случаев, указанных ниже.

-   Компьютеры под управлением Windows Server

-   Компьютеры, на которых выполняется приложение App-V 4.6 SP1 или более ранние версии

-   Клиент служб удаленных рабочих столов App-V 5,0 (SP3) поддерживается только для серверов с поддержкой RDS

### <a href="" id="app-v-client-hardware-requirements-"></a>Требования к оборудованию клиента App-V

Ниже приведен список поддерживаемых конфигураций оборудования для установки клиента App-V 5,0 SP3.

-   Процессор — процессор с тактовой частотой 1,4 ГГц или более 32 мощный (x86) или 64-bit (x64)

-   ОЗУ — 1 ГБ (32-разрядная версия) или 2 ГБ (64-разр.)

-   Диск — 100 МБАЙТ для установки, не включая пространство на диске, используемое виртуализированными приложениями.

## Требования к клиентским системам служб удаленных рабочих столов


В таблице ниже перечислены операционные системы, которые поддерживаются в установке клиента служб удаленных рабочих столов для App-V 5,0 SP3 (RDS).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>

 

### Требования к оборудованию клиента служб удаленных рабочих столов

Приложение App-V не добавляет никаких дополнительных требований за пределы Windows Server.

-   Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор

-   ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)

-   Место на диске — 200 МБАЙТ свободного места на жестком диске

## Требования к системе Sequencer


В таблице ниже перечислены операционные системы, которые поддерживаются при установке App-V 5,0 с пакетом обновления 3 (SP3).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server2012 R2</p></td>
<td align="left"></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- и 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- и 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32- и 64-разрядная</p></td>
</tr>
</tbody>
</table>

 

### Требования к оборудованию Sequencer

Требования к оборудованию приведены в документации по Windows или Windows Server. Приложение App-V добавляет дополнительные требования к оборудованию.

## <a href="" id="bkmk-supp-ver-sccm"></a>Поддерживаемые версии System Center Configuration Manager


Клиент App-V поддерживает следующие версии System Center Configuration Manager:

-   MicrosoftSystemCenter2012 ConfigurationManager

-   System Center 2012 R2 Configuration Manager

-   System Center 2012 R2 Configuration Manager с пакетом обновления 1 (SP1)

Дополнительные сведения о том, как Configuration Manager интегрируется с App-V, можно найти в разделе [Планирование интеграции App-v с Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).






## Статьи по теме


[Планирование развертывания App-V](planning-to-deploy-app-v.md)

[Необходимые условия для App-V 5.0 с пакетом обновления 3 (SP3)](app-v-50-sp3-prerequisites.md)

 

 





