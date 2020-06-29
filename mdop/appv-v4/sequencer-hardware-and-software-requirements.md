---
title: Требования программы Sequencer к оборудованию и программному обеспечению
description: Требования программы Sequencer к оборудованию и программному обеспечению
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815532"
---
# Требования программы Sequencer к оборудованию и программному обеспечению


В этой статье описаны минимальные рекомендуемые требования к оборудованию и программному обеспечению для компьютера, на котором работает секвенсор Microsoft Application Virtualization (App-V).

Перед установкой секвенсора и после упорядочения каждого приложения необходимо восстановить чистую копию операционной системы на компьютере виртуализации. Для восстановления компьютера, на котором запущен секвенсор, можно использовать один из следующих способов:

-   Переформатируйте жесткий диск и переустановите операционную систему.

-   Восстановите жесткий диск компьютера, на котором запущено изображение секвенсора, с помощью другого программного обеспечения для обработки изображений.

Ниже приведен список рекомендуемых требований к оборудованию для работы секвенсора App-V.

### <a href="" id="hardware-requirements-"></a>Требования к оборудованию

-   Процессор — Intel Pentium III, 1 ГГц (32-разрядная или 64-разр.). Процесс упорядочения является однопотоковым процессом и не использует преимущества двух процессоров.

-   Память (1 ГБ или более), рекомендуется не менее 2 Гбайт.

-   Жесткий диск — объем свободного места на жестком диске объемом не менее 15 ГБ. Рекомендуется, чтобы в три места на жестком диске соработало приложение, для которого требуется выполнить виртуализацию.

    **Примечание**  Для виртуализации требуется высокая нагрузка на диск. Ускоренная скорость диска может уменьшить время последовательности.

     

### Требования к программному обеспечению

В следующем списке описаны поддерживаемые операционные системы для запуска секвенсора.

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
<td align="left"><p>Профессиональная</p></td>
<td align="left"><p>SP2 или 3 (SP3)</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Бизнес, Корпоративная или максимальная</p></td>
<td align="left"><p>Пакет обновления, пакет обновления 1 (SP1) или пакет обновления 2 (SP2)</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7 ¹</p></td>
<td align="left"><p>Профессиональная, Корпоративная или максимальная</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

¹ поддерживается для App-V 4,5 с пакетом обновления 1 или 2, а также App-V 4,6

**Примечание**  Приложение Application Virtualization (App-V) 4,6 поддерживает версию с 32-и 64-разрядные версии этих операционных систем.

 

На компьютерах под управлением программы Sequencer следует настроить те же приложения, которые установлены на целевом компьютере.

### Требования к программному обеспечению для служб удаленных рабочих столов

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
<td align="left"><p>Standard Edition, Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Стандартный, корпоративный или центр обработки данных</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

**Примечание**  Application Virtualization (App-V) 4,6 для служб удаленных рабочих столов поддерживает 32-разр и 64-разрядные версии этих операционных систем.

 

## Статьи по теме


[Обзор программы Application Virtualization Sequencer](application-virtualization-sequencer-overview.md)

 

 





