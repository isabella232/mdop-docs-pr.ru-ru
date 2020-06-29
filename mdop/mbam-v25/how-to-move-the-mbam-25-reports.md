---
title: Перенос отчетов MBAM 2.5
description: Перенос отчетов MBAM 2.5
author: dansimp
ms.assetid: c8223656-ca9d-41c8-94a3-64d07a6b99e9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdef260b4381671a1b9de66565ece0b70876200
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812392"
---
# <span data-ttu-id="918ed-103">Перенос отчетов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="918ed-103">How to Move the MBAM 2.5 Reports</span></span>


<span data-ttu-id="918ed-104">Используйте эти инструкции, чтобы переместить функцию "отчеты" с одного компьютера на другой, а также переместить функцию "отчеты" с сервера A на сервер B.</span><span class="sxs-lookup"><span data-stu-id="918ed-104">Use these procedures to move the Reports feature from one computer to another, that is, to move the Reports feature from Server A to Server B.</span></span>

<span data-ttu-id="918ed-105">Ниже приведены высокоуровневые действия по перемещению отчетов.</span><span class="sxs-lookup"><span data-stu-id="918ed-105">The high-level steps for moving the Reports feature are:</span></span>

1.  <span data-ttu-id="918ed-106">Остановите все экземпляры веб-сайта администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="918ed-106">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="918ed-107">Установите серверное программное обеспечение MBAM 2,5 на сервере B и настройте функцию "отчеты" на сервере B.</span><span class="sxs-lookup"><span data-stu-id="918ed-107">Install the MBAM 2.5 Server software on Server B and configure the Reports feature on Server B.</span></span>

3.  <span data-ttu-id="918ed-108">Обновите данные соединения отчетов на серверах администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="918ed-108">Update the reports connection data on the MBAM Administration and Monitoring servers.</span></span>

4.  <span data-ttu-id="918ed-109">Возобновление работы на веб-сайте администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="918ed-109">Resume the instance of the MBAM Administration and Monitoring Website.</span></span>

<span data-ttu-id="918ed-110">**Примечание**  Чтобы выполнить примеры сценариев Windows PowerShell в этом разделе, необходимо обновить политику выполнения Windows PowerShell, чтобы включить сценарии для выполнения.</span><span class="sxs-lookup"><span data-stu-id="918ed-110">**Note** To run the example Windows PowerShell scripts in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="918ed-111">Инструкции приведены в разделе [выполнение сценариев Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) .</span><span class="sxs-lookup"><span data-stu-id="918ed-111">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

 

**<span data-ttu-id="918ed-112">Остановка веб-сайта администрирования и мониторинга MBAM</span><span class="sxs-lookup"><span data-stu-id="918ed-112">Stop the MBAM Administration and Monitoring Website</span></span>**

-   <span data-ttu-id="918ed-113">На сервере, на котором запущен веб-сайт администрирования и наблюдения, остановите веб-сайт администрирования и наблюдения с помощью консоли диспетчера служб IIS.</span><span class="sxs-lookup"><span data-stu-id="918ed-113">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="918ed-114">Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода команды, которая похожа на приведенную ниже.</span><span class="sxs-lookup"><span data-stu-id="918ed-114">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**<span data-ttu-id="918ed-115">Установка программного обеспечения сервера MBAM и запуск мастера настройки MBAM сервера на сервере B</span><span class="sxs-lookup"><span data-stu-id="918ed-115">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>**

