---
title: Перемещение компонентов MBAM 1.0 на другой компьютер
description: Перемещение компонентов MBAM 1.0 на другой компьютер
author: dansimp
ms.assetid: e1907d92-6b42-4ba3-b0e4-60a9cc8285cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 874c3983220f341e39fa5fb7c60f655e2f208082
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812949"
---
# Перемещение компонентов MBAM 1.0 на другой компьютер


В этой статье описаны действия, которые необходимо выполнить для перемещения одной или нескольких функций администрирования и мониторинга Microsoft BitLocker (MBAM) на другой компьютер. Если вы перемещаете более одной функции MBAM на другой компьютер, вы должны переместить их в указанном ниже порядке.

1.  База данных восстановления и оборудования

2.  База данных соответствия требованиям и аудита

3.  Отчеты о соответствии и аудите

4.  Администрирование и мониторинг

## Перемещение базы данных восстановления и оборудования


Вы можете использовать описанную ниже процедуру для перемещения базы данных восстановления MBAM и оборудования с одного компьютера на другой (вы можете переместить эту функцию сервера MBAM с сервера A на сервер B):

****

1.  Остановите все экземпляры веб-сайта администрирования и мониторинга MBAM.

2.  Запустите настройку MBAM на сервере B.

3.  Создание резервной копии базы данных восстановления MBAM и конфигурации оборудования на сервере A.

4.  MBAM восстановления и базы данных оборудования с сервера A в B

5.  Восстановление MBAM базы данных восстановления и оборудования на сервере B

6.  Настройка доступа к базе данных восстановления MBAM и конфигурации оборудования на сервере B

7.  Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM

8.  Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM

**Отключение всех экземпляров веб-сайта администрирования и мониторинга MBAM**

1.  С помощью консоли диспетчера служб IIS остановите веб-сайт MBAM на каждом сервере, на котором работает функция администрирования и мониторинга MBAM. Веб-сайт MBAM называется **администрированием и мониторингом Microsoft BitLocker**.

2.  Для автоматизации этой процедуры вы можете использовать в командной строке командную команду, подобную приведенной ниже, с помощью Windows PowerShell.

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Примечание.**  
    Чтобы запустить эту командную команду PowerShell, необходимо добавить в текущий экземпляр PowerShell модуль IIS для PowerShell. Кроме того, необходимо обновить политику выполнения PowerShell, чтобы обеспечить выполнение сценариев.



**Запуск настройки MBAM на сервере B**

1.  Запустите настройку MBAM на сервере B и выберите базу данных восстановления и оборудования для установки.

2.  Для автоматизации этой процедуры вы можете использовать в командной строке командную команду, подобную приведенной ниже, с помощью Windows PowerShell.

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **Примечание.**  
    Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, на который будет перемещена база данных восстановления и оборудования.

    -   $DOMAIN $ \ \ $SERVERNAME $-введите имена домена и сервера для каждого приложения MBAM и сервера мониторинга, которые будут обращаться к базе данных восстановления и оборудования. Если у вас несколько имен домена и сервера, для разделения каждого из них в списке используйте точку с запятой. Например, $DOMAIN _сервера $; $DOMAIN \ \ $SERVERNAME $ $. Кроме того, за именем каждого сервера должен следовать a **$** . Например, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.



**Создание резервной копии базы данных на сервере A**

1.  Для резервного копирования базы данных восстановления и оборудования на сервере A используйте SQL Server Management Studio и задачу с именем **резервное копирование..**.. По умолчанию имя базы данных **MBAM восстановлением и базой данных оборудования**.

