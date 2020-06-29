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
# <span data-ttu-id="668ea-103">Перемещение компонентов MBAM 1.0 на другой компьютер</span><span class="sxs-lookup"><span data-stu-id="668ea-103">How to Move MBAM 1.0 Features to Another Computer</span></span>


<span data-ttu-id="668ea-104">В этой статье описаны действия, которые необходимо выполнить для перемещения одной или нескольких функций администрирования и мониторинга Microsoft BitLocker (MBAM) на другой компьютер.</span><span class="sxs-lookup"><span data-stu-id="668ea-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="668ea-105">Если вы перемещаете более одной функции MBAM на другой компьютер, вы должны переместить их в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="668ea-105">When you move more than one MBAM feature to another computer, you should move them in the following order:</span></span>

1.  <span data-ttu-id="668ea-106">База данных восстановления и оборудования</span><span class="sxs-lookup"><span data-stu-id="668ea-106">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="668ea-107">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="668ea-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="668ea-108">Отчеты о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="668ea-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="668ea-109">Администрирование и мониторинг</span><span class="sxs-lookup"><span data-stu-id="668ea-109">Administration and Monitoring</span></span>

## <span data-ttu-id="668ea-110">Перемещение базы данных восстановления и оборудования</span><span class="sxs-lookup"><span data-stu-id="668ea-110">To move the Recovery and Hardware Database</span></span>


<span data-ttu-id="668ea-111">Вы можете использовать описанную ниже процедуру для перемещения базы данных восстановления MBAM и оборудования с одного компьютера на другой (вы можете переместить эту функцию сервера MBAM с сервера A на сервер B):</span><span class="sxs-lookup"><span data-stu-id="668ea-111">You can use the following procedure to move the MBAM Recovery and Hardware Database from one computer to another (you can move this MBAM Server feature from Server A to Server B):</span></span>

****

1.  <span data-ttu-id="668ea-112">Остановите все экземпляры веб-сайта администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="668ea-112">Stop all instances of the MBAM Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="668ea-113">Запустите настройку MBAM на сервере B.</span><span class="sxs-lookup"><span data-stu-id="668ea-113">Run the MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="668ea-114">Создание резервной копии базы данных восстановления MBAM и конфигурации оборудования на сервере A.</span><span class="sxs-lookup"><span data-stu-id="668ea-114">Back up the MBAM Recovery and Hardware database on Server A.</span></span>

4.  <span data-ttu-id="668ea-115">MBAM восстановления и базы данных оборудования с сервера A в B</span><span class="sxs-lookup"><span data-stu-id="668ea-115">MBAM Recovery and Hardware database from Server A to B</span></span>

5.  <span data-ttu-id="668ea-116">Восстановление MBAM базы данных восстановления и оборудования на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-116">Restore the MBAM Recovery and Hardware database on Server B</span></span>

6.  <span data-ttu-id="668ea-117">Настройка доступа к базе данных восстановления MBAM и конфигурации оборудования на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-117">Configure the access to the MBAM Recovery and Hardware database on Server B</span></span>

7.  <span data-ttu-id="668ea-118">Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-118">Update the database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="668ea-119">Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-119">Resume all instances of the MBAM Administration and Monitoring web site</span></span>

**<span data-ttu-id="668ea-120">Отключение всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-120">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="668ea-121">С помощью консоли диспетчера служб IIS остановите веб-сайт MBAM на каждом сервере, на котором работает функция администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="668ea-121">Use the Internet Information Services (IIS) Manager console to stop the MBAM website on each of the servers that run the MBAM Administration and Monitoring feature.</span></span> <span data-ttu-id="668ea-122">Веб-сайт MBAM называется **администрированием и мониторингом Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="668ea-122">The MBAM website is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="668ea-123">Для автоматизации этой процедуры вы можете использовать в командной строке командную команду, подобную приведенной ниже, с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="668ea-123">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="668ea-124">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-124">Note</span></span>**  
    <span data-ttu-id="668ea-125">Чтобы запустить эту командную команду PowerShell, необходимо добавить в текущий экземпляр PowerShell модуль IIS для PowerShell.</span><span class="sxs-lookup"><span data-stu-id="668ea-125">To run this PowerShell command prompt, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="668ea-126">Кроме того, необходимо обновить политику выполнения PowerShell, чтобы обеспечить выполнение сценариев.</span><span class="sxs-lookup"><span data-stu-id="668ea-126">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="668ea-127">Запуск настройки MBAM на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-127">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="668ea-128">Запустите настройку MBAM на сервере B и выберите базу данных восстановления и оборудования для установки.</span><span class="sxs-lookup"><span data-stu-id="668ea-128">Run the MBAM setup on Server B and select the Recovery and Hardware Database for installation.</span></span>

2.  <span data-ttu-id="668ea-129">Для автоматизации этой процедуры вы можете использовать в командной строке командную команду, подобную приведенной ниже, с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="668ea-129">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="668ea-130">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-130">Note</span></span>**  
    <span data-ttu-id="668ea-131">Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-131">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="668ea-132">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, на который будет перемещена база данных восстановления и оборудования.</span><span class="sxs-lookup"><span data-stu-id="668ea-132">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery and Hardware database will be moved.</span></span>

    -   <span data-ttu-id="668ea-133">$DOMAIN $ \ \ $SERVERNAME $-введите имена домена и сервера для каждого приложения MBAM и сервера мониторинга, которые будут обращаться к базе данных восстановления и оборудования.</span><span class="sxs-lookup"><span data-stu-id="668ea-133">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Application and Monitoring Server that will contact the Recovery and Hardware database.</span></span> <span data-ttu-id="668ea-134">Если у вас несколько имен домена и сервера, для разделения каждого из них в списке используйте точку с запятой.</span><span class="sxs-lookup"><span data-stu-id="668ea-134">If there are multiple domain and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="668ea-135">Например, $DOMAIN _сервера $; $DOMAIN \ \ $SERVERNAME $ $.</span><span class="sxs-lookup"><span data-stu-id="668ea-135">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="668ea-136">Кроме того, за именем каждого сервера должен следовать a **$** .</span><span class="sxs-lookup"><span data-stu-id="668ea-136">Additionally, each server name must be followed by a **$**.</span></span> <span data-ttu-id="668ea-137">Например, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="668ea-137">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>



