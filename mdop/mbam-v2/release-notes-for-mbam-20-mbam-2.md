---
title: Заметки о выпуске для MBAM 2.0
description: Заметки о выпуске для MBAM 2.0
author: dansimp
ms.assetid: c3f16cf3-94f2-47ac-b3a4-3dc505c6a8dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d5d3c7d539cf2828d28c1844321bc34ab7736ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825589"
---
# Заметки о выпуске для MBAM 2.0


Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.

Внимательно прочитайте эти заметки о выпуске, прежде чем устанавливать Microsoft BitLockerAdministration и мониторинг (MBAM) 2.0. Эти заметки о выпуске содержат сведения, необходимые для успешной установки BitLockerAdministration и мониторинга версии 2.0, и содержат сведения, недоступные в документации по продукту. Если существует разница между этими заметками о выпуске и другой документацией MBAM 2.0, Последнее изменение должно считаться полномочным. Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.

## <a href="" id="---------mbam-2-0-known-issues"></a> Известные проблемы с MBAM 2.0


В этом разделе содержатся заметки о выпуске MBAM 2.0.

### При запуске MBAM с помощью Microsoft System Center Configuration Manager 2007 поле "имя компьютера" не отображается в отчетах о соответствии требованиям, предъявляемых к компьютеру и требованиям BitLocker Enterprise

При использовании MBAM с Configuration Manager 2007 поле "имя компьютера" может быть пустым в соответствии с подробными сведениями о требованиях к системе BitLocker и требованиям BitLocker Enterprise.

ВРЕМЕННОе решение: нет.

### После обновления инфраструктуры сервера MBAM не удается обновить отчет о соответствии требованиям предприятия

Если вы используете изолированную топологию MBAM и обновляете инфраструктуру сервера с версии 1,0 на 2,0, отчет о соответствии требованиям предприятия не будет обновляться.

ВРЕМЕННОе решение: после обновления выполните следующий сценарий в базе данных соответствия требованиям и аудита.

```sql
-- =============================================
-- Script Template
-- =============================================

DECLARE @DatabaseName nvarchar(255);
SET @DatabaseName = DB_NAME()

USE msdb;

DECLARE @JobID BINARY(16)
SELECT @JobID = job_id
FROM msdb.dbo.sysjobs
WHERE (name = N'CreateCache')

if (@JobID IS NOT NULL)
BEGIN
    EXEC dbo.sp_delete_job
         @job_name = N'CreateCache';
END

EXEC dbo.sp_add_job
    @job_name = N'CreateCache',
    @enabled = 1;

EXEC dbo.sp_add_jobstep
     @job_name = N'CreateCache',
     @step_name = N'Copy Data',
     @subsystem = N'TSQL',
     @command = N'EXEC [ComplianceCore].UpdateCache',
     @database_name = @DatabaseName,
     @retry_attempts = 5,
     @retry_interval = 5;


EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 010000,
     @active_end_time = 020000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 070000,
     @active_end_time = 080000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 130000,
     @active_end_time = 140000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1pm';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 190000,
     @active_end_time = 200000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7pm';

EXEC dbo.sp_add_jobserver
     @job_name = N'CreateCache';
```

### Отчеты на портале службы поддержки выводят предупреждение, если не настроен протокол SSL в SSRS

Если для служб SQL Server Reporting Services (SSRS) не настроено использование протокола SSL, при установке сервера MBAM URL-адрес для отчетов будет установлен в значение HTTP вместо HTTPS. Если затем перейти на портал службы поддержки и выбрать отчет, появится следующее сообщение: "только безопасное содержимое отображается".

ВРЕМЕННОе решение: чтобы отобразить отчет, выберите пункт **Показать весь контент**. Чтобы устранить эту ошибку, перейдите на компьютер MBAM, на котором установлены службы SQL Server Reporting Services, запустите **Диспетчер конфигураций служб Reporting Services**и выберите **URL-адрес Web Service**. Выберите необходимый SSL-сертификат для сервера, введите соответствующий порт SSL (порт по умолчанию — 443), а затем нажмите кнопку **Применить**.

### Экземпляры базы данных Configuration Manager, отличные от используемых по умолчанию, не поддерживаются

