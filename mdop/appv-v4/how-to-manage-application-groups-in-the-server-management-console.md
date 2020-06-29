---
title: Управление группами приложений на консоли управления серверами
description: Управление группами приложений на консоли управления серверами
author: dansimp
ms.assetid: 46997971-bdc8-4565-aefd-f47e90d6d7a6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 59a357d93ea63cc728f59a0633b7a5b9953aad14
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817202"
---
# <span data-ttu-id="a1629-103">Управление группами приложений на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="a1629-103">How to Manage Application Groups in the Server Management Console</span></span>


<span data-ttu-id="a1629-104">Вы можете отобразить и управлять одним или несколькими приложениями в группах приложений в консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="a1629-104">You can display and manage one or more applications in application groups in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="a1629-105">Это может быть полезно, если вы хотите сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="a1629-105">This can be useful when you want to do the following:</span></span>

-   <span data-ttu-id="a1629-106">Упорядочите несколько приложений в более управляемые подгруппы.</span><span class="sxs-lookup"><span data-stu-id="a1629-106">Organize many applications into more manageable subgroups.</span></span>

-   <span data-ttu-id="a1629-107">Создание групп приложений, относящихся к отделам и другим подразделениям компании.</span><span class="sxs-lookup"><span data-stu-id="a1629-107">Create groups of applications specific to a department or other company division.</span></span>

-   <span data-ttu-id="a1629-108">Группировка сходных типов приложений, например финансовых программ.</span><span class="sxs-lookup"><span data-stu-id="a1629-108">Group similar types of applications, such as financial software.</span></span>

-   <span data-ttu-id="a1629-109">Упрощение разрешений на доступ или управление лицензиями по группам.</span><span class="sxs-lookup"><span data-stu-id="a1629-109">Simplify access permissions or license management by group.</span></span>

-   <span data-ttu-id="a1629-110">Одновременное изменение свойств приложений и групп приложений в группе.</span><span class="sxs-lookup"><span data-stu-id="a1629-110">Change the properties of applications and application groups within a group simultaneously.</span></span>

<span data-ttu-id="a1629-111">Вы можете создать группу, поместить ее в нужное место в дереве **приложений** консоли и импортировать в нее приложения.</span><span class="sxs-lookup"><span data-stu-id="a1629-111">You can create a group, place it where you would like in the console's **Applications** tree, and import applications to the group.</span></span> <span data-ttu-id="a1629-112">Затем вы можете настроить свойства группы и управлять ими, чтобы повлиять на все ее приложения.</span><span class="sxs-lookup"><span data-stu-id="a1629-112">Then you can configure and manage the group's properties to affect all of its applications.</span></span> <span data-ttu-id="a1629-113">Вы также можете перемещать приложения между группами.</span><span class="sxs-lookup"><span data-stu-id="a1629-113">You can also move applications among groups.</span></span>

<span data-ttu-id="a1629-114">**Примечание**  Перемещение приложений в группы не влияет на расположение файлов (SFT, OSD или SPRJ) в файловой системе сервера.</span><span class="sxs-lookup"><span data-stu-id="a1629-114">**Note** Moving applications into groups does not affect the locations of their files (SFT, OSD, or SPRJ) on the server's file system.</span></span>

 

## <span data-ttu-id="a1629-115">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="a1629-115">In This Section</span></span>


<a href="" id="how-to-create-an-application-group"></a>[<span data-ttu-id="a1629-116">Создание группы приложений</span><span class="sxs-lookup"><span data-stu-id="a1629-116">How to Create an Application Group</span></span>](how-to-create-an-application-group.md)  
<span data-ttu-id="a1629-117">В этой статье приведены пошаговые инструкции по созданию группы приложения.</span><span class="sxs-lookup"><span data-stu-id="a1629-117">Provides step-by-step instructions for creating an application group.</span></span>

<a href="" id="how-to-move-an-application-group"></a>[<span data-ttu-id="a1629-118">Перенос группа приложений</span><span class="sxs-lookup"><span data-stu-id="a1629-118">How to Move an Application Group</span></span>](how-to-move-an-application-group.md)  
<span data-ttu-id="a1629-119">В этой статье приведены пошаговые инструкции по перемещению группы приложения.</span><span class="sxs-lookup"><span data-stu-id="a1629-119">Provides step-by-step instructions for moving an application group.</span></span>

<a href="" id="how-to-rename-an-application-group"></a>[<span data-ttu-id="a1629-120">Переименование группы приложений</span><span class="sxs-lookup"><span data-stu-id="a1629-120">How to Rename an Application Group</span></span>](how-to-rename-an-application-group.md)  
<span data-ttu-id="a1629-121">В этой статье приведены пошаговые инструкции по переименованию группы приложения.</span><span class="sxs-lookup"><span data-stu-id="a1629-121">Provides step-by-step instructions for renaming an application group.</span></span>

<a href="" id="how-to-remove-an-application-group"></a>[<span data-ttu-id="a1629-122">Удаление группы приложений</span><span class="sxs-lookup"><span data-stu-id="a1629-122">How to Remove an Application Group</span></span>](how-to-remove-an-application-group.md)  
<span data-ttu-id="a1629-123">Содержит пошаговые инструкции по удалению или удалению группы приложения.</span><span class="sxs-lookup"><span data-stu-id="a1629-123">Provides step-by-step instructions for removing or deleting an application group.</span></span>

## <span data-ttu-id="a1629-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a1629-124">Related topics</span></span>


[<span data-ttu-id="a1629-125">Управление приложениями на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="a1629-125">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

[<span data-ttu-id="a1629-126">Выполнение задач администрирования на консоли управления серверами Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="a1629-126">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





