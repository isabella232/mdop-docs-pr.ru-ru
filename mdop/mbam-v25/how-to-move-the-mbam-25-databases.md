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
# Перенос баз данных MBAM 2.5

Воспользуйтесь этими инструкциями, чтобы переместить следующие базы данных с одного компьютера на другой; с сервера A на сервер B, например:

-   База данных соответствия требованиям и аудита

-   База данных восстановления

>[!NOTE]
>Важно, чтобы базы данных были восстановлены на компьютере B перед запуском мастера настройки MBAM для их обновления или настройки.

Если базы данных не отображаются, мастер настройки создает новые, пустые, базы данных. После того как существующие базы данных восстановлены, этот процесс будет прерывать конфигурацию MBAM.

Сначала восстановите базы данных, а затем запустите мастер настройки MBAM, выберите параметр база данных, и мастер настройки подключится к восстанавливаемым базам данных. При необходимости обновите их в рамках процесса.

**Если вы перемещаете несколько функций, наведите их в указанном ниже порядке.**

1.  База данных восстановления

2.  База данных соответствия требованиям и аудита

3.  Отчеты

4.  Веб-сайт администрирования и мониторинга

5.  Портал самообслуживания

>[!Note]
>Чтобы выполнить примеры сценариев Windows PowerShell, описанных в этой статье, необходимо обновить политику выполнения Windows PowerShell, чтобы включить сценарии для выполнения. Инструкции приведены в разделе [выполнение сценариев Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) .

## Перемещение базы данных восстановления

Ниже описаны действия, которые нужно выполнить для перемещения базы данных восстановления.

1.  Остановка всех экземпляров веб-сайта администрирования и мониторинга MBAM

2.  Создание резервной копии базы данных восстановления на сервере A

3.  Перемещение базы данных восстановления с сервера A на сервер B

4.  Восстановление базы данных восстановления на сервере B

5.  Настройка доступа к базе данных на сервере B и обновление данных соединения

6.  Установка программного обеспечения сервера MBAM и запуск мастера настройки MBAM сервера на сервере B

7.  Возобновление работы веб-сайта администрирования и мониторинга

### Перемещение базы данных восстановления

**Остановите все экземпляры веб-сайта администрирования и мониторинга MBAM.** На каждом сервере, на котором работает веб-сайт сервера администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта администрирования и наблюдения.

Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода команды, которая похожа на приведенную ниже.

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Для выполнения этой команды необходимо добавить в текущий экземпляр Windows PowerShell модуль служб IIS для Windows PowerShell.

### Создание резервной копии базы данных восстановления на сервере A

1.  Используйте задачу **резервного копирования** в SQL Server Management Studio для резервного копирования базы данных восстановления на сервере A.  По умолчанию в качестве имени базы данных используется **база данных восстановления MBAM**.

2.  Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий приведенный ниже сценарий SQL, и измените MBAM базу данных восстановления для использования режима полного восстановления.

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

3.  Используйте следующее значение, чтобы заменить значения в примере кода значениями, которые соответствуют вашей среде:

    **$Password $** -пароль, который используется для шифрования файла закрытого ключа.

4.  В Windows PowerShell выполните сценарий, хранящийся в файле, как показано ниже.

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  Используйте следующее значение, чтобы заменить значения в примере кода значениями, которые соответствуют вашей среде:

    **$ServerName $ \ $SQLINSTANCENAME $** — имя сервера и экземпляр, из которого будет создаваться резервная копия базы данных восстановления.

### Перемещение базы данных восстановления с сервера A на сервер B

С помощью проводника Windows переместите файл **Data MBAM Database. bak** с сервера A на сервер B.

Для автоматизации этой процедуры можно использовать Windows PowerShell для выполнения команды, которая похожа на описанную ниже.

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
Используйте сведения из приведенной ниже таблицы, чтобы заменить значения в примере кода значениями, которые соответствуют вашей среде.

| **Параметр**        | **Описание**  |
|----------------------|------------------|
| $SERVERNAME $       | Имя сервера, на который будут скопированы файлы. |
| $DESTINATIONSHARE $ | Имя общего доступа и путь, в который будут скопированы файлы. |


### Восстановление базы данных восстановления на сервере B

1.  Восстановите базу данных восстановления на сервере B, используя задачу **восстановления базы данных** в SQL Server Management Studio.

2.  После завершения предыдущей задачи выберите вариант **с устройства**, а затем выберите файл резервной копии базы данных.

3.  С помощью команды **Добавить** выберите файл **Data MBAM rerecovery Database. bak** и нажмите кнопку **ОК** , чтобы завершить процесс восстановления.

4.  Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:

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

