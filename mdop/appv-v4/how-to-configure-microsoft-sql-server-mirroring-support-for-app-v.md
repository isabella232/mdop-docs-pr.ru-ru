---
title: Настройка поддержки зеркального отображения Microsoft SQL Server для App-V
description: Настройка поддержки зеркального отображения Microsoft SQL Server для App-V
author: dansimp
ms.assetid: 6d069eb5-109f-460a-836a-de49473b7035
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fb572442cd12bb32fc9406de65f05a3bf061f946
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817932"
---
# <span data-ttu-id="da7ee-103">Настройка поддержки зеркального отображения Microsoft SQL Server для App-V</span><span class="sxs-lookup"><span data-stu-id="da7ee-103">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span>


<span data-ttu-id="da7ee-104">С помощью описанной ниже процедуры можно настроить среду Microsoft Application Virtualization (App-V) для использования зеркального отображения базы данных Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="da7ee-104">You can use the following procedure to configure your Microsoft Application Virtualization (App-V) environment to use Microsoft SQL Server database mirroring.</span></span> <span data-ttu-id="da7ee-105">Настройка зеркального отображения базы данных может помочь в сценариях аварийного восстановления и перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="da7ee-105">Configuring database mirroring can help with disaster recovery and failover scenarios.</span></span> <span data-ttu-id="da7ee-106">App-V 4,5 SP2 поддерживает все режимы зеркального отображения базы данных, доступные в настоящее время для Microsoft SQL Server 2005 и SQL Server 2008.</span><span class="sxs-lookup"><span data-stu-id="da7ee-106">App-V 4.5 SP2 supports all modes of database mirroring currently available for Microsoft SQL Server 2005 and SQL Server 2008.</span></span>

**<span data-ttu-id="da7ee-107">Примечание.</span><span class="sxs-lookup"><span data-stu-id="da7ee-107">Note</span></span>**  
<span data-ttu-id="da7ee-108">Эта процедура предназначена для администраторов, знакомых с настройкой и настройкой баз данных SQL Server и зеркальным отображением базы данных в Microsoft SQL Server и, следовательно, охватывает только определенные параметры конфигурации, уникальные для App-V.</span><span class="sxs-lookup"><span data-stu-id="da7ee-108">This procedure is written for administrators who are familiar with setting up and configuring SQL Server databases and database mirroring with Microsoft SQL Server, and therefore covers only the specific configuration settings that are unique to App-V.</span></span>



**<span data-ttu-id="da7ee-109">Настройка среды App-V для использования зеркального отображения базы данных Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="da7ee-109">To configure your App-V environment to use Microsoft SQL Server database mirroring</span></span>**

