---
title: Сведения об App-V 5.0 с пакетом обновления 3 (SP3)
description: Сведения об App-V 5.0 с пакетом обновления 3 (SP3)
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814972"
---
# Сведения об App-V 5.0 с пакетом обновления 3 (SP3)


В следующих разделах приведены сведения о значительных изменениях, которые относятся к Microsoft Application Virtualization (App-V) 5,0 SP3:

-   [Требования к программному обеспечению для App-V 5,0 SP3 и поддерживаемые конфигурации](#bkmk-sp3-prereq-configs)

-   [Переход на App-V 5,0 SP3](#bkmk-migrate-to-50sp3)

-   [Для созданного вручную XML-файла группы подключения требуется обновление схемы](#bkmk-update-schema-cg)

-   [Усовершенствования групп соединений](#bkmk-cg-improvements)

-   [Администраторы могут публиковать и отменять публикацию пакетов для определенного пользователя](#bkmk-usersid-pub-pkgs-specf-user)

-   [Разрешение только администраторам публиковать и отменять публикацию пакетов](#bkmk-admins-only-pub-unpub-pkgs)

-   [Раздел реестра RunVirtual поддерживает пакеты, опубликованные для пользователя](#bkmk-runvirtual-reg-key)

-   [Новые командлеты PowerShell и Справка по обновляемым командлетам](#bkmk-posh-cmdlets-help)

-   [Основной каталог виртуального приложения (PVAD) является скрытым, но его можно включить](#bkmk-pvad-hidden)

-   [ClientVersion требуется для просмотра метаданных публикации App-V](#bkmk-pub-metadata-clientversion)

-   [Журналы событий App-V объединены](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a>Требования к программному обеспечению для App-V 5,0 SP3 и поддерживаемые конфигурации


Ниже приведены ссылки на дополнительные требования к программному обеспечению App-V 5,0 SP3 и поддерживаемые конфигурации.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ссылки на предварительные и поддерживаемые конфигурации</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)">Необходимые условия для App-V 5.0 с пакетом обновления 3 (SP3)</a></p></td>
<td align="left"><p>Необходимое программное обеспечение, которое необходимо установить перед началом установки App-V 5,0 SP3</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">Поддерживаемые конфигурации App-V 5.0 с пакетом обновления 3 (SP3)</a></p></td>
<td align="left"><p>Поддерживаемые операционные системы и требования к оборудованию для серверов App-V, секвенсоров и клиентских компонентов</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a>Переход на App-V 5,0 SP3


Воспользуйтесь приведенными ниже сведениями, чтобы перейти на версию App-V 5,0 SP3 из более ранних версий.

### Перед началом обновления

Прежде чем приступить к обновлению, ознакомьтесь с приведенными ниже сведениями.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Элементы для проверки перед обновлением</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Компоненты для обновления</p></td>
<td align="left"><ol>
<li><p>Сервер App-V</p></li>
<li><p>Секвенсор</p></li>
<li><p>Клиент App-V или клиент служб удаленных рабочих столов (RDS) для App-V</p></li>
<li><p>Группы подключения</p></li>
</ol>
<div class="alert">
<strong>Примечание.</strong><br/><p>Чтобы использовать пользовательский интерфейс клиента App-V, скачайте текущую версию из <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> приложения пользовательского интерфейса клиента Microsoft Application Virtualization 5,0 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Обновление для App-V 4. x</p></td>
<td align="left"><p>Сначала необходимо выполнить обновление до версии App-V 5,0. Вы не можете выполнить обновление непосредственно из App-V 4. x в App-V 5,0 SP3.</p>
<p>Дополнительные сведения см. в следующих разделах:</p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)">Сведения о App-V 5.0</a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)">Планирование миграции из предыдущей версии App-V</a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Обновление для App-V 5,0 или более поздней версии</p></td>
<td align="left"><p>Вы можете выполнить обновление до версии App-V 5,0 SP3 прямо из любой из указанных ниже версий.</p>
<ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul>
<p>Чтобы перейти на версию App-V 5,0 SP3, выполните действия, приведенные в остальных разделах этой статьи.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Изменения, необходимые для пакетов и групп подключений после обновления</p></td>
<td align="left"><p>Нет. Пакеты и группы соединений продолжат работать, как в настоящее время.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a>Инструкции по обновлению инфраструктуры App-V

Выполните описанные ниже действия, чтобы обновить каждый компонент инфраструктуры App-V до версии App-v 5,0 SP3.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Шаг</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Шаг 1. Обновите сервер App-V.</p>
<p>Если вы не используете сервер App-V, пропустите этот шаг и перейдите к следующему шагу.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Клиент App-V 5,0 с пакетом обновления 3 (SP3) совместим с сервером App-V 5,0 SP1.</p>
</div>
<div>

</div></td>
<td align="left"><p>Выполните следующие действия: </p>
<ol>
<li><p>Ознакомьтесь с <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> заметками о выпуске для App-v 5,0 SP3 </a> для устранения проблем, которые могут повлиять на установку сервера App-v.</p></li>
<li><p>Выполните одно из указанных ниже действий в зависимости от того, какой метод вы используете для обновления базы данных управления и (или) базы данных отчетов.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Метод обновления базы данных</th>
<th align="left">Шаг</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Установщик Windows</p></td>
<td align="left"><p>Пропустите этот шаг и перейдите к шагу 3, "Если вы обновляете сервер App-V..."</p></td>
</tr>
<tr class="even">
<td align="left"><p>Скрипты SQL</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>База данных управления</strong></p></td>
<td align="left"><p>Для установки или обновления ознакомьтесь со <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> сценариями SQL, чтобы установить или обновить базу данных сервера управления App-V 5,0 с пакетом обновления 3 (SP3) не удалось </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>База данных отчетов</strong></p></td>
<td align="left"><p>Выполните действия, описанные в разделе <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> развертывание баз данных App-V с помощью сценариев SQL </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p>Если вы обновляете приложение App-V 5,0 с пакетом обновления 1 (SP1) или более поздней версии, выполните действия, описанные в разделе <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> Проверка разделов реестра после установки приложения App-v 5,0 SP3 </a> .</p></li>
<li><p>Выполните действия, описанные в статье <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> развертывание сервера App-V 5,0 </a> .</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Шаг 2. Обновите секвенсор App-V.</p></td>
<td align="left"><p>Узнайте <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> , как установить секвенсор </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Шаг 3. Обновите клиент App-V или клиентское приложение RDS-V.</p></td>
<td align="left"><p>Узнайте <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> , как развернуть клиент App-V </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a>Проверка разделов реестра перед установкой сервера App-V 5,0 с пакетом обновления 3 (SP3)

Это шаг 3 из предыдущей таблицы.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Если это действие является обязательным</strong></p></td>
<td align="left"><p>Вы обновляете версию App-V с пакетом обновления 1 (SP1), используя любые последующие пакеты исправлений, которые вы установили с помощью MSP-файла.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>В каких компонентах требуется выполнить это действие</strong></p></td>
<td align="left"><p>Только обновляемые серверные компоненты App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Если вам понадобится это действие</strong></p></td>
<td align="left"><p>Перед обновлением сервера App-V до версии App-V 5,0 с пакетом обновления 3 (SP3)</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Что вам нужно сделать?</strong></p></td>
<td align="left"><p>С помощью сведений, указанных в приведенных ниже таблицах, обновите значение каждого раздела реестра в соответствии <code>HKLM\Software\Microsoft\AppV\Server</code> со значением, которое вы указали при первоначальной установке сервера. При выполнении этого шага восстанавливаются значения реестра, которые могут быть удалены при установке пакетов исправлений для App-V SP1.</p></td>
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



## <a href="" id="bkmk-update-schema-cg"></a>Для созданного вручную XML-файла группы подключения требуется обновление схемы


Если вы вручную создаете XML-файл группы подключений и хотите использовать новые возможности, описанные в разделе [улучшения для групп подключения](#bkmk-cg-improvements), в XML-файле, необходимо указать следующую схему:

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

Примеры и дополнительные сведения можно найти [в разделе о файле группы подключения](about-the-connection-group-file.md).

## <a href="" id="bkmk-cg-improvements"></a>Усовершенствования групп соединений


Для упрощения управления группами подключений можно использовать дополнительные пакеты и другие улучшения, добавленные в App-V 5,0 SP3. В следующей таблице перечислены задачи, которые можно выполнять с помощью новых функций групп подключений, а также ссылки на более подробные сведения о каждой задаче.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Задача или компонент</th>
<th align="left">Описание</th>
<th align="left">Ссылки на дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Включение дополнительных пакетов в группу подключения</p></td>
<td align="left"><p>Включение необязательных пакетов в группу подключения позволяет динамически определять, какие приложения будут включены в виртуальную среду группы подключений, в зависимости от того, для каких пользователей они предназначены.</p>
<p>Управлять количеством групп подключений не требуется, так как вы можете смешивать необязательные и ненужные пакеты в одной группе подключения. Смешивание пакетов позволяет разным группам пользователей использовать одну и ту же группу подключений, несмотря на то, что у пользователей может быть только один общий пакет.</p>
<p><strong>Пример </strong> . Вы можете включить пакет для Microsoft Office для всех пользователей, но включить различные дополнительные пакеты, которые содержат различные подключаемые модули Office, для разных подмножества пользователей.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">Использование дополнительных пакетов в группах соединений</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Отмена публикации или удаление необязательного пакета без изменения группы подключения</p></td>
<td align="left"><p>Отменять публикацию или удаление, а также отменять публикацию и повторно публиковать необязательный пакет, который находится в группе подключений, не отключая и не возвращающую в клиенте App-V группу подключения.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">Использование дополнительных пакетов в группах соединений</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Публикация групп подключений, которые содержат опубликованные пользователями и публикуемые глобально пакеты</p></td>
<td align="left"><p>Создайте опубликованную пользователем группу подключений, которая включает опубликованные пользователем и глобально опубликованные пакеты.</p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)">Создание связывающей группы с опубликованными пользователями и глобально опубликованными пакетами</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Как сделать так, чтобы группа соединений не проигнорировала версию пакета</p></td>
<td align="left"><p>Настройте группу подключений таким образом, чтобы она принимала любую версию пакета, которая позволяет обновить пакет, не отключая группу подключения. Кроме того, если в группе подключения есть дополнительный пакет с неверной версией, пакет игнорируется и не блокирует создание виртуальной среды группы подключения.</p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)">Настройка игнорирования версии пакета группой соединений</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ограничение возможностей публикации конечных пользователей</p></td>
<td align="left"><p>Разрешите публиковать пакеты и включать группы подключений только для администраторов (не конечных пользователей).</p></td>
<td align="left"><p>Сведения о группах подключений можно найти <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> в разделе разрешение включения групп подключения только администраторам.</a></p>
<p>Сведения о пакетах можно найти в следующих статьях:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Метод</th>
<th align="left">Ссылка на дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Консоль управления</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)">Публикация пакета с помощью консоли управления</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)">Управление группами соединений на отдельном компьютере с помощью PowerShell</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Почтовая система электронной почты от сторонних разработчиков</p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)">Настройка публикации пакетов с помощью ESD только для администраторов</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>Включение и отключение группы подключений для определенного пользователя</p></td>
<td align="left"><p>Администраторы могут включать и отключать группу подключений для определенного пользователя с помощью необязательного <strong> </strong> параметра – параметр с указанными ниже командлетами.</p>
<ul>
<li><p>Enable-AppVClientConnectionGroup</p></li>
<li><p>Disable-AppVClientConnectionGroup</p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)">Управление группами соединений на отдельном компьютере с помощью PowerShell</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Слияние одинаковых путей к пакетам в один виртуальный каталог в группах подключений</p></td>
<td align="left"><p>Если несколько пакетов в группе подключения содержат одинаковые пути к каталогам, они объединяются в один виртуальный каталог в виртуальной среде "Группа подключения".</p>
<p>Это объединение путей позволяет приложению в одном пакете получить доступ к файлам в другом пакете.</p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)">О виртуальной среде связывающей группы</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a>Администраторы могут публиковать и отменять публикацию пакетов для определенного пользователя


Администраторы могут использовать следующие командлеты для публикации и отмены публикации пакетов для определенного пользователя. Чтобы использовать командлеты, введите параметр **–** , а затем идентификатор безопасности пользователя (SID). Дополнительные сведения см. в следующих разделах:

-   [Управление пакетами App-V 5.0, работающими на автономном компьютере, с помощью PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [Управление пакетами App-V 5.0, работающими на автономном компьютере, с помощью PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Командлет</th>
<th align="left">Примеры:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Publish-AppvClientPackage</p></td>
<td align="left"><p>Publish-AppvClientPackage "ContosoApplication"-в чем заключается S-1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
<tr class="even">
<td align="left"><p>Отмена публикации — AppvClientPackage</p></td>
<td align="left"><p>Отмена публикации-AppvClientPackage "ContosoApplication"-от S до 1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a>Разрешение только администраторам публиковать и отменять публикацию пакетов


Вы можете включить только администраторов (не конечных пользователей) для публикации и отмены публикации пакетов с помощью одного из указанных ниже способов.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Метод</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Параметр групповой политики</p></td>
<td align="left"><p>Перейдите к следующему узлу объекта групповой политики:</p>
<p><strong>Политики конфигурации &gt; компьютера &gt; . Административные &gt; шаблоны &gt; Публикация System App-V &gt; </strong> .</p>
<p>Включите <strong> параметр требуется опубликовать как </strong> групповую политику администратора.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)">Управление пакетами App-V 5.0, работающими на автономном компьютере, с помощью PowerShell</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a>Раздел реестра RunVirtual поддерживает пакеты, опубликованные для пользователя


App-V 5,0 SP3 добавляет поддержку использования раздела реестра **RunVirtual** с виртуализированными приложениями, которые находятся в опубликованных пользователем пакетах. Раздел реестра **RunVirtual** позволяет запускать локально установленное приложение в виртуальной среде вместе с приложениями, виртуализованными с помощью App-V.

Ранее виртуализированные приложения в пакетах App-V были опубликованы глобально. Дополнительные сведения о **RunVirtual** и других методах выполнения локально установленных приложений в виртуальной среде с виртуализированными приложениями можно найти в разделе [выполнение локально установленного приложения в виртуальной среде с виртуализированными приложениями](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).

## <a href="" id="bkmk-posh-cmdlets-help"></a>Новые командлеты PowerShell и Справка по обновляемым командлетам


Новые командлеты PowerShell и Справка по обновляемым командлетам включены в App-V 5,0 SP3. Чтобы скачать модули командлетов, Узнайте, [как загрузить командлеты PowerShell и получить справку по командлетам](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).

### Новые командлеты PowerShell для App-V 5,0 с пакетом обновления 3 (SP3)

Добавлены новые командлеты Windows PowerShell для сервера App-V, помогающие управлять группами подключений.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Командлет</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Add-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Добавляет пакет в конец группы подключения&#39;s и позволяет настроить пакет как необязательный и/или без версии в группе подключения.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Set-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Позволяет изменять сведения о пакете группы подключения, например, является ли это необязательным.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Remove-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Удаление пакета из группы подключения.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a>Вызов справки по командлетам PowerShell

Справка по командлетам доступна в следующих форматах:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Формат</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Как загружаемый модуль</p></td>
<td align="left"><p>Чтобы получить последнюю справку после загрузки модуля командлета, выполните указанные ниже действия.</p>
<ol>
<li><p>Откройте Windows PowerShell или интегрированную среду сценариев Windows PowerShell (ISE).</p></li>
<li><p>Чтобы загрузить командлеты для нужного модуля, введите одну из следующих команд:</p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Компонент App-V</th>
<th align="left">Команда для ввода</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Сервер App-V</p></td>
<td align="left"><p>Update-Help-Module AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Секвенсор App-V</p></td>
<td align="left"><p>Update-Help-Module AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Клиент App-V</p></td>
<td align="left"><p>Update-Help-Module AppvClient</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>На веб-страницах TechNet</p></td>
<td align="left"><p>Ознакомьтесь с разделом App-V в разделе <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> Автоматизация пакета оптимизации рабочей среды Microsoft для Windows PowerShell </a> .</p></td>
</tr>
</tbody>
</table>



Дополнительные сведения можно найти [в разделе как загрузить командлеты PowerShell и получить справку по командлетам](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).

## <a href="" id="bkmk-pvad-hidden"></a>Основной каталог виртуального приложения (PVAD) является скрытым, но его можно включить


Основной каталог виртуальных приложений (PVAD) будет скрыт в App-V 5,0 SP3, но его можно снова включить и сделать видимым с помощью одного из указанных ниже методов.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Метод</th>
<th align="left">Действия</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Использование параметра командной строки</p></td>
<td align="left"><p>Передайте <strong> параметр – EnablePVADControl в </strong> <strong>Sequencer.exe</strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Создание подраздела реестра</p></td>
<td align="left"><ol>
<li><p>В редакторе реестра перейдите к разделу: <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Если <code>Compatibility</code> подраздел не существует, его необходимо создать.</p>
</div>
<div>

</div></li>
<li><p>Создайте параметр DWORD с именем <strong> EnablePVADControl </strong> и установите для него значение <strong> 1 </strong> .</p>
<p><strong>Нулевое значение </strong> означает, что PVAD является скрытым.</p></li>
</ol></td>
</tr>
</tbody>
</table>



**Дополнительные сведения о PVAD:** При использовании секвенсора для создания пакета можно указать любой путь установки пакета. В предыдущих версиях App-V вам требовалось указать основной каталог виртуальных приложений (PVAD) для приложения в качестве пути. PVAD — это каталог, в который вы обычно устанавливаете приложение на локальном компьютере, если вы не используете App-V. Например, если вы устанавливаете Office на компьютере, PVAD, как правило, C:\\program Files Files\\Microsoft Office\\.

## <a href="" id="bkmk-pub-metadata-clientversion"></a>ClientVersion требуется для просмотра метаданных публикации App-V


В приложении App-V 5,0 с пакетом обновления 3 (SP3) при выполнении запроса метаданных на сервере публикации App-V необходимо указать указанные ниже значения.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Значение</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ClientVersion</strong></p></td>
<td align="left"><p>Если вы пропускаете <strong> </strong> параметр ClientVersion из запроса, метаданные не включают новую функциональность App-V 5,0 SP3.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>ClientOS</strong></p></td>
<td align="left"><p>Это значение нужно указывать только в том случае, если в качестве последовательности пакетов выбраны определенные клиентские операционные системы. Если вы выбрали вариант по умолчанию (все операционные системы), не указывайте это значение в запросе.</p>
<p>Если вы пропускаете <strong> </strong> параметр ClientOS из запроса, только пакеты, упорядоченные для поддержки любой операционной системы, отображаются в метаданных.</p></td>
</tr>
</tbody>
</table>



Синтаксис и примеры этого запроса приведены в разделе [Просмотр метаданных публикации сервера App-V Server](viewing-app-v-server-publishing-metadata.md).

## <a href="" id="bkmk-event-logs-moved"></a>Журналы событий App-V объединены


Перечисленные ниже журналы событий, ранее размещенные в ** &lt; компонентах &gt; журналов приложений и служб/Microsoft/AppV/App-V**, были перемещены в **журналы приложений и служб/Microsoft/AppV/ServiceLog**.

Чтобы просмотреть журналы, выберите **вид** &gt; **Показать аналитические и отладочные журналы** в приложении "Просмотр событий".

Клиентский каталог клиент-клиент — клиент клиента для интеграции: клиент клиент-службы клиента-PackageConfig Client-Vemgr Client-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary подсистемы-подсистемы ActiveX-AppPath подсистем

## Получение технологий для MDOP


App-V входит в состав пакета оптимизации рабочего стола Майкрософт (MDOP). MDOP входит в состав Microsoft Software Assurance. Дополнительные сведения о программе Software Assurance и приобретении MDOP можно найти в [статьях получение MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).






## Статьи по теме


[Заметки о выпуске для App-V 5.0 с пакетом обновления 3 (SP3)](release-notes-for-app-v-50-sp3.md)









