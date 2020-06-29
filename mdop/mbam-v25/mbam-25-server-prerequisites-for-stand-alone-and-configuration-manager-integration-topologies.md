---
title: Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций
description: Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825999"
---
# Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций


Прежде чем приступить к установке Microsoft BitLocker Administration и Monitoring (MBAM), необходимо выполнить необходимые требования, описанные в этой статье. Эти требования применимы к изолированной топологии MBAM и топологии интеграции System Center Configuration Manager.

Если вы развертываете MBAM с помощью System Center Configuration Manager, необходимо выполнить дополнительные требования, которые указаны в [требованиях к топологии интеграции Configuration Manager для MBAM 2,5 Server](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).

Список поддерживаемых аппаратных и операционных систем для MBAM можно найти в разделе [Поддерживаемые конфигурации MBAM 2,5](mbam-25-supported-configurations.md).

**Важно.**  
Если вы используете BitLocker без MBAM, необходимо дешифровать диск и затем очистить TPM с помощью TPM. msc. MBAM не может сменить владельца доверенного платформенного модуля, если клиентский компьютер уже зашифрован и пароль владельца доверенного платформенного модуля создан.



## Обязательные роли MBAM и учетные записи


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
<td align="left"><p>Группы, созданные в доменных службах Active Directory (AD DS)</p></td>
<td align="left"><p><a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"> </a> Описание этих групп и учетных записей MBAM в разделе планирование групп 2,5 и учетных записей.</p></td>
</tr>
</tbody>
</table>



## Предварительные условия для базы данных восстановления


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
<td align="left"><p>Поддерживаемая версия SQL Server</p></td>
<td align="left"><p>Установка Microsoft SQL Server с SQL_Latin1_General_CP1_CI_AS параметрами сортировки.</p>
<p>Поддерживаемые <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Требуемые разрешения SQL Server</p></td>
<td align="left"><p>Необходимые разрешения:</p>
<ul>
<li><p>Роли сервера входа для экземпляра SQL Server:</p>
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
<td align="left"><p>Необязательный-Установка компонента прозрачного шифрования данных (TDE), доступного в SQL Server</p></td>
<td align="left"><p>Функция TDE SQL Server осуществляет шифрование и расшифровку данных и файлов журнала в режиме реального времени, что поможет вам соблюдать законы, правила и положения, применимые к различным отраслям.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>TDE выполняет расшифровку сведений о базе данных в режиме реального времени. Это означает, что если вы просматриваете данные ключа восстановления в базе данных SQL Server и вошли в систему под учетной записью, обладающей разрешениями для базы данных, отображается информация ключа для восстановления. Подробнее об TDEах можно узнать в статье <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> рекомендации по безопасности в MBAM 2,5 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Службы ядра СУБД SQL Server</p></td>
<td align="left"><p>Службы SQL Server Database Engine должны быть установлены и запущены во время установки сервера MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3,0 или более поздняя версия</p></td>
<td align="left"><p>Windows PowerShell не нужно устанавливать на сервере базы данных восстановления, если вы используете Windows PowerShell для настройки базы данных с удаленного компьютера.</p></td>
</tr>
</tbody>
</table>



## Предварительные условия для базы данных соответствия требованиям и аудита


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
<td align="left"><p>Поддерживаемая версия SQL Server</p></td>
<td align="left"><p>Установка SQL Server с SQL_Latin1_General_CP1_CI_AS параметрами сортировки.</p>
<p>Поддерживаемые <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Требуемые разрешения SQL Server</p></td>
<td align="left"><p>Необходимые разрешения:</p>
<ul>
<li><p>Роли сервера входа для экземпляра SQL Server:</p>
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
<td align="left"><p>Необязательный-Установка функции шифрования прозрачных данных (TDE) в SQL Server</p></td>
<td align="left"><p>Функция TDE SQL Server осуществляет шифрование и расшифровку данных и файлов журнала в режиме реального времени, что поможет вам соблюдать законы, правила и положения, применимые к различным отраслям.</p>
<p>TDE выполняет расшифровку сведений о базе данных в режиме реального времени. Это означает, что если вы просматриваете данные ключа восстановления в базе данных SQL Server и вошли в систему под учетной записью, обладающей разрешениями для базы данных, отображается информация ключа для восстановления. Подробнее об TDEах можно узнать в статье <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> рекомендации по безопасности в MBAM 2,5 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Службы ядра СУБД SQL Server</p></td>
<td align="left"><p>Службы SQL Server Database Engine должны быть установлены и запущены во время установки сервера MBAM. Однако SQL Server можно запускать удаленно. Он не должен находиться на том же сервере, на котором выполняется установка программного обеспечения сервера MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3,0 или более поздняя версия</p></td>
<td align="left"><p>Если вы используете Windows PowerShell для настройки базы данных с удаленного компьютера, не нужно устанавливать Windows PowerShell на сервер базы данных соответствия требованиям и аудита.</p></td>
</tr>
</tbody>
</table>



