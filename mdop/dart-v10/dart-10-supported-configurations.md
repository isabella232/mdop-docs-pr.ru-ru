---
title: Поддерживаемые конфигурации в DaRT 10
description: Поддерживаемые конфигурации в DaRT 10
author: dansimp
ms.assetid: a07d6562-1fa9-499f-829c-9cc487ede0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 414b9d5cb7bf78dcfeda3fafc1c476e367709446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813136"
---
# <span data-ttu-id="f99f7-103">Поддерживаемые конфигурации в DaRT 10</span><span class="sxs-lookup"><span data-stu-id="f99f7-103">DaRT 10 Supported Configurations</span></span>


<span data-ttu-id="f99f7-104">В этой статье указаны требования к программному обеспечению и поддерживаемые конфигурации, необходимые для установки и запуска набора средств диагностики и восстановления Microsoft (DaRT) 10 в среде.</span><span class="sxs-lookup"><span data-stu-id="f99f7-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment.</span></span> <span data-ttu-id="f99f7-105">Указаны требования к операционной системе и требования к системе, необходимые для запуска DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="f99f7-105">Both the operating system requirements and the system requirements that are required to run DaRT 10 are specified.</span></span> <span data-ttu-id="f99f7-106">Сведения о предварительных требованиях для создания изображения для восстановления DaRT вы можете найти в разделе [планирование создания образа для восстановления DaRT 10](planning-to-create-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="f99f7-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 10 Recovery Image](planning-to-create-the-dart-10-recovery-image.md).</span></span>

<span data-ttu-id="f99f7-107">Для поддерживаемых конфигураций, которые относятся к более поздним выпускам, ознакомьтесь с документацией по соответствующему выпуску.</span><span class="sxs-lookup"><span data-stu-id="f99f7-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="f99f7-108">Вы можете установить DaRT одним из двух способов.</span><span class="sxs-lookup"><span data-stu-id="f99f7-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="f99f7-109">Вы можете установить все возможности на компьютере администратора, где будут выполняться все задачи, связанные с выполнением DaRT.</span><span class="sxs-lookup"><span data-stu-id="f99f7-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="f99f7-110">Кроме того, вы можете установить на компьютер администратора, только функцию DaRT, которая создает образ восстановления, а затем установить функции, используемые для запуска DaRT (то есть средство просмотра удаленного подключения DaRT) на компьютере службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="f99f7-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <span data-ttu-id="f99f7-111">DaRT 10 необходимое программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="f99f7-111">DaRT 10 prerequisite software</span></span>


<span data-ttu-id="f99f7-112">Перед установкой DaRT убедитесь, что выполнены следующие предварительные требования.</span><span class="sxs-lookup"><span data-stu-id="f99f7-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="f99f7-113">Требования для компьютера администратора</span><span class="sxs-lookup"><span data-stu-id="f99f7-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="f99f7-114">В приведенной ниже таблице перечислены требования к установке для компьютера администратора при установке DaRT 10 и всех инструментов DaRT.</span><span class="sxs-lookup"><span data-stu-id="f99f7-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 10 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f99f7-115">Предварительные</span><span class="sxs-lookup"><span data-stu-id="f99f7-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="f99f7-116">Сведения</span><span class="sxs-lookup"><span data-stu-id="f99f7-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f99f7-117">Комплект средств для оценки и разработки Windows (ADK)</span><span class="sxs-lookup"><span data-stu-id="f99f7-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f99f7-118">Обязательный для мастера создания изображений для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="f99f7-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="f99f7-119">В нем содержатся инструменты развертывания, которые используются для настройки, развертывания и обслуживания образов Windows, а также для работы со средой предварительной установки Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="f99f7-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="f99f7-120">При установке только средства просмотра удаленных подключений и (или) Crash Analyzer не требуется ADK.</span><span class="sxs-lookup"><span data-stu-id="f99f7-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f99f7-121">Комплект средств разработки для Windows или пакет средств разработки программного обеспечения (необязательно)</span><span class="sxs-lookup"><span data-stu-id="f99f7-121">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f99f7-122">Для анализа файлов дампа памяти анализатору отказа требуется средство отладки Windows 10 из комплекта драйверов для Windows.</span><span class="sxs-lookup"><span data-stu-id="f99f7-122">Crash Analyzer requires the Windows 10 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f99f7-123">Образ ISO для Windows 10 64-bit или 32-bit</span><span class="sxs-lookup"><span data-stu-id="f99f7-123">Windows 10 64-bit or 32-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f99f7-124">Для DaRT требуется образ среды восстановления Windows (Windows RE) с носителя Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f99f7-124">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 10 media.</span></span> <span data-ttu-id="f99f7-125">Загрузите 32-разрядную или 64-разрядную версию Windows 10, в зависимости от типа изображения для восстановления DaRT, которое вы хотите создать.</span><span class="sxs-lookup"><span data-stu-id="f99f7-125">Download the 32-bit or 64-bit version of Windows 10, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="f99f7-126">Если в вашей среде поддерживаются оба типа систем, загрузите обе версии Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f99f7-126">If you support both system types in your environment, download both versions of Windows 10.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f99f7-127">Необходимые условия для поддержки справочной системы</span><span class="sxs-lookup"><span data-stu-id="f99f7-127">Help desk computer prerequisites</span></span>

