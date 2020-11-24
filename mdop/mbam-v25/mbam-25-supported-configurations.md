---
title: Поддерживаемые конфигурации MBAM 2.5
description: Поддерживаемые конфигурации MBAM 2.5
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 8ed7915e33c5e4735a7c58674ed5f7d6da8e9a06
ms.sourcegitcommit: 9087f0a1b5bd3f81a9b790d5e39fdf39c18a2411
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2020
ms.locfileid: "11182931"
---
# Поддерживаемые конфигурации MBAM 2.5


Вы можете выполнить администрирование и мониторинг Microsoft BitLocker (MBAM) 2,5 в изолированной топологии или в топологии интеграции Configuration Manager, которая интегрирует MBAM с System Center Configuration Manager. Если вы используете рекомендуемую конфигурацию для любой топологии в рабочей среде, MBAM поддерживает до 500 000 MBAM клиентов. Сведения о рекомендуемой архитектуре и функциональных возможностях, которые настроены на каждом сервере для каждой топологии, можно найти в разделе [архитектура высокого уровня для MBAM 2,5](high-level-architecture-for-mbam-25.md).

Дополнительные конфигурации, специфичные для топологии интеграции Configuration Manager, приведены в разделе [версии Configuration Manager, которые MBAM поддерживаются](#bkmk-cm-ramreqs).

**Примечание.**  
Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления. Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975). Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.



## Языки, поддерживаемые MBAM


В приведенных ниже таблицах показаны языки, которые поддерживаются клиентом MBAM (включая портал Self-Service) и сервер MBAM в MBAM 2,5 и MBAM 2,5 SP1.

**Поддерживаемые языки в MBAM 2,5 с пакетом обновления 1 (SP1):**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Языки клиента</th>
<th align="left">Языки сервера</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Чешский (Чешская Республика) cs-CZ</p>
<p>Датский (Дания) da-DK</p>
<p>Нидерландский (Нидерланды) nl-NL</p>
<p>Английский (США) EN-US</p>
<p>Финский (Финляндия) Fi-FI</p>
<p>Французский (Франция) fr-FR</p>
<p>Немецкий (Германия) de-DE</p>
<p>Греческий (Греция) Эль-GR</p>
<p>Венгерский (Венгрия) hu-HU</p>
<p>Итальянский (Италия) IT-IT</p>
<p>Японский (Япония) ja-JP</p>
<p>Корейский (Корея) ko-KR</p>
<p>Норвежский (букмол, Норвегия) без датаграмм</p>
<p>Польский (Польша) PL-PL</p>
<p>Португальский (Бразилия) Пт — BR</p>
<p>Португальский (Португалия), пт</p>
<p>Русский (Россия) ru-RU</p>
<p>Словацкий (Словакия) sk-SK</p>
<p>Испанский (Испания) ES-ES</p>
<p>Шведский (Швеция) SV-SE</p>
<p>Турецкий (Турция) tr-TR</p>
<p>Словенский (Словения) SL-SI</p>
<p>Упрощенный китайский (КНР) zh-CN</p>
<p>Китайский (традиционное письмо, Тайвань) zh-TW</p></td>
<td align="left"><ul>
<li><p>Английский (США) EN-US</p></li>
<li><p>Французский (Франция) fr-FR</p></li>
<li><p>Немецкий (Германия) de-DE</p></li>
<li><p>Итальянский (Италия) IT-IT</p></li>
<li><p>Японский (Япония) ja-JP</p></li>
<li><p>Корейский (Корея) ko-KR</p></li>
<li><p>Португальский (Бразилия) Пт — BR</p></li>
<li><p>Русский (Россия) ru-RU</p></li>
<li><p>Испанский (Испания) ES-ES</p></li>
<li><p>Упрощенный китайский (КНР) zh-CN</p></li>
<li><p>Китайский (традиционное письмо, Тайвань) zh-TW</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Поддерживаемые языки в MBAM 2,5:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Языки клиента</th>
<th align="left">Языки сервера</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>Английский (США) EN-US</p></li>
<li><p>Французский (Франция) fr-FR</p></li>
<li><p>Немецкий (Германия) de-DE</p></li>
<li><p>Итальянский (Италия) IT-IT</p></li>
<li><p>Японский (Япония) ja-JP</p></li>
<li><p>Корейский (Корея) ko-KR</p></li>
<li><p>Португальский (Бразилия) Пт — BR</p></li>
<li><p>Русский (Россия) ru-RU</p></li>
<li><p>Испанский (Испания) ES-ES</p></li>
<li><p>Упрощенный китайский (КНР) zh-CN</p></li>
<li><p>Китайский (традиционное письмо, Тайвань) zh-TW</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Английский (США) EN-US</p></li>
<li><p>Французский (Франция) fr-FR</p></li>
<li><p>Немецкий (Германия) de-DE</p></li>
<li><p>Итальянский (Италия) IT-IT</p></li>
<li><p>Японский (Япония) ja-JP</p></li>
<li><p>Корейский (Корея) ko-KR</p></li>
<li><p>Португальский (Бразилия) Пт — BR</p></li>
<li><p>Русский (Россия) ru-RU</p></li>
<li><p>Испанский (Испания) ES-ES</p></li>
<li><p>Упрощенный китайский (КНР) zh-CN</p></li>
<li><p>Китайский (традиционное письмо, Тайвань) zh-TW</p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> Требования к серверной системе MBAM


