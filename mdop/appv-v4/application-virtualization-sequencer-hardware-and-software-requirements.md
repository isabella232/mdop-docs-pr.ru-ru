---
title: Требования программы Application Virtualization Sequencer к оборудованию и программному обеспечению
description: Требования программы Application Virtualization Sequencer к оборудованию и программному обеспечению
author: dansimp
ms.assetid: c88a1b5b-23e1-4460-afa9-a5f37e32eb05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d68afe4d4a3f6f301d38f2e86139d94319583467
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819622"
---
# <span data-ttu-id="d4aa4-103">Требования программы Application Virtualization Sequencer к оборудованию и программному обеспечению</span><span class="sxs-lookup"><span data-stu-id="d4aa4-103">Application Virtualization Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="d4aa4-104">В этой статье описаны минимальные рекомендуемые требования к оборудованию и программному обеспечению для компьютера, на котором работает секвенсор Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="d4aa4-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="d4aa4-105">**Важно!**  Вы должны запустить секвенсор App-V (**SFTSequencer.exe**), используя учетную запись с правами администратора из-за изменений, которые секвенсор делает в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-105">**Important** You must run the App-V sequencer (**SFTSequencer.exe**) using an account that has administrator privileges because of the changes the sequencer makes to the local system.</span></span> <span data-ttu-id="d4aa4-106">Эти изменения могут включать запись файлов в каталог **C:\\program Files Files** , внесение изменений в реестр, запуск и остановку служб, обновление дескрипторов безопасности для файлов и изменение разрешений.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-106">These changes can include writing files to the **C:\\Program Files** directory, making registry changes, starting and stopping services, updating security descriptors for files, and changing permissions.</span></span>

 

<span data-ttu-id="d4aa4-107">Перед установкой секвенсора и после упорядочения каждого приложения необходимо восстановить чистую копию операционной системы на компьютере виртуализации.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-107">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="d4aa4-108">Для восстановления компьютера, на котором запущен секвенсор, можно использовать один из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="d4aa4-108">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="d4aa4-109">Переформатируйте жесткий диск и переустановите операционную систему.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-109">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="d4aa4-110">Восстановите жесткий диск компьютера, на котором запущено изображение секвенсора, с помощью другого программного обеспечения для обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-110">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

-   <span data-ttu-id="d4aa4-111">Возврат образа виртуальной операционной системы, например, изображения виртуального компьютера Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-111">Revert a virtual operating system image such as a Microsoft Virtual PC image.</span></span> <span data-ttu-id="d4aa4-112">С помощью виртуальной машины можно легко повторно использовать чистые среды виртуализации с минимальным администрированием.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-112">Using a virtual machine allows for clean sequencing environments to be easily reused with minimal administration.</span></span>

<span data-ttu-id="d4aa4-113">Ниже приведен список рекомендуемых требований к оборудованию для работы секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-113">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

<span data-ttu-id="d4aa4-114">Требования перечислены в первую очередь для Microsoft Application Virtualization (App-V) 4.6 SP2, за которым следуют требования для версий, предшествующих App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-114">The requirements are listed first for Microsoft Application Virtualization (App-V)4.6 SP2, followed by the requirements for versions that preceded App-V4.6SP2.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="d4aa4-115">Требования к оборудованию</span><span class="sxs-lookup"><span data-stu-id="d4aa4-115">Hardware Requirements</span></span>

-   <span data-ttu-id="d4aa4-116">Процессор — Intel Pentium III, 1 ГГц (32-разрядная или 64-разр.).</span><span class="sxs-lookup"><span data-stu-id="d4aa4-116">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="d4aa4-117">Процесс упорядочения является однопотоковым процессом и не использует преимущества двух процессоров.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-117">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="d4aa4-118">Память (1 ГБ или выше) рекомендуется 2 ГБ.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-118">Memory—1GB or above, 2GB recommended.</span></span>

-   <span data-ttu-id="d4aa4-119">Жесткий диск — объем свободного места на жестком диске объемом не менее 15 ГБ.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-119">Hard disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="d4aa4-120">Рекомендуется, чтобы в три места на жестком диске соработало приложение, для которого требуется выполнить виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-120">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="d4aa4-121">**Примечание**  Для виртуализации требуется высокая нагрузка на диск.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-121">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="d4aa4-122">Ускоренная скорость диска может уменьшить время последовательности.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-122">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="d4aa4-123">Требования к программному обеспечению для App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="d4aa4-123">Software Requirements for App-V 4.6 SP2</span></span>

