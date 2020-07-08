---
title: Поддерживаемые конфигурации MED-V 1.0
description: Поддерживаемые конфигурации MED-V 1.0
author: dansimp
ms.assetid: 74643de6-549e-4177-a559-6407e156ed3a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3b8ffdfb6e34fe7888ea5ace0ff7264bd978a548
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812608"
---
# Поддерживаемые конфигурации MED-V 1.0


В этой статье указаны требования, необходимые для установки и запуска Microsoft Enterprise Virtualization (MED-V) 1,0 в среде.

## Требования к системе для клиента MED-V 1,0


### Требования клиентской операционной системы для MED-V

В таблице ниже перечислены операционные системы, которые поддерживаются при установке клиента MED-V 1,0.

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
<td align="left"><p>Windows XP</p></td>
<td align="left"><p>Профессиональный выпуск</p></td>
<td align="left"><p>SP2 или 3 (SP3)</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Бизнес, Корпоративная или максимальная выпускная версия</p></td>
<td align="left"><p>Пакет обновления 1 (SP1) или 2</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>



**Примечание.**  
Клиент MED-V не работает в режиме собственного 64-разрядного режима. Вместо этого MED-V работает в режиме Windows в Windows 64-bit (WOW64) на 64-разрядных компьютерах.



### <a href="" id="med-v-1-0-client-configuration-"></a>Конфигурация клиента для MED-V 1,0

**Версия .NET Framework**

Для установки клиента MED-V 1,0 поддерживаются следующие версии Microsoft .NET Framework:

-   .NET Framework 2,0 или .NET Framework 2,0 SP1

-   .NET Framework 3,0 или .NET Framework 3,0 SP1

-   .NET Framework 3,5 или .NET Framework 3,5 SP1

**Модуль виртуализации**

Microsoft Virtual PC 2007 с пакетом обновления 1 (SP1) с исправлением, описанным в статье Microsoft Knowledge Base 974918, поддерживается для установки клиента MED-V 1,0 в указанных ниже конфигурациях.

-   Статический файл виртуального жесткого диска (VHD)

-   Несколько файлов VHD, расположенных в одном и том же каталоге

-   Динамический файл виртуального жесткого диска

**Интернет-браузер**

Windows Internet Explorer 7 и Windows Internet Explorer 8 поддерживаются для установки клиента MED-V 1,0.

**Microsoft Hyper-V Server**

Клиент MED-V не поддерживается в среде сервера Microsoft Hyper-V.

## Системные требования для рабочих областей MED-V 1,0


### Требования к операционной системе для рабочих областей MED-V

В таблице ниже перечислены операционные системы, поддерживаемые в рабочих областях для MED-V 1,0.

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
<td align="left"><p>Windows 2000</p></td>
<td align="left"><p>Профессиональная</p></td>
<td align="left"><p>Сервис</p></td>
<td align="left"><p>Выпуск</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows XP</p></td>
<td align="left"><p>Профессиональный выпуск</p></td>
<td align="left"><p>SP2 или 3 (SP3)</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Для обеспечения совместимости рабочей области MED-V с будущими версиями MED-V рекомендуется использовать пакет обновления 3 (SP3).</p>
</div>
<div>

</div></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-workspace-configuration-"></a>Настройка рабочей области для MED-V 1,0

**Версия .NET Framework**

Для использования MED-V требуется одна из указанных ниже поддерживаемых версий Microsoft .NET Framework для MED-V 1,0 Workspace:

-   .NET Framework 2,0 SP1

-   .NET Framework 3,0 SP1

-   .NET Framework 3,5 или .NET Framework 3,5 SP1

**Примечание.**  
.NET Framework 3,5 с пакетом обновления 1 (SP1) рекомендуется использовать для обеспечения совместимости рабочей области MED-V с будущими версиями MED-V.



**Интернет-браузер**

Windows Internet Explorer 6 с пакетом обновления 2 (SP2) и Windows Internet Explorer 7 поддерживаются для установки рабочей области MED-V 1,0.

### <a href="" id="med-v-workspace-images-"></a>Образы рабочих областей MED-V

Образы рабочих областей для MED-V должны создаваться с помощью Virtual PC 2007 с пакетом обновления 1 (SP1).

## Требования к серверной системе для MED-V 1,0


### Требования к серверной операционной системе для MED-V 1,0

В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера MED-V 1,0.

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
<td align="left"><p>Standard или Enterprise</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>X86 или x64</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-server-configuration-"></a>Конфигурация сервера MED-V 1,0

**Версия .NET Framework**

Для использования MED-V требуется одна из указанных ниже поддерживаемых версий Microsoft .NET Framework для MED-V 1,0 Workspace:

-   .NET Framework 2,0 или .NET Framework 2,0 SP1

-   .NET Framework 3,0 или .NET Framework 3,0 SP1

-   .NET Framework 3,5 или .NET Framework 3,5 SP1

**Версия Microsoft SQL Server**

Следующие версии Microsoft SQL Server поддерживаются для MED-V 1,0, когда SQL Server установлен локально или удаленно с сервера MED-V 1,0:

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
<td align="left"><p>SQL Server 2005</p></td>
<td align="left"><p>Экспресс, стандартная или Корпоративная выпускная версия</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>X86 или x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server 2008</p></td>
<td align="left"><p>Экспресс, стандартная или Корпоративная</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>X86 или x64</p></td>
</tr>
</tbody>
</table>



**Microsoft Hyper-V Server**

Сервер MED-V поддерживается в среде Microsoft Hyper-V Server.

## Сведения о глобализации для MED-V 1,0


Несмотря на то что MED-V не выпускается на языках, отличных от английского, для установки клиента, рабочей области и сервера MED-V 1,0 поддерживаются следующие языковые версии операционной системы Windows.

-   Английский

-   Французский

-   Немецкий

-   Итальянский

-   Испанский

-   Португальский (Бразилия)









