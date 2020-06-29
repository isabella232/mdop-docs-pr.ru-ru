---
title: Необходимые условия для развертывания MBAM 2.0
description: Необходимые условия для развертывания MBAM 2.0
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826012"
---
# Необходимые условия для развертывания MBAM 2.0


Перед запуском настройки администрирования и мониторинга Microsoft BitLocker (MBAM) необходимо убедиться в соблюдении необходимых условий для установки продукта. В этом разделе содержится информация, которая поможет вам успешно спланировать вычислительную среду перед развертыванием администрирования Microsoft BitLocker и наблюдения за функциями и клиентами сервера. Если вы устанавливаете MBAM с помощью Configuration Manager, ознакомьтесь со сведениями о том, [как развернуть MBAM с помощью Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) для дополнительных необходимых компонентов.

## Требования для установки функций сервера MBAM


Каждый из функций сервера MBAM имеет определенные предварительные требования, которые должны быть выполнены, прежде чем можно будет успешно установить компоненты MBAM. Программа установки MBAM проверяет, выполнены ли все необходимые условия перед началом установки.

### Предварительные требования для сервера администрирования и мониторинга

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
<td align="left"><p><strong>Роль веб-сервера Windows Server</strong></p></td>
<td align="left"><p>Эту роль необходимо добавить в серверную операционную систему, которая поддерживается для компонента администрирования и мониторинга сервера.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Средства управления веб-сервером (IIS)</strong></p></td>
<td align="left"><p>Выберите <strong> сценарии управления IIS и инструменты </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>SSL-сертификат</strong></p></td>
<td align="left"><p>Необязательно. Для безопасной связи между клиентами и веб-службами необходимо получить и установить сертификат, подписанный надежным центром безопасности.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Службы ролей веб-сервера</strong></p></td>
<td align="left"><p><strong>Основные возможности HTTP:</strong></p>
<ul>
<li><p>Статическое содержимое</p></li>
<li><p>Документ по умолчанию</p></li>
</ul>
<p><strong>Разработка приложений.</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Расширяемость .NET</p></li>
<li><p>Расширения ISAPI</p></li>
<li><p>Фильтры ISAPI</p></li>
</ul>
<p><strong>Разрешения</strong></p>
<ul>
<li><p>Проверка подлинности Windows</p></li>
<li><p>Фильтрация запросов</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Возможности Windows Server</strong></p></td>
<td align="left"><p><strong>Компоненты .NET Framework 3.5.1:</strong></p>
<ul>
<li><p>.NET Framework 3.5.1</p></li>
<li><p>Активация WCF</p>
<ul>
<li><p>Активация по HTTP</p></li>
<li><p>Активация не по протоколу HTTP</p></li>
</ul></li>
</ul>
<p><strong>Служба активации процессов Windows.</strong></p>
<ul>
<li><p>Модель процесса</p></li>
<li><p>Среда .NET</p></li>
<li><p>API конфигурации</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Примечание.**  
Список поддерживаемых операционных систем можно найти в разделе [Поддерживаемые конфигурации MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).



### Предварительные требования для отчетов о соответствии и аудите

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
<td align="left"><p>Поддерживаемая версия SQL Server</p>
<p>Поддерживаемые <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,0.</p></td>
<td align="left"><p>Установка SQL Server с помощью:</p>
<ul>
<li><p>SQL_Latin1_General_CP1_CI_AS параметры сортировки</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Службы SQL Server Reporting Services (SSRS)</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Права экземпляра SSRS — необходимы для установки отчетов, только если вы устанавливаете базы данных на отдельном сервере из отчетов.</p></td>
<td align="left"><p>Необходимые права для экземпляра:</p>
<ul>
<li><p>Создание папок</p></li>
<li><p>Публикация отчетов</p></li>
</ul>
<p>Службы SSRS должны быть установлены и запущены во время установки сервера MBAM. Настройка SSRS в режиме "машинный", а не в ненастроенном режиме или "SharePoint".</p></td>
</tr>
</tbody>
</table>



