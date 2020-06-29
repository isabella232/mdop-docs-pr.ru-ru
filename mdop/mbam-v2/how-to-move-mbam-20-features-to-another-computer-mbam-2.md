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
# <span data-ttu-id="4eabf-103">Перемещение компонентов MBAM 2.0 на другой компьютер</span><span class="sxs-lookup"><span data-stu-id="4eabf-103">How to Move MBAM 2.0 Features to Another Computer</span></span>


<span data-ttu-id="4eabf-104">В этой статье описаны действия, которые необходимо выполнить для перемещения одной или нескольких функций администрирования и мониторинга Microsoft BitLocker (MBAM) на другой компьютер.</span><span class="sxs-lookup"><span data-stu-id="4eabf-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="4eabf-105">При перемещении нескольких функций администрирования и мониторинга Microsoft BitLocker следует переместить их в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="4eabf-105">When moving more than one Microsoft BitLocker Administration and Monitoring feature, you should move them in the following order:</span></span>

1.  <span data-ttu-id="4eabf-106">База данных восстановления</span><span class="sxs-lookup"><span data-stu-id="4eabf-106">Recovery Database</span></span>

2.  <span data-ttu-id="4eabf-107">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="4eabf-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="4eabf-108">Отчеты о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="4eabf-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="4eabf-109">Администрирование и мониторинг</span><span class="sxs-lookup"><span data-stu-id="4eabf-109">Administration and Monitoring</span></span>

## <span data-ttu-id="4eabf-110">Перемещение базы данных восстановления</span><span class="sxs-lookup"><span data-stu-id="4eabf-110">Moving the Recovery Database</span></span>


<span data-ttu-id="4eabf-111">Чтобы переместить базу данных восстановления с одного компьютера на другой (например, с сервера A на сервер B), выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4eabf-111">To move the Recovery Database from one computer to another (for example, from Server A to Server B), use the following procedure.</span></span>

1.  <span data-ttu-id="4eabf-112">Остановите все экземпляры веб-сайта администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="4eabf-112">Stop all instances of the Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="4eabf-113">Запустите настройку MBAM на сервере B.</span><span class="sxs-lookup"><span data-stu-id="4eabf-113">Run MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="4eabf-114">Создание резервной копии базы данных восстановления MBAM на сервере A.</span><span class="sxs-lookup"><span data-stu-id="4eabf-114">Back up the MBAM Recovery Database on Server A.</span></span>

4.  <span data-ttu-id="4eabf-115">Перенесите базу данных восстановления MBAM с сервера A в B.</span><span class="sxs-lookup"><span data-stu-id="4eabf-115">Move the MBAM Recovery Database from Server A to B.</span></span>

5.  <span data-ttu-id="4eabf-116">Восстановите базу данных восстановления MBAM на сервере B.</span><span class="sxs-lookup"><span data-stu-id="4eabf-116">Restore the MBAM Recovery Database on Server B.</span></span>

6.  <span data-ttu-id="4eabf-117">Настройка доступа к базе данных восстановления MBAM на сервере B.</span><span class="sxs-lookup"><span data-stu-id="4eabf-117">Configure access to the MBAM Recovery Database on Server B.</span></span>

7.  <span data-ttu-id="4eabf-118">Обновите данные подключения к базе данных на серверах администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="4eabf-118">Update the database connection data on MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="4eabf-119">Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="4eabf-119">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="4eabf-120">Остановка всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="4eabf-120">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="4eabf-121">На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта MBAM, который называется **администрированием и мониторингом Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-121">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="4eabf-122">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, сходной с:</span><span class="sxs-lookup"><span data-stu-id="4eabf-122">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="4eabf-123">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-123">Note</span></span>**  
    <span data-ttu-id="4eabf-124">Чтобы выполнить эту командную строку PowerShell, необходимо добавить модуль IIS для PowerShell в текущий экземпляр PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4eabf-124">To run this PowerShell command line, the IIS Module for PowerShell must be added to current instance of PowerShell.</span></span> <span data-ttu-id="4eabf-125">Кроме того, необходимо обновить политику выполнения PowerShell, чтобы разрешить выполнение сценариев.</span><span class="sxs-lookup"><span data-stu-id="4eabf-125">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



**<span data-ttu-id="4eabf-126">Запуск настройки MBAM на сервере B</span><span class="sxs-lookup"><span data-stu-id="4eabf-126">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="4eabf-127">Запустите настройку MBAM на сервере B и выберите только **базу данных восстановления** для установки.</span><span class="sxs-lookup"><span data-stu-id="4eabf-127">Run MBAM Setup on Server B and select only the **Recovery Database** for installation.</span></span>