### Требования к серверной операционной системе MBAM

Настоятельно рекомендуется запускать клиент MBAM и сервер MBAM в одной и той же строке операционной системы. Например, Windows 10 с Windows Server 2016, Windows 8,1 с Windows Server 2012 R2 и т. д.

В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера MBAM.

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
<td align="left"><p>WindowsServer2019</p></td>
<td align="left"><p>Стандартный или центр обработки данных</p></td>
<td align="left"></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2016</p></td>
<td align="left"><p>Стандартный или центр обработки данных</p></td>
<td align="left"></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>Стандартный или центр обработки данных</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Стандартный или центр обработки данных</p></td>
<td align="left"></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Стандартный, корпоративный или центр обработки данных</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>



Корпоративный домен должен содержать по крайней мере один контроллер домена Windows Server 2008 (или более поздней версии).

### <a href="" id="bkmk-stand-alone-ramreqs"></a>MBAM, оперативная память и требования к дисковому пространству — изолированная топология

Эти требования предназначены для изолированной топологии MBAM. Требования к топологии интеграции Configuration Manager можно найти в разделе [процессор сервера MBAM, ОЗУ и требования к дисковому пространству — топология интеграции Configuration Manager](#bkmk-cm-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Элемент оборудования</th>
<th align="left">Минимальные требования</th>
<th align="left">Рекомендуемое требование</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Процессор</p></td>
<td align="left"><p>2,33 ГГц</p></td>
<td align="left"><p>2,33 ГГц или выше</p></td>
</tr>
<tr class="even">
<td align="left"><p>ОЗУ</p></td>
<td align="left"><p>8 ГБ</p></td>
<td align="left"><p>12 ГБ</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Свободное место на диске</p></td>
<td align="left"><p>1 ГБ</p></td>
<td align="left"><p>2 ГБ</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a>Требования к процессору сервера MBAM, ОЗУ и дисковому пространству — топология интеграции Configuration Manager

В таблице ниже перечислены требования к серверному процессору, ОЗУ и дисковому пространству для серверов MBAM при использовании топологии интеграции Configuration Manager. Требования для изолированной топологии можно найти в разделе [процессор сервера MBAM, ОЗУ и требования к дисковому пространству — изолированная топология](#bkmk-stand-alone-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Элемент оборудования</th>
<th align="left">Минимальные требования</th>
<th align="left">Рекомендуемое требование</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Процессор</p></td>
<td align="left"><p>2,33 ГГц</p></td>
<td align="left"><p>2,33 ГГц или выше</p></td>
</tr>
<tr class="even">
<td align="left"><p>ОЗУ</p></td>
<td align="left"><p>4 ГБ</p></td>
<td align="left"><p>8 ГБ</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Свободное место на диске</p></td>
<td align="left"><p>1 ГБ</p></td>
<td align="left"><p>2 ГБ</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a>Версии Configuration Manager, которые поддерживает MBAM

MBAM поддерживает следующие версии Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Поддерживаемая версия</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (Текущая ветвь), версии до 1902</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 1806</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (LTSB-Version 1606)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft System Center 2012 Configuration Manager</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2 или более поздней версии</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p>

&gt;<strong>Примечание </strong> несмотря на то, что Configuration Manager 2007 R2 имеет значение 32, необходимо установить его и SQL Server на 64-разрядную версию операционной системы, чтобы обеспечить соответствие с программным обеспечением 64-bit MBAM.
</td>
</tr>
</tbody>
</table>



Список поддерживаемых конфигураций для сервера Configuration Manager можно найти в соответствующей документации TechNet о версии Configuration Manager, которую вы используете. В MBAM отсутствуют дополнительные требования к системе для сервера Configuration Manager.

### <a href="" id="sql-server-database-requirements-"></a>Требования к базам данных SQL Server

В приведенной ниже таблице указаны версии Microsoft SQL Server, которые поддерживаются для функций сервера MBAM, включая базу данных восстановления, базу данных соответствия требованиям и журнал аудита, а также функцию отчеты. Требуемые версии применяются к отдельным топологиям или топологии интеграции Configuration Manager.

Необходимо установить SQL Server с параметрами сортировки **SQL \ _Latin1 \ _General \ _CP1 \ _CI \ _AS** .

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Версия SQL Server</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2019</p></td>
<td align="left"><p>Стандартный, корпоративный или центр обработки данных</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td><br/><tr class="even">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p>Стандартный, корпоративный или центр обработки данных</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td><br/><tr class="even">
<td align="left"><p>Microsoft SQL Server2016</p></td>
<td align="left"><p>Стандартный, корпоративный или центр обработки данных</p></td>
<td align="left"><p>SP1</p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p>64-разрядная</p></td>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>Стандартный, корпоративный или центр обработки данных</p></td>
<td align="left"><p>ПАКЕТ ОБНОВЛЕНИЯ 1 (SP1)</p></td>
<td align="left"><p>64-разрядная</p></td>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>Стандартный, корпоративный или центр обработки данных</p></td>
<td align="left"><p>ОБНОВЛЕНИЙ</p></td>
<td align="left"><p>64-разрядная</p></td>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>Standard или Enterprise</p></td>
<td align="left"><p>ОБНОВЛЕНИЙ</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>

**Примечание.**  
MBAM имеет максимальный поддерживаемый уровень совместимости 140. Уровень совместимости по умолчанию для новых баз данных, созданных в SQL Server 2019, составляет 150, которые необходимо изменить в 140 или более ранней, с помощью команды ALTER DATABASE после создания базы данных. Существующие базы данных, перенесенные из SQL Server 2017 или более ранних версий, останутся на прежнем уровне совместимости и не нуждаются в изменении.

Для поддержки SQL 2016 необходимо установить выпуск за март 2017 для MDOP https://www.microsoft.com/download/details.aspx?id=54967  , а также поддержку sql 2017 вы должны установить выпуск за июль 2018 и сопровождение для MDOP https://www.microsoft.com/download/details.aspx?id=57157 . В общем, всегда используйте Последнее обновление обслуживания, поскольку оно также включает все исправления ошибок и новые возможности.


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a>Требования процессора SQL Server, ОЗУ и места на диске — изолированная топология

В таблице ниже перечислены рекомендуемые требования к серверному процессору, ОЗУ и дисковому пространству для компьютера SQL Server при использовании изолированной топологии. Используйте эти требования как руководство. Конкретные требования будут зависеть от количества клиентских компьютеров, которые поддерживаются в вашей организации. Сведения о требованиях к топологии интеграции Configuration Manager можно найти в разделе [требования к процессорам SQL Server, ОЗУ и пространству на диске — топология интеграции Configuration Manager](#bkmk-cm-sql-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Элемент оборудования</th>
<th align="left">Минимальные требования</th>
<th align="left">Рекомендуемое требование</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Процессор</p></td>
<td align="left"><p>2,33 ГГц</p></td>
<td align="left"><p>2,33 ГГц или выше</p></td>
</tr>
<tr class="even">
<td align="left"><p>ОЗУ</p></td>
<td align="left"><p>8 ГБ</p></td>
<td align="left"><p>12 ГБ</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Свободное место на диске</p></td>
<td align="left"><p>5 ГБ</p></td>
<td align="left"><p>5 ГБ или больше</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a>Требования для процессора SQL Server, ОЗУ и места на диске — топология интеграции Configuration Manager

В приведенной ниже таблице перечислены требования к серверному процессору, ОЗУ и дисковому пространству для компьютера с Microsoft SQL Server при использовании топологии интеграции Configuration Manager [: изолированная топология процессора SQL Server, ОЗУ и места на диске](#bkmk-sql-stand-alone-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Элемент оборудования</th>
<th align="left">Минимальные требования</th>
<th align="left">Рекомендуемое требование</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Процессор</p></td>
<td align="left"><p>2,33 ГГц</p></td>
<td align="left"><p>2,33 ГГц или выше</p></td>
</tr>
<tr class="even">
<td align="left"><p>ОЗУ</p></td>
<td align="left"><p>4 ГБ</p></td>
<td align="left"><p>8 ГБ</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Свободное место на диске</p></td>
<td align="left"><p>5 ГБ</p></td>
<td align="left"><p>5 ГБ</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> Требования к системе клиента MBAM


### Требования к операционной системе клиента

Настоятельно рекомендуется запускать клиент MBAM и сервер MBAM в одной и той же строке операционной системы. Например, Windows 10 с Windows Server 2016, Windows 8,1 с Windows Server 2012 R2 и т. д.

В таблице ниже перечислены операционные системы, которые поддерживаются при установке клиента MBAM. Те же требования применимы к отдельным топологиям и топологии интеграции Configuration Manager.

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
<tr class="even">
    <td align="left"><p>Windows 10 IoT</p></td>
    <td align="left"><p>Функции корпоративного уровня</p></td>
    <td align="left"><p></p></td>
    <td align="left"><p>32- или 64-разрядная</p></td>
</tr><br/><tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Функции корпоративного уровня</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Функции корпоративного уровня</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7;</p></td>
<td align="left"><p>Корпоративная или максимальная</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows с собой</p></td>
<td align="left"><p>Windows 8,1 и Windows 10 корпоративный</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>Требования к ОЗУ для клиента

Нет требований к ОЗУ, которые относятся к установке клиента MBAM.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> Системные требования для групповой политики MBAM


В таблице ниже перечислены операционные системы, которые поддерживаются при установке шаблонов групповой политики MBAM.

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
 <tr class="even">
      <td align="left"><p>Windows 10 IoT</p></td>
      <td align="left"><p>Функции корпоративного уровня</p></td>
      <td align="left"><p></p></td>
      <td align="left"><p>32- или 64-разрядная</p></td>
 </tr>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Функции корпоративного уровня</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Функции корпоративного уровня</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7;</p></td>
<td align="left"><p>Корпоративная или максимальная</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>Стандартный или центр обработки данных</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Стандартный или центр обработки данных</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Стандартный, корпоративный или центр обработки данных</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>

## MBAM в Azure IaaS

Сервер MBAM может быть развернут в инфраструктуре Azure как служба (IaaS) в какой-либо из поддерживаемых версий ОС, которые подключаются к службе каталогов Active Directory, размещенной в локальной системе или службе каталогов Active Directory, также размещенной в Azure IaaS.  В [этой статье приведены](https://msdn.microsoft.com/library/azure/jj156090.aspx)сведения о настройке и настройке Active Directory в Azure IaaS.

Клиент MBAM не поддерживается на виртуальных машинах, а также не поддерживается в Azure IaaS.


## Пакеты исправлений 

- [Исправление от апреля 2016](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [Сентябрь 2016 г.](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [Декабрь 2016 г.](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [Март 2017г.](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [Июнь, 2017г.](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [Сентябрь 2017г.](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [Март 2018 г.](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [2018 июля](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [2019 мая](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## Статьи по теме


[Планирование развертывания MBAM 2.5](planning-to-deploy-mbam-25.md)

[Подготовка среды для развертывания MBAM 2.5](preparing-your-environment-for-mbam-25.md)




## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




