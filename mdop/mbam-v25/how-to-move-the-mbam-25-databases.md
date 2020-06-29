---
title: Перенос баз данных MBAM 2.5
description: Перенос баз данных MBAM 2.5
author: dansimp
ms.assetid: 34b46f2d-0add-4377-8e4e-04b628fdfcf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 63c509e7ae1460ece815ef6c0a22350f76b52018
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812400"
---
# <span data-ttu-id="041a7-103">Перенос баз данных MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="041a7-103">How to Move the MBAM 2.5 Databases</span></span>

<span data-ttu-id="041a7-104">Воспользуйтесь этими инструкциями, чтобы переместить следующие базы данных с одного компьютера на другой; с сервера A на сервер B, например:</span><span class="sxs-lookup"><span data-stu-id="041a7-104">Use these procedures to move the following databases from one computer to another; from Server A to Server B, for example:</span></span>

-   <span data-ttu-id="041a7-105">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="041a7-105">Compliance and Audit Database</span></span>

-   <span data-ttu-id="041a7-106">База данных восстановления</span><span class="sxs-lookup"><span data-stu-id="041a7-106">Recovery Database</span></span>

>[!NOTE]
><span data-ttu-id="041a7-107">Важно, чтобы базы данных были восстановлены на компьютере B перед запуском мастера настройки MBAM для их обновления или настройки.</span><span class="sxs-lookup"><span data-stu-id="041a7-107">It is important that the databases be restored to Machine B PRIOR to running the MBAM Configuration Wizard to update/configure them.</span></span>

<span data-ttu-id="041a7-108">Если базы данных не отображаются, мастер настройки создает новые, пустые, базы данных.</span><span class="sxs-lookup"><span data-stu-id="041a7-108">If the databases are NOT present, the Configuration Wizard creates NEW, empty, databases.</span></span> <span data-ttu-id="041a7-109">После того как существующие базы данных восстановлены, этот процесс будет прерывать конфигурацию MBAM.</span><span class="sxs-lookup"><span data-stu-id="041a7-109">When your existing databases are then restored, this process will break the MBAM configuration.</span></span>

<span data-ttu-id="041a7-110">Сначала восстановите базы данных, а затем запустите мастер настройки MBAM, выберите параметр база данных, и мастер настройки подключится к восстанавливаемым базам данных. При необходимости обновите их в рамках процесса.</span><span class="sxs-lookup"><span data-stu-id="041a7-110">Restore the databases FIRST, then run the MBAM Configuration Wizard, choose the database option, and the Configuration Wizard will “connect” to the databases you restored; upgrading them if needed as part of the process.</span></span>

**<span data-ttu-id="041a7-111">Если вы перемещаете несколько функций, наведите их в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="041a7-111">If you are moving multiple features, move them in the following order:</span></span>**

1.  <span data-ttu-id="041a7-112">База данных восстановления</span><span class="sxs-lookup"><span data-stu-id="041a7-112">Recovery Database</span></span>

2.  <span data-ttu-id="041a7-113">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="041a7-113">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="041a7-114">Отчеты</span><span class="sxs-lookup"><span data-stu-id="041a7-114">Reports</span></span>

4.  <span data-ttu-id="041a7-115">Веб-сайт администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="041a7-115">Administration and Monitoring Website</span></span>

5.  <span data-ttu-id="041a7-116">Портал самообслуживания</span><span class="sxs-lookup"><span data-stu-id="041a7-116">Self-Service Portal</span></span>

>[!Note]
><span data-ttu-id="041a7-117">Чтобы выполнить примеры сценариев Windows PowerShell, описанных в этой статье, необходимо обновить политику выполнения Windows PowerShell, чтобы включить сценарии для выполнения.</span><span class="sxs-lookup"><span data-stu-id="041a7-117">To run the example Windows PowerShell scripts provided in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="041a7-118">Инструкции приведены в разделе [выполнение сценариев Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) .</span><span class="sxs-lookup"><span data-stu-id="041a7-118">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