**<span data-ttu-id="668ea-138">Создание резервной копии базы данных на сервере A</span><span class="sxs-lookup"><span data-stu-id="668ea-138">To back up the Database on Server A</span></span>**

1.  <span data-ttu-id="668ea-139">Для резервного копирования базы данных восстановления и оборудования на сервере A используйте SQL Server Management Studio и задачу с именем **резервное копирование..**..</span><span class="sxs-lookup"><span data-stu-id="668ea-139">To back up the Recovery and Hardware database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="668ea-140">По умолчанию имя базы данных **MBAM восстановлением и базой данных оборудования**.</span><span class="sxs-lookup"><span data-stu-id="668ea-140">By default, the database name is **MBAM Recovery and Hardware Database**.</span></span>

2.  <span data-ttu-id="668ea-141">Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:</span><span class="sxs-lookup"><span data-stu-id="668ea-141">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="668ea-142">Измените базу данных MBAM восстановления и оборудования, чтобы использовать режим полного восстановления.</span><span class="sxs-lookup"><span data-stu-id="668ea-142">Modify the MBAM Recovery and Hardware Database to use the full recovery mode.</span></span>

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    <span data-ttu-id="668ea-143">Создавайте резервные копии MBAM и данные в базе данных оборудования и MBAM восстановления для логических устройств архивации.</span><span class="sxs-lookup"><span data-stu-id="668ea-143">Create MBAM Recovery and Hardware Database Data and MBAM Recovery logical backup devices.</span></span>

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    <span data-ttu-id="668ea-144">Создавайте резервные копии всей базы данных восстановления MBAM и оборудования.</span><span class="sxs-lookup"><span data-stu-id="668ea-144">Back up the full MBAM Recovery and Hardware database.</span></span>

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

    **<span data-ttu-id="668ea-145">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-145">Note</span></span>**  
    <span data-ttu-id="668ea-146">Замените значения из предыдущего примера на те, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-146">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="668ea-147">$PASSWORD $-введите пароль, который будет использоваться для шифрования файла закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="668ea-147">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="668ea-148">Выполните SQL-файл с помощью SQL Server PowerShell и команды, аналогичные приведенным ниже.</span><span class="sxs-lookup"><span data-stu-id="668ea-148">Execute the SQL file by using SQL Server PowerShell and a command that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="668ea-149">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-149">Note</span></span>**  
    <span data-ttu-id="668ea-150">Замените в предыдущем примере значение, совпадающее с вашей средой.</span><span class="sxs-lookup"><span data-stu-id="668ea-150">Replace the value in the previous example with those that match your environment:</span></span>

    -   <span data-ttu-id="668ea-151">$SERVERNAME $ \ \ $SQLINSTANCENAME $ — введите имя сервера и экземпляр, из которого вы хотите создать резервную копию базы данных восстановления и оборудования.</span><span class="sxs-lookup"><span data-stu-id="668ea-151">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance from which you back up the Recovery and Hardware database.</span></span>



**<span data-ttu-id="668ea-152">Чтобы переместить базу данных и сертификат с сервера A в B</span><span class="sxs-lookup"><span data-stu-id="668ea-152">To move the Database and Certificate from Server A to B</span></span>**

1.  <span data-ttu-id="668ea-153">Перемещайте данные восстановления MBAM и базы данных оборудования. bak с сервера A на сервер B с помощью проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="668ea-153">Move the MBAM Recovery and Hardware database data.bak from Server A to Server B by using Windows Explorer.</span></span>

2.  <span data-ttu-id="668ea-154">Чтобы переместить сертификат для зашифрованной базы данных, необходимо выполнить описанные ниже действия по автоматизации.</span><span class="sxs-lookup"><span data-stu-id="668ea-154">To move the certificate for the encrypted database, you will need to use the following automation steps.</span></span> <span data-ttu-id="668ea-155">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода команды, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="668ea-155">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="668ea-156">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-156">Note</span></span>**  
    <span data-ttu-id="668ea-157">Замените значение из предыдущего примера на те, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-157">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="668ea-158">$SERVERNAME $-введите имя сервера, на который будут скопированы файлы.</span><span class="sxs-lookup"><span data-stu-id="668ea-158">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="668ea-159">$DESTINATIONSHARE $-введите имя общего доступа и путь к файлам, куда они будут скопированы.</span><span class="sxs-lookup"><span data-stu-id="668ea-159">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="668ea-160">Восстановление базы данных на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-160">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="668ea-161">Восстановите базу данных восстановления и оборудования на сервере B с помощью SQL Server Management Studio и задачи с именем **Database Restore**.</span><span class="sxs-lookup"><span data-stu-id="668ea-161">Restore the Recovery and Hardware database on Server B by using the SQL Server Management Studio and the Task named **Restore Database**.</span></span>

2.  <span data-ttu-id="668ea-162">После выполнения задачи выберите файл резервной копии базы данных, выбрав параметр **с устройства** , а затем с помощью команды **Добавить** выберите файл Data Recovery и MBAM Database **. bak** .</span><span class="sxs-lookup"><span data-stu-id="668ea-162">Once the task has been executed, choose the database backup file by selecting the **From Device** option, and then use the **Add** command to choose the MBAM Recovery and Hardware database **Data.bak** file.</span></span>

