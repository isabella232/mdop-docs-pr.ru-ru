---
title: Руководство по работе со средством расширенного управления групповыми политиками4.0
description: Руководство по работе со средством расширенного управления групповыми политиками4.0
author: dansimp
ms.assetid: 0bafeba3-20a9-4360-be5d-03f786df11ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b51956c319f1b0a77e4a4bdf71090be4f322236e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820482"
---
# <span data-ttu-id="2850e-103">Руководство по работе со средством расширенного управления групповыми политиками4.0</span><span class="sxs-lookup"><span data-stu-id="2850e-103">Operations Guide for Microsoft Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="2850e-104">Вы можете использовать расширенные возможности управления групповыми политиками (Майкрософт) для продления возможностей консоли управления групповыми политиками (GPMC).</span><span class="sxs-lookup"><span data-stu-id="2850e-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="2850e-105">Функция управления групповыми политиками обеспечивает всестороннее управление изменениями и улучшенные возможности управления объектами групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="2850e-105">AGPM provides comprehensive change control and improved management of Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="2850e-106">С помощью РАСШИРЕНного использования функций вы можете выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="2850e-106">Using AGPM, you can do these tasks:</span></span>

-   <span data-ttu-id="2850e-107">Автономное редактирование объектов групповой политики позволяет создавать и тестировать их перед развертыванием в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="2850e-107">Perform offline editing of GPOs so that you can create and test them before you deploy them to a production environment.</span></span>

-   <span data-ttu-id="2850e-108">Поддерживать несколько версий объекта групповой политики в центральном архиве, чтобы можно было выполнить откат в случае возникновения проблемы.</span><span class="sxs-lookup"><span data-stu-id="2850e-108">Maintain multiple versions of a GPO in a central archive so that you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="2850e-109">Вы можете предоставить ответственность за редактирование, утверждение и проверку объектов групповой политики нескольким людям с помощью делегирования на основе ролей.</span><span class="sxs-lookup"><span data-stu-id="2850e-109">Share the responsibility for editing, approving, and reviewing GPOs among multiple people by using role-based delegation.</span></span>

-   <span data-ttu-id="2850e-110">Устраните опасность, с которой администраторы нескольких групповых политик перезапишут другую работу с помощью функции "вернуть и извлечь" для GPO.</span><span class="sxs-lookup"><span data-stu-id="2850e-110">Eliminate the danger of multiple Group Policy administrators overwriting one another's work by using the check-in and check-out capability for GPOs.</span></span>

-   <span data-ttu-id="2850e-111">Анализ изменений в объекте групповой политики, сравнение его с другим объектом групповой политики или другой версией того же объекта групповой политики с помощью отчетов о различиях.</span><span class="sxs-lookup"><span data-stu-id="2850e-111">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO by using difference reporting.</span></span>

-   <span data-ttu-id="2850e-112">Упрощение создания объектов групповой политики с помощью шаблонов GPO с сохранением общих параметров политики и параметров настройки, которые используются в качестве отправных точек для новых объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="2850e-112">Simplify creating new GPOs by using GPO templates, storing common policy settings and preference settings to use as starting points for new GPOs.</span></span>

-   <span data-ttu-id="2850e-113">Передача доступа в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="2850e-113">Delegate access to the production environment.</span></span>

-   <span data-ttu-id="2850e-114">Поиск объектов групповой политики с определенными атрибутами и фильтрация списка объектов групповой политики, отображаемых в списке.</span><span class="sxs-lookup"><span data-stu-id="2850e-114">Search for GPOs with specific attributes and filter the list of GPOs displayed.</span></span>

-   <span data-ttu-id="2850e-115">Экспортируйте объект групповой политики в файл, чтобы его можно было скопировать из домена в тестовом лесе в домен в рабочем лесу.</span><span class="sxs-lookup"><span data-stu-id="2850e-115">Export a GPO to a file so that you can copy it from a domain in a test forest to a domain in a production forest.</span></span>

<span data-ttu-id="2850e-116">РАСШИРЕНная Настройка групповой политики добавляет в каждый из доменов, отображаемых в консоли управления групповыми политиками, папку для **изменения** в дополнение к вкладке " **Журнал** " для всех GPO и ссылки на групповую политику, которая отображается в GPMC.</span><span class="sxs-lookup"><span data-stu-id="2850e-116">AGPM adds a **Change Control** folder under each domain displayed in the GPMC, in addition to a **History** tab for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="2850e-117">Обзор средства расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="2850e-117">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="2850e-118">Советы и рекомендации по управлению версиями</span><span class="sxs-lookup"><span data-stu-id="2850e-118">Best Practices for Version Control</span></span>](best-practices-for-version-control-agpm40.md)

-   [<span data-ttu-id="2850e-119">Контрольный список: администрирование сервера и архива AGPM</span><span class="sxs-lookup"><span data-stu-id="2850e-119">Checklist: Administer the AGPM Server and Archive</span></span>](checklist-administer-the-agpm-server-and-archive-agpm40.md)

-   [<span data-ttu-id="2850e-120">Контрольный список: создание, редактирование и развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="2850e-120">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo-agpm40.md)

-   [<span data-ttu-id="2850e-121">Поиск и фильтрация списка объектов групповой политики</span><span class="sxs-lookup"><span data-stu-id="2850e-121">Search and Filter the List of GPOs</span></span>](search-and-filter-the-list-of-gpos.md)

-   [<span data-ttu-id="2850e-122">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="2850e-122">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

-   [<span data-ttu-id="2850e-123">Выполнение задач редактора</span><span class="sxs-lookup"><span data-stu-id="2850e-123">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="2850e-124">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="2850e-124">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="2850e-125">Выполнение задач рецензента</span><span class="sxs-lookup"><span data-stu-id="2850e-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

-   [<span data-ttu-id="2850e-126">Устранение неполадок AGPM</span><span class="sxs-lookup"><span data-stu-id="2850e-126">Troubleshooting AGPM</span></span>](troubleshooting-agpm-agpm40.md)

-   [<span data-ttu-id="2850e-127">Пользовательский интерфейс: расширенное управление групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="2850e-127">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

 

 





