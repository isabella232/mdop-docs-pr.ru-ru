---
title: Поддерживаемые конфигурации App-V 5.0 с пакетом обновления 3 (SP3)
description: Поддерживаемые конфигурации App-V 5.0 с пакетом обновления 3 (SP3)
author: dansimp
ms.assetid: 08ced79a-0ed3-43c3-82e7-de01c1f33e81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b5a8858c703add3dc84c7eed4f62aa97e60ec9b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814792"
---
# <span data-ttu-id="78059-103">Поддерживаемые конфигурации App-V 5.0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="78059-103">App-V 5.0 SP3 Supported Configurations</span></span>


<span data-ttu-id="78059-104">В этой статье указаны требования для установки и запуска Microsoft Application Virtualization (App-V) 5,0 SP3 в среде.</span><span class="sxs-lookup"><span data-stu-id="78059-104">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.0 SP3 in your environment.</span></span>

## <span data-ttu-id="78059-105">Требования к системе для App-V Server</span><span class="sxs-lookup"><span data-stu-id="78059-105">App-V Server system requirements</span></span>


<span data-ttu-id="78059-106">В этом разделе перечислены требования к операционной системе и оборудованию для всех серверных компонентов App-V.</span><span class="sxs-lookup"><span data-stu-id="78059-106">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="78059-107">Неподдерживаемые сценарии сервера App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="78059-107">Unsupported App-V 5.0 SP3 Server scenarios</span></span>

<span data-ttu-id="78059-108">Сервер App-V 5,0 с пакетом обновления 3 (SP3) не поддерживает указанные ниже сценарии.</span><span class="sxs-lookup"><span data-stu-id="78059-108">The App-V 5.0 SP3 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="78059-109">Развертывание на компьютере, на котором запущен Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="78059-109">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="78059-110">Развертывание на компьютере, на котором установлена предыдущая версия App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="78059-110">Deployment to a computer that runs a previous version of App-V 5.0 SP3 Server components.</span></span> <span data-ttu-id="78059-111">Вы можете установить приложение App-V 5,0 SP3 рядом с сервером App-V 4.5 облегченного потокового сервера (LWS).</span><span class="sxs-lookup"><span data-stu-id="78059-111">You can install App-V 5.0 SP3 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="78059-112">Развертывание App-V на стороне с сервером (серверная служба управления виртуализацией приложений для App-V 4,5) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="78059-112">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="78059-113">Развертывание на компьютере, на котором запущен Microsoft SQL Server, Экспресс-выпуск.</span><span class="sxs-lookup"><span data-stu-id="78059-113">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="78059-114">Удаленное развертывание базы данных сервера управления или базы данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="78059-114">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="78059-115">Вы должны запустить установщик прямо на компьютере, на котором установлен Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="78059-115">You must run the installer directly on the computer that is running Microsoft SQL Server.</span></span>

-   <span data-ttu-id="78059-116">Развертывание на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="78059-116">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="78059-117">Короткие пути.</span><span class="sxs-lookup"><span data-stu-id="78059-117">Short paths.</span></span> <span data-ttu-id="78059-118">Если вы планируете использовать короткий путь, вы должны создать новый том.</span><span class="sxs-lookup"><span data-stu-id="78059-118">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="78059-119">Требования к операционной системе для сервера управления</span><span class="sxs-lookup"><span data-stu-id="78059-119">Management server operating system requirements</span></span>

<span data-ttu-id="78059-120">В таблице ниже перечислены операционные системы, которые поддерживаются в установке сервера управления App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="78059-120">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Management server installation.</span></span>