3.  <span data-ttu-id="668ea-163">Нажмите кнопку **ОК** , чтобы завершить процесс восстановления.</span><span class="sxs-lookup"><span data-stu-id="668ea-163">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="668ea-164">Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:</span><span class="sxs-lookup"><span data-stu-id="668ea-164">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    <span data-ttu-id="668ea-165">Удалите сертификат, созданный программой установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="668ea-165">Drop the certificate created by MBAM Setup.</span></span>

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    <span data-ttu-id="668ea-166">Добавление сертификата</span><span class="sxs-lookup"><span data-stu-id="668ea-166">Add certificate</span></span>

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

    <span data-ttu-id="668ea-167">Восстановите данные базы данных MBAM восстановления и оборудования, а также файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="668ea-167">Restore the MBAM Recovery and Hardware database data and the log files.</span></span>

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **<span data-ttu-id="668ea-168">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-168">Note</span></span>**  
    <span data-ttu-id="668ea-169">Замените значения из предыдущего примера на те, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-169">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="668ea-170">$PASSWORD $-введите пароль, который вы использовали для шифрования файла закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="668ea-170">$PASSWORD$ - Enter the password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="668ea-171">С помощью Windows PowerShell введите командную строку, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="668ea-171">Use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="668ea-172">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-172">Note</span></span>**  
    <span data-ttu-id="668ea-173">Замените значение из примера receding на те, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-173">Replace the value from the receding example with those that match your environment:</span></span>

    -   <span data-ttu-id="668ea-174">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, на который будет восстановлена база данных восстановления и оборудования.</span><span class="sxs-lookup"><span data-stu-id="668ea-174">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance to which the Recovery and Hardware Database will be restored.</span></span>



**<span data-ttu-id="668ea-175">Настройка доступа к базе данных на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-175">Configure the access to the Database on Server B</span></span>**

1.  <span data-ttu-id="668ea-176">На сервере B с помощью оснастки "Локальные пользователи и группы" в диспетчере серверов можно добавить учетные записи компьютеров с каждого сервера, на котором запущена функция администрирования и мониторинга MBAM, в локальную группу с именем **MBAM и доступом к базе данных оборудования**.</span><span class="sxs-lookup"><span data-stu-id="668ea-176">On Server B, use the Local user and Groups snap-in from Server Manager, to add the computer accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="668ea-177">Для автоматизации этой процедуры можно использовать Windows PowerShell на сервере B для ввода команды, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="668ea-177">To automate this procedure, you can use Windows PowerShell on Server B to enter a command that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="668ea-178">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-178">Note</span></span>**  
    <span data-ttu-id="668ea-179">Замените значения из предыдущего примера соответствующими значениями для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="668ea-179">Replace the values from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="668ea-180">$DOMAIN $ \ \ $SERVERNAME $ $-введите имя домена и имя компьютера сервера MBAM администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="668ea-180">$DOMAIN$\\$SERVERNAME$$ - Enter the domain name and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="668ea-181">За именем сервера должен следовать a **$** , например, MyDomain\\MyServerName1 $.</span><span class="sxs-lookup"><span data-stu-id="668ea-181">The server name must be followed by a **$**, for example, MyDomain\\MyServerName1$.</span></span>



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="668ea-182">Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-182">To update the Database Connection data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="668ea-183">На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для обновления данных строки подключения для указанных ниже приложений, размещенных на веб-сайте администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="668ea-183">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="668ea-184">Служба администрирования MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-184">MBAM Administration Service</span></span>

   -   <span data-ttu-id="668ea-185">MBAM восстановления и обслуживания оборудования</span><span class="sxs-lookup"><span data-stu-id="668ea-185">MBAM Recovery And Hardware Service</span></span>

2. <span data-ttu-id="668ea-186">Выберите каждое приложение и используйте функцию **редактора конфигурации** , расположенную в разделе **Управление** **представлением функций**.</span><span class="sxs-lookup"><span data-stu-id="668ea-186">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="668ea-187">В элементе управления списком разделов выберите параметр **configurationStrings** .</span><span class="sxs-lookup"><span data-stu-id="668ea-187">Select the **configurationStrings** option from the Section list control.</span></span>

4. <span data-ttu-id="668ea-188">Выберите строку с именем **(коллекцией)** и откройте **Редактор коллекций** , нажав кнопку в правой части строки.</span><span class="sxs-lookup"><span data-stu-id="668ea-188">Choose the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="668ea-189">В **редакторе коллекции**выберите строку с именем **KeyRecoveryConnectionString** , если вы обновили конфигурацию для приложения "MBAMAdministrationService", или выберите строку с именем <strong> Microsoft. MBAM. RecoveryAndHardwareDataStore. </strong> ConnectionString при обновлении конфигурации для "MBAMRecoveryAndHardwareService".</span><span class="sxs-lookup"><span data-stu-id="668ea-189">In the **Collection Editor**, choose the row named **KeyRecoveryConnectionString** when you updated the configuration for the ‘MBAMAdministrationService’ application, or choose the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString, when updating the configuration for the ‘MBAMRecoveryAndHardwareService’.</span></span>

6. <span data-ttu-id="668ea-190">Обновите **источник данных =** значение для свойства **configurationStrings** , чтобы вывести имя сервера и экземпляр, на который была перемещена база данных восстановления и оборудования.</span><span class="sxs-lookup"><span data-stu-id="668ea-190">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance where the Recovery and Hardware Database was moved to.</span></span> <span data-ttu-id="668ea-191">Например, $SERVERNAME $ \ \ $SQLINSTANCENAME $.</span><span class="sxs-lookup"><span data-stu-id="668ea-191">For example, $SERVERNAME$\\$SQLINSTANCENAME$.</span></span>

