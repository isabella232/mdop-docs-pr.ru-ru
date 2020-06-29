---
title: Требования программы Sequencer к оборудованию и программному обеспечению
description: Требования программы Sequencer к оборудованию и программному обеспечению
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815532"
---
# <span data-ttu-id="b4965-103">Требования программы Sequencer к оборудованию и программному обеспечению</span><span class="sxs-lookup"><span data-stu-id="b4965-103">Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="b4965-104">В этой статье описаны минимальные рекомендуемые требования к оборудованию и программному обеспечению для компьютера, на котором работает секвенсор Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="b4965-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="b4965-105">Перед установкой секвенсора и после упорядочения каждого приложения необходимо восстановить чистую копию операционной системы на компьютере виртуализации.</span><span class="sxs-lookup"><span data-stu-id="b4965-105">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="b4965-106">Для восстановления компьютера, на котором запущен секвенсор, можно использовать один из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="b4965-106">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="b4965-107">Переформатируйте жесткий диск и переустановите операционную систему.</span><span class="sxs-lookup"><span data-stu-id="b4965-107">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="b4965-108">Восстановите жесткий диск компьютера, на котором запущено изображение секвенсора, с помощью другого программного обеспечения для обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="b4965-108">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

<span data-ttu-id="b4965-109">Ниже приведен список рекомендуемых требований к оборудованию для работы секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="b4965-109">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="b4965-110">Требования к оборудованию</span><span class="sxs-lookup"><span data-stu-id="b4965-110">Hardware Requirements</span></span>

-   <span data-ttu-id="b4965-111">Процессор — Intel Pentium III, 1 ГГц (32-разрядная или 64-разр.).</span><span class="sxs-lookup"><span data-stu-id="b4965-111">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="b4965-112">Процесс упорядочения является однопотоковым процессом и не использует преимущества двух процессоров.</span><span class="sxs-lookup"><span data-stu-id="b4965-112">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="b4965-113">Память (1 ГБ или более), рекомендуется не менее 2 Гбайт.</span><span class="sxs-lookup"><span data-stu-id="b4965-113">Memory—1GB or above, 2 GB recommended.</span></span>

-   <span data-ttu-id="b4965-114">Жесткий диск — объем свободного места на жестком диске объемом не менее 15 ГБ.</span><span class="sxs-lookup"><span data-stu-id="b4965-114">Hard Disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="b4965-115">Рекомендуется, чтобы в три места на жестком диске соработало приложение, для которого требуется выполнить виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="b4965-115">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="b4965-116">**Примечание**  Для виртуализации требуется высокая нагрузка на диск.</span><span class="sxs-lookup"><span data-stu-id="b4965-116">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="b4965-117">Ускоренная скорость диска может уменьшить время последовательности.</span><span class="sxs-lookup"><span data-stu-id="b4965-117">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="b4965-118">Требования к программному обеспечению</span><span class="sxs-lookup"><span data-stu-id="b4965-118">Software Requirements</span></span>

<span data-ttu-id="b4965-119">В следующем списке описаны поддерживаемые операционные системы для запуска секвенсора.</span><span class="sxs-lookup"><span data-stu-id="b4965-119">The following list outlines the supported operating systems for running the Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b4965-120">Операционная система</span><span class="sxs-lookup"><span data-stu-id="b4965-120">Operating System</span></span></th>
<th align="left"><span data-ttu-id="b4965-121">Выпуск</span><span class="sxs-lookup"><span data-stu-id="b4965-121">Edition</span></span></th>
<th align="left"><span data-ttu-id="b4965-122">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="b4965-122">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="b4965-123">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="b4965-123">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4965-124">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="b4965-124">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-125">Профессиональная</span><span class="sxs-lookup"><span data-stu-id="b4965-125">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-126">SP2 или 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="b4965-126">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-127">x86</span><span class="sxs-lookup"><span data-stu-id="b4965-127">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4965-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4965-128">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-129">Бизнес, Корпоративная или максимальная</span><span class="sxs-lookup"><span data-stu-id="b4965-129">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-130">Пакет обновления, пакет обновления 1 (SP1) или пакет обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="b4965-130">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-131">x86</span><span class="sxs-lookup"><span data-stu-id="b4965-131">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4965-132">Windows7 ¹</span><span class="sxs-lookup"><span data-stu-id="b4965-132">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-133">Профессиональная, Корпоративная или максимальная</span><span class="sxs-lookup"><span data-stu-id="b4965-133">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b4965-134">x86</span><span class="sxs-lookup"><span data-stu-id="b4965-134">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b4965-135">¹ поддерживается для App-V 4,5 с пакетом обновления 1 или 2, а также App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="b4965-135">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="b4965-136">**Примечание**  Приложение Application Virtualization (App-V) 4,6 поддерживает версию с 32-и 64-разрядные версии этих операционных систем.</span><span class="sxs-lookup"><span data-stu-id="b4965-136">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="b4965-137">На компьютерах под управлением программы Sequencer следует настроить те же приложения, которые установлены на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="b4965-137">You should configure computers running the Sequencer with the same applications that are installed on target computers.</span></span>

### <span data-ttu-id="b4965-138">Требования к программному обеспечению для служб удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="b4965-138">Software Requirements for Remote Desktop Services</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b4965-139">Операционная система</span><span class="sxs-lookup"><span data-stu-id="b4965-139">Operating System</span></span></th>
<th align="left"><span data-ttu-id="b4965-140">Выпуск</span><span class="sxs-lookup"><span data-stu-id="b4965-140">Edition</span></span></th>
<th align="left"><span data-ttu-id="b4965-141">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="b4965-141">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="b4965-142">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="b4965-142">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4965-143">Windows server2003</span><span class="sxs-lookup"><span data-stu-id="b4965-143">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-144">Standard Edition, Enterprise Edition или Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="b4965-144">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-145">Пакет обновления 1 (SP1) или 2</span><span class="sxs-lookup"><span data-stu-id="b4965-145">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-146">x86</span><span class="sxs-lookup"><span data-stu-id="b4965-146">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4965-147">Windows server2003 R2</span><span class="sxs-lookup"><span data-stu-id="b4965-147">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-148">Standard Edition, Enterprise Edition или Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="b4965-148">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b4965-149">x86</span><span class="sxs-lookup"><span data-stu-id="b4965-149">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4965-150">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="b4965-150">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-151">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="b4965-151">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-152">Пакет обновления 1 (SP1) или 2</span><span class="sxs-lookup"><span data-stu-id="b4965-152">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4965-153">x86</span><span class="sxs-lookup"><span data-stu-id="b4965-153">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b4965-154">**Примечание**  Application Virtualization (App-V) 4,6 для служб удаленных рабочих столов поддерживает 32-разр и 64-разрядные версии этих операционных систем.</span><span class="sxs-lookup"><span data-stu-id="b4965-154">**Note** Application Virtualization (App-V) 4.6 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="b4965-155">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b4965-155">Related topics</span></span>


[<span data-ttu-id="b4965-156">Обзор программы Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="b4965-156">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





