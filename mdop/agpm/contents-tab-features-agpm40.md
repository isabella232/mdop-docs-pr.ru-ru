---
title: Функции вкладки "Содержимое"
description: Функции вкладки "Содержимое"
author: dansimp
ms.assetid: f1f4849d-bf94-47d5-ad81-0eee33abcaca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 081cffb7c2871d0e49abd229ec06773726483f2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818892"
---
# <span data-ttu-id="938d5-103">Функции вкладки "Содержимое"</span><span class="sxs-lookup"><span data-stu-id="938d5-103">Contents Tab Features</span></span>


<span data-ttu-id="938d5-104">Каждая вспомогательная вкладка на вкладке " **содержимое** " состоит из двух разделов:**объектов групповой политики** и **групп и пользователей**.</span><span class="sxs-lookup"><span data-stu-id="938d5-104">Each secondary tab within the **Contents** tab has two sections—**Group Policy objects** and **Groups and Users**.</span></span>

## <span data-ttu-id="938d5-105">Раздел "объекты групповой политики"</span><span class="sxs-lookup"><span data-stu-id="938d5-105">Group Policy objects section</span></span>


<span data-ttu-id="938d5-106">Раздел " **объекты групповой политики** " отображает отфильтрованный список объектов групповой политики (GPO) и определяет указанные ниже атрибуты для каждого GPO.</span><span class="sxs-lookup"><span data-stu-id="938d5-106">The **Group Policy objects** section displays a filtered list of Group Policy Objects (GPOs) and identifies the following attributes for each GPO.</span></span> <span data-ttu-id="938d5-107">Вы можете использовать поле **поиска** для поиска объектов групповой политики с определенными атрибутами.</span><span class="sxs-lookup"><span data-stu-id="938d5-107">You can use the **Search** box to search for GPOs with specific attributes.</span></span> <span data-ttu-id="938d5-108">Дополнительные сведения можно найти [в разделе Поиск и фильтрация списка объектов групповой политики](search-and-filter-the-list-of-gpos.md).</span><span class="sxs-lookup"><span data-stu-id="938d5-108">For more information, see [Search and Filter the List of GPOs](search-and-filter-the-list-of-gpos.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="938d5-109">Атрибут GPO</span><span class="sxs-lookup"><span data-stu-id="938d5-109">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="938d5-110">Описание</span><span class="sxs-lookup"><span data-stu-id="938d5-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="938d5-111">Name</span><span class="sxs-lookup"><span data-stu-id="938d5-111">Name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="938d5-112">Имя объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="938d5-112">Name of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="938d5-113">Состояние</span><span class="sxs-lookup"><span data-stu-id="938d5-113">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="938d5-114">Состояние выбранного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="938d5-114">The state of the selected GPO</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="938d5-115">Кем изменено</span><span class="sxs-lookup"><span data-stu-id="938d5-115">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="938d5-116">Редактор, который вернул или утверждающий, который развернул выбранный объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="938d5-116">The Editor who checked in or the Approver who deployed the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="938d5-117">Изменить дату</span><span class="sxs-lookup"><span data-stu-id="938d5-117">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="938d5-118">Для управляемого объекта групповой политики: самая поздняя дата, когда она была возвращена после изменения или извлечения для изменения.</span><span class="sxs-lookup"><span data-stu-id="938d5-118">For a controlled GPO, the most recent date it was checked in after being modified or checked out to be modified.</span></span> <span data-ttu-id="938d5-119">Для неконтрольного объекта групповой политики — Дата последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="938d5-119">For an uncontrolled GPO, the date when it was last modified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="938d5-120">Comment</span><span class="sxs-lookup"><span data-stu-id="938d5-120">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="938d5-121">Примечание, введенное пользователем, который вернул или развернул объект групповой политики на момент его изменения.</span><span class="sxs-lookup"><span data-stu-id="938d5-121">A comment entered by the person who checked in or deployed a GPO at the time that it was modified.</span></span> <span data-ttu-id="938d5-122">Полезен для выявления конкретных версий в случае необходимости возврата к более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="938d5-122">Useful for identifying the specifics of the version in case of the need to roll back to an earlier version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="938d5-123">Версия компьютера</span><span class="sxs-lookup"><span data-stu-id="938d5-123">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="938d5-124">Автоматически созданная версия части конфигурации компьютера для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="938d5-124">Automatically generated version of the Computer Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="938d5-125">Пользовательская версия</span><span class="sxs-lookup"><span data-stu-id="938d5-125">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="938d5-126">Автоматически созданная версия части конфигурации пользователя для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="938d5-126">Automatically generated version of the User Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="938d5-127">Состояние объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="938d5-127">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="938d5-128">Конфигурацию компьютера и конфигурацию пользователя можно управлять отдельно.</span><span class="sxs-lookup"><span data-stu-id="938d5-128">The Computer Configuration and the User Configuration can be managed separately.</span></span> <span data-ttu-id="938d5-129">Состояние GPO показывает, какие части объекта групповой политики включены.</span><span class="sxs-lookup"><span data-stu-id="938d5-129">The GPO Status indicates which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="938d5-130">Фильтр WMI</span><span class="sxs-lookup"><span data-stu-id="938d5-130">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="938d5-131">Отобразить все фильтры WMI, примененные к этому объекту групповой политики.</span><span class="sxs-lookup"><span data-stu-id="938d5-131">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="938d5-132">Фильтры WMI управляются в <strong> папке "фильтры WMI" </strong> для домена в дереве консоли консоли управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="938d5-132">WMI filters are managed under the <strong>WMI Filters</strong> folder for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="938d5-133">Раздел групп и пользователей</span><span class="sxs-lookup"><span data-stu-id="938d5-133">Groups and Users section</span></span>


<span data-ttu-id="938d5-134">При выборе объекта групповой политики в разделе **группы и пользователи** отображается список групп и пользователей, имеющих доступ к этому объекту групповой политики.</span><span class="sxs-lookup"><span data-stu-id="938d5-134">When a GPO is selected, the **Groups and Users** section displays a list of the groups and users with access to that GPO.</span></span> <span data-ttu-id="938d5-135">Разрешенные разрешения и наследование отображаются для каждой группы или пользователя.</span><span class="sxs-lookup"><span data-stu-id="938d5-135">The allowed permissions and inheritance are displayed for each group or user.</span></span> <span data-ttu-id="938d5-136">Администратор РАСШИРЕНного доступа может настраивать разрешения с помощью стандартных ролей (редактор, утверждающий, рецензент и администратор РАСШИРЕНного доступа) или настроенного сочетания разрешений.</span><span class="sxs-lookup"><span data-stu-id="938d5-136">An AGPM Administrator can configure permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="938d5-137">Кнопка</span><span class="sxs-lookup"><span data-stu-id="938d5-137">Button</span></span></th>
<th align="left"><span data-ttu-id="938d5-138">Эффект</span><span class="sxs-lookup"><span data-stu-id="938d5-138">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="938d5-139">Add</span><span class="sxs-lookup"><span data-stu-id="938d5-139">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="938d5-140">Добавьте новую запись в дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="938d5-140">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="938d5-141">Вы можете добавить пользователя или группу в службе каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="938d5-141">Any user or group in Active Directory can be added.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="938d5-142">Удалить</span><span class="sxs-lookup"><span data-stu-id="938d5-142">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="938d5-143">Удаление выделенного элемента из списка управления доступом.</span><span class="sxs-lookup"><span data-stu-id="938d5-143">Remove the selected entry from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="938d5-144">Свойства</span><span class="sxs-lookup"><span data-stu-id="938d5-144">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="938d5-145">Отображение свойств выбранного объекта.</span><span class="sxs-lookup"><span data-stu-id="938d5-145">Display the properties for the selected object.</span></span> <span data-ttu-id="938d5-146">На странице "Свойства" отображается один и тот же объект в окне " <strong> Пользователи и компьютеры Active Directory" </strong> .</span><span class="sxs-lookup"><span data-stu-id="938d5-146">The properties page is the same one displayed for an object in <strong>Active Directory Users and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="938d5-147">Дополнительно</span><span class="sxs-lookup"><span data-stu-id="938d5-147">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="938d5-148">Откройте <strong> Редактор списка управления доступом </strong> .</span><span class="sxs-lookup"><span data-stu-id="938d5-148">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="938d5-149">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="938d5-149">Additional considerations</span></span>

-   <span data-ttu-id="938d5-150">Сведения о ролях и разрешениях, связанных с определенными задачами, можно найти в разделе [выполнение задач администратора расширенного администрирования](performing-agpm-administrator-tasks-agpm40.md), [выполнение задач редактора](performing-editor-tasks-agpm40.md), [выполнение задач утверждающего](performing-approver-tasks-agpm40.md)и [выполнение задач рецензента](performing-reviewer-tasks-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="938d5-150">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks-agpm40.md), [Performing Editor Tasks](performing-editor-tasks-agpm40.md), [Performing Approver Tasks](performing-approver-tasks-agpm40.md), and [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md).</span></span>

### <span data-ttu-id="938d5-151">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="938d5-151">Additional references</span></span>

-   [<span data-ttu-id="938d5-152">Вкладка "Содержимое"</span><span class="sxs-lookup"><span data-stu-id="938d5-152">Contents Tab</span></span>](contents-tab-agpm40.md)

 

 





