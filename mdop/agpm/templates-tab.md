---
title: Вкладка "Шаблоны"
description: Вкладка "Шаблоны"
author: dansimp
ms.assetid: 5676e9f9-eb52-49e1-a55d-15c1059af368
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7469ee72eb23903ddec66152f8cc5d59861dfc9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820172"
---
# <span data-ttu-id="1441e-103">Вкладка "Шаблоны"</span><span class="sxs-lookup"><span data-stu-id="1441e-103">Templates Tab</span></span>


<span data-ttu-id="1441e-104">Вкладка " **шаблоны** "</span><span class="sxs-lookup"><span data-stu-id="1441e-104">The **Templates** tab:</span></span>

-   <span data-ttu-id="1441e-105">Выводит список доступных шаблонов, которые можно использовать для создания новых объектов групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="1441e-105">Displays a list of available templates that you can use to create new Group Policy objects (GPOs).</span></span>

-   <span data-ttu-id="1441e-106">Контекстное меню с командами для создания объекта групповой политики на основе выбранного шаблона, управления шаблонами и отображения отчетов для шаблонов.</span><span class="sxs-lookup"><span data-stu-id="1441e-106">Provides a shortcut menu with commands for creating a GPO based on a selected template, managing templates, and displaying reports for templates.</span></span>

-   <span data-ttu-id="1441e-107">Выводит список групп и пользователей, которые имеют разрешение на доступ к выбранному шаблону.</span><span class="sxs-lookup"><span data-stu-id="1441e-107">Displays a list of the groups and users who have permission to access a selected template.</span></span>

<span data-ttu-id="1441e-108">Поскольку шаблон не может быть изменен, шаблоны не имеют истории.</span><span class="sxs-lookup"><span data-stu-id="1441e-108">Because a template cannot be altered, templates have no history.</span></span> <span data-ttu-id="1441e-109">Но, как и любая версия объекта групповой политики, параметры шаблона можно отобразить с помощью отчета о параметрах или по сравнению с другим GPO с отчетом о разнице.</span><span class="sxs-lookup"><span data-stu-id="1441e-109">However, like any GPO version, the settings of a template can be displayed with a settings report or compared to another GPO with a difference report.</span></span>

