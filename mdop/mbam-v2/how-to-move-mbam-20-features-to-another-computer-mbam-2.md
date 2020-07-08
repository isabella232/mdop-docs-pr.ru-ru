---
title: Перемещение компонентов MBAM 2.0 на другой компьютер
description: Перемещение компонентов MBAM 2.0 на другой компьютер
author: dansimp
ms.assetid: 49bc0792-60a4-473f-89cc-ada30191e04a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 340d87e26d87f124a9ab64c63d33e89c293d8a86
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825079"
---
# Перемещение компонентов MBAM 2.0 на другой компьютер


В этой статье описаны действия, которые необходимо выполнить для перемещения одной или нескольких функций администрирования и мониторинга Microsoft BitLocker (MBAM) на другой компьютер. При перемещении нескольких функций администрирования и мониторинга Microsoft BitLocker следует переместить их в указанном ниже порядке.

1.  База данных восстановления

2.  База данных соответствия требованиям и аудита

3.  Отчеты о соответствии и аудите

4.  Администрирование и мониторинг

## Перемещение базы данных восстановления


Чтобы переместить базу данных восстановления с одного компьютера на другой (например, с сервера A на сервер B), выполните указанные ниже действия.

1.  Остановите все экземпляры веб-сайта администрирования и мониторинга.

2.  Запустите настройку MBAM на сервере B.

3.  Создание резервной копии базы данных восстановления MBAM на сервере A.

4.  Перенесите базу данных восстановления MBAM с сервера A в B.

5.  Восстановите базу данных восстановления MBAM на сервере B.

6.  Настройка доступа к базе данных восстановления MBAM на сервере B.

7.  Обновите данные подключения к базе данных на серверах администрирования и мониторинга MBAM.

8.  Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM.

**Остановка всех экземпляров веб-сайта администрирования и мониторинга MBAM**

1.  На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта MBAM, который называется **администрированием и мониторингом Microsoft BitLocker**.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, сходной с:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Примечание.**  
    Чтобы выполнить эту командную строку PowerShell, необходимо добавить модуль IIS для PowerShell в текущий экземпляр PowerShell. Кроме того, необходимо обновить политику выполнения PowerShell, чтобы разрешить выполнение сценариев.



**Запуск настройки MBAM на сервере B**

1.  Запустите настройку MBAM на сервере B и выберите только **базу данных восстановления** для установки.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ TOPOLOGY=$X$`

    **Примечание.**  
    Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, в который будет перемещена база данных восстановления.

    -   $DOMAIN $ \ \ $SERVERNAME $-введите имена домена и сервера для каждого сервера администрирования и мониторинга MBAM, который будет обращаться к базе данных восстановления. Используйте точку с запятой для разделения каждой пары домена и сервера в списке (например, $DOMAIN \ \ мой домен \; $DOMAIN \ \ $SERVERNAME $ $). За именем каждого сервера должен следовать символ "$", как показано в примере (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).

    -   $X $-введите **0** , если вы устанавливаете изолированную топологию MBAM или **1** при установке топологии Configuration Manager MBAM.



**Создание резервной копии базы данных восстановления на сервере A**

1.  Чтобы создать резервную копию базы данных восстановления на сервере A, используйте SQL Server Management Studio и задачу с именем "резервная копия". По умолчанию в качестве имени базы данных используется **база данных восстановления MBAM**.

2.  Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:

    Измените базу данных восстановления MBAM, чтобы использовать режим полного восстановления.

    ```sql
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

    **Примечание.**  
    Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:

    -   $PASSWORD $-введите пароль, который будет использоваться для шифрования файла закрытого ключа.



3.  Запустите SQL-файл, используя SQL Server PowerShell, и командную строку, подобную следующей:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Примечание.**  
    Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляра, из которого будет создаваться резервная копия базы данных восстановления.



**Перемещение базы данных восстановления и сертификата с сервера A на сервер B**

1.  Переместите следующий файл с сервера A на сервер B с помощью проводника Windows.

    -   Данные базы данных MBAM Recovery. bak

