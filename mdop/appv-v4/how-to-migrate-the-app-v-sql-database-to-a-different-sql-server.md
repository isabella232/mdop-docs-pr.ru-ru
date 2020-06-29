---
title: Миграция базы данных SQL App-V на другой сервер SQL Server
description: Миграция базы данных SQL App-V на другой сервер SQL Server
author: dansimp
ms.assetid: 353892a1-9327-4489-a19c-4ec7bd1b736f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e3d84b0cb328873db3722ad3eb9af6a2b442fdcf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817072"
---
# <span data-ttu-id="abb65-103">Миграция базы данных SQL App-V на другой сервер SQL Server</span><span class="sxs-lookup"><span data-stu-id="abb65-103">How to Migrate the App-V SQL Database to a Different SQL Server</span></span>


<span data-ttu-id="abb65-104">Ниже описаны инструкции по переносу базы данных SQL сервера управления Microsoft Application Virtualization (App-V) на другой сервер SQL Server.</span><span class="sxs-lookup"><span data-stu-id="abb65-104">The following procedures describe in detail how to migrate the SQL database of the Microsoft Application Virtualization (App-V) Management Server to a different SQL Server.</span></span>

<span data-ttu-id="abb65-105">**Важно!**  Для этой процедуры требуется, чтобы служба App-V была остановлена, а конечные пользователи не смогут использовать свои приложения.</span><span class="sxs-lookup"><span data-stu-id="abb65-105">**Important** This procedure requires that the App-V server service is stopped and this will prevent end-users from using their applications.</span></span>

 

**<span data-ttu-id="abb65-106">Создание резервной копии базы данных SQL App-V</span><span class="sxs-lookup"><span data-stu-id="abb65-106">To back up the App-V SQL database</span></span>**

1.  <span data-ttu-id="abb65-107">Откройте программу Services. msc и остановите службу сервера управления App-V на всех серверах управления, использующих эту базу данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="abb65-107">Open the Services.msc program and stop the App-V Management Server service on all Management Servers that use the database to be migrated.</span></span>

2.  <span data-ttu-id="abb65-108">На компьютере, на котором находится база данных App-V, откройте центр SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="abb65-108">On the computer where the App-V database is located, open SQL Server Management Studio.</span></span>

3.  <span data-ttu-id="abb65-109">Разверните узел **базы данных** и найдите базу данных App-V (имя по умолчанию — APPVIRT).</span><span class="sxs-lookup"><span data-stu-id="abb65-109">Expand the **Databases** node and locate the App-V database (default name is APPVIRT).</span></span>

4.  <span data-ttu-id="abb65-110">Щелкните правой кнопкой мыши базу данных и выберите **задачи** , а затем нажмите кнопку **создать резервную копию**.</span><span class="sxs-lookup"><span data-stu-id="abb65-110">Right-click the database and select **Tasks** and then select **Back Up**.</span></span>

5.  <span data-ttu-id="abb65-111">Убедитесь в том, что для **модели восстановления** задано значение **Simple** , а для **типа резервной копии** задано значение **полная**.</span><span class="sxs-lookup"><span data-stu-id="abb65-111">Verify that **Recovery model** is set to **SIMPLE** and the **Backup type** is set to **Full**.</span></span> <span data-ttu-id="abb65-112">При необходимости измените параметры **резервного** и **конечного** данных.</span><span class="sxs-lookup"><span data-stu-id="abb65-112">Change the **Backup set** and **Destination** settings if it is necessary.</span></span>

6.  <span data-ttu-id="abb65-113">Нажмите кнопку **ОК** , чтобы создать резервную копию базы данных.</span><span class="sxs-lookup"><span data-stu-id="abb65-113">Click **OK** to back up the database.</span></span> <span data-ttu-id="abb65-114">После успешного завершения архивации нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="abb65-114">After the backup has completed successfully, click **OK**.</span></span>

7.  <span data-ttu-id="abb65-115">Откройте проводник и перейдите в папку, содержащую файл резервной копии базы данных, например APPVIRT. BAK.</span><span class="sxs-lookup"><span data-stu-id="abb65-115">Open Windows Explorer and browse to the folder that contains the database backup file, for example APPVIRT.BAK.</span></span> <span data-ttu-id="abb65-116">Скопируйте файл резервной копии базы данных на конечный компьютер, на котором работает SQL Server.</span><span class="sxs-lookup"><span data-stu-id="abb65-116">Copy the database backup file to the destination computer that is running SQL Server.</span></span>

