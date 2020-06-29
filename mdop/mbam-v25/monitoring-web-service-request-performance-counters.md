---
title: Отслеживание счетчиков производительности запросов веб-службы
description: Отслеживание счетчиков производительности запросов веб-службы
author: dansimp
ms.assetid: bdb812a1-465a-4098-b4c0-cb99890d1b0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2db96e3375562b48d289ea5a21dc7e89b800d1ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823879"
---
# <span data-ttu-id="0e557-103">Отслеживание счетчиков производительности запросов веб-службы</span><span class="sxs-lookup"><span data-stu-id="0e557-103">Monitoring Web Service Request Performance Counters</span></span>


<span data-ttu-id="0e557-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) обеспечивает счетчики производительности, которые записывают производительность запросов, которые отправляются в указанные ниже веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0e557-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides performance counters that record the performance of requests that are sent to the following web services:</span></span>

-   <span data-ttu-id="0e557-105">**StatusReportingService. svc** — служба, принимающая запросы на состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="0e557-105">**StatusReportingService.svc** – service that receives requests for compliance status</span></span>

-   <span data-ttu-id="0e557-106">**CoreService. svc** — служба, принимающая запросы на попытки восстановления ключа</span><span class="sxs-lookup"><span data-stu-id="0e557-106">**CoreService.svc** – service that receives requests for key recovery attempts</span></span>

## <span data-ttu-id="0e557-107">Счетчики производительности, предоставляемые MBAM</span><span class="sxs-lookup"><span data-stu-id="0e557-107">Performance counters that MBAM provides</span></span>


<span data-ttu-id="0e557-108">MBAM предоставляет следующие счетчики производительности для каждого из открытых методов, реализуемых его веб-службами StatusReportingService и CoreService.</span><span class="sxs-lookup"><span data-stu-id="0e557-108">MBAM provides the following performance counters for each of the public methods that is implemented by its StatusReportingService and CoreService web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0e557-109">Тип счетчика производительности</span><span class="sxs-lookup"><span data-stu-id="0e557-109">Type of performance counter</span></span></th>
<th align="left"><span data-ttu-id="0e557-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0e557-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0e557-111">Общее количество запросов</span><span class="sxs-lookup"><span data-stu-id="0e557-111">Total number of requests</span></span></p></td>
<td align="left"><p><span data-ttu-id="0e557-112">Обеспечивает счетчик приращений, который начинается с нуля при запуске или перезапуске сервера.</span><span class="sxs-lookup"><span data-stu-id="0e557-112">Provides an incrementing count that starts from zero when the server is started or restarted.</span></span></p>
<p><span data-ttu-id="0e557-113">Общие сведения об активности системы.</span><span class="sxs-lookup"><span data-stu-id="0e557-113">Provides an overall view of system activity.</span></span> <span data-ttu-id="0e557-114">Можно отслеживать с помощью автоматизированных средств для обеспечения работоспособности сервера и проверки того, что счетчик постоянно увеличивается в течение определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="0e557-114">Can be monitored by automated tools to ensure the health of the server and to validate that the counter continually increments over a specified period of time.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0e557-115">Количество запросов в секунду</span><span class="sxs-lookup"><span data-stu-id="0e557-115">Requests per second</span></span></p></td>
<td align="left"><p><span data-ttu-id="0e557-116">Показывает текущую пропускную способность сервера MBAM, так как она поддерживает базу клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="0e557-116">Indicates the current throughput of the MBAM Server as it supports the MBAM client base.</span></span></p>
<p><span data-ttu-id="0e557-117">Позволяет администраторам сайтов выполнять указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="0e557-117">Enables site administrators to:</span></span></p>
<ul>
<li><p><span data-ttu-id="0e557-118">Вычисление среднего количества запросов в секунду на основе количества клиентов MBAM и частоту их создания.</span><span class="sxs-lookup"><span data-stu-id="0e557-118">Calculate the average number of requests per second, based on the number of MBAM Clients and their reporting frequency.</span></span></p></li>
<li><p><span data-ttu-id="0e557-119">Проверка числа корреляции запросов в секунду на общее число запросов в секунду с вычисленным средним значением.</span><span class="sxs-lookup"><span data-stu-id="0e557-119">Validate that the number of requests per second broadly correlates with the calculated average number of requests per second.</span></span> <span data-ttu-id="0e557-120">Значительная вариация может указывать на то, что клиент MBAM не установлен на процент клиентской части, а также в том, что объект групповой политики MBAM не был успешно развернут.</span><span class="sxs-lookup"><span data-stu-id="0e557-120">A significant variance can indicate that the MBAM Client isn't installed on a percentage of the client base or that an MBAM Group Policy Object hasn't been successfully deployed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0e557-121">Длительность запроса</span><span class="sxs-lookup"><span data-stu-id="0e557-121">Request duration</span></span></p></td>
<td align="left"><p><span data-ttu-id="0e557-122">Записывает продолжительность запросов в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="0e557-122">Records the duration of requests in milliseconds.</span></span></p>
<p><span data-ttu-id="0e557-123">Несмотря на то, что этот счетчик обновляется с учетом длительности каждого запроса, системный монитор Windows выдает его только периодически (обычно каждую секунду), так что вы можете увидеть определенную вариативность значения.</span><span class="sxs-lookup"><span data-stu-id="0e557-123">Although this counter is updated with the duration of each request, Windows Performance Monitor samples it only periodically (typically every second), so you might see some variability in the value.</span></span> <span data-ttu-id="0e557-124">По этой причине следует использовать среднее значение, отображаемое монитором производительности.</span><span class="sxs-lookup"><span data-stu-id="0e557-124">For this reason, consider using the average value displayed by Performance Monitor.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0e557-125">Результаты и рекомендации для счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="0e557-125">Performance counter results and recommendations</span></span>


