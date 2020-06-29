---
title: Поддерживаемые конфигурации в App-V 5.1
description: Поддерживаемые конфигурации в App-V 5.1
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814725"
---
# <span data-ttu-id="60d72-103">Поддерживаемые конфигурации в App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="60d72-103">App-V 5.1 Supported Configurations</span></span>

><span data-ttu-id="60d72-104">Применимо к Windows 10 версии 1607; Window Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (расширенная обновление для системы безопасности)</span><span class="sxs-lookup"><span data-stu-id="60d72-104">Applies to: Windows 10, version 1607; Window Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (Extended Security Update)</span></span>

<span data-ttu-id="60d72-105">В этой статье указаны требования для установки и запуска Microsoft Application Virtualization (App-V) 5,1 в среде.</span><span class="sxs-lookup"><span data-stu-id="60d72-105">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.1 in your environment.</span></span>

## <span data-ttu-id="60d72-106">Требования к системе для App-V Server</span><span class="sxs-lookup"><span data-stu-id="60d72-106">App-V Server system requirements</span></span>

<span data-ttu-id="60d72-107">В этом разделе перечислены требования к операционной системе и оборудованию для всех серверных компонентов App-V.</span><span class="sxs-lookup"><span data-stu-id="60d72-107">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="60d72-108">Неподдерживаемые серверные сценарии App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="60d72-108">Unsupported App-V 5.1 Server scenarios</span></span>

<span data-ttu-id="60d72-109">Сервер App-V 5,1 не поддерживает указанные ниже сценарии.</span><span class="sxs-lookup"><span data-stu-id="60d72-109">The App-V 5.1 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="60d72-110">Развертывание на компьютере, на котором запущен Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="60d72-110">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="60d72-111">Развертывание на компьютере, на котором установлена предыдущая версия App-V 5,1 Server.</span><span class="sxs-lookup"><span data-stu-id="60d72-111">Deployment to a computer that runs a previous version of App-V 5.1 Server components.</span></span> <span data-ttu-id="60d72-112">Приложение App-V 5,1 можно установить рядом с сервером App-V 4.5 облегченного потокового сервера (LWS).</span><span class="sxs-lookup"><span data-stu-id="60d72-112">You can install App-V 5.1 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="60d72-113">Развертывание App-V на стороне с сервером (серверная служба управления виртуализацией приложений для App-V 4,5) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="60d72-113">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="60d72-114">Развертывание на компьютере, на котором запущен Microsoft SQL Server, Экспресс-выпуск.</span><span class="sxs-lookup"><span data-stu-id="60d72-114">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="60d72-115">Развертывание на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="60d72-115">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="60d72-116">Короткие пути.</span><span class="sxs-lookup"><span data-stu-id="60d72-116">Short paths.</span></span> <span data-ttu-id="60d72-117">Если вы планируете использовать короткий путь, вы должны создать новый том.</span><span class="sxs-lookup"><span data-stu-id="60d72-117">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="60d72-118">Требования к операционной системе для сервера управления</span><span class="sxs-lookup"><span data-stu-id="60d72-118">Management server operating system requirements</span></span>

<span data-ttu-id="60d72-119">В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="60d72-119">The following table lists the operating systems that are supported for the App-V 5.1 Management server installation.</span></span>