**<span data-ttu-id="abb65-117">Восстановление базы данных SQL App-V на конечном компьютере</span><span class="sxs-lookup"><span data-stu-id="abb65-117">To restore the App-V SQL database to the destination computer</span></span>**

1.  <span data-ttu-id="abb65-118">На конечном компьютере откройте центр SQL Server Management Studio, щелкните правой кнопкой мыши узел **базы данных** и выберите команду **восстановить базу данных**.</span><span class="sxs-lookup"><span data-stu-id="abb65-118">On the destination computer, open SQL Server Management Studio, right-click the **Databases** node and select **Restore Database**.</span></span>

2.  <span data-ttu-id="abb65-119">В разделе **источник для восстановления**выберите вариант **с устройства** и нажмите кнопку "**...".**</span><span class="sxs-lookup"><span data-stu-id="abb65-119">Under **Source for Restore**, choose **From device** and then click the “**…**”</span></span> <span data-ttu-id="abb65-120">.</span><span class="sxs-lookup"><span data-stu-id="abb65-120">button.</span></span>

3.  <span data-ttu-id="abb65-121">В диалоговом окне **Определение резервной копии** убедитесь, что на **носителе резервной копии** задан **файл** , а затем нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="abb65-121">In the **Specify Backup** dialog box, make sure that the **Backup Media** is set to **File** and then click **Add**.</span></span>

4.  <span data-ttu-id="abb65-122">Выберите файл резервной копии, который вы скопировали с исходного компьютера, на котором запущен SQL Server, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="abb65-122">Select the backup file that you copied from the original computer that is running SQL Server, and then click **OK**.</span></span>

5.  <span data-ttu-id="abb65-123">Нажмите кнопку **ОК** , а затем щелкните, чтобы выбрать резервную копию для восстановления.</span><span class="sxs-lookup"><span data-stu-id="abb65-123">Click **OK** and then click to select the backup set to restore.</span></span>

6.  <span data-ttu-id="abb65-124">В разделе **назначение для восстановления**щелкните раскрывающийся список для **базы данных** и выберите имя базы данных App-V (например, APPVIRT).</span><span class="sxs-lookup"><span data-stu-id="abb65-124">Under **Destination for restore**, click the drop-down for **To database** and select the App-V database name, for example APPVIRT.</span></span>

7.  <span data-ttu-id="abb65-125">Нажмите кнопку **ОК** , чтобы начать восстановление.</span><span class="sxs-lookup"><span data-stu-id="abb65-125">Click **OK** to start the restore.</span></span> <span data-ttu-id="abb65-126">После успешного завершения восстановления нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="abb65-126">After the restore has completed successfully, click **OK**.</span></span>

8.  <span data-ttu-id="abb65-127">Разверните узел **Безопасность** , щелкните правой кнопкой мыши **логины** и выберите команду **создать учетную запись**.</span><span class="sxs-lookup"><span data-stu-id="abb65-127">Expand the **Security** node, right-click **Logins** and select **New Login**.</span></span>

9.  <span data-ttu-id="abb65-128">В поле **имя для входа** введите сведения об учетной записи сетевой службы для сервера управления App-V в формате DOMAIN\\SERVERNAME $.</span><span class="sxs-lookup"><span data-stu-id="abb65-128">In the **Login Name** field, enter the Network Service account details for the App-V Management Server in the format of DOMAIN\\SERVERNAME$.</span></span>

10. <span data-ttu-id="abb65-129">На странице **Общие** в разделе **база данных по умолчанию** выберите имя базы данных App-V (например, APPVIRT), а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="abb65-129">On the **General** page under **Default database** select the App-V database name, for example, APPVIRT, and then click **OK**.</span></span>

11. <span data-ttu-id="abb65-130">В разделе **Выбор страницы**нажмите кнопку, чтобы выбрать страницу **сопоставления пользователей** .</span><span class="sxs-lookup"><span data-stu-id="abb65-130">Under **Select a page**, click to select the **User Mapping** page.</span></span> <span data-ttu-id="abb65-131">В разделе **Пользователи, сопоставленные с этим именем входа**, установите флажок в столбце **сопоставить** , чтобы выбрать базу данных App-V.</span><span class="sxs-lookup"><span data-stu-id="abb65-131">Under **Users mapped to this login**, click the check box in the **Map** column to select the App-V database.</span></span>