2.  Чтобы переместить сертификат для зашифрованной базы данных, выполните указанные ниже действия автоматизации. Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.

    `PS C:\> Copy-Item “Z:\MBAM Recovery Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Примечание.**  
    Замените приведенное ниже значение в приведенном выше примере, чтобы оно соответствовало вашей среде.

    -   $SERVERNAME $-введите имя сервера, на который будут скопированы файлы.

    -   $DESTINATIONSHARE $-введите имя общего доступа и путь к файлам, куда они будут скопированы.



**Восстановление базы данных восстановления на сервере B**

1.  Восстановите базу данных восстановления на сервере B с помощью SQL Server Management Studio и задачи с именем **Database Restore**.

2.  После завершения задачи выберите файл резервной копии базы данных, выбрав параметр **с устройства** , а затем с помощью команды **Добавить** выберите файл Data MBAM Database **. bak** .

3.  Нажмите кнопку **ОК** , чтобы завершить процесс восстановления.

4.  Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:

    ```sql
    -- Restore MBAM Recovery Database. 

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

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

    **Примечание.**  
    Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:

    -   $PASSWORD $ — введите пароль, который вы использовали для шифрования файла закрытого ключа.



5.  С помощью Windows PowerShell можно вводить командную строку, подобную следующей:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Примечание.**  
    Замените приведенное ниже значение в приведенном выше примере, чтобы оно соответствовало вашей среде.

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, в который будет восстановлена база данных восстановления.



**Настройка доступа к базе данных восстановления на сервере B**

1.  На сервере B с помощью оснастки "Локальные пользователи и группы" в диспетчере серверов добавьте учетные записи компьютеров с каждого сервера, на котором запущена функция администрирования и мониторинга MBAM, в локальную группу с именем **MBAM и доступом к базе данных оборудования**.

2.  Убедитесь, что в восстановленной базе данных **MBAM и доступ** к базе данных с помощью учетной записи SQL Server сопоставлен с именем входа **$MachineName $ \\MBAM и доступом к базе данных оборудования**. Если оно не сопоставлено так, как описано, создайте другое имя для входа, совпадающее с участием в группах, и сопоставьте его имени для входа **$MachineName $ \\MBAM и получите доступ к базе данных оборудования**.

3.  Для автоматизации этой процедуры можно использовать Windows PowerShell на сервере B для ввода командной строки, которая похожа на приведенную ниже.

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Примечание.**  
    Замените следующие значения в приведенном выше примере соответствующими значениями для вашей среды.

    -   $DOMAIN $ \ \ $SERVERNAME $ $-введите домен и имя MBAM сервера администрирования и мониторинга. За именем сервера должен следовать $, как показано в примере (например, MyDomain\\MyServerName1 $).



~~~
This command line must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Обновление данных подключения к базе данных восстановления на серверах администрирования и мониторинга MBAM**

1. На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, обновите данные строки подключения для указанных ниже приложений, размещенных на веб-сайте администрирования и мониторинга, с помощью консоли диспетчера информационных служб Интернета (IIS).

   -   MBAMAdministrationService

   -   MBAMRecoveryAndHardwareService

2. Выберите каждое приложение и используйте функцию **редактора конфигурации** , расположенную в разделе **Управление** **представлением функций**.

3. В элементе управления **списком разделов** выберите параметр **configurationStrings** .

4. Выберите строку с именем **(коллекцией)** и откройте **Редактор коллекций** , нажав кнопку в правой части строки.

5. В **редакторе коллекции**выберите строку с именем **KeyRecoveryConnectionString** при обновлении конфигурации приложения MBAMAdministrationService или строки с именем <strong> Microsoft. MBAM. RecoveryAndHardwareDataStore. </strong> Строка подключения к обновлению конфигурации для MBAMRecoveryAndHardwareService.

6. Обновите **источник данных =** значение для свойства **configurationStrings** , чтобы получить список имени сервера и экземпляра (например, $SERVERNAME $ \ \ $SQLINSTANCENAME $), на который была перемещена база данных восстановления.

7. Для автоматизации этой процедуры вы можете ввести в Windows командную строку, подобную приведенной ниже, на каждом сервере администрирования и мониторинга.

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **Примечание.**  
   Замените приведенное ниже значение в приведенном выше примере, чтобы оно соответствовало вашей среде.

   -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, где находится база данных восстановления.



**Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM**

1.  На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для запуска веб-сайта MBAM, который называется **администрированием и мониторингом Microsoft BitLocker**.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, сходной с:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Переход на функцию соответствия и аудита базы данных


Если вы хотите перенести базу данных соответствия MBAM и аудита с одного компьютера на другой (то есть переместить базу данных с сервера A на сервер B), выполните указанные ниже действия. Этот процесс включает следующие высокоуровневые этапы.

1.  Остановите все экземпляры веб-сайта администрирования и наблюдения.

2.  Запустите настройку MBAM на сервере B.

3.  Создание резервной копии базы данных на сервере A.

4.  Переместить базу данных с сервера A в B.

5.  Восстановите базу данных на сервере B.

6.  Настройка доступа к базе данных на сервере B.

