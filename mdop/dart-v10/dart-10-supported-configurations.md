---
title: Поддерживаемые конфигурации в DaRT 10
description: Поддерживаемые конфигурации в DaRT 10
author: dansimp
ms.assetid: a07d6562-1fa9-499f-829c-9cc487ede0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 414b9d5cb7bf78dcfeda3fafc1c476e367709446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813136"
---
# Поддерживаемые конфигурации в DaRT 10


В этой статье указаны требования к программному обеспечению и поддерживаемые конфигурации, необходимые для установки и запуска набора средств диагностики и восстановления Microsoft (DaRT) 10 в среде. Указаны требования к операционной системе и требования к системе, необходимые для запуска DaRT 10. Сведения о предварительных требованиях для создания изображения для восстановления DaRT вы можете найти в разделе [планирование создания образа для восстановления DaRT 10](planning-to-create-the-dart-10-recovery-image.md).

Для поддерживаемых конфигураций, которые относятся к более поздним выпускам, ознакомьтесь с документацией по соответствующему выпуску.

Вы можете установить DaRT одним из двух способов. Вы можете установить все возможности на компьютере администратора, где будут выполняться все задачи, связанные с выполнением DaRT. Кроме того, вы можете установить на компьютер администратора, только функцию DaRT, которая создает образ восстановления, а затем установить функции, используемые для запуска DaRT (то есть средство просмотра удаленного подключения DaRT) на компьютере службы поддержки.

## DaRT 10 необходимое программное обеспечение


Перед установкой DaRT убедитесь, что выполнены следующие предварительные требования.

### Требования для компьютера администратора

В приведенной ниже таблице перечислены требования к установке для компьютера администратора при установке DaRT 10 и всех инструментов DaRT.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Предварительные</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Комплект средств для оценки и разработки Windows (ADK)</strong></p></td>
<td align="left"><p>Обязательный для мастера создания изображений для восстановления DaRT. В нем содержатся инструменты развертывания, которые используются для настройки, развертывания и обслуживания образов Windows, а также для работы со средой предварительной установки Windows (Windows PE). При установке только средства просмотра удаленных подключений и (или) Crash Analyzer не требуется ADK.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Комплект средств разработки для Windows или пакет средств разработки программного обеспечения (необязательно)</strong></p></td>
<td align="left"><p>Для анализа файлов дампа памяти анализатору отказа требуется средство отладки Windows 10 из комплекта драйверов для Windows.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Образ ISO для Windows 10 64-bit или 32-bit</strong></p></td>
<td align="left"><p>Для DaRT требуется образ среды восстановления Windows (Windows RE) с носителя Windows 10. Загрузите 32-разрядную или 64-разрядную версию Windows 10, в зависимости от типа изображения для восстановления DaRT, которое вы хотите создать. Если в вашей среде поддерживаются оба типа систем, загрузите обе версии Windows 10.</p></td>
</tr>
</tbody>
</table>

 

### Необходимые условия для поддержки справочной системы

В приведенной ниже таблице перечислены требования к установке для компьютера службы поддержки, когда вы запускаете средство просмотра удаленных подключений DaRT 10.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Предварительные</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>DaRT 10 Remote Connection Viewer</strong></p></td>
<td align="left"><p>Должен быть установлен в операционной системе Windows 10.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Средства отладки для Windows</strong></p></td>
<td align="left"><p>Требуется только при установке средства анализа аварийного восстановления</p></td>
</tr>
</tbody>
</table>

 

### Предварительные требования к компьютеру конечного пользователя

Отсутствует необходимое программное обеспечение, которое должно быть установлено на компьютерах конечных пользователей, кроме операционной системы Windows 10.

## <a href="" id="---------dart-10-operating-system-requirements"></a> DaRT 10 требования к операционной системе


### Системные требования для компьютера администратора

В таблице ниже перечислены операционные системы, которые поддерживаются установкой на компьютере администратора DaRT 10.

**Примечание**  Убедитесь, что на компьютере администратора выделяются все дополнительные инструменты, которые вы хотите установить.

 

**Примечание**  Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления. Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975). Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.

 

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
<th align="left">Требования к операционной системе</th>
<th align="left">Требования к ОЗУ для запуска DaRT</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Все выпуски</p></td>
<td align="left"><p>Н/Д</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>2 ГБ</p></td>
<td align="left"><p>2,5 ГБ</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Все выпуски</p></td>
<td align="left"><p>Н/Д</p></td>
<td align="left"><p>32-разрядная</p></td>
<td align="left"><p>1 ГБ</p></td>
<td align="left"><p>1,5 ГБ</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> DaRT справочные требования к системе технической поддержки