2.  Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:

    Измените базу данных MBAM восстановления и оборудования, чтобы использовать режим полного восстановления.

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    Создавайте резервные копии MBAM и данные в базе данных оборудования и MBAM восстановления для логических устройств архивации.

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    Создавайте резервные копии всей базы данных восстановления MBAM и оборудования.

    ```sql
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
    Замените значения из предыдущего примера на те, которые соответствуют вашей среде:

    -   $PASSWORD $-введите пароль, который будет использоваться для шифрования файла закрытого ключа.



3.  Выполните SQL-файл с помощью SQL Server PowerShell и команды, аналогичные приведенным ниже.

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Примечание.**  
    Замените в предыдущем примере значение, совпадающее с вашей средой.

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $ — введите имя сервера и экземпляр, из которого вы хотите создать резервную копию базы данных восстановления и оборудования.



**Чтобы переместить базу данных и сертификат с сервера A в B**

1.  Перемещайте данные восстановления MBAM и базы данных оборудования. bak с сервера A на сервер B с помощью проводника Windows.

2.  Чтобы переместить сертификат для зашифрованной базы данных, необходимо выполнить описанные ниже действия по автоматизации. Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода команды, которая похожа на приведенную ниже.

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Примечание.**  
    Замените значение из предыдущего примера на те, которые соответствуют вашей среде:

    -   $SERVERNAME $-введите имя сервера, на который будут скопированы файлы.

    -   $DESTINATIONSHARE $-введите имя общего доступа и путь к файлам, куда они будут скопированы.



**Восстановление базы данных на сервере B**

1.  Восстановите базу данных восстановления и оборудования на сервере B с помощью SQL Server Management Studio и задачи с именем **Database Restore**.

2.  После выполнения задачи выберите файл резервной копии базы данных, выбрав параметр **с устройства** , а затем с помощью команды **Добавить** выберите файл Data Recovery и MBAM Database **. bak** .

3.  Нажмите кнопку **ОК** , чтобы завершить процесс восстановления.

4.  Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    Удалите сертификат, созданный программой установки MBAM.

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    Добавление сертификата

    ```sql
    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

        FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

        DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

    Восстановите данные базы данных MBAM восстановления и оборудования, а также файлы журнала.

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **Примечание.**  
    Замените значения из предыдущего примера на те, которые соответствуют вашей среде:

    -   $PASSWORD $-введите пароль, который вы использовали для шифрования файла закрытого ключа.



5.  С помощью Windows PowerShell введите командную строку, подобную следующей:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Примечание.**  
    Замените значение из примера receding на те, которые соответствуют вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, на который будет восстановлена база данных восстановления и оборудования.



**Настройка доступа к базе данных на сервере B**

1.  На сервере B с помощью оснастки "Локальные пользователи и группы" в диспетчере серверов можно добавить учетные записи компьютеров с каждого сервера, на котором запущена функция администрирования и мониторинга MBAM, в локальную группу с именем **MBAM и доступом к базе данных оборудования**.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell на сервере B для ввода команды, которая похожа на приведенную ниже.

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Примечание.**  
    Замените значения из предыдущего примера соответствующими значениями для вашей среды.

    -   $DOMAIN $ \ \ $SERVERNAME $ $-введите имя домена и имя компьютера сервера MBAM администрирования и мониторинга. За именем сервера должен следовать a **$** , например, MyDomain\\MyServerName1 $.



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM**

1. На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для обновления данных строки подключения для указанных ниже приложений, размещенных на веб-сайте администрирования и мониторинга Microsoft BitLocker.

   -   Служба администрирования MBAM

   -   MBAM восстановления и обслуживания оборудования

2. Выберите каждое приложение и используйте функцию **редактора конфигурации** , расположенную в разделе **Управление** **представлением функций**.

3. В элементе управления списком разделов выберите параметр **configurationStrings** .

4. Выберите строку с именем **(коллекцией)** и откройте **Редактор коллекций** , нажав кнопку в правой части строки.

5. В **редакторе коллекции**выберите строку с именем **KeyRecoveryConnectionString** , если вы обновили конфигурацию для приложения "MBAMAdministrationService", или выберите строку с именем <strong> Microsoft. MBAM. RecoveryAndHardwareDataStore. </strong> ConnectionString при обновлении конфигурации для "MBAMRecoveryAndHardwareService".

6. Обновите **источник данных =** значение для свойства **configurationStrings** , чтобы вывести имя сервера и экземпляр, на который была перемещена база данных восстановления и оборудования. Например, $SERVERNAME $ \ \ $SQLINSTANCENAME $.

7. Для автоматизации этой процедуры вы можете использовать команду Windows PowerShell на каждом сервере администрирования и наблюдения, которая похожа на приведенную ниже.

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **Примечание.**  
   Замените значение из предыдущего примера на те, которые соответствуют вашей среде:

   -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, где находится база данных восстановления и оборудования.



**Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM**

1.  На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для запуска веб-сайта MBAM, который называется **администрированием и мониторингом Microsoft BitLocker**.

2.  Для автоматизации этой процедуры можно использовать команду Windows PowerShell, похожую на одну из приведенных ниже команд.

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Перемещение функции базы данных состояния соответствия требованиям


Если вы решили переместить функцию базы данных состояния соответствия MBAM с одного компьютера на другой, например с сервера A на сервер B, необходимо выполнить описанные ниже действия.

1.  Остановка всех экземпляров веб-сайта администрирования и мониторинга MBAM

2.  Запуск настройки MBAM на сервере B

3.  Резервное копирование базы данных на сервере A

