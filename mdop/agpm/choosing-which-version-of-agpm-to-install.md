---
title: Выбор версии AGPM для установки
description: Выбор версии AGPM для установки
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: b09ea8161b6801c62552f1c0d0ef8455dc111e2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819099"
---
# Выбор версии AGPM для установки


Каждый выпуск управления групповыми политиками MicrosoftAdvanced поддерживает определенные версии операционной системы Windows. Мы настоятельно рекомендуем использовать клиент и сервер РАСШИРЕНного использования РАСШИРЕНного взаимодействия в той же строке операционной системы. Например, Windows 10 с Windows Server 2016, Windows 8.1 и Windows Server2012 R2 и т. д.

Рекомендуем установить сервер расширенного управления групповыми политиками в новейшей версии операционной системы домена. С помощью консоли управления групповыми политиками (GPMC) можно архивировать и восстанавливать объекты групповой политики (GPO). Поскольку новые версии GPMC предоставляют дополнительные параметры политики, недоступные в более ранних версиях, вы можете управлять дополнительными параметрами политики, используя самую последнюю версию операционной системы.

Все версии расширенного управления групповыми политиками могут управлять только параметрами политики, которые были введены в той же или более ранней версии операционной системы, в которой работает служба управления групповыми политиками. Например, если установить пакет обновления 2 (SP2) для Windows Server 2012, вы можете управлять параметрами политики, которые были введены в Windows Server 2012 или более ранней версии, но вы не можете управлять параметрами политики, которые появились позже в Windows 8.1 или Windows Server2012 R2.

Если версия GPMC на сервере управления ГРУППОВыми политиками старше, чем версия на компьютерах, используемых администраторами для управления групповой политикой, сервер управления ГРУППОВыми политиками не сможет хранить параметры политики, недоступные в более ранней версии GPMC. Таблицу параметров групповой политики, включенных в Windows, см. в [Справочнике по параметрам групповой политики Windows и Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).

## РАСШИРЕННАЯ ВЕРСИЯ ДЛЯ ВЕРСИИ 4.0 SP3


Если вы используете на компьютерах под управлением Windows 10 Управление объектами групповой политики, необходимо использовать параметр РАСШИРЕНного обновления для 4,0. На компьютерах под управлением операционной системы Windows 10 невозможно установить более раннюю версию РАСШИРЕНного использования службы.

В таблице 1 перечислены операционные системы, для которых вы можете установить пакет управления групповыми политиками версии 4.0 SP3, и параметры политики, которые можно управлять с помощью расширенного управления групповыми политиками.

**Таблица 1: РАСШИРЕНная поддержка операционных систем и параметров политики в конфигурации со всеми 4,0 SP3**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Поддерживаемые конфигурации для сервера РАСШИРЕНного языка</strong></th>
<th align="left"><strong>Поддерживаемые конфигурации для клиента с расширенным управлением групповыми политиками</strong></th>
<th align="left"><strong>Поддержка РАСШИРЕНных возможностей</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2016 или Windows 10</p></td>
<td align="left"><p>Windows Server 2016 или Windows 10</p></td>
<td align="left"><p>Поддерживается</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2</p></td>
<td align="left"><p>Windows 10;</p></td>
<td align="left"><p>Поддерживается с помощью предостережений, описанных в <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> статьях KB 4015786</a>
</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2 или Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 или Windows 8.1</p></td>
<td align="left"><p>Поддерживается</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 или Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 или Windows 8,1</p></td>
<td align="left"><p>Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Windows Server2008 или WindowsVista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 или Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 и Windows7</p></td>
<td align="left"><p>Не поддерживается.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Поддерживается, но не может сообщить или изменить параметры политики или элементы предпочтений, существующие только в Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 или Windows7</p></td>
</tr>
</tbody>
</table>

 

## РАСШИРЕННОЕ ОБНОВЛЕНИЕ ДЛЯ ВЕРСИИ 4.0 SP2


Если вы используете компьютеры с операционной системой Windows Server2012 R2 или Windows 8.1 для управления объектами групповой политики, необходимо использовать многодоменные версии 2 (SP2). Вы не можете установить более ранние версии РАСШИРЕНного использования службы на компьютерах под управлением этих операционных систем.