7.  Обновите данные подключения к базе данных на серверах администрирования и мониторинга MBAM.

8.  Обновите строку подключения к источнику данных отчетов SSRS с новым расположением базы данных соответствия требованиям и аудита.

9.  Возобновление всех экземпляров веб-сайта администрирования и мониторинга.

**Остановка всех экземпляров веб-сайта администрирования и мониторинга**

1.  На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.

    `PS C:\> Stop-s “Microsoft BitLocker Administration and Monitoring”`

    **Примечание.**  
    Чтобы выполнить эту командную строку, необходимо добавить в текущий экземпляр PowerShell модуль IIS для PowerShell. Кроме того, необходимо обновить политику выполнения PowerShell, чтобы разрешить выполнение сценариев.



**Запуск настройки MBAM на сервере B**

1.  Запустите настройку MBAM на сервере B и выберите только **базу данных соответствия требованиям и аудита** для установки.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$ TOPOLOGY=$X$`

    **Примечание.**  
    Примечание. Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, на который будет перемещена база данных соответствия и аудита.

    -   $DOMAIN $ \ \ $SERVERNAME $ — введите имена домена и сервера для каждого сервера администрирования и мониторинга MBAM, который будет обращаться к базе данных "соответствие требованиям и аудиту". Для разделения каждой пары доменных и серверных серверов в списке используйте точку с запятой (например, $DOMAIN \ \ \ \ \ домен \; $DOMAIN \ \ $SERVERNAME $ $). За именем каждого сервера должен следовать символ "$", как показано в примере (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).

    -   $DOMAIN $ \ \ $USERNAME $-введите домен и имя пользователя, которые будут использоваться функцией проверки соответствия и аудита для подключения к базе данных "соответствие требованиям" и "Аудит".

    -   $X $-введите **0** , если вы устанавливаете изолированную топологию MBAM или **1** при установке топологии Configuration Manager MBAM.



**Создание резервной копии базы данных соответствия требованиям и аудита на сервере A**

1.  Для резервного копирования базы данных соответствия требованиям и аудита на сервере A используйте SQL Server Management Studio и задачу с именем " **резервная копия**". По умолчанию в качестве имени базы данных используется **база данных состояния соответствия MBAM**.

2.  Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:

    ```sql
    -- Modify the MBAM Compliance Status Database to use the full recovery model.

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

    -- Back up the full MBAM Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  Запустите SQL-файл, используя командную строку Windows PowerShell, подобную приведенной ниже:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Примечание.**  
    Замените приведенное ниже значение в приведенном выше примере, чтобы оно соответствовало вашей среде.

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, из которого будет выполняться резервное копирование базы данных соответствия требованиям и аудита.



**Перенос базы данных соответствия требованиям и аудита с сервера A на B**

1.  Переместите следующие файлы с сервера A на сервер B с помощью проводника Windows.

    -   Данные базы данных о состоянии соответствия MBAM. bak

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Примечание.**  
    Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:

    -   $SERVERNAME $ — введите имя сервера, куда будут скопированы файлы.

    -   $DESTINATIONSHARE $ — введите имя и путь к папке, куда будут скопированы файлы.



**Восстановление базы данных соответствия и аудита на сервере B**

1.  Восстановите базу данных соответствия и аудита на сервере B с помощью SQL Server Management Studio и задачи с именем **Database Restore**.

2.  После завершения задачи выберите файл резервной копии базы данных, выбрав параметр **с устройства** , а затем с помощью команды **Добавить** выберите файл Data MBAM. bak (состояние соответствия требованиям к БД). Нажмите кнопку **ОК** , чтобы завершить процесс восстановления.

3.  Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  Запустите SQL-файл, используя командную строку Windows PowerShell, подобную приведенной ниже:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Примечание.**  
    Замените приведенное ниже значение в приведенном выше примере, чтобы оно соответствовало вашей среде.

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, на который будет восстановлена база данных соответствия требованиям и аудита.



**Настройка доступа к базе данных "соответствие требованиям" и "Аудит" на сервере B**

1.  На сервере B с помощью оснастки "Локальные пользователи и группы" в диспетчере серверов добавьте учетные записи компьютеров с каждого сервера, на котором запущена функция администрирования и мониторинга MBAM, в локальную группу с именем **MBAM соответствия требованиям к базе данных**.

2.  Убедитесь, что доступ к базе данных **аудита соответствия MBAM** для учетной записи SQL для восстановленной базы данных сопоставлен с именем для входа **$MachineName $ \ \ MBAM аудит соответствия требованиям к БД**. Если оно не сопоставлено так, как описано, создайте другое имя для входа, совпадающее с участием в группах, и сопоставьте его имени для входа **$MachineName $ \ \ MBAM для аудита соответствия требованиям к БД**.