## Предварительные требования для отчетов


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
<td align="left"><p>Поддерживаемая версия SQL Server</p></td>
<td align="left"><p>Установка SQL Server с SQL_Latin1_General_CP1_CI_AS параметрами сортировки.</p>
<p>Поддерживаемые <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Службы SQL Server Reporting Services (SSRS)</p></td>
<td align="left"><p>Службы SSRS должны быть установлены и запущены во время установки сервера MBAM.</p>
<p>Настройка SSRS в &quot; основном &quot; режиме, а не в режиме "в конфигурации" или в &quot; SharePoint &quot; .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Права экземпляра служб SSRS — необходимы для настройки отчетов только в том случае, если вы устанавливаете базы данных на отдельном сервере с сервера, на котором настроены отчеты.</p></td>
<td align="left"><p>Необходимые права для экземпляра:</p>
<ul>
<li><p>Создание папок</p></li>
<li><p>Публикация отчетов</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows PowerShell 3,0 или более поздняя версия</p></td>
<td align="left"><p>Если вы используете Windows PowerShell для настройки базы данных с удаленного компьютера, вам не нужно устанавливать Windows PowerShell на этом сервере базы данных.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a>Предварительные требования для сервера администрирования и мониторинга


В следующей таблице перечислены требования к установке сервера администрирования и мониторинга MBAM.

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
<td align="left"><p>Роль веб-сервера Windows Server</p></td>
<td align="left"><p>Эту роль необходимо добавить в серверную операционную систему, которая поддерживается для компонента администрирования и мониторинга сервера.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Средства управления веб-сервером (IIS)</p></td>
<td align="left"><p>Выберите пункт <strong> сценарии и инструменты управления IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>SSL-сертификат</strong></p></td>
<td align="left"><p>Необязательно. Для безопасной связи между клиентскими компьютерами и веб-службами необходимо получить и установить сертификат, подписанный надежным центром безопасности.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Службы ролей веб-сервера</p></td>
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
<td align="left"><p>Возможности Windows Server</p></td>
<td align="left"><p><strong>Возможности .NET Framework 4,5:</strong></p>
<ul>
<li><p><strong>Платформа .NET Framework 4,5 или 4,6</strong></p>
<ul>
<li><p><strong>Платформа Windows Server 2016 </strong> - .net Framework 4,6 уже установлена для этих версий Windows Server, но ее необходимо включить.</p></li>  
<li><p><strong>Windows Server 2012 или Windows Server 2012 R2 </strong> - .net Framework 4,5 уже установлены для этих версий Windows Server, но необходимо включить ее.</p></li>
<li><p><strong>Windows Server 2008 R2 </strong> - .net Framework 4,5 не входит в состав windows Server 2008 R2, поэтому необходимо <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> загрузить Microsoft .NET Framework 4,5 </a> и установить его отдельно.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Если вы выполняете обновление с MBAM 2,0 или MBAM 2,0 SP1 и вам нужно установить .NET Framework 4,5, ознакомьтесь с <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> заметками о выпуске для MBAM 2,5 </a> для получения дополнительных необходимых шагов по выполнению веб-сайтов.</p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong>Активация WCF</strong></p>
<ul>
<li><p>Активация по HTTP</p></li>
<li><p>Активация не по протоколу HTTP (только для Windows Server 2008, 2012 и 2012 R2)</p>
<p></p></li>
</ul></li>
<li><p><strong>Активация по протоколу TCP</strong></p></li>
</ul>
<p><strong>Служба активации процессов Windows.</strong></p>
<ul>
<li><p>Модель процесса</p></li>
<li><p>Среда .NET Framework</p></li>
<li><p>API конфигурации</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">Загрузка ASP.NET MVC 4</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Имя субъекта-службы (SPN)</p></td>
<td align="left"><p>Для веб-приложений требуется имя SPN для имени виртуального узла под учетной записью домена, которую вы используете для пулов веб-приложений.</p>
<p>Если ваши административные права разрешают вам создавать SPN в доменных службах Active Directory, MBAM создает имя участника-службы. <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> </a> Сведения о правах, необходимых для создания SPN, можно найти в SetSPN.</p>
<p>Если у вас нет прав администратора для создания SPN, вы должны обратиться к администраторам Active Directory в вашей организации, чтобы создать для вас SPN, выполнив следующую команду:</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>В примере кода имя виртуального узла — mbamvirtual.contoso.com, а учетная запись домена, используемая для пулов веб-приложений, — contoso\mbamapppooluser.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>При настройке балансировки нагрузки используйте одну и ту же учетную запись пула приложений на всех серверах.</p>
</div>
<div>

