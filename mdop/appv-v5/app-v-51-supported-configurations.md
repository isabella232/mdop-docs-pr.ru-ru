---
title: Поддерживаемые конфигурации в App-V 5.1
description: Поддерживаемые конфигурации в App-V 5.1
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814725"
---
# Поддерживаемые конфигурации в App-V 5.1

>Применимо к Windows 10 версии 1607; Window Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (расширенная обновление для системы безопасности)

В этой статье указаны требования для установки и запуска Microsoft Application Virtualization (App-V) 5,1 в среде.

## Требования к системе для App-V Server

В этом разделе перечислены требования к операционной системе и оборудованию для всех серверных компонентов App-V.

### Неподдерживаемые серверные сценарии App-V 5,1

Сервер App-V 5,1 не поддерживает указанные ниже сценарии.

-   Развертывание на компьютере, на котором запущен Microsoft Windows Server Core.

-   Развертывание на компьютере, на котором установлена предыдущая версия App-V 5,1 Server. Приложение App-V 5,1 можно установить рядом с сервером App-V 4.5 облегченного потокового сервера (LWS). Развертывание App-V на стороне с сервером (серверная служба управления виртуализацией приложений для App-V 4,5) не поддерживается.

-   Развертывание на компьютере, на котором запущен Microsoft SQL Server, Экспресс-выпуск.

-   Развертывание на контроллере домена.

-   Короткие пути. Если вы планируете использовать короткий путь, вы должны создать новый том.

### Требования к операционной системе для сервера управления

В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера управления App-V 5,1.

