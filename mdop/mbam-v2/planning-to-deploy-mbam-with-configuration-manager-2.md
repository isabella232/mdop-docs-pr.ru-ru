---
title: Планирование развертывания MBAM с помощью диспетчера конфигураций
description: Планирование развертывания MBAM с помощью диспетчера конфигураций
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825629"
---
# Планирование развертывания MBAM с помощью диспетчера конфигураций


Для развертывания MBAM с топологией Configuration Manager рекомендуются архитектура с тремя серверами, поддерживающая клиенты 200 000. Используйте отдельный сервер для запуска Configuration Manager и устанавливайте основные возможности администрирования и наблюдения на двух серверах, как показано на рисунке архитектуры в разделе [Приступая к работе с помощью диспетчера конфигураций](getting-started---using-mbam-with-configuration-manager.md).

**Важно.**  
Windows To Go не поддерживается при установке интегрированной топологии MBAM с Configuration Manager 2007.



## Предварительные требования к развертыванию для установки MBAM с помощью Configuration Manager


Перед установкой MBAM с помощью Configuration Manager убедитесь, что выполнены следующие предварительные требования:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Предварительные</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Убедитесь, что сервер Configuration Manager является основным сайтом в системе Configuration Manager.</p></td>
<td align="left"><p>Н/Д</p></td>
</tr>
<tr class="even">
<td align="left"><p>Включите агент клиента инвентаризации оборудования на сервере Configuration Manager.</p></td>
<td align="left"><p>В Configuration Manager 2007 вы можете узнать, <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> как настроить инвентаризацию оборудования для сайта </a> .</p>
<p>Инструкции для System Center 2012 Configuration Manager можно найти <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> в разделе Настройка инвентаризации оборудования в Configuration Manager </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Включите агент управления требуемой конфигурацией (DCM) или параметры соответствия требованиям в зависимости от используемой версии Configuration Manager.</p></td>
<td align="left"><p>В Configuration Manager 2007 включите раздел Просмотр <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> свойств агента клиента управления требуемой конфигурацией </a> .</p>
<p>Сведения о System Center 2012 Configuration Manager можно найти <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> в разделе Настройка параметров соответствия в Configuration Manager </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Определите точку служб Reporting Services в диспетчере конфигураций. Требуется для служб отчетов SQL.</p></td>
<td align="left"><p>В Configuration Manager 2007 вы узнаете, <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> как создать точку служб Reporting Services для служб отчетов SQL </a> .</p>
<p>Для System Center 2012 Configuration Manager ознакомьтесь с разделами <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> Предварительные требования для создания отчетов в Configuration Manager </a> .</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> Поддерживаемые версии Configuration Manager


MBAM поддерживает следующие версии Configuration Manager:

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
<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2</p></td>
<td align="left"><p>SP1 или более поздней версии</p></td>
<td align="left"><p>64-разрядная</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Несмотря на то, что Configuration Manager 2007 имеет значение 32, необходимо установить его и SQL Server на 64-разрядную версию операционной системы, чтобы обеспечить соответствие с программным обеспечением 64-bit MBAM.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center 2012 Configuration Manager</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>



Список поддерживаемых конфигураций для сервера Configuration Manager можно найти на соответствующей веб-странице для используемой версии Configuration Manager. В MBAM отсутствуют дополнительные требования к системе для сервера Configuration Manager.

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> Требования к системе для MBAM и SQL Server


Поддерживаемые конфигурации и требования к системе для серверов MBAM и SQL Server для топологии Configuration Manager совпадают с параметрами изолированной топологии. Требования к отдельным системам можно найти в разделе [Поддерживаемые конфигурации MBAM 2,0](mbam-20-supported-configurations-mbam-2.md). Сведения о требованиях к MBAM серверу и процессору SQL Server, ОЗУ и дисковому пространству для топологии Configuration Manager можно найти в следующих разделах.

## Требования к MBAM процессору, ОЗУ и дисковому пространству для MBAM


В таблице ниже перечислены требования к серверному процессору, ОЗУ и дисковому пространству для серверов MBAM при использовании топологии интеграции Configuration Manager.

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



## Требования для процессора SQL Server, ОЗУ и места на диске