7. <span data-ttu-id="668ea-192">Для автоматизации этой процедуры вы можете использовать команду Windows PowerShell на каждом сервере администрирования и наблюдения, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="668ea-192">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="668ea-193">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-193">Note</span></span>**  
   <span data-ttu-id="668ea-194">Замените значение из предыдущего примера на те, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-194">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="668ea-195">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, где находится база данных восстановления и оборудования.</span><span class="sxs-lookup"><span data-stu-id="668ea-195">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery and Hardware database is.</span></span>



**<span data-ttu-id="668ea-196">Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-196">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="668ea-197">На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для запуска веб-сайта MBAM, который называется **администрированием и мониторингом Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="668ea-197">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="668ea-198">Для автоматизации этой процедуры можно использовать команду Windows PowerShell, похожую на одну из приведенных ниже команд.</span><span class="sxs-lookup"><span data-stu-id="668ea-198">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="668ea-199">Перемещение функции базы данных состояния соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="668ea-199">To move the Compliance Status Database feature</span></span>


<span data-ttu-id="668ea-200">Если вы решили переместить функцию базы данных состояния соответствия MBAM с одного компьютера на другой, например с сервера A на сервер B, необходимо выполнить описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="668ea-200">If you choose to move the MBAM Compliance Status Database feature from one computer to another, such as from Server A to Server B, you should use the following procedure:</span></span>

1.  <span data-ttu-id="668ea-201">Остановка всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-201">Stop all instances of the MBAM Administration and Monitoring website</span></span>

2.  <span data-ttu-id="668ea-202">Запуск настройки MBAM на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-202">Run MBAM setup on Server B</span></span>

3.  <span data-ttu-id="668ea-203">Резервное копирование базы данных на сервере A</span><span class="sxs-lookup"><span data-stu-id="668ea-203">Backup the Database on Server A</span></span>

4.  <span data-ttu-id="668ea-204">Перемещение базы данных с сервера A в B</span><span class="sxs-lookup"><span data-stu-id="668ea-204">Move the Database from Server A to B</span></span>

5.  <span data-ttu-id="668ea-205">Восстановление базы данных на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-205">Restore the Database on Server B</span></span>

6.  <span data-ttu-id="668ea-206">Настройка доступа к базе данных на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-206">Configure Access to the Database on Server B</span></span>

7.  <span data-ttu-id="668ea-207">Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-207">Update database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="668ea-208">Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-208">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="668ea-209">Отключение всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-209">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="668ea-210">На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта MBAM, который называется **администрированием и мониторингом Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="668ea-210">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="668ea-211">Для автоматизации этой процедуры можно использовать команду Windows PowerShell, похожую на одну из приведенных ниже команд.</span><span class="sxs-lookup"><span data-stu-id="668ea-211">To automate this procedure, you can use a command that is similar to the following one,by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="668ea-212">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-212">Note</span></span>**  
    <span data-ttu-id="668ea-213">Для выполнения этой команды необходимо добавить модуль IIS для PowerShell в текущий экземпляр PowerShell.</span><span class="sxs-lookup"><span data-stu-id="668ea-213">To execute this command, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="668ea-214">Кроме того, необходимо обновить политику выполнения PowerShell, чтобы обеспечить выполнение сценариев.</span><span class="sxs-lookup"><span data-stu-id="668ea-214">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="668ea-215">Запуск настройки MBAM на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-215">To run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="668ea-216">Запустите настройку MBAM на сервере B и выберите компонент базы данных состояния соответствия требованиям для установки.</span><span class="sxs-lookup"><span data-stu-id="668ea-216">Run MBAM Setup on Server B and select the Compliance Status Database feature for installation.</span></span>

2.  <span data-ttu-id="668ea-217">Для автоматизации этой процедуры можно использовать команду Windows PowerShell, похожую на одну из приведенных ниже команд.</span><span class="sxs-lookup"><span data-stu-id="668ea-217">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **<span data-ttu-id="668ea-218">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-218">Note</span></span>**  
    <span data-ttu-id="668ea-219">Замените значения из предыдущего примера на те, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-219">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="668ea-220">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, в который будет перемещена база данных состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="668ea-220">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be moved to.</span></span>

    -   <span data-ttu-id="668ea-221">$DOMAIN $ \ \ $SERVERNAME $-введите имена доменов и имена серверов для каждого приложения MBAM и сервера мониторинга, которые будут обращаться к базе данных о состоянии соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="668ea-221">$DOMAIN$\\$SERVERNAME$ - Enter the domain names and server names of each MBAM Application and Monitoring Server that will contact the Compliance Status Database.</span></span> <span data-ttu-id="668ea-222">Если вы используете несколько доменных имен и имен серверов, для разделения каждого из них в списке используйте точку с запятой.</span><span class="sxs-lookup"><span data-stu-id="668ea-222">If there are multiple domain names and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="668ea-223">Например, $DOMAIN _сервера $; $DOMAIN \ \ $SERVERNAME $ $.</span><span class="sxs-lookup"><span data-stu-id="668ea-223">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="668ea-224">За именем каждого сервера должен следовать a, **$** как показано в примере.</span><span class="sxs-lookup"><span data-stu-id="668ea-224">Each server name must be followed by a **$** as shown in the example.</span></span> <span data-ttu-id="668ea-225">Например, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="668ea-225">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>

    -   <span data-ttu-id="668ea-226">$DOMAIN $ \ \ $USERNAME $-введите домен и имя пользователя, которые будут использоваться функцией проверки соответствия и аудита для подключения к базе данных состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="668ea-226">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="668ea-227">Создание резервной копии базы данных соответствия на сервере A</span><span class="sxs-lookup"><span data-stu-id="668ea-227">To back up the Compliance Database on Server A</span></span>**

