---
title: Проверка разделов реестра перед установкой сервера App-V 5.x
description: Проверка разделов реестра перед установкой сервера App-V 5.x
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814709"
---
# Проверка разделов реестра перед установкой сервера App-V 5.x

Если вы обновляете приложение App-V 5,0 с пакетом обновления 1 (SP1) или более поздней версии, выполните действия, описанные в этом разделе, перед установкой сервера App-V 5. x

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Если это действие является обязательным</strong></p></td>
<td align="left"><p>Вы обновляете приложение App-V 5,0 SP1 со всеми последующими пакетами исправлений, которые вы установили с помощью MSP-файла.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>В каких компонентах требуется выполнить это действие</strong></p></td>
<td align="left"><p>Только обновляемые серверные компоненты App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Если вам понадобится это действие</strong></p></td>
<td align="left"><p>Перед обновлением сервера App-V на App-V 5. x</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Что вам нужно сделать?</strong></p></td>
<td align="left"><p>С помощью сведений, указанных в приведенных ниже таблицах, обновите значение каждого раздела реестра в соответствии <code>HKLM\Software\Microsoft\AppV\Server</code> со значением, которое вы указали при первоначальной установке сервера. При выполнении этого шага восстанавливаются значения реестра, которые могут быть удалены, если установлены пакеты исправлений App-V 5,0 SP1.</p></td>
</tr>
</tbody>
</table>

 

**Клавиша ManagementDatabase**

Если вы устанавливаете базу данных управления, настройте эти разделы реестра в разделе `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Имя ключа</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Указывает, требуется ли учетной записи Public Access для доступа к нелокальным базам данных управления. Если требуется, для параметра value задано значение "1".</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_NAME</p></td>
<td align="left"><p>Имя базы данных управления.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Учетная запись, используемая для чтения (общедоступной) доступа к базе данных управления.</p>
<p>Используется, если <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> задано значение 1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Идентификатор безопасности (SID) учетной записи, используемой для чтения (общедоступного) доступа к базе данных управления.</p>
<p>Используется, если <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> задано значение 1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Экземпляр SQL Server для базы данных управления.</p>
<p>Если значение пусто, используется экземпляр базы данных по умолчанию.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Учетная запись, используемая для доступа на запись (администратора) к базе данных управления.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Идентификатор безопасности (SID) учетной записи, используемой для доступа записи (администратора) к базе данных управления.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Учетная запись удаленного компьютера сервера управления (домен \ учетная_запись).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Учетная запись администратора установки для сервера управления (домен \ учетная_запись).</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Допустимые значения:</p>
<ul>
<li><p><strong>1 </strong> – Служба управления находится на локальном компьютере, то есть MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT пуста.</p></li>
<li><p><strong>0 </strong> - Служба управления находится на другом компьютере, а не на локальном компьютере.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Клавиша ManagementService**

Если вы устанавливаете сервер управления, настройте эти разделы реестра в разделе `HKLM\Software\Microsoft\AppV\Server\ManagementService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Имя ключа</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MANAGEMENT_ADMINACCOUNT</p></td>
<td align="left"><p>Группа доменных служб Active Directory (AD DS) или учетная запись, которой разрешено управлять App-V (домен \ учетная_запись).</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Экземпляр SQL Server, содержащий базу данных управления.</p>
<p>Если значение пусто, используется экземпляр базы данных по умолчанию.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Имя удаленного сервера SQL Server с базой данных управления.</p>
<p>Если значение пусто, используется локальный компьютер.</p></td>
</tr>
</tbody>
</table>

 

**Клавиша ReportingDatabase**

Если вы устанавливаете базу данных отчетов, настройте эти разделы реестра в разделе `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Имя ключа</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Указывает, требуется ли учетной записи Public Access для доступа к нелокальным базам данных отчетов. Если требуется, для параметра value задано значение "1".</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_NAME</p></td>
<td align="left"><p>Имя базы данных отчетов.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Учетная запись, используемая для чтения (общего доступа) к базе данных отчетов.</p>
<p>Используется, если <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> задано значение 1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Идентификатор безопасности (SID) учетной записи, используемой для чтения (общедоступного) доступа к базе данных отчетов.</p>
<p>Используется, если <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> задано значение 1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Экземпляр SQL Server для базы данных отчетов.</p>
<p>Если значение пусто, используется экземпляр базы данных по умолчанию.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Учетная запись удаленного компьютера сервера отчетов (домен \ учетная_запись).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Учетная запись администратора установки для сервера отчетов (домен \ учетная_запись).</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Допустимые значения:</p>
<ul>
<li><p><strong>1 </strong> – Служба отчетов находится на локальном компьютере, то есть REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT пустая.</p></li>
<li><p><strong>0 </strong> - Служба отчетов находится на другом компьютере, а не на локальном компьютере.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Клавиша ReportingService**

Если вы устанавливаете сервер отчетов, настройте эти разделы реестра в разделе `HKLM\Software\Microsoft\AppV\Server\ReportingService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Имя ключа</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Экземпляр SQL Server для базы данных отчетов.</p>
<p>Если значение пусто, используется экземпляр базы данных по умолчанию.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Имя удаленного сервера SQL Server с базой данных отчетов.</p>
<p>Если значение пусто, используется локальный компьютер.</p></td>
</tr>
</tbody>
</table>