В таблице 1 перечислены операционные системы, для которых можно установить пакет управления групповыми политиками и параметры политики, которые можно управлять с помощью РАСШИРЕНного обновления для версии 4.0 SP2.

**Таблица 2. Поддерживаемые операционные системы и параметры политики для РАСШИРЕНной версии 4.0 с пакетом обновления**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Поддерживаемые конфигурации для сервера РАСШИРЕНного языка</strong></th>
<th align="left"><strong>Поддерживаемые конфигурации для клиента с расширенным управлением групповыми политиками</strong></th>
<th align="left"><strong>Поддержка РАСШИРЕНных возможностей</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2 или Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 или Windows 8.1</p></td>
<td align="left"><p>Поддерживается</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 или Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 или Windows 8,1</p></td>
<td align="left"><p>Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Windows Server2008 или WindowsVista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 или Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Не поддерживается.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Поддерживается, но не может сообщить или изменить параметры политики или элементы предпочтений, существующие только в Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 или Windows7</p></td>
</tr>
</tbody>
</table>

 

## РАСШИРЕННАЯ ВЕРСИЯ ДЛЯ NT 4.0 SP1


В таблице 2 перечислены операционные системы, для которых можно установить 4,0 РАСШИРЕНную настройку конфигурации с пакетом обновления 1 (SP1), а также параметры политики, которые можно управлять с помощью РАСШИРЕНного пакета администрирования.

**Таблица 3: РАСШИРЕНная поддержка операционных систем и параметров политики в версии 4.0 с пакетом обновления (SP1)**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Поддерживаемые конфигурации для сервера РАСШИРЕНного языка</strong></th>
<th align="left"><strong>Поддерживаемые конфигурации для клиента с расширенным управлением групповыми политиками</strong></th>
<th align="left"><strong>Поддержка РАСШИРЕНных возможностей</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Поддерживается</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8,1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Поддерживается</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Поддерживается, но не может сообщать или изменять параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</p></td>
</tr>
</tbody>
</table>

 

## РАСШИРЕНная версия для версии 4.0


В таблице 3 перечислены операционные системы, для которых можно установить параметры расширенного управления групповыми политиками 4,0, а также настройки политики, которые можно управлять с помощью служб управления ГРУППОВыми политиками.

**Таблица 4: Поддерживаемые операционные системы и параметры политики для РАСШИРЕНной версии 4.0**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Поддерживаемые операционные системы для сервера РАСШИРЕНного языка</th>
<th align="left">Поддерживаемые операционные системы для клиента с расширенным управлением групповыми политиками</th>
<th align="left">Поддержка РАСШИРЕНных возможностей</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Поддерживается</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Windows Server2008R2 или Windows7</p></td>
<td align="left"><p>Не поддерживается.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>Поддерживается, но не может сообщать или изменять параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</p></td>
</tr>
</tbody>
</table>

 

## Версии РАСШИРЕНного типа данных, предшествующих РАСШИРЕНному (для версии 4.0)


В таблице 4 перечислены операционные системы, для которых вы можете установить версии РАСШИРЕНного типа, предшествующие РАСШИРЕНию для версии 4.0. Если операционная система не указана в списке, вы не можете установить в этой операционной системе РАСШИРЕНную учетную запись.

**Таблица 5: Поддерживаемые операционные системы для версий с расширенным управлением групповыми политиками, предшествующих РАСШИРЕНному набору**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Версия расширенного управления групповыми политиками, которая может быть установлена</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>3,0</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista с пакетом обновления 1 (SP1)</p></td>
<td align="left"><p>3,0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WindowsVista без установленного пакета обновления (32-разрядная версия)</p></td>
<td align="left"><p>2,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows server2003 (32-разрядная версия)</p></td>
<td align="left"><p>2,5</p></td>
</tr>
</tbody>
</table>

 

## Получение технологий для MDOP


Компонент РАСШИРЕНной оптимизации для настольных систем (MDOP) 4,0 входит в состав пакета обновления. MDOP входит в состав Microsoft Software Assurance. Дополнительные сведения о программе Software Assurance и приобретении MDOP можно найти в [статьях получение MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Статьи по теме


[Расширенное управление групповыми политиками (AGPM)](index.md)

 

 