<span data-ttu-id="d4aa4-124">В приведенном ниже списке описаны поддерживаемые операционные системы для работы с секвенсором App-V 4,6 с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="d4aa4-124">The following list outlines the supported operating systems for running the App-V 4.6 SP2 Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d4aa4-125">Операционная система</span><span class="sxs-lookup"><span data-stu-id="d4aa4-125">Operating System</span></span></th>
<th align="left"><span data-ttu-id="d4aa4-126">Выпуск</span><span class="sxs-lookup"><span data-stu-id="d4aa4-126">Edition</span></span></th>
<th align="left"><span data-ttu-id="d4aa4-127">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="d4aa4-127">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="d4aa4-128">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="d4aa4-128">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4aa4-129">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="d4aa4-129">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-130">Профессиональная</span><span class="sxs-lookup"><span data-stu-id="d4aa4-130">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-131">ОБНОВЛЕНИЙ</span><span class="sxs-lookup"><span data-stu-id="d4aa4-131">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-132">x86</span><span class="sxs-lookup"><span data-stu-id="d4aa4-132">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4aa4-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4aa4-133">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-134">Бизнес, Корпоративная или максимальная</span><span class="sxs-lookup"><span data-stu-id="d4aa4-134">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-135">SP2</span><span class="sxs-lookup"><span data-stu-id="d4aa4-135">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-136">x86</span><span class="sxs-lookup"><span data-stu-id="d4aa4-136">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4aa4-137">Windows7</span><span class="sxs-lookup"><span data-stu-id="d4aa4-137">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-138">Профессиональная, Корпоративная или максимальная</span><span class="sxs-lookup"><span data-stu-id="d4aa4-138">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-139">Пакет обновления или пакет обновления 1 (SP1) отсутствуют</span><span class="sxs-lookup"><span data-stu-id="d4aa4-139">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-140">x86 и x64</span><span class="sxs-lookup"><span data-stu-id="d4aa4-140">x86 and x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4aa4-141">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d4aa4-141">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-142">Pro или Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="d4aa4-142">Pro or Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-143">x86 и x64</span><span class="sxs-lookup"><span data-stu-id="d4aa4-143">x86 and x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d4aa4-144">**Примечание**  Application Virtualization (App-V) 4,6 с пакетом обновления 2 (SP2) поддерживает 32-разрядные и 64-разрядные версии этих операционных систем.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-144">**Note** The Application Virtualization (App-V) 4.6 SP2 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="d4aa4-145">На компьютерах под управлением программы Sequencer следует настроить те же приложения, которые установлены на целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-145">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="d4aa4-146">Требования к программному обеспечению для версий, предшествующих App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="d4aa4-146">Software Requirements for Versions that Precede App-V 4.6 SP2</span></span>

<span data-ttu-id="d4aa4-147">В следующем списке описаны поддерживаемые операционные системы для работы программы Sequencer для версий, предшествующих App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-147">The following list outlines the supported operating systems for running the Sequencer for versions that precede App-V 4.6 SP2.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d4aa4-148">Операционная система</span><span class="sxs-lookup"><span data-stu-id="d4aa4-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="d4aa4-149">Выпуск</span><span class="sxs-lookup"><span data-stu-id="d4aa4-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="d4aa4-150">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="d4aa4-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="d4aa4-151">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="d4aa4-151">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4aa4-152">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="d4aa4-152">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-153">Профессиональная</span><span class="sxs-lookup"><span data-stu-id="d4aa4-153">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-154">SP2 или 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="d4aa4-154">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-155">x86</span><span class="sxs-lookup"><span data-stu-id="d4aa4-155">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4aa4-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4aa4-156">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-157">Бизнес, Корпоративная или максимальная</span><span class="sxs-lookup"><span data-stu-id="d4aa4-157">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-158">Пакет обновления, пакет обновления 1 (SP1) или пакет обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="d4aa4-158">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-159">x86</span><span class="sxs-lookup"><span data-stu-id="d4aa4-159">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4aa4-160">Windows7 ¹</span><span class="sxs-lookup"><span data-stu-id="d4aa4-160">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-161">Профессиональная, Корпоративная или максимальная</span><span class="sxs-lookup"><span data-stu-id="d4aa4-161">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-162">x86</span><span class="sxs-lookup"><span data-stu-id="d4aa4-162">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d4aa4-163">¹ поддерживается для App-V 4,5 с пакетом обновления 1 или 2, а также App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="d4aa4-163">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="d4aa4-164">**Примечание**  Приложение Application Virtualization (App-V) 4,6 поддерживает версию с 32-и 64-разрядные версии этих операционных систем.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-164">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="d4aa4-165">На компьютерах под управлением программы Sequencer следует настроить те же приложения, которые установлены на целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-165">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="d4aa4-166">Требования к программному обеспечению для служб удаленных рабочих столов для App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="d4aa4-166">Software Requirements for Remote Desktop Services for App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d4aa4-167">Операционная система</span><span class="sxs-lookup"><span data-stu-id="d4aa4-167">Operating System</span></span></th>
<th align="left"><span data-ttu-id="d4aa4-168">Выпуск</span><span class="sxs-lookup"><span data-stu-id="d4aa4-168">Edition</span></span></th>
<th align="left"><span data-ttu-id="d4aa4-169">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="d4aa4-169">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="d4aa4-170">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="d4aa4-170">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4aa4-171">Windows server2003 R2</span><span class="sxs-lookup"><span data-stu-id="d4aa4-171">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-172">Standard Edition, Enterprise Edition или Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="d4aa4-172">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-173">SP2</span><span class="sxs-lookup"><span data-stu-id="d4aa4-173">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-174">x86</span><span class="sxs-lookup"><span data-stu-id="d4aa4-174">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4aa4-175">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="d4aa4-175">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-176">Standard, Enterprise и Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="d4aa4-176">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-177">SP2</span><span class="sxs-lookup"><span data-stu-id="d4aa4-177">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-178">x86</span><span class="sxs-lookup"><span data-stu-id="d4aa4-178">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4aa4-179">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="d4aa4-179">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-180">Standard, Enterprise и Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="d4aa4-180">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-181">Пакет обновления или пакет обновления 1 (SP1) отсутствуют</span><span class="sxs-lookup"><span data-stu-id="d4aa4-181">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-182">x64</span><span class="sxs-lookup"><span data-stu-id="d4aa4-182">x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4aa4-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d4aa4-183">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-184">Standard, Enterprise и Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="d4aa4-184">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-185">x86 или x64</span><span class="sxs-lookup"><span data-stu-id="d4aa4-185">x86 or x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d4aa4-186">**Примечание**  Application Virtualization (App-V) 4,6 с пакетом обновления 2 (SP2) для служб удаленных рабочих столов поддерживает 32-разрядные и 64-разрядные версии этих операционных систем.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-186">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