1.  <span data-ttu-id="da7ee-110">Настройте зеркальное отображение базы данных SQL Server в базе данных App-V, следуя стандартным бизнес-рекомендациям для зеркального отображения базы данных.</span><span class="sxs-lookup"><span data-stu-id="da7ee-110">Set up SQL Server database mirroring of the App-V database following your standard business practices for database mirroring.</span></span> <span data-ttu-id="da7ee-111">Чтобы получить общие сведения о реализации зеркального отображения базы данных Microsoft SQL Server, воспользуйтесь следующими ссылками:</span><span class="sxs-lookup"><span data-stu-id="da7ee-111">Use the following links for general information about implementing Microsoft SQL Server database mirroring:</span></span>

    -   <span data-ttu-id="da7ee-112">**Microsoft SQL 2005**—[Настройка зеркального отображения базы данных](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)</span><span class="sxs-lookup"><span data-stu-id="da7ee-112">**Microsoft SQL 2005**—[Setting Up Database Mirroring](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)</span></span>

    -   <span data-ttu-id="da7ee-113">**Microsoft SQL 2008**—[Настройка зеркального отображения базы данных](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)</span><span class="sxs-lookup"><span data-stu-id="da7ee-113">**Microsoft SQL 2008**—[Setting Up Database Mirroring](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)</span></span>

    <span data-ttu-id="da7ee-114">Кроме того, вы можете найти советы и рекомендации по [обеспечению зеркального отображения баз данных и их производительности](https://go.microsoft.com/fwlink/?LinkId=190270) ( https://go.microsoft.com/fwlink/?LinkId=190270) .</span><span class="sxs-lookup"><span data-stu-id="da7ee-114">In addition, you can find Best Practices information in [Database Mirroring Best Practices and Performance Considerations](https://go.microsoft.com/fwlink/?LinkId=190270) (https://go.microsoft.com/fwlink/?LinkId=190270).</span></span>

2.  <span data-ttu-id="da7ee-115">После настройки зеркального отображения убедитесь в том, что база данных App-V показывает состояние **(основной, синхронизированный)**, а зеркальная база данных показывает состояние **(зеркало, синхронизированное и восстановление)**.</span><span class="sxs-lookup"><span data-stu-id="da7ee-115">After mirroring has been set up, verify that the App-V database shows a status of **(Principal, Synchronized)**, and the mirrored database shows a status of **(Mirror, Synchronized / Restoring)**.</span></span> <span data-ttu-id="da7ee-116">Устраните проблемы зеркального отображения, прежде чем переходить к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="da7ee-116">Resolve any mirroring issues before proceeding to the next step.</span></span> <span data-ttu-id="da7ee-117">Дополнительные сведения о наблюдении за состоянием можно найти в разделе [наблюдение за состоянием зеркального отображения](https://go.microsoft.com/fwlink/?LinkId=190279) ( https://go.microsoft.com/fwlink/?LinkId=190279) .</span><span class="sxs-lookup"><span data-stu-id="da7ee-117">For additional information about monitoring the status, see [Monitoring Mirroring Status](https://go.microsoft.com/fwlink/?LinkId=190279) (https://go.microsoft.com/fwlink/?LinkId=190279).</span></span>

3.  <span data-ttu-id="da7ee-118">На компьютере SQL Server с зеркалом базы данных App-v создайте имя пользователя SQL Server для учетной записи сетевой службы сервера управления App-v с помощью имени учетной записи \*\* &lt; domain &gt; \\ &lt; ManagementServerHostName &gt; $ \*\*.</span><span class="sxs-lookup"><span data-stu-id="da7ee-118">On the SQL Server computer that hosts the mirror of the App-V database, create the SQL Server Login for the network service account of the App-V Management Server by using the account name **&lt;domain&gt;\\&lt;ManagementServerHostName&gt;$**.</span></span>

4.  <span data-ttu-id="da7ee-119">Установите Microsoft SQL Server Native Client на сервере App-V Management Server и на компьютере с веб-службой управления App-V, установленном на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="da7ee-119">Install the Microsoft SQL Server Native Client on the App-V Management Server, and on the computer running the App-V Management Web Service if installed on a different computer.</span></span> <span data-ttu-id="da7ee-120">Если вы планируете подключить дополнительные серверы управления App-V к зеркальной базе данных SQL для балансировки нагрузки, необходимо также установить клиент Microsoft SQL Server Native на этих компьютерах.</span><span class="sxs-lookup"><span data-stu-id="da7ee-120">If you plan to have additional App-V Management Servers connect to the mirrored SQL database for load balancing, you must install the Microsoft SQL Server Native Client on those computers as well.</span></span> <span data-ttu-id="da7ee-121">Вы можете скачать собственный клиент Microsoft SQL Server на веб-странице Microsoft [SQL server 2008 с пакетом дополнительных компонентов](https://go.microsoft.com/fwlink/?LinkId=187479) в центре загрузки Майкрософт ( https://go.microsoft.com/fwlink/?LinkId=187479) .</span><span class="sxs-lookup"><span data-stu-id="da7ee-121">You can download the Microsoft SQL Server Native Client from the [Microsoft SQL Server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) page in the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=187479).</span></span>

5.  <span data-ttu-id="da7ee-122">Проверьте раздел **hKey \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlservername** и убедитесь, что он включает только имя узла сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="da7ee-122">Check the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLServerName** and make sure that it contains only the host name of the SQL Server.</span></span> <span data-ttu-id="da7ee-123">Если он содержит имя экземпляра (например, *serverhostname\\instancename*), его имя должно быть удалено.</span><span class="sxs-lookup"><span data-stu-id="da7ee-123">If it includes an instance name, for example *serverhostname\\instancename*, the instance name must be removed.</span></span>

    **<span data-ttu-id="da7ee-124">Важно.</span><span class="sxs-lookup"><span data-stu-id="da7ee-124">Important</span></span>**  
    <span data-ttu-id="da7ee-125">Сервер управления App-V использует сетевую библиотеку TCP/IP для связи с SQL Server при включенном зеркальном отображении базы данных, поэтому имена экземпляров использовать нельзя.</span><span class="sxs-lookup"><span data-stu-id="da7ee-125">The App-V Management Server uses the TCP/IP networking library to communicate with the SQL Server when database mirroring is enabled, and therefore instance names cannot be used.</span></span> <span data-ttu-id="da7ee-126">Вместо этого номера портов должны быть указаны в разделах реестра.</span><span class="sxs-lookup"><span data-stu-id="da7ee-126">The port numbers must be specified in the registry keys instead.</span></span>



6.  <span data-ttu-id="da7ee-127">Проверьте раздел **hKey \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlserverport** и убедитесь, что он содержит номер порта, который используется для SQL на компьютере SQL Server.</span><span class="sxs-lookup"><span data-stu-id="da7ee-127">Check the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLServerPort** and make sure that it contains the port number that is used for SQL on the SQL Server computer.</span></span> <span data-ttu-id="da7ee-128">Если вы используете именованный экземпляр, это значение ключа должно быть задано для порта, используемого для именованного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="da7ee-128">If you are using a named instance this key value must be set to the port that is used for the named instance.</span></span>

7.  <span data-ttu-id="da7ee-129">Создайте раздел реестра **hKey \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverservername** AS REG \ _SZ и укажите в качестве значения имя узла сервера SQL Server, на котором размещается зеркало.</span><span class="sxs-lookup"><span data-stu-id="da7ee-129">Create the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLFailoverServerName** as REG\_SZ and then set the value to the host name of the SQL Server that hosts the mirror.</span></span>

8.  <span data-ttu-id="da7ee-130">Создайте раздел реестра **hKey \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverserverport** как DWORD и укажите номер порта, который будет использоваться для SQL на компьютере, на котором запущен SQL Server, для размещения зеркала.</span><span class="sxs-lookup"><span data-stu-id="da7ee-130">Create the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLFailoverServerPort** as DWORD and then set the value to the port number that is used for SQL on the computer that is running SQL Server to host the mirror.</span></span> <span data-ttu-id="da7ee-131">Если вы используете именованный экземпляр для зеркала, это значение ключа должно быть задано на номер порта, который используется для именованного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="da7ee-131">If you are using a named instance for the mirror this key value must be set to the port number that is used for the named instance.</span></span>

9.  <span data-ttu-id="da7ee-132">На компьютере, на котором работает веб-служба управления App-V, настройте текстовый файл универсальной связи с данными (UDL).</span><span class="sxs-lookup"><span data-stu-id="da7ee-132">On the computer that is running the App-V Management Web Service, configure the Universal Data Link (UDL) text file.</span></span> <span data-ttu-id="da7ee-133">В каталоге, где установлено приложение App-V, дважды щелкните **SftMgmt. udl** и укажите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="da7ee-133">In the directory where App-V is installed, double-click **SftMgmt.udl** and specify the following values:</span></span>

    -   <span data-ttu-id="da7ee-134">На вкладке **поставщик** выберите поставщик OLE DB **Native Client 10,0 клиента SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="da7ee-134">On the **Provider** tab, select the OLE DB provider **SQL Server Native Client 10.0**.</span></span>

    -   <span data-ttu-id="da7ee-135">Нажмите кнопку **Далее** , чтобы выбрать вкладку **Подключение** . В поле **имя сервера** введите имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="da7ee-135">Click **Next** to select the **Connection** tab. In the **Server Name** box, enter the server name of the SQL Server.</span></span> <span data-ttu-id="da7ee-136">Затем выберите **использовать встроенную безопасность Windows NT**.</span><span class="sxs-lookup"><span data-stu-id="da7ee-136">Next, select **Use Windows NT Integrated Security**.</span></span> <span data-ttu-id="da7ee-137">Наконец, щелкните список, **выберите базу данных**и укажите имя базы данных App-V.</span><span class="sxs-lookup"><span data-stu-id="da7ee-137">Finally, click the list **Select the database**, and then select the App-V database name.</span></span>

    -   <span data-ttu-id="da7ee-138">Откройте вкладку **все** , а затем выберите участника, на котором будет находиться **отказ**при входе.</span><span class="sxs-lookup"><span data-stu-id="da7ee-138">Click the **All** tab, and then select the entry **Failover Partner**.</span></span> <span data-ttu-id="da7ee-139">Нажмите кнопку **изменить значение**, а затем введите имя сервера SQL Server, на котором будет отработка отказа.</span><span class="sxs-lookup"><span data-stu-id="da7ee-139">Click **Edit Value**, and then enter the server name of the failover SQL Server.</span></span> <span data-ttu-id="da7ee-140">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="da7ee-140">Click **OK**.</span></span>

    **<span data-ttu-id="da7ee-141">Важно.</span><span class="sxs-lookup"><span data-stu-id="da7ee-141">Important</span></span>**  
    <span data-ttu-id="da7ee-142">Система App-V использует проверку подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="da7ee-142">The App-V system uses Kerberos authentication.</span></span> <span data-ttu-id="da7ee-143">Таким образом, когда вы настраиваете зеркальное отображение SQL, в котором включена проверка подлинности Kerberos на сервере SQL Server и служба SQL Server работает под учетной записью пользователя домена, необходимо вручную настроить SPN.</span><span class="sxs-lookup"><span data-stu-id="da7ee-143">Therefore, when you configure SQL mirroring where Kerberos Authentication is enabled on the SQL Server and the SQL Server service runs under a domain user account, you must manually configure an SPN.</span></span> <span data-ttu-id="da7ee-144">Дополнительные сведения можно найти в разделе "когда служба SQL использует учетные записи на основе доменов" в статье [Настройка администрирования App-V для распределенной среды](https://go.microsoft.com/fwlink/?LinkId=203186) ( https://go.microsoft.com/fwlink/?LinkId=203186) .</span><span class="sxs-lookup"><span data-stu-id="da7ee-144">For more information, see “When SQL Service Uses Domain-Based Account” in the article [Configuring App-V Administration for a Distributed Environment](https://go.microsoft.com/fwlink/?LinkId=203186) (https://go.microsoft.com/fwlink/?LinkId=203186).</span></span>



10. <span data-ttu-id="da7ee-145">Чтобы убедиться в том, что зеркальное отображение базы данных работает правильно, проверьте переход на другой ресурс и убедитесь, что сервер управления App-V продолжает работать правильно.</span><span class="sxs-lookup"><span data-stu-id="da7ee-145">To verify that database mirroring is running correctly, test the failover and confirm that the App-V Management Server continues to function correctly.</span></span>

    **<span data-ttu-id="da7ee-146">Важно.</span><span class="sxs-lookup"><span data-stu-id="da7ee-146">Important</span></span>**  
    <span data-ttu-id="da7ee-147">Будьте внимательны и проследите за вашими стандартными бизнес-рекомендациями, чтобы убедиться в том, что в случае сбоя система не будет прервана.</span><span class="sxs-lookup"><span data-stu-id="da7ee-147">Proceed with care, and follow your standard business practices to ensure that system operations are not disrupted in the event of a failure.</span></span>



~~~
After the failover has occurred successfully, as verified by using the SQL Server status monitoring information, right-click the **Applications** node in the App-V Management Console, and then select **Refresh**. The list of applications should display normally if the system is working correctly.
~~~

## <span data-ttu-id="da7ee-148">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="da7ee-148">Related topics</span></span>


[<span data-ttu-id="da7ee-149">Выполнение задач администрирования на консоли управления серверами Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="da7ee-149">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)