5.  Используйте следующее значение, чтобы заменить значения в примере кода значениями, которые соответствуют вашей среде.

    **$Password $** -пароль, который использовался для шифрования файла закрытого ключа.

6.  В Windows PowerShell выполните сценарий, хранящийся в файле, как показано ниже.

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  Используйте следующее значение, чтобы заменить значения в примере кода значениями, которые соответствуют вашей среде.

    **$ServerName $ \ $SQLINSTANCENAME $** — имя сервера и экземпляр, в который будет восстановлена база данных восстановления.

### Настройка доступа к базе данных на сервере B и обновление данных соединения

1. Убедитесь, что имя пользователя Microsoft SQL Server, обеспечивающее доступ к базе данных восстановления для восстановленной базы данных, сопоставлено с учетной записью доступа, которую вы указали в процессе настройки.

   >[!NOTE]
   >Если имя пользователя не совпадает, создайте его с помощью SQL Server Management Studio и сопоставьте его с существующим пользователем базы данных.

2. На сервере, на котором запущен веб-сайт администрирования и наблюдения, обновите данные строки подключения для веб-сайтов MBAM с помощью консоли диспетчера служб IIS.

3. Измените следующий раздел реестра:

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString**

4. Обновите значение **источника данных** именем сервера и экземпляра (например, \ $servername \ $ \ \ \ $SQLINSTANCENAME), в который была перемещена база данных восстановления.

5. Обновите **начальное значение каталога** с восстановленным именем базы данных.

6. Для автоматизации этого процесса можно использовать командную строку Windows PowerShell для ввода командной строки на сервере администрирования и мониторинга, которая аналогична описанной ниже:

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
   >Эта строка подключения совместно используется всеми локальными веб-приложениями MBAM. Следовательно, его необходимо обновить только один раз на сервер.


7. С помощью приведенной ниже таблицы замените значения в примере кода значениями, которые соответствуют вашей среде.

   |Параметр|Описание|
   |---------|-----------|
   |$SERVERNAME $/\ $SQLINSTANCENAME $|Имя сервера и экземпляр SQL Server, на котором находится база данных восстановления.|
   |$DATABASE $|Имя базы данных восстановления.|


### Установка программного обеспечения сервера MBAM и запуск мастера настройки MBAM сервера на сервере B

