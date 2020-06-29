---
title: Функции вкладки "Содержимое"
description: Функции вкладки "Содержимое"
author: dansimp
ms.assetid: 725f025a-c30a-4d07-add1-4e0ed9a1a5fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f64aad16a3335d78641812121692f6d5f6436ee1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818909"
---
# <span data-ttu-id="34e28-103">Функции вкладки "Содержимое"</span><span class="sxs-lookup"><span data-stu-id="34e28-103">Contents Tab Features</span></span>


<span data-ttu-id="34e28-104">Каждая вспомогательная вкладка на вкладке " **содержимое** " состоит из двух разделов:**объектов групповой политики** и **групп и пользователей**.</span><span class="sxs-lookup"><span data-stu-id="34e28-104">Each secondary tab within the **Contents** tab has two sections—**Group Policy objects** and **Groups and Users**.</span></span>

## <span data-ttu-id="34e28-105">Раздел "объекты групповой политики"</span><span class="sxs-lookup"><span data-stu-id="34e28-105">Group Policy objects section</span></span>


<span data-ttu-id="34e28-106">Раздел " **объекты групповой политики** " отображает отфильтрованный список объектов групповой политики (GPO) и определяет указанные ниже атрибуты для каждого GPO.</span><span class="sxs-lookup"><span data-stu-id="34e28-106">The **Group Policy objects** section displays a filtered list of Group Policy Objects (GPOs) and identifies the following attributes for each GPO:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="34e28-107">Атрибут GPO</span><span class="sxs-lookup"><span data-stu-id="34e28-107">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="34e28-108">Описание</span><span class="sxs-lookup"><span data-stu-id="34e28-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="34e28-109">Name</span><span class="sxs-lookup"><span data-stu-id="34e28-109">Name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="34e28-110">Имя объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="34e28-110">Name of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="34e28-111">Состояние</span><span class="sxs-lookup"><span data-stu-id="34e28-111">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="34e28-112">Состояние выбранного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="34e28-112">The state of the selected GPO</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="34e28-113">Кем изменено</span><span class="sxs-lookup"><span data-stu-id="34e28-113">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="34e28-114">Редактор, который вернул или утверждающий, который развернул выбранный объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="34e28-114">The Editor who checked in or the Approver who deployed the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="34e28-115">Изменить дату</span><span class="sxs-lookup"><span data-stu-id="34e28-115">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="34e28-116">Для управляемого объекта групповой политики: самая поздняя дата, когда она была возвращена после изменения или извлечения для изменения.</span><span class="sxs-lookup"><span data-stu-id="34e28-116">For a controlled GPO, the most recent date it was checked in after being modified or checked out to be modified.</span></span> <span data-ttu-id="34e28-117">Для неконтрольного объекта групповой политики — Дата последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="34e28-117">For an uncontrolled GPO, the date when it was last modified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="34e28-118">Comment</span><span class="sxs-lookup"><span data-stu-id="34e28-118">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="34e28-119">Примечание, введенное пользователем, который вернул или развернул объект групповой политики на момент его изменения.</span><span class="sxs-lookup"><span data-stu-id="34e28-119">A comment entered by the person who checked in or deployed a GPO at the time that it was modified.</span></span> <span data-ttu-id="34e28-120">Полезен для выявления конкретных версий в случае необходимости возврата к предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="34e28-120">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="34e28-121">Версия компьютера</span><span class="sxs-lookup"><span data-stu-id="34e28-121">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="34e28-122">Автоматически созданная версия части объекта групповой политики на компьютере.</span><span class="sxs-lookup"><span data-stu-id="34e28-122">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="34e28-123">Пользовательская версия</span><span class="sxs-lookup"><span data-stu-id="34e28-123">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="34e28-124">Автоматически созданная версия части объекта групповой политики пользователя.</span><span class="sxs-lookup"><span data-stu-id="34e28-124">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="34e28-125">Состояние объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="34e28-125">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="34e28-126">Конфигурацию компьютера и конфигурацию пользователя можно управлять отдельно.</span><span class="sxs-lookup"><span data-stu-id="34e28-126">The Computer Configuration and the User Configuration can be managed separately.</span></span> <span data-ttu-id="34e28-127">Состояние GPO показывает, какие части объекта групповой политики включены.</span><span class="sxs-lookup"><span data-stu-id="34e28-127">The GPO Status indicates which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="34e28-128">Фильтр WMI</span><span class="sxs-lookup"><span data-stu-id="34e28-128">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="34e28-129">Отобразить все фильтры WMI, примененные к этому объекту групповой политики.</span><span class="sxs-lookup"><span data-stu-id="34e28-129">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="34e28-130">Фильтры WMI управляются в <strong> папке "фильтры WMI" </strong> для домена в дереве консоли консоли управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="34e28-130">WMI filters are managed under the <strong>WMI Filters</strong> folder for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="34e28-131">Раздел групп и пользователей</span><span class="sxs-lookup"><span data-stu-id="34e28-131">Groups and Users section</span></span>