MBAM ищет только экземпляр базы данных Configuration Manager по умолчанию в Configuration Manager 2007 и SystemCenter2012 ConfigurationManager. Если вы используете экземпляр, не заданный по умолчанию, вы не сможете установить MBAM.

ВРЕМЕННОе решение: нет.

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a>При нажатии кнопки "назад" в отчете "Сводка соответствия требованиям" может возникнуть ошибка

При детализации отчета "Сводка соответствия требованиям" и нажатии **обратной** ссылки в отчете SSRS может возникать ошибка.

ВРЕМЕННОе решение: нет.

### Шифрование только использованного пространства не работает должным образом

Если после установки клиента MBAM вы зашифруете компьютер в первый раз, а вы настроили объект групповой политики, чтобы реализовать шифрование только занятого пространства, MBAM ошибочно шифрует весь диск вместо того, чтобы шифровать использованное место на диске. Если при установке клиента MBAM компьютер уже был зашифрован и вы установили тот же объект групповой политики, шифрование работает правильно и шифрует только используемое дисковое пространство на компьютере.

ВРЕМЕННОе решение: нет.

### Неправильное отображение стойкости шифра в отчете о соответствии компьютера

Если вы не настроили определенную стойкость шифра в разделе **Выбор метода шифрования диска и объекта групповой политики стойкости шифра** , то отчет о соответствии компьютера в топологии интеграции Configuration Manager всегда отображается как "неизвестно" для стойкости шифра, даже если стойкость шифра использует значение по умолчанию для 128-битного шифрования. В отчете показана правильная стойкость шифра, если в объекте групповой политики указана определенная стойкость шифра.

ВРЕМЕННОе решение: всегда устанавливайте определенную стойкость шифра в разделе **Выбор метода шифрования диска и объекта групповой политики стойкости шифра** .

### При распределении состояния соответствия по типу диска старые данные отображаются после обновления элементов конфигурации.

После того как вы обновите элементы конфигурации MBAM в SystemCenter2012 ConfigurationManager, распределение состояния соответствия по типам дисков на панели мониторинга соответствия требованиям для предприятий BitLocker показывает данные, основанные на данных из старых версий элементов конфигурации.

ВРЕМЕННОе решение: нет. Изменение элементов конфигурации MBAM не поддерживается, и отчет может не отображаться должным образом.

### Конфигурация усиленной безопасности может привести к тому, что отчеты отображаются неправильно

Если включена конфигурация усиленной безопасности Internet Explorer (ESC), при попытке просмотреть отчеты на сервере MBAM может появиться сообщение "отказано в доступе". По умолчанию функция ESC включена, чтобы защитить сервер, уменьшая уязвимость сервера для потенциальных атак, которые могут возникать в результате веб-содержимого и сценариев приложений.

ВРЕМЕННОе решение: Если при попытке просмотреть отчеты на сервере MBAM появляется сообщение "отказано в доступе", вы можете задать объект групповой политики или изменить параметры по умолчанию вручную в своем изображении, чтобы отключить конфигурацию усиленной безопасности. Кроме того, вы можете просматривать отчеты с другого компьютера, на котором не включена ESC.

### Установка сервера MBAM завершается сбоем при переходе с SQL Server 2008 на SQL Server 2012

При переходе с SQL Server 2008 на SQL Server 2012 и последующей попытке установить базу данных соответствия требованиям и аудита или базу данных восстановления, установка завершается сбоем и откатывается назад. Эта проблема возникает из-за того, что необходимый файл SQLCMD.exe был удален во время обновления SQL и не удается найти в установщике MBAM. Строки в файле журнала MSI могут выглядеть примерно следующим образом:

Центр восстановления RunDbInstallScript: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery DB: dbInstance-xxxxxx\\I01RunDbInstallScript DB: sqlScript-c:\\program Files Files\\Microsoft\\Microsoft DB: dbname-Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript \ _Recovery \ _and \ _HardwareRunDbInstallScript восстановления базы данных ЦС: MBAM defaultFileName \ _Recovery \ _and \ _HardwareRunDbInstallScript центра восстановления базы данных ЦС: MBAM-defaultDataPath Центр восстановления I01\\MSSQL\\DATA\\RunDbInstallScript: defaultLogPath-K:\\MSSQL\\MSSQL10. Центр восстановления I01\\MSSQL\\Data\\RunDbInstallScript: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\program Files Files\\Microsoft\\Microsoft, администрирование BitLocker и Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript Recovery DB: Начало работы с базой данных восстановления. После этого файл журнала восстановления для Jet-файла будет находиться в разделе" журнал "базы данных ЦС для восстановления:

Установщик Windows MBAM Server имеет встроенные сведения о том, как найти путь SQLCMD.exe, просмотрев строковое значение пути в реестре в разделе HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup. Ключ по-прежнему отображается во время миграции из SQL Server 2008 в SQL Server 2012, но путь, на который ссылается значение данных, не содержит SQLCMD.exe файл, так как процесс обновления SQL удалил файл.

Временное решение: временно переименуйте строковое значение HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup Path на **path \ _OLD**, а затем снова запустите установщик Windows Server MBAM. После успешного завершения установки и создания баз данных в SQL Server 2012 переименуйте **путь \ _OLD** в значение **path**.

## Исправления и статьи базы знаний для MBAM 2.0


В этом разделе содержатся исправления и статьи базы знаний для MBAM 2.0.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Статья базы знаний</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Ссылка</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2831166</p></td>
<td align="left"><p>Установка системы администрирования и наблюдения (MBAM 2,0) для Microsoft BitLocker завершается сбоем, если &quot; уже установлены объекты System Center cm&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)">support.microsoft.com/kb/2831166/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870849</p></td>
<td align="left"><p>Пользователи не могут получить ключ восстановления BitLocker с помощью портала самообслуживания MBAM 2.0.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)">support.microsoft.com/kb/2870849/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2756402</p></td>
<td align="left"><p>Клиент MBAM в описании события не сможет выполнить событие с кодом 4 и кодом ошибки 0x8004100E</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620287</p></td>
<td align="left"><p>Сообщение об ошибке "ошибка сервера в"/Reports "приложение" при выборе вкладки "отчеты" в MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)">support.microsoft.com/kb/2620287/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Ошибка при открытии отчетов о соответствии требованиям предприятия или компьютера в MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>Корпоративная отчетность MBAM не обновляется</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2712461</p></td>
<td align="left"><p>Установка MBAM на контроллере домена не поддерживается</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)">support.microsoft.com/kb/2712461/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2876732</p></td>
<td align="left"><p>Сообщение об ошибке с кодом 0x80071a90 во время отдельного процесса или настройки интеграции Configuration Manager для MBAM 2.0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)">support.microsoft.com/kb/2876732/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2754259</p></td>
<td align="left"><p>MBAM и безопасная сетевая связь</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)">support.microsoft.com/kb/2754259/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>Установка MBAM 2.0 завершается сбоем во время интеграции Configuration Manager с SQL Server 2008</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2668533</p></td>
<td align="left"><p>Установка MBAM завершается сбоем, если неправильно настроена служба SSRS SQL</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)">support.microsoft.com/kb/2668533/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870847</p></td>
<td align="left"><p>Программа установки MBAM 2,0 завершает работу с &quot; ошибкой при получении параметров роли сервера Configuration Manager для &#39;точки служб Reporting Services&#39; роли&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)">support.microsoft.com/kb/2870847/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2870839</p></td>
<td align="left"><p>Корпоративные отчеты MBAM 2.0 не обновляются в автономной топологии MBAM 2.0 из-за сбоя в работе CreateCache задания SQL</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)">support.microsoft.com/kb/2870839/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>Корпоративная отчетность MBAM не обновляется</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2935997</p></td>
<td align="left"><p>MBAM поддерживаемые компьютеры с неправильными отчетами о соответствия требованиям включают Неподдерживаемые продукты</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)">support.microsoft.com/kb/2935997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2612822</p></td>
<td align="left"><p>Запись компьютера отклонена в MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)">support.microsoft.com/kb/2612822/EN-US</a></p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Сведения о MBAM 2.0](about-mbam-20-mbam-2.md)

 

 