Если вы разрешите службе поддержки удаленно устранять неполадки на компьютерах, на компьютере службы поддержки должна быть установлена программа просмотра удаленных подключений. При необходимости вы можете установить средство анализа аварийного восстановления на компьютере службы поддержки.

DaRT 10 позволяет сотрудникам службы поддержки подключаться к компьютеру с DaRT 10 с помощью DaRT 7,0, DaRT 8,0, DaRt 8,1 или DaRT 10 Remote Connection Viewer. Для стрелок DaRT 7,0, DaRT 8,0 и DaRt 8,1, для просмотра удаленных подключений требуется операционная система Windows 7, Windows 8 или Windows 8,1, в то время как в средстве просмотра удаленного подключения для DaRT 10 требуется Windows 10. Средство просмотра удаленных подключений DaRT 10 и все другие инструменты DaRT 10 можно установить только на компьютер под управлением Windows 10.

В таблице ниже перечислены операционные системы, которые поддерживаются для установки на компьютере с помощью функции DaRT Help.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
<th align="left">Требования к операционной системе</th>
<th align="left">Требования к ОЗУ для запуска DaRT</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Все выпуски</p></td>
<td align="left"><p>Н/Д</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>2 ГБ</p></td>
<td align="left"><p>2,5 ГБ</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows10 (только для средства просмотра удаленных подключений 10,0)</p></td>
<td align="left"><p>Все выпуски</p></td>
<td align="left"><p>Н/Д</p></td>
<td align="left"><p>32-разрядная</p></td>
<td align="left"><p>1 ГБ</p></td>
<td align="left"><p>1,5 ГБ</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Все выпуски</p></td>
<td align="left"><p>Н/Д</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>2 ГБ</p></td>
<td align="left"><p>2,5 ГБ</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8 (только для средства просмотра удаленных подключений 8,0)</p></td>
<td align="left"><p>Все выпуски</p></td>
<td align="left"><p>Н/Д</p></td>
<td align="left"><p>32-разрядная</p></td>
<td align="left"><p>1 ГБ</p></td>
<td align="left"><p>1,5 ГБ</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7 (только для средства просмотра удаленного подключения 7,0)</p></td>
<td align="left"><p>Все выпуски</p></td>
<td align="left"><p>ПАКЕТ ОБНОВЛЕНИЯ 1 (SP1)</p></td>
<td align="left"><p>64-разрядный или 32-разрядный</p></td>
<td align="left"><p>1 ГБ</p></td>
<td align="left"><p>Н/Д</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Стандартная, Корпоративная, центр обработки данных</p></td>
<td align="left"><p>Н/Д</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>2 ГБ</p></td>
<td align="left"><p>1,0 ГБ</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>Стандартная, Корпоративная, центр обработки данных</p></td>
<td align="left"><p>Н/Д</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>2 ГБ</p></td>
<td align="left"><p>1,0 ГБ</p></td>
</tr>
</tbody>
</table>

 

Для DaRT также предусмотрены следующие минимальные требования к оборудованию для конечного пользователя.

CD-или DVD-диск или порт USB — требуется только в том случае, если вы развертываете DaRT на своем предприятии с помощью компакт-диска, DVD-диска или USB.

Поддержка BIOS по запуску компьютера с компакт-диска, DVD-диска, устройства USB или из удаленного или восстановленного раздела.

### <a href="" id="-------------dart-10-end-user-computer-system-requirements"></a> DaRT 10 требования к системе для компьютеров конечных пользователей

В окне инструментов для диагностики и восстановления на DaRT 10 требуется, чтобы на компьютере конечного пользователя использовалась одна из следующих операционных систем с указанным объемом системной памяти, доступной для DaRT:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
<th align="left">Требования к операционной системе</th>
<th align="left">Требования к ОЗУ</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Все выпуски</p></td>
<td align="left"><p>Н/Д</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>2 ГБ</p></td>
<td align="left"><p>2,5 ГБ</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Все выпуски</p></td>
<td align="left"><p>Н/Д</p></td>
<td align="left"><p>32-разрядная</p></td>
<td align="left"><p>1 ГБ</p></td>
<td align="left"><p>1,5 ГБ</p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Планирование развертывания DaRT 10](planning-to-deploy-dart-10.md)

 

 





