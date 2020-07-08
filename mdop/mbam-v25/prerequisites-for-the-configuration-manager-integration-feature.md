---
title: Необходимые условия для компонента интеграции диспетчера конфигураций
description: Необходимые условия для компонента интеграции диспетчера конфигураций
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825012"
---
# Необходимые условия для компонента интеграции диспетчера конфигураций


Если вы разворачиваете MBAM с помощью топологии интеграции System Center Configuration Manager, мы рекомендуем использовать архитектуру с тремя серверами, как описано в [высоком уровне архитектуры MBAM 2,5 с топологией интеграции Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md). Эта архитектура может поддерживать клиентские компьютеры 500 000.

**Важно.**  
Windows To Go не поддерживается при установке топологии интеграции Configuration Manager при использовании Configuration Manager 2007.



## Общие требования для компонента интеграции Configuration Manager


При установке MBAM с помощью Configuration Manager необходимо добавить в дополнение к предварительным требованиям для изолированной топологии следующие дополнительные требования.

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
<td align="left"><p>Сервер Configuration Manager — это основной сайт в системе Configuration Manager.</p></td>
<td align="left"><p>Н/Д</p></td>
</tr>
<tr class="even">
<td align="left"><p>Агент клиента инвентаризации оборудования находится на сервере Configuration Manager Server.</p></td>
<td align="left"><p>Инструкции для System Center 2012 Configuration Manager можно найти <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> в разделе Настройка инвентаризации оборудования в Configuration Manager </a> .</p>
<p>В Configuration Manager 2007 вы можете узнать, <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> как настроить инвентаризацию оборудования для сайта </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>В зависимости от используемой версии Configuration Manager включена одна из следующих функций:</p>
<ul>
<li><p>Параметры соответствия требованиям — (System Center 2012 Configuration Manager)</p></li>
<li><p>Агент клиента управления требуемой конфигурацией (DCM) — (Configuration Manager 2007)</p></li>
</ul></td>
<td align="left"><p>Сведения о System Center 2012 Configuration Manager можно найти <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> в разделе Настройка параметров соответствия в Configuration Manager </a> .</p>
<p>Сведения о Configuration Manager 2007 можно найти в разделе <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> Свойства агента клиента управления требуемой конфигурацией </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Точка служб Reporting Services определена в Configuration Manager. Требуется для служб SQL Server Reporting Services (SSRS).</p></td>
<td align="left"><p>Для System Center 2012 Configuration Manager ознакомьтесь с разделами <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> Предварительные требования для создания отчетов в Configuration Manager </a> .</p>
<p>В Configuration Manager 2007 вы узнаете, <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> как создать точку служб Reporting Services для служб отчетов SQL </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Для Configuration Manager 2007 требуется Microsoft .NET Framework 2,0</p></td>
<td align="left"><p>Для агента клиента управления требуемой конфигурацией (DCM) в Configuration Manager 2007 требуется платформа .NET Framework 2,0 для создания отчета о соответствии.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Установка .NET Framework 3,5 автоматически устанавливает .NET Framework 2,0.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Необходимые разрешения для установки MBAM с помощью Configuration Manager


Чтобы установить MBAM с помощью Configuration Manager, необходимо обладать правами администратора в Configuration Manager, у которого есть роль безопасности с минимальными разрешениями, указанными в приведенной ниже таблице. Кроме того, для установки сервера MBAM в таблице также выводятся права, выходящие за основные права администратора компьютера.

**Разрешения, указанные в приведенной ниже таблице, применимы к обеим версиям Configuration Manager.**

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
<td align="left"><p>Роли сервера входа для экземпляра SQL Server:-dbcreator-processadmin</p></td>
<td align="left"><p>- База данных для восстановления — база данных аудита</p></td>
</tr>
<tr class="even">
<td align="left"><p>Права экземпляра служб SSRS:-создание папок — публикация отчетов</p></td>
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



## Изменения, необходимые для файлов. mof


Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker в отчетах Configuration Manager MBAM, необходимо изменить файл Configuration. mof и SMS \ _def. mof для System Center 2012 Configuration Manager и Microsoft System Center Configuration Manager 2007. Инструкции можно найти [в разделе MBAM 2,5 Server требования, применимые только к топологии интеграции Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).



## Статьи по теме


[Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





