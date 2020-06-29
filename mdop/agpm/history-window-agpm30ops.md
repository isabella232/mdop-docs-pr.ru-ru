---
title: Окно "Журнал"
description: Окно "Журнал"
author: dansimp
ms.assetid: 114f50a4-508d-4589-b006-6cd05cffe6b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81911b5103c76e267d806fb7cd8acf55811440c9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820799"
---
# <span data-ttu-id="6a158-103">Окно "Журнал"</span><span class="sxs-lookup"><span data-stu-id="6a158-103">History Window</span></span>


<span data-ttu-id="6a158-104">История объекта групповой политики (GPO) может быть отображена двойным щелчком GPO или щелчком правой кнопкой мыши и выбором команды **Журнал**.</span><span class="sxs-lookup"><span data-stu-id="6a158-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="6a158-105">Оно также отображается в **консоли управления групповыми политиками** в качестве вкладки для каждого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6a158-105">It is also displayed in the **Group Policy Management Console** (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="6a158-106">Журнал предоставляет запись событий во время существования выбранного объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6a158-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="6a158-107">В окне **журнала** можно получить отчет о параметрах в версии объекта групповой политики, сравнить несколько версий объекта групповой политики или вернуться к предыдущей версии GPO.</span><span class="sxs-lookup"><span data-stu-id="6a158-107">From the **History** window, you can obtain a report of the settings within a version of the GPO, compare multiple versions of a GPO, or roll back to a previous version of a GPO.</span></span>

## <span data-ttu-id="6a158-108">Фильтрация событий в окне "журнал"</span><span class="sxs-lookup"><span data-stu-id="6a158-108">Filtering events in the History window</span></span>


<span data-ttu-id="6a158-109">На вкладках в окне **журнала** фильтруются состояния объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6a158-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a158-110">Закладок</span><span class="sxs-lookup"><span data-stu-id="6a158-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="6a158-111">Тегов</span><span class="sxs-lookup"><span data-stu-id="6a158-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6a158-112">Все состояния</span><span class="sxs-lookup"><span data-stu-id="6a158-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-113">Отобразить все состояния в истории объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6a158-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6a158-114">Уникальные версии</span><span class="sxs-lookup"><span data-stu-id="6a158-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-115">Отобразить только уникальные версии объекта групповой политики, которые были возвращены в архив.</span><span class="sxs-lookup"><span data-stu-id="6a158-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="6a158-116">Версия, развернутая в производственной среде, сочетания клавиш для уникальных версий и информационные состояния указаны в этом списке.</span><span class="sxs-lookup"><span data-stu-id="6a158-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6a158-117">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="6a158-117">Event information</span></span>


<span data-ttu-id="6a158-118">Информация предоставляется для каждого состояния в журнале объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6a158-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a158-119">Атрибут GPO</span><span class="sxs-lookup"><span data-stu-id="6a158-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="6a158-120">Описание</span><span class="sxs-lookup"><span data-stu-id="6a158-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6a158-121">Изменить дату</span><span class="sxs-lookup"><span data-stu-id="6a158-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-122">Метка времени выполнения действия в <strong> столбце "состояние" </strong> .</span><span class="sxs-lookup"><span data-stu-id="6a158-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6a158-123">Состояние</span><span class="sxs-lookup"><span data-stu-id="6a158-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-124">Состояние в истории объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6a158-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6a158-125">Кем изменено</span><span class="sxs-lookup"><span data-stu-id="6a158-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-126">Пользователь, который вернул или развернул объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6a158-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6a158-127">Comment</span><span class="sxs-lookup"><span data-stu-id="6a158-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-128">Примечание, введенное пользователем, который вернул или развернул объект групповой политики на момент изменения этой версии.</span><span class="sxs-lookup"><span data-stu-id="6a158-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was modified.</span></span> <span data-ttu-id="6a158-129">Полезен для выявления конкретных версий в случае необходимости возврата к предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="6a158-129">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6a158-130">Удаляемый</span><span class="sxs-lookup"><span data-stu-id="6a158-130">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-131">Может ли эта версия объекта групповой политики быть удалена, если число уникальных версий всех объектов групповой политики, сохраненных в архиве, ограничено.</span><span class="sxs-lookup"><span data-stu-id="6a158-131">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="6a158-132">Примечание.</span><span class="sxs-lookup"><span data-stu-id="6a158-132">Note</span></span></strong><br/><p><span data-ttu-id="6a158-133">Вы можете изменить тип удаляемого объекта, щелкнув его правой кнопкой мыши и выбрав команду не <strong> разрешать удаление </strong> или <strong> Разрешить удаление </strong> .</span><span class="sxs-lookup"><span data-stu-id="6a158-133">You can modify whether a version of a GPO is deletable by right-clicking it and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6a158-134">Версия компьютера</span><span class="sxs-lookup"><span data-stu-id="6a158-134">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-135">Автоматически созданная версия части объекта групповой политики на компьютере.</span><span class="sxs-lookup"><span data-stu-id="6a158-135">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6a158-136">Пользовательская версия</span><span class="sxs-lookup"><span data-stu-id="6a158-136">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-137">Автоматически созданная версия части объекта групповой политики пользователя.</span><span class="sxs-lookup"><span data-stu-id="6a158-137">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6a158-138">Состояние объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="6a158-138">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-139">Конфигурацию компьютера и конфигурацию пользователя можно управлять отдельно друг от друга.</span><span class="sxs-lookup"><span data-stu-id="6a158-139">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="6a158-140">Этот статус показывает, какие части объекта групповой политики включены.</span><span class="sxs-lookup"><span data-stu-id="6a158-140">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6a158-141">Фильтр WMI</span><span class="sxs-lookup"><span data-stu-id="6a158-141">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-142">Отобразить все фильтры WMI, примененные к этому объекту групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6a158-142">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="6a158-143">Фильтры WMI управляются в <strong> папке "фильтры WMI" </strong> для домена в дереве консоли консоли управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="6a158-143">WMI filters are managed under the <strong>WMI Filters</strong> folder for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6a158-144">Отчеты</span><span class="sxs-lookup"><span data-stu-id="6a158-144">Reports</span></span>


<span data-ttu-id="6a158-145">На кнопках " **Параметры** " и " **различия** " отображаются отчеты о параметрах GPO для выбранной версии или версий GPO.</span><span class="sxs-lookup"><span data-stu-id="6a158-145">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="6a158-146">Если щелкнуть правой кнопкой мыши версию объекта групповой политики, вы также можете отобразить отчеты на основе XML.</span><span class="sxs-lookup"><span data-stu-id="6a158-146">Right-clicking GPO versions provides the option to display XML-based reports as well.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a158-147">Кнопка</span><span class="sxs-lookup"><span data-stu-id="6a158-147">Button</span></span></th>
<th align="left"><span data-ttu-id="6a158-148">Эффект</span><span class="sxs-lookup"><span data-stu-id="6a158-148">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6a158-149">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a158-149">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-150">Создание отчета на основе HTML, в котором отображаются параметры в выбранной версии объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6a158-150">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6a158-151">Соответствия</span><span class="sxs-lookup"><span data-stu-id="6a158-151">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-152">Создание отчета на основе HTML, который сравнивает параметры в нескольких выбранных версиях объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6a158-152">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="6a158-153">Ключевые для отчетов о различиях</span><span class="sxs-lookup"><span data-stu-id="6a158-153">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a158-154">Символ</span><span class="sxs-lookup"><span data-stu-id="6a158-154">Symbol</span></span></th>
<th align="left"><span data-ttu-id="6a158-155">Значение</span><span class="sxs-lookup"><span data-stu-id="6a158-155">Meaning</span></span></th>
<th align="left"><span data-ttu-id="6a158-156">Цвет</span><span class="sxs-lookup"><span data-stu-id="6a158-156">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a158-157">Нет</span><span class="sxs-lookup"><span data-stu-id="6a158-157">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a158-158">Элемент существует с одинаковыми параметрами в обоих объектах групповой политики</span><span class="sxs-lookup"><span data-stu-id="6a158-158">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a158-159">Зависит от уровня</span><span class="sxs-lookup"><span data-stu-id="6a158-159">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6a158-160">[#]</span><span class="sxs-lookup"><span data-stu-id="6a158-160">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-161">Элемент существует в обоих объектах GPO, но с измененными параметрами</span><span class="sxs-lookup"><span data-stu-id="6a158-161">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a158-162">Синюю</span><span class="sxs-lookup"><span data-stu-id="6a158-162">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6a158-163">[-]</span><span class="sxs-lookup"><span data-stu-id="6a158-163">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-164">Элемент существует только в первом объекте групповой политики</span><span class="sxs-lookup"><span data-stu-id="6a158-164">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a158-165">Красный</span><span class="sxs-lookup"><span data-stu-id="6a158-165">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6a158-166">[+]</span><span class="sxs-lookup"><span data-stu-id="6a158-166">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a158-167">Элемент существует только во втором объекте групповой политики</span><span class="sxs-lookup"><span data-stu-id="6a158-167">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a158-168">Зеленый</span><span class="sxs-lookup"><span data-stu-id="6a158-168">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="6a158-169">Для элементов с измененными параметрами измененные параметры определяются при разворачивании элемента.</span><span class="sxs-lookup"><span data-stu-id="6a158-169">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="6a158-170">Значение атрибута в каждом объекте групповой политики отображается в том же порядке, в котором эти объекты отображаются в отчете.</span><span class="sxs-lookup"><span data-stu-id="6a158-170">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="6a158-171">Некоторые изменения в параметрах могут привести к тому, что элемент будет представлен в виде двух разных элементов (один — только в первый объект групповой политики, один — только во второй), а не как один из измененных элементов.</span><span class="sxs-lookup"><span data-stu-id="6a158-171">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second), rather than as one item that has changed.</span></span>

### <span data-ttu-id="6a158-172">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="6a158-172">Additional references</span></span>

-   [<span data-ttu-id="6a158-173">Вкладка "Содержимое"</span><span class="sxs-lookup"><span data-stu-id="6a158-173">Contents Tab</span></span>](contents-tab-agpm30ops.md)









