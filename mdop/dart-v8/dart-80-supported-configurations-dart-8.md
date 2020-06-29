---
title: Поддерживаемые конфигурации в DaRT 8.0
description: Поддерживаемые конфигурации в DaRT 8.0
author: dansimp
ms.assetid: 95d68e5c-d202-4f4a-adef-d2098328172e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02c891555992652bf2a9b2b674ab8377536ef9d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823929"
---
# <span data-ttu-id="be88a-103">Поддерживаемые конфигурации в DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="be88a-103">DaRT 8.0 Supported Configurations</span></span>


<span data-ttu-id="be88a-104">В этой статье указаны требования к программному обеспечению и поддерживаемые конфигурации, необходимые для установки и запуска средств диагностики и восстановления Microsoft (DaRT) 8,0 в среде.</span><span class="sxs-lookup"><span data-stu-id="be88a-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 in your environment.</span></span> <span data-ttu-id="be88a-105">Указаны требования к операционной системе и требования к системе, необходимые для запуска DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="be88a-105">Both the operating system requirements and the system requirements that are required to run DaRT 8.0 are specified.</span></span> <span data-ttu-id="be88a-106">Сведения о предварительных требованиях для создания изображения для восстановления DaRT можно найти в разделе [планирование создания образа для восстановления dart 8,0](planning-to-create-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="be88a-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 8.0 Recovery Image](planning-to-create-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="be88a-107">Для поддерживаемых конфигураций, которые относятся к более поздним выпускам, ознакомьтесь с документацией по соответствующему выпуску.</span><span class="sxs-lookup"><span data-stu-id="be88a-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="be88a-108">Вы можете установить DaRT одним из двух способов.</span><span class="sxs-lookup"><span data-stu-id="be88a-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="be88a-109">Вы можете установить все возможности на компьютере администратора, где будут выполняться все задачи, связанные с выполнением DaRT.</span><span class="sxs-lookup"><span data-stu-id="be88a-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="be88a-110">Кроме того, вы можете установить на компьютер администратора, только функцию DaRT, которая создает образ восстановления, а затем установить функции, используемые для запуска DaRT (то есть средство просмотра удаленного подключения DaRT) на компьютере службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="be88a-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <a href="" id="---------dart-8-0-prerequisite-software"></a> <span data-ttu-id="be88a-111">DaRT 8,0 необходимое программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="be88a-111">DaRT 8.0 prerequisite software</span></span>


<span data-ttu-id="be88a-112">Перед установкой DaRT убедитесь, что выполнены следующие предварительные требования.</span><span class="sxs-lookup"><span data-stu-id="be88a-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="be88a-113">Требования для компьютера администратора</span><span class="sxs-lookup"><span data-stu-id="be88a-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="be88a-114">В приведенной ниже таблице перечислены требования к установке для компьютера администратора при установке DaRT 8,0 и всех инструментов DaRT.</span><span class="sxs-lookup"><span data-stu-id="be88a-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 8.0 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be88a-115">Предварительные</span><span class="sxs-lookup"><span data-stu-id="be88a-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="be88a-116">Сведения</span><span class="sxs-lookup"><span data-stu-id="be88a-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="be88a-117">Комплект средств для оценки и разработки Windows (ADK)</span><span class="sxs-lookup"><span data-stu-id="be88a-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be88a-118">Обязательный для мастера создания изображений для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="be88a-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="be88a-119">В нем содержатся инструменты развертывания, которые используются для настройки, развертывания и обслуживания образов Windows, а также для работы со средой предварительной установки Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="be88a-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="be88a-120">При установке только средства просмотра удаленных подключений и (или) Crash Analyzer не требуется ADK.</span><span class="sxs-lookup"><span data-stu-id="be88a-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="be88a-121">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="be88a-121">.NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be88a-122">Требуется мастером создания изображений для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="be88a-122">Required by the DaRT Recovery Image wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="be88a-123">Комплект средств разработки для Windows или пакет средств разработки программного обеспечения (необязательно)</span><span class="sxs-lookup"><span data-stu-id="be88a-123">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be88a-124">Для анализа файлов дампа памяти анализатору отказа требуется средство отладки Windows 8 из комплекта драйверов для Windows.</span><span class="sxs-lookup"><span data-stu-id="be88a-124">Crash Analyzer requires the Windows 8 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="be88a-125">Образ ISO для Windows 8 64-bit</span><span class="sxs-lookup"><span data-stu-id="be88a-125">Windows 8 64-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be88a-126">Для DaRT требуется образ среды восстановления Windows (Windows RE) с носителя Windows 8.</span><span class="sxs-lookup"><span data-stu-id="be88a-126">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 8 media.</span></span> <span data-ttu-id="be88a-127">Загрузите 32-разрядную или 64-разрядную версию Windows 8 в зависимости от типа изображения для восстановления DaRT, которое вы хотите создать.</span><span class="sxs-lookup"><span data-stu-id="be88a-127">Download the 32-bit or 64-bit version of Windows 8, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="be88a-128">Если в вашей среде поддерживаются оба типа систем, загрузите обе версии Windows 8.</span><span class="sxs-lookup"><span data-stu-id="be88a-128">If you support both system types in your environment, download both versions of Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="be88a-129">Необходимые условия для поддержки справочной системы</span><span class="sxs-lookup"><span data-stu-id="be88a-129">Help desk computer prerequisites</span></span>

<span data-ttu-id="be88a-130">В приведенной ниже таблице перечислены требования к установке для компьютера службы поддержки, когда вы используете средство для просмотра удаленных подключений DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="be88a-130">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 8.0 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be88a-131">Предварительные</span><span class="sxs-lookup"><span data-stu-id="be88a-131">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="be88a-132">Сведения</span><span class="sxs-lookup"><span data-stu-id="be88a-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="be88a-133">DaRT 8,0 средство просмотра удаленных подключений</span><span class="sxs-lookup"><span data-stu-id="be88a-133">DaRT 8.0 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be88a-134">Должен быть установлен в операционной системе Windows 8.</span><span class="sxs-lookup"><span data-stu-id="be88a-134">Must be installed on a Windows 8 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="be88a-135">NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="be88a-135">NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be88a-136">Обязательно для мастера изображений для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="be88a-136">Required by the DaRT Recovery Image wizard</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="be88a-137">Средства отладки для Windows</span><span class="sxs-lookup"><span data-stu-id="be88a-137">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be88a-138">Требуется только при установке средства анализа аварийного восстановления</span><span class="sxs-lookup"><span data-stu-id="be88a-138">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="be88a-139">Предварительные требования к компьютеру конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="be88a-139">End-user computer prerequisites</span></span>

<span data-ttu-id="be88a-140">Отсутствует необходимое программное обеспечение, которое должно быть установлено на компьютерах конечных пользователей, кроме операционной системы Windows 8.</span><span class="sxs-lookup"><span data-stu-id="be88a-140">There is no prerequisite software that must be installed on end-user computers, other than the Windows 8 operating system.</span></span>

## <a href="" id="---------dart-operating-system-requirements"></a> <span data-ttu-id="be88a-141">Технические требования к операционной системе DaRT</span><span class="sxs-lookup"><span data-stu-id="be88a-141">DaRT operating system requirements</span></span>


### <span data-ttu-id="be88a-142">Системные требования для компьютера администратора</span><span class="sxs-lookup"><span data-stu-id="be88a-142">Administrator computer system requirements</span></span>

<span data-ttu-id="be88a-143">В таблице ниже перечислены операционные системы, которые поддерживаются при установке компьютера администратора DaRT.</span><span class="sxs-lookup"><span data-stu-id="be88a-143">The following table lists the operating systems that are supported for the DaRT administrator computer installation.</span></span>

<span data-ttu-id="be88a-144">**Примечание**  Убедитесь, что на компьютере администратора выделяются все дополнительные инструменты, которые вы хотите установить.</span><span class="sxs-lookup"><span data-stu-id="be88a-144">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="be88a-145">**Примечание**  Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="be88a-145">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="be88a-146">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="be88a-146">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="be88a-147">Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="be88a-147">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be88a-148">Операционная система</span><span class="sxs-lookup"><span data-stu-id="be88a-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="be88a-149">Выпуск</span><span class="sxs-lookup"><span data-stu-id="be88a-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="be88a-150">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="be88a-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="be88a-151">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="be88a-151">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="be88a-152">Требования к операционной системе</span><span class="sxs-lookup"><span data-stu-id="be88a-152">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="be88a-153">Требования к ОЗУ для запуска DaRT</span><span class="sxs-lookup"><span data-stu-id="be88a-153">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be88a-154">Windows8</span><span class="sxs-lookup"><span data-stu-id="be88a-154">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-155">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="be88a-155">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-156">Н/Д</span><span class="sxs-lookup"><span data-stu-id="be88a-156">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-157">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="be88a-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-158">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-158">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-159">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-159">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be88a-160">Windows8</span><span class="sxs-lookup"><span data-stu-id="be88a-160">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-161">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="be88a-161">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-162">Н/Д</span><span class="sxs-lookup"><span data-stu-id="be88a-162">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-163">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="be88a-163">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-164">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-164">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-165">1,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-165">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be88a-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be88a-166">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-167">Стандартная, Корпоративная, центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="be88a-167">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-168">Н/Д</span><span class="sxs-lookup"><span data-stu-id="be88a-168">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-169">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="be88a-169">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-170">512 МБ</span><span class="sxs-lookup"><span data-stu-id="be88a-170">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-171">1.0 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-171">1 .0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="be88a-172">DaRT справочные требования к системе технической поддержки</span><span class="sxs-lookup"><span data-stu-id="be88a-172">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="be88a-173">Если вы разрешите службе поддержки удаленно устранять неполадки на компьютерах, на компьютере службы поддержки должна быть установлена программа просмотра удаленных подключений.</span><span class="sxs-lookup"><span data-stu-id="be88a-173">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="be88a-174">При необходимости вы можете установить средство анализа аварийного восстановления на компьютере службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="be88a-174">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="be88a-175">DaRT 8,0 позволяет сотрудникам службы поддержки подключаться к компьютеру с помощью DaRT 8,0 с помощью средства "DaRT 7,0" или DaRT 8,0 Remote Connection.</span><span class="sxs-lookup"><span data-stu-id="be88a-175">DaRT 8.0 enables a help desk worker to connect to a DaRT 8.0 computer by using either the DaRT 7.0 or DaRT 8.0 Remote Connection Viewer.</span></span> <span data-ttu-id="be88a-176">Средство DaRT 7,0 для работы с удаленным подключением использует операционную систему Windows 7, а для программы DaRT 8,0 для удаленного подключения требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="be88a-176">The DaRT 7.0 Remote Connection Viewer requires a Windows 7 operating system, while the DaRT 8.0 Remote Connection Viewer requires Windows 8.</span></span> <span data-ttu-id="be88a-177">Средство DaRT 8,0 с удаленным подключением и все другие инструменты DaRT 8,0 можно установить только на компьютер под управлением Windows 8.</span><span class="sxs-lookup"><span data-stu-id="be88a-177">The DaRT 8.0 Remote Connection Viewer and all other DaRT 8.0 tools can be installed only on a computer running Windows 8.</span></span>

<span data-ttu-id="be88a-178">В таблице ниже перечислены операционные системы, которые поддерживаются для установки на компьютере с помощью функции DaRT Help.</span><span class="sxs-lookup"><span data-stu-id="be88a-178">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be88a-179">Операционная система</span><span class="sxs-lookup"><span data-stu-id="be88a-179">Operating System</span></span></th>
<th align="left"><span data-ttu-id="be88a-180">Выпуск</span><span class="sxs-lookup"><span data-stu-id="be88a-180">Edition</span></span></th>
<th align="left"><span data-ttu-id="be88a-181">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="be88a-181">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="be88a-182">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="be88a-182">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="be88a-183">Требования к операционной системе</span><span class="sxs-lookup"><span data-stu-id="be88a-183">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="be88a-184">Требования к ОЗУ для запуска DaRT</span><span class="sxs-lookup"><span data-stu-id="be88a-184">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be88a-185">Windows8</span><span class="sxs-lookup"><span data-stu-id="be88a-185">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-186">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="be88a-186">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-187">Н/Д</span><span class="sxs-lookup"><span data-stu-id="be88a-187">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-188">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="be88a-188">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-189">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-189">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-190">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-190">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be88a-191">Windows8 (только для средства просмотра удаленных подключений 8,0)</span><span class="sxs-lookup"><span data-stu-id="be88a-191">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-192">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="be88a-192">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-193">Н/Д</span><span class="sxs-lookup"><span data-stu-id="be88a-193">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-194">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="be88a-194">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-195">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-195">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-196">1,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-196">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be88a-197">Windows 7 (только для средства просмотра удаленного подключения 7,0)</span><span class="sxs-lookup"><span data-stu-id="be88a-197">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-198">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="be88a-198">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-199">ПАКЕТ ОБНОВЛЕНИЯ 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="be88a-199">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-200">64-разрядный или 32-разрядный</span><span class="sxs-lookup"><span data-stu-id="be88a-200">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-201">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-201">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-202">Н/Д</span><span class="sxs-lookup"><span data-stu-id="be88a-202">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be88a-203">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be88a-203">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-204">Стандартная, Корпоративная, центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="be88a-204">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-205">Н/Д</span><span class="sxs-lookup"><span data-stu-id="be88a-205">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-206">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="be88a-206">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-207">51</span><span class="sxs-lookup"><span data-stu-id="be88a-207">51</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-208">1,0 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-208">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="be88a-209">Для DaRT также предусмотрены следующие минимальные требования к оборудованию для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="be88a-209">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="be88a-210">CD-или DVD-диск или порт USB — требуется только в том случае, если вы развертываете DaRT на своем предприятии с помощью компакт-диска, DVD-диска или USB.</span><span class="sxs-lookup"><span data-stu-id="be88a-210">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="be88a-211">Поддержка BIOS по запуску компьютера с компакт-диска, DVD-диска, устройства USB или из удаленного или восстановленного раздела.</span><span class="sxs-lookup"><span data-stu-id="be88a-211">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-end-user-computer-system-requirements"></a> <span data-ttu-id="be88a-212">Системные требования DaRT для конечных пользователей компьютера</span><span class="sxs-lookup"><span data-stu-id="be88a-212">DaRT end-user computer system requirements</span></span>

<span data-ttu-id="be88a-213">В окне инструментов "Диагностика" и "восстановление" для DaRT требуется, чтобы на компьютере конечного пользователя использовалась одна из следующих операционных систем с указанным объемом системной памяти, доступной для DaRT:</span><span class="sxs-lookup"><span data-stu-id="be88a-213">The Diagnostics and Recovery Toolset window in DaRT requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be88a-214">Операционная система</span><span class="sxs-lookup"><span data-stu-id="be88a-214">Operating System</span></span></th>
<th align="left"><span data-ttu-id="be88a-215">Выпуск</span><span class="sxs-lookup"><span data-stu-id="be88a-215">Edition</span></span></th>
<th align="left"><span data-ttu-id="be88a-216">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="be88a-216">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="be88a-217">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="be88a-217">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="be88a-218">Требования к операционной системе</span><span class="sxs-lookup"><span data-stu-id="be88a-218">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="be88a-219">Требования к ОЗУ</span><span class="sxs-lookup"><span data-stu-id="be88a-219">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be88a-220">Windows8</span><span class="sxs-lookup"><span data-stu-id="be88a-220">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-221">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="be88a-221">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-222">Н/Д</span><span class="sxs-lookup"><span data-stu-id="be88a-222">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-223">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="be88a-223">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-224">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-224">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-225">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-225">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be88a-226">Windows8</span><span class="sxs-lookup"><span data-stu-id="be88a-226">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-227">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="be88a-227">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-228">Н/Д</span><span class="sxs-lookup"><span data-stu-id="be88a-228">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-229">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="be88a-229">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-230">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-230">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-231">1,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-231">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be88a-232">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be88a-232">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-233">Стандартная, Корпоративная, центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="be88a-233">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-234">Н/Д</span><span class="sxs-lookup"><span data-stu-id="be88a-234">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-235">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="be88a-235">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-236">512 МБ</span><span class="sxs-lookup"><span data-stu-id="be88a-236">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="be88a-237">1,0 ГБ</span><span class="sxs-lookup"><span data-stu-id="be88a-237">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="be88a-238">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="be88a-238">Related topics</span></span>


[<span data-ttu-id="be88a-239">Планирование развертывания DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="be88a-239">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