### <span data-ttu-id="d4aa4-187">Требования к программному обеспечению для служб удаленных рабочих столов для версий, предшествующих App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="d4aa4-187">Software Requirements for Remote Desktop Services for Versions that Precede App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d4aa4-188">Операционная система</span><span class="sxs-lookup"><span data-stu-id="d4aa4-188">Operating System</span></span></th>
<th align="left"><span data-ttu-id="d4aa4-189">Выпуск</span><span class="sxs-lookup"><span data-stu-id="d4aa4-189">Edition</span></span></th>
<th align="left"><span data-ttu-id="d4aa4-190">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="d4aa4-190">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="d4aa4-191">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="d4aa4-191">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4aa4-192">Windows server2003</span><span class="sxs-lookup"><span data-stu-id="d4aa4-192">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-193">Standard Edition, Enterprise Edition или Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="d4aa4-193">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-194">Пакет обновления 1 (SP1) или 2</span><span class="sxs-lookup"><span data-stu-id="d4aa4-194">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-195">x86</span><span class="sxs-lookup"><span data-stu-id="d4aa4-195">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4aa4-196">Windows server2003 R2</span><span class="sxs-lookup"><span data-stu-id="d4aa4-196">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-197">Standard Edition, Enterprise Edition или Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="d4aa4-197">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-198">Нет пакета обновления или пакета обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="d4aa4-198">No service pack or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-199">x86</span><span class="sxs-lookup"><span data-stu-id="d4aa4-199">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4aa4-200">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="d4aa4-200">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-201">Standard, Enterprise и Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="d4aa4-201">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-202">Пакет обновления 1 (SP1) или 2</span><span class="sxs-lookup"><span data-stu-id="d4aa4-202">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-203">x86</span><span class="sxs-lookup"><span data-stu-id="d4aa4-203">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4aa4-204">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="d4aa4-204">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-205">Standard, Enterprise и Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="d4aa4-205">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-206">Пакет обновления или пакет обновления 1 (SP1) отсутствуют</span><span class="sxs-lookup"><span data-stu-id="d4aa4-206">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4aa4-207">x64</span><span class="sxs-lookup"><span data-stu-id="d4aa4-207">x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d4aa4-208">**Примечание**  Application Virtualization (App-V) 4,6 с пакетом обновления 2 (SP2) для служб удаленных рабочих столов поддерживает 32-разрядные и 64-разрядные версии этих операционных систем.</span><span class="sxs-lookup"><span data-stu-id="d4aa4-208">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="d4aa4-209">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d4aa4-209">Related topics</span></span>


[<span data-ttu-id="d4aa4-210">Требования клиента Application Virtualization к оборудованию и программному обеспечению</span><span class="sxs-lookup"><span data-stu-id="d4aa4-210">Application Virtualization Client Hardware and Software Requirements</span></span>](application-virtualization-client-hardware-and-software-requirements.md)

[<span data-ttu-id="d4aa4-211">Требования к системе при работе с Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="d4aa4-211">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="d4aa4-212">Установка программы Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="d4aa4-212">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)

[<span data-ttu-id="d4aa4-213">Обновление программы Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="d4aa4-213">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

 

 