> [!NOTE]
> <span data-ttu-id="60d72-120">Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="60d72-120">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="60d72-121">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="60d72-121">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="60d72-122">Дополнительные сведения о [политике поддержки жизненного цикла поддержки Майкрософт приведены в разделе вопросы и ответы](https://go.microsoft.com/fwlink/p/?LinkId=31976) .</span><span class="sxs-lookup"><span data-stu-id="60d72-122">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 | <span data-ttu-id="60d72-123">Операционная система</span><span class="sxs-lookup"><span data-stu-id="60d72-123">Operating System</span></span>                 | <span data-ttu-id="60d72-124">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="60d72-124">Service Pack</span></span> | <span data-ttu-id="60d72-125">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="60d72-125">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="60d72-126">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="60d72-126">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="60d72-127">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-127">64-bit</span></span>       |
| <span data-ttu-id="60d72-128">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="60d72-128">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="60d72-129">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-129">64-bit</span></span>       |
| <span data-ttu-id="60d72-130">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="60d72-130">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="60d72-131">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-131">64-bit</span></span>       |
| <span data-ttu-id="60d72-132">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60d72-132">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="60d72-133">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-133">64-bit</span></span>       |
| <span data-ttu-id="60d72-134">[Расширенное обновление для системы безопасности](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="60d72-134">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span>|      <span data-ttu-id="60d72-135">SP1</span><span class="sxs-lookup"><span data-stu-id="60d72-135">SP1</span></span>     |        <span data-ttu-id="60d72-136">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-136">64-bit</span></span>       |
 

<span data-ttu-id="60d72-137">**Важно!**  Развертывание роли сервера управления на компьютере с включенным удаленным доступом к рабочему столу не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="60d72-137">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="60d72-138">Требования к оборудованию сервера управления</span><span class="sxs-lookup"><span data-stu-id="60d72-138">Management server hardware requirements</span></span>

-   <span data-ttu-id="60d72-139">Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор</span><span class="sxs-lookup"><span data-stu-id="60d72-139">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="60d72-140">ОЗУ — 1 ГБ ОЗУ (64-разр.)</span><span class="sxs-lookup"><span data-stu-id="60d72-140">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="60d72-141">Место на диске — 200 МБАЙТ свободного места на жестком диске, не включая каталог содержимого</span><span class="sxs-lookup"><span data-stu-id="60d72-141">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="60d72-142">Требования к базам данных сервера управления</span><span class="sxs-lookup"><span data-stu-id="60d72-142">Management server database requirements</span></span>

<span data-ttu-id="60d72-143">В следующей таблице перечислены версии SQL Server, которые поддерживаются при установке базы данных управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="60d72-143">The following table lists the SQL Server versions that are supported for the App-V 5.1 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="60d72-144">Версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="60d72-144">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="60d72-145">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="60d72-145">Service pack</span></span></th>
<th align="left"><span data-ttu-id="60d72-146">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="60d72-146">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="60d72-147">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="60d72-147">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="60d72-148">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-148">32-bit or 64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="60d72-149">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="60d72-149">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="60d72-150">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-150">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60d72-151">Microsoft SQL Server2016</span><span class="sxs-lookup"><span data-stu-id="60d72-151">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-152">SP2</span><span class="sxs-lookup"><span data-stu-id="60d72-152">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-153">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-153">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60d72-154">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="60d72-154">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-155">SP2</span><span class="sxs-lookup"><span data-stu-id="60d72-155">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-156">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-156">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60d72-157">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="60d72-157">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-158">SP2</span><span class="sxs-lookup"><span data-stu-id="60d72-158">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-159">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-159">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60d72-160">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="60d72-160">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-161">ОБНОВЛЕНИЙ</span><span class="sxs-lookup"><span data-stu-id="60d72-161">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-162">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-162">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="60d72-163">Дополнительные сведения о файлах конфигурации пользователей в SQL Server 2016 и более поздних версиях можно найти в [статье поддержка](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).</span><span class="sxs-lookup"><span data-stu-id="60d72-163">For more information on user configuration files with SQL server 2016 or later, see the [support article](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).</span></span>

### <span data-ttu-id="60d72-164">Требования к операционной системе сервера публикаций</span><span class="sxs-lookup"><span data-stu-id="60d72-164">Publishing server operating system requirements</span></span>

<span data-ttu-id="60d72-165">В таблице ниже перечислены операционные системы, которые поддерживаются в установке сервера публикаций App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="60d72-165">The following table lists the operating systems that are supported for the App-V 5.1 Publishing server installation.</span></span>

| <span data-ttu-id="60d72-166">Операционная система</span><span class="sxs-lookup"><span data-stu-id="60d72-166">Operating System</span></span>                 | <span data-ttu-id="60d72-167">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="60d72-167">Service Pack</span></span> | <span data-ttu-id="60d72-168">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="60d72-168">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="60d72-169">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="60d72-169">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="60d72-170">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-170">64-bit</span></span>       |
| <span data-ttu-id="60d72-171">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="60d72-171">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="60d72-172">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-172">64-bit</span></span>       |
| <span data-ttu-id="60d72-173">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="60d72-173">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="60d72-174">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-174">64-bit</span></span>       |
| <span data-ttu-id="60d72-175">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60d72-175">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="60d72-176">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-176">64-bit</span></span>       |
| <span data-ttu-id="60d72-177">[Расширенное обновление для системы безопасности](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="60d72-177">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="60d72-178">SP1</span><span class="sxs-lookup"><span data-stu-id="60d72-178">SP1</span></span>     |        <span data-ttu-id="60d72-179">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-179">64-bit</span></span>       |

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="60d72-180">Требования к оборудованию сервера публикаций</span><span class="sxs-lookup"><span data-stu-id="60d72-180">Publishing server hardware requirements</span></span>

<span data-ttu-id="60d72-181">Приложение App-V не добавляет никаких дополнительных требований за пределы Windows Server.</span><span class="sxs-lookup"><span data-stu-id="60d72-181">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="60d72-182">Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор</span><span class="sxs-lookup"><span data-stu-id="60d72-182">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="60d72-183">ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="60d72-183">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="60d72-184">Место на диске — 200 МБАЙТ свободного места на жестком диске, не включая каталог содержимого</span><span class="sxs-lookup"><span data-stu-id="60d72-184">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="60d72-185">Требования к операционной системе сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="60d72-185">Reporting server operating system requirements</span></span>

<span data-ttu-id="60d72-186">В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера Reporting Server App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="60d72-186">The following table lists the operating systems that are supported for the App-V 5.1 Reporting server installation.</span></span>

| <span data-ttu-id="60d72-187">Операционная система</span><span class="sxs-lookup"><span data-stu-id="60d72-187">Operating System</span></span>                 | <span data-ttu-id="60d72-188">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="60d72-188">Service Pack</span></span> | <span data-ttu-id="60d72-189">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="60d72-189">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="60d72-190">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="60d72-190">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="60d72-191">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-191">64-bit</span></span>       |
| <span data-ttu-id="60d72-192">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="60d72-192">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="60d72-193">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-193">64-bit</span></span>       |
| <span data-ttu-id="60d72-194">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="60d72-194">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="60d72-195">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-195">64-bit</span></span>       |
| <span data-ttu-id="60d72-196">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60d72-196">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="60d72-197">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-197">64-bit</span></span>       |
| <span data-ttu-id="60d72-198">[Расширенное обновление для системы безопасности](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="60d72-198">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="60d72-199">SP1</span><span class="sxs-lookup"><span data-stu-id="60d72-199">SP1</span></span>     |        <span data-ttu-id="60d72-200">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-200">64-bit</span></span>       |

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="60d72-201">Требования к оборудованию сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="60d72-201">Reporting server hardware requirements</span></span>

<span data-ttu-id="60d72-202">Приложение App-V не добавляет никаких дополнительных требований за пределы Windows Server.</span><span class="sxs-lookup"><span data-stu-id="60d72-202">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="60d72-203">Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор</span><span class="sxs-lookup"><span data-stu-id="60d72-203">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="60d72-204">ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="60d72-204">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="60d72-205">Место на диске — 200 МБАЙТ свободного места на жестком диске</span><span class="sxs-lookup"><span data-stu-id="60d72-205">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="60d72-206">Требования к базам данных сервера отчетов</span><span class="sxs-lookup"><span data-stu-id="60d72-206">Reporting server database requirements</span></span>

<span data-ttu-id="60d72-207">В приведенной ниже таблице указаны версии SQL Server, которые поддерживаются при установке базы данных Reporting App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="60d72-207">The following table lists the SQL Server versions that are supported for the App-V 5.1 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="60d72-208">Версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="60d72-208">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="60d72-209">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="60d72-209">Service pack</span></span></th>
<th align="left"><span data-ttu-id="60d72-210">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="60d72-210">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60d72-211">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="60d72-211">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="60d72-212">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-212">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60d72-213">Microsoft SQL Server2016</span><span class="sxs-lookup"><span data-stu-id="60d72-213">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-214">SP2</span><span class="sxs-lookup"><span data-stu-id="60d72-214">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-215">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-215">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60d72-216">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="60d72-216">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-217">SP2</span><span class="sxs-lookup"><span data-stu-id="60d72-217">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-218">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-218">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60d72-219">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="60d72-219">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-220">SP2</span><span class="sxs-lookup"><span data-stu-id="60d72-220">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-221">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-221">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60d72-222">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="60d72-222">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-223">ОБНОВЛЕНИЙ</span><span class="sxs-lookup"><span data-stu-id="60d72-223">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-224">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-224">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="60d72-225">Требования к системе для клиента App-V</span><span class="sxs-lookup"><span data-stu-id="60d72-225">App-V client system requirements</span></span>

<span data-ttu-id="60d72-226">В таблице ниже перечислены операционные системы, которые поддерживаются при установке клиента App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="60d72-226">The following table lists the operating systems that are supported for the App-V 5.1 client installation.</span></span>

> [!NOTE]
> <span data-ttu-id="60d72-227">С выпуском годовщины Windows 10 (версия 1607) клиент App-V входит в комплект и будет блокировать установку любой предыдущей версии клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="60d72-227">With the Windows 10 Anniversary release (aka 1607 version), the App-V client is in-box and will block installation of any previous version of the App-V client</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="60d72-228">Операционная система</span><span class="sxs-lookup"><span data-stu-id="60d72-228">Operating system</span></span></th>
<th align="left"><span data-ttu-id="60d72-229">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="60d72-229">Service pack</span></span></th>
<th align="left"><span data-ttu-id="60d72-230">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="60d72-230">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60d72-231">Microsoft Windows10 (версия до 1607)</span><span class="sxs-lookup"><span data-stu-id="60d72-231">Microsoft Windows10 (pre-1607 version)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="60d72-232">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-232">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60d72-233">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="60d72-233">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="60d72-234">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-234">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60d72-235">Windows7</span><span class="sxs-lookup"><span data-stu-id="60d72-235">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-236">SP1</span><span class="sxs-lookup"><span data-stu-id="60d72-236">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-237">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-237">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="60d72-238">Следующие сценарии установки клиента App-V не поддерживаются, за исключением случаев, указанных ниже.</span><span class="sxs-lookup"><span data-stu-id="60d72-238">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="60d72-239">Компьютеры под управлением Windows Server</span><span class="sxs-lookup"><span data-stu-id="60d72-239">Computers that run Windows Server</span></span>

-   <span data-ttu-id="60d72-240">Компьютеры, на которых выполняется приложение App-V 4.6 SP1 или более ранние версии</span><span class="sxs-lookup"><span data-stu-id="60d72-240">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="60d72-241">Клиент служб удаленных рабочих столов App-V 5,1 поддерживается только для серверов с поддержкой служб удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="60d72-241">The App-V 5.1 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="60d72-242">Требования к оборудованию клиента App-V</span><span class="sxs-lookup"><span data-stu-id="60d72-242">App-V client hardware requirements</span></span>

<span data-ttu-id="60d72-243">В списке ниже показана конфигурация оборудования, поддерживаемая установкой клиента App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="60d72-243">The following list displays the supported hardware configuration for the App-V 5.1 client installation.</span></span>

-   <span data-ttu-id="60d72-244">Процессор — процессор с тактовой частотой 1,4 ГГц или более 32 мощный (x86) или 64-bit (x64)</span><span class="sxs-lookup"><span data-stu-id="60d72-244">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="60d72-245">ОЗУ — 1 ГБ (32-разрядная версия) или 2 ГБ (64-разр.)</span><span class="sxs-lookup"><span data-stu-id="60d72-245">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="60d72-246">Диск — 100 МБАЙТ для установки, не включая пространство на диске, используемое виртуализированными приложениями.</span><span class="sxs-lookup"><span data-stu-id="60d72-246">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="60d72-247">Требования к клиентским системам служб удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="60d72-247">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="60d72-248">В следующей таблице перечислены операционные системы, которые поддерживаются при установке клиента служб удаленных рабочих столов App-V 5,1 (RDS).</span><span class="sxs-lookup"><span data-stu-id="60d72-248">The following table lists the operating systems that are supported for App-V 5.1 Remote Desktop Services (RDS) client installation.</span></span>

| <span data-ttu-id="60d72-249">Операционная система</span><span class="sxs-lookup"><span data-stu-id="60d72-249">Operating System</span></span>                 | <span data-ttu-id="60d72-250">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="60d72-250">Service Pack</span></span> | <span data-ttu-id="60d72-251">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="60d72-251">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="60d72-252">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="60d72-252">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="60d72-253">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-253">64-bit</span></span>       |
| <span data-ttu-id="60d72-254">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="60d72-254">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="60d72-255">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-255">64-bit</span></span>       |
| <span data-ttu-id="60d72-256">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="60d72-256">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="60d72-257">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-257">64-bit</span></span>       |
| <span data-ttu-id="60d72-258">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60d72-258">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="60d72-259">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-259">64-bit</span></span>       |
| <span data-ttu-id="60d72-260">[Расширенное обновление для системы безопасности](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="60d72-260">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="60d72-261">SP1</span><span class="sxs-lookup"><span data-stu-id="60d72-261">SP1</span></span>     |        <span data-ttu-id="60d72-262">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-262">64-bit</span></span>       |

### <span data-ttu-id="60d72-263">Требования к оборудованию клиента служб удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="60d72-263">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="60d72-264">Приложение App-V не добавляет никаких дополнительных требований за пределы Windows Server.</span><span class="sxs-lookup"><span data-stu-id="60d72-264">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="60d72-265">Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор</span><span class="sxs-lookup"><span data-stu-id="60d72-265">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="60d72-266">ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="60d72-266">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="60d72-267">Место на диске — 200 МБАЙТ свободного места на жестком диске</span><span class="sxs-lookup"><span data-stu-id="60d72-267">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="60d72-268">Требования к системе Sequencer</span><span class="sxs-lookup"><span data-stu-id="60d72-268">Sequencer system requirements</span></span>

<span data-ttu-id="60d72-269">В следующей таблице перечислены операционные системы, которые поддерживаются при установке App-V 5,1 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="60d72-269">The following table lists the operating systems that are supported for the App-V 5.1 Sequencer installation.</span></span>

| <span data-ttu-id="60d72-270">Операционная система</span><span class="sxs-lookup"><span data-stu-id="60d72-270">Operating System</span></span>                 | <span data-ttu-id="60d72-271">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="60d72-271">Service Pack</span></span> | <span data-ttu-id="60d72-272">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="60d72-272">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="60d72-273">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="60d72-273">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="60d72-274">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-274">64-bit</span></span>       |
| <span data-ttu-id="60d72-275">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="60d72-275">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="60d72-276">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-276">64-bit</span></span>       |
| <span data-ttu-id="60d72-277">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="60d72-277">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="60d72-278">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-278">64-bit</span></span>       |
| <span data-ttu-id="60d72-279">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60d72-279">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="60d72-280">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-280">64-bit</span></span>       |
| <span data-ttu-id="60d72-281">[Расширенное обновление для системы безопасности](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="60d72-281">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="60d72-282">SP1</span><span class="sxs-lookup"><span data-stu-id="60d72-282">SP1</span></span>     |        <span data-ttu-id="60d72-283">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-283">64-bit</span></span>       |
| <span data-ttu-id="60d72-284">Microsoft Windows 10</span><span class="sxs-lookup"><span data-stu-id="60d72-284">Microsoft Windows 10</span></span>             |              | <span data-ttu-id="60d72-285">32- и 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-285">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="60d72-286">Microsoft Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="60d72-286">Microsoft Windows 8.1</span></span>            |              | <span data-ttu-id="60d72-287">32- и 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-287">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="60d72-288">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="60d72-288">Microsoft Windows 7</span></span>              |      <span data-ttu-id="60d72-289">SP1</span><span class="sxs-lookup"><span data-stu-id="60d72-289">SP1</span></span>     | <span data-ttu-id="60d72-290">32- и 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="60d72-290">32-bit and 64-bit</span></span>   |

### <span data-ttu-id="60d72-291">Требования к оборудованию Sequencer</span><span class="sxs-lookup"><span data-stu-id="60d72-291">Sequencer hardware requirements</span></span>

<span data-ttu-id="60d72-292">Требования к оборудованию приведены в документации по Windows или Windows Server.</span><span class="sxs-lookup"><span data-stu-id="60d72-292">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="60d72-293">Приложение App-V добавляет дополнительные требования к оборудованию.</span><span class="sxs-lookup"><span data-stu-id="60d72-293">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="60d72-294">Поддерживаемые версии System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="60d72-294">Supported versions of System Center Configuration Manager</span></span>

<span data-ttu-id="60d72-295">Клиент App-V поддерживает следующие версии System Center Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="60d72-295">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="60d72-296">MicrosoftSystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="60d72-296">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="60d72-297">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="60d72-297">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="60d72-298">System Center 2012 R2 Configuration Manager с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="60d72-298">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="60d72-299">В следующей матрице версий App-V и System Center Configuration Manager показаны все официально поддерживаемые комбинации App-V и Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="60d72-299">The following App-V and System Center Configuration Manager version matrix shows all officially supported combinations of App-V and Configuration Manager.</span></span>

> [!NOTE]
> <span data-ttu-id="60d72-300">Приложение App-V 4,5 и 4,6 успешно завершило работу базовой поддержки.</span><span class="sxs-lookup"><span data-stu-id="60d72-300">Both App-V 4.5 and 4.6 have exited Mainstream support.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="60d72-301">Версия App-V</span><span class="sxs-lookup"><span data-stu-id="60d72-301">App-V Version</span></span></th>
<th align="left"><span data-ttu-id="60d72-302">System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="60d72-302">System Center Configuration Manager 2007</span></span></th>
<th align="left"><span data-ttu-id="60d72-303">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="60d72-303">System Center 2012 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="60d72-304">System Center 2012 Configuration Manager с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="60d72-304">System Center 2012 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="60d72-305">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="60d72-305">System Center 2012 R2 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="60d72-306">System Center 2012 R2 Configuration Manager с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="60d72-306">System Center 2012 R2 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="60d72-307">System Center 2012 Configuration Manager с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="60d72-307">System Center 2012 Configuration Manager SP2</span></span></th>
<th align="left"><span data-ttu-id="60d72-308">System Center Configuration Manager версии 1511</span><span class="sxs-lookup"><span data-stu-id="60d72-308">System Center Configuration Manager Version 1511</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60d72-309">App-V 5,0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="60d72-309">App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-310">Только обертки MSI</span><span class="sxs-lookup"><span data-stu-id="60d72-310">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-311">Нет</span><span class="sxs-lookup"><span data-stu-id="60d72-311">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-312">2012 SP1 НАКОПИТЕЛЬНЫМ</span><span class="sxs-lookup"><span data-stu-id="60d72-312">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-313">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="60d72-313">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-314">Да</span><span class="sxs-lookup"><span data-stu-id="60d72-314">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-315">Да</span><span class="sxs-lookup"><span data-stu-id="60d72-315">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-316">Да</span><span class="sxs-lookup"><span data-stu-id="60d72-316">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60d72-317">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="60d72-317">App-V 5.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-318">Только обертки MSI</span><span class="sxs-lookup"><span data-stu-id="60d72-318">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-319">Нет</span><span class="sxs-lookup"><span data-stu-id="60d72-319">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-320">2012 SP1 НАКОПИТЕЛЬНЫМ</span><span class="sxs-lookup"><span data-stu-id="60d72-320">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-321">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="60d72-321">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-322">Да</span><span class="sxs-lookup"><span data-stu-id="60d72-322">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-323">Да</span><span class="sxs-lookup"><span data-stu-id="60d72-323">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="60d72-324">Да</span><span class="sxs-lookup"><span data-stu-id="60d72-324">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="60d72-325">Дополнительные сведения о том, как Configuration Manager интегрируется с App-V, можно найти в разделе [Планирование интеграции App-v с Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="60d72-325">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>

## <span data-ttu-id="60d72-326">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="60d72-326">Related topics</span></span>

[<span data-ttu-id="60d72-327">Планирование развертывания App-V</span><span class="sxs-lookup"><span data-stu-id="60d72-327">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="60d72-328">Предварительные требования App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="60d72-328">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)