1.  <span data-ttu-id="668ea-228">Чтобы создать резервную копию базы данных соответствия на сервере A, используйте SQL Server Management Studio и задачу с именем **резервное копирование..**..</span><span class="sxs-lookup"><span data-stu-id="668ea-228">To back up the Compliance Database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="668ea-229">По умолчанию в качестве имени базы данных используется **база данных состояния соответствия MBAM**.</span><span class="sxs-lookup"><span data-stu-id="668ea-229">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="668ea-230">Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:</span><span class="sxs-lookup"><span data-stu-id="668ea-230">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

3.  <span data-ttu-id="668ea-231">Запустите SQL-файл с помощью команды, подобной приведенной ниже, используя SQL Server PowerShell.</span><span class="sxs-lookup"><span data-stu-id="668ea-231">Run the SQL file with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="668ea-232">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-232">Note</span></span>**  
    <span data-ttu-id="668ea-233">Замените значение из предыдущего примера на те, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-233">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="668ea-234">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, из которого будет создаваться резервная копия базы данных состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="668ea-234">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and the instance from where the Compliance Status database will be backed up.</span></span>



**<span data-ttu-id="668ea-235">Чтобы переместить базу данных с сервера A в B</span><span class="sxs-lookup"><span data-stu-id="668ea-235">To move the Database from Server A to B</span></span>**

1.  <span data-ttu-id="668ea-236">Переместите указанные ниже файлы с сервера A на сервер B с помощью проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="668ea-236">Move the following files from Server A to Server B, by using Windows Explorer:</span></span>

    -   <span data-ttu-id="668ea-237">Данные базы данных о состоянии соответствия MBAM. bak</span><span class="sxs-lookup"><span data-stu-id="668ea-237">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="668ea-238">Для автоматизации этой процедуры можно использовать команду, подобную описанной ниже, с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="668ea-238">To automate this procedure, you can use a command that is similar to the following using Windows PowerShell:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="668ea-239">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-239">Note</span></span>**  
    <span data-ttu-id="668ea-240">Замените значение из предыдущего примера на те, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-240">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="668ea-241">$SERVERNAME $ — введите имя сервера, куда будут скопированы файлы.</span><span class="sxs-lookup"><span data-stu-id="668ea-241">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="668ea-242">$DESTINATIONSHARE $ — введите имя и путь к папке, куда будут скопированы файлы.</span><span class="sxs-lookup"><span data-stu-id="668ea-242">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="668ea-243">Восстановление базы данных на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-243">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="668ea-244">Восстановите базу данных состояния соответствия на сервере B с помощью SQL Server Management Studio и задачи **RESTORE DATABASE.**...</span><span class="sxs-lookup"><span data-stu-id="668ea-244">Restore the Compliance Status database on Server B by using SQL Server Management Studio and the Task named **Restore Database…**.</span></span>

2.  <span data-ttu-id="668ea-245">После выполнения задачи выберите файл резервной копии базы данных, выбрав параметр с устройства, а затем с помощью команды Добавить выберите файл Data MBAM. bak (состояние соответствия требованиям к БД).</span><span class="sxs-lookup"><span data-stu-id="668ea-245">Once the task is executed, select the database backup file, by selecting the From Device option, and then use the Add command to choose the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="668ea-246">Нажмите кнопку ОК, чтобы завершить процесс восстановления.</span><span class="sxs-lookup"><span data-stu-id="668ea-246">Click OK to complete the restoration process.</span></span>

3.  <span data-ttu-id="668ea-247">Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:</span><span class="sxs-lookup"><span data-stu-id="668ea-247">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="668ea-248">Запустите SQL-файл с помощью команды, подобной приведенной ниже, используя SQL Server PowerShell.</span><span class="sxs-lookup"><span data-stu-id="668ea-248">Run the SQL File with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="668ea-249">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-249">Note</span></span>**  
    <span data-ttu-id="668ea-250">Замените значение из предыдущего примера на те, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-250">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="668ea-251">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, на который будет восстанавливаться база данных состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="668ea-251">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be restored to.</span></span>



**<span data-ttu-id="668ea-252">Настройка доступа к базе данных на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-252">To configure the Access to the Database on Server B</span></span>**

1.  <span data-ttu-id="668ea-253">На сервере B с помощью оснастки "локальный пользователь и группы" в диспетчере серверов добавьте учетные записи компьютеров с каждого сервера, на котором запускается функция администрирования и мониторинга MBAM, в локальную группу с именем **MBAM соответствие требованиям Access**.</span><span class="sxs-lookup"><span data-stu-id="668ea-253">On Server B use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="668ea-254">Для автоматизации этой процедуры можно использовать команду Windows PowerShell на сервере B, которая похожа на указанную ниже.</span><span class="sxs-lookup"><span data-stu-id="668ea-254">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on Server B:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="668ea-255">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-255">Note</span></span>**  
    <span data-ttu-id="668ea-256">Замените значение из предыдущего примера соответствующими значениями для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="668ea-256">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="668ea-257">$DOMAIN $ \ \ $SERVERNAME $ $-введите домен и имя MBAM сервера администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="668ea-257">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="668ea-258">За именем сервера должно следовать a **$** . Например, MyDomain\\MyServerName1 $.</span><span class="sxs-lookup"><span data-stu-id="668ea-258">The server name must be followed by a **$**.For example, MyDomain\\MyServerName1$.</span></span>

    -   <span data-ttu-id="668ea-259">$DOMAIN $ \ \ $REPORTSUSERNAME $-введите имя учетной записи пользователя, которое использовалось для настройки источника данных для отчетов о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="668ea-259">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**<span data-ttu-id="668ea-260">Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-260">To update the database connection data on MBAM Administration and Monitoring servers</span></span>**