4.  Перемещение базы данных с сервера A в B

5.  Восстановление базы данных на сервере B

6.  Настройка доступа к базе данных на сервере B

7.  Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM

8.  Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM

**Отключение всех экземпляров веб-сайта администрирования и мониторинга MBAM**

1.  На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта MBAM, который называется **администрированием и мониторингом Microsoft BitLocker**.

2.  Для автоматизации этой процедуры можно использовать команду Windows PowerShell, похожую на одну из приведенных ниже команд.

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Примечание.**  
    Для выполнения этой команды необходимо добавить модуль IIS для PowerShell в текущий экземпляр PowerShell. Кроме того, необходимо обновить политику выполнения PowerShell, чтобы обеспечить выполнение сценариев.



**Запуск настройки MBAM на сервере B**

1.  Запустите настройку MBAM на сервере B и выберите компонент базы данных состояния соответствия требованиям для установки.

2.  Для автоматизации этой процедуры можно использовать команду Windows PowerShell, похожую на одну из приведенных ниже команд.

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **Примечание.**  
    Замените значения из предыдущего примера на те, которые соответствуют вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, в который будет перемещена база данных состояния соответствия требованиям.

    -   $DOMAIN $ \ \ $SERVERNAME $-введите имена доменов и имена серверов для каждого приложения MBAM и сервера мониторинга, которые будут обращаться к базе данных о состоянии соответствия требованиям. Если вы используете несколько доменных имен и имен серверов, для разделения каждого из них в списке используйте точку с запятой. Например, $DOMAIN _сервера $; $DOMAIN \ \ $SERVERNAME $ $. За именем каждого сервера должен следовать a, **$** как показано в примере. Например, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.

    -   $DOMAIN $ \ \ $USERNAME $-введите домен и имя пользователя, которые будут использоваться функцией проверки соответствия и аудита для подключения к базе данных состояния соответствия требованиям.



**Создание резервной копии базы данных соответствия на сервере A**

1.  Чтобы создать резервную копию базы данных соответствия на сервере A, используйте SQL Server Management Studio и задачу с именем **резервное копирование..**.. По умолчанию в качестве имени базы данных используется **база данных состояния соответствия MBAM**.

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

    -- Back up the full MBAM Recovery and Hardware database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  Запустите SQL-файл с помощью команды, подобной приведенной ниже, используя SQL Server PowerShell.

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Примечание.**  
    Замените значение из предыдущего примера на те, которые соответствуют вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, из которого будет создаваться резервная копия базы данных состояния соответствия требованиям.



**Чтобы переместить базу данных с сервера A в B**

1.  Переместите указанные ниже файлы с сервера A на сервер B с помощью проводника Windows.

    -   Данные базы данных о состоянии соответствия MBAM. bak

2.  Для автоматизации этой процедуры можно использовать команду, подобную описанной ниже, с помощью Windows PowerShell.

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Примечание.**  
    Замените значение из предыдущего примера на те, которые соответствуют вашей среде:

    -   $SERVERNAME $ — введите имя сервера, куда будут скопированы файлы.

    -   $DESTINATIONSHARE $ — введите имя и путь к папке, куда будут скопированы файлы.



**Восстановление базы данных на сервере B**

1.  Восстановите базу данных состояния соответствия на сервере B с помощью SQL Server Management Studio и задачи **RESTORE DATABASE.**...

2.  После выполнения задачи выберите файл резервной копии базы данных, выбрав параметр с устройства, а затем с помощью команды Добавить выберите файл Data MBAM. bak (состояние соответствия требованиям к БД). Нажмите кнопку ОК, чтобы завершить процесс восстановления.

3.  Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  Запустите SQL-файл с помощью команды, подобной приведенной ниже, используя SQL Server PowerShell.

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Примечание.**  
    Замените значение из предыдущего примера на те, которые соответствуют вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, на который будет восстанавливаться база данных состояния соответствия требованиям.



**Настройка доступа к базе данных на сервере B**

1.  На сервере B с помощью оснастки "локальный пользователь и группы" в диспетчере серверов добавьте учетные записи компьютеров с каждого сервера, на котором запускается функция администрирования и мониторинга MBAM, в локальную группу с именем **MBAM соответствие требованиям Access**.

2.  Для автоматизации этой процедуры можно использовать команду Windows PowerShell на сервере B, которая похожа на указанную ниже.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Примечание.**  
    Замените значение из предыдущего примера соответствующими значениями для вашей среды.

    -   $DOMAIN $ \ \ $SERVERNAME $ $-введите домен и имя MBAM сервера администрирования и мониторинга. За именем сервера должно следовать a **$** . Например, MyDomain\\MyServerName1 $.

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-введите имя учетной записи пользователя, которое использовалось для настройки источника данных для отчетов о соответствии и аудите.



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM**