1.  <span data-ttu-id="918ed-116">Установка программного обеспечения сервера MBAM на сервере B. Инструкции можно найти [в разделе Установка серверного программного обеспечения MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="918ed-116">Install the MBAM Server software on Server B. For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="918ed-117">На сервере B запустите мастер настройки сервера MBAM, выберите команду **Добавить новые функции**и выберите только функции **отчеты** .</span><span class="sxs-lookup"><span data-stu-id="918ed-117">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Reports** feature.</span></span>

    <span data-ttu-id="918ed-118">Кроме того, для настройки отчетов можно использовать командлет Windows PowerShell **Enable-MbamReport** .</span><span class="sxs-lookup"><span data-stu-id="918ed-118">Alternatively, you can use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span>

    <span data-ttu-id="918ed-119">Инструкции по настройке отчетов можно найти в разделе [Настройка MBAM отчетов 2,5](how-to-configure-the-mbam-25-reports.md).</span><span class="sxs-lookup"><span data-stu-id="918ed-119">For instructions on how to configure the Reports, see [How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md).</span></span>

**<span data-ttu-id="918ed-120">Обновление данных соединения отчетов на сервере администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="918ed-120">Update the reports connection data on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="918ed-121">На сервере, на котором работает функция отчетов, обновите URL-адрес отчетов с помощью консоли диспетчера служб IIS.</span><span class="sxs-lookup"><span data-stu-id="918ed-121">On the server that is running the Reports feature, use the Internet Information Services (IIS) Manager console to update the Reports URL.</span></span>

2.  <span data-ttu-id="918ed-122">Разверните раздел **Администрирование и мониторинг Microsoft BitLocker**и выберите узел Служба **поддержки** .</span><span class="sxs-lookup"><span data-stu-id="918ed-122">Expand **Microsoft BitLocker Administration and Monitoring**, and then select the **HelpDesk** node.</span></span>

3.  <span data-ttu-id="918ed-123">В разделе **Управление** **представлениями "функции**" выберите " **Редактор конфигураций**".</span><span class="sxs-lookup"><span data-stu-id="918ed-123">In the **Management** section of the **Features View**, select **Configuration Editor**.</span></span>

4.  <span data-ttu-id="918ed-124">В поле **раздел** выберите параметр **appSettings**.</span><span class="sxs-lookup"><span data-stu-id="918ed-124">In the **Section** field, select **appSettings**.</span></span>

5.  <span data-ttu-id="918ed-125">Выберите строку **коллекция** , а затем нажмите кнопку с многоточием **(...)** в правой части панели, чтобы открыть **Редактор коллекции**.</span><span class="sxs-lookup"><span data-stu-id="918ed-125">Select the **Collection** row, and then click the "ellipses" button **(…)** at the far right of the pane to open the **Collection Editor**.</span></span>

6.  <span data-ttu-id="918ed-126">В **редакторе коллекций**выберите строку, содержащую **Microsoft. MBAM. Reports. URL**, и обновите значение **Microsoft. MBAM. Reports. URL** , чтобы оно отражало имя сервера в сервере B.</span><span class="sxs-lookup"><span data-stu-id="918ed-126">In the **Collection Editor**, select the row that contains **Microsoft.Mbam.Reports.Url**, and update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B.</span></span>

    <span data-ttu-id="918ed-127">Если вы уже настроили функцию "отчеты" на именованном экземпляре служб SQL Server Reporting Services, добавьте или обновите имя экземпляра по URL-адресу, например:</span><span class="sxs-lookup"><span data-stu-id="918ed-127">If you previously configured the Reports feature on a named instance of SQL Server Reporting Services, add or update the name of the instance to the URL, for example:</span></span>

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  <span data-ttu-id="918ed-128">Для автоматизации этой процедуры вы можете использовать Windows PowerShell для выполнения команды на сервере администрирования и мониторинга, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="918ed-128">To automate this procedure, you can use Windows PowerShell to run a command on the Administration and Monitoring Server that is similar to the following code example.</span></span>

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    <span data-ttu-id="918ed-129">Используя описания в следующей таблице, замените значения в примере кода значениями, которые соответствуют вашей среде.</span><span class="sxs-lookup"><span data-stu-id="918ed-129">Using the descriptions in the following table, replace the values in the code example with values that match your environment.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="918ed-130">Параметр</span><span class="sxs-lookup"><span data-stu-id="918ed-130">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="918ed-131">Описание</span><span class="sxs-lookup"><span data-stu-id="918ed-131">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="918ed-132">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="918ed-132">$SERVERNAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="918ed-133">Имя сервера, на который были перемещены отчеты.</span><span class="sxs-lookup"><span data-stu-id="918ed-133">Name of the server to which the Reports were moved.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="918ed-134">$SRSINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="918ed-134">$SRSINSTANCENAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="918ed-135">Имя экземпляра служб SQL Server Reporting Services, которым были перемещены отчеты.</span><span class="sxs-lookup"><span data-stu-id="918ed-135">Name of the instance of SQL Server Reporting Services to which the Reports were moved.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="918ed-136">Возобновление работы веб-сайта администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="918ed-136">Resume the instance of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="918ed-137">На сервере, на котором запущен веб-сайт администрирования и наблюдения, запустите веб-сайт администрирования и наблюдения с помощью консоли диспетчера служб IIS.</span><span class="sxs-lookup"><span data-stu-id="918ed-137">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="918ed-138">Для автоматизации этой процедуры можно использовать Windows PowerShell для выполнения команды, которая похожа на описанную ниже.</span><span class="sxs-lookup"><span data-stu-id="918ed-138">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    <span data-ttu-id="918ed-139">**Примечание**  Для выполнения этой команды необходимо добавить в текущий экземпляр Windows PowerShell модуль IIS для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="918ed-139">**Note** To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

     



## <span data-ttu-id="918ed-140">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="918ed-140">Related topics</span></span>


[<span data-ttu-id="918ed-141">Настройка отчетов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="918ed-141">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="918ed-142">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="918ed-142">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="918ed-143">Перенос компонентов MBAM 2.5 на другой сервер</span><span class="sxs-lookup"><span data-stu-id="918ed-143">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 
## <span data-ttu-id="918ed-144">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="918ed-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="918ed-145">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="918ed-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="918ed-146">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="918ed-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