1.  <span data-ttu-id="668ea-261">На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для обновления данных строки подключения для указанных ниже приложений, размещенных на веб-сайте администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="668ea-261">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following Applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="668ea-262">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="668ea-262">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="668ea-263">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="668ea-263">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="668ea-264">Выберите каждое приложение и используйте функцию **редактора конфигурации** , расположенную в разделе **Управление** **представлением функций**.</span><span class="sxs-lookup"><span data-stu-id="668ea-264">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="668ea-265">В элементе управления списком разделов выберите параметр **configurationStrings** .</span><span class="sxs-lookup"><span data-stu-id="668ea-265">Select the **configurationStrings** option from the Section list control.</span></span>

4.  <span data-ttu-id="668ea-266">Выберите строку с именем **(коллекцией)** и откройте редактор коллекций, нажав кнопку в правой части строки.</span><span class="sxs-lookup"><span data-stu-id="668ea-266">Select the row named **(Collection)**, and open the Collection Editor by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="668ea-267">В **редакторе коллекции**выберите строку с именем **ComplianceStatusConnectionString**, при обновлении конфигурации для приложения MBAMAdministrationService или строку с именем **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString**, при обновлении конфигурации для MBAMComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="668ea-267">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString**, when you update the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString**, when you update the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="668ea-268">Обновите **источник данных =** значение для свойства **configurationStrings** , чтобы вывести имя сервера и имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="668ea-268">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance name.</span></span> <span data-ttu-id="668ea-269">Например, $SERVERNAME $ \ \ $SQLINSTANCENAME, на который была перемещена база данных восстановления и оборудования.</span><span class="sxs-lookup"><span data-stu-id="668ea-269">For example, $SERVERNAME$\\$SQLINSTANCENAME, to which the Recovery and Hardware Database was moved.</span></span>

7.  <span data-ttu-id="668ea-270">Для автоматизации этой процедуры вы можете использовать Windows PowerShell для ввода команды, сходной с одной из следующих на каждом сервере администрирования и наблюдения.</span><span class="sxs-lookup"><span data-stu-id="668ea-270">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="668ea-271">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-271">Note</span></span>**  
    <span data-ttu-id="668ea-272">Замените значение из предыдущего примера на те, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-272">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="668ea-273">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и имя экземпляра, где находится база данных восстановления и оборудования.</span><span class="sxs-lookup"><span data-stu-id="668ea-273">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance name where the Recovery and Hardware Database is located.</span></span>



**<span data-ttu-id="668ea-274">Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-274">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="668ea-275">На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для запуска веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="668ea-275">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="668ea-276">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода команды, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="668ea-276">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    **<span data-ttu-id="668ea-277">PS C:\\ &gt; Start-website "Администрирование и мониторинг Microsoft BitLocker"</span><span class="sxs-lookup"><span data-stu-id="668ea-277">PS C:\\&gt; Start-Website “Microsoft BitLocker Administration and Monitoring”</span></span>**

## <span data-ttu-id="668ea-278">Перемещение отчетов о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="668ea-278">To moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="668ea-279">Если вы решили переместить отчеты о соответствии MBAM и аудиты между компьютерами (например, если вы перемещаете компонент с сервера A на сервер B), необходимо выполнить описанные ниже действия и шаги.</span><span class="sxs-lookup"><span data-stu-id="668ea-279">If you choose to move the MBAM Compliance and Audit Reports from one computer to another (specifically, if you move feature from Server A to Server B), you should use the following procedure and steps:</span></span>

1.  <span data-ttu-id="668ea-280">Запуск настройки MBAM на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-280">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="668ea-281">Настройка доступа к отчетам о соответствии и аудиту на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-281">Configure Access to the Compliance and Audit Reports on Server B</span></span>

3.  <span data-ttu-id="668ea-282">Остановка всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-282">Stop all instances of the MBAM Administration and Monitoring website</span></span>

4.  <span data-ttu-id="668ea-283">Обновление данных о соединениях на серверах администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-283">Update the reports connection data on MBAM Administration and Monitoring servers</span></span>

5.  <span data-ttu-id="668ea-284">Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-284">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="668ea-285">Запуск настройки MBAM на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-285">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="668ea-286">Запустите настройку MBAM на сервере B и выберите компонент "соответствие требованиям и аудит" для установки.</span><span class="sxs-lookup"><span data-stu-id="668ea-286">Run MBAM setup on Server B and only select the Compliance and Audit feature for installation.</span></span>

2.  <span data-ttu-id="668ea-287">Для автоматизации этой процедуры можно использовать команду Windows PowerShell, подобную приведенной ниже.</span><span class="sxs-lookup"><span data-stu-id="668ea-287">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **<span data-ttu-id="668ea-288">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-288">Note</span></span>**  
    <span data-ttu-id="668ea-289">Замените значения из предыдущего примера на те, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-289">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="668ea-290">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, в котором находится база данных состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="668ea-290">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database is located.</span></span>

    -   <span data-ttu-id="668ea-291">$DOMAIN $ \ \ $USERNAME $-введите доменное имя и имя пользователя, которые будут использоваться функцией "отчеты о соответствии и аудите" для подключения к базе данных состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="668ea-291">$DOMAIN$\\$USERNAME$ - Enter the domain name and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="668ea-292">$PASSWORD $ — введите пароль учетной записи пользователя, который будет использоваться для подключения к базе данных состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="668ea-292">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="668ea-293">Настройка доступа к отчетам о соответствии и аудиту на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-293">To configure the access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="668ea-294">На сервере B с помощью оснастки "Локальные пользователи и группы" в диспетчере серверов добавьте учетные записи пользователей, которые получат доступ к отчетам о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="668ea-294">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="668ea-295">Добавьте учетные записи пользователей в локальную группу с именем "Пользователи отчетов MBAM".</span><span class="sxs-lookup"><span data-stu-id="668ea-295">Add the user accounts to the local group named “MBAM Report Users”.</span></span>