<span data-ttu-id="f99f7-128">В приведенной ниже таблице перечислены требования к установке для компьютера службы поддержки, когда вы запускаете средство просмотра удаленных подключений DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="f99f7-128">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 10 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f99f7-129">Предварительные</span><span class="sxs-lookup"><span data-stu-id="f99f7-129">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="f99f7-130">Сведения</span><span class="sxs-lookup"><span data-stu-id="f99f7-130">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f99f7-131">DaRT 10 Remote Connection Viewer</span><span class="sxs-lookup"><span data-stu-id="f99f7-131">DaRT 10 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f99f7-132">Должен быть установлен в операционной системе Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f99f7-132">Must be installed on a Windows 10 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f99f7-133">Средства отладки для Windows</span><span class="sxs-lookup"><span data-stu-id="f99f7-133">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f99f7-134">Требуется только при установке средства анализа аварийного восстановления</span><span class="sxs-lookup"><span data-stu-id="f99f7-134">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f99f7-135">Предварительные требования к компьютеру конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="f99f7-135">End-user computer prerequisites</span></span>

<span data-ttu-id="f99f7-136">Отсутствует необходимое программное обеспечение, которое должно быть установлено на компьютерах конечных пользователей, кроме операционной системы Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f99f7-136">There is no prerequisite software that must be installed on end-user computers, other than the Windows 10 operating system.</span></span>

## <a href="" id="---------dart-10-operating-system-requirements"></a> <span data-ttu-id="f99f7-137">DaRT 10 требования к операционной системе</span><span class="sxs-lookup"><span data-stu-id="f99f7-137">DaRT 10 operating system requirements</span></span>


### <span data-ttu-id="f99f7-138">Системные требования для компьютера администратора</span><span class="sxs-lookup"><span data-stu-id="f99f7-138">Administrator computer system requirements</span></span>

<span data-ttu-id="f99f7-139">В таблице ниже перечислены операционные системы, которые поддерживаются установкой на компьютере администратора DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="f99f7-139">The following table lists the operating systems that are supported for the DaRT 10 administrator computer installation.</span></span>