<span data-ttu-id="0e557-126">По мере добавления новых клиентов MBAM на сервер MBAM с запасной емкостью вы должны увеличивать количество запросов в секунду.</span><span class="sxs-lookup"><span data-stu-id="0e557-126">As you add new MBAM Clients to an MBAM Server with spare capacity, expect to see an increase in the number of requests per second.</span></span> <span data-ttu-id="0e557-127">Это увеличение будет пропорционально количеству новых клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="0e557-127">This increase will be proportional to the number of new client computers.</span></span> <span data-ttu-id="0e557-128">Средняя длительность запроса останется относительно статической.</span><span class="sxs-lookup"><span data-stu-id="0e557-128">The average request duration will remain relatively static.</span></span> <span data-ttu-id="0e557-129">Так как сервер приближается к максимальной мощности, запросы в секунду начинают выполняться, а средняя продолжительность запроса начинается дольше.</span><span class="sxs-lookup"><span data-stu-id="0e557-129">As the server nears its maximum capacity, the requests per second start to level out, and the average request duration starts to get longer.</span></span>

<span data-ttu-id="0e557-130">Если вы не уверены в том, что ваши серверы MBAM могут поддерживать клиентскую базу, рассматривайте MBAM на разных семействах клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="0e557-130">If you are concerned about whether your MBAM Servers can support your client base, consider deploying MBAM in phases across different collections of client computers.</span></span> <span data-ttu-id="0e557-131">При развертывании MBAM на каждом семействе клиентских компьютеров мы рекомендуем использовать снимки счетчиков производительности, чтобы увидеть, как именно они влияют на развертывание в каждой новой клиентской коллекции.</span><span class="sxs-lookup"><span data-stu-id="0e557-131">As you deploy MBAM to each collection of client computers, we recommend that you take snapshots of the performance counters to see the relative impact of deploying to each new client collection.</span></span> <span data-ttu-id="0e557-132">Если число запросов в секунду начинается на OFF и средняя длительность запроса увеличивается, рассматривайте инфраструктуру сервера MBAM, выполнив одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="0e557-132">If the number of requests per second starts to level off and the average request duration increases, consider enhancing your MBAM Server infrastructure by doing one of the following:</span></span>

-   <span data-ttu-id="0e557-133">Перемещение базы данных MBAM на выделенный кластер Microsoft SQL Server или SQL Server</span><span class="sxs-lookup"><span data-stu-id="0e557-133">Moving the MBAM database onto a dedicated Microsoft SQL Server or SQL Server cluster</span></span>

-   <span data-ttu-id="0e557-134">Балансировка нагрузки MBAM на нескольких веб-серверах служб Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="0e557-134">Load-balancing MBAM across multiple Internet Information Services (IIS) web servers</span></span>

-   <span data-ttu-id="0e557-135">Развертывание MBAM на более мощном серверном оборудовании</span><span class="sxs-lookup"><span data-stu-id="0e557-135">Deploying MBAM on more powerful server hardware</span></span>

## <span data-ttu-id="0e557-136">Просмотр счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="0e557-136">Viewing performance counters</span></span>


<span data-ttu-id="0e557-137">Рекомендуемым средством просмотра счетчиков производительности MBAM является системный монитор Windows, который поставляется вместе с Windows.</span><span class="sxs-lookup"><span data-stu-id="0e557-137">The recommended tool for viewing MBAM performance counters is Windows Performance Monitor, which comes with Windows.</span></span> <span data-ttu-id="0e557-138">Если вы используете Windows PowerShell, вам не нужно включать эти счетчики, так как они автоматически регистрируются с помощью командлета **Enable** для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0e557-138">If you are using Windows PowerShell, you don’t need to enable the counters before viewing them, as they are automatically registered by the Windows PowerShell **Enable-webapplication** cmdlet.</span></span>

<span data-ttu-id="0e557-139">Подробные инструкции по просмотру счетчиков производительности приведены в разделе [Просмотр счетчиков производительности MBAM](https://go.microsoft.com/fwlink/?LinkId=393457).</span><span class="sxs-lookup"><span data-stu-id="0e557-139">For detailed instructions on how to view performance counters, see [How to View MBAM Performance Counters](https://go.microsoft.com/fwlink/?LinkId=393457).</span></span>



## <span data-ttu-id="0e557-140">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0e557-140">Related topics</span></span>


[<span data-ttu-id="0e557-141">Обслуживание MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0e557-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)

 

 


## <span data-ttu-id="0e557-142">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="0e557-142">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="0e557-143">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="0e557-143">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="0e557-144">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="0e557-144">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>