## <span data-ttu-id="041a7-119">Перемещение базы данных восстановления</span><span class="sxs-lookup"><span data-stu-id="041a7-119">Move the Recovery Database</span></span>

<span data-ttu-id="041a7-120">Ниже описаны действия, которые нужно выполнить для перемещения базы данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="041a7-120">The high-level steps for moving the Recovery Database are:</span></span>

1.  <span data-ttu-id="041a7-121">Остановка всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="041a7-121">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="041a7-122">Создание резервной копии базы данных восстановления на сервере A</span><span class="sxs-lookup"><span data-stu-id="041a7-122">Back up the Recovery Database on Server A</span></span>

3.  <span data-ttu-id="041a7-123">Перемещение базы данных восстановления с сервера A на сервер B</span><span class="sxs-lookup"><span data-stu-id="041a7-123">Move the Recovery Database from Server A to Server B</span></span>

4.  <span data-ttu-id="041a7-124">Восстановление базы данных восстановления на сервере B</span><span class="sxs-lookup"><span data-stu-id="041a7-124">Restore the Recovery Database on Server B</span></span>

5.  <span data-ttu-id="041a7-125">Настройка доступа к базе данных на сервере B и обновление данных соединения</span><span class="sxs-lookup"><span data-stu-id="041a7-125">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="041a7-126">Установка программного обеспечения сервера MBAM и запуск мастера настройки MBAM сервера на сервере B</span><span class="sxs-lookup"><span data-stu-id="041a7-126">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="041a7-127">Возобновление работы веб-сайта администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="041a7-127">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="041a7-128">Перемещение базы данных восстановления</span><span class="sxs-lookup"><span data-stu-id="041a7-128">How to move the Recovery Database</span></span>

**<span data-ttu-id="041a7-129">Остановите все экземпляры веб-сайта администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="041a7-129">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>** <span data-ttu-id="041a7-130">На каждом сервере, на котором работает веб-сайт сервера администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта администрирования и наблюдения.</span><span class="sxs-lookup"><span data-stu-id="041a7-130">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="041a7-131">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода команды, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="041a7-131">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="041a7-132">Для выполнения этой команды необходимо добавить в текущий экземпляр Windows PowerShell модуль служб IIS для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="041a7-132">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="041a7-133">Создание резервной копии базы данных восстановления на сервере A</span><span class="sxs-lookup"><span data-stu-id="041a7-133">Back up the Recovery Database on Server A</span></span>

