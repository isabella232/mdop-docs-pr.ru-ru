---
title: Страница "Дополнительные параметры" мастера последовательностей виртуализации приложений
description: Страница "Дополнительные параметры" мастера последовательностей виртуализации приложений
author: dansimp
ms.assetid: 2c4c5d95-d55e-463d-a851-8486f6a724f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 716fa27852f1cadfebec31a267ce1b9b581b8ff7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819599"
---
# <span data-ttu-id="b1d6b-103">Страница "Дополнительные параметры" мастера последовательностей виртуализации приложений</span><span class="sxs-lookup"><span data-stu-id="b1d6b-103">Application Virtualization Sequencing Wizard Advanced Options Page</span></span>


<span data-ttu-id="b1d6b-104">На странице " **Дополнительные параметры** " мастера виртуализации приложений (App-V) можно указать дополнительные параметры для установки приложения.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-104">Use the **Advanced Options** page of the Application Virtualization (App-V) Sequencing Wizard to specify advanced options for the application to be installed.</span></span> <span data-ttu-id="b1d6b-105">На странице содержатся элементы, описанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-105">The page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b1d6b-106">Имя</span><span class="sxs-lookup"><span data-stu-id="b1d6b-106">Name</span></span></th>
<th align="left"><span data-ttu-id="b1d6b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b1d6b-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b1d6b-108">Размер блока</span><span class="sxs-lookup"><span data-stu-id="b1d6b-108">Block Size</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b1d6b-109">Используется для указания размера блоков, на которые будет разбит файл SFT при потоковой передаче по сети.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-109">Use to specify the size of blocks that the SFT file will be divided into when streamed across a network.</span></span> <span data-ttu-id="b1d6b-110">Все блоки, размер которых равен указанному значению; Однако последний блок может быть меньше указанного.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-110">All blocks equal the specified size; however, the last block might be smaller than specified.</span></span> <span data-ttu-id="b1d6b-111">Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b1d6b-111">Select one of the following values:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="b1d6b-112">4 КБ</span><span class="sxs-lookup"><span data-stu-id="b1d6b-112">4 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="b1d6b-113">16 КБ</span><span class="sxs-lookup"><span data-stu-id="b1d6b-113">16 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="b1d6b-114">32 КБ</span><span class="sxs-lookup"><span data-stu-id="b1d6b-114">32 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="b1d6b-115">64 КБ</span><span class="sxs-lookup"><span data-stu-id="b1d6b-115">64 KB</span></span></strong></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="b1d6b-116">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-116">Note</span></span></strong><br/><p><span data-ttu-id="b1d6b-117">При выборе размера блока учитывайте размер SFT-файла и пропускной способности сети.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-117">When you select a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="b1d6b-118">Файл с меньшим размером блока занимает больше времени для потоковой передачи по сети, но менее интенсивно использует пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-118">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="b1d6b-119">Файлы с более крупными размерами блоков могут работать быстрее, но они используют дополнительную пропускную способность сети.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-119">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="b1d6b-120">С помощью экспериментов вы можете найти оптимальный размер блока для потоковой передачи приложений в сети.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-120">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b1d6b-121">Включение центра обновления Майкрософт во время наблюдения</span><span class="sxs-lookup"><span data-stu-id="b1d6b-121">Enable Microsoft Update During Monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b1d6b-122">Позволяет устанавливать обновления Майкрософт на этапе мониторинга мастера виртуализации&#39;s.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-122">Enables installation of Microsoft Updates during the Sequencing Wizard&#39;s monitoring phase.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b1d6b-123">Перебазовые библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="b1d6b-123">Rebase DLLs</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b1d6b-124">Позволяет повторно сопоставлять Поддерживаемые библиотеки динамической компоновки с непрерывным пространством в ОЗУ, экономя память и повышая производительность.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-124">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM, saving memory and improving performance.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b1d6b-125">Back</span><span class="sxs-lookup"><span data-stu-id="b1d6b-125">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b1d6b-126">Доступ к мастеру последовательностей&#39;s предыдущей страницей.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-126">Accesses the Sequencing Wizard&#39;s previous page.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b1d6b-127">Next</span><span class="sxs-lookup"><span data-stu-id="b1d6b-127">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b1d6b-128">Доступ к мастеру последовательностей&#39;s на следующую страницу.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-128">Accesses the Sequencing Wizard&#39;s next page.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b1d6b-129">Отмена</span><span class="sxs-lookup"><span data-stu-id="b1d6b-129">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b1d6b-130">Прекращение работы мастера виртуализации.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-130">Terminates operation of the Sequencing Wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="b1d6b-131">\ [Значение маркера шаблона \]</span><span class="sxs-lookup"><span data-stu-id="b1d6b-131">\[Template Token Value\]</span></span>