</div>
<p>Дополнительные сведения о регистрации SPN для полных, NetBIOS-и настраиваемых имен узлов вы можете найти <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> в разделе Планирование защиты сайтов MBAM </a> .</p></td>
</tr>
</tbody>
</table>



## Предварительные требования для портала самообслуживания


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
<td align="left"><p>Поддерживаемая версия Windows Server</p></td>
<td align="left"><p>Поддерживаемые <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">Загрузка ASP.NET MVC 4</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Средства управления IIS для веб-служб</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Имя субъекта-службы (SPN)</p></td>
<td align="left"><p>Для веб-приложений требуется имя SPN для имени виртуального узла под учетной записью домена, которую вы используете для пулов веб-приложений.</p>
<p>Если ваши административные права разрешают вам создавать SPN в доменных службах Active Directory, MBAM создает имя участника-службы. <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> </a> Сведения о правах, необходимых для создания SPN, можно найти в SetSPN.</p>
<p>Если у вас нет прав администратора для создания имен участников-служб, вы должны обратиться к администраторам Active Directory в своей организации, чтобы создать для вас SPN, выполнив следующую команду:</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>В примере кода имя виртуального узла — mbamvirtual.contoso.com, а учетная запись домена, используемая для пулов веб-приложений, — contoso\mbamapppooluser.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>При настройке балансировки нагрузки используйте одну и ту же учетную запись пула приложений на всех серверах.</p>
</div>
<div>

</div>
<p>Дополнительные сведения о регистрации SPN для полных, NetBIOS-и настраиваемых имен узлов вы можете найти <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> в разделе Планирование защиты сайтов MBAM </a> .</p></td>
</tr>
</tbody>
</table>



## Предварительные требования для рабочей станции управления


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
<td align="left"><p>Перед установкой клиента MBAM Скачайте шаблоны групповой политики MBAM, <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> чтобы получить шаблоны групповой политики для MDOP, </a> и настройте их с помощью параметров, которые вы хотите реализовать на вашем предприятии для шифрования диска BitLocker.</p></td>
<td align="left"><p>Прежде чем устанавливать клиент MBAM, выполните указанные ниже действия.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Что делать</th>
<th align="left">Где найти инструкции</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Копирование шаблонов групповой политики MBAM</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Копирование шаблонов групповой политики MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Изменение параметров групповой политики</p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Изменение параметров групповой политики MBAM 2.5</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## Статьи по теме


[Подготовка среды для развертывания MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Планирование развертывания MBAM 2.5](planning-to-deploy-mbam-25.md)

[Поддерживаемые конфигурации MBAM 2.5](mbam-25-supported-configurations.md)




## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




