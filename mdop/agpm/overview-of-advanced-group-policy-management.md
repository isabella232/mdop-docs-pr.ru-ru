---
title: Обзор средства расширенного управления групповыми политиками
description: Обзор средства расширенного управления групповыми политиками
author: dansimp
ms.assetid: 028de9dd-848b-42bc-a982-65ba5c433772
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38396de6bd8bdace72d3add1bba09769ae26de32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822482"
---
# <span data-ttu-id="db62f-103">Обзор средства расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="db62f-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="db62f-104">С помощью расширенного управления групповыми политиками можно расширить возможности консоли управления групповыми политиками, обеспечивая всестороннее управление изменениями и улучшенное управление объектами групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="db62f-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy objects (GPOs).</span></span>

## <span data-ttu-id="db62f-105">Разработка объектов групповой политики с помощью элемента управления изменениями</span><span class="sxs-lookup"><span data-stu-id="db62f-105">Group Policy object development with change control</span></span>


<span data-ttu-id="db62f-106">С помощью расширенного управления групповыми политиками вы можете хранить копии всех объектов групповой политики в центральном архиве, поэтому администраторы групповой политики могут просматривать и изменять их в автономном режиме, не влияя на развернутую версию GPO.</span><span class="sxs-lookup"><span data-stu-id="db62f-106">With AGPM, you can store a copy of each GPO in a central archive, so Group Policy administrators can view and modify it offline without immediately impacting the deployed version of the GPO.</span></span> <span data-ttu-id="db62f-107">Кроме того, в разделе управления групповыми политиками хранится копия каждой версии каждого управляемого объекта групповой политики в архиве, чтобы при необходимости можно было выполнить откат к более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="db62f-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if needed.</span></span>

<span data-ttu-id="db62f-108">Условия "вернуть" и "извлечь" используются в большинстве тем же способом, что и в библиотеке (или в приложениях, которые предоставляют Управление изменениями, контроль версий и управление исходным кодом для разработки программного обеспечения).</span><span class="sxs-lookup"><span data-stu-id="db62f-108">The terms "check in" and "check out" are used in much the same way as in a library (or in applications that provide change control, version control, or source code control for programming development).</span></span> <span data-ttu-id="db62f-109">Чтобы использовать книгу, которая находится в библиотеке, вы можете извлечь ее из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="db62f-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="db62f-110">Никто другой не сможет использовать его, пока он не будет извлечен. После того как вы закончите работу с книгой, вы вернете ее в библиотеку, чтобы другие пользователи смогли ее использовать.</span><span class="sxs-lookup"><span data-stu-id="db62f-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="db62f-111">При разработке объектов групповой политики с помощью функции РАСШИРЕНного использования функций:</span><span class="sxs-lookup"><span data-stu-id="db62f-111">When developing GPOs using AGPM:</span></span>

1.  <span data-ttu-id="db62f-112">Создание нового управляемого объекта групповой политики или управление ранее неуправляемым объектом групповой политики.</span><span class="sxs-lookup"><span data-stu-id="db62f-112">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="db62f-113">Изучите объект групповой политики, и вы можете изменить его.</span><span class="sxs-lookup"><span data-stu-id="db62f-113">Check out the GPO, so you and only you can modify it.</span></span>

3.  <span data-ttu-id="db62f-114">Измените объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="db62f-114">Edit the GPO.</span></span>

4.  <span data-ttu-id="db62f-115">Установите отредактированный объект групповой политики, чтобы другие пользователи могли изменить его, и это может быть развернуто.</span><span class="sxs-lookup"><span data-stu-id="db62f-115">Check in the edited GPO, so others can modify it, or so it can be deployed.</span></span>

5.  <span data-ttu-id="db62f-116">Проверьте изменения.</span><span class="sxs-lookup"><span data-stu-id="db62f-116">Review the changes.</span></span>

