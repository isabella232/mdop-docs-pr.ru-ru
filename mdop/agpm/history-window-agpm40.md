---
title: Окно "Журнал"
description: Окно "Журнал"
author: dansimp
ms.assetid: 5bea62e7-d267-40b2-a66d-fb1be7373a1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81f19e3834e945a45238856e23f6ee4a86407c4a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820792"
---
# <span data-ttu-id="6b812-103">Окно "Журнал"</span><span class="sxs-lookup"><span data-stu-id="6b812-103">History Window</span></span>


<span data-ttu-id="6b812-104">История объекта групповой политики (GPO) может быть отображена двойным щелчком GPO или щелчком правой кнопкой мыши и выбором команды **Журнал**.</span><span class="sxs-lookup"><span data-stu-id="6b812-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="6b812-105">Оно также отображается в консоли управления групповыми политиками в качестве вкладки для каждого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6b812-105">It is also displayed in the Group Policy Management Console (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="6b812-106">Журнал предоставляет запись событий во время существования выбранного объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6b812-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="6b812-107">В окне **журнала** можно получить отчет о параметрах в версии объекта групповой политики, сравнить несколько версий объекта групповой политики или вернуться к более ранней версии GPO.</span><span class="sxs-lookup"><span data-stu-id="6b812-107">From the **History** window, you can obtain a report of the settings in a version of the GPO, compare multiple versions of a GPO, or roll back to an earlier version of a GPO.</span></span>

## <span data-ttu-id="6b812-108">Фильтрация событий в окне "журнал"</span><span class="sxs-lookup"><span data-stu-id="6b812-108">Filtering events in the History window</span></span>


<span data-ttu-id="6b812-109">На вкладках в окне **журнала** фильтруются состояния объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6b812-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b812-110">Закладок</span><span class="sxs-lookup"><span data-stu-id="6b812-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="6b812-111">Тегов</span><span class="sxs-lookup"><span data-stu-id="6b812-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6b812-112">Все состояния</span><span class="sxs-lookup"><span data-stu-id="6b812-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-113">Отобразить все состояния в истории объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6b812-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6b812-114">Уникальные версии</span><span class="sxs-lookup"><span data-stu-id="6b812-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-115">Отобразить только уникальные версии объекта групповой политики, которые были возвращены в архив.</span><span class="sxs-lookup"><span data-stu-id="6b812-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="6b812-116">Версия, развернутая в производственной среде, сочетания клавиш для уникальных версий и информационные состояния указаны в этом списке.</span><span class="sxs-lookup"><span data-stu-id="6b812-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6b812-117">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="6b812-117">Event information</span></span>


<span data-ttu-id="6b812-118">Информация предоставляется для каждого состояния в журнале объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6b812-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b812-119">Атрибут GPO</span><span class="sxs-lookup"><span data-stu-id="6b812-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="6b812-120">Описание</span><span class="sxs-lookup"><span data-stu-id="6b812-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6b812-121">Изменить дату</span><span class="sxs-lookup"><span data-stu-id="6b812-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-122">Метка времени выполнения действия в <strong> столбце "состояние" </strong> .</span><span class="sxs-lookup"><span data-stu-id="6b812-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6b812-123">Состояние</span><span class="sxs-lookup"><span data-stu-id="6b812-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-124">Состояние в истории объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6b812-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6b812-125">Кем изменено</span><span class="sxs-lookup"><span data-stu-id="6b812-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-126">Пользователь, который вернул или развернул объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6b812-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6b812-127">Comment</span><span class="sxs-lookup"><span data-stu-id="6b812-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-128">Примечание, введенное пользователем, который вернул или развернул объект групповой политики на момент изменения этой версии, можно использовать для определения конкретных версий в случае необходимости возврата к более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="6b812-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was changed, useful for identifying the specifics of the version in case of the need to roll back to an earlier version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6b812-129">Удаляемый</span><span class="sxs-lookup"><span data-stu-id="6b812-129">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-130">Может ли эта версия объекта групповой политики быть удалена, если число уникальных версий всех объектов групповой политики, сохраненных в архиве, ограничено.</span><span class="sxs-lookup"><span data-stu-id="6b812-130">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="6b812-131">Примечание.</span><span class="sxs-lookup"><span data-stu-id="6b812-131">Note</span></span></strong><br/><p><span data-ttu-id="6b812-132">Вы можете изменить способ удаления объекта GPO, щелкнув его правой кнопкой мыши и выбрав команду не <strong> разрешать удаление </strong> или <strong> Разрешить удаление </strong> .</span><span class="sxs-lookup"><span data-stu-id="6b812-132">You can change whether a version of a GPO can be deleted by right-clicking the GPO and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6b812-133">Версия компьютера</span><span class="sxs-lookup"><span data-stu-id="6b812-133">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-134">Автоматически созданная версия части конфигурации компьютера для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6b812-134">Automatically generated version of the Computer Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6b812-135">Пользовательская версия</span><span class="sxs-lookup"><span data-stu-id="6b812-135">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-136">Автоматически созданная версия части конфигурации пользователя для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6b812-136">Automatically generated version of the User Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6b812-137">Состояние объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="6b812-137">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-138">Конфигурацию компьютера и конфигурацию пользователя можно управлять отдельно друг от друга.</span><span class="sxs-lookup"><span data-stu-id="6b812-138">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="6b812-139">Этот статус показывает, какие части объекта групповой политики включены.</span><span class="sxs-lookup"><span data-stu-id="6b812-139">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6b812-140">Данные исходного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="6b812-140">Source GPO Information</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-141">Для объекта групповой политики, который был импортирован из другого леса, исходное имя GPO, домен и пользователь и дата, связанные с последним изменением.</span><span class="sxs-lookup"><span data-stu-id="6b812-141">For a GPO that has been imported from another forest, the original GPO name, domain, and user and date associated with the last change.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6b812-142">Отчеты</span><span class="sxs-lookup"><span data-stu-id="6b812-142">Reports</span></span>


<span data-ttu-id="6b812-143">На кнопках " **Параметры** " и " **различия** " отображаются отчеты о параметрах GPO для выбранной версии или версий GPO.</span><span class="sxs-lookup"><span data-stu-id="6b812-143">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="6b812-144">Кроме того, вы также можете щелкнуть правой кнопкой мыши версию объекта групповой политики или его версии, чтобы отобразить отчеты на основе XML.</span><span class="sxs-lookup"><span data-stu-id="6b812-144">Also, right-clicking a GPO version or versions provides the option to display XML-based reports.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b812-145">Кнопка</span><span class="sxs-lookup"><span data-stu-id="6b812-145">Button</span></span></th>
<th align="left"><span data-ttu-id="6b812-146">Эффект</span><span class="sxs-lookup"><span data-stu-id="6b812-146">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6b812-147">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b812-147">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-148">Создание отчета на основе HTML, в котором отображаются параметры в выбранной версии объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6b812-148">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6b812-149">Соответствия</span><span class="sxs-lookup"><span data-stu-id="6b812-149">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-150">Создание отчета на основе HTML, который сравнивает параметры в нескольких выбранных версиях объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6b812-150">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="6b812-151">Ключевые для отчетов о различиях</span><span class="sxs-lookup"><span data-stu-id="6b812-151">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b812-152">Символ</span><span class="sxs-lookup"><span data-stu-id="6b812-152">Symbol</span></span></th>
<th align="left"><span data-ttu-id="6b812-153">Значение</span><span class="sxs-lookup"><span data-stu-id="6b812-153">Meaning</span></span></th>
<th align="left"><span data-ttu-id="6b812-154">Цвет</span><span class="sxs-lookup"><span data-stu-id="6b812-154">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b812-155">Нет</span><span class="sxs-lookup"><span data-stu-id="6b812-155">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b812-156">Элемент существует с одинаковыми параметрами в обоих объектах групповой политики</span><span class="sxs-lookup"><span data-stu-id="6b812-156">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b812-157">Зависит от уровня</span><span class="sxs-lookup"><span data-stu-id="6b812-157">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6b812-158">[#]</span><span class="sxs-lookup"><span data-stu-id="6b812-158">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-159">Элемент существует в обоих объектах GPO, но с измененными параметрами</span><span class="sxs-lookup"><span data-stu-id="6b812-159">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b812-160">Синюю</span><span class="sxs-lookup"><span data-stu-id="6b812-160">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6b812-161">[-]</span><span class="sxs-lookup"><span data-stu-id="6b812-161">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-162">Элемент существует только в первом объекте групповой политики</span><span class="sxs-lookup"><span data-stu-id="6b812-162">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b812-163">Красный</span><span class="sxs-lookup"><span data-stu-id="6b812-163">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6b812-164">[+]</span><span class="sxs-lookup"><span data-stu-id="6b812-164">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6b812-165">Элемент существует только во втором объекте групповой политики</span><span class="sxs-lookup"><span data-stu-id="6b812-165">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b812-166">Зеленый</span><span class="sxs-lookup"><span data-stu-id="6b812-166">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="6b812-167">Для элементов с измененными параметрами измененные параметры определяются при разворачивании элемента.</span><span class="sxs-lookup"><span data-stu-id="6b812-167">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="6b812-168">Значение атрибута в каждом объекте групповой политики отображается в том же порядке, в котором эти объекты отображаются в отчете.</span><span class="sxs-lookup"><span data-stu-id="6b812-168">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="6b812-169">Некоторые изменения в параметрах могут привести к тому, что элемент будет представлен в виде двух элементов (только в первом объекте групповой политики), а только во втором — вместо одного элемента, который был изменен.</span><span class="sxs-lookup"><span data-stu-id="6b812-169">Some changes to settings may cause an item to be reported as two items (one present only in the first GPO, one present only in the second), instead of one item that has changed.</span></span>

### <span data-ttu-id="6b812-170">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="6b812-170">Additional references</span></span>

-   [<span data-ttu-id="6b812-171">Вкладка "Содержимое"</span><span class="sxs-lookup"><span data-stu-id="6b812-171">Contents Tab</span></span>](contents-tab-agpm40.md)









