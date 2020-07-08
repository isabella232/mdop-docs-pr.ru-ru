---
title: Поддерживаемые конфигурации MBAM 1.0
description: Поддерживаемые конфигурации MBAM 1.0
author: dansimp
ms.assetid: 1f5ac58e-6a3f-47df-8a9b-4b57631ab9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2c72320379d1c9328a6b40537d37998402b1b38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825939"
---
# Поддерживаемые конфигурации MBAM 1.0


В этой статье указаны необходимые требования для установки и запуска администрирования и мониторинга Microsoft BitLocker (MBAM) в среде.

## <a href="" id="---------mbam-server-system-requirements"></a> Требования к серверной системе MBAM


### Требования к серверной операционной системе

В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера администрирования и мониторинга Microsoft BitLocker.

**Примечание.**  
Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления. Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975). Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.



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
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Стандартная, Корпоративная, для центра обработки данных или веб-сервера</p></td>
<td align="left"><p>Только SP2</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Стандартная, Корпоративная, для центра обработки данных или веб-сервера</p></td>
<td align="left"></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>



**Warning**  
Установка служб MBAM, отчетов и баз данных на компьютере контроллера домена не поддерживается.



### <a href="" id="server-random-access-memory--ram--requirements-"></a>Требования к оперативной памяти (RAM) сервера

Нет требований к ОЗУ, которые относятся к установке сервера MBAM.

### <a href="" id="sql-server-database-requirements-"></a>Требования к базам данных SQL Server

В следующей таблице перечислены версии SQL Server, которые поддерживаются при установке компонентов сервера MBAM.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Компонент сервера MBAM</th>
<th align="left">Версия SQL Server</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Отчеты о соответствии и аудите</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Стандартный, корпоративный, центр обработки данных или выпуск для разработчиков</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>База данных восстановления и оборудования</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Enterprise, Datacenter или Developer Edition</p>
<div class="alert">
<strong>Важно.</strong><br/><p>Стандартные выпуски SQL Server не поддерживаются для восстановления MBAM и установки компонента сервера базы данных оборудования.</p>
</div>
<div>

</div></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>База данных соответствия требованиям и аудита</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Стандартный, корпоративный, центр обработки данных или выпуск для разработчиков</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> Требования к системе клиента MBAM


### Требования к операционной системе клиента

В таблице ниже перечислены операционные системы, которые поддерживаются при установке клиента MBAM.

**Примечание.**  
Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления. Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975). Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.



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
<td align="left"><p>Windows 7;</p></td>
<td align="left"><p>выпуск Корпоративная</p></td>
<td align="left"><p>Нет, SP1</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7;</p></td>
<td align="left"><p>Максимальная выпускная версия</p></td>
<td align="left"><p>Нет, SP1</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>Требования к ОЗУ для клиента

Нет требований к ОЗУ, которые относятся к установке клиента MBAM.

## Статьи по теме


[Планирование развертывания MBAM 1.0](planning-to-deploy-mbam-10.md)

[Необходимые компоненты развертывания MBAM 1.0](mbam-10-deployment-prerequisites.md)









