---
title: Контрольный список для создания, изменения и развертывания объекта групповой политики
description: Контрольный список для создания, изменения и развертывания объекта групповой политики
author: dansimp
ms.assetid: 614e2d9a-c18b-4f62-99fd-e17a2ac8559d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c79fefaa65c138372ebee00b769ccc5243142e22
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819112"
---
# <span data-ttu-id="6d0ae-103">Контрольный список: создание, редактирование и развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="6d0ae-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="6d0ae-104">В среде, в которой несколько пользователей вносит изменения в объекты групповой политики (GPO), администраторы РАСШИРЕНного доступа (Full Control) делегируют разрешение на редакторы, утверждающие и рецензенты либо в виде групп, либо в качестве отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="6d0ae-104">In an environment where multiple people make changes to Group Policy objects (GPOs), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="6d0ae-105">Ниже приведен типичный процесс разработки объектов групповой политики для редактора и утверждающего.</span><span class="sxs-lookup"><span data-stu-id="6d0ae-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6d0ae-106">Задача</span><span class="sxs-lookup"><span data-stu-id="6d0ae-106">Task</span></span></th>
<th align="left"><span data-ttu-id="6d0ae-107">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="6d0ae-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6d0ae-108">Редактор запрашивает создание нового объекта групповой политики или утверждающего создает новый объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6d0ae-108">Editor requests the creation of a new GPO or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo.md)"><span data-ttu-id="6d0ae-109">Запрос на создание нового управляемого объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="6d0ae-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo.md)"><span data-ttu-id="6d0ae-110">Создание нового управляемого объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="6d0ae-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6d0ae-111">Утверждающее лицо утверждает создание объекта групповой политики, если оно было запрошено редактором.</span><span class="sxs-lookup"><span data-stu-id="6d0ae-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)"><span data-ttu-id="6d0ae-112">Утверждение или отклонение ожидающего действия</span><span class="sxs-lookup"><span data-stu-id="6d0ae-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6d0ae-113">Редактор извлекает копию объекта групповой политики из архива, поэтому никто другой не может изменить объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6d0ae-113">Editor checks out a copy of the GPO from the archive, so no one else can modify the GPO.</span></span> <span data-ttu-id="6d0ae-114">Редактор вносит изменения в объект групповой политики, а затем проверяет измененный объект GPO в архив.</span><span class="sxs-lookup"><span data-stu-id="6d0ae-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline.md)"><span data-ttu-id="6d0ae-115">Изменение объекта групповой политики в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="6d0ae-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6d0ae-116">Редактор запрашивает развертывание объекта групповой политики в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="6d0ae-116">Editor requests deployment of the GPO to the production environment.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo.md)"><span data-ttu-id="6d0ae-117">Запрос на развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="6d0ae-117">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6d0ae-118">С помощью рецензентов, например утверждающих или редакторов, можно проанализировать объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6d0ae-118">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks.md)"><span data-ttu-id="6d0ae-119">Выполнение задач рецензента</span><span class="sxs-lookup"><span data-stu-id="6d0ae-119">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6d0ae-120">Утверждающее лицо утверждает и развертывает объект групповой политики в рабочей среде или отклоняет объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6d0ae-120">Approver approves and deploys the GPO to the production environment or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)"><span data-ttu-id="6d0ae-121">Утверждение или отклонение ожидающего действия</span><span class="sxs-lookup"><span data-stu-id="6d0ae-121">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