1.  <span data-ttu-id="041a7-134">Используйте задачу **резервного копирования** в SQL Server Management Studio для резервного копирования базы данных восстановления на сервере A.  По умолчанию в качестве имени базы данных используется **база данных восстановления MBAM**.</span><span class="sxs-lookup"><span data-stu-id="041a7-134">Use the **Back Up** task in SQL Server Management Studio to back up the Recovery Database on Server A.  By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="041a7-135">Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий приведенный ниже сценарий SQL, и измените MBAM базу данных восстановления для использования режима полного восстановления.</span><span class="sxs-lookup"><span data-stu-id="041a7-135">To automate this procedure, create a SQL file (.sql) that contains the following SQL script, and change the MBAM Recovery Database to use the full recovery mode:</span></span>

    ```
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

    SET RECOVERY FULL;

    GO

    -- Create MBAM Recovery Database Data and MBAM Recovery logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery Database Data.bak';

    GO

    -- Back up the full MBAM Recovery Database.

    BACKUP DATABASE [MBAM Recovery and Hardware] TO [MBAM Recovery and Hardware Database Data Device];

    GO

    BACKUP CERTIFICATE [MBAM Recovery Encryption Certificate]

    TO FILE = 'Z:\SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

    FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

    ENCRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

3.  <span data-ttu-id="041a7-136">Используйте следующее значение, чтобы заменить значения в примере кода значениями, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="041a7-136">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="041a7-137">**$Password $** -пароль, который используется для шифрования файла закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="041a7-137">**$PASSWORD$** - password that you use to encrypt the Private Key file.</span></span>

4.  <span data-ttu-id="041a7-138">В Windows PowerShell выполните сценарий, хранящийся в файле, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="041a7-138">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  <span data-ttu-id="041a7-139">Используйте следующее значение, чтобы заменить значения в примере кода значениями, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="041a7-139">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="041a7-140">**$ServerName $ \ $SQLINSTANCENAME $** — имя сервера и экземпляр, из которого будет создаваться резервная копия базы данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="041a7-140">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Recovery Database will be backed up.</span></span>

### <span data-ttu-id="041a7-141">Перемещение базы данных восстановления с сервера A на сервер B</span><span class="sxs-lookup"><span data-stu-id="041a7-141">Move the Recovery Database from Server A to Server B</span></span>

<span data-ttu-id="041a7-142">С помощью проводника Windows переместите файл **Data MBAM Database. bak** с сервера A на сервер B.</span><span class="sxs-lookup"><span data-stu-id="041a7-142">Use Windows Explorer to move the **MBAM Recovery Database Data.bak** file from Server A to Server B.</span></span>

<span data-ttu-id="041a7-143">Для автоматизации этой процедуры можно использовать Windows PowerShell для выполнения команды, которая похожа на описанную ниже.</span><span class="sxs-lookup"><span data-stu-id="041a7-143">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
<span data-ttu-id="041a7-144">Используйте сведения из приведенной ниже таблицы, чтобы заменить значения в примере кода значениями, которые соответствуют вашей среде.</span><span class="sxs-lookup"><span data-stu-id="041a7-144">Use the information in the following table to replace the values in the code example with values that match your environment.</span></span>

| **<span data-ttu-id="041a7-145">Параметр</span><span class="sxs-lookup"><span data-stu-id="041a7-145">Parameter</span></span>**        | **<span data-ttu-id="041a7-146">Описание</span><span class="sxs-lookup"><span data-stu-id="041a7-146">Description</span></span>**  |
|----------------------|------------------|
| <span data-ttu-id="041a7-147">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="041a7-147">$SERVERNAME$</span></span>       | <span data-ttu-id="041a7-148">Имя сервера, на который будут скопированы файлы.</span><span class="sxs-lookup"><span data-stu-id="041a7-148">Name of the server to which the files will be copied.</span></span> |
| <span data-ttu-id="041a7-149">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="041a7-149">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="041a7-150">Имя общего доступа и путь, в который будут скопированы файлы.</span><span class="sxs-lookup"><span data-stu-id="041a7-150">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="041a7-151">Восстановление базы данных восстановления на сервере B</span><span class="sxs-lookup"><span data-stu-id="041a7-151">Restore the Recovery Database on Server B</span></span>

1.  <span data-ttu-id="041a7-152">Восстановите базу данных восстановления на сервере B, используя задачу **восстановления базы данных** в SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="041a7-152">Restore the Recovery Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="041a7-153">После завершения предыдущей задачи выберите вариант **с устройства**, а затем выберите файл резервной копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="041a7-153">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="041a7-154">С помощью команды **Добавить** выберите файл **Data MBAM rerecovery Database. bak** и нажмите кнопку **ОК** , чтобы завершить процесс восстановления.</span><span class="sxs-lookup"><span data-stu-id="041a7-154">Use the **Add** command to select the **MBAM Recovery Database Data.bak** file, and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="041a7-155">Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:</span><span class="sxs-lookup"><span data-stu-id="041a7-155">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    -- Restore MBAM Recovery Database.

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z:\SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

    FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

    DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO

    -- Restore the MBAM Recovery Database data and log files.

    RESTORE DATABASE [MBAM Recovery and Hardware]

    FROM DISK = 'Z:\MBAM Recovery Database Data.bak'

    WITH REPLACE
    ```

