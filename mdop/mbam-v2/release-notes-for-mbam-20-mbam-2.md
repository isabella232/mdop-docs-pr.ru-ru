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
# <span data-ttu-id="b9604-103">Заметки о выпуске для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b9604-103">Release Notes for MBAM 2.0</span></span>


<span data-ttu-id="b9604-104">Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="b9604-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="b9604-105">Внимательно прочитайте эти заметки о выпуске, прежде чем устанавливать Microsoft BitLockerAdministration и мониторинг (MBAM) 2.0.</span><span class="sxs-lookup"><span data-stu-id="b9604-105">Read these release notes thoroughly before you install Microsoft BitLockerAdministration and Monitoring(MBAM)2.0.</span></span> <span data-ttu-id="b9604-106">Эти заметки о выпуске содержат сведения, необходимые для успешной установки BitLockerAdministration и мониторинга версии 2.0, и содержат сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="b9604-106">These release notes contain information that is required to successfully install BitLockerAdministration and Monitoring2.0 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="b9604-107">Если существует разница между этими заметками о выпуске и другой документацией MBAM 2.0, Последнее изменение должно считаться полномочным.</span><span class="sxs-lookup"><span data-stu-id="b9604-107">If there is a difference between these release notes and other MBAM2.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="b9604-108">Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.</span><span class="sxs-lookup"><span data-stu-id="b9604-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-known-issues"></a> <span data-ttu-id="b9604-109">Известные проблемы с MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b9604-109">MBAM2.0 Known Issues</span></span>


<span data-ttu-id="b9604-110">В этом разделе содержатся заметки о выпуске MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="b9604-110">This section contains release notes for MBAM2.0.</span></span>

### <span data-ttu-id="b9604-111">При запуске MBAM с помощью Microsoft System Center Configuration Manager 2007 поле "имя компьютера" не отображается в отчетах о соответствии требованиям, предъявляемых к компьютеру и требованиям BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="b9604-111">Computer Name field may not appear in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you run MBAM with Microsoft System Center Configuration Manager 2007</span></span>

<span data-ttu-id="b9604-112">При использовании MBAM с Configuration Manager 2007 поле "имя компьютера" может быть пустым в соответствии с подробными сведениями о требованиях к системе BitLocker и требованиям BitLocker Enterprise.</span><span class="sxs-lookup"><span data-stu-id="b9604-112">The Computer Name field may be blank in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you use MBAM with Configuration Manager 2007.</span></span>

<span data-ttu-id="b9604-113">ВРЕМЕННОе решение: нет.</span><span class="sxs-lookup"><span data-stu-id="b9604-113">WORKAROUND: None.</span></span>

### <span data-ttu-id="b9604-114">После обновления инфраструктуры сервера MBAM не удается обновить отчет о соответствии требованиям предприятия</span><span class="sxs-lookup"><span data-stu-id="b9604-114">Enterprise Compliance Report fails to update after you upgrade the Stand-alone MBAM server infrastructure</span></span>

<span data-ttu-id="b9604-115">Если вы используете изолированную топологию MBAM и обновляете инфраструктуру сервера с версии 1,0 на 2,0, отчет о соответствии требованиям предприятия не будет обновляться.</span><span class="sxs-lookup"><span data-stu-id="b9604-115">If you are using the MBAM Stand-alone topology, and you upgrade the server infrastructure from version 1.0 to 2.0, the Enterprise Compliance Report fails to update.</span></span>

<span data-ttu-id="b9604-116">ВРЕМЕННОе решение: после обновления выполните следующий сценарий в базе данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="b9604-116">WORKAROUND: After the upgrade, run the following script on the Compliance and Audit Database:</span></span>

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