6.  <span data-ttu-id="db62f-117">Развертывание объекта групповой политики в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="db62f-117">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="db62f-118">Делегирование на основе ролей</span><span class="sxs-lookup"><span data-stu-id="db62f-118">Role-based delegation</span></span>


<span data-ttu-id="db62f-119">С помощью РАСШИРЕНного доступа к учетной задаче можно легко использовать делегирование на основе ролей.</span><span class="sxs-lookup"><span data-stu-id="db62f-119">AGPM provides comprehensive, easy-to-use role-based delegation.</span></span> <span data-ttu-id="db62f-120">Разрешения на уровне домена позволяют администраторам РАСШИРЕНного доступа предоставлять доступ к отдельным доменам без предоставления доступа к другим доменам.</span><span class="sxs-lookup"><span data-stu-id="db62f-120">Domain-level permissions allow AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="db62f-121">Делегирование на основе GPO позволяет администраторам РАСШИРЕНного доступа к данным предоставлять доступ только к определенным объектам групповой политики.</span><span class="sxs-lookup"><span data-stu-id="db62f-121">GPO-based delegation enables AGPM Administrators to allow access only to specific GPOs.</span></span>

<span data-ttu-id="db62f-122">В режиме управления групповыми политиками существуют определенные роли: администратор РАСШИРЕНного доступа (полный доступ), утверждающий, редактор и рецензент.</span><span class="sxs-lookup"><span data-stu-id="db62f-122">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="db62f-123">Роль администратора РАСШИРЕНного доступа включает разрешения для всех других ролей.</span><span class="sxs-lookup"><span data-stu-id="db62f-123">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="db62f-124">По умолчанию только утверждающие обладают возможностями развертывания объектов групповой политики в рабочей среде, защищая среду от случайных ошибок при помощи менее опытных редакторов.</span><span class="sxs-lookup"><span data-stu-id="db62f-124">By default, only Approvers have the power to deploy GPOs to the production environment, protecting the environment from inadvertent mistakes by less experienced Editors.</span></span> <span data-ttu-id="db62f-125">Кроме того, по умолчанию все роли включают роль проверяющего и, следовательно, возможность просматривать параметры объектов групповой политики в отчетах.</span><span class="sxs-lookup"><span data-stu-id="db62f-125">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="db62f-126">Тем не менее, для настройки доступа к объекту групповой политики в соответствии с потребностями вашей организации управление групповыми политиками обеспечивает администраторам РАСШИРЕНного разрешения на доступ к GPO.</span><span class="sxs-lookup"><span data-stu-id="db62f-126">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="db62f-127">Делегирование в среде администратора с несколькими групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="db62f-127">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="db62f-128">В среде, в которой несколько пользователей изменяют GPO, администратор РАСШИРЕНного доступа делегирует разрешение на редакторы, утверждающие и рецензенты либо в виде групп, либо в качестве отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="db62f-128">In an environment where multiple people make changes to GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="db62f-129">Типичный процесс разработки объектов групповой политики для редактора и утверждающего можно найти в разделе [Контрольный список: создание, изменение и развертывание объекта групповой политики](checklist-create-edit-and-deploy-a-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="db62f-129">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo.md).</span></span>

### <span data-ttu-id="db62f-130">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="db62f-130">Additional references</span></span>

-   [<span data-ttu-id="db62f-131">Контрольный список: создание, редактирование и развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="db62f-131">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo.md)

-   [<span data-ttu-id="db62f-132">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="db62f-132">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

-   [<span data-ttu-id="db62f-133">Выполнение задач редактора</span><span class="sxs-lookup"><span data-stu-id="db62f-133">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="db62f-134">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="db62f-134">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="db62f-135">Выполнение задач рецензента</span><span class="sxs-lookup"><span data-stu-id="db62f-135">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

-   [<span data-ttu-id="db62f-136">Устранение неполадок средства расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="db62f-136">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management.md)

-   [<span data-ttu-id="db62f-137">Пользовательский интерфейс: расширенное управление групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="db62f-137">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

 

 