2.  <span data-ttu-id="4eabf-128">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-128">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="4eabf-129">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-129">Note</span></span>**  
    <span data-ttu-id="4eabf-130">Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:</span><span class="sxs-lookup"><span data-stu-id="4eabf-130">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="4eabf-131">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, в который будет перемещена база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="4eabf-131">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be moved.</span></span>

    -   <span data-ttu-id="4eabf-132">$DOMAIN $ \ \ $SERVERNAME $-введите имена домена и сервера для каждого сервера администрирования и мониторинга MBAM, который будет обращаться к базе данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="4eabf-132">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Recovery Database.</span></span> <span data-ttu-id="4eabf-133">Используйте точку с запятой для разделения каждой пары домена и сервера в списке (например, $DOMAIN \ \ мой домен \; $DOMAIN \ \ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="4eabf-133">Use a semi-colon to separate each domain and server pairs in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="4eabf-134">За именем каждого сервера должен следовать символ "$", как показано в примере (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="4eabf-134">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="4eabf-135">$X $-введите **0** , если вы устанавливаете изолированную топологию MBAM или **1** при установке топологии Configuration Manager MBAM.</span><span class="sxs-lookup"><span data-stu-id="4eabf-135">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="4eabf-136">Создание резервной копии базы данных восстановления на сервере A</span><span class="sxs-lookup"><span data-stu-id="4eabf-136">Back Up the Recovery Database on Server A</span></span>**

1.  <span data-ttu-id="4eabf-137">Чтобы создать резервную копию базы данных восстановления на сервере A, используйте SQL Server Management Studio и задачу с именем "резервная копия".</span><span class="sxs-lookup"><span data-stu-id="4eabf-137">To back up the Recovery Database on Server A, use SQL Server Management Studio and the Task named Back Up.</span></span> <span data-ttu-id="4eabf-138">По умолчанию в качестве имени базы данных используется **база данных восстановления MBAM**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-138">By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="4eabf-139">Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:</span><span class="sxs-lookup"><span data-stu-id="4eabf-139">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="4eabf-140">Измените базу данных восстановления MBAM, чтобы использовать режим полного восстановления.</span><span class="sxs-lookup"><span data-stu-id="4eabf-140">Modify the MBAM Recovery Database to use the full recovery mode.</span></span>

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

    **<span data-ttu-id="4eabf-141">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-141">Note</span></span>**  
    <span data-ttu-id="4eabf-142">Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:</span><span class="sxs-lookup"><span data-stu-id="4eabf-142">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="4eabf-143">$PASSWORD $-введите пароль, который будет использоваться для шифрования файла закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="4eabf-143">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="4eabf-144">Запустите SQL-файл, используя SQL Server PowerShell, и командную строку, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="4eabf-144">Run the SQL File by using SQL Server PowerShell and a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="4eabf-145">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-145">Note</span></span>**  
    <span data-ttu-id="4eabf-146">Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:</span><span class="sxs-lookup"><span data-stu-id="4eabf-146">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="4eabf-147">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляра, из которого будет создаваться резервная копия базы данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="4eabf-147">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance from which the Recovery Database will be backed up.</span></span>



**<span data-ttu-id="4eabf-148">Перемещение базы данных восстановления и сертификата с сервера A на сервер B</span><span class="sxs-lookup"><span data-stu-id="4eabf-148">Move the Recovery Database and Certificate from Server A to Server B</span></span>**

1.  <span data-ttu-id="4eabf-149">Переместите следующий файл с сервера A на сервер B с помощью проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="4eabf-149">Move the following file from Server A to Server B by using Windows Explorer.</span></span>

    -   <span data-ttu-id="4eabf-150">Данные базы данных MBAM Recovery. bak</span><span class="sxs-lookup"><span data-stu-id="4eabf-150">MBAM Recovery Database data.bak</span></span>

2.  <span data-ttu-id="4eabf-151">Чтобы переместить сертификат для зашифрованной базы данных, выполните указанные ниже действия автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4eabf-151">To move the certificate for the encrypted database, use the following automation steps.</span></span> <span data-ttu-id="4eabf-152">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-152">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="4eabf-153">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-153">Note</span></span>**  
    <span data-ttu-id="4eabf-154">Замените приведенное ниже значение в приведенном выше примере, чтобы оно соответствовало вашей среде.</span><span class="sxs-lookup"><span data-stu-id="4eabf-154">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="4eabf-155">$SERVERNAME $-введите имя сервера, на который будут скопированы файлы.</span><span class="sxs-lookup"><span data-stu-id="4eabf-155">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="4eabf-156">$DESTINATIONSHARE $-введите имя общего доступа и путь к файлам, куда они будут скопированы.</span><span class="sxs-lookup"><span data-stu-id="4eabf-156">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="4eabf-157">Восстановление базы данных восстановления на сервере B</span><span class="sxs-lookup"><span data-stu-id="4eabf-157">Restore the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="4eabf-158">Восстановите базу данных восстановления на сервере B с помощью SQL Server Management Studio и задачи с именем **Database Restore**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-158">Restore the Recovery Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="4eabf-159">После завершения задачи выберите файл резервной копии базы данных, выбрав параметр **с устройства** , а затем с помощью команды **Добавить** выберите файл Data MBAM Database **. bak** .</span><span class="sxs-lookup"><span data-stu-id="4eabf-159">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Recovery database **Data.bak** file.</span></span>

3.  <span data-ttu-id="4eabf-160">Нажмите кнопку **ОК** , чтобы завершить процесс восстановления.</span><span class="sxs-lookup"><span data-stu-id="4eabf-160">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="4eabf-161">Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:</span><span class="sxs-lookup"><span data-stu-id="4eabf-161">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

    **<span data-ttu-id="4eabf-162">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-162">Note</span></span>**  
    <span data-ttu-id="4eabf-163">Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:</span><span class="sxs-lookup"><span data-stu-id="4eabf-163">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="4eabf-164">$PASSWORD $ — введите пароль, который вы использовали для шифрования файла закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="4eabf-164">$PASSWORD$ - Enter a password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="4eabf-165">С помощью Windows PowerShell можно вводить командную строку, подобную следующей:</span><span class="sxs-lookup"><span data-stu-id="4eabf-165">You can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="4eabf-166">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-166">Note</span></span>**  
    <span data-ttu-id="4eabf-167">Замените приведенное ниже значение в приведенном выше примере, чтобы оно соответствовало вашей среде.</span><span class="sxs-lookup"><span data-stu-id="4eabf-167">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="4eabf-168">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, в который будет восстановлена база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="4eabf-168">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be restored.</span></span>



**<span data-ttu-id="4eabf-169">Настройка доступа к базе данных восстановления на сервере B</span><span class="sxs-lookup"><span data-stu-id="4eabf-169">Configure Access to the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="4eabf-170">На сервере B с помощью оснастки "Локальные пользователи и группы" в диспетчере серверов добавьте учетные записи компьютеров с каждого сервера, на котором запущена функция администрирования и мониторинга MBAM, в локальную группу с именем **MBAM и доступом к базе данных оборудования**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-170">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="4eabf-171">Убедитесь, что в восстановленной базе данных **MBAM и доступ** к базе данных с помощью учетной записи SQL Server сопоставлен с именем входа **$MachineName $ \\MBAM и доступом к базе данных оборудования**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-171">Verify that the SQL login **MBAM Recovery and Hardware DB Access** on the restored database is mapped to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span> <span data-ttu-id="4eabf-172">Если оно не сопоставлено так, как описано, создайте другое имя для входа, совпадающее с участием в группах, и сопоставьте его имени для входа **$MachineName $ \\MBAM и получите доступ к базе данных оборудования**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-172">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span>

3.  <span data-ttu-id="4eabf-173">Для автоматизации этой процедуры можно использовать Windows PowerShell на сервере B для ввода командной строки, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-173">To automate this procedure, you can use Windows PowerShell on Server B to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="4eabf-174">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-174">Note</span></span>**  
    <span data-ttu-id="4eabf-175">Замените следующие значения в приведенном выше примере соответствующими значениями для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="4eabf-175">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="4eabf-176">$DOMAIN $ \ \ $SERVERNAME $ $-введите домен и имя MBAM сервера администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="4eabf-176">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="4eabf-177">За именем сервера должен следовать $, как показано в примере (например, MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="4eabf-177">The server name must be followed by a $, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>



~~~
This command line must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="4eabf-178">Обновление данных подключения к базе данных восстановления на серверах администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="4eabf-178">Update the Recovery Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="4eabf-179">На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, обновите данные строки подключения для указанных ниже приложений, размещенных на веб-сайте администрирования и мониторинга, с помощью консоли диспетчера информационных служб Интернета (IIS).</span><span class="sxs-lookup"><span data-stu-id="4eabf-179">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="4eabf-180">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="4eabf-180">MBAMAdministrationService</span></span>

   -   <span data-ttu-id="4eabf-181">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="4eabf-181">MBAMRecoveryAndHardwareService</span></span>

2. <span data-ttu-id="4eabf-182">Выберите каждое приложение и используйте функцию **редактора конфигурации** , расположенную в разделе **Управление** **представлением функций**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-182">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="4eabf-183">В элементе управления **списком разделов** выберите параметр **configurationStrings** .</span><span class="sxs-lookup"><span data-stu-id="4eabf-183">Select the **configurationStrings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="4eabf-184">Выберите строку с именем **(коллекцией)** и откройте **Редактор коллекций** , нажав кнопку в правой части строки.</span><span class="sxs-lookup"><span data-stu-id="4eabf-184">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="4eabf-185">В **редакторе коллекции**выберите строку с именем **KeyRecoveryConnectionString** при обновлении конфигурации приложения MBAMAdministrationService или строки с именем <strong> Microsoft. MBAM. RecoveryAndHardwareDataStore. </strong> Строка подключения к обновлению конфигурации для MBAMRecoveryAndHardwareService.</span><span class="sxs-lookup"><span data-stu-id="4eabf-185">In the **Collection Editor**, select the row named **KeyRecoveryConnectionString** when updating the configuration for the MBAMAdministrationService application or the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString when updating the configuration for the MBAMRecoveryAndHardwareService.</span></span>

6. <span data-ttu-id="4eabf-186">Обновите **источник данных =** значение для свойства **configurationStrings** , чтобы получить список имени сервера и экземпляра (например, $SERVERNAME $ \ \ $SQLINSTANCENAME $), на который была перемещена база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="4eabf-186">Update the **Data Source=** value for the **configurationStrings** property to list the server name and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME$) where the Recovery Database was moved to.</span></span>

7. <span data-ttu-id="4eabf-187">Для автоматизации этой процедуры вы можете ввести в Windows командную строку, подобную приведенной ниже, на каждом сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="4eabf-187">To automate this procedure, you can use Windows to enter a command line, that is similar to the following, on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="4eabf-188">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-188">Note</span></span>**  
   <span data-ttu-id="4eabf-189">Замените приведенное ниже значение в приведенном выше примере, чтобы оно соответствовало вашей среде.</span><span class="sxs-lookup"><span data-stu-id="4eabf-189">Replace the following value in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="4eabf-190">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, где находится база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="4eabf-190">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is.</span></span>



**<span data-ttu-id="4eabf-191">Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="4eabf-191">Resume all Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="4eabf-192">На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для запуска веб-сайта MBAM, который называется **администрированием и мониторингом Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-192">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="4eabf-193">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, сходной с:</span><span class="sxs-lookup"><span data-stu-id="4eabf-193">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="4eabf-194">Переход на функцию соответствия и аудита базы данных</span><span class="sxs-lookup"><span data-stu-id="4eabf-194">Moving the Compliance and Audit Database Feature</span></span>


<span data-ttu-id="4eabf-195">Если вы хотите перенести базу данных соответствия MBAM и аудита с одного компьютера на другой (то есть переместить базу данных с сервера A на сервер B), выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4eabf-195">If you want to move the MBAM Compliance and Audit Database from one computer to another (that is, move the database from Server A to Server B), use the following procedure.</span></span> <span data-ttu-id="4eabf-196">Этот процесс включает следующие высокоуровневые этапы.</span><span class="sxs-lookup"><span data-stu-id="4eabf-196">The process includes the following high-level steps:</span></span>

1.  <span data-ttu-id="4eabf-197">Остановите все экземпляры веб-сайта администрирования и наблюдения.</span><span class="sxs-lookup"><span data-stu-id="4eabf-197">Stop all instances of the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="4eabf-198">Запустите настройку MBAM на сервере B.</span><span class="sxs-lookup"><span data-stu-id="4eabf-198">Run MBAM setup on Server B.</span></span>

3.  <span data-ttu-id="4eabf-199">Создание резервной копии базы данных на сервере A.</span><span class="sxs-lookup"><span data-stu-id="4eabf-199">Back up the Database on Server A.</span></span>

4.  <span data-ttu-id="4eabf-200">Переместить базу данных с сервера A в B.</span><span class="sxs-lookup"><span data-stu-id="4eabf-200">Move the Database from Server A to B.</span></span>

5.  <span data-ttu-id="4eabf-201">Восстановите базу данных на сервере B.</span><span class="sxs-lookup"><span data-stu-id="4eabf-201">Restore the Database on Server B.</span></span>

6.  <span data-ttu-id="4eabf-202">Настройка доступа к базе данных на сервере B.</span><span class="sxs-lookup"><span data-stu-id="4eabf-202">Configure access to the Database on Server B.</span></span>

7.  <span data-ttu-id="4eabf-203">Обновите данные подключения к базе данных на серверах администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="4eabf-203">Update the database connection data on the MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="4eabf-204">Обновите строку подключения к источнику данных отчетов SSRS с новым расположением базы данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="4eabf-204">Update the SSRS reports data source connection string with the new location of the Compliance and Audit Database.</span></span>

9.  <span data-ttu-id="4eabf-205">Возобновление всех экземпляров веб-сайта администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="4eabf-205">Resume all instances of the Administration and Monitoring website.</span></span>

**<span data-ttu-id="4eabf-206">Остановка всех экземпляров веб-сайта администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="4eabf-206">Stop All Instances of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="4eabf-207">На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-207">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="4eabf-208">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-208">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-s “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="4eabf-209">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-209">Note</span></span>**  
    <span data-ttu-id="4eabf-210">Чтобы выполнить эту командную строку, необходимо добавить в текущий экземпляр PowerShell модуль IIS для PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4eabf-210">To run this command line, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="4eabf-211">Кроме того, необходимо обновить политику выполнения PowerShell, чтобы разрешить выполнение сценариев.</span><span class="sxs-lookup"><span data-stu-id="4eabf-211">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



**<span data-ttu-id="4eabf-212">Запуск настройки MBAM на сервере B</span><span class="sxs-lookup"><span data-stu-id="4eabf-212">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="4eabf-213">Запустите настройку MBAM на сервере B и выберите только **базу данных соответствия требованиям и аудита** для установки.</span><span class="sxs-lookup"><span data-stu-id="4eabf-213">Run MBAM Setup on Server B and select only the **Compliance and Audit Database** for installation.</span></span>

2.  <span data-ttu-id="4eabf-214">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-214">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="4eabf-215">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-215">Note</span></span>**  
    <span data-ttu-id="4eabf-216">Примечание. Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:</span><span class="sxs-lookup"><span data-stu-id="4eabf-216">Note: Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="4eabf-217">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, на который будет перемещена база данных соответствия и аудита.</span><span class="sxs-lookup"><span data-stu-id="4eabf-217">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be moved to.</span></span>

    -   <span data-ttu-id="4eabf-218">$DOMAIN $ \ \ $SERVERNAME $ — введите имена домена и сервера для каждого сервера администрирования и мониторинга MBAM, который будет обращаться к базе данных "соответствие требованиям и аудиту".</span><span class="sxs-lookup"><span data-stu-id="4eabf-218">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Compliance and Audit Database.</span></span> <span data-ttu-id="4eabf-219">Для разделения каждой пары доменных и серверных серверов в списке используйте точку с запятой (например, $DOMAIN \ \ \ \ \ домен \; $DOMAIN \ \ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="4eabf-219">Use a semi-colon to separate each domain and server pair in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="4eabf-220">За именем каждого сервера должен следовать символ "$", как показано в примере (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="4eabf-220">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="4eabf-221">$DOMAIN $ \ \ $USERNAME $-введите домен и имя пользователя, которые будут использоваться функцией проверки соответствия и аудита для подключения к базе данных "соответствие требованиям" и "Аудит".</span><span class="sxs-lookup"><span data-stu-id="4eabf-221">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="4eabf-222">$X $-введите **0** , если вы устанавливаете изолированную топологию MBAM или **1** при установке топологии Configuration Manager MBAM.</span><span class="sxs-lookup"><span data-stu-id="4eabf-222">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="4eabf-223">Создание резервной копии базы данных соответствия требованиям и аудита на сервере A</span><span class="sxs-lookup"><span data-stu-id="4eabf-223">Back Up the Compliance and Audit Database on Server A</span></span>**

1.  <span data-ttu-id="4eabf-224">Для резервного копирования базы данных соответствия требованиям и аудита на сервере A используйте SQL Server Management Studio и задачу с именем " **резервная копия**".</span><span class="sxs-lookup"><span data-stu-id="4eabf-224">To back up the Compliance and Audit Database on Server A, use SQL Server Management Studio and the task named **Back Up**.</span></span> <span data-ttu-id="4eabf-225">По умолчанию в качестве имени базы данных используется **база данных состояния соответствия MBAM**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-225">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="4eabf-226">Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:</span><span class="sxs-lookup"><span data-stu-id="4eabf-226">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

3.  <span data-ttu-id="4eabf-227">Запустите SQL-файл, используя командную строку Windows PowerShell, подобную приведенной ниже:</span><span class="sxs-lookup"><span data-stu-id="4eabf-227">Run the SQL file by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="4eabf-228">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-228">Note</span></span>**  
    <span data-ttu-id="4eabf-229">Замените приведенное ниже значение в приведенном выше примере, чтобы оно соответствовало вашей среде.</span><span class="sxs-lookup"><span data-stu-id="4eabf-229">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="4eabf-230">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, из которого будет выполняться резервное копирование базы данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="4eabf-230">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit database will be backed up from.</span></span>



**<span data-ttu-id="4eabf-231">Перенос базы данных соответствия требованиям и аудита с сервера A на B</span><span class="sxs-lookup"><span data-stu-id="4eabf-231">Move the Compliance and Audit Database from Server A to B</span></span>**

1.  <span data-ttu-id="4eabf-232">Переместите следующие файлы с сервера A на сервер B с помощью проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="4eabf-232">Move the following files from Server A to Server B using Windows Explorer.</span></span>

    -   <span data-ttu-id="4eabf-233">Данные базы данных о состоянии соответствия MBAM. bak</span><span class="sxs-lookup"><span data-stu-id="4eabf-233">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="4eabf-234">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-234">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="4eabf-235">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-235">Note</span></span>**  
    <span data-ttu-id="4eabf-236">Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:</span><span class="sxs-lookup"><span data-stu-id="4eabf-236">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="4eabf-237">$SERVERNAME $ — введите имя сервера, куда будут скопированы файлы.</span><span class="sxs-lookup"><span data-stu-id="4eabf-237">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="4eabf-238">$DESTINATIONSHARE $ — введите имя и путь к папке, куда будут скопированы файлы.</span><span class="sxs-lookup"><span data-stu-id="4eabf-238">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="4eabf-239">Восстановление базы данных соответствия и аудита на сервере B</span><span class="sxs-lookup"><span data-stu-id="4eabf-239">Restore the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="4eabf-240">Восстановите базу данных соответствия и аудита на сервере B с помощью SQL Server Management Studio и задачи с именем **Database Restore**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-240">Restore the Compliance and Audit Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="4eabf-241">После завершения задачи выберите файл резервной копии базы данных, выбрав параметр **с устройства** , а затем с помощью команды **Добавить** выберите файл Data MBAM. bak (состояние соответствия требованиям к БД).</span><span class="sxs-lookup"><span data-stu-id="4eabf-241">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="4eabf-242">Нажмите кнопку **ОК** , чтобы завершить процесс восстановления.</span><span class="sxs-lookup"><span data-stu-id="4eabf-242">Select **OK** to complete the restoration process.</span></span>

3.  <span data-ttu-id="4eabf-243">Для автоматизации этой процедуры создайте SQL-файл (SQL), содержащий следующий сценарий SQL:</span><span class="sxs-lookup"><span data-stu-id="4eabf-243">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="4eabf-244">Запустите SQL-файл, используя командную строку Windows PowerShell, подобную приведенной ниже:</span><span class="sxs-lookup"><span data-stu-id="4eabf-244">Run the SQL File by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="4eabf-245">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-245">Note</span></span>**  
    <span data-ttu-id="4eabf-246">Замените приведенное ниже значение в приведенном выше примере, чтобы оно соответствовало вашей среде.</span><span class="sxs-lookup"><span data-stu-id="4eabf-246">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="4eabf-247">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, на который будет восстановлена база данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="4eabf-247">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be restored to.</span></span>



**<span data-ttu-id="4eabf-248">Настройка доступа к базе данных "соответствие требованиям" и "Аудит" на сервере B</span><span class="sxs-lookup"><span data-stu-id="4eabf-248">Configure Access to the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="4eabf-249">На сервере B с помощью оснастки "Локальные пользователи и группы" в диспетчере серверов добавьте учетные записи компьютеров с каждого сервера, на котором запущена функция администрирования и мониторинга MBAM, в локальную группу с именем **MBAM соответствия требованиям к базе данных**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-249">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the local group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="4eabf-250">Убедитесь, что доступ к базе данных **аудита соответствия MBAM** для учетной записи SQL для восстановленной базы данных сопоставлен с именем для входа **$MachineName $ \ \ MBAM аудит соответствия требованиям к БД**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-250">Verify that the SQL login **MBAM Compliance Auditing DB Access** on the restored database is mapped to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span> <span data-ttu-id="4eabf-251">Если оно не сопоставлено так, как описано, создайте другое имя для входа, совпадающее с участием в группах, и сопоставьте его имени для входа **$MachineName $ \ \ MBAM для аудита соответствия требованиям к БД**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-251">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span>

3.  <span data-ttu-id="4eabf-252">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки на сервере B, похожей на указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-252">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="4eabf-253">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-253">Note</span></span>**  
    <span data-ttu-id="4eabf-254">Замените следующие значения в приведенном выше примере соответствующими значениями для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="4eabf-254">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="4eabf-255">$DOMAIN $ \ \ $SERVERNAME $ $-введите домен и имя MBAM сервера администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="4eabf-255">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="4eabf-256">За именем сервера должен следовать "$", как показано в примере.</span><span class="sxs-lookup"><span data-stu-id="4eabf-256">The server name must be followed by a “$” as shown in the example.</span></span> <span data-ttu-id="4eabf-257">(например, MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="4eabf-257">(for example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="4eabf-258">$DOMAIN $ \ \ $REPORTSUSERNAME $ — введите имя учетной записи пользователя, которое использовалось для настройки источника данных для отчетов о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="4eabf-258">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command line for adding the servers to the MBAM Compliance and Audit Database access local group must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="4eabf-259">Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="4eabf-259">Update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="4eabf-260">На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для обновления данных строки подключения для следующих приложений, размещенных на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="4eabf-260">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the connection string information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="4eabf-261">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="4eabf-261">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="4eabf-262">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="4eabf-262">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="4eabf-263">Выберите каждое приложение и используйте функцию **редактора конфигурации** , расположенную в разделе **Управление** **представлением функций**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-263">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="4eabf-264">В элементе управления **списком разделов** выберите параметр **configurationStrings** .</span><span class="sxs-lookup"><span data-stu-id="4eabf-264">Select the **configurationStrings** option from the **Section list** control.</span></span>

4.  <span data-ttu-id="4eabf-265">Выберите строку с именем **(коллекцией)** и откройте **Редактор коллекций** , нажав кнопку в правой части строки.</span><span class="sxs-lookup"><span data-stu-id="4eabf-265">Select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="4eabf-266">В **редакторе коллекций**выберите строку с именем **ComplianceStatusConnectionString** при обновлении конфигурации для приложения MBAMAdministrationService или строку с именем **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString** при обновлении конфигурации для MBAMComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="4eabf-266">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString** when updating the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString** when updating the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="4eabf-267">Обновите **источник данных =** значение свойства **configurationStrings** , чтобы получить список имен сервера и экземпляра (например, $SERVERNAME $ \ \ $SQLINSTANCENAME), в который была перемещена база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="4eabf-267">Update the **Data Source=** value for the **configurationStrings** property to list the name of the server and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

7.  <span data-ttu-id="4eabf-268">Для автоматизации этой процедуры вы можете ввести командную строку для каждого сервера администрирования и наблюдения с помощью Windows, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-268">To automate this procedure, you can use Windows to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="4eabf-269">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-269">Note</span></span>**  
    <span data-ttu-id="4eabf-270">Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:</span><span class="sxs-lookup"><span data-stu-id="4eabf-270">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="4eabf-271">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, где находится база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="4eabf-271">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is located.</span></span>



**<span data-ttu-id="4eabf-272">Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="4eabf-272">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="4eabf-273">На каждом сервере, на котором запущена функция администрирования и мониторинга MBAM, используйте консоль диспетчера служб IIS для запуска веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-273">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="4eabf-274">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-274">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="4eabf-275">Перемещение отчетов о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="4eabf-275">Moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="4eabf-276">Если вы хотите перенести отчеты о соответствии MBAM и аудиты с одного компьютера на другой (то есть переместить отчеты с сервера A на сервер B), выполните указанные ниже действия, в том числе следующие высокоуровневые этапы.</span><span class="sxs-lookup"><span data-stu-id="4eabf-276">If you want to move the MBAM Compliance and Audit Reports from one computer to another (that is, move the reports from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="4eabf-277">Запустите настройку MBAM на сервере B.</span><span class="sxs-lookup"><span data-stu-id="4eabf-277">Run MBAM setup on Server B.</span></span>

2.  <span data-ttu-id="4eabf-278">Настройка доступа к отчетам о соответствии и аудиту на сервере B.</span><span class="sxs-lookup"><span data-stu-id="4eabf-278">Configure access to the Compliance and Audit Reports on Server B.</span></span>

3.  <span data-ttu-id="4eabf-279">Остановите все экземпляры веб-сайта администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="4eabf-279">Stop all instances of the MBAM Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="4eabf-280">Обновите данные соединения отчетов на серверах администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="4eabf-280">Update the reports connection data on MBAM Administration and Monitoring servers.</span></span>

5.  <span data-ttu-id="4eabf-281">Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="4eabf-281">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="4eabf-282">Запуск настройки MBAM на сервере B</span><span class="sxs-lookup"><span data-stu-id="4eabf-282">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="4eabf-283">Запустите настройку MBAM на сервере B и выберите только **отчеты о соответствии и аудите** для установки.</span><span class="sxs-lookup"><span data-stu-id="4eabf-283">Run MBAM Setup on Server B and select only the **Compliance and Audit Reports** feature for installation.</span></span>

2.  <span data-ttu-id="4eabf-284">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-284">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$ TOPOLOGY=$X$`

    **<span data-ttu-id="4eabf-285">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-285">Note</span></span>**  
    <span data-ttu-id="4eabf-286">Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:</span><span class="sxs-lookup"><span data-stu-id="4eabf-286">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="4eabf-287">$SERVERNAME $ \ \ $SQLINSTANCENAME $-введите имя сервера и экземпляр, в котором находится база данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="4eabf-287">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database is located.</span></span>

    -   <span data-ttu-id="4eabf-288">$DOMAIN $ \ \ $USERNAME $-введите домен и имя пользователя, которые будут использоваться функцией проверки соответствия и аудита для подключения к базе данных "соответствие требованиям" и "Аудит".</span><span class="sxs-lookup"><span data-stu-id="4eabf-288">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="4eabf-289">$PASSWORD $-введите пароль учетной записи пользователя, который будет использоваться для подключения к базе данных "соответствие требованиям" и "Аудит".</span><span class="sxs-lookup"><span data-stu-id="4eabf-289">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="4eabf-290">$X $-введите **0** , если вы устанавливаете изолированную топологию MBAM или **1** при установке топологии Configuration Manager MBAM.</span><span class="sxs-lookup"><span data-stu-id="4eabf-290">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="4eabf-291">Настройка доступа к отчетам о соответствии и аудиту на сервере B</span><span class="sxs-lookup"><span data-stu-id="4eabf-291">Configure Access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="4eabf-292">На сервере B с помощью оснастки "Локальные пользователи и группы" в диспетчере серверов добавьте учетные записи пользователей, которые получат доступ к отчетам о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="4eabf-292">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="4eabf-293">Добавьте учетные записи пользователей в локальную группу с именем Пользователи отчета MBAM.</span><span class="sxs-lookup"><span data-stu-id="4eabf-293">Add the user accounts to the local group named MBAM Report Users.</span></span>

2.  <span data-ttu-id="4eabf-294">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки на сервере B, похожей на указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-294">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="4eabf-295">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-295">Note</span></span>**  
    <span data-ttu-id="4eabf-296">Замените следующие значения в приведенном выше примере соответствующими значениями для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="4eabf-296">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="4eabf-297">$DOMAIN $ \ \ $REPORTSUSERNAME $ — введите имя учетной записи пользователя, которое использовалось для настройки источника данных для отчетов о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="4eabf-297">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The command line for adding the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="4eabf-298">Остановка всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="4eabf-298">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="4eabf-299">На каждом сервере, на котором запущена функция администрирования и сервера мониторинга MBAM, используйте консоль диспетчера служб IIS для остановки веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-299">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="4eabf-300">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-300">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="4eabf-301">Обновление данных подключения к базе данных на серверах администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="4eabf-301">Update the Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="4eabf-302">На каждом сервере, на котором запущена функция администрирования и сервера мониторинга MBAM, обновите URL-адрес отчетов о соответствии и аудите с помощью консоли диспетчера служб IIS.</span><span class="sxs-lookup"><span data-stu-id="4eabf-302">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to update the Compliance and Audit Reports URL.</span></span>

2. <span data-ttu-id="4eabf-303">Выберите веб-сайт **администрирования Microsoft BitLocker и наблюдение за** ним с помощью средства **редактирования конфигурации** , расположенного в разделе **Управление** **представлением функций**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-303">Select the **Microsoft BitLocker Administration and Monitoring** website, and use the **Configuration Editor** feature that is location under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="4eabf-304">В элементе управления **списком разделов** выберите параметр **appSettings** .</span><span class="sxs-lookup"><span data-stu-id="4eabf-304">Select the **appSettings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="4eabf-305">Выберите строку с именем **(коллекцией)** и откройте **Редактор коллекций** , нажав кнопку в правой части строки.</span><span class="sxs-lookup"><span data-stu-id="4eabf-305">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="4eabf-306">В **редакторе коллекций**выберите строку с названием **Microsoft. MBAM. Reports. URL**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-306">In the **Collection Editor**, select the row named **Microsoft.Mbam.Reports.Url**.</span></span>

6. <span data-ttu-id="4eabf-307">Обновите значение **Microsoft. MBAM. Reports. URL** , чтобы оно отражало имя сервера для сервера B. Если функция проверки соответствия и аудита была установлена на именованном экземпляре служб SQL Reporting Services, не забудьте добавить или обновить имя экземпляра по URL-адресу (например, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....)</span><span class="sxs-lookup"><span data-stu-id="4eabf-307">Update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B. If the Compliance and Audit Reports feature was installed on a named SQL Reporting Services instance, be sure to add or update the name of the instance to the URL (for example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....)</span></span>

7. <span data-ttu-id="4eabf-308">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки на каждом сервере администрирования и наблюдения, которая аналогична описанной ниже:</span><span class="sxs-lookup"><span data-stu-id="4eabf-308">To automate this procedure, you can use Windows PowerShell to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\ \sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/ Microsoft+BitLocker+Administration+and+Monitoring/”`

   **<span data-ttu-id="4eabf-309">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-309">Note</span></span>**  
   <span data-ttu-id="4eabf-310">Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:</span><span class="sxs-lookup"><span data-stu-id="4eabf-310">Replace the following values in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="4eabf-311">$SERVERNAME $-введите имя сервера, на котором установлены отчеты о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="4eabf-311">$SERVERNAME$ - Enter the name of the server name to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="4eabf-312">$SRSINSTANCENAME $ — введите имя экземпляра служб SQL Reporting Services, для которого установлены отчеты о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="4eabf-312">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="4eabf-313">Возобновление всех экземпляров веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="4eabf-313">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="4eabf-314">На каждом сервере, на котором запущена функция администрирования и сервера мониторинга MBAM, используйте консоль диспетчера служб IIS для запуска веб-сайта MBAM, именуемого **администрированием и мониторингом Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="4eabf-314">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="4eabf-315">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-315">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="4eabf-316">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-316">Note</span></span>**  
    <span data-ttu-id="4eabf-317">Чтобы выполнить эту командную строку, необходимо добавить модуль IIS для PowerShell в текущий экземпляр PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4eabf-317">To run this command line, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="4eabf-318">Кроме того, необходимо обновить политику выполнения PowerShell, чтобы разрешить выполнение сценариев.</span><span class="sxs-lookup"><span data-stu-id="4eabf-318">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



## <span data-ttu-id="4eabf-319">Перемещение функций администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="4eabf-319">Moving the Administration and Monitoring Feature</span></span>


<span data-ttu-id="4eabf-320">Если вы хотите переместить функцию отчетов администрирования и мониторинга MBAM с одного компьютера на другой (то есть, переместить компонент с сервера A на сервер B), выполните указанные ниже действия, в том числе следующие высокоуровневые этапы.</span><span class="sxs-lookup"><span data-stu-id="4eabf-320">If you want to move the MBAM Administration and Monitoring Reports feature from one computer to another (that is, move the feature from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="4eabf-321">Запустите настройку MBAM на сервере B.</span><span class="sxs-lookup"><span data-stu-id="4eabf-321">Run MBAM Setup on Server B.</span></span>

2.  <span data-ttu-id="4eabf-322">Настройка доступа к базе данных на сервере B.</span><span class="sxs-lookup"><span data-stu-id="4eabf-322">Configure access to the Database on Server B.</span></span>

**<span data-ttu-id="4eabf-323">Запуск настройки MBAM на сервере B</span><span class="sxs-lookup"><span data-stu-id="4eabf-323">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="4eabf-324">Запустите настройку MBAM на сервере B и выберите компонент **сервера администрирования и мониторинга** для установки.</span><span class="sxs-lookup"><span data-stu-id="4eabf-324">Run MBAM Setup on Server B and select only the **Administration and Monitoring Server** feature for installation.</span></span>

2.  <span data-ttu-id="4eabf-325">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="4eabf-325">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer, COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$ TOPOLOGY=$X$`

    **<span data-ttu-id="4eabf-326">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-326">Note</span></span>**  
    <span data-ttu-id="4eabf-327">Замените следующие значения в приведенном выше примере, чтобы они соответствовали вашей среде:</span><span class="sxs-lookup"><span data-stu-id="4eabf-327">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="4eabf-328">$SERVERNAME $ \ \ $SQLINSTANCENAME $ — для параметра COMPLIDB \ _SQLINSTANCE введите имя сервера и экземпляр, в котором находится база данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="4eabf-328">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, enter the server name and instance where the Compliance and Audit Database is located.</span></span> <span data-ttu-id="4eabf-329">Для параметра RECOVERYANDHWDB \ _SQLINSTANCE введите имя сервера и экземпляр, где находится база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="4eabf-329">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, enter the server name and instance where the Recovery Database is located.</span></span>

    -   <span data-ttu-id="4eabf-330">$DOMAIN $ \ \ $USERNAME $-введите домен и имя пользователя, которые будут использоваться функцией проверки соответствия и аудита для подключения к базе данных "соответствие требованиям" и "Аудит".</span><span class="sxs-lookup"><span data-stu-id="4eabf-330">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="4eabf-331">$ REPORTSSERVERURL $ — введите URL-адрес домашнего расположения веб-сайта службы отчетов SQL.</span><span class="sxs-lookup"><span data-stu-id="4eabf-331">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="4eabf-332">Если отчеты были установлены в экземпляре SRS по умолчанию, формат URL-адреса будет иметь формат "http://$SERVERNAME $/ReportServer".</span><span class="sxs-lookup"><span data-stu-id="4eabf-332">If the reports were installed to a default SRS instance, the URL format will have the format “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="4eabf-333">Если отчеты были установлены в экземпляре SRS по умолчанию, формат URL-адреса будет иметь формат "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $".</span><span class="sxs-lookup"><span data-stu-id="4eabf-333">If the reports were installed to a default SRS instance, the URL format will have the format “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>

    -   <span data-ttu-id="4eabf-334">$X $-введите **0** , если вы устанавливаете изолированную топологию MBAM или **1** при установке топологии Configuration Manager MBAM.</span><span class="sxs-lookup"><span data-stu-id="4eabf-334">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="4eabf-335">Настройка доступа к базам данных</span><span class="sxs-lookup"><span data-stu-id="4eabf-335">Configure Access to the Databases</span></span>**

1.  <span data-ttu-id="4eabf-336">На сервере или серверах, на которых развернута база данных восстановления и соответствие требованиям и учетной записи, используйте оснастку "Локальные пользователи и группы" в диспетчере серверов, чтобы добавить учетные записи компьютеров с сервера, на котором работает сервер MBAM **администрирования и мониторинга** , в локальные группы с именами **MBAM Recovery**</span><span class="sxs-lookup"><span data-stu-id="4eabf-336">On the server or servers where the Recovery Database and Compliance and Audit Database are deployed, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring Server feature to the local groups named **MBAM Recovery and Hardware DB Access** (Recovery DB Server) and **MBAM Compliance Status DB Access** (Compliance and Audit Database Server).</span></span>

2.  <span data-ttu-id="4eabf-337">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода командной строки, которая аналогична приведенной ниже, на сервере, на котором развернута база данных соответствия и аудита.</span><span class="sxs-lookup"><span data-stu-id="4eabf-337">To automate this procedure, you can use Windows PowerShell to enter a command line, that is similar to the following, on the server where the Compliance and Audit Database was deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

3.  <span data-ttu-id="4eabf-338">На сервере, на котором развернута база данных восстановления, вы можете использовать Windows PowerShell для ввода следующей командной строки:</span><span class="sxs-lookup"><span data-stu-id="4eabf-338">On the server where the Recovery database was deployed, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="4eabf-339">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4eabf-339">Note</span></span>**  
    <span data-ttu-id="4eabf-340">Замените приведенное ниже значение в приведенном выше примере на применимые значения для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="4eabf-340">Replace the following value in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="4eabf-341">$DOMAIN $ \ \ $SERVERNAME $ $-введите домен и имя сервера администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="4eabf-341">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the Administration and Monitoring Server.</span></span> <span data-ttu-id="4eabf-342">За именем сервера должен следовать символ "$", как показано в примере (например, MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="4eabf-342">The server name must be followed by a “$” symbol, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>

    -   <span data-ttu-id="4eabf-343">$DOMAIN $ \ \ $REPORTSUSERNAME $ — введите имя учетной записи пользователя, которое использовалось для настройки источника данных для отчетов о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="4eabf-343">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command lines that are listed for adding server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="4eabf-344">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4eabf-344">Related topics</span></span>


[<span data-ttu-id="4eabf-345">Обслуживание MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="4eabf-345">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)









