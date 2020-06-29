---
title: Требования программы Application Virtualization Sequencer к оборудованию и программному обеспечению
description: Требования программы Application Virtualization Sequencer к оборудованию и программному обеспечению
author: dansimp
ms.assetid: c88a1b5b-23e1-4460-afa9-a5f37e32eb05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d68afe4d4a3f6f301d38f2e86139d94319583467
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819622"
---
# Требования программы Application Virtualization Sequencer к оборудованию и программному обеспечению


В этой статье описаны минимальные рекомендуемые требования к оборудованию и программному обеспечению для компьютера, на котором работает секвенсор Microsoft Application Virtualization (App-V).

**Важно!**  Вы должны запустить секвенсор App-V (**SFTSequencer.exe**), используя учетную запись с правами администратора из-за изменений, которые секвенсор делает в локальной системе. Эти изменения могут включать запись файлов в каталог **C:\\program Files Files** , внесение изменений в реестр, запуск и остановку служб, обновление дескрипторов безопасности для файлов и изменение разрешений.

 

Перед установкой секвенсора и после упорядочения каждого приложения необходимо восстановить чистую копию операционной системы на компьютере виртуализации. Для восстановления компьютера, на котором запущен секвенсор, можно использовать один из следующих способов:

-   Переформатируйте жесткий диск и переустановите операционную систему.

-   Восстановите жесткий диск компьютера, на котором запущено изображение секвенсора, с помощью другого программного обеспечения для обработки изображений.

-   Возврат образа виртуальной операционной системы, например, изображения виртуального компьютера Microsoft. С помощью виртуальной машины можно легко повторно использовать чистые среды виртуализации с минимальным администрированием.

Ниже приведен список рекомендуемых требований к оборудованию для работы секвенсора App-V.

Требования перечислены в первую очередь для Microsoft Application Virtualization (App-V) 4.6 SP2, за которым следуют требования для версий, предшествующих App-V 4.6 SP2.

### <a href="" id="hardware-requirements-"></a>Требования к оборудованию

-   Процессор — Intel Pentium III, 1 ГГц (32-разрядная или 64-разр.). Процесс упорядочения является однопотоковым процессом и не использует преимущества двух процессоров.

-   Память (1 ГБ или выше) рекомендуется 2 ГБ.

-   Жесткий диск — объем свободного места на жестком диске объемом не менее 15 ГБ. Рекомендуется, чтобы в три места на жестком диске соработало приложение, для которого требуется выполнить виртуализацию.

    **Примечание**  Для виртуализации требуется высокая нагрузка на диск. Ускоренная скорость диска может уменьшить время последовательности.

     

### Требования к программному обеспечению для App-V 4,6 SP2

В приведенном ниже списке описаны поддерживаемые операционные системы для работы с секвенсором App-V 4,6 с пакетом обновления 2 (SP2).

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
<td align="left"><p>ОБНОВЛЕНИЙ</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Бизнес, Корпоративная или максимальная</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Профессиональная, Корпоративная или максимальная</p></td>
<td align="left"><p>Пакет обновления или пакет обновления 1 (SP1) отсутствуют</p></td>
<td align="left"><p>x86 и x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Pro или Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 и x64</p></td>
</tr>
</tbody>
</table>

 

**Примечание**  Application Virtualization (App-V) 4,6 с пакетом обновления 2 (SP2) поддерживает 32-разрядные и 64-разрядные версии этих операционных систем.

 

На компьютерах под управлением программы Sequencer следует настроить те же приложения, которые установлены на целевые компьютеры.

### Требования к программному обеспечению для версий, предшествующих App-V 4,6 SP2

В следующем списке описаны поддерживаемые операционные системы для работы программы Sequencer для версий, предшествующих App-V 4,6 SP2.

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

 

На компьютерах под управлением программы Sequencer следует настроить те же приложения, которые установлены на целевые компьютеры.

### Требования к программному обеспечению для служб удаленных рабочих столов для App-V 4,6 SP2

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
<td align="left"><p>Windows server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition или Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления или пакет обновления 1 (SP1) отсутствуют</p></td>
<td align="left"><p>x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
</tbody>
</table>

 

**Примечание**  Application Virtualization (App-V) 4,6 с пакетом обновления 2 (SP2) для служб удаленных рабочих столов поддерживает 32-разрядные и 64-разрядные версии этих операционных систем.

 

### Требования к программному обеспечению для служб удаленных рабочих столов для версий, предшествующих App-V 4,6 SP2

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
<td align="left"><p>Нет пакета обновления или пакета обновления 2 (SP2)</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise и Datacenter Edition</p></td>
<td align="left"><p>Пакет обновления или пакет обновления 1 (SP1) отсутствуют</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

**Примечание**  Application Virtualization (App-V) 4,6 с пакетом обновления 2 (SP2) для служб удаленных рабочих столов поддерживает 32-разрядные и 64-разрядные версии этих операционных систем.

 

## Статьи по теме


[Требования клиента Application Virtualization к оборудованию и программному обеспечению](application-virtualization-client-hardware-and-software-requirements.md)

[Требования к системе при работе с Application Virtualization](application-virtualization-system-requirements.md)

[Установка программы Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md)

[Обновление программы Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)

 

 