В таблице ниже перечислены требования к серверному процессору, ОЗУ и дисковому пространству для компьютера SQL Server при использовании топологии интеграции Configuration Manager.

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
<td align="left"><p>4 ГБ</p></td>
<td align="left"><p>8 ГБ</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Свободное место на диске</p></td>
<td align="left"><p>5 ГБ</p></td>
<td align="left"><p>5 ГБ или больше</p></td>
</tr>
</tbody>
</table>



## Необходимые разрешения для установки сервера MBAM


Чтобы установить MBAM с помощью Configuration Manager, необходимо обладать правами администратора в Configuration Manager, у которого есть роль безопасности с минимальными разрешениями, указанными в приведенной ниже таблице. Кроме того, для установки сервера MBAM в таблице также выводятся права, выходящие за основные права администратора компьютера.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Разрешения</th>
<th align="left">Компонент сервера MBAM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Роли сервера для входа в экземпляр SQL:-dbcreator-processadmin</p></td>
<td align="left"><p>- База данных для восстановления — база данных аудита</p></td>
</tr>
<tr class="even">
<td align="left"><p>Права экземпляра служб SQL Server Reporting Services:-создание папок — публикация отчетов</p></td>
<td align="left"><p>- Интеграция System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**System Center 2012 Configuration Manager**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Разрешения</th>
<th align="left">Компонент сервера Configuration Manager</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Права доступа к сайту Configuration Manager:-Read</p></td>
<td align="left"><p>Интеграция System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Права на сбор Configuration Manager:-создание элементов конфигурации и развертывание</p></td>
<td align="left"><p>Интеграция System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Разрешения элемента конфигурации Configuration Manager:-Create-Delete-Read</p></td>
<td align="left"><p>Интеграция System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**Configuration Manager 2007**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Разрешения</th>
<th align="left">Компонент сервера Configuration Manager</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Права доступа к сайту Configuration Manager:-Read</p></td>
<td align="left"><p>Интеграция System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Права на сбор Configuration Manager:-Create-Delete-Read-ReadResource</p></td>
<td align="left"><p>Интеграция System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Права конфигурации Configuration Manager:-создание-удаление-чтение и распространение</p></td>
<td align="left"><p>Интеграция System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



## Порядок развертывания функций MBAM для топологии Configuration Manager


При развертывании MBAM на сервере Configuration Manager необходимо выполнить задачи развертывания в указанном ниже порядке.

1.  Измените файл Configuration. mof на сервере Configuration Manager.

2.  Создайте или измените сервер конфигурации SMS \ _def. mof.

3.  Установите MBAM на сервере Configuration Manager.

4.  Установите базу данных восстановления и базу данных аудита на сервере базы данных.

5.  Установите компоненты MBAM на сервере администрирования и мониторинга.

## Контрольный список планирования для установки MBAM с помощью Configuration Manager


В этом контрольном списке описаны рекомендуемые шаги и высокоуровневый список элементов, которые следует принимать во время планирования развертывания администрирования Microsoft BitLocker и мониторинга с помощью Configuration Manager. Рекомендуется скопировать этот контрольный список в программу для работы с электронными таблицами и настроить ее для использования.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Задача</th>
<th align="left">Ссылки</th>
<th align="left">Заметки</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ознакомьтесь со сведениями о начале работы, в котором описано, как работает Configuration Manager, в MBAM и показана Рекомендуемая архитектура высокого уровня.</p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)">Начало работы — использование MBAM с диспетчером конфигураций</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ознакомьтесь с информацией по планированию, которая описывает требования к развертыванию, Поддерживаемые конфигурации, необходимые разрешения и порядок развертывания для каждой функции.</p></td>
<td align="left"><p>Планирование развертывания MBAM с помощью диспетчера конфигураций</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Спланируйте и настройте требования к групповой политике MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Планирование требований групповой политики MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Планируйте и создавайте необходимые группы безопасности доменных служб Active Directory и планируйте требования к членству в локальной группе безопасности MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Планирование ролей администратора MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Планируйте развертывание клиента MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">Планирование развертывания клиента MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Статьи по теме


[Использование MBAM с диспетчером конфигураций](using-mbam-with-configuration-manager.md)