1.  Установите серверное программное обеспечение MBAM 2,5 на сервер B. Подробности можно найти [в разделе Установка серверного программного обеспечения MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

2.  На сервере B запустите мастер настройки сервера MBAM, выберите команду **Добавить новые функции**и выберите только функцию **восстановления базы данных** . Подробнее о том, как настроить базы данных, можно найти в разделе [Настройка баз данных MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

    >[!TIP]
    >Кроме того, вы можете настроить базу данных восстановления с помощью командлета Windows PowerShell **Enable-MbamDatabase** .


### Возобновление работы веб-сайта администрирования и мониторинга

На сервере, на котором запущен веб-сайт администрирования и наблюдения, запустите веб-сайт администрирования и наблюдения с помощью консоли диспетчера служб IIS.

Для автоматизации этой процедуры можно использовать Windows PowerShell для выполнения команды, которая похожа на описанную ниже.

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Для выполнения этой команды необходимо добавить в текущий экземпляр Windows PowerShell модуль IIS для Windows PowerShell.

## Перемещение базы данных соответствия требованиям и аудита

Ниже приведены высокоуровневые инструкции по переносу базы данных соответствия требованиям и аудита.

1.  Остановка всех экземпляров веб-сайта администрирования и мониторинга MBAM

2.  Создание резервной копии базы данных соответствия требованиям и аудита на сервере A

3.  Перенос базы данных соответствия требованиям и аудита с сервера A на сервер B

4.  Восстановление базы данных соответствия и аудита на сервере B

5.  Настройка доступа к базе данных на сервере B и обновление данных соединения

6.  Установка программного обеспечения сервера MBAM и запуск мастера настройки MBAM сервера на сервере B

7.  Возобновление работы веб-сайта администрирования и мониторинга

### Как переместить базу данных соответствия требованиям и аудита

**Остановите все экземпляры веб-сайта администрирования и мониторинга MBAM.**  На каждом сервере, на котором работает веб-сайт сервера администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта администрирования и наблюдения.

Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода команды, которая похожа на приведенную ниже.

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Для выполнения этой команды необходимо добавить в текущий экземпляр Windows PowerShell модуль служб IIS для Windows PowerShell.

### Создание резервной копии базы данных соответствия требованиям и аудита на сервере A

1.  Используйте задачу **резервного копирования** в SQL Server Management Studio для резервного копирования базы данных соответствия требованиям и аудита на сервере A. По умолчанию в качестве имени базы данных используется **база данных состояния соответствия MBAM**.

2.  Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:

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

3.  Запустите сценарий, хранящийся в SQL-файле, с помощью команды Windows PowerShell, которая похожа на приведенную ниже.

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  Замените значения в примере кода следующими значениями, которые соответствуют вашей среде:

    **$ServerName $ \ $SQLINSTANCENAME $** — имя сервера и экземпляр, из которого будет создаваться резервная копия базы данных соответствия требованиям и аудита.

### Перенос базы данных соответствия требованиям и аудита с сервера A на сервер B * *

1.  С помощью проводника Windows переместите файл **Data MBAM. bak** из сервера а на сервер B.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для выполнения команды, которая похожа на описанную ниже.

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  С помощью приведенной ниже таблицы замените значения в примере кода значениями, которые соответствуют вашей среде.

    | **Параметр**        | **Описание**                                               |
    |----------------------|---------------------------------------------------------------|
    | $SERVERNAME $       | Имя сервера, на который будут скопированы файлы.         |
    | $DESTINATIONSHARE $ | Имя общего доступа и путь, в который будут скопированы файлы. |


### Восстановление базы данных соответствия и аудита на сервере B

1.  Восстановите базу данных соответствия и аудита на сервере B, используя задачу **восстановления базы данных** в SQL Server Management Studio.

2.  После завершения предыдущей задачи выберите вариант **с устройства**, а затем выберите файл резервной копии базы данных.

3.  С помощью команды **Добавить** выберите файл **Data MBAM. bak (состояние соответствия требованиям** ) и нажмите кнопку **ОК** , чтобы завершить процесс восстановления.

4.  Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  В Windows PowerShell выполните сценарий, хранящийся в файле, как показано ниже.

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  С помощью следующего значения замените значения в примере кода значениями, которые соответствуют вашей среде.

    **$ServerName $ \ $SQLINSTANCENAME $** — имя сервера и экземпляр, на который будет восстановлена база данных соответствия требованиям и аудита.

### Настройка доступа к базе данных на сервере B и обновление данных соединения

1. Убедитесь в том, что учетная запись пользователя Microsoft SQL Server, которая обеспечивает соответствие и аудит доступа к базе данных в восстановленной базе данных, сопоставлена со счетом доступа, который вы указали в процессе настройки.

   >[!NOTE]
   >Если имя пользователя не совпадает, создайте его с помощью SQL Server Management Studio и сопоставьте его с существующим пользователем базы данных.

2. На сервере, на котором запущен веб-сайт администрирования и наблюдения, обновите данные строки подключения для веб-сайта с помощью консоли диспетчера служб IIS.

3. Измените следующий раздел реестра:

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString**

4. Обновите значение **источника данных** именем сервера и экземпляра (например, \ $servername \ $ \ \ \ $SQLINSTANCENAME), в который была перемещена база данных восстановления.

5. Обновите **начальное значение каталога** с восстановленным именем базы данных.

6. Для автоматизации этого процесса можно использовать командную строку Windows PowerShell для ввода командной строки на сервере администрирования и мониторинга, которая аналогична описанной ниже:

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   >Эта строка подключения совместно используется всеми локальными веб-приложениями MBAM. Следовательно, его необходимо обновить только один раз на сервер.


7. С помощью приведенной ниже таблицы замените значения в примере кода значениями, которые соответствуют вашей среде.

   |Параметр | Описание |
   |---------|------------|
   |$SERVERNAME $ \ $SQLINSTANCENAME $ | Имя сервера и экземпляр SQL Server, на котором находится база данных восстановления.|
   |$DATABASE $|Имя восстановленной базы данных.|

### Установка программного обеспечения сервера MBAM и запуск мастера настройки MBAM сервера на сервере B

1.  Установите серверное программное обеспечение MBAM 2,5 на сервер B. Подробности можно найти [в разделе Установка серверного программного обеспечения MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

2.  На сервере B запустите мастер настройки сервера MBAM, выберите команду **Добавить новые функции**, а затем выберите только компонент **базы данных соответствие требованиям и аудита** . Подробнее о том, как настроить базы данных, можно найти в разделе [Настройка баз данных MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

    >[!TIP]
    >Кроме того, можно использовать командлет Windows PowerShell **Enable-MbamDatabase** , чтобы настроить базу данных соответствия требованиям и аудита.


### Возобновление работы веб-сайта администрирования и мониторинга

На сервере, на котором запущен веб-сайт администрирования и наблюдения, запустите веб-сайт администрирования и наблюдения с помощью консоли диспетчера служб IIS.

Для автоматизации этой процедуры можно использовать Windows PowerShell для выполнения команды, которая похожа на описанную ниже.

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Для выполнения этой команды необходимо добавить в текущий экземпляр Windows PowerShell модуль IIS для Windows PowerShell.