<span data-ttu-id="f99f7-140">**Примечание**  Убедитесь, что на компьютере администратора выделяются все дополнительные инструменты, которые вы хотите установить.</span><span class="sxs-lookup"><span data-stu-id="f99f7-140">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="f99f7-141">**Примечание**  Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="f99f7-141">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="f99f7-142">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="f99f7-142">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="f99f7-143">Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f99f7-143">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

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
<th align="left"><span data-ttu-id="f99f7-144">Операционная система</span><span class="sxs-lookup"><span data-stu-id="f99f7-144">Operating System</span></span></th>
<th align="left"><span data-ttu-id="f99f7-145">Выпуск</span><span class="sxs-lookup"><span data-stu-id="f99f7-145">Edition</span></span></th>
<th align="left"><span data-ttu-id="f99f7-146">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="f99f7-146">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="f99f7-147">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="f99f7-147">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="f99f7-148">Требования к операционной системе</span><span class="sxs-lookup"><span data-stu-id="f99f7-148">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="f99f7-149">Требования к ОЗУ для запуска DaRT</span><span class="sxs-lookup"><span data-stu-id="f99f7-149">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f99f7-150">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f99f7-150">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-151">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="f99f7-151">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-152">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f99f7-152">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-153">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="f99f7-153">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-154">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-154">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-155">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-155">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f99f7-156">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f99f7-156">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-157">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="f99f7-157">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-158">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f99f7-158">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-159">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="f99f7-159">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-160">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-160">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-161">1,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-161">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="f99f7-162">DaRT справочные требования к системе технической поддержки</span><span class="sxs-lookup"><span data-stu-id="f99f7-162">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="f99f7-163">Если вы разрешите службе поддержки удаленно устранять неполадки на компьютерах, на компьютере службы поддержки должна быть установлена программа просмотра удаленных подключений.</span><span class="sxs-lookup"><span data-stu-id="f99f7-163">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="f99f7-164">При необходимости вы можете установить средство анализа аварийного восстановления на компьютере службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="f99f7-164">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="f99f7-165">DaRT 10 позволяет сотрудникам службы поддержки подключаться к компьютеру с DaRT 10 с помощью DaRT 7,0, DaRT 8,0, DaRt 8,1 или DaRT 10 Remote Connection Viewer.</span><span class="sxs-lookup"><span data-stu-id="f99f7-165">DaRT 10 enables a help desk worker to connect to a DaRT 10 computer by using either the DaRT 7.0, DaRT 8.0, DaRt 8.1, or DaRT 10 Remote Connection Viewer.</span></span> <span data-ttu-id="f99f7-166">Для стрелок DaRT 7,0, DaRT 8,0 и DaRt 8,1, для просмотра удаленных подключений требуется операционная система Windows 7, Windows 8 или Windows 8,1, в то время как в средстве просмотра удаленного подключения для DaRT 10 требуется Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f99f7-166">The DaRT 7.0, DaRT 8.0 and DaRt 8.1, Remote Connection Viewers require Windows 7, Windows 8, or Windows 8.1 operating systems respectively, while the DaRT 10 Remote Connection Viewer requires Windows 10.</span></span> <span data-ttu-id="f99f7-167">Средство просмотра удаленных подключений DaRT 10 и все другие инструменты DaRT 10 можно установить только на компьютер под управлением Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f99f7-167">The DaRT 10 Remote Connection Viewer and all other DaRT 10 tools can be installed only on a computer running Windows 10.</span></span>

