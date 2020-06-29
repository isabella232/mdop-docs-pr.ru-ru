---
title: Использование командной строки для установки сервера MBAM
description: Использование командной строки для установки сервера MBAM
author: dansimp
ms.assetid: 6ffc6d41-a793-42c2-b997-95ba47550648
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a689a2df77300300073b2731281004feac87305f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825642"
---
# Использование командной строки для установки сервера MBAM


Вы можете использовать командную строку для установки сервера MBAM с помощью изолированной топологии или Configuration Manager. Следующий пример командной строки предназначен для развертывания MBAM на одном сервере, который является архитектурой, которая должна использоваться только в тестовой среде. При развертывании MBAM в рабочей среде, которая должна иметь несколько серверов, необходимо изменить командную строку соответствующим образом.

## Командная строка для развертывания сервера MBAM 2.0 с изолированной топологией


Чтобы установить сервер MBAM с изолированной топологией, можно использовать командную строку, подобную приведенной ниже.

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

В приведенной ниже таблице описаны параметры командной строки для развертывания сервера MBAM с изолированной топологией.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Параметр</th>
<th align="left">Значение параметра</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TOPOLOGY</p></td>
<td align="left"><p>до</p></td>
<td align="left"><p>0 — изолированная топология</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>ведение</p></td>
<td align="left"><p>0 – не принимайте лицензию agreement1 – принимайте условия лицензионного соглашения</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADDLOCAL</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Компоненты, устанавливаемые на сервере</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>KeyDatabase</p></td>
<td align="left"><p>База данных восстановления</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>ReportsDatabase</p></td>
<td align="left"><p>База данных отчетов о сертификации и аудите</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Отчеты</p></td>
<td align="left"><p>Отчеты о соответствии и аудите</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>AdministrationMonitoringServer</p></td>
<td align="left"><p>Веб-сайт администрирования и мониторинга</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>SelfServiceServer</p></td>
<td align="left"><p>Портал самообслуживания</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>PolicyTemplate</p></td>
<td align="left"><p>Шаблон групповой политики MBAM</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>[UserDomain] [UserName1]</p></td>
<td align="left"><p>Домен и учетная запись пользователя для учетной записи служб Reporting Services, которая будет обращаться к базе данных соответствия требованиям и аудита.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>Пароль учетной записи служб Reporting Services, которая будет обращаться к базе данных соответствия требованиям и аудита.</p></td>
</tr>
<tr class="even">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>ComputerName</p></td>
<td align="left"><p>Имя экземпляра SQL Server для базы данных соответствия требованиям и аудита — замените <strong> % ComputerName% </strong> именем компьютера</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>ComputerName</p></td>
<td align="left"><p>Имя экземпляра SQL Server для базы данных восстановления — замените <strong> % ComputerName% </strong> именем компьютера</p></td>
</tr>
<tr class="even">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>ComputerName</p></td>
<td align="left"><p>Экземпляр сервера SQL Server Reporting Server, на котором будут установлены отчеты о соответствии и аудите — замените <strong> % ComputerName% на </strong> имя компьютера</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Порт для веб-сайта администрирования и наблюдения; "83" — это только пример</p></td>
</tr>
<tr class="even">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Порт для веб-сайта портала самообслуживания; "83" — это только пример</p></td>
</tr>
</tbody>
</table>

 

## Командная строка для развертывания сервера MBAM 2.0 с топологией Configuration Manager


Для установки сервера MBAM с топологией Configuration Manager можно использовать командную строку, подобную приведенной ниже.

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

В приведенной ниже таблице описаны параметры командной строки для установки сервера MBAM 2.0 с топологией Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Параметр</th>
<th align="left">Значение параметра</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TOPOLOGY</p></td>
<td align="left"><p>1,1</p></td>
<td align="left"><p>1 — топология Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>ведение</p></td>
<td align="left"><p>0 – не принимайте лицензию agreement1 – принимайте условия лицензионного соглашения</p></td>
</tr>
<tr class="odd">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>ComputerName</p></td>
<td align="left"><p>Имя экземпляра SQL Server для базы данных аудита — замените <strong> % ComputerName% </strong> именем компьютера</p></td>
</tr>
<tr class="even">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>ComputerName</p></td>
<td align="left"><p>Имя экземпляра SQL Server для базы данных восстановления — замените <strong> % ComputerName% </strong> именем компьютера</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>ComputerName</p></td>
<td align="left"><p>Экземпляр сервера SQL Server Reporting Server, на котором будут установлены отчеты аудита — замена% ComputerName% на имя компьютера</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>[UserDomain] [UserName1]</p></td>
<td align="left"><p>Домен и учетная запись пользователя для учетной записи служб Reporting Services, которая будет обращаться к базе данных соответствия требованиям и аудита.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>Пароль учетной записи служб Reporting Services, которая будет обращаться к базе данных соответствия требованиям и аудита.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Порт для веб-сайта администрирования и наблюдения; "83" — это только пример</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Порт для веб-сайта портала самообслуживания; "83" — это только пример</p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Развертывание инфраструктуры сервера MBAM 2.0 Server](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





