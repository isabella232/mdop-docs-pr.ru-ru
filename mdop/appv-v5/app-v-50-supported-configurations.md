---
title: Поддерживаемые конфигурации в App-V 5.0
description: Поддерживаемые конфигурации в App-V 5.0
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814789"
---
# <span data-ttu-id="8379a-103">Поддерживаемые конфигурации в App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="8379a-103">App-V 5.0 Supported Configurations</span></span>


<span data-ttu-id="8379a-104">В этой статье указаны требования, необходимые для установки и запуска Microsoft Application Virtualization (App-V) 5,0 в среде.</span><span class="sxs-lookup"><span data-stu-id="8379a-104">This topic specifies the requirements that are necessary to install and run Microsoft Application Virtualization (App-V) 5.0 in your environment.</span></span>

**<span data-ttu-id="8379a-105">Важно.</span><span class="sxs-lookup"><span data-stu-id="8379a-105">Important</span></span>**  
<span data-ttu-id="8379a-106">**Поддерживаемые конфигурации, описанные в этой статье, относятся только к приложению App-V 5,0**.</span><span class="sxs-lookup"><span data-stu-id="8379a-106">**The supported configurations in this article apply only to App-V 5.0**.</span></span> <span data-ttu-id="8379a-107">Поддерживаемые конфигурации, которые относятся к пакетам обновления App-V 5,0, можно найти на веб-страницах ниже.</span><span class="sxs-lookup"><span data-stu-id="8379a-107">For supported configurations that apply to App-V 5.0 Service Packs, see the following web pages:</span></span>