5.  <span data-ttu-id="041a7-156">Используйте следующее значение, чтобы заменить значения в примере кода значениями, которые соответствуют вашей среде.</span><span class="sxs-lookup"><span data-stu-id="041a7-156">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="041a7-157">**$Password $** -пароль, который использовался для шифрования файла закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="041a7-157">**$PASSWORD$** - password that you used to encrypt the Private Key file.</span></span>

6.  <span data-ttu-id="041a7-158">В Windows PowerShell выполните сценарий, хранящийся в файле, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="041a7-158">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  <span data-ttu-id="041a7-159">Используйте следующее значение, чтобы заменить значения в примере кода значениями, которые соответствуют вашей среде.</span><span class="sxs-lookup"><span data-stu-id="041a7-159">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="041a7-160">**$ServerName $ \ $SQLINSTANCENAME $** — имя сервера и экземпляр, в который будет восстановлена база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="041a7-160">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Recovery Database will be restored.</span></span>

### <span data-ttu-id="041a7-161">Настройка доступа к базе данных на сервере B и обновление данных соединения</span><span class="sxs-lookup"><span data-stu-id="041a7-161">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="041a7-162">Убедитесь, что имя пользователя Microsoft SQL Server, обеспечивающее доступ к базе данных восстановления для восстановленной базы данных, сопоставлено с учетной записью доступа, которую вы указали в процессе настройки.</span><span class="sxs-lookup"><span data-stu-id="041a7-162">Verify that the Microsoft SQL Server user login that enables Recovery Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="041a7-163">Если имя пользователя не совпадает, создайте его с помощью SQL Server Management Studio и сопоставьте его с существующим пользователем базы данных.</span><span class="sxs-lookup"><span data-stu-id="041a7-163">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="041a7-164">На сервере, на котором запущен веб-сайт администрирования и наблюдения, обновите данные строки подключения для веб-сайтов MBAM с помощью консоли диспетчера служб IIS.</span><span class="sxs-lookup"><span data-stu-id="041a7-164">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the MBAM websites.</span></span>

3. <span data-ttu-id="041a7-165">Измените следующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="041a7-165">Edit the following registry key:</span></span>

   **<span data-ttu-id="041a7-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="041a7-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span></span>**