12. <span data-ttu-id="abb65-132">В разделе \*\*членство в роли базы данных для: &lt; Appvdatabasename &gt; \*\*выберите **SFTEveryone** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="abb65-132">Under **Database role membership for: &lt;appvdatabasename&gt;**, click to select **SFTEveryone** and then click **OK**.</span></span>

13. <span data-ttu-id="abb65-133">Убедитесь в том, что брандмауэр Windows на новом компьютере, на котором запущен SQL Server, настроен так, чтобы сервер управления App-V мог получить доступ к системе.</span><span class="sxs-lookup"><span data-stu-id="abb65-133">Make sure that the Windows Firewall on the new computer that is running SQL Server is configured to allow the App-V Management Server to access the system.</span></span> <span data-ttu-id="abb65-134">В разделе **средства администрирования**с помощью **брандмауэра Windows в приложении Advanced Security** можно создать **правило входящего трафика** для порта, используемого SQL Server (по умолчанию — это порт 1433).</span><span class="sxs-lookup"><span data-stu-id="abb65-134">Under **Administrative Tools**, use the **Windows Firewall with Advanced Security** program to create an **Inbound Rule** for the port that is used by SQL Server (default is port 1433).</span></span>

**<span data-ttu-id="abb65-135">Миграция заданий агента SQL Server App-V</span><span class="sxs-lookup"><span data-stu-id="abb65-135">To migrate the App-V SQL Server Agent jobs</span></span>**

1.  <span data-ttu-id="abb65-136">На исходном компьютере, на котором запущен SQL Server, в SQL Server Management Studio, разверните узел **агента SQL Server** , а затем разверните узел **задания** .</span><span class="sxs-lookup"><span data-stu-id="abb65-136">On the original computer that is running SQL Server, in SQL Server Management Studio, expand the **SQL Server Agent** node, and then expand the **Jobs** node.</span></span>

2.  <span data-ttu-id="abb65-137">Щелкните правой кнопкой мыши четыре задания App-V и выберите **Задание для сценария: | Создание | Файл**и сохраните каждый сценарий в папке и присвойте каждому из них описательное имя.</span><span class="sxs-lookup"><span data-stu-id="abb65-137">Right-click the following four App-V jobs and select **Script Job as | CREATE to | File**, and save each script to a folder and give each script a descriptive name.</span></span>

    -   **<span data-ttu-id="abb65-138">Журнал использования базы данных SoftGrid (appvdbname)</span><span class="sxs-lookup"><span data-stu-id="abb65-138">Softgrid Database (appvdbname) Check Usage History</span></span>**

    -   **<span data-ttu-id="abb65-139">База данных SoftGrid (appvdbname) закрытие потерянных сеансов</span><span class="sxs-lookup"><span data-stu-id="abb65-139">Softgrid Database (appvdbname) Close Orphaned Sessions</span></span>**

    -   **<span data-ttu-id="abb65-140">База данных SoftGrid (appvdbname) принудительное ограничение размера</span><span class="sxs-lookup"><span data-stu-id="abb65-140">Softgrid Database (appvdbname) Enforce Size Limit</span></span>**

    -   **<span data-ttu-id="abb65-141">Управление базой данных SoftGrid (appvdbname) отслеживание состояния уведомлений и заданий</span><span class="sxs-lookup"><span data-stu-id="abb65-141">Softgrid Database (appvdbname) Monitor Alert/Job Status</span></span>**

3.  <span data-ttu-id="abb65-142">Скопируйте четыре файла сценария (SQL) на конечный компьютер, на котором работает SQL Server, и откройте центр SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="abb65-142">Copy the four script files (.sql) to the destination computer that is running SQL Server and open SQL Server Management Studio.</span></span>

4.  <span data-ttu-id="abb65-143">В проводнике щелкните каждый из файлов SQL правой кнопкой мыши и выберите команду **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="abb65-143">In Windows Explorer, right-click each .sql file and then click **Run**.</span></span> <span data-ttu-id="abb65-144">Каждый сценарий откроется в окне запроса в SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="abb65-144">Each script will open in a query window in SQL Server Management Studio.</span></span> <span data-ttu-id="abb65-145">Нажмите кнопку **выполнить** для каждого сценария и убедитесь, что все выполнены успешно.</span><span class="sxs-lookup"><span data-stu-id="abb65-145">Click **Execute** for each script and verify that each is completed successfully.</span></span>

