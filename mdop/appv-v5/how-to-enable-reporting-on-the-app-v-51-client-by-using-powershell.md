---
title: Порядок включения отчетов в клиенте App-V 5.1 с помощью PowerShell
description: Порядок включения отчетов в клиенте App-V 5.1 с помощью PowerShell
author: dansimp
ms.assetid: c4c58be6-cc50-44f6-bf4f-8346fc5d0c0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1d8c0d5e1930020ed1ce354f806f8917a9644e02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814072"
---
# <span data-ttu-id="f3027-103">Порядок включения отчетов в клиенте App-V 5.1 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3027-103">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>


<span data-ttu-id="f3027-104">Чтобы настроить приложение App-V 5,1 для создания отчетов, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f3027-104">Use the following procedure to configure the App-V 5.1 for reporting.</span></span>

**<span data-ttu-id="f3027-105">Настройка компьютера с клиентским приложением App-V 5,1 для создания отчетов</span><span class="sxs-lookup"><span data-stu-id="f3027-105">To configure the computer running the App-V 5.1 client for reporting</span></span>**

1. <span data-ttu-id="f3027-106">Установите клиент App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="f3027-106">Install the App-V 5.1 client.</span></span> <span data-ttu-id="f3027-107">Дополнительные сведения об установке клиента см. в разделе [развертывание клиента App-V](how-to-deploy-the-app-v-client-51gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="f3027-107">For more information about installing the client see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md).</span></span>

2. <span data-ttu-id="f3027-108">После установки клиента App-V 5,1 с помощью PowerShell **Set-AppvClientConfiguration** настройте соответствующие параметры конфигурации отчетов.</span><span class="sxs-lookup"><span data-stu-id="f3027-108">After you have installed the App-V 5.1 client, use the **Set-AppvClientConfiguration** PowerShell to configure appropriate Reporting Configuration settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f3027-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="f3027-109">Setting</span></span></th>
   <th align="left"><span data-ttu-id="f3027-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f3027-110">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f3027-111">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="f3027-111">ReportingEnabled</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f3027-112">Позволяет клиенту возвращать данные на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="f3027-112">Enables the client to return information to a reporting server.</span></span> <span data-ttu-id="f3027-113">Этот параметр необходим для того, чтобы клиент собирал данные отчета на клиенте.</span><span class="sxs-lookup"><span data-stu-id="f3027-113">This setting is required for the client to collect the reporting data on the client.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f3027-114">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="f3027-114">ReportingServerURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f3027-115">Задает расположение на сервере отчетов, на котором сохраняются сведения о клиенте.</span><span class="sxs-lookup"><span data-stu-id="f3027-115">Specifies the location on the reporting server where client information is saved.</span></span> <span data-ttu-id="f3027-116">Например, http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt; .</span><span class="sxs-lookup"><span data-stu-id="f3027-116">For example, http://&lt;reportingservername&gt;:&lt;reportingportnumber&gt;.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="f3027-117">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f3027-117">Note</span></span></strong><br/><p><span data-ttu-id="f3027-118">Номер порта, назначенный во время настройки сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="f3027-118">This is the port number that was assigned during the Reporting Server setup</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f3027-119">Время начала отчета</span><span class="sxs-lookup"><span data-stu-id="f3027-119">Reporting Start Time</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f3027-120">Задается запланировать клиент для автоматической отправки данных на сервер.</span><span class="sxs-lookup"><span data-stu-id="f3027-120">This is set to schedule the client to automatically send the data to the server.</span></span> <span data-ttu-id="f3027-121">Этот параметр укажет время, когда данные отчета будут начинаться с начала отправки.</span><span class="sxs-lookup"><span data-stu-id="f3027-121">This setting will indicate the hour at which the reporting data will start to send.</span></span> <span data-ttu-id="f3027-122">Он представлен в 24-часовом формате и займет число от 0-23.</span><span class="sxs-lookup"><span data-stu-id="f3027-122">It is in the 24 hour format and will take a number between 0-23.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f3027-123">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="f3027-123">ReportingRandomDelay</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f3027-124">Указывает максимальную задержку (в минутах) для данных, отправляемых на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="f3027-124">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="f3027-125">При запуске запланированной задачи клиент создает произвольную задержку от 0 до ReportingRandomDelay и ждет указанное время перед отправкой данных.</span><span class="sxs-lookup"><span data-stu-id="f3027-125">When the scheduled task is started, the client generates a random delay between 0 and ReportingRandomDelay and will wait the specified duration before sending data.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f3027-126">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="f3027-126">ReportingInterval</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f3027-127">Указывает интервал повтора, который будет использоваться клиентом для повторной отправки данных на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="f3027-127">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f3027-128">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="f3027-128">ReportingDataCacheLimit</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f3027-129">Задает максимальный размер кэша XML в мегабайтах (МБ) для хранения сведений о отчетах.</span><span class="sxs-lookup"><span data-stu-id="f3027-129">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="f3027-130">Размер применяется к кэшу в памяти.</span><span class="sxs-lookup"><span data-stu-id="f3027-130">The size applies to the cache in memory.</span></span> <span data-ttu-id="f3027-131">По достижении этого предела файл журнала будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="f3027-131">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f3027-132">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="f3027-132">ReportingDataBlockSize</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f3027-133">Задает максимальный размер кэша XML в мегабайтах (МБ) для хранения сведений о отчетах.</span><span class="sxs-lookup"><span data-stu-id="f3027-133">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="f3027-134">Размер применяется к кэшу в памяти.</span><span class="sxs-lookup"><span data-stu-id="f3027-134">The size applies to the cache in memory.</span></span> <span data-ttu-id="f3027-135">По достижении этого предела файл журнала будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="f3027-135">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="f3027-136">После настройки соответствующих параметров компьютер, на котором работает клиент App-V 5,1, будет автоматически собирать данные и отправлять данные обратно на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="f3027-136">After the appropriate settings have been configured, the computer running the App-V 5.1 client will automatically collect data and will send the data back to the reporting server.</span></span>

   <span data-ttu-id="f3027-137">Кроме того, администраторы могут вручную отправлять данные по запросу с помощью командлета PowerShell **Send-AppvClientReport** .</span><span class="sxs-lookup"><span data-stu-id="f3027-137">Additionally, administrators can manually send the data back in an on-demand manner using the **Send-AppvClientReport** PowerShell cmdlet.</span></span>

   <span data-ttu-id="f3027-138">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="f3027-138">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f3027-139">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="f3027-139">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f3027-140">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="f3027-140">Got an App-V issue?</span></span>** <span data-ttu-id="f3027-141">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f3027-141">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f3027-142">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f3027-142">Related topics</span></span>


[<span data-ttu-id="f3027-143">Администрирование App-V 5.1 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3027-143">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)