### Предварительные условия для базы данных восстановления

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
<td align="left"><p>Поддерживаемая версия SQL Server</p>
<p>Поддерживаемые <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,0.</p></td>
<td align="left"><p>Установка SQL Server с помощью:</p>
<ul>
<li><p>SQL_Latin1_General_CP1_CI_AS параметры сортировки</p></li>
<li><p>Средства управления SQL Server</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Требуемые разрешения SQL Server</p></td>
<td align="left"><p>Необходимые разрешения:</p>
<ul>
<li><p>Роли сервера входа для экземпляра SQL:</p>
<ul>
<li><p>dbcreator</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>Права экземпляра служб SQL Server Reporting Services:</p>
<ul>
<li><p>Создание папок</p></li>
<li><p>Публикация отчетов</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Необязательный параметр-Установка прозрачного шифрования данных (TDE), доступные в SQL Server</p></td>
<td align="left"><p>Функция TDE SQL Server осуществляет шифрование и расшифровку данных и файлов журнала в режиме реального времени, что поможет вам соблюдать многочисленные законы, правила и правила, определенные в разных отраслях.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>TDE выполняет расшифровку сведений о базе данных в режиме реального времени, что означает, что если учетная запись, под которой вы вошли в систему, имеет разрешения на доступ к базе данных, когда вы просматриваете данные ключа восстановления в таблицах SQL Server, отображаются сведения о ключе восстановления.</p>
</div>
<div>

</div>
<p>Дополнительные сведения о TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 в вопросах безопасности </a> .</p></td>
</tr>
</tbody>
</table>



### Предварительные условия для базы данных соответствия требованиям и аудита

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
<td align="left"><p>Поддерживаемая версия SQL Server</p>
<p>Поддерживаемые <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,0.</p></td>
<td align="left"><p>Установка SQL Server с помощью:</p>
<ul>
<li><p>SQL_Latin1_General_CP1_CI_AS параметры сортировки</p></li>
<li><p>Средства управления SQL Server</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Требуемые разрешения SQL Server</p></td>
<td align="left"><p>Необходимые разрешения:</p>
<ul>
<li><p>Роли сервера входа для экземпляра SQL:</p>
<ul>
<li><p>dbcreator</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>Права экземпляра служб SQL Server Reporting Services:</p>
<ul>
<li><p>Создание папок</p></li>
<li><p>Публикация отчетов</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Необязательный параметр-Установка прозрачного шифрования данных (TDE) в SQL Server.</p></td>
<td align="left"><p>Функция TDE SQL Server осуществляет шифрование и расшифровку данных и файлов журнала в режиме реального времени, что поможет вам соблюдать многочисленные законы, правила и правила, определенные в разных отраслях.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>TDE выполняет расшифровку сведений о базе данных в режиме реального времени, что означает, что если учетная запись, под которой вы вошли в систему, имеет разрешения на доступ к базе данных, когда вы просматриваете данные ключа восстановления в таблицах SQL Server, отображаются сведения о ключе восстановления.</p>
</div>
<div>

</div>
<p>Дополнительные сведения о TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 вопросы безопасности</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>При установке сервера MBAM на сервере SQL Server должны быть установлены и запущены службы ядра СУБД.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Служба агента SQL Server должна быть запущена и настроена на автоматическое начало для выбранных экземпляров SQL Server.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Предварительные требования для портала самообслуживания

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
<td align="left"><p>Поддерживаемая версия Windows Server</p>
<p>Поддерживаемые <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,0.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 2,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)">Загрузка ASP.NET MVC 2</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Средства управления IIS для веб-служб</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Предварительные требования для клиентов MBAM


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
<td align="left"><p><strong>Для клиентов Windows 7 </strong> - требуется возможность доверенного платформенного модуля (TPM).</p></td>
<td align="left"><p>Версия доверенного платформенного модуля должна быть 1,2 или более поздней.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Микросхема TPM должна быть включена в BIOS и может быть переустановлена из операционной системы.</p></td>
<td align="left"><p>Дополнительные сведения можно найти в документации по BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Только для клиентов Windows 8 </strong> : MBAM хранение и управление ключами восстановления доверенного платформенного модуля: необходимо отключить автоматическое наполнение TPM, и перед развертыванием MBAM необходимо назначить MBAM в качестве владельца доверенного платформенного модуля. Сведения о том, как отключить автоматическое предоставление TPM, можно найти в разделе <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</p>
<ul>
<li><p>Автоматическое конфигурирование TPM должно быть отключено.</p></li>
<li><p>Перед развертыванием MBAM необходимо назначить MBAM в качестве владельца доверенного платформенного модуля.</p></li>
</ul></td>
<td align="left"><p>Сведения о том, как отключить автоматическое предоставление TPM, можно найти в разделе <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Убедитесь, что клавиатура, видео или мышь подключены напрямую и не управляются с помощью клавиатуры, видео или мыши (KVM) Switch. КВМ-коммутатор может взаимодействовать с возможностями компьютера, чтобы обнаружить физическое присутствие оборудования.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Статьи по теме


[Планирование развертывания MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Поддерживаемые конфигурации MBAM 2.0](mbam-20-supported-configurations-mbam-2.md)