<span data-ttu-id="b1d6b-132">На странице **Дополнительные параметры** мастера последовательностей App-V можно указать дополнительные параметры для упорядочения приложения.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-132">Use the **Advanced Options** page of the App-V Sequencing Wizard to specify advanced options for the application you are sequencing.</span></span> <span data-ttu-id="b1d6b-133">На этой странице содержатся элементы, описанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-133">This page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b1d6b-134">Имя</span><span class="sxs-lookup"><span data-stu-id="b1d6b-134">Name</span></span></th>
<th align="left"><span data-ttu-id="b1d6b-135">Описание</span><span class="sxs-lookup"><span data-stu-id="b1d6b-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b1d6b-136">Разрешение запуска центра обновления Майкрософт во время наблюдения</span><span class="sxs-lookup"><span data-stu-id="b1d6b-136">Allow Microsoft Update to run during monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b1d6b-137">Определяет, будут ли в приложение применяться обновления программного обеспечения на этапе мониторинга последовательности приложений.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-137">Specifies whether software updates will be applied to the application during the monitoring phase of application sequencing.</span></span> <span data-ttu-id="b1d6b-138">Этот параметр полезен, если для успешного завершения установки приложения требуются обновления.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-138">This option is helpful if updates are required to successfully complete the application installation.</span></span> <span data-ttu-id="b1d6b-139">Этот параметр не выбран по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-139">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b1d6b-140">Перебазовые библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="b1d6b-140">Rebase Dlls</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b1d6b-141">Позволяет повторно сопоставить Поддерживаемые библиотеки динамической компоновки с непрерывным пространством в ОЗУ.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-141">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM.</span></span> <span data-ttu-id="b1d6b-142">Выбор этого параметра помогает управлять памятью и повышать производительность приложения.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-142">Selecting this option can help manage memory and improve application performance.</span></span> <span data-ttu-id="b1d6b-143">Этот параметр не выбран по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-143">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b1d6b-144">Back</span><span class="sxs-lookup"><span data-stu-id="b1d6b-144">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b1d6b-145">Переход на предыдущую страницу мастера.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-145">Goes to the previous page of the wizard.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b1d6b-146">Next</span><span class="sxs-lookup"><span data-stu-id="b1d6b-146">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b1d6b-147">Переход на следующую страницу мастера.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-147">Goes to the next page of the wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b1d6b-148">Отмена</span><span class="sxs-lookup"><span data-stu-id="b1d6b-148">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b1d6b-149">Отмена параметров и выход из мастера.</span><span class="sxs-lookup"><span data-stu-id="b1d6b-149">Discards the settings and exits the wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="b1d6b-150">\ [Значение маркера шаблона \]</span><span class="sxs-lookup"><span data-stu-id="b1d6b-150">\[Template Token Value\]</span></span>

## <span data-ttu-id="b1d6b-151">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b1d6b-151">Related topics</span></span>


[<span data-ttu-id="b1d6b-152">Мастер виртуализации</span><span class="sxs-lookup"><span data-stu-id="b1d6b-152">Sequencing Wizard</span></span>](sequencing-wizard.md)