3.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки на сервере B, похожей на указанные ниже.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Примечание.**  
    Замените следующие значения в приведенном выше примере соответствующими значениями для вашей среды.

    -   $DOMAIN $ \ \ $SERVERNAME $ $-введите домен и имя MBAM сервера администрирования и мониторинга. За именем сервера должен следовать "$", как показано в примере. (например, MyDomain\\MyServerName1 $)

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $ — введите имя учетной записи пользователя, которое использовалось для настройки источника данных для отчетов о соответствии и аудите.



~~~
The command line for adding the servers to the MBAM Compliance and Audit Database access local group must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM**

1.  На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для обновления данных строки подключения для следующих приложений, размещенных на веб-сайте администрирования и мониторинга.

    -   MBAMAdministrationService

    -   MBAMComplianceStatusService

2.  Выберите каждое приложение и используйте функцию **редактора конфигурации** , расположенную в разделе **Управление** **представлением функций**.

3.  В элементе управления **списком разделов** выберите параметр **configurationStrings** .

4.  Выберите строку с именем **(коллекцией)** и откройте **Редактор коллекций** , нажав кнопку в правой части строки.

5.  В **редакторе коллекций**выберите строку с именем **ComplianceStatusConnectionString** при обновлении конфигурации для приложения MBAMAdministrationService или строку с именем **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString** при обновлении конфигурации для MBAMComplianceStatusService.

6.  Обновите **источник данных =** значение свойства **configurationStrings** , чтобы получить список имен сервера и экземпляра (например, $SERVERNAME $ \ \ $SQLINSTANCENAME), в который была перемещена база данных восстановления.

7.  Для автоматизации этой процедуры вы можете ввести командную строку для каждого сервера администрирования и наблюдения с помощью Windows, как показано ниже.

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **Примечание.**  
    Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, где находится база данных восстановления.



**Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM**

1.  На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для запуска веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Перемещение отчетов о соответствии и аудите


Если вы хотите перенести отчеты о соответствии MBAM и аудиты с одного компьютера на другой (то есть переместить отчеты с сервера A на сервер B), выполните указанные ниже действия, в том числе следующие высокоуровневые этапы.

1.  Запустите настройку MBAM на сервере B.

2.  Настройка доступа к отчетам о соответствии и аудиту на сервере B.

3.  Остановите все экземпляры веб-сайта администрирования и мониторинга MBAM.

4.  Обновите данные соединения отчетов на серверах администрирования и мониторинга MBAM.

5.  Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM.

**Запуск настройки MBAM на сервере B**

1.  Запустите настройку MBAM на сервере B и выберите только **отчеты о соответствии и аудите** для установки.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$ TOPOLOGY=$X$`

    **Примечание.**  
    Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, в котором находится база данных соответствия требованиям и аудита.

    -   $DOMAIN $ \ \ $USERNAME $-введите домен и имя пользователя, которые будут использоваться функцией проверки соответствия и аудита для подключения к базе данных "соответствие требованиям" и "Аудит".

    -   $PASSWORD $-введите пароль учетной записи пользователя, который будет использоваться для подключения к базе данных "соответствие требованиям" и "Аудит".

    -   $X $-введите **0** , если вы устанавливаете изолированную топологию MBAM или **1** при установке топологии Configuration Manager MBAM.



**Настройка доступа к отчетам о соответствии и аудиту на сервере B**

1.  На сервере B с помощью оснастки "Локальные пользователи и группы" в диспетчере серверов добавьте учетные записи пользователей, которые получат доступ к отчетам о соответствии и аудите. Добавьте учетные записи пользователей в локальную группу с именем Пользователи отчета MBAM.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки на сервере B, похожей на указанные ниже.

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Примечание.**  
    Замените следующие значения в приведенном выше примере соответствующими значениями для вашей среды.

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $ — введите имя учетной записи пользователя, которое использовалось для настройки источника данных для отчетов о соответствии и аудите.



~~~
The command line for adding the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**Остановка всех экземпляров веб-сайта администрирования и мониторинга MBAM**

1.  На каждом сервере, на котором запущена функция администрирования и сервера мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM**

1. На каждом сервере, на котором запущена функция администрирования и сервера мониторинга MBAM, обновите URL-адрес отчетов о соответствии и аудите с помощью консоли диспетчера служб IIS.

2. Выберите веб-сайт **администрирования Microsoft BitLocker и наблюдение за** ним с помощью средства **редактирования конфигурации** , расположенного в разделе **Управление** **представлением функций**.

3. В элементе управления **списком разделов** выберите параметр **appSettings** .

4. Выберите строку с именем **(коллекцией)** и откройте **Редактор коллекций** , нажав кнопку в правой части строки.

5. В **редакторе коллекций**выберите строку с названием **Microsoft. MBAM. Reports. URL**.

6. Обновите значение **Microsoft. MBAM. Reports. URL** , чтобы оно отражало имя сервера для сервера B. Если функция проверки соответствия и аудита была установлена на именованном экземпляре служб SQL Reporting Services, не забудьте добавить или обновить имя экземпляра по URL-адресу (например, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....)

7. Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки на каждом сервере администрирования и наблюдения, которая аналогична описанной ниже:

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\ \sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/ Microsoft+BitLocker+Administration+and+Monitoring/”`

   **Примечание.**  
   Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:

   -   $SERVERNAME $-введите имя сервера, на котором установлены отчеты о соответствии и аудите.

   -   $SRSINSTANCENAME $ — введите имя экземпляра служб SQL Reporting Services, для которого установлены отчеты о соответствии и аудите.



**Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM**

1.  На каждом сервере, на котором запущена функция администрирования и сервера мониторинга MBAM, используйте консоль диспетчера служб IIS для запуска веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **Примечание.**  
    Чтобы выполнить эту командную строку, необходимо добавить модуль IIS для PowerShell в текущий экземпляр PowerShell. Кроме того, необходимо обновить политику выполнения PowerShell, чтобы разрешить выполнение сценариев.



## Перемещение функций администрирования и мониторинга


Если вы хотите переместить функцию отчетов администрирования и мониторинга MBAM с одного компьютера на другой (то есть, переместить компонент с сервера A на сервер B), выполните указанные ниже действия, в том числе следующие высокоуровневые этапы.

1.  Запустите настройку MBAM на сервере B.

2.  Настройка доступа к базе данных на сервере B.

**Запуск настройки MBAM на сервере B**

1.  Запустите настройку MBAM на сервере B и выберите компонент **сервера администрирования и мониторинга** для установки.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer, COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$ TOPOLOGY=$X$`

    **Примечание.**  
    Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $ — для параметра COMPLIDB \ _SQLINSTANCE введите имя сервера и экземпляр, в котором находится база данных соответствия требованиям и аудита. Для параметра RECOVERYANDHWDB \ _SQLINSTANCE введите имя сервера и экземпляр, где находится база данных восстановления.

    -   $DOMAIN $ \ \ $USERNAME $-введите домен и имя пользователя, которые будут использоваться функцией проверки соответствия и аудита для подключения к базе данных "соответствие требованиям" и "Аудит".

    -   $ REPORTSSERVERURL $ — введите URL-адрес домашнего расположения веб-сайта службы отчетов SQL. Если отчеты были установлены в экземпляре SRS по умолчанию, формат URL-адреса будет иметь формат "http://$SERVERNAME $/ReportServer". Если отчеты были установлены в экземпляре SRS по умолчанию, формат URL-адреса будет иметь формат "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $".

    -   $X $-введите **0** , если вы устанавливаете изолированную топологию MBAM или **1** при установке топологии Configuration Manager MBAM.



**Настройка доступа к базам данных**

1.  На сервере или серверах, на которых развернута база данных восстановления и соответствие требованиям и учетной записи, используйте оснастку "Локальные пользователи и группы" в диспетчере серверов, чтобы добавить учетные записи компьютеров с сервера, на котором работает сервер MBAM **администрирования и мониторинга** , в локальные группы с именами **MBAM Recovery**

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая аналогична приведенной ниже, на сервере, на котором развернута база данных соответствия и аудита.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

3.  На сервере, на котором развернута база данных восстановления, вы можете использовать Windows PowerShell для ввода следующей командной строки:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Примечание.**  
    Замените приведенное ниже значение в приведенном выше примере на применимые значения для вашей среды.

    -   $DOMAIN $ \ \ $SERVERNAME $ $-введите домен и имя сервера администрирования и мониторинга. За именем сервера должен следовать символ "$", как показано в примере (например, MyDomain\\MyServerName1 $).

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $ — введите имя учетной записи пользователя, которое использовалось для настройки источника данных для отчетов о соответствии и аудите.



~~~
The command lines that are listed for adding server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## Статьи по теме


[Обслуживание MBAM 2.0](maintaining-mbam-20-mbam-2.md)