2.  <span data-ttu-id="668ea-296">Для автоматизации этой процедуры можно использовать команду Windows PowerShell на сервере B, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="668ea-296">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell on Server B.</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="668ea-297">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-297">Note</span></span>**  
    <span data-ttu-id="668ea-298">Замените приведенное ниже значение из предыдущего примера на применимые значения для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="668ea-298">Replace the following value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="668ea-299">$DOMAIN $ \ \ $REPORTSUSERNAME $-введите имя учетной записи пользователя, которое использовалось для настройки источника данных для отчетов о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="668ea-299">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="668ea-300">Отключение всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-300">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="668ea-301">На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="668ea-301">On each of the servers that run the MBAM Administration and Monitoring Feature use the Internet Information Services (IIS) Manager console to Stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="668ea-302">Для автоматизации этой процедуры можно использовать команду Windows PowerShell, похожую на одну из приведенных ниже команд.</span><span class="sxs-lookup"><span data-stu-id="668ea-302">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="668ea-303">Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-303">To update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="668ea-304">На каждом из серверов, на которых выполняется функция администрирования и мониторинга MBAM, обновите URL-адрес отчетов о соответствиях с помощью консоли диспетчера служб IIS.</span><span class="sxs-lookup"><span data-stu-id="668ea-304">On each of the servers that run the MBAM Administration and Monitoring Feature, use the Internet Information Services (IIS) Manager console to update the Compliance Reports URL.</span></span>

2. <span data-ttu-id="668ea-305">Выберите веб-сайт **администрирования и наблюдения Microsoft BitLocker** и используйте средство **редактирования конфигурации** , которое можно найти в разделе " **Управление** " в **представлении "возможности**".</span><span class="sxs-lookup"><span data-stu-id="668ea-305">Select the **Microsoft BitLocker Administration and Monitoring** website and use the **Configuration Editor** feature which can be found under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="668ea-306">В элементе управления списком разделов выберите параметр **appSettings** .</span><span class="sxs-lookup"><span data-stu-id="668ea-306">Select the **appSettings** option from the Section list control.</span></span>

4. <span data-ttu-id="668ea-307">В этой статье выберите строку с именем **(коллекцией)** и откройте **Редактор коллекции** , нажав кнопку в правой части строки.</span><span class="sxs-lookup"><span data-stu-id="668ea-307">From here, select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="668ea-308">В **редакторе коллекций**выберите строку с именем "Microsoft. MBAM. Reports. URL".</span><span class="sxs-lookup"><span data-stu-id="668ea-308">In the **Collection Editor**, select the row named “Microsoft.Mbam.Reports.Url”.</span></span>

6. <span data-ttu-id="668ea-309">Обновите значение Microsoft. MBAM. Reports. URL, чтобы оно отражало имя сервера для сервера B. Если функция проверки соответствия и аудита была установлена на именованном экземпляре служб SQL Reporting Services, убедитесь, что вы добавите или обновите имя экземпляра в URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="668ea-309">Update the value for Microsoft.Mbam.Reports.Url to reflect the server name for Server B. If the Compliance and Audit reports feature was installed on a named SQL Reporting Services instance, make sure that you add or update the name of the instance to the URL.</span></span> <span data-ttu-id="668ea-310">Например, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....</span><span class="sxs-lookup"><span data-stu-id="668ea-310">For example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....</span></span>

7. <span data-ttu-id="668ea-311">Для автоматизации этой процедуры вы можете использовать Windows PowerShell для ввода команды, сходной с одной из следующих на каждом сервере администрирования и наблюдения.</span><span class="sxs-lookup"><span data-stu-id="668ea-311">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **<span data-ttu-id="668ea-312">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-312">Note</span></span>**  
   <span data-ttu-id="668ea-313">Замените значение из предыдущего примера на те, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-313">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="668ea-314">$SERVERNAME $-введите имя сервера, на котором установлены отчеты о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="668ea-314">$SERVERNAME$ - Enter the name of the server to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="668ea-315">$SRSINSTANCENAME $ — введите имя экземпляра служб SQL Reporting Services, для которого установлены отчеты о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="668ea-315">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="668ea-316">Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="668ea-316">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="668ea-317">На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для запуска веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="668ea-317">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="668ea-318">Для автоматизации этой процедуры можно использовать команду Windows PowerShell, похожую на одну из приведенных ниже команд.</span><span class="sxs-lookup"><span data-stu-id="668ea-318">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="668ea-319">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-319">Note</span></span>**  
    <span data-ttu-id="668ea-320">Для выполнения этой команды необходимо добавить модуль IIS для PowerShell в текущий экземпляр PowerShell.</span><span class="sxs-lookup"><span data-stu-id="668ea-320">To execute this command, the IIS Module for PowerShell must be added to the current instance of PowerShell.</span></span> <span data-ttu-id="668ea-321">Кроме того, необходимо обновить политику выполнения PowerShell, чтобы разрешить выполнение сценариев.</span><span class="sxs-lookup"><span data-stu-id="668ea-321">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



## <span data-ttu-id="668ea-322">Перемещение компонента администрирования и наблюдения</span><span class="sxs-lookup"><span data-stu-id="668ea-322">To move the Administration and Monitoring feature</span></span>