<span data-ttu-id="f99f7-168">В таблице ниже перечислены операционные системы, которые поддерживаются для установки на компьютере с помощью функции DaRT Help.</span><span class="sxs-lookup"><span data-stu-id="f99f7-168">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

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
<th align="left"><span data-ttu-id="f99f7-169">Операционная система</span><span class="sxs-lookup"><span data-stu-id="f99f7-169">Operating System</span></span></th>
<th align="left"><span data-ttu-id="f99f7-170">Выпуск</span><span class="sxs-lookup"><span data-stu-id="f99f7-170">Edition</span></span></th>
<th align="left"><span data-ttu-id="f99f7-171">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="f99f7-171">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="f99f7-172">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="f99f7-172">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="f99f7-173">Требования к операционной системе</span><span class="sxs-lookup"><span data-stu-id="f99f7-173">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="f99f7-174">Требования к ОЗУ для запуска DaRT</span><span class="sxs-lookup"><span data-stu-id="f99f7-174">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f99f7-175">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f99f7-175">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-176">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="f99f7-176">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-177">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f99f7-177">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-178">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="f99f7-178">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-179">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-179">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-180">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-180">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f99f7-181">Windows10 (только для средства просмотра удаленных подключений 10,0)</span><span class="sxs-lookup"><span data-stu-id="f99f7-181">Windows10 (with Remote Connection Viewer 10.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-182">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="f99f7-182">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-183">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f99f7-183">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-184">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="f99f7-184">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-185">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-185">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-186">1,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-186">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f99f7-187">Windows8</span><span class="sxs-lookup"><span data-stu-id="f99f7-187">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-188">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="f99f7-188">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-189">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f99f7-189">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-190">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="f99f7-190">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-191">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-191">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-192">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-192">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f99f7-193">Windows8 (только для средства просмотра удаленных подключений 8,0)</span><span class="sxs-lookup"><span data-stu-id="f99f7-193">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-194">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="f99f7-194">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-195">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f99f7-195">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-196">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="f99f7-196">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-197">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-197">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-198">1,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-198">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f99f7-199">Windows 7 (только для средства просмотра удаленного подключения 7,0)</span><span class="sxs-lookup"><span data-stu-id="f99f7-199">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-200">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="f99f7-200">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-201">ПАКЕТ ОБНОВЛЕНИЯ 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="f99f7-201">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-202">64-разрядный или 32-разрядный</span><span class="sxs-lookup"><span data-stu-id="f99f7-202">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-203">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-203">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-204">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f99f7-204">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f99f7-205">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f99f7-205">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-206">Стандартная, Корпоративная, центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="f99f7-206">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-207">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f99f7-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-208">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="f99f7-208">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-209">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-209">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-210">1,0 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-210">1.0 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f99f7-211">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f99f7-211">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-212">Стандартная, Корпоративная, центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="f99f7-212">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-213">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f99f7-213">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-214">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="f99f7-214">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-215">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-215">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-216">1,0 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-216">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f99f7-217">Для DaRT также предусмотрены следующие минимальные требования к оборудованию для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="f99f7-217">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="f99f7-218">CD-или DVD-диск или порт USB — требуется только в том случае, если вы развертываете DaRT на своем предприятии с помощью компакт-диска, DVD-диска или USB.</span><span class="sxs-lookup"><span data-stu-id="f99f7-218">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="f99f7-219">Поддержка BIOS по запуску компьютера с компакт-диска, DVD-диска, устройства USB или из удаленного или восстановленного раздела.</span><span class="sxs-lookup"><span data-stu-id="f99f7-219">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-10-end-user-computer-system-requirements"></a> <span data-ttu-id="f99f7-220">DaRT 10 требования к системе для компьютеров конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="f99f7-220">DaRT 10 end-user computer system requirements</span></span>

<span data-ttu-id="f99f7-221">В окне инструментов для диагностики и восстановления на DaRT 10 требуется, чтобы на компьютере конечного пользователя использовалась одна из следующих операционных систем с указанным объемом системной памяти, доступной для DaRT:</span><span class="sxs-lookup"><span data-stu-id="f99f7-221">The Diagnostics and Recovery Toolset window in DaRT 10 requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

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
<th align="left"><span data-ttu-id="f99f7-222">Операционная система</span><span class="sxs-lookup"><span data-stu-id="f99f7-222">Operating System</span></span></th>
<th align="left"><span data-ttu-id="f99f7-223">Выпуск</span><span class="sxs-lookup"><span data-stu-id="f99f7-223">Edition</span></span></th>
<th align="left"><span data-ttu-id="f99f7-224">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="f99f7-224">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="f99f7-225">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="f99f7-225">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="f99f7-226">Требования к операционной системе</span><span class="sxs-lookup"><span data-stu-id="f99f7-226">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="f99f7-227">Требования к ОЗУ</span><span class="sxs-lookup"><span data-stu-id="f99f7-227">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f99f7-228">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f99f7-228">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-229">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="f99f7-229">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-230">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f99f7-230">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-231">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="f99f7-231">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-232">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-232">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-233">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-233">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f99f7-234">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f99f7-234">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-235">Все выпуски</span><span class="sxs-lookup"><span data-stu-id="f99f7-235">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-236">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f99f7-236">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-237">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="f99f7-237">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-238">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-238">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f99f7-239">1,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="f99f7-239">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f99f7-240">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f99f7-240">Related topics</span></span>


[<span data-ttu-id="f99f7-241">Планирование развертывания DaRT 10</span><span class="sxs-lookup"><span data-stu-id="f99f7-241">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 





