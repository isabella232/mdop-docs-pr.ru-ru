---
title: Команды неуправляемого объекта групповой политики
description: Команды неуправляемого объекта групповой политики
author: dansimp
ms.assetid: 05a8050f-adc3-465b-8524-bbe95745165c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8efd1c1d3005fd97b92d392140b92bae6a38681
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818242"
---
# <span data-ttu-id="4b9ac-103">Команды неуправляемого объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="4b9ac-103">Uncontrolled GPO Commands</span></span>


<span data-ttu-id="4b9ac-104">Вкладка " **неуправление** ":</span><span class="sxs-lookup"><span data-stu-id="4b9ac-104">The **Uncontrolled** tab:</span></span>

-   <span data-ttu-id="4b9ac-105">Отображает список объектов групповой политики (GPO), не управляемых с помощью расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-105">Displays a list of Group Policy Objects (GPOs) not managed by Advanced Group Policy Management (AGPM).</span></span>

-   <span data-ttu-id="4b9ac-106">Контекстное меню с командами для отключения неуправляемых объектов групповой политики в управлении групповыми политиками и для отображения журнала и отчетов для GPO.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-106">Provides a shortcut menu with commands for bringing uncontrolled GPOs under the management of AGPM and for displaying the history and reports for GPOs.</span></span>

-   <span data-ttu-id="4b9ac-107">Выводит список групп и пользователей, которые имеют разрешение на доступ к выбранному объекту групповой политики.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-107">Displays a list of the groups and users who have permission to access a selected GPO.</span></span>

<span data-ttu-id="4b9ac-108">При щелчке правой кнопкой мыши списка **объектов групповой политики** на этой вкладке отображается контекстное меню, в том числе один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-108">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="4b9ac-109">Управление и журнал</span><span class="sxs-lookup"><span data-stu-id="4b9ac-109">Control and history</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4b9ac-110">Команда</span><span class="sxs-lookup"><span data-stu-id="4b9ac-110">Command</span></span></th>
<th align="left"><span data-ttu-id="4b9ac-111">Эффект</span><span class="sxs-lookup"><span data-stu-id="4b9ac-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4b9ac-112">Журнал</span><span class="sxs-lookup"><span data-stu-id="4b9ac-112">History</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4b9ac-113">Открытие окна со списком всех версий выбранного объекта групповой политики, сохраненных в архиве.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-113">Open a window listing all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="4b9ac-114">Из истории вы можете получить отчет о параметрах в объекте групповой политики, сравнить две версии объекта групповой политики, сравнить GPO с шаблоном или вернуться к более ранней версии GPO.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-114">From the history, you can obtain a report of the settings within a GPO, compare two versions of a GPO, compare a GPO to a template, or roll back to an earlier version of a GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4b9ac-115">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="4b9ac-115">Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4b9ac-116">Перевод выделенного неуправляемого объекта групповой политики в соответствии с управлением изменениями управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-116">Bring the selected uncontrolled GPO under the change control management of AGPM.</span></span> <span data-ttu-id="4b9ac-117">Если у вас нет разрешения на управление объектом групповой политики, вам будет предложено отправить запрос.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-117">If you do not have permission to control a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4b9ac-118">Сохранение в качестве шаблона</span><span class="sxs-lookup"><span data-stu-id="4b9ac-118">Save as Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4b9ac-119">Создание нового шаблона на основе параметров выбранного объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-119">Create a new template based on the settings of the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4b9ac-120">Отчеты</span><span class="sxs-lookup"><span data-stu-id="4b9ac-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4b9ac-121">Команда</span><span class="sxs-lookup"><span data-stu-id="4b9ac-121">Command</span></span></th>
<th align="left"><span data-ttu-id="4b9ac-122">Эффект</span><span class="sxs-lookup"><span data-stu-id="4b9ac-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4b9ac-123">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b9ac-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4b9ac-124">Создание отчета на основе HTML или XML, в котором отображаются параметры выбранного объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4b9ac-125">Соответствия</span><span class="sxs-lookup"><span data-stu-id="4b9ac-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4b9ac-126">Создание отчета на основе HTML или XML для сравнения параметров в двух выбранных объектах групповой политики или в выбранном объекте групповой политики и шаблоне.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPOs or within the selected GPO and a template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4b9ac-127">Прочее</span><span class="sxs-lookup"><span data-stu-id="4b9ac-127">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4b9ac-128">Команда</span><span class="sxs-lookup"><span data-stu-id="4b9ac-128">Command</span></span></th>
<th align="left"><span data-ttu-id="4b9ac-129">Эффект</span><span class="sxs-lookup"><span data-stu-id="4b9ac-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4b9ac-130">Обновить</span><span class="sxs-lookup"><span data-stu-id="4b9ac-130">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4b9ac-131">Обновите отображение консоли управления групповыми политиками (GPMC), чтобы внести изменения.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-131">Update the display of the Group Policy Management Console (GPMC) to incorporate any changes.</span></span> <span data-ttu-id="4b9ac-132">Некоторые изменения не видны до тех пор, пока не будет обновлено представление.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-132">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4b9ac-133">Help</span><span class="sxs-lookup"><span data-stu-id="4b9ac-133">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4b9ac-134">Вывести справку по РАСШИРЕНному языку.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-134">Display help for AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="4b9ac-135">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="4b9ac-135">Additional references</span></span>

-   [<span data-ttu-id="4b9ac-136">Вкладка "Содержимое"</span><span class="sxs-lookup"><span data-stu-id="4b9ac-136">Contents Tab</span></span>](contents-tab-agpm40.md)

-   [<span data-ttu-id="4b9ac-137">Выполнение задач редактора</span><span class="sxs-lookup"><span data-stu-id="4b9ac-137">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="4b9ac-138">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="4b9ac-138">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="4b9ac-139">Выполнение задач рецензента</span><span class="sxs-lookup"><span data-stu-id="4b9ac-139">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





