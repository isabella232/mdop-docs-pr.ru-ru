---
title: Поддерживаемые конфигурации MBAM 2.0
description: Поддерживаемые конфигурации MBAM 2.0
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823909"
---
# Поддерживаемые конфигурации MBAM 2.0


В этой статье указаны требования для установки и запуска администрирования и мониторинга Microsoft BitLocker (MBAM) 2,0 в среде с помощью изолированной топологии. Для поддерживаемых конфигураций, которые относятся к более поздним выпускам, ознакомьтесь с документацией по соответствующему выпуску.

Если вы планируете установить MBAM 2,0 с помощью топологии Configuration Manager и хотите просмотреть список требований к системе, ознакомьтесь с [Разпланированием развертывания MBAM с помощью Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

Рекомендуемая конфигурация для запуска MBAM в рабочей среде состоит из двух серверов, в зависимости от требований к масштабируемости. Эта конфигурация поддерживает до 200 000 MBAM клиентов. Изображение и описания изолированной инфраструктуры сервера MBAM можно найти в разделе [архитектура высокого уровня для MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).

**Примечание**  Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления. Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975). Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.

 

## <a href="" id="---------mbam-server-system-requirements"></a> Требования к серверной системе MBAM


### Требования к серверной операционной системе

В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера администрирования и мониторинга Microsoft BitLocker.

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
<td align="left"><p>WindowsServer2008 R2</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsServer2012</p></td>
<td align="left"><p>Standard или Datacenter Edition</p></td>
<td align="left"></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>

 

**Примечание**  Установка служб MBAM, отчетов и баз данных на компьютере контроллера домена не поддерживается.

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a>Требования к серверному процессору, ОЗУ и дисковому пространству

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Аппаратный компонент</th>
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

 

### <a href="" id="sql-server-database-requirements-"></a>Требования к базам данных SQLServer

В приведенной ниже таблице перечислены версии SQLServer, которые поддерживаются при установке компонентов сервера администрирования и мониторинга, включая базу данных восстановления, базу данных соответствия требованиям и сведения о соответствии и аудите. Кроме того, для баз данных дополнительно требуется установка средств управления SQL Server.

**Примечание**  MBAM изначально не поддерживает группы кластеризации, зеркального отображения и доступности SQL. Чтобы установить базу данных, необходимо выполнить установку сервера MBAM на отдельном сервере SQL Server.

 

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
<td align="left"><p>MicrosoftSQLServer2008 R2</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftSQLServer2012</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Аппаратный компонент</th>
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

 

## <a href="" id="---------mbam-client-system-requirements"></a> Требования к системе клиента MBAM


### Требования к операционной системе клиента

В таблице ниже перечислены операционные системы, которые поддерживаются для администрирования Microsoft BitLocker и наблюдения за установкой клиентов.

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
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Корпоративная или максимальная выпускная версия</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>выпуск Корпоративная</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows с собой</p></td>
<td align="left"><p>Windows 8 Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a>Требования к ОЗУ для клиента

Нет требований к ОЗУ, которые относятся к установке и мониторингу клиента Microsoft BitLocker.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> Системные требования для групповой политики MBAM


В таблице ниже перечислены операционные системы, которые поддерживаются для администрирования Microsoft BitLocker и наблюдения за установкой шаблонов групповой политики.

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
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Корпоративная или максимальная выпускная версия</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>выпуск Корпоративная</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard или Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Планирование развертывания MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Необходимые условия для развертывания MBAM 2.0](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