<span data-ttu-id="34e28-132">При выборе объекта групповой политики в разделе **группы и пользователи** отображается список групп и пользователей, имеющих доступ к этому объекту групповой политики.</span><span class="sxs-lookup"><span data-stu-id="34e28-132">When a GPO is selected, the **Groups and Users** section displays a list of the groups and users with access to that GPO.</span></span> <span data-ttu-id="34e28-133">Разрешенные разрешения и наследование отображаются для каждой группы или пользователя.</span><span class="sxs-lookup"><span data-stu-id="34e28-133">The allowed permissions and inheritance are displayed for each group or user.</span></span> <span data-ttu-id="34e28-134">Администратор РАСШИРЕНного доступа может настраивать разрешения с помощью стандартных ролей (редактор, утверждающий, рецензент и администратор РАСШИРЕНного доступа) или настроенного сочетания разрешений.</span><span class="sxs-lookup"><span data-stu-id="34e28-134">An AGPM Administrator can configure permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="34e28-135">Кнопка</span><span class="sxs-lookup"><span data-stu-id="34e28-135">Button</span></span></th>
<th align="left"><span data-ttu-id="34e28-136">Эффект</span><span class="sxs-lookup"><span data-stu-id="34e28-136">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="34e28-137">Add</span><span class="sxs-lookup"><span data-stu-id="34e28-137">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="34e28-138">Добавьте новую запись в дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="34e28-138">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="34e28-139">Вы можете добавить пользователя или группу в службе каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="34e28-139">Any user or group in Active Directory can be added.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="34e28-140">Удалить</span><span class="sxs-lookup"><span data-stu-id="34e28-140">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="34e28-141">Удаление выделенного элемента из списка управления доступом.</span><span class="sxs-lookup"><span data-stu-id="34e28-141">Remove the selected entry from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="34e28-142">Свойства</span><span class="sxs-lookup"><span data-stu-id="34e28-142">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="34e28-143">Отображение свойств выбранного объекта.</span><span class="sxs-lookup"><span data-stu-id="34e28-143">Display the properties for the selected object.</span></span> <span data-ttu-id="34e28-144">На странице "Свойства" отображается один и тот же объект в окне " <strong> Пользователи и компьютеры Active Directory" </strong> .</span><span class="sxs-lookup"><span data-stu-id="34e28-144">The properties page is the same one displayed for an object in <strong>Active Directory Users and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="34e28-145">Дополнительно</span><span class="sxs-lookup"><span data-stu-id="34e28-145">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="34e28-146">Откройте <strong> Редактор списка управления доступом </strong> .</span><span class="sxs-lookup"><span data-stu-id="34e28-146">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="34e28-147">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="34e28-147">Additional considerations</span></span>

-   <span data-ttu-id="34e28-148">Сведения о ролях и разрешениях, связанных с определенными задачами, можно найти в разделе [выполнение задач администратора расширенного администрирования](performing-agpm-administrator-tasks-agpm30ops.md), [выполнение задач редактора](performing-editor-tasks-agpm30ops.md), [выполнение задач утверждающего](performing-approver-tasks-agpm30ops.md)и [выполнение задач рецензента](performing-reviewer-tasks-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="34e28-148">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks-agpm30ops.md), [Performing Editor Tasks](performing-editor-tasks-agpm30ops.md), [Performing Approver Tasks](performing-approver-tasks-agpm30ops.md), and [Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md).</span></span>

### <span data-ttu-id="34e28-149">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="34e28-149">Additional references</span></span>

-   [<span data-ttu-id="34e28-150">Вкладка "Содержимое"</span><span class="sxs-lookup"><span data-stu-id="34e28-150">Contents Tab</span></span>](contents-tab-agpm30ops.md)

 

 





