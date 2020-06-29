---
title: Определение необходимости изменения или обновления пакета виртуального приложения
description: Определение необходимости изменения или обновления пакета виртуального приложения
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817502"
---
# <span data-ttu-id="4b952-103">Определение необходимости изменения или обновления пакета виртуального приложения</span><span class="sxs-lookup"><span data-stu-id="4b952-103">How to Determine Whether to Edit or Upgrade a Virtual Application Package</span></span>


<span data-ttu-id="4b952-104">Используйте следующую таблицу, чтобы определить, можно ли открыть виртуальный пакет приложения для редактирования, нужно ли создавать новую версию пакета, или один из доступных вариантов — с помощью секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="4b952-104">Use the following table to help determine whether a virtual application package can be opened for edit, whether you need to create a new version of the package, or whether either option is available, using the App-V Sequencer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4b952-105">Действие</span><span class="sxs-lookup"><span data-stu-id="4b952-105">Action</span></span></th>
<th align="left"><span data-ttu-id="4b952-106">Открыть для редактирования</span><span class="sxs-lookup"><span data-stu-id="4b952-106">Open for edit</span></span></th>
<th align="left"><span data-ttu-id="4b952-107">Открыть для обновления</span><span class="sxs-lookup"><span data-stu-id="4b952-107">Open for upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b952-108">Просмотр свойств пакета.</span><span class="sxs-lookup"><span data-stu-id="4b952-108">View package properties.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-109">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-109">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-110">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-110">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b952-111">Просмотр журнала изменений в пакете.</span><span class="sxs-lookup"><span data-stu-id="4b952-111">View package change history.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-112">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-112">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-113">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-113">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b952-114">Просмотр связанных файлов пакетов.</span><span class="sxs-lookup"><span data-stu-id="4b952-114">View associated package files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-115">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-115">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-116">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-116">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b952-117">Редактирование параметров реестра.</span><span class="sxs-lookup"><span data-stu-id="4b952-117">Edit registry settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-118">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-118">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-119">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-119">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b952-120">Ознакомьтесь с дополнительными параметрами пакета (кроме свойств файла операционной системы).</span><span class="sxs-lookup"><span data-stu-id="4b952-120">Review additional package settings (except operating system file properties).</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-121">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-121">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-122">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b952-123">Создание связанного установщика Windows (MSI).</span><span class="sxs-lookup"><span data-stu-id="4b952-123">Create associated Windows Installer (MSI).</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-124">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-124">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-125">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-125">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b952-126">Изменить OSD файл.</span><span class="sxs-lookup"><span data-stu-id="4b952-126">Modify OSD file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-127">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-127">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-128">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b952-129">Сжатие и распаковка пакета.</span><span class="sxs-lookup"><span data-stu-id="4b952-129">Compress and uncompress package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-130">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-130">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-131">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b952-132">Добавление сопоставлений типов файлов.</span><span class="sxs-lookup"><span data-stu-id="4b952-132">Add file type associations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-133">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-133">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-134">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-134">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b952-135">Переименование сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="4b952-135">Rename shortcuts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-136">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-136">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-137">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-137">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b952-138">Задает состояние виртуальной клавиши в реестре (переопределение/слияние).</span><span class="sxs-lookup"><span data-stu-id="4b952-138">Set virtualized registry key state (override / merge).</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-139">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-139">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-140">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-140">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b952-141">Настройте состояние виртуализированной папки.</span><span class="sxs-lookup"><span data-stu-id="4b952-141">Set virtualized folder state.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-142">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-142">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-143">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-143">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b952-144">Изменение сопоставлений виртуальной файловой системы.</span><span class="sxs-lookup"><span data-stu-id="4b952-144">Edit virtual file system mappings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-145">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-146">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b952-147">Ознакомьтесь со всеми свойствами файлов операционной системы, связанными с пакетом.</span><span class="sxs-lookup"><span data-stu-id="4b952-147">Review all associated operating system file properties for a package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-148">Нет</span><span class="sxs-lookup"><span data-stu-id="4b952-148">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-149">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-149">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b952-150">Добавление дополнительных служб.</span><span class="sxs-lookup"><span data-stu-id="4b952-150">Add additional services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-151">Нет</span><span class="sxs-lookup"><span data-stu-id="4b952-151">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-152">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b952-153">Добавление дополнительных файлов.</span><span class="sxs-lookup"><span data-stu-id="4b952-153">Add additional files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-154">Нет</span><span class="sxs-lookup"><span data-stu-id="4b952-154">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-155">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b952-156">Соберите и настройте соответствующие дескрипторы безопасности.</span><span class="sxs-lookup"><span data-stu-id="4b952-156">Collect and configure associated security descriptors.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-157">Нет</span><span class="sxs-lookup"><span data-stu-id="4b952-157">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-158">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b952-159">Примените обновления для системы безопасности или обновите ее до новой версии.</span><span class="sxs-lookup"><span data-stu-id="4b952-159">Apply security updates or upgrade to a new version.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-160">Нет</span><span class="sxs-lookup"><span data-stu-id="4b952-160">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-161">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-161">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b952-162">Добавьте дополнительное приложение.</span><span class="sxs-lookup"><span data-stu-id="4b952-162">Add an additional application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-163">Нет</span><span class="sxs-lookup"><span data-stu-id="4b952-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-164">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-164">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b952-165">Примените обновления, для которых требуется открыть приложение.</span><span class="sxs-lookup"><span data-stu-id="4b952-165">Apply updates that require the application to open.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-166">Нет</span><span class="sxs-lookup"><span data-stu-id="4b952-166">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-167">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b952-168">Примените обновления, требующие перезагрузки компьютера.</span><span class="sxs-lookup"><span data-stu-id="4b952-168">Apply updates that require the computer to restart.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-169">Нет</span><span class="sxs-lookup"><span data-stu-id="4b952-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b952-170">Да</span><span class="sxs-lookup"><span data-stu-id="4b952-170">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4b952-171">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="4b952-171">Related topics</span></span>


[<span data-ttu-id="4b952-172">Изменение существующего виртуального приложения</span><span class="sxs-lookup"><span data-stu-id="4b952-172">How to Edit an Existing Virtual Application</span></span>](how-to-edit-an-existing-virtual-application.md)

[<span data-ttu-id="4b952-173">Обновление существующего виртуального приложения</span><span class="sxs-lookup"><span data-stu-id="4b952-173">How to Upgrade an Existing Virtual Application</span></span>](how-to-upgrade-an-existing-virtual-application.md)

 

 