4. <span data-ttu-id="041a7-167">Обновите значение **источника данных** именем сервера и экземпляра (например, \ $servername \ $ \ \ \ $SQLINSTANCENAME), в который была перемещена база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="041a7-167">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="041a7-168">Обновите **начальное значение каталога** с восстановленным именем базы данных.</span><span class="sxs-lookup"><span data-stu-id="041a7-168">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="041a7-169">Для автоматизации этого процесса можно использовать командную строку Windows PowerShell для ввода командной строки на сервере администрирования и мониторинга, которая аналогична описанной ниже:</span><span class="sxs-lookup"><span data-stu-id="041a7-169">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\\Microsoft\MBAM Server\\Web" /v
   RecoveryDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f

   Set-WebConfigurationProperty
   'connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath
   "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data
   Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and
   Hardware;Integrated Security=SSPI;"

   Set-WebConfigurationProperty
   'connectionStrings/add[\@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]'
   -PSPath "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value
   "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery
   and Hardware;Integrated Security=SSPI;"
   ```

   >[!Note]
   ><span data-ttu-id="041a7-170">Эта строка подключения совместно используется всеми локальными веб-приложениями MBAM.</span><span class="sxs-lookup"><span data-stu-id="041a7-170">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="041a7-171">Следовательно, его необходимо обновить только один раз на сервер.</span><span class="sxs-lookup"><span data-stu-id="041a7-171">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="041a7-172">С помощью приведенной ниже таблицы замените значения в примере кода значениями, которые соответствуют вашей среде.</span><span class="sxs-lookup"><span data-stu-id="041a7-172">Use the following table to replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="041a7-173">Параметр</span><span class="sxs-lookup"><span data-stu-id="041a7-173">Parameter</span></span>|<span data-ttu-id="041a7-174">Описание</span><span class="sxs-lookup"><span data-stu-id="041a7-174">Description</span></span>|
   |---------|-----------|
   |<span data-ttu-id="041a7-175">$SERVERNAME $/\ $SQLINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="041a7-175">$SERVERNAME$/\$SQLINSTANCENAME$</span></span>|<span data-ttu-id="041a7-176">Имя сервера и экземпляр SQL Server, на котором находится база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="041a7-176">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="041a7-177">$DATABASE $</span><span class="sxs-lookup"><span data-stu-id="041a7-177">$DATABASE$</span></span>|<span data-ttu-id="041a7-178">Имя базы данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="041a7-178">Name of the Recovery database.</span></span>|


### <span data-ttu-id="041a7-179">Установка программного обеспечения сервера MBAM и запуск мастера настройки MBAM сервера на сервере B</span><span class="sxs-lookup"><span data-stu-id="041a7-179">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="041a7-180">Установите серверное программное обеспечение MBAM 2,5 на сервер B. Подробности можно найти [в разделе Установка серверного программного обеспечения MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span><span class="sxs-lookup"><span data-stu-id="041a7-180">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="041a7-181">На сервере B запустите мастер настройки сервера MBAM, выберите команду **Добавить новые функции**и выберите только функцию **восстановления базы данных** .</span><span class="sxs-lookup"><span data-stu-id="041a7-181">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Recovery Database** feature.</span></span> <span data-ttu-id="041a7-182">Подробнее о том, как настроить базы данных, можно найти в разделе [Настройка баз данных MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span><span class="sxs-lookup"><span data-stu-id="041a7-182">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="041a7-183">Кроме того, вы можете настроить базу данных восстановления с помощью командлета Windows PowerShell **Enable-MbamDatabase** .</span><span class="sxs-lookup"><span data-stu-id="041a7-183">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Recovery Database.</span></span>


### <span data-ttu-id="041a7-184">Возобновление работы веб-сайта администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="041a7-184">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="041a7-185">На сервере, на котором запущен веб-сайт администрирования и наблюдения, запустите веб-сайт администрирования и наблюдения с помощью консоли диспетчера служб IIS.</span><span class="sxs-lookup"><span data-stu-id="041a7-185">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="041a7-186">Для автоматизации этой процедуры можно использовать Windows PowerShell для выполнения команды, которая похожа на описанную ниже.</span><span class="sxs-lookup"><span data-stu-id="041a7-186">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="041a7-187">Для выполнения этой команды необходимо добавить в текущий экземпляр Windows PowerShell модуль IIS для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="041a7-187">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

## <span data-ttu-id="041a7-188">Перемещение базы данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="041a7-188">Move the Compliance and Audit Database</span></span>

<span data-ttu-id="041a7-189">Ниже приведены высокоуровневые инструкции по переносу базы данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="041a7-189">The high-level steps for moving the Compliance and Audit Database are:</span></span>

1.  <span data-ttu-id="041a7-190">Остановка всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="041a7-190">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="041a7-191">Создание резервной копии базы данных соответствия требованиям и аудита на сервере A</span><span class="sxs-lookup"><span data-stu-id="041a7-191">Back up the Compliance and Audit Database on Server A</span></span>

3.  <span data-ttu-id="041a7-192">Перенос базы данных соответствия требованиям и аудита с сервера A на сервер B</span><span class="sxs-lookup"><span data-stu-id="041a7-192">Move the Compliance and Audit Database from Server A to Server B</span></span>

4.  <span data-ttu-id="041a7-193">Восстановление базы данных соответствия и аудита на сервере B</span><span class="sxs-lookup"><span data-stu-id="041a7-193">Restore the Compliance and Audit Database on Server B</span></span>

5.  <span data-ttu-id="041a7-194">Настройка доступа к базе данных на сервере B и обновление данных соединения</span><span class="sxs-lookup"><span data-stu-id="041a7-194">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="041a7-195">Установка программного обеспечения сервера MBAM и запуск мастера настройки MBAM сервера на сервере B</span><span class="sxs-lookup"><span data-stu-id="041a7-195">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="041a7-196">Возобновление работы веб-сайта администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="041a7-196">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="041a7-197">Как переместить базу данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="041a7-197">How to move the Compliance and Audit Database</span></span>

**<span data-ttu-id="041a7-198">Остановите все экземпляры веб-сайта администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="041a7-198">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>**  <span data-ttu-id="041a7-199">На каждом сервере, на котором работает веб-сайт сервера администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта администрирования и наблюдения.</span><span class="sxs-lookup"><span data-stu-id="041a7-199">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="041a7-200">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода команды, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="041a7-200">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="041a7-201">Для выполнения этой команды необходимо добавить в текущий экземпляр Windows PowerShell модуль служб IIS для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="041a7-201">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="041a7-202">Создание резервной копии базы данных соответствия требованиям и аудита на сервере A</span><span class="sxs-lookup"><span data-stu-id="041a7-202">Back up the Compliance and Audit Database on Server A</span></span>

1.  <span data-ttu-id="041a7-203">Используйте задачу **резервного копирования** в SQL Server Management Studio для резервного копирования базы данных соответствия требованиям и аудита на сервере A. По умолчанию в качестве имени базы данных используется **база данных состояния соответствия MBAM**.</span><span class="sxs-lookup"><span data-stu-id="041a7-203">Use the **Back Up** task in SQL Server Management Studio to back up the Compliance and Audit Database on Server A. By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="041a7-204">Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:</span><span class="sxs-lookup"><span data-stu-id="041a7-204">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    USE master;

    GO

    ALTER DATABASE "MBAM Compliance Status"

    SET RECOVERY FULL;

    GO

    -- Create MBAM Compliance Status Data logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Compliance Status Database Data Device',

    'Z: \MBAM Compliance Status Database Data.bak';

    GO

    -- Back up the full MBAM Compliance Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO

    ```