### <span data-ttu-id="b9604-117">Отчеты на портале службы поддержки выводят предупреждение, если не настроен протокол SSL в SSRS</span><span class="sxs-lookup"><span data-stu-id="b9604-117">Reports in the Help Desk Portal display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="b9604-118">Если для служб SQL Server Reporting Services (SSRS) не настроено использование протокола SSL, при установке сервера MBAM URL-адрес для отчетов будет установлен в значение HTTP вместо HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b9604-118">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="b9604-119">Если затем перейти на портал службы поддержки и выбрать отчет, появится следующее сообщение: "только безопасное содержимое отображается".</span><span class="sxs-lookup"><span data-stu-id="b9604-119">If you then browse to the Help Desk Portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="b9604-120">ВРЕМЕННОе решение: чтобы отобразить отчет, выберите пункт **Показать весь контент**.</span><span class="sxs-lookup"><span data-stu-id="b9604-120">WORKAROUND: To show the report, click **Show All Content**.</span></span> <span data-ttu-id="b9604-121">Чтобы устранить эту ошибку, перейдите на компьютер MBAM, на котором установлены службы SQL Server Reporting Services, запустите **Диспетчер конфигураций служб Reporting Services**и выберите **URL-адрес Web Service**.</span><span class="sxs-lookup"><span data-stu-id="b9604-121">To address this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="b9604-122">Выберите необходимый SSL-сертификат для сервера, введите соответствующий порт SSL (порт по умолчанию — 443), а затем нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="b9604-122">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="b9604-123">Экземпляры базы данных Configuration Manager, отличные от используемых по умолчанию, не поддерживаются</span><span class="sxs-lookup"><span data-stu-id="b9604-123">Non-default instances of the Configuration Manager database are not supported</span></span>

<span data-ttu-id="b9604-124">MBAM ищет только экземпляр базы данных Configuration Manager по умолчанию в Configuration Manager 2007 и SystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="b9604-124">MBAM looks only for the default instance of the Configuration Manager database in Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="b9604-125">Если вы используете экземпляр, не заданный по умолчанию, вы не сможете установить MBAM.</span><span class="sxs-lookup"><span data-stu-id="b9604-125">If you use a non-default instance, you cannot install MBAM.</span></span>

<span data-ttu-id="b9604-126">ВРЕМЕННОе решение: нет.</span><span class="sxs-lookup"><span data-stu-id="b9604-126">WORKAROUND: None.</span></span>

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a><span data-ttu-id="b9604-127">При нажатии кнопки "назад" в отчете "Сводка соответствия требованиям" может возникнуть ошибка</span><span class="sxs-lookup"><span data-stu-id="b9604-127">Clicking “Back” in the Compliance Summary report might throw an error</span></span>

<span data-ttu-id="b9604-128">При детализации отчета "Сводка соответствия требованиям" и нажатии **обратной** ссылки в отчете SSRS может возникать ошибка.</span><span class="sxs-lookup"><span data-stu-id="b9604-128">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="b9604-129">ВРЕМЕННОе решение: нет.</span><span class="sxs-lookup"><span data-stu-id="b9604-129">WORKAROUND: None.</span></span>

### <span data-ttu-id="b9604-130">Шифрование только использованного пространства не работает должным образом</span><span class="sxs-lookup"><span data-stu-id="b9604-130">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="b9604-131">Если после установки клиента MBAM вы зашифруете компьютер в первый раз, а вы настроили объект групповой политики, чтобы реализовать шифрование только занятого пространства, MBAM ошибочно шифрует весь диск вместо того, чтобы шифровать использованное место на диске.</span><span class="sxs-lookup"><span data-stu-id="b9604-131">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="b9604-132">Если при установке клиента MBAM компьютер уже был зашифрован и вы установили тот же объект групповой политики, шифрование работает правильно и шифрует только используемое дисковое пространство на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b9604-132">If a computer is already encrypted when you install the MBAM Client, and you have set the same Group Policy Object, the encryption works correctly and encrypts only the used disk space on your computer.</span></span>

<span data-ttu-id="b9604-133">ВРЕМЕННОе решение: нет.</span><span class="sxs-lookup"><span data-stu-id="b9604-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="b9604-134">Неправильное отображение стойкости шифра в отчете о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="b9604-134">Cipher strength displays incorrectly on the Computer Compliance report</span></span>

