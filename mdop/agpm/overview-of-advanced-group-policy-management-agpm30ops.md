---
title: Обзор средства расширенного управления групповыми политиками
description: Обзор средства расширенного управления групповыми политиками
author: dansimp
ms.assetid: 3a8d1e58-12b9-42bd-898f-6d57514dfbb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: feb43972c78ed12501e372800c1f5ec19609477a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822492"
---
# <span data-ttu-id="fa69e-103">Обзор средства расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="fa69e-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="fa69e-104">С помощью расширенного управления групповыми политиками можно расширять возможности консоли управления групповыми политиками для обеспечения полного контроля изменений и улучшенного управления объектами групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="fa69e-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC) to provide comprehensive change control and improved management for Group Policy Objects (GPOs).</span></span>

## <span data-ttu-id="fa69e-105">Разработка объектов групповой политики с помощью элемента управления изменениями</span><span class="sxs-lookup"><span data-stu-id="fa69e-105">Group Policy object development with change control</span></span>


<span data-ttu-id="fa69e-106">С помощью расширенного управления групповыми политиками вы можете хранить копии всех GPO в центральном архиве, чтобы администраторы групповых политик могли просматривать и изменять ее автономно, не влияя на развернутую версию объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="fa69e-106">With AGPM, you can store a copy of each GPO in a central archive so that Group Policy administrators can view and change it offline without immediately affecting the deployed version of the GPO.</span></span> <span data-ttu-id="fa69e-107">Кроме того, в разделе управления групповыми политиками хранится копия каждой версии каждого управляемого объекта групповой политики в архиве, чтобы при необходимости можно было вернуться к более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="fa69e-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if necessary.</span></span>

<span data-ttu-id="fa69e-108">Условия "вернуть" и "извлечь" используются так же, как и в библиотеке (или в приложениях, которые предоставляют Управление изменениями, контроль версий или системы управления версиями для разработки программного обеспечения).</span><span class="sxs-lookup"><span data-stu-id="fa69e-108">The terms "check in" and "check out" are used just as in a library (or in applications that provide change control, version control, or source control for programming development).</span></span> <span data-ttu-id="fa69e-109">Чтобы использовать книгу, которая находится в библиотеке, вы можете извлечь ее из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="fa69e-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="fa69e-110">Никто другой не сможет использовать его, пока он не будет извлечен. После того как вы закончите работу с книгой, вы вернете ее в библиотеку, чтобы другие пользователи смогли ее использовать.</span><span class="sxs-lookup"><span data-stu-id="fa69e-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="fa69e-111">При разработке объектов групповой политики с помощью РАСШИРЕНного использования функций:</span><span class="sxs-lookup"><span data-stu-id="fa69e-111">When you develop GPOs by using AGPM:</span></span>

1.  <span data-ttu-id="fa69e-112">Создание нового управляемого объекта групповой политики или управление ранее неуправляемым объектом групповой политики.</span><span class="sxs-lookup"><span data-stu-id="fa69e-112">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="fa69e-113">Изучите объект групповой политики, и вы можете изменить его только вы.</span><span class="sxs-lookup"><span data-stu-id="fa69e-113">Check out the GPO, so that you and only you can change it.</span></span>

3.  <span data-ttu-id="fa69e-114">Измените объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="fa69e-114">Edit the GPO.</span></span>

4.  <span data-ttu-id="fa69e-115">Установите отредактированный объект групповой политики, чтобы другие пользователи могли его изменить или чтобы его можно было развернуть.</span><span class="sxs-lookup"><span data-stu-id="fa69e-115">Check in the edited GPO, so that others can change it, or so that it can be deployed.</span></span>

5.  <span data-ttu-id="fa69e-116">Проверьте изменения.</span><span class="sxs-lookup"><span data-stu-id="fa69e-116">Review the changes.</span></span>

6.  <span data-ttu-id="fa69e-117">Развертывание объекта групповой политики в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="fa69e-117">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="fa69e-118">Делегирование на основе ролей</span><span class="sxs-lookup"><span data-stu-id="fa69e-118">Role-based delegation</span></span>


<span data-ttu-id="fa69e-119">Функция расширенного управления групповыми политиками обеспечивает полное и простое использование делегирования на основе ролей для доступа к объектам групповой политики в архиве.</span><span class="sxs-lookup"><span data-stu-id="fa69e-119">AGPM provides comprehensive, easy-to-use role-based delegation for managing access to GPOs in the archive.</span></span> <span data-ttu-id="fa69e-120">Разрешения на уровне домена позволяют администраторам РАСШИРЕНного доступа предоставлять доступ к отдельным доменам без предоставления доступа к другим доменам.</span><span class="sxs-lookup"><span data-stu-id="fa69e-120">Domain-level permissions enable AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="fa69e-121">Делегирование на основе GPO позволяет администраторам РАСШИРЕНного доступа предоставлять доступ к определенным объектам групповой политики, не предоставляя доступ к домену.</span><span class="sxs-lookup"><span data-stu-id="fa69e-121">GPO-based delegation enables AGPM Administrators to provide access to specific GPOs without providing domain-wide access.</span></span>

<span data-ttu-id="fa69e-122">В режиме управления групповыми политиками существуют определенные роли: администратор РАСШИРЕНного доступа (полный доступ), утверждающий, редактор и рецензент.</span><span class="sxs-lookup"><span data-stu-id="fa69e-122">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="fa69e-123">Роль администратора РАСШИРЕНного доступа включает разрешения для всех других ролей.</span><span class="sxs-lookup"><span data-stu-id="fa69e-123">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="fa69e-124">По умолчанию только утверждающие обладают возможностями развертывания объектов групповой политики в рабочей среде, защищая среду от ошибок с помощью менее опытных редакторов.</span><span class="sxs-lookup"><span data-stu-id="fa69e-124">By default, only Approvers have the power to deploy GPOs to the production environment, protecting the environment from mistakes by less experienced Editors.</span></span> <span data-ttu-id="fa69e-125">Кроме того, по умолчанию все роли включают роль проверяющего и, следовательно, возможность просматривать параметры объектов групповой политики в отчетах.</span><span class="sxs-lookup"><span data-stu-id="fa69e-125">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="fa69e-126">Тем не менее, для настройки доступа к объекту групповой политики в соответствии с потребностями вашей организации управление групповыми политиками обеспечивает администраторам РАСШИРЕНного разрешения на доступ к GPO.</span><span class="sxs-lookup"><span data-stu-id="fa69e-126">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="fa69e-127">Делегирование в среде администратора с несколькими групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="fa69e-127">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="fa69e-128">В среде, в которой несколько пользователей изменяют GPO, администратор РАСШИРЕНного доступа делегирует разрешение на редакторы, утверждающие и рецензенты либо в виде групп, либо в качестве отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="fa69e-128">In an environment where multiple people change GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="fa69e-129">Типичный процесс разработки объектов групповой политики для редактора и утверждающего можно найти в разделе [Контрольный список: создание, изменение и развертывание объекта групповой политики](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="fa69e-129">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md).</span></span>

### <span data-ttu-id="fa69e-130">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="fa69e-130">Additional references</span></span>

-   [<span data-ttu-id="fa69e-131">Руководство по работе со средством расширенного управления групповыми политиками3.0</span><span class="sxs-lookup"><span data-stu-id="fa69e-131">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