3.  <span data-ttu-id="041a7-205">Запустите сценарий, хранящийся в SQL-файле, с помощью команды Windows PowerShell, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="041a7-205">Run the script that is stored in the .sql file by using a Windows PowerShell command that is similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  <span data-ttu-id="041a7-206">Замените значения в примере кода следующими значениями, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="041a7-206">Using the following value, replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="041a7-207">**$ServerName $ \ $SQLINSTANCENAME $** — имя сервера и экземпляр, из которого будет создаваться резервная копия базы данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="041a7-207">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Compliance and Audit Database will be backed up.</span></span>

### <span data-ttu-id="041a7-208">Перенос базы данных соответствия требованиям и аудита с сервера A на сервер B \* \*</span><span class="sxs-lookup"><span data-stu-id="041a7-208">Move the Compliance and Audit Database from Server A to Server B\*\*</span></span>

1.  <span data-ttu-id="041a7-209">С помощью проводника Windows переместите файл **Data MBAM. bak** из сервера а на сервер B.</span><span class="sxs-lookup"><span data-stu-id="041a7-209">Use Windows Explorer to move the **MBAM Compliance Status Database Data.bak** file from Server A to Server B.</span></span>

2.  <span data-ttu-id="041a7-210">Для автоматизации этой процедуры можно использовать Windows PowerShell для выполнения команды, которая похожа на описанную ниже.</span><span class="sxs-lookup"><span data-stu-id="041a7-210">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  <span data-ttu-id="041a7-211">С помощью приведенной ниже таблицы замените значения в примере кода значениями, которые соответствуют вашей среде.</span><span class="sxs-lookup"><span data-stu-id="041a7-211">Using the following table, replace the values in the code example with values that match your environment.</span></span>

    | **<span data-ttu-id="041a7-212">Параметр</span><span class="sxs-lookup"><span data-stu-id="041a7-212">Parameter</span></span>**        | **<span data-ttu-id="041a7-213">Описание</span><span class="sxs-lookup"><span data-stu-id="041a7-213">Description</span></span>**                                               |
    |----------------------|---------------------------------------------------------------|
    | <span data-ttu-id="041a7-214">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="041a7-214">$SERVERNAME$</span></span>       | <span data-ttu-id="041a7-215">Имя сервера, на который будут скопированы файлы.</span><span class="sxs-lookup"><span data-stu-id="041a7-215">Name of the server to which the files will be copied.</span></span>         |
    | <span data-ttu-id="041a7-216">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="041a7-216">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="041a7-217">Имя общего доступа и путь, в который будут скопированы файлы.</span><span class="sxs-lookup"><span data-stu-id="041a7-217">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="041a7-218">Восстановление базы данных соответствия и аудита на сервере B</span><span class="sxs-lookup"><span data-stu-id="041a7-218">Restore the Compliance and Audit Database on Server B</span></span>