<span data-ttu-id="b9604-135">Если вы не настроили определенную стойкость шифра в разделе **Выбор метода шифрования диска и объекта групповой политики стойкости шифра** , то отчет о соответствии компьютера в топологии интеграции Configuration Manager всегда отображается как "неизвестно" для стойкости шифра, даже если стойкость шифра использует значение по умолчанию для 128-битного шифрования.</span><span class="sxs-lookup"><span data-stu-id="b9604-135">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager Integration topology always displays “unknown” for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="b9604-136">В отчете показана правильная стойкость шифра, если в объекте групповой политики указана определенная стойкость шифра.</span><span class="sxs-lookup"><span data-stu-id="b9604-136">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="b9604-137">ВРЕМЕННОе решение: всегда устанавливайте определенную стойкость шифра в разделе **Выбор метода шифрования диска и объекта групповой политики стойкости шифра** .</span><span class="sxs-lookup"><span data-stu-id="b9604-137">WORKAROUND: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="b9604-138">При распределении состояния соответствия по типу диска старые данные отображаются после обновления элементов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b9604-138">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="b9604-139">После того как вы обновите элементы конфигурации MBAM в SystemCenter2012 ConfigurationManager, распределение состояния соответствия по типам дисков на панели мониторинга соответствия требованиям для предприятий BitLocker показывает данные, основанные на данных из старых версий элементов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b9604-139">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="b9604-140">ВРЕМЕННОе решение: нет.</span><span class="sxs-lookup"><span data-stu-id="b9604-140">WORKAROUND: None.</span></span> <span data-ttu-id="b9604-141">Изменение элементов конфигурации MBAM не поддерживается, и отчет может не отображаться должным образом.</span><span class="sxs-lookup"><span data-stu-id="b9604-141">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="b9604-142">Конфигурация усиленной безопасности может привести к тому, что отчеты отображаются неправильно</span><span class="sxs-lookup"><span data-stu-id="b9604-142">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="b9604-143">Если включена конфигурация усиленной безопасности Internet Explorer (ESC), при попытке просмотреть отчеты на сервере MBAM может появиться сообщение "отказано в доступе".</span><span class="sxs-lookup"><span data-stu-id="b9604-143">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an “Access Denied” message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="b9604-144">По умолчанию функция ESC включена, чтобы защитить сервер, уменьшая уязвимость сервера для потенциальных атак, которые могут возникать в результате веб-содержимого и сценариев приложений.</span><span class="sxs-lookup"><span data-stu-id="b9604-144">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="b9604-145">ВРЕМЕННОе решение: Если при попытке просмотреть отчеты на сервере MBAM появляется сообщение "отказано в доступе", вы можете задать объект групповой политики или изменить параметры по умолчанию вручную в своем изображении, чтобы отключить конфигурацию усиленной безопасности.</span><span class="sxs-lookup"><span data-stu-id="b9604-145">WORKAROUND: If the “Access Denied” message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="b9604-146">Кроме того, вы можете просматривать отчеты с другого компьютера, на котором не включена ESC.</span><span class="sxs-lookup"><span data-stu-id="b9604-146">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="b9604-147">Установка сервера MBAM завершается сбоем при переходе с SQL Server 2008 на SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="b9604-147">MBAM Server installation fails when you upgrade from SQL Server 2008 to SQL Server 2012</span></span>