<span data-ttu-id="78059-121">**Примечание**  Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="78059-121">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="78059-122">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="78059-122">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="78059-123">Дополнительные сведения о [политике поддержки жизненного цикла поддержки Майкрософт приведены в разделе вопросы и ответы](https://go.microsoft.com/fwlink/p/?LinkId=31976) .</span><span class="sxs-lookup"><span data-stu-id="78059-123">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="78059-124">Операционная система</span><span class="sxs-lookup"><span data-stu-id="78059-124">Operating system</span></span></th>
<th align="left"><span data-ttu-id="78059-125">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="78059-125">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="78059-126">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="78059-126">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-127">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="78059-127">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-128">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-128">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78059-129">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78059-129">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-130">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-130">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-131">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78059-131">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-132">SP1</span><span class="sxs-lookup"><span data-stu-id="78059-132">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-133">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-133">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="78059-134">**Важно!**  Развертывание роли сервера управления на компьютере с включенным удаленным доступом к рабочему столу не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="78059-134">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="78059-135">Требования к оборудованию сервера управления</span><span class="sxs-lookup"><span data-stu-id="78059-135">Management server hardware requirements</span></span>

-   <span data-ttu-id="78059-136">Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор</span><span class="sxs-lookup"><span data-stu-id="78059-136">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="78059-137">ОЗУ — 1 ГБ ОЗУ (64-разр.)</span><span class="sxs-lookup"><span data-stu-id="78059-137">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="78059-138">Место на диске — 200 МБАЙТ свободного места на жестком диске, не включая каталог содержимого</span><span class="sxs-lookup"><span data-stu-id="78059-138">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="78059-139">Требования к базам данных сервера управления</span><span class="sxs-lookup"><span data-stu-id="78059-139">Management server database requirements</span></span>

<span data-ttu-id="78059-140">В следующей таблице перечислены версии SQL Server, которые поддерживаются при установке App-V 5,0 с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="78059-140">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="78059-141">Версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="78059-141">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="78059-142">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="78059-142">Service pack</span></span></th>
<th align="left"><span data-ttu-id="78059-143">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="78059-143">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-144">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="78059-144">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-145">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-145">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78059-146">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="78059-146">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-147">SP2</span><span class="sxs-lookup"><span data-stu-id="78059-147">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-148">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-148">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-149">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78059-149">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-150">ОБНОВЛЕНИЙ</span><span class="sxs-lookup"><span data-stu-id="78059-150">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-151">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-151">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="78059-152">Требования к операционной системе сервера публикаций</span><span class="sxs-lookup"><span data-stu-id="78059-152">Publishing server operating system requirements</span></span>

<span data-ttu-id="78059-153">В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера App-V 5,0 с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="78059-153">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Publishing server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="78059-154">Операционная система</span><span class="sxs-lookup"><span data-stu-id="78059-154">Operating system</span></span></th>
<th align="left"><span data-ttu-id="78059-155">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="78059-155">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="78059-156">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="78059-156">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-157">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="78059-157">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-158">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-158">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78059-159">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78059-159">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-160">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-160">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-161">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78059-161">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-162">SP1</span><span class="sxs-lookup"><span data-stu-id="78059-162">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-163">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-163">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="78059-164">Требования к оборудованию сервера публикаций</span><span class="sxs-lookup"><span data-stu-id="78059-164">Publishing server hardware requirements</span></span>

<span data-ttu-id="78059-165">Приложение App-V не добавляет никаких дополнительных требований за пределы Windows Server.</span><span class="sxs-lookup"><span data-stu-id="78059-165">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="78059-166">Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор</span><span class="sxs-lookup"><span data-stu-id="78059-166">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="78059-167">ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="78059-167">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="78059-168">Место на диске — 200 МБАЙТ свободного места на жестком диске, не включая каталог содержимого</span><span class="sxs-lookup"><span data-stu-id="78059-168">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="78059-169">Требования к операционной системе сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="78059-169">Reporting server operating system requirements</span></span>

<span data-ttu-id="78059-170">В таблице ниже перечислены операционные системы, которые поддерживаются в установке сервера отчетов App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="78059-170">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Reporting server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="78059-171">Операционная система</span><span class="sxs-lookup"><span data-stu-id="78059-171">Operating system</span></span></th>
<th align="left"><span data-ttu-id="78059-172">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="78059-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="78059-173">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="78059-173">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-174">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="78059-174">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-175">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-175">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78059-176">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78059-176">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-177">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-177">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-178">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78059-178">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-179">SP1</span><span class="sxs-lookup"><span data-stu-id="78059-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-180">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-180">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="78059-181">Требования к оборудованию сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="78059-181">Reporting server hardware requirements</span></span>

<span data-ttu-id="78059-182">Приложение App-V не добавляет никаких дополнительных требований за пределы Windows Server.</span><span class="sxs-lookup"><span data-stu-id="78059-182">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="78059-183">Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор</span><span class="sxs-lookup"><span data-stu-id="78059-183">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="78059-184">ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="78059-184">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="78059-185">Место на диске — 200 МБАЙТ свободного места на жестком диске</span><span class="sxs-lookup"><span data-stu-id="78059-185">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="78059-186">Требования к базам данных сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="78059-186">Reporting server database requirements</span></span>

<span data-ttu-id="78059-187">В следующей таблице перечислены версии SQL Server, которые поддерживаются при установке приложения Database-V 5,0 с базой данных для создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="78059-187">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="78059-188">Версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="78059-188">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="78059-189">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="78059-189">Service pack</span></span></th>
<th align="left"><span data-ttu-id="78059-190">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="78059-190">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-191">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="78059-191">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-192">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-192">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78059-193">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="78059-193">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-194">SP2</span><span class="sxs-lookup"><span data-stu-id="78059-194">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-195">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-195">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-196">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78059-196">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-197">ОБНОВЛЕНИЙ</span><span class="sxs-lookup"><span data-stu-id="78059-197">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-198">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-198">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="78059-199">Требования к системе для клиента App-V</span><span class="sxs-lookup"><span data-stu-id="78059-199">App-V client system requirements</span></span>


<span data-ttu-id="78059-200">В таблице ниже перечислены операционные системы, которые поддерживаются при установке клиента App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="78059-200">The following table lists the operating systems that are supported for the App-V 5.0 SP3 client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="78059-201">Операционная система</span><span class="sxs-lookup"><span data-stu-id="78059-201">Operating system</span></span></th>
<th align="left"><span data-ttu-id="78059-202">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="78059-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="78059-203">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="78059-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-204">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="78059-204">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-205">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-205">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78059-206">Microsoft Windows8</span><span class="sxs-lookup"><span data-stu-id="78059-206">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-207">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-208">Windows7</span><span class="sxs-lookup"><span data-stu-id="78059-208">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-209">SP1</span><span class="sxs-lookup"><span data-stu-id="78059-209">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-210">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-210">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="78059-211">Следующие сценарии установки клиента App-V не поддерживаются, за исключением случаев, указанных ниже.</span><span class="sxs-lookup"><span data-stu-id="78059-211">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="78059-212">Компьютеры под управлением Windows Server</span><span class="sxs-lookup"><span data-stu-id="78059-212">Computers that run Windows Server</span></span>

-   <span data-ttu-id="78059-213">Компьютеры, на которых выполняется приложение App-V 4.6 SP1 или более ранние версии</span><span class="sxs-lookup"><span data-stu-id="78059-213">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="78059-214">Клиент служб удаленных рабочих столов App-V 5,0 (SP3) поддерживается только для серверов с поддержкой RDS</span><span class="sxs-lookup"><span data-stu-id="78059-214">The App-V 5.0 SP3 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="78059-215">Требования к оборудованию клиента App-V</span><span class="sxs-lookup"><span data-stu-id="78059-215">App-V client hardware requirements</span></span>

<span data-ttu-id="78059-216">Ниже приведен список поддерживаемых конфигураций оборудования для установки клиента App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="78059-216">The following list displays the supported hardware configuration for the App-V 5.0 SP3 client installation.</span></span>

-   <span data-ttu-id="78059-217">Процессор — процессор с тактовой частотой 1,4 ГГц или более 32 мощный (x86) или 64-bit (x64)</span><span class="sxs-lookup"><span data-stu-id="78059-217">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="78059-218">ОЗУ — 1 ГБ (32-разрядная версия) или 2 ГБ (64-разр.)</span><span class="sxs-lookup"><span data-stu-id="78059-218">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="78059-219">Диск — 100 МБАЙТ для установки, не включая пространство на диске, используемое виртуализированными приложениями.</span><span class="sxs-lookup"><span data-stu-id="78059-219">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="78059-220">Требования к клиентским системам служб удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="78059-220">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="78059-221">В таблице ниже перечислены операционные системы, которые поддерживаются в установке клиента служб удаленных рабочих столов для App-V 5,0 SP3 (RDS).</span><span class="sxs-lookup"><span data-stu-id="78059-221">The following table lists the operating systems that are supported for App-V 5.0 SP3 Remote Desktop Services (RDS) client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="78059-222">Операционная система</span><span class="sxs-lookup"><span data-stu-id="78059-222">Operating system</span></span></th>
<th align="left"><span data-ttu-id="78059-223">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="78059-223">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="78059-224">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="78059-224">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-225">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="78059-225">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-226">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-226">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78059-227">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78059-227">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-228">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-228">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-229">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78059-229">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-230">SP1</span><span class="sxs-lookup"><span data-stu-id="78059-230">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-231">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-231">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="78059-232">Требования к оборудованию клиента служб удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="78059-232">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="78059-233">Приложение App-V не добавляет никаких дополнительных требований за пределы Windows Server.</span><span class="sxs-lookup"><span data-stu-id="78059-233">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="78059-234">Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор</span><span class="sxs-lookup"><span data-stu-id="78059-234">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="78059-235">ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="78059-235">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="78059-236">Место на диске — 200 МБАЙТ свободного места на жестком диске</span><span class="sxs-lookup"><span data-stu-id="78059-236">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="78059-237">Требования к системе Sequencer</span><span class="sxs-lookup"><span data-stu-id="78059-237">Sequencer system requirements</span></span>


<span data-ttu-id="78059-238">В таблице ниже перечислены операционные системы, которые поддерживаются при установке App-V 5,0 с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="78059-238">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Sequencer installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="78059-239">Операционная система</span><span class="sxs-lookup"><span data-stu-id="78059-239">Operating system</span></span></th>
<th align="left"><span data-ttu-id="78059-240">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="78059-240">Service pack</span></span></th>
<th align="left"><span data-ttu-id="78059-241">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="78059-241">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-242">Microsoft Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="78059-242">Microsoft Windows Server2012 R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="78059-243">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-243">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78059-244">Microsoft Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="78059-244">Microsoft Windows Server2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-245">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-245">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-246">Microsoft Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="78059-246">Microsoft Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-247">SP1</span><span class="sxs-lookup"><span data-stu-id="78059-247">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-248">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-248">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78059-249">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="78059-249">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-250">32- и 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-250">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78059-251">Microsoft Windows8</span><span class="sxs-lookup"><span data-stu-id="78059-251">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="78059-252">32- и 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-252">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78059-253">Microsoft Windows7</span><span class="sxs-lookup"><span data-stu-id="78059-253">Microsoft Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-254">SP1</span><span class="sxs-lookup"><span data-stu-id="78059-254">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="78059-255">32- и 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="78059-255">32-bit and 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="78059-256">Требования к оборудованию Sequencer</span><span class="sxs-lookup"><span data-stu-id="78059-256">Sequencer hardware requirements</span></span>

<span data-ttu-id="78059-257">Требования к оборудованию приведены в документации по Windows или Windows Server.</span><span class="sxs-lookup"><span data-stu-id="78059-257">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="78059-258">Приложение App-V добавляет дополнительные требования к оборудованию.</span><span class="sxs-lookup"><span data-stu-id="78059-258">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="78059-259">Поддерживаемые версии System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="78059-259">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="78059-260">Клиент App-V поддерживает следующие версии System Center Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="78059-260">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="78059-261">MicrosoftSystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="78059-261">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="78059-262">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="78059-262">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="78059-263">System Center 2012 R2 Configuration Manager с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="78059-263">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="78059-264">Дополнительные сведения о том, как Configuration Manager интегрируется с App-V, можно найти в разделе [Планирование интеграции App-v с Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="78059-264">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="78059-265">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="78059-265">Related topics</span></span>


[<span data-ttu-id="78059-266">Планирование развертывания App-V</span><span class="sxs-lookup"><span data-stu-id="78059-266">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="78059-267">Необходимые условия для App-V 5.0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="78059-267">App-V 5.0 SP3 Prerequisites</span></span>](app-v-50-sp3-prerequisites.md)

 

 