> [!NOTE]
> Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления. Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975). Дополнительные сведения о [политике поддержки жизненного цикла поддержки Майкрософт приведены в разделе вопросы и ответы](https://go.microsoft.com/fwlink/p/?LinkId=31976) .

 | Операционная система                 | Пакет обновления | Системная архитектура |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64-разрядная       |
| Microsoft Windows Server 2016    |              |        64-разрядная       |
| Microsoft Windows Server 2012 R2 |              |        64-разрядная       |
| Microsoft Windows Server 2012    |              |        64-разрядная       |
| [Расширенное обновление для системы безопасности](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2|      SP1     |        64-разрядная       |
 

**Важно!**  Развертывание роли сервера управления на компьютере с включенным удаленным доступом к рабочему столу не поддерживается.

 

### <a href="" id="management-server-hardware-requirements-"></a>Требования к оборудованию сервера управления

-   Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор

-   ОЗУ — 1 ГБ ОЗУ (64-разр.)

-   Место на диске — 200 МБАЙТ свободного места на жестком диске, не включая каталог содержимого

### Требования к базам данных сервера управления

В следующей таблице перечислены версии SQL Server, которые поддерживаются при установке базы данных управления App-V 5,1.

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
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2019</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>SP2</p></td>
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

Дополнительные сведения о файлах конфигурации пользователей в SQL Server 2016 и более поздних версиях можно найти в [статье поддержка](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).

### Требования к операционной системе сервера публикаций

В таблице ниже перечислены операционные системы, которые поддерживаются в установке сервера публикаций App-V 5,1.

| Операционная система                 | Пакет обновления | Системная архитектура |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64-разрядная       |
| Microsoft Windows Server 2016    |              |        64-разрядная       |
| Microsoft Windows Server 2012 R2 |              |        64-разрядная       |
| Microsoft Windows Server 2012    |              |        64-разрядная       |
| [Расширенное обновление для системы безопасности](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2 |      SP1     |        64-разрядная       |

### <a href="" id="publishing-server-hardware-requirements-"></a>Требования к оборудованию сервера публикаций

Приложение App-V не добавляет никаких дополнительных требований за пределы Windows Server.

-   Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор

-   ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)

-   Место на диске — 200 МБАЙТ свободного места на жестком диске, не включая каталог содержимого

### Требования к операционной системе сервера отчетов

В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера Reporting Server App-V 5,1.

| Операционная система                 | Пакет обновления | Системная архитектура |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64-разрядная       |
| Microsoft Windows Server 2016    |              |        64-разрядная       |
| Microsoft Windows Server 2012 R2 |              |        64-разрядная       |
| Microsoft Windows Server 2012    |              |        64-разрядная       |
| [Расширенное обновление для системы безопасности](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2 |      SP1     |        64-разрядная       |

### <a href="" id="reporting-server-hardware-requirements-"></a>Требования к оборудованию сервера отчетов

Приложение App-V не добавляет никаких дополнительных требований за пределы Windows Server.

-   Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор

-   ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)

-   Место на диске — 200 МБАЙТ свободного места на жестком диске

### Требования к базам данных сервера отчетов

В приведенной ниже таблице указаны версии SQL Server, которые поддерживаются при установке базы данных Reporting App-V 5,1.

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
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>SP2</p></td>
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

В таблице ниже перечислены операционные системы, которые поддерживаются при установке клиента App-V 5,1.

> [!NOTE]
> С выпуском годовщины Windows 10 (версия 1607) клиент App-V входит в комплект и будет блокировать установку любой предыдущей версии клиента App-V.

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
<td align="left"><p>Microsoft Windows10 (версия до 1607)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8.1</p></td>
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

-   Клиент служб удаленных рабочих столов App-V 5,1 поддерживается только для серверов с поддержкой служб удаленных рабочих столов.

### <a href="" id="app-v-client-hardware-requirements-"></a>Требования к оборудованию клиента App-V

В списке ниже показана конфигурация оборудования, поддерживаемая установкой клиента App-V 5,1.

-   Процессор — процессор с тактовой частотой 1,4 ГГц или более 32 мощный (x86) или 64-bit (x64)

-   ОЗУ — 1 ГБ (32-разрядная версия) или 2 ГБ (64-разр.)

-   Диск — 100 МБАЙТ для установки, не включая пространство на диске, используемое виртуализированными приложениями.

## Требования к клиентским системам служб удаленных рабочих столов


В следующей таблице перечислены операционные системы, которые поддерживаются при установке клиента служб удаленных рабочих столов App-V 5,1 (RDS).

| Операционная система                 | Пакет обновления | Системная архитектура |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64-разрядная       |
| Microsoft Windows Server 2016    |              |        64-разрядная       |
| Microsoft Windows Server 2012 R2 |              |        64-разрядная       |
| Microsoft Windows Server 2012    |              |        64-разрядная       |
| [Расширенное обновление для системы безопасности](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2 |      SP1     |        64-разрядная       |

### Требования к оборудованию клиента служб удаленных рабочих столов

Приложение App-V не добавляет никаких дополнительных требований за пределы Windows Server.

-   Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор

-   ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)

-   Место на диске — 200 МБАЙТ свободного места на жестком диске

## Требования к системе Sequencer

В следующей таблице перечислены операционные системы, которые поддерживаются при установке App-V 5,1 Sequencer.

| Операционная система                 | Пакет обновления | Системная архитектура |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64-разрядная       |
| Microsoft Windows Server 2016    |              |        64-разрядная       |
| Microsoft Windows Server 2012 R2 |              |        64-разрядная       |
| Microsoft Windows Server 2012    |              |        64-разрядная       |
| [Расширенное обновление для системы безопасности](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2 |      SP1     |        64-разрядная       |
| Microsoft Windows 10             |              | 32- и 64-разрядная   |
| Microsoft Windows 8,1            |              | 32- и 64-разрядная   |
| Microsoft Windows 7              |      SP1     | 32- и 64-разрядная   |

### Требования к оборудованию Sequencer

Требования к оборудованию приведены в документации по Windows или Windows Server. Приложение App-V добавляет дополнительные требования к оборудованию.

## <a href="" id="bkmk-supp-ver-sccm"></a>Поддерживаемые версии System Center Configuration Manager

Клиент App-V поддерживает следующие версии System Center Configuration Manager:

-   MicrosoftSystemCenter2012 ConfigurationManager

-   System Center 2012 R2 Configuration Manager

-   System Center 2012 R2 Configuration Manager с пакетом обновления 1 (SP1)

В следующей матрице версий App-V и System Center Configuration Manager показаны все официально поддерживаемые комбинации App-V и Configuration Manager.

> [!NOTE]
> Приложение App-V 4,5 и 4,6 успешно завершило работу базовой поддержки.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Версия App-V</th>
<th align="left">System Center Configuration Manager 2007</th>
<th align="left">System Center 2012 Configuration Manager</th>
<th align="left">System Center 2012 Configuration Manager с пакетом обновления 1 (SP1)</th>
<th align="left">System Center 2012 R2 Configuration Manager</th>
<th align="left">System Center 2012 R2 Configuration Manager с пакетом обновления 1 (SP1)</th>
<th align="left">System Center 2012 Configuration Manager с пакетом обновления 2 (SP2)</th>
<th align="left">System Center Configuration Manager версии 1511</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 с пакетом обновления 3 (SP3)</p></td>
<td align="left"><p>Только обертки MSI</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>2012 SP1 НАКОПИТЕЛЬНЫМ</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5.1</p></td>
<td align="left"><p>Только обертки MSI</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>2012 SP1 НАКОПИТЕЛЬНЫМ</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
</tbody>
</table>

 

Дополнительные сведения о том, как Configuration Manager интегрируется с App-V, можно найти в разделе [Планирование интеграции App-v с Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).

## Статьи по теме

[Планирование развертывания App-V](planning-to-deploy-app-v51.md)

[Предварительные требования App-V 5.1](app-v-51-prerequisites.md)