5.  <span data-ttu-id="abb65-146">Обновите узел **задания** под узлом **агента SQL Server** и убедитесь, что четыре задания успешно созданы.</span><span class="sxs-lookup"><span data-stu-id="abb65-146">Refresh the **Jobs** node under the **SQL Server Agent** node and confirm that the four jobs are created successfully.</span></span>

**<span data-ttu-id="abb65-147">Обновление конфигурации сервера управления App-V</span><span class="sxs-lookup"><span data-stu-id="abb65-147">To update the configuration of the App-V Management Server</span></span>**

1.  <span data-ttu-id="abb65-148">На сервере управления App-V измените указанные ниже разделы реестра.</span><span class="sxs-lookup"><span data-stu-id="abb65-148">On the App-V Management Server, modify the following registry keys:</span></span>

    -   <span data-ttu-id="abb65-149">**SQLServerName**  =  SQLSERVERNAME &lt; newservername&gt;</span><span class="sxs-lookup"><span data-stu-id="abb65-149">**SQLServerName** = &lt;newservername&gt;</span></span>

    -   <span data-ttu-id="abb65-150">**SQLServerPort**  =  SQLServerPort &lt; newserverport&gt;</span><span class="sxs-lookup"><span data-stu-id="abb65-150">**SQLServerPort** = &lt;newserverport&gt;</span></span>

    <span data-ttu-id="abb65-151">Затем перезапустите службу App-V Server.</span><span class="sxs-lookup"><span data-stu-id="abb65-151">Then restart the App-V server service.</span></span>

2.  <span data-ttu-id="abb65-152">Найдите файл SftMgmt. UDL в каталоге установки сервера App-V (по умолчанию — C:\\program Files Files\\Microsoft приложение System Center virt Management Service Server\\App-virt Management).</span><span class="sxs-lookup"><span data-stu-id="abb65-152">Browse to find the file SftMgmt.udl under the App-V Management Server installation directory (default is C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Service).</span></span> <span data-ttu-id="abb65-153">Щелкните файл правой кнопкой мыши и выберите команду **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="abb65-153">Right-click the file and select **Open**.</span></span>

3.  <span data-ttu-id="abb65-154">На вкладке **Подключение** введите имя конечного компьютера, на котором запущен SQL Server, и нажмите кнопку **проверить подключение**.</span><span class="sxs-lookup"><span data-stu-id="abb65-154">On the **Connection** tab, enter the name of the destination computer that is running SQL Server, and then click **Test Connection**.</span></span> <span data-ttu-id="abb65-155">При успешном завершении проверки нажмите кнопку **ОК** , а затем еще раз нажмите кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="abb65-155">When the test is successful, click **OK** and then click **OK** again.</span></span>

4.  <span data-ttu-id="abb65-156">В версиях сервера управления App-V до 4,5 с пакетом обновления 2 (SP2) необходимо обновить параметры ведения журнала SQL.</span><span class="sxs-lookup"><span data-stu-id="abb65-156">For App-V Management Server versions before 4.5 SP2, you must update the SQL Logging settings.</span></span> <span data-ttu-id="abb65-157">В разделе **группы серверов**щелкните правой кнопкой мыши группу серверов, в которую входит сервер, и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="abb65-157">Under **Server Groups**, right-click the server group the server is a member of and select **Properties**.</span></span>

5.  <span data-ttu-id="abb65-158">На вкладке **ведение журнала** выберите запись **базы данных SQL** и нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="abb65-158">On the **Logging** tab click to select the **SQL Database** entry and then click **Edit**.</span></span>

6.  <span data-ttu-id="abb65-159">Измените **имя узла DNS** на имя узла нового компьютера, на котором запущен SQL Server, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="abb65-159">Change the **DNS Host Name** to the host name of the new computer that is running SQL Server and then click **OK**.</span></span> <span data-ttu-id="abb65-160">Дважды нажмите кнопку **ОК** , а затем перезапустите службу App-V Server.</span><span class="sxs-lookup"><span data-stu-id="abb65-160">Click **OK** two times more, and then restart the App-V server service.</span></span>

7.  <span data-ttu-id="abb65-161">Откройте консоль управления App-V, щелкните правой кнопкой мыши узел **приложения** и выберите команду **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="abb65-161">Open the App-V Management Console, right-click the **Applications** node and select **Refresh**.</span></span> <span data-ttu-id="abb65-162">Список приложений должен отображаться так, как раньше.</span><span class="sxs-lookup"><span data-stu-id="abb65-162">The list of applications should be displayed as before.</span></span>

 

 