1.  На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для обновления данных строки подключения для указанных ниже приложений, размещенных на веб-сайте администрирования и мониторинга Microsoft BitLocker.

    -   MBAMAdministrationService

    -   MBAMComplianceStatusService

2.  Выберите каждое приложение и используйте функцию **редактора конфигурации** , расположенную в разделе **Управление** **представлением функций**.

3.  В элементе управления списком разделов выберите параметр **configurationStrings** .

4.  Выберите строку с именем **(коллекцией)** и откройте редактор коллекций, нажав кнопку в правой части строки.

5.  В **редакторе коллекции**выберите строку с именем **ComplianceStatusConnectionString**, при обновлении конфигурации для приложения MBAMAdministrationService или строку с именем **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString**, при обновлении конфигурации для MBAMComplianceStatusService.

6.  Обновите **источник данных =** значение для свойства **configurationStrings** , чтобы вывести имя сервера и имя экземпляра. Например, $SERVERNAME $ \ \ $SQLINSTANCENAME, на который была перемещена база данных восстановления и оборудования.

7.  Для автоматизации этой процедуры вы можете использовать Windows PowerShell для ввода команды, сходной с одной из следующих на каждом сервере администрирования и наблюдения.

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **Примечание.**  
    Замените значение из предыдущего примера на те, которые соответствуют вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и имя экземпляра, где находится база данных восстановления и оборудования.



**Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM**

1.  На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для запуска веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода команды, которая похожа на приведенную ниже.

    **PS C:\\ &gt; Start-website "Администрирование и мониторинг Microsoft BitLocker"**

## Перемещение отчетов о соответствии и аудите


Если вы решили переместить отчеты о соответствии MBAM и аудиты между компьютерами (например, если вы перемещаете компонент с сервера A на сервер B), необходимо выполнить описанные ниже действия и шаги.

1.  Запуск настройки MBAM на сервере B

2.  Настройка доступа к отчетам о соответствии и аудиту на сервере B

3.  Остановка всех экземпляров веб-сайта администрирования и мониторинга MBAM

4.  Обновление данных о соединениях на серверах администрирования и мониторинга MBAM

5.  Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM

**Запуск настройки MBAM на сервере B**

1.  Запустите настройку MBAM на сервере B и выберите компонент "соответствие требованиям и аудит" для установки.

2.  Для автоматизации этой процедуры можно использовать команду Windows PowerShell, подобную приведенной ниже.

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **Примечание.**  
    Замените значения из предыдущего примера на те, которые соответствуют вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, в котором находится база данных состояния соответствия требованиям.

    -   $DOMAIN $ \ \ $USERNAME $-введите доменное имя и имя пользователя, которые будут использоваться функцией "отчеты о соответствии и аудите" для подключения к базе данных состояния соответствия требованиям.

    -   $PASSWORD $ — введите пароль учетной записи пользователя, который будет использоваться для подключения к базе данных состояния соответствия требованиям.



**Настройка доступа к отчетам о соответствии и аудиту на сервере B**

1.  На сервере B с помощью оснастки "Локальные пользователи и группы" в диспетчере серверов добавьте учетные записи пользователей, которые получат доступ к отчетам о соответствии и аудите. Добавьте учетные записи пользователей в локальную группу с именем "Пользователи отчетов MBAM".

2.  Для автоматизации этой процедуры можно использовать команду Windows PowerShell на сервере B, которая похожа на приведенную ниже.

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Примечание.**  
    Замените приведенное ниже значение из предыдущего примера на применимые значения для вашей среды.

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-введите имя учетной записи пользователя, которое использовалось для настройки источника данных для отчетов о соответствии и аудите.



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**Отключение всех экземпляров веб-сайта администрирования и мониторинга MBAM**

1.  На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.

2.  Для автоматизации этой процедуры можно использовать команду Windows PowerShell, похожую на одну из приведенных ниже команд.

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM**

1. На каждом из серверов, на которых выполняется функция администрирования и мониторинга MBAM, обновите URL-адрес отчетов о соответствиях с помощью консоли диспетчера служб IIS.

2. Выберите веб-сайт **администрирования и наблюдения Microsoft BitLocker** и используйте средство **редактирования конфигурации** , которое можно найти в разделе " **Управление** " в **представлении "возможности**".