<span data-ttu-id="668ea-323">Если вы решили переместить функцию отчетов администрирования и мониторинга MBAM с одного компьютера на другой (если вы перемещаете компонент с сервера A на сервер B), необходимо выполнить описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="668ea-323">If you choose to move the MBAM Administration and Monitoring Reports feature from one computer to another, (if you move feature from Server A to Server B), you should use the following procedure.</span></span> <span data-ttu-id="668ea-324">Процесс включает следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="668ea-324">The process includes the following steps:</span></span>

1.  <span data-ttu-id="668ea-325">Запуск настройки MBAM на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-325">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="668ea-326">Настройка доступа к базе данных на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-326">Configure Access to the Database on Server B</span></span>

**<span data-ttu-id="668ea-327">Запуск настройки MBAM на сервере B</span><span class="sxs-lookup"><span data-stu-id="668ea-327">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="668ea-328">Запустите настройку MBAM на сервере B и выберите компонент администрирования для установки.</span><span class="sxs-lookup"><span data-stu-id="668ea-328">Run MBAM setup on Server B and only select the Administration feature for installation.</span></span>

2.  <span data-ttu-id="668ea-329">Для автоматизации этой процедуры можно использовать команду Windows PowerShell, похожую на одну из приведенных ниже команд.</span><span class="sxs-lookup"><span data-stu-id="668ea-329">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **<span data-ttu-id="668ea-330">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-330">Note</span></span>**  
    <span data-ttu-id="668ea-331">Замените значения из предыдущего примера на те, которые соответствуют вашей среде:</span><span class="sxs-lookup"><span data-stu-id="668ea-331">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="668ea-332">$SERVERNAME $ \ \ $SQLINSTANCENAME $ — для параметра COMPLIDB \ _SQLINSTANCE введите имя сервера и экземпляр, в котором находится база данных состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="668ea-332">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, input the server name and instance where the Compliance Status Database is located.</span></span> <span data-ttu-id="668ea-333">Для параметра RECOVERYANDHWDB \ _SQLINSTANCE введите имя сервера и экземпляр, где находится база данных восстановления и оборудования.</span><span class="sxs-lookup"><span data-stu-id="668ea-333">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, input the server name and instance where the Recovery and Hardware Database is located.</span></span>

    -   <span data-ttu-id="668ea-334">$DOMAIN $ \ \ $USERNAME $-введите домен и имя пользователя, которые будут использоваться функцией проверки соответствия и аудита для подключения к базе данных состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="668ea-334">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="668ea-335">$ REPORTSSERVERURL $ — введите URL-адрес домашнего расположения веб-сайта службы отчетов SQL.</span><span class="sxs-lookup"><span data-stu-id="668ea-335">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="668ea-336">Если отчеты были установлены в экземпляре SRS по умолчанию, формат URL-адреса будет отформатирован как "http://$SERVERNAME $/ReportServer".</span><span class="sxs-lookup"><span data-stu-id="668ea-336">If the reports were installed to a default SRS instance the URL format will formatted “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="668ea-337">Если отчеты были установлены в экземпляре SRS по умолчанию, формат URL-адреса будет отформатирован в формате "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $".</span><span class="sxs-lookup"><span data-stu-id="668ea-337">If the reports were installed to a default SRS instance, the URL format will be formatted to “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>



**<span data-ttu-id="668ea-338">Настройка доступа к базам данных</span><span class="sxs-lookup"><span data-stu-id="668ea-338">To configure the Access to the Databases</span></span>**

1.  <span data-ttu-id="668ea-339">На сервере или серверах, на которых восстановлено и оборудование; и базы данных проверки соответствия и аудита развертываются с помощью оснастки "Локальные пользователи и группы" в диспетчере серверов, чтобы добавить учетные записи компьютеров с каждого сервера, на котором запущена функция администрирования и мониторинга MBAM, в локальные группы с именем "MBAM Recovery и DB (сервер DB)" (восстановление и доступ к базам данных оборудования) и "MBAM соответствие требованиям к БД"</span><span class="sxs-lookup"><span data-stu-id="668ea-339">On server or servers where the Recovery and Hardware, and Compliance and Audit databases are deployed, use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that run the MBAM Administration and Monitoring feature to the Local Groups named “MBAM Recovery and Hardware DB Access” (Recovery and Hardware DB Server) and “MBAM Compliance Status DB Access” (Compliance and Audit DB Server).</span></span>

2.  <span data-ttu-id="668ea-340">Для автоматизации этой процедуры можно использовать командную команду Windows PowerShell на сервере, на котором развернуты базы данных соответствия и аудита.</span><span class="sxs-lookup"><span data-stu-id="668ea-340">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on the server where the Compliance and Audit databases were deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  <span data-ttu-id="668ea-341">На сервере, на котором развернуты базы данных восстановления и оборудования, выполните команду, подобную следующей, с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="668ea-341">On the server where the Recovery and Hardware databases were deployed, run a command that is similar to the following one, by using Windows PowerShell.</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="668ea-342">Примечание.</span><span class="sxs-lookup"><span data-stu-id="668ea-342">Note</span></span>**  
    <span data-ttu-id="668ea-343">Замените значение из предыдущего примера соответствующими значениями для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="668ea-343">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="668ea-344">$DOMAIN $ \ \ $SERVERNAME $ $-введите домен и имя MBAM сервера администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="668ea-344">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="668ea-345">За именем сервера должно следовать a **$** .</span><span class="sxs-lookup"><span data-stu-id="668ea-345">The server name must be followed by a **$**.</span></span> <span data-ttu-id="668ea-346">Например, MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="668ea-346">For example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="668ea-347">$DOMAIN $ \ \ $REPORTSUSERNAME $ — введите имя учетной записи пользователя, которое использовалось для настройки источника данных для отчетов о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="668ea-347">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="668ea-348">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="668ea-348">Related topics</span></span>


[<span data-ttu-id="668ea-349">Администрирование компонентов MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="668ea-349">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)









