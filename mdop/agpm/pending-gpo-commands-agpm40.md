---
title: Команды ожидающего объекта групповой политики
description: Команды ожидающего объекта групповой политики
author: dansimp
ms.assetid: b62f49e1-43ab-4c93-8102-96cd97a4adad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa5afed2335d75132c0fd99c69e0b5e09985d98f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822462"
---
# <span data-ttu-id="1b147-103">Команды ожидающего объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="1b147-103">Pending GPO Commands</span></span>


<span data-ttu-id="1b147-104">Вкладка " **ожидающие** ":</span><span class="sxs-lookup"><span data-stu-id="1b147-104">The **Pending** tab:</span></span>

-   <span data-ttu-id="1b147-105">Отображает список объектов групповой политики (GPO) с отложенными запросами на действия по управлению объектами GPO (например, создание, управление, развертывание и удаление).</span><span class="sxs-lookup"><span data-stu-id="1b147-105">Displays a list of Group Policy Objects (GPOs) with pending requests for GPO management actions (such as creation, control, deployment, or deletion).</span></span>

-   <span data-ttu-id="1b147-106">Контекстное меню с командами для реагирования на запросы, ожидающие обработки, и для отображения журнала и отчетов для GPO.</span><span class="sxs-lookup"><span data-stu-id="1b147-106">Provides a shortcut menu with commands for responding to pending requests and for displaying the history and reports for GPOs.</span></span>

-   <span data-ttu-id="1b147-107">Выводит список групп и пользователей, которые имеют разрешение на доступ к выбранному объекту групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1b147-107">Displays a list of the groups and users who have permission to access a selected GPO.</span></span>

<span data-ttu-id="1b147-108">При щелчке правой кнопкой мыши списка **объектов групповой политики** на этой вкладке отображается контекстное меню, в том числе один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="1b147-108">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="1b147-109">Управление и журнал</span><span class="sxs-lookup"><span data-stu-id="1b147-109">Control and history</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1b147-110">Команда</span><span class="sxs-lookup"><span data-stu-id="1b147-110">Command</span></span></th>
<th align="left"><span data-ttu-id="1b147-111">Эффект</span><span class="sxs-lookup"><span data-stu-id="1b147-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1b147-112">Журнал</span><span class="sxs-lookup"><span data-stu-id="1b147-112">History</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1b147-113">Открытие окна со списком всех версий выбранного объекта групповой политики, сохраненных в архиве.</span><span class="sxs-lookup"><span data-stu-id="1b147-113">Open a window listing all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="1b147-114">Из истории вы можете получить отчет о параметрах в объекте групповой политики, сравнить две версии объекта групповой политики, сравнить GPO с шаблоном или вернуться к более ранней версии GPO.</span><span class="sxs-lookup"><span data-stu-id="1b147-114">From the history, you can obtain a report of the settings within a GPO, compare two versions of a GPO, compare a GPO to a template, or roll back to an earlier version of a GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1b147-115">Казать</span><span class="sxs-lookup"><span data-stu-id="1b147-115">Withdraw</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1b147-116">Отмена ожидающего запроса на создание, контроль или удаление выделенного объекта групповой политики до утверждения запроса.</span><span class="sxs-lookup"><span data-stu-id="1b147-116">Withdraw your pending request to create, control, or delete the selected GPO before the request has been approved.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1b147-117">Утвердить</span><span class="sxs-lookup"><span data-stu-id="1b147-117">Approve</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1b147-118">Выполнение ожидающего запроса от редактора для создания, управления и удаления выбранного объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1b147-118">Complete a pending request from an Editor to create, control, or delete the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1b147-119">Отклонить</span><span class="sxs-lookup"><span data-stu-id="1b147-119">Reject</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1b147-120">Отказ от редактора для запроса на создание, управление или удаление выделенного объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1b147-120">Deny a pending request from an Editor to create, control, or delete the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1b147-121">Отчеты</span><span class="sxs-lookup"><span data-stu-id="1b147-121">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1b147-122">Команда</span><span class="sxs-lookup"><span data-stu-id="1b147-122">Command</span></span></th>
<th align="left"><span data-ttu-id="1b147-123">Эффект</span><span class="sxs-lookup"><span data-stu-id="1b147-123">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1b147-124">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b147-124">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1b147-125">Создание отчета на основе HTML или XML с параметрами в выбранном объекте групповой политики или отображение ссылок на выделенные объекты GPO из организационных подразделений на момент последнего управления, импорта или возврата объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1b147-125">Generate an HTML-based or XML-based report displaying the settings within the selected GPO or display links to the selected GPOs from organizational units as of when the GPOs are most recently controlled, imported, or checked in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1b147-126">Соответствия</span><span class="sxs-lookup"><span data-stu-id="1b147-126">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1b147-127">Создание отчета на основе HTML или XML для сравнения параметров в двух выбранных объектах групповой политики или в выбранном объекте групповой политики и шаблоне.</span><span class="sxs-lookup"><span data-stu-id="1b147-127">Generate an HTML-based or XML-based report comparing the settings within two selected GPOs or within the selected GPO and a template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1b147-128">Прочее</span><span class="sxs-lookup"><span data-stu-id="1b147-128">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1b147-129">Команда</span><span class="sxs-lookup"><span data-stu-id="1b147-129">Command</span></span></th>
<th align="left"><span data-ttu-id="1b147-130">Эффект</span><span class="sxs-lookup"><span data-stu-id="1b147-130">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1b147-131">Обновить</span><span class="sxs-lookup"><span data-stu-id="1b147-131">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1b147-132">Обновите отображение консоли управления групповыми политиками (GPMC), чтобы внести изменения.</span><span class="sxs-lookup"><span data-stu-id="1b147-132">Update the display of the Group Policy Management Console (GPMC) to incorporate any changes.</span></span> <span data-ttu-id="1b147-133">Некоторые изменения не видны до тех пор, пока не будет обновлено представление.</span><span class="sxs-lookup"><span data-stu-id="1b147-133">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1b147-134">Help</span><span class="sxs-lookup"><span data-stu-id="1b147-134">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1b147-135">Вывести справку по РАСШИРЕНному языку.</span><span class="sxs-lookup"><span data-stu-id="1b147-135">Display help for AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="1b147-136">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="1b147-136">Additional references</span></span>

-   [<span data-ttu-id="1b147-137">Вкладка "Содержимое"</span><span class="sxs-lookup"><span data-stu-id="1b147-137">Contents Tab</span></span>](contents-tab-agpm40.md)

-   [<span data-ttu-id="1b147-138">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="1b147-138">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="1b147-139">Выполнение задач рецензента</span><span class="sxs-lookup"><span data-stu-id="1b147-139">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





