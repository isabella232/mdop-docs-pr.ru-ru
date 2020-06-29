---
title: Руководство по работе со средством расширенного управления групповыми политиками3.0
description: Руководство по работе со средством расширенного управления групповыми политиками3.0
author: dansimp
ms.assetid: aaefe6d1-a9e5-43eb-b4d8-85880798cb8b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4958609444a62560060a565fb8626bcc9680fd9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822509"
---
# <span data-ttu-id="9269d-103">Руководство по работе со средством расширенного управления групповыми политиками3.0</span><span class="sxs-lookup"><span data-stu-id="9269d-103">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>


<span data-ttu-id="9269d-104">С помощью расширенного управления групповыми политиками Майкрософт можно расширить возможности консоли управления групповыми политиками, обеспечивая полное управление изменениями и улучшенное управление объектами групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="9269d-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="9269d-105">С помощью РАСШИРЕНного многотекстовой возможности вы можете:</span><span class="sxs-lookup"><span data-stu-id="9269d-105">With AGPM you can:</span></span>

-   <span data-ttu-id="9269d-106">Автономное редактирование объектов групповой политики, так что вы можете создавать и тестировать их перед развертыванием в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="9269d-106">Perform offline editing of GPOs, so you can create and test them before deploying to a production environment.</span></span>

-   <span data-ttu-id="9269d-107">Сохраняйте несколько версий объекта групповой политики в центральном архиве, поэтому при возникновении проблемы вы можете выполнить откат.</span><span class="sxs-lookup"><span data-stu-id="9269d-107">Retain multiple versions of a GPO in a central archive, so you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="9269d-108">Предоставьте ответственность за редактирование, утверждение и проверку объектов групповой политики нескольким людям с помощью делегирования на основе ролей.</span><span class="sxs-lookup"><span data-stu-id="9269d-108">Share the responsibility for editing, approving, and reviewing GPOs among multiple people using role-based delegation.</span></span>

-   <span data-ttu-id="9269d-109">Устраните опасность нескольких администраторов групповых политик, переписывая работу друг друга с помощью функции возврата и извлечения для GPO.</span><span class="sxs-lookup"><span data-stu-id="9269d-109">Eliminate the danger of multiple Group Policy administrators overwriting each other's work by using a check-in/check-out capability for GPOs.</span></span>

-   <span data-ttu-id="9269d-110">Анализ изменений в объекте групповой политики, сравнение его с другим объектом групповой политики или другой версией того же объекта групповой политики с помощью отчетов о различиях.</span><span class="sxs-lookup"><span data-stu-id="9269d-110">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO using difference reporting.</span></span>

-   <span data-ttu-id="9269d-111">Упрощение создания объектов групповой политики с помощью шаблонов объектов групповой политики, в котором хранятся стандартные параметры, которые используются в качестве отправных точек для новых объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9269d-111">Simplify the creation of new GPOs by using GPO templates, storing standard settings to use as starting points for new GPOs.</span></span>

<span data-ttu-id="9269d-112">РАСШИРЕНная Настройка групповой политики добавляет в каждый домен, отображаемый в консоли управления групповыми политиками, папку для **изменения** , а также на вкладке " **Журнал** " для всех GPO и ссылки на групповую политику, которые отображаются в GPMC.</span><span class="sxs-lookup"><span data-stu-id="9269d-112">AGPM adds a **Change Control** folder under each domain displayed in the GPMC, as well as a **History** tab for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="9269d-113">Обзор средства расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="9269d-113">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="9269d-114">Советы и рекомендации по управлению версиями</span><span class="sxs-lookup"><span data-stu-id="9269d-114">Best Practices for Version Control</span></span>](best-practices-for-version-control.md)

-   [<span data-ttu-id="9269d-115">Контрольный список: администрирование сервера и архива AGPM</span><span class="sxs-lookup"><span data-stu-id="9269d-115">Checklist: Administer the AGPM Server and Archive</span></span>](checklist-administer-the-agpm-server-and-archive.md)

-   [<span data-ttu-id="9269d-116">Контрольный список: создание, редактирование и развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9269d-116">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="9269d-117">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="9269d-117">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

-   [<span data-ttu-id="9269d-118">Выполнение задач редактора</span><span class="sxs-lookup"><span data-stu-id="9269d-118">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="9269d-119">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="9269d-119">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="9269d-120">Выполнение задач рецензента</span><span class="sxs-lookup"><span data-stu-id="9269d-120">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

-   [<span data-ttu-id="9269d-121">Устранение неполадок средства расширенного управления групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="9269d-121">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="9269d-122">Пользовательский интерфейс: расширенное управление групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="9269d-122">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm30ops.md)

 

 





