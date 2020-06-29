---
title: Контрольный список для создания, изменения и развертывания объекта групповой политики
description: Контрольный список для создания, изменения и развертывания объекта групповой политики
author: dansimp
ms.assetid: 44631bed-16d2-4b5a-af70-17a73fb5f6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d8bea9109040aa81a20df62356ef1d307d5eac0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819102"
---
# <span data-ttu-id="9f803-103">Контрольный список: создание, редактирование и развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9f803-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="9f803-104">В среде, в которой несколько пользователей изменяют объекты групповой политики (GPO) с помощью расширенного управления групповыми политиками (режимом MARS), администраторы РАСШИРЕНного доступа (полный доступ) делегируют разрешение на редакторы, утверждающие и рецензенты либо в виде групп, либо в качестве отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="9f803-104">In an environment where multiple people change Group Policy Objects (GPOs) by using Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers either as groups or as individuals.</span></span> <span data-ttu-id="9f803-105">Ниже приведен типичный процесс разработки объектов групповой политики для редактора и утверждающего.</span><span class="sxs-lookup"><span data-stu-id="9f803-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9f803-106">Задача</span><span class="sxs-lookup"><span data-stu-id="9f803-106">Task</span></span></th>
<th align="left"><span data-ttu-id="9f803-107">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="9f803-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9f803-108">Редактор запрашивает создание нового объекта групповой политики или утверждающего создает новый объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9f803-108">Editor requests that a new GPO be created or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm40.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm40.md)"><span data-ttu-id="9f803-109">Запрос на создание нового управляемого объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9f803-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo-agpm40.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md)"><span data-ttu-id="9f803-110">Создание нового управляемого объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9f803-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9f803-111">Утверждающее лицо утверждает создание объекта групповой политики, если оно было запрошено редактором.</span><span class="sxs-lookup"><span data-stu-id="9f803-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)"><span data-ttu-id="9f803-112">Утверждение или отклонение ожидающего действия</span><span class="sxs-lookup"><span data-stu-id="9f803-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9f803-113">Редактор извлекает из архива копию объекта групповой политики, чтобы никто из них не мог изменить объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9f803-113">Editor checks out a copy of the GPO from the archive so that no one else can modify the GPO.</span></span> <span data-ttu-id="9f803-114">Редактор вносит изменения в объект групповой политики, а затем проверяет измененный объект GPO в архив.</span><span class="sxs-lookup"><span data-stu-id="9f803-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm40.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm40.md)"><span data-ttu-id="9f803-115">Изменение объекта групповой политики в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="9f803-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9f803-116">При разработке в тестовом лесе редактор экспортирует объект групповой политики в файл, передает файл в производственный лес и импортирует файл.</span><span class="sxs-lookup"><span data-stu-id="9f803-116">If developing in a test forest, Editor exports the GPO to a file, transfers the file to the production forest, and imports the file.</span></span> <span data-ttu-id="9f803-117">Кроме того, редактор может связать GPO с подразделением, содержащим тестовые компьютеры и пользователей.</span><span class="sxs-lookup"><span data-stu-id="9f803-117">Additionally, an Editor can link the GPO to an organizational unit that contains test computers and users.</span></span></p></td>
<td align="left"><p><a href="using-a-test-environment.md" data-raw-source="[Using a Test Environment](using-a-test-environment.md)"><span data-ttu-id="9f803-118">Использование тестовой среды</span><span class="sxs-lookup"><span data-stu-id="9f803-118">Using a Test Environment</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9f803-119">Редактор запрашивает развертывание объекта групповой политики в производственной среде домена.</span><span class="sxs-lookup"><span data-stu-id="9f803-119">Editor requests deployment of the GPO to the production environment of the domain.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm40.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md)"><span data-ttu-id="9f803-120">Запрос на развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9f803-120">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9f803-121">С помощью рецензентов, например утверждающих или редакторов, можно проанализировать объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9f803-121">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm40.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md)"><span data-ttu-id="9f803-122">Выполнение задач рецензента</span><span class="sxs-lookup"><span data-stu-id="9f803-122">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9f803-123">Утверждающее лицо утверждает и развертывает объект групповой политики в рабочей среде домена или отвергает объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9f803-123">Approver approves and deploys the GPO to the production environment of the domain or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)"><span data-ttu-id="9f803-124">Утверждение или отклонение ожидающего действия</span><span class="sxs-lookup"><span data-stu-id="9f803-124">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="9f803-125">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="9f803-125">Additional references</span></span>

[<span data-ttu-id="9f803-126">Средство расширенного управления групповыми политиками 4.0</span><span class="sxs-lookup"><span data-stu-id="9f803-126">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