1.  <span data-ttu-id="041a7-219">Восстановите базу данных соответствия и аудита на сервере B, используя задачу **восстановления базы данных** в SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="041a7-219">Restore the Compliance and Audit Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="041a7-220">После завершения предыдущей задачи выберите вариант **с устройства**, а затем выберите файл резервной копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="041a7-220">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="041a7-221">С помощью команды **Добавить** выберите файл **Data MBAM. bak (состояние соответствия требованиям** ) и нажмите кнопку **ОК** , чтобы завершить процесс восстановления.</span><span class="sxs-lookup"><span data-stu-id="041a7-221">Use the **Add** command to select the **MBAM Compliance Status Database Data.bak** file and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="041a7-222">Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:</span><span class="sxs-lookup"><span data-stu-id="041a7-222">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  <span data-ttu-id="041a7-223">В Windows PowerShell выполните сценарий, хранящийся в файле, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="041a7-223">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  <span data-ttu-id="041a7-224">С помощью следующего значения замените значения в примере кода значениями, которые соответствуют вашей среде.</span><span class="sxs-lookup"><span data-stu-id="041a7-224">Using the following value, replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="041a7-225">**$ServerName $ \ $SQLINSTANCENAME $** — имя сервера и экземпляр, на который будет восстановлена база данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="041a7-225">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Compliance and Audit Database will be restored.</span></span>

### <span data-ttu-id="041a7-226">Настройка доступа к базе данных на сервере B и обновление данных соединения</span><span class="sxs-lookup"><span data-stu-id="041a7-226">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="041a7-227">Убедитесь в том, что учетная запись пользователя Microsoft SQL Server, которая обеспечивает соответствие и аудит доступа к базе данных в восстановленной базе данных, сопоставлена со счетом доступа, который вы указали в процессе настройки.</span><span class="sxs-lookup"><span data-stu-id="041a7-227">Verify that the Microsoft SQL Server user login that enables Compliance and Audit Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="041a7-228">Если имя пользователя не совпадает, создайте его с помощью SQL Server Management Studio и сопоставьте его с существующим пользователем базы данных.</span><span class="sxs-lookup"><span data-stu-id="041a7-228">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="041a7-229">На сервере, на котором запущен веб-сайт администрирования и наблюдения, обновите данные строки подключения для веб-сайта с помощью консоли диспетчера служб IIS.</span><span class="sxs-lookup"><span data-stu-id="041a7-229">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the Website.</span></span>

3. <span data-ttu-id="041a7-230">Измените следующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="041a7-230">Edit the following registry key:</span></span>

   **<span data-ttu-id="041a7-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="041a7-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span></span>**

