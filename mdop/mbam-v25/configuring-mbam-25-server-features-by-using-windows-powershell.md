---
title: Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell
description: Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822839"
---
# Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell


После установки программного обеспечения сервера MBAM 2,5 вы можете настроить серверные компоненты MBAM 2,5 с помощью командлетов Windows PowerShell или мастера конфигурации сервера MBAM. В этой статье описано, как настроить MBAM 2,5 с помощью командлетов Windows PowerShell. Чтобы использовать мастер, ознакомьтесь с [Разстройкой функций сервера MBAM 2,5](configuring-the-mbam-25-server-features.md).

## В этой статье


В этой статье приведены сведения об использовании Windows PowerShell для настройки MBAM:

-   [Как загрузить справку по Windows PowerShell для MBAM 2,5](#bkmk-load-posh-help)

-   [Получение справки о командлете Windows PowerShell MBAM](#bkmk-help-specific-cmdlet)

-   [Конфигурации, которые можно выполнять только с Windows PowerShell, но не с помощью мастера конфигурации сервера MBAM](#bkmk-config-only-posh)

-   [Необходимые условия и требования для использования Windows PowerShell для настройки функций сервера MBAM](#bkmk-prereqs-posh-mbamsvr)

-   [Настройка MBAM на удаленном компьютере с помощью Windows PowerShell](#bkmk-remote-config)

-   [Обязательные учетные записи и соответствующие параметры командлета Windows PowerShell](#bkmk-reqd-posh-accts)

Дополнительные сведения о командлетах Windows PowerShell **Get-MbamBitLockerRecoveryKey** и **Get-MbamTPMOwnerPassword** , которые используются для управления MBAM, приведены в разделе [Использование Windows PowerShell для администрирования MBAM 2,5](using-windows-powershell-to-administer-mbam-25.md).

## <a href="" id="bkmk-load-posh-help"></a>Как загрузить справку по Windows PowerShell для MBAM 2,5


Список командлетов Windows PowerShell на веб-сайте TechNet можно найти в разделе [Автоматизация пакета оптимизации рабочей среды Microsoft для Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).

**Загрузка справки по MBAM 2,5 для командлетов Windows PowerShell после установки серверного программного обеспечения MBAM**

1.  Откройте Windows PowerShell или интегрированную среду сценариев Windows PowerShell (ISE).

2.  Введите **Update-Help-Module Microsoft. MBAM**.

## <a href="" id="bkmk-help-specific-cmdlet"></a>Получение справки о командлете Windows PowerShell MBAM


Справка по Windows PowerShell для MBAM доступна в следующих форматах:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Формат справки Windows PowerShell</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>В командной строке Windows PowerShell введите <strong> </strong> &lt; <em> командлет Get-Help</em>&gt;</p></td>
<td align="left"><p>Чтобы загрузить последние командлеты Windows PowerShell, следуйте инструкциям, приведенным в предыдущем разделе о том, как загрузить справку Windows PowerShell для MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>На веб-страницах TechNet.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>В центре загрузки как файл Word. docx</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>В центре загрузки в виде PDF-файла</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a>Конфигурации, которые можно выполнять только с Windows PowerShell, но не с помощью мастера конфигурации сервера MBAM


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Конфигурации, которые можно выполнять только с помощью Windows PowerShell</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Установите веб-службы на отдельном компьютере из веб-приложений.</p></td>
<td align="left"><p>С помощью мастера необходимо установить веб-службы и веб-приложения на одном и том же компьютере.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Разрешите отчеты на отдельной точке служб Reporting Services, не устанавливая все объекты Configuration Manager.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Удалите все объекты из Configuration Manager.</p></td>
<td align="left"><p>В свою очередь, удаление объектов приводит к удалению всех данных о соответствии из Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Введите специальную строку подключения для баз данных.</p></td>
<td align="left"><p>Пример: чтобы настроить веб-приложения для работы с зеркальным отображением, необходимо использовать <strong> командлет Enable-MbamWebApplication, </strong> чтобы указать в строке соединения соответствующий синтаксис для резервной копии.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Пропустить проверку и настроить функцию, несмотря на то, что проверка готовности к установке завершилась сбоем.</p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

**Примечание**  Вы не можете отключить базы данных MBAM с помощью командлета Windows PowerShell или мастера настройки сервера MBAM. Чтобы предотвратить случайное удаление данных о соответствии и аудите, администраторы баз данных должны удалить базы данных вручную.

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a>Необходимые условия и требования для использования Windows PowerShell для настройки функций сервера MBAM


Перед началом настройки выполните следующие предварительные требования.

**Необходимые для учетной записи требования**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Предварительные</th>
<th align="left">Сведения или дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Создайте необходимые учетные записи.</p></td>
<td align="left"><p>Ознакомьтесь с <strong> необходимыми учетными записями и соответствующими параметрами командлета Windows PowerShell </strong> позже в этом разделе.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Учетные записи пользователей и группы, передаваемые в качестве параметров командлетам Windows PowerShell, должны быть действительными учетными записями домена.</p></td>
<td align="left"><p>Нельзя использовать локальные учетные записи.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Укажите учетные записи в формате нижнего уровня.</p></td>
<td align="left"><p>Примеры:</p>
<p>domainNetBiosName\userdomainNetBiosName\group</p></td>
</tr>
</tbody>
</table>

 

**Требования, связанные с разрешениями**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Предварительные</th>
<th align="left">Сведения или дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Вы должны быть администратором на локальном компьютере, на котором вы настраиваете функцию MBAM.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Используйте командную команду Windows PowerShell с повышенными привилегиями, чтобы выполнить все командлеты Windows PowerShell.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Только для <strong> командлета Enable-MbamDatabase </strong> :</p>
<p>Вы должны иметь &quot; разрешения на создание всех баз данных &quot; для экземпляра целевой базы данных Microsoft SQL Server.</p>
<p>Эта учетная запись пользователя должна входить в локальную группу администраторов или группу "операторы резервного копирования", чтобы зарегистрировать средство записи MBAM (VSS) Service Writer (служба теневого копирования тома).</p></td>
<td align="left"><p>По умолчанию администратор базы данных или системный администратор обладает необходимыми &quot; разрешениями на создание баз данных &quot; .</p>
<p></p>
<p>Дополнительные сведения о средстве записи VSS можно найти в разделе <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> Служба теневого копирования тома </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Для <strong> компонента интеграции System Center Configuration Manager </strong> :</p>
<p>У пользователя, который включает эту функцию, должны быть следующие права в Configuration Manager:</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Тип прав в Configuration Manager</th>
<th align="left">Необходимые права</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Права сайтов Configuration Manager:</p></td>
<td align="left"><p>- Read</p></td>
</tr>
<tr class="even">
<td align="left"><p>Права на сбор Configuration Manager:</p></td>
<td align="left"><p>- Создание, удаление, изменение и развертывание элементов конфигурации</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Разрешения элемента конфигурации Configuration Manager:</p></td>
<td align="left"><p>- Создание-удаление — чтение</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a>Настройка MBAM на удаленном компьютере с помощью Windows PowerShell


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Когда следует использовать эту возможность</strong></p></td>
<td align="left"><p>Если вы хотите настроить серверные компоненты MBAM 2,5 на удаленном компьютере. Командлеты Windows PowerShell выполняются на одном компьютере, и вы настраиваете эти функции на другом удаленном компьютере.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Что вам нужно сделать?</strong></p></td>
<td align="left"><p>Чтобы использовать Windows PowerShell для настройки функций сервера MBAM 2,5 на удаленном компьютере, необходимо выполнить указанные ниже действия.</p>
<ul>
<li><p>Убедитесь, что на удаленном компьютере установлено программное обеспечение сервера MBAM 2,5.</p></li>
<li><p>Используйте протокол службы поддержки безопасности учетных данных (CredSSP) для открытия сеанса Windows PowerShell.</p></li>
<li><p>Включите удаленное управление Windows (WinRM). Если вы не запустили службу WinRM и хотите правильно настроить ее, в <strong> командлете New-PSSession </strong> , описанный в этой таблице, появится сообщение об ошибке и инструкции по устранению этой проблемы. Дополнительные сведения об WinRM можно найти <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> в разделе Использование удаленного управления Windows </a> .</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Зачем это нужно сделать</strong></p></td>
<td align="left"><p>Этот протокол позволяет командлетам Windows PowerShell подключаться к доменным службам Active Directory с помощью учетных данных администратора пользователя. При запуске сеанса Windows PowerShell без этого протокола может возникнуть ошибка проверки.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Запуск сеанса Windows PowerShell с протоколом CredSSP</strong></p></td>
<td align="left"><p>Введите следующий код в командной строке Windows PowerShell:</p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p>Следующий код демонстрирует пример.</p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a>Обязательные учетные записи и соответствующие параметры командлета Windows PowerShell


В следующей таблице описаны учетные записи, необходимые для настройки функций сервера MBAM 2,5. В нем также перечислены соответствующие командлеты и параметры Windows PowerShell, для которых необходимо указать учетную запись во время настройки.

Тип параметра командлета (пользователь или группа) описание Enable-MBAMDatabase

AccessAccount

Пользователь или группа

Укажите пользователя или группу домена, у которых есть разрешение на чтение и запись в эту базу данных, чтобы предоставить веб-приложениям доступ к данным и отчетам в этой базе данных. Если значением является пользователь домена, параметр **WebServiceApplicationPoolCredential** , который используется при запуске командлета **Enable-MbamWebApplication** , должен использовать одну и ту же учетную запись пользователя. Если значением является группа "Пользователи домена", учетная запись домена, используемая параметром **WebServiceApplicationPoolCredential** , должна быть членом этой группы.

ReportAccount

Пользователь или группа

Укажите группу пользователей или пользователей домена с разрешением только на чтение в эту базу данных, чтобы предоставить MBAM отчеты для доступа к данным о соответствии и аудите. Если значением является пользователь домена, параметр **ComplianceAndAuditDBCredential** командлета **Enable-MbamReport** должен использовать одну и ту же учетную запись пользователя. Если значением является группа "Пользователи домена", учетная запись домена, используемая параметром **ComplianceAndAuditDBCredential** , должна быть членом этой группы.

Enable-MbamReport

ComplianceAndAuditDBCredential

Пользователь

Указывает учетные данные администратора, которые использует локальный экземпляр служб SSRS для подключения к базе данных соответствия MBAM и аудита. Пользователь домена в учетных данных администратора должен совпадать с учетной записью пользователя, используемой для параметра **ReportAccount** , который используется при запуске командлета **Enable-MbamDatabase** . Если в качестве параметра **ReportAccount** используется группа "Пользователи домена", эта учетная запись должна быть членом этой группы.

**Важно!**  Учетная запись, указанная в учетных данных администратора, должна иметь ограниченные права для повышения безопасности. Кроме того, пароль учетной записи должен быть установлен в значение "не ограничен".

 

ReportsReadOnlyAccessGroup

Группа

Указывает группу пользователей домена с разрешениями на чтение для отчетов. Указанная группа должна находиться в той же группе, которая используется для параметра **ReportsReadOnlyAccessGroup** в командлете **Enable-MbamWebApplication** .

Enable-MBAMWebApplication

AdvancedHelpdeskAccessGroup

Группа

Указывает группу "Пользователи домена", которая имеет доступ ко всем областям веб-сайта администрирования и мониторинга, кроме области "отчеты".

HelpdeskAccessGroup

Группа

Указывает группу "Пользователи домена", которая имеет доступ к разделу " **Управление TPM** и **восстановлением диска** " на веб-сайте администрирования и мониторинга.

ReportsReadOnlyAccessGroup

Группа

Указывает группу "Пользователи домена", которая имеет разрешение на чтение в области " **отчеты** " на веб-сайте администрирования и мониторинга. Указанная группа должна находиться в той же группе, которая используется для параметра **ReportsReadOnlyAccessGroup** в командлете **Enable-MbamReport** .

WebServiceApplicationPoolCredential

Пользователь

Указывает пользователя домена, который будет использоваться пулом приложений для веб-приложений MBAM. Она должна быть той же учетной записью пользователя домена, которая указана в параметре **AccessAccount** командлета **Enable-MbamDatabase** . Если при запуске командлета **Enable-MbamDatabase** в качестве параметра **AccessAccount** используется группа "Пользователи домена", пользователь домена, указанный здесь, должен быть членом этой группы. Если вы не указали учетные данные администратора, используются учетные данные администратора, которые были указаны в предыдущем включенном веб-приложении. Все веб-приложения используют один и тот же идентификатор пула приложений. Если задано несколько значений, используется последнее указанное значение.

**Важно!**  Для повышения безопасности укажите учетную запись, указанную в разделе Учетные данные администратора, для ограничения прав пользователя. Кроме того, установите для пароля учетной записи значение бессрочной. Убедитесь в том, что встроенная учетная запись IIS \ _IUSRS или учетная запись, используемая для параметра **WebServiceApplicationPoolCredential** , была добавлена в "олицетворение" клиента после настройки локальной безопасности для **проверки подлинности** .

Чтобы просмотреть локальные параметры безопасности, откройте **Редактор локальной политики безопасности**, разверните узел **Локальные политики** , выберите узел **Назначение прав пользователя** , а затем дважды щелкните **олицетворение клиента после проверки подлинности** и войдите в систему в качестве параметров групповой политики **для пакетного задания** в области сведений.

 

 




## Статьи по теме


[Настройка компонентов сервера MBAM 2.5 Server](configuring-the-mbam-25-server-features.md)

[Проверка конфигурации компонентов MBAM 2.5 Server](validating-the-mbam-25-server-feature-configuration.md)

[Использование Windows PowerShell для администрирования MBAM 2.5](using-windows-powershell-to-administer-mbam-25.md)

 
## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