<span data-ttu-id="b9604-148">При переходе с SQL Server 2008 на SQL Server 2012 и последующей попытке установить базу данных соответствия требованиям и аудита или базу данных восстановления, установка завершается сбоем и откатывается назад.</span><span class="sxs-lookup"><span data-stu-id="b9604-148">If you upgrade from SQL Server 2008 to SQL Server 2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="b9604-149">Эта проблема возникает из-за того, что необходимый файл SQLCMD.exe был удален во время обновления SQL и не удается найти в установщике MBAM.</span><span class="sxs-lookup"><span data-stu-id="b9604-149">The failure occurs because the required SQLCMD.exe file was removed during the SQL upgrade and cannot be found by the MBAM installer.</span></span> <span data-ttu-id="b9604-150">Строки в файле журнала MSI могут выглядеть примерно следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b9604-150">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="b9604-151">Центр восстановления RunDbInstallScript: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery DB: dbInstance-xxxxxx\\I01RunDbInstallScript DB: sqlScript-c:\\program Files Files\\Microsoft\\Microsoft DB: dbname-Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript \ _Recovery \ _and \ _HardwareRunDbInstallScript восстановления базы данных ЦС: MBAM defaultFileName \ _Recovery \ _and \ _HardwareRunDbInstallScript центра восстановления базы данных ЦС: MBAM-defaultDataPath Центр восстановления I01\\MSSQL\\DATA\\RunDbInstallScript: defaultLogPath-K:\\MSSQL\\MSSQL10. Центр восстановления I01\\MSSQL\\Data\\RunDbInstallScript: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\program Files Files\\Microsoft\\Microsoft, администрирование BitLocker и Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript Recovery DB: Начало работы с базой данных восстановления. После этого файл журнала восстановления для Jet-файла будет находиться в разделе" журнал "базы данных ЦС для восстановления:</span><span class="sxs-lookup"><span data-stu-id="b9604-151">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="b9604-152">Установщик Windows MBAM Server имеет встроенные сведения о том, как найти путь SQLCMD.exe, просмотрев строковое значение пути в реестре в разделе HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup.</span><span class="sxs-lookup"><span data-stu-id="b9604-152">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="b9604-153">Ключ по-прежнему отображается во время миграции из SQL Server 2008 в SQL Server 2012, но путь, на который ссылается значение данных, не содержит SQLCMD.exe файл, так как процесс обновления SQL удалил файл.</span><span class="sxs-lookup"><span data-stu-id="b9604-153">The key is still present during the migration from SQL Server 2008 to SQL Server 2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQL upgrade process removed the file.</span></span>

<span data-ttu-id="b9604-154">Временное решение: временно переименуйте строковое значение HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup Path на **path \ _OLD**, а затем снова запустите установщик Windows Server MBAM.</span><span class="sxs-lookup"><span data-stu-id="b9604-154">WORKAROUND: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup Path string value to **Path\_old**, and then re-run the MBAM Server Windows Installer.</span></span> <span data-ttu-id="b9604-155">После успешного завершения установки и создания баз данных в SQL Server 2012 переименуйте **путь \ _OLD** в значение **path**.</span><span class="sxs-lookup"><span data-stu-id="b9604-155">When the installation completes successfully and creates the databases in SQL Server 2012, rename the **Path\_old** value to **Path**.</span></span>

## <span data-ttu-id="b9604-156">Исправления и статьи базы знаний для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b9604-156">Hotfixes and Knowledge Base articles for MBAM2.0</span></span>