3. В элементе управления списком разделов выберите параметр **appSettings** .

4. В этой статье выберите строку с именем **(коллекцией)** и откройте **Редактор коллекции** , нажав кнопку в правой части строки.

5. В **редакторе коллекций**выберите строку с именем "Microsoft. MBAM. Reports. URL".

6. Обновите значение Microsoft. MBAM. Reports. URL, чтобы оно отражало имя сервера для сервера B. Если функция проверки соответствия и аудита была установлена на именованном экземпляре служб SQL Reporting Services, убедитесь, что вы добавите или обновите имя экземпляра в URL-адрес. Например, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....

7. Для автоматизации этой процедуры вы можете использовать Windows PowerShell для ввода команды, сходной с одной из следующих на каждом сервере администрирования и наблюдения.

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **Примечание.**  
   Замените значение из предыдущего примера на те, которые соответствуют вашей среде:

   -   $SERVERNAME $-введите имя сервера, на котором установлены отчеты о соответствии и аудите.

   -   $SRSINSTANCENAME $ — введите имя экземпляра служб SQL Reporting Services, для которого установлены отчеты о соответствии и аудите.



**Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM**

1.  На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для запуска веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.

2.  Для автоматизации этой процедуры можно использовать команду Windows PowerShell, похожую на одну из приведенных ниже команд.

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **Примечание.**  
    Для выполнения этой команды необходимо добавить модуль IIS для PowerShell в текущий экземпляр PowerShell. Кроме того, необходимо обновить политику выполнения PowerShell, чтобы разрешить выполнение сценариев.



## Перемещение компонента администрирования и наблюдения


Если вы решили переместить функцию отчетов администрирования и мониторинга MBAM с одного компьютера на другой (если вы перемещаете компонент с сервера A на сервер B), необходимо выполнить описанные ниже действия. Процесс включает следующие шаги:

1.  Запуск настройки MBAM на сервере B

2.  Настройка доступа к базе данных на сервере B

**Запуск настройки MBAM на сервере B**

1.  Запустите настройку MBAM на сервере B и выберите компонент администрирования для установки.

2.  Для автоматизации этой процедуры можно использовать команду Windows PowerShell, похожую на одну из приведенных ниже команд.

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **Примечание.**  
    Замените значения из предыдущего примера на те, которые соответствуют вашей среде:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $ — для параметра COMPLIDB \ _SQLINSTANCE введите имя сервера и экземпляр, в котором находится база данных состояния соответствия требованиям. Для параметра RECOVERYANDHWDB \ _SQLINSTANCE введите имя сервера и экземпляр, где находится база данных восстановления и оборудования.

    -   $DOMAIN $ \ \ $USERNAME $-введите домен и имя пользователя, которые будут использоваться функцией проверки соответствия и аудита для подключения к базе данных состояния соответствия требованиям.

    -   $ REPORTSSERVERURL $ — введите URL-адрес домашнего расположения веб-сайта службы отчетов SQL. Если отчеты были установлены в экземпляре SRS по умолчанию, формат URL-адреса будет отформатирован как "http://$SERVERNAME $/ReportServer". Если отчеты были установлены в экземпляре SRS по умолчанию, формат URL-адреса будет отформатирован в формате "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $".



**Настройка доступа к базам данных**

1.  На сервере или серверах, на которых восстановлено и оборудование; и базы данных проверки соответствия и аудита развертываются с помощью оснастки "Локальные пользователи и группы" в диспетчере серверов, чтобы добавить учетные записи компьютеров с каждого сервера, на котором запущена функция администрирования и мониторинга MBAM, в локальные группы с именем "MBAM Recovery и DB (сервер DB)" (восстановление и доступ к базам данных оборудования) и "MBAM соответствие требованиям к БД"

2.  Для автоматизации этой процедуры можно использовать командную команду Windows PowerShell на сервере, на котором развернуты базы данных соответствия и аудита.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  На сервере, на котором развернуты базы данных восстановления и оборудования, выполните команду, подобную следующей, с помощью Windows PowerShell.

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Примечание.**  
    Замените значение из предыдущего примера соответствующими значениями для вашей среды.

    -   $DOMAIN $ \ \ $SERVERNAME $ $-введите домен и имя MBAM сервера администрирования и мониторинга. За именем сервера должно следовать a **$** . Например, MyDomain\\MyServerName1 $)

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $ — введите имя учетной записи пользователя, которое использовалось для настройки источника данных для отчетов о соответствии и аудите.



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## Статьи по теме


[Администрирование компонентов MBAM 1.0](administering-mbam-10-features.md)