4. <span data-ttu-id="041a7-232">Обновите значение **источника данных** именем сервера и экземпляра (например, \ $servername \ $ \ \ \ $SQLINSTANCENAME), в который была перемещена база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="041a7-232">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="041a7-233">Обновите **начальное значение каталога** с восстановленным именем базы данных.</span><span class="sxs-lookup"><span data-stu-id="041a7-233">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="041a7-234">Для автоматизации этого процесса можно использовать командную строку Windows PowerShell для ввода командной строки на сервере администрирования и мониторинга, которая аналогична описанной ниже:</span><span class="sxs-lookup"><span data-stu-id="041a7-234">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   ><span data-ttu-id="041a7-235">Эта строка подключения совместно используется всеми локальными веб-приложениями MBAM.</span><span class="sxs-lookup"><span data-stu-id="041a7-235">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="041a7-236">Следовательно, его необходимо обновить только один раз на сервер.</span><span class="sxs-lookup"><span data-stu-id="041a7-236">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="041a7-237">С помощью приведенной ниже таблицы замените значения в примере кода значениями, которые соответствуют вашей среде.</span><span class="sxs-lookup"><span data-stu-id="041a7-237">Using the following table, replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="041a7-238">Параметр</span><span class="sxs-lookup"><span data-stu-id="041a7-238">Parameter</span></span> | <span data-ttu-id="041a7-239">Описание</span><span class="sxs-lookup"><span data-stu-id="041a7-239">Description</span></span> |
   |---------|------------|
   |<span data-ttu-id="041a7-240">$SERVERNAME $ \ $SQLINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="041a7-240">$SERVERNAME$\$SQLINSTANCENAME$</span></span> | <span data-ttu-id="041a7-241">Имя сервера и экземпляр SQL Server, на котором находится база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="041a7-241">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="041a7-242">$DATABASE $</span><span class="sxs-lookup"><span data-stu-id="041a7-242">$DATABASE$</span></span>|<span data-ttu-id="041a7-243">Имя восстановленной базы данных.</span><span class="sxs-lookup"><span data-stu-id="041a7-243">Name of the recovered database.</span></span>|

### <span data-ttu-id="041a7-244">Установка программного обеспечения сервера MBAM и запуск мастера настройки MBAM сервера на сервере B</span><span class="sxs-lookup"><span data-stu-id="041a7-244">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="041a7-245">Установите серверное программное обеспечение MBAM 2,5 на сервер B. Подробности можно найти [в разделе Установка серверного программного обеспечения MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span><span class="sxs-lookup"><span data-stu-id="041a7-245">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="041a7-246">На сервере B запустите мастер настройки сервера MBAM, выберите команду **Добавить новые функции**, а затем выберите только компонент **базы данных соответствие требованиям и аудита** .</span><span class="sxs-lookup"><span data-stu-id="041a7-246">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Compliance and Audit Database** feature.</span></span> <span data-ttu-id="041a7-247">Подробнее о том, как настроить базы данных, можно найти в разделе [Настройка баз данных MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span><span class="sxs-lookup"><span data-stu-id="041a7-247">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="041a7-248">Кроме того, можно использовать командлет Windows PowerShell **Enable-MbamDatabase** , чтобы настроить базу данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="041a7-248">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Compliance and Audit Database.</span></span>


### <span data-ttu-id="041a7-249">Возобновление работы веб-сайта администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="041a7-249">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="041a7-250">На сервере, на котором запущен веб-сайт администрирования и наблюдения, запустите веб-сайт администрирования и наблюдения с помощью консоли диспетчера служб IIS.</span><span class="sxs-lookup"><span data-stu-id="041a7-250">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="041a7-251">Для автоматизации этой процедуры можно использовать Windows PowerShell для выполнения команды, которая похожа на описанную ниже.</span><span class="sxs-lookup"><span data-stu-id="041a7-251">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="041a7-252">Для выполнения этой команды необходимо добавить в текущий экземпляр Windows PowerShell модуль IIS для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="041a7-252">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>