<span data-ttu-id="b9604-157">В этом разделе содержатся исправления и статьи базы знаний для MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="b9604-157">This section contains hotfixes and KB articles for MBAM2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="b9604-158">Статья базы знаний</span><span class="sxs-lookup"><span data-stu-id="b9604-158">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="b9604-159">Title</span><span class="sxs-lookup"><span data-stu-id="b9604-159">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="b9604-160">Ссылка</span><span class="sxs-lookup"><span data-stu-id="b9604-160">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9604-161">2831166</span><span class="sxs-lookup"><span data-stu-id="b9604-161">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-162">Установка системы администрирования и наблюдения (MBAM 2,0) для Microsoft BitLocker завершается сбоем, если &quot; уже установлены объекты System Center cm&quot;</span><span class="sxs-lookup"><span data-stu-id="b9604-162">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="b9604-163">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-163">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9604-164">2870849</span><span class="sxs-lookup"><span data-stu-id="b9604-164">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-165">Пользователи не могут получить ключ восстановления BitLocker с помощью портала самообслуживания MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="b9604-165">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="b9604-166">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-166">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9604-167">2756402</span><span class="sxs-lookup"><span data-stu-id="b9604-167">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-168">Клиент MBAM в описании события не сможет выполнить событие с кодом 4 и кодом ошибки 0x8004100E</span><span class="sxs-lookup"><span data-stu-id="b9604-168">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="b9604-169">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-169">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9604-170">2620287</span><span class="sxs-lookup"><span data-stu-id="b9604-170">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-171">Сообщение об ошибке "ошибка сервера в"/Reports "приложение" при выборе вкладки "отчеты" в MBAM</span><span class="sxs-lookup"><span data-stu-id="b9604-171">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="b9604-172">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-172">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9604-173">2639518</span><span class="sxs-lookup"><span data-stu-id="b9604-173">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-174">Ошибка при открытии отчетов о соответствии требованиям предприятия или компьютера в MBAM</span><span class="sxs-lookup"><span data-stu-id="b9604-174">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="b9604-175">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-175">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9604-176">2620269</span><span class="sxs-lookup"><span data-stu-id="b9604-176">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-177">Корпоративная отчетность MBAM не обновляется</span><span class="sxs-lookup"><span data-stu-id="b9604-177">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="b9604-178">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-178">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9604-179">2712461</span><span class="sxs-lookup"><span data-stu-id="b9604-179">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-180">Установка MBAM на контроллере домена не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b9604-180">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="b9604-181">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-181">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9604-182">2876732</span><span class="sxs-lookup"><span data-stu-id="b9604-182">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-183">Сообщение об ошибке с кодом 0x80071a90 во время отдельного процесса или настройки интеграции Configuration Manager для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b9604-183">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="b9604-184">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-184">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9604-185">2754259</span><span class="sxs-lookup"><span data-stu-id="b9604-185">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-186">MBAM и безопасная сетевая связь</span><span class="sxs-lookup"><span data-stu-id="b9604-186">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="b9604-187">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-187">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9604-188">2870842</span><span class="sxs-lookup"><span data-stu-id="b9604-188">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-189">Установка MBAM 2.0 завершается сбоем во время интеграции Configuration Manager с SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9604-189">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="b9604-190">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-190">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9604-191">2668533</span><span class="sxs-lookup"><span data-stu-id="b9604-191">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-192">Установка MBAM завершается сбоем, если неправильно настроена служба SSRS SQL</span><span class="sxs-lookup"><span data-stu-id="b9604-192">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="b9604-193">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-193">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9604-194">2870847</span><span class="sxs-lookup"><span data-stu-id="b9604-194">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-195">Программа установки MBAM 2,0 завершает работу с &quot; ошибкой при получении параметров роли сервера Configuration Manager для &#39;точки служб Reporting Services&#39; роли&quot;</span><span class="sxs-lookup"><span data-stu-id="b9604-195">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="b9604-196">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-196">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9604-197">2870839</span><span class="sxs-lookup"><span data-stu-id="b9604-197">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-198">Корпоративные отчеты MBAM 2.0 не обновляются в автономной топологии MBAM 2.0 из-за сбоя в работе CreateCache задания SQL</span><span class="sxs-lookup"><span data-stu-id="b9604-198">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="b9604-199">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-199">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9604-200">2620269</span><span class="sxs-lookup"><span data-stu-id="b9604-200">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-201">Корпоративная отчетность MBAM не обновляется</span><span class="sxs-lookup"><span data-stu-id="b9604-201">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="b9604-202">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-202">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9604-203">2935997</span><span class="sxs-lookup"><span data-stu-id="b9604-203">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-204">MBAM поддерживаемые компьютеры с неправильными отчетами о соответствия требованиям включают Неподдерживаемые продукты</span><span class="sxs-lookup"><span data-stu-id="b9604-204">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="b9604-205">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-205">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9604-206">2612822</span><span class="sxs-lookup"><span data-stu-id="b9604-206">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9604-207">Запись компьютера отклонена в MBAM</span><span class="sxs-lookup"><span data-stu-id="b9604-207">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="b9604-208">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9604-208">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b9604-209">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b9604-209">Related topics</span></span>


[<span data-ttu-id="b9604-210">Сведения о MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b9604-210">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)

 

 