-   [<span data-ttu-id="8379a-108">Новые возможности в App-V 5.0 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="8379a-108">What's new in App-V 5.0 SP1</span></span>](whats-new-in-app-v-50-sp1.md)

-   [<span data-ttu-id="8379a-109">Сведения об App-V 5.0 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="8379a-109">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

-   [<span data-ttu-id="8379a-110">Поддерживаемые конфигурации App-V 5.0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="8379a-110">App-V 5.0 SP3 Supported Configurations</span></span>](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> <span data-ttu-id="8379a-111">Требования к серверной системе для App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="8379a-111">App-V 5.0 server system requirements</span></span>


**<span data-ttu-id="8379a-112">Важно.</span><span class="sxs-lookup"><span data-stu-id="8379a-112">Important</span></span>**  
<span data-ttu-id="8379a-113">Сервер App-V 5,0 не поддерживает указанные ниже сценарии.</span><span class="sxs-lookup"><span data-stu-id="8379a-113">The App-V 5.0 server does not support the following scenarios:</span></span>



-   <span data-ttu-id="8379a-114">Развертывание на компьютере, на котором запущен Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="8379a-114">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="8379a-115">Развертывание на компьютере, на котором установлена предыдущая версия App-V 5,0 Server.</span><span class="sxs-lookup"><span data-stu-id="8379a-115">Deployment to a computer that runs a previous version of App-V 5.0 server components.</span></span>

    **<span data-ttu-id="8379a-116">Примечание.</span><span class="sxs-lookup"><span data-stu-id="8379a-116">Note</span></span>**  
    <span data-ttu-id="8379a-117">Вы можете установить App-V 5,0 рядом с сервером App-V 4,5 Lightweight Streaming Server (LWS).</span><span class="sxs-lookup"><span data-stu-id="8379a-117">You can install App-V 5.0 side-by-side with the App-V 4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="8379a-118">Развертывание App-V 5,0 с помощью службы управления виртуализацией приложений App-V 4,5 (HWS) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8379a-118">Deployment of App-V 5.0 side-by-side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>



-   <span data-ttu-id="8379a-119">Развертывание на компьютере, на котором запущен Microsoft SQL Server, Экспресс-выпуск.</span><span class="sxs-lookup"><span data-stu-id="8379a-119">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="8379a-120">Удаленное развертывание базы данных сервера управления или базы данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="8379a-120">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="8379a-121">Чтобы успешно установить базу данных, необходимо запустить установщик прямо на компьютере с Microsoft SQL.</span><span class="sxs-lookup"><span data-stu-id="8379a-121">The installer must be run directly on the computer running Microsoft SQL for the database installation to succeed.</span></span>

-   <span data-ttu-id="8379a-122">Развертывание на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="8379a-122">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="8379a-123">Короткие пути не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="8379a-123">Short paths are not supported.</span></span> <span data-ttu-id="8379a-124">Если вы планируете использовать короткий путь, вы должны создать новый том.</span><span class="sxs-lookup"><span data-stu-id="8379a-124">If you plan to use a short path you must create a new volume.</span></span>

### <span data-ttu-id="8379a-125">Требования к операционной системе для сервера управления</span><span class="sxs-lookup"><span data-stu-id="8379a-125">Management Server operating system requirements</span></span>

<span data-ttu-id="8379a-126">В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8379a-126">The following table lists the operating systems that are supported for the App-V 5.0 management server installation.</span></span>

**<span data-ttu-id="8379a-127">Примечание.</span><span class="sxs-lookup"><span data-stu-id="8379a-127">Note</span></span>**  
<span data-ttu-id="8379a-128">Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="8379a-128">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8379a-129">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8379a-129">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8379a-130">Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8379a-130">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8379a-131">Операционная система</span><span class="sxs-lookup"><span data-stu-id="8379a-131">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8379a-132">Выпуск</span><span class="sxs-lookup"><span data-stu-id="8379a-132">Edition</span></span></th>
<th align="left"><span data-ttu-id="8379a-133">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="8379a-133">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8379a-134">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="8379a-134">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8379a-135">Microsoft Windows Server 2008 (стандартный, корпоративный, центр обработки данных или веб-сервер)</span><span class="sxs-lookup"><span data-stu-id="8379a-135">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-136">ОС</span><span class="sxs-lookup"><span data-stu-id="8379a-136">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-137">SP1 и более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="8379a-137">SP1 and higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-138">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-138">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8379a-139">Microsoft Windows Server 2012 (стандартный центр обработки данных)</span><span class="sxs-lookup"><span data-stu-id="8379a-139">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8379a-140">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-140">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8379a-141">Microsoft Windows Server 2012 (стандартный центр обработки данных)</span><span class="sxs-lookup"><span data-stu-id="8379a-141">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-142">ОС</span><span class="sxs-lookup"><span data-stu-id="8379a-142">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8379a-143">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-143">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="8379a-144">Важно.</span><span class="sxs-lookup"><span data-stu-id="8379a-144">Important</span></span>**  
<span data-ttu-id="8379a-145">Развертывание роли сервера управления на компьютере с включенным удаленным доступом к рабочему столу не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8379a-145">Deployment of the management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>



### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="8379a-146">Требования к оборудованию сервера управления</span><span class="sxs-lookup"><span data-stu-id="8379a-146">Management Server hardware requirements</span></span>

-   <span data-ttu-id="8379a-147">Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор</span><span class="sxs-lookup"><span data-stu-id="8379a-147">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="8379a-148">ОЗУ — 1 ГБ ОЗУ (64-разр.)</span><span class="sxs-lookup"><span data-stu-id="8379a-148">RAM— 1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="8379a-149">Место на диске — 200 МБАЙТ свободного места на жестком диске, не включая каталог содержимого.</span><span class="sxs-lookup"><span data-stu-id="8379a-149">Disk space—200 MB available hard disk space, not including the content directory.</span></span>

### <span data-ttu-id="8379a-150">Требования к операционной системе сервера публикаций</span><span class="sxs-lookup"><span data-stu-id="8379a-150">Publishing Server operating system requirements</span></span>

<span data-ttu-id="8379a-151">В таблице ниже перечислены операционные системы, которые поддерживаются в установке сервера публикаций App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8379a-151">The following table lists the operating systems that are supported for the App-V 5.0 publishing server installation.</span></span>

**<span data-ttu-id="8379a-152">Примечание.</span><span class="sxs-lookup"><span data-stu-id="8379a-152">Note</span></span>**  
<span data-ttu-id="8379a-153">Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="8379a-153">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8379a-154">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8379a-154">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8379a-155">Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8379a-155">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8379a-156">Операционная система</span><span class="sxs-lookup"><span data-stu-id="8379a-156">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8379a-157">Выпуск</span><span class="sxs-lookup"><span data-stu-id="8379a-157">Edition</span></span></th>
<th align="left"><span data-ttu-id="8379a-158">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="8379a-158">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8379a-159">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="8379a-159">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8379a-160">Microsoft Windows Server 2008 (стандартный, корпоративный, центр обработки данных или веб-сервер)</span><span class="sxs-lookup"><span data-stu-id="8379a-160">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-161">ОС</span><span class="sxs-lookup"><span data-stu-id="8379a-161">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8379a-162">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-162">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8379a-163">Microsoft Windows Server 2012 (стандартный центр обработки данных)</span><span class="sxs-lookup"><span data-stu-id="8379a-163">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8379a-164">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-164">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8379a-165">Microsoft Windows Server 2012 (стандартный центр обработки данных)</span><span class="sxs-lookup"><span data-stu-id="8379a-165">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-166">ОС</span><span class="sxs-lookup"><span data-stu-id="8379a-166">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8379a-167">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-167">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="8379a-168">Требования к оборудованию сервера публикаций</span><span class="sxs-lookup"><span data-stu-id="8379a-168">Publishing Server hardware requirements</span></span>

-   <span data-ttu-id="8379a-169">Процессор – 1,4 ГГц или более мощный.</span><span class="sxs-lookup"><span data-stu-id="8379a-169">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="8379a-170">64-разрядный процессор (x64)</span><span class="sxs-lookup"><span data-stu-id="8379a-170">64-bit (x64) processor</span></span>

-   <span data-ttu-id="8379a-171">ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="8379a-171">RAM— 2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="8379a-172">Место на диске — 200 МБАЙТ свободного места на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="8379a-172">Disk space—200 MB available hard disk space.</span></span> <span data-ttu-id="8379a-173">не включает каталог контента</span><span class="sxs-lookup"><span data-stu-id="8379a-173">not including content directory</span></span>

### <span data-ttu-id="8379a-174">Требования к операционной системе сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="8379a-174">Reporting Server operating system requirements</span></span>

<span data-ttu-id="8379a-175">В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера Reporting Server App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8379a-175">The following table lists the operating systems that are supported for the App-V 5.0 reporting server installation.</span></span>

**<span data-ttu-id="8379a-176">Примечание.</span><span class="sxs-lookup"><span data-stu-id="8379a-176">Note</span></span>**  
<span data-ttu-id="8379a-177">Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="8379a-177">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8379a-178">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8379a-178">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8379a-179">Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8379a-179">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8379a-180">Операционная система</span><span class="sxs-lookup"><span data-stu-id="8379a-180">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8379a-181">Выпуск</span><span class="sxs-lookup"><span data-stu-id="8379a-181">Edition</span></span></th>
<th align="left"><span data-ttu-id="8379a-182">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="8379a-182">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="8379a-183">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="8379a-183">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8379a-184">Microsoft Windows Server 2008 (стандартный, корпоративный, центр обработки данных или веб-сервер)</span><span class="sxs-lookup"><span data-stu-id="8379a-184">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-185">ОС</span><span class="sxs-lookup"><span data-stu-id="8379a-185">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8379a-186">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-186">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8379a-187">Microsoft Windows Server 2012 (стандартный центр обработки данных)</span><span class="sxs-lookup"><span data-stu-id="8379a-187">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8379a-188">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8379a-189">Microsoft Windows Server 2012 (стандартный центр обработки данных)</span><span class="sxs-lookup"><span data-stu-id="8379a-189">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-190">ОС</span><span class="sxs-lookup"><span data-stu-id="8379a-190">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8379a-191">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-191">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="8379a-192">Требования к оборудованию сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="8379a-192">Reporting Server hardware requirements</span></span>

-   <span data-ttu-id="8379a-193">Процессор – 1,4 ГГц или более мощный.</span><span class="sxs-lookup"><span data-stu-id="8379a-193">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="8379a-194">64-разрядный процессор (x64)</span><span class="sxs-lookup"><span data-stu-id="8379a-194">64-bit (x64) processor</span></span>

-   <span data-ttu-id="8379a-195">ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="8379a-195">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="8379a-196">Место на диске — 200 МБАЙТ свободного места на жестком диске</span><span class="sxs-lookup"><span data-stu-id="8379a-196">Disk space—200 MB available hard disk space</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="8379a-197">Требования к базам данных SQL Server</span><span class="sxs-lookup"><span data-stu-id="8379a-197">SQL Server database requirements</span></span>

<span data-ttu-id="8379a-198">В следующей таблице перечислены версии SQL Server, которые поддерживаются для базы данных App-V 5,0 и сервера.</span><span class="sxs-lookup"><span data-stu-id="8379a-198">The following table lists the SQL Server versions that are supported for the App-V 5.0 database and server installation.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8379a-199">Тип сервера App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="8379a-199">App-V 5.0 server type</span></span></th>
<th align="left"><span data-ttu-id="8379a-200">Версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="8379a-200">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="8379a-201">Выпуск</span><span class="sxs-lookup"><span data-stu-id="8379a-201">Edition</span></span></th>
<th align="left"><span data-ttu-id="8379a-202">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="8379a-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8379a-203">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="8379a-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8379a-204">Управление и отчетность</span><span class="sxs-lookup"><span data-stu-id="8379a-204">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-205">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="8379a-205">Microsoft SQL Server 2008</span></span></p>
<p><span data-ttu-id="8379a-206">(Standard, предприятие, центр обработки данных или выпуск разработчика с помощью следующего компонента: <strong> Службы ядра СУБД </strong> .)</span><span class="sxs-lookup"><span data-stu-id="8379a-206">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8379a-207">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8379a-208">Управление и отчетность</span><span class="sxs-lookup"><span data-stu-id="8379a-208">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-209">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="8379a-209">Microsoft SQL Server 2008</span></span> </p>
<p><span data-ttu-id="8379a-210">(Standard, предприятие, центр обработки данных или выпуск разработчика с помощью следующего компонента: <strong> Службы ядра СУБД </strong> .)</span><span class="sxs-lookup"><span data-stu-id="8379a-210">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-211">ОС</span><span class="sxs-lookup"><span data-stu-id="8379a-211">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-212">SP2</span><span class="sxs-lookup"><span data-stu-id="8379a-212">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-213">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-213">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8379a-214">Управление и отчетность</span><span class="sxs-lookup"><span data-stu-id="8379a-214">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-215">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="8379a-215">Microsoft SQL Server 2012</span></span></p>
<p><span data-ttu-id="8379a-216">(Standard, предприятие, центр обработки данных или выпуск разработчика с помощью следующего компонента: <strong> Службы ядра СУБД </strong> .)</span><span class="sxs-lookup"><span data-stu-id="8379a-216">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8379a-217">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-217">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> <span data-ttu-id="8379a-218">Требования к системе клиента App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="8379a-218">App-V 5.0 client system requirements</span></span>


<span data-ttu-id="8379a-219">В таблице ниже перечислены операционные системы, которые поддерживаются при установке клиента App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8379a-219">The following table lists the operating systems that are supported for the App-V 5.0 client installation.</span></span>

**<span data-ttu-id="8379a-220">Примечание.</span><span class="sxs-lookup"><span data-stu-id="8379a-220">Note</span></span>**  
<span data-ttu-id="8379a-221">Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="8379a-221">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8379a-222">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8379a-222">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8379a-223">Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8379a-223">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8379a-224">Операционная система</span><span class="sxs-lookup"><span data-stu-id="8379a-224">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8379a-225">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="8379a-225">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8379a-226">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="8379a-226">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8379a-227">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="8379a-227">Microsoft Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-228">SP1</span><span class="sxs-lookup"><span data-stu-id="8379a-228">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-229">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-229">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8379a-230">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="8379a-230">Microsoft Windows 8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8379a-231">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-231">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="8379a-232">Важно.</span><span class="sxs-lookup"><span data-stu-id="8379a-232">Important</span></span></strong><br/><p><span data-ttu-id="8379a-233">Windows 8,1 поддерживается только приложением App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="8379a-233">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="8379a-234">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8379a-234">Windows 8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8379a-235">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-235">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="8379a-236">Следующие сценарии установки клиента App-V не поддерживаются, за исключением случаев, указанных ниже.</span><span class="sxs-lookup"><span data-stu-id="8379a-236">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="8379a-237">Компьютеры под управлением Windows Server</span><span class="sxs-lookup"><span data-stu-id="8379a-237">Computers that run Windows Server</span></span>

-   <span data-ttu-id="8379a-238">Компьютеры под управлением App-V 4,6 SP1 или более ранних версий</span><span class="sxs-lookup"><span data-stu-id="8379a-238">Computers that run App-V 4.6 SP1 or earlier versions</span></span>

-   <span data-ttu-id="8379a-239">Клиент служб удаленных рабочих столов App-V 5,0 поддерживается только для серверов с поддержкой служб удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="8379a-239">The App-V 5.0 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="client-hardware-requirements-"></a><span data-ttu-id="8379a-240">Требования к оборудованию клиента</span><span class="sxs-lookup"><span data-stu-id="8379a-240">Client hardware requirements</span></span>

<span data-ttu-id="8379a-241">В списке ниже показана конфигурация оборудования, поддерживаемая установкой клиента App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8379a-241">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="8379a-242">Процессор — процессор с тактовой частотой 1,4 ГГц или более 32 мощный (x86) или 64-bit (x64)</span><span class="sxs-lookup"><span data-stu-id="8379a-242">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="8379a-243">ОЗУ — 1 ГБ (32-разрядная версия) или 2 ГБ (64-разр.)</span><span class="sxs-lookup"><span data-stu-id="8379a-243">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="8379a-244">Диск — 100 МБАЙТ для установки, не включая пространство на диске, используемое виртуализированными приложениями.</span><span class="sxs-lookup"><span data-stu-id="8379a-244">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> <span data-ttu-id="8379a-245">Требования к клиентской системе для удаленных рабочих столов для App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="8379a-245">App-V 5.0 Remote Desktop client system requirements</span></span>


<span data-ttu-id="8379a-246">В приведенной ниже таблице перечислены операционные системы, которые поддерживаются при установке клиента для удаленного рабочего стола App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8379a-246">The following table lists the operating systems that are supported for App-V 5.0 Remote Desktop client installation.</span></span>

**<span data-ttu-id="8379a-247">Примечание.</span><span class="sxs-lookup"><span data-stu-id="8379a-247">Note</span></span>**  
<span data-ttu-id="8379a-248">Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="8379a-248">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8379a-249">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8379a-249">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8379a-250">Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8379a-250">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<span data-ttu-id="8379a-251">Выпуск операционной системы, пакет обновления Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8379a-251">Operating system Edition Service pack Microsoft Windows Server 2008</span></span>

<span data-ttu-id="8379a-252">ОС</span><span class="sxs-lookup"><span data-stu-id="8379a-252">R2</span></span>

<span data-ttu-id="8379a-253">SP1</span><span class="sxs-lookup"><span data-stu-id="8379a-253">SP1</span></span>

<span data-ttu-id="8379a-254">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8379a-254">Microsoft Windows Server 2012</span></span>

**<span data-ttu-id="8379a-255">Важно.</span><span class="sxs-lookup"><span data-stu-id="8379a-255">Important</span></span>**  
<span data-ttu-id="8379a-256">Windows Server 2012 R2 поддерживается только приложением App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="8379a-256">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span>



<span data-ttu-id="8379a-257">Microsoft Windows Server 2012 (стандартный центр обработки данных)</span><span class="sxs-lookup"><span data-stu-id="8379a-257">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span>

<span data-ttu-id="8379a-258">ОС</span><span class="sxs-lookup"><span data-stu-id="8379a-258">R2</span></span>

<span data-ttu-id="8379a-259">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-259">64-bit</span></span>



### <a href="" id="remote-desktop-client-hardware-requirements-"></a><span data-ttu-id="8379a-260">Требования к оборудованию клиента удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="8379a-260">Remote Desktop client hardware requirements</span></span>

<span data-ttu-id="8379a-261">В списке ниже показана конфигурация оборудования, поддерживаемая установкой клиента App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8379a-261">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="8379a-262">Процессор — процессор с тактовой частотой 1,4 ГГц или более 32 мощный (x86) или 64-bit (x64)</span><span class="sxs-lookup"><span data-stu-id="8379a-262">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="8379a-263">ОЗУ — 1 ГБ (32-разрядная версия) или 2 ГБ (64-разр.)</span><span class="sxs-lookup"><span data-stu-id="8379a-263">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="8379a-264">Диск — 100 МБАЙТ для установки, не включая пространство на диске, используемое виртуализированными приложениями.</span><span class="sxs-lookup"><span data-stu-id="8379a-264">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> <span data-ttu-id="8379a-265">Требования к системе Sequencer для App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="8379a-265">App-V 5.0 Sequencer system requirements</span></span>


<span data-ttu-id="8379a-266">В следующей таблице перечислены операционные системы, которые поддерживаются при установке App-V 5,0 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="8379a-266">The following table lists the operating systems that are supported for App-V 5.0 Sequencer installation.</span></span>

**<span data-ttu-id="8379a-267">Примечание.</span><span class="sxs-lookup"><span data-stu-id="8379a-267">Note</span></span>**  
<span data-ttu-id="8379a-268">Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="8379a-268">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8379a-269">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8379a-269">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8379a-270">Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8379a-270">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8379a-271">Операционная система</span><span class="sxs-lookup"><span data-stu-id="8379a-271">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8379a-272">Выпуск</span><span class="sxs-lookup"><span data-stu-id="8379a-272">Edition</span></span></th>
<th align="left"><span data-ttu-id="8379a-273">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="8379a-273">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8379a-274">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="8379a-274">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8379a-275">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="8379a-275">Microsoft Windows 7</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8379a-276">SP1</span><span class="sxs-lookup"><span data-stu-id="8379a-276">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-277">32- и 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-277">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8379a-278">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="8379a-278">Microsoft Windows 8</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8379a-279">32- и 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-279">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="8379a-280">Важно.</span><span class="sxs-lookup"><span data-stu-id="8379a-280">Important</span></span></strong><br/><p><span data-ttu-id="8379a-281">Windows 8,1 поддерживается только приложением App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="8379a-281">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="8379a-282">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8379a-282">Windows 8.1</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8379a-283">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-283">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8379a-284">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8379a-284">Microsoft Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-285">ОС</span><span class="sxs-lookup"><span data-stu-id="8379a-285">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-286">SP1</span><span class="sxs-lookup"><span data-stu-id="8379a-286">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-287">32- и 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-287">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8379a-288">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8379a-288">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8379a-289">32- и 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-289">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong><span data-ttu-id="8379a-290">Важно.</span><span class="sxs-lookup"><span data-stu-id="8379a-290">Important</span></span></strong><br/><p><span data-ttu-id="8379a-291">Windows Server 2012 R2 поддерживается только приложением App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="8379a-291">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="8379a-292">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8379a-292">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="8379a-293">ОС</span><span class="sxs-lookup"><span data-stu-id="8379a-293">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8379a-294">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="8379a-294">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="8379a-295">Поддерживаемые версии System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8379a-295">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="8379a-296">Вы можете использовать Microsoft System Center 2012 Configuration Manager или System Center 2012 R2 Configuration Manager для управления виртуальными приложениями App-V, отчетами и другими функциями.</span><span class="sxs-lookup"><span data-stu-id="8379a-296">You can use Microsoft System Center 2012 Configuration Manager or System Center 2012 R2 Configuration Manager to manage App-V virtual applications, reporting, and other functions.</span></span> <span data-ttu-id="8379a-297">В следующей таблице перечислены поддерживаемые версии Configuration Manager для каждой применимой версии App-V.</span><span class="sxs-lookup"><span data-stu-id="8379a-297">The following table lists the supported versions of Configuration Manager for each applicable version of App-V.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8379a-298">Поддерживаемая версия Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8379a-298">Supported Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="8379a-299">Версия App-V</span><span class="sxs-lookup"><span data-stu-id="8379a-299">App-V version</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8379a-300">Microsoft System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8379a-300">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="8379a-301">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="8379a-301">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="8379a-302">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="8379a-302">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="8379a-303">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="8379a-303">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8379a-304">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8379a-304">System Center 2012 R2 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="8379a-305">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="8379a-305">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="8379a-306">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="8379a-306">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="8379a-307">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="8379a-307">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="8379a-308">Дополнительные сведения о том, как Configuration Manager интегрируется с App-V, можно найти в разделе [Планирование интеграции App-v с Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="8379a-308">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="8379a-309">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8379a-309">Related topics</span></span>


[<span data-ttu-id="8379a-310">Планирование развертывания App-V</span><span class="sxs-lookup"><span data-stu-id="8379a-310">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="8379a-311">Предварительные требования App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="8379a-311">App-V 5.0 Prerequisites</span></span>](app-v-50-prerequisites.md)