<span data-ttu-id="1441e-110">**Примечание**  Шаблон — это нередактируемая статическая версия GPO, используемая в качестве отправной точки для создания новых редактируемых GPO.</span><span class="sxs-lookup"><span data-stu-id="1441e-110">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="1441e-111">При щелчке правой кнопкой мыши списка **объектов групповой политики** на этой вкладке отображается контекстное меню, в том числе один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="1441e-111">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="1441e-112">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="1441e-112">Control</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1441e-113">Команда</span><span class="sxs-lookup"><span data-stu-id="1441e-113">Command</span></span></th>
<th align="left"><span data-ttu-id="1441e-114">Эффект</span><span class="sxs-lookup"><span data-stu-id="1441e-114">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1441e-115">Новый управляемый объект групповой политики</span><span class="sxs-lookup"><span data-stu-id="1441e-115">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1441e-116">Создание нового объекта групповой политики на основе выбранного шаблона.</span><span class="sxs-lookup"><span data-stu-id="1441e-116">Create a new GPO based on the selected template.</span></span> <span data-ttu-id="1441e-117">В производственную среду предоставляется параметр для развертывания нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1441e-117">The option to deploy the new GPO to the production environment is provided.</span></span> <span data-ttu-id="1441e-118">Если у вас нет разрешения на создание объекта групповой политики, вам будет предложено отправить запрос.</span><span class="sxs-lookup"><span data-stu-id="1441e-118">If you do not have permission to create a GPO, you will be prompted to submit a request.</span></span> <span data-ttu-id="1441e-119">(Этот параметр отображается, если не выбран ни одного объекта групповой политики, если щелкнуть правой кнопкой мыши в области <strong> Список объектов групповой политики </strong> .)</span><span class="sxs-lookup"><span data-stu-id="1441e-119">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1441e-120">Отчеты</span><span class="sxs-lookup"><span data-stu-id="1441e-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1441e-121">Команда</span><span class="sxs-lookup"><span data-stu-id="1441e-121">Command</span></span></th>
<th align="left"><span data-ttu-id="1441e-122">Эффект</span><span class="sxs-lookup"><span data-stu-id="1441e-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1441e-123">Параметры</span><span class="sxs-lookup"><span data-stu-id="1441e-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1441e-124">Создание отчета на основе HTML или XML, в котором отображаются параметры выбранного объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1441e-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1441e-125">Соответствия</span><span class="sxs-lookup"><span data-stu-id="1441e-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1441e-126">Создание отчета на основе HTML или XML для сравнения параметров в двух выбранных шаблонах GPO.</span><span class="sxs-lookup"><span data-stu-id="1441e-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPO templates.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1441e-127">Управление шаблонами</span><span class="sxs-lookup"><span data-stu-id="1441e-127">Template management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1441e-128">Команда</span><span class="sxs-lookup"><span data-stu-id="1441e-128">Command</span></span></th>
<th align="left"><span data-ttu-id="1441e-129">Эффект</span><span class="sxs-lookup"><span data-stu-id="1441e-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1441e-130">Использовать по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1441e-130">Set as Default</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1441e-131">Настройка выбранного шаблона в качестве используемого по умолчанию при создании нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1441e-131">Set the selected template as the default to be used automatically when creating a new GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1441e-132">Delete</span><span class="sxs-lookup"><span data-stu-id="1441e-132">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1441e-133">Переместить выбранный шаблон в <strong> корзину </strong> .</span><span class="sxs-lookup"><span data-stu-id="1441e-133">Move the selected template to the <strong>Recycle Bin</strong>.</span></span> <span data-ttu-id="1441e-134">Если у вас нет разрешения на удаление объекта групповой политики, вам будет предложено отправить запрос.</span><span class="sxs-lookup"><span data-stu-id="1441e-134">If you do not have permission to delete a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1441e-135">Rename</span><span class="sxs-lookup"><span data-stu-id="1441e-135">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1441e-136">Изменение имени выбранного шаблона.</span><span class="sxs-lookup"><span data-stu-id="1441e-136">Change the name of the selected template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1441e-137">Прочее</span><span class="sxs-lookup"><span data-stu-id="1441e-137">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1441e-138">Команда</span><span class="sxs-lookup"><span data-stu-id="1441e-138">Command</span></span></th>
<th align="left"><span data-ttu-id="1441e-139">Эффект</span><span class="sxs-lookup"><span data-stu-id="1441e-139">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1441e-140">Обновить</span><span class="sxs-lookup"><span data-stu-id="1441e-140">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1441e-141">Обновите отображение консоли управления групповыми политиками, чтобы внести изменения.</span><span class="sxs-lookup"><span data-stu-id="1441e-141">Update the display of the Group Policy Management Console to incorporate any changes.</span></span> <span data-ttu-id="1441e-142">Некоторые изменения не видны до тех пор, пока не будет обновлено представление.</span><span class="sxs-lookup"><span data-stu-id="1441e-142">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1441e-143">Help</span><span class="sxs-lookup"><span data-stu-id="1441e-143">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1441e-144">Вывести справку по расширенному управлению групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="1441e-144">Display help for Advanced Group Policy Management (AGPM).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="1441e-145">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="1441e-145">Additional references</span></span>

-   [<span data-ttu-id="1441e-146">Вкладка "Содержимое"</span><span class="sxs-lookup"><span data-stu-id="1441e-146">Contents Tab</span></span>](contents-tab.md)

-   [<span data-ttu-id="1441e-147">Выполнение задач редактора</span><span class="sxs-lookup"><span data-stu-id="1441e-147">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="1441e-148">Выполнение задач рецензента</span><span class="sxs-lookup"><span data-stu-id="1441e-148">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 





