---
title: Определение области проекта
description: Определение области проекта
author: dansimp
ms.assetid: 84637d2a-2e30-417d-b150-dc81f414b3a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f33562452327bba9036f56d9f6f96650f00c1f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823642"
---
# <span data-ttu-id="c1ca9-103">Определение области проекта</span><span class="sxs-lookup"><span data-stu-id="c1ca9-103">Define the Project Scope</span></span>


<span data-ttu-id="c1ca9-104">При определении области охвата проекта определите следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="c1ca9-104">When defining the project scope, determine the following:</span></span>

1.  <span data-ttu-id="c1ca9-105">Конечные пользователи MED-V — расположение и количество конечных пользователей используются для определения расположения установок клиента MED-V и количества экземпляров MED-V, а также числа и размещения репозиториев изображений MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-105">The MED-V end users—the location and number of end users are used in determining the location of MED-V client installations and the number of MED-V instances, as well as the number and placement of MED-V image repositories.</span></span>

2.  <span data-ttu-id="c1ca9-106">Образы виртуальных машин (VM) для управления с помощью MED-V — определяют способ распространения изображений и размещения репозиториев изображений.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-106">The virtual machine (VM) images to be managed by MED-V—to determine the method of distributing images and placement of image repositories.</span></span>

3.  <span data-ttu-id="c1ca9-107">Ожидание уровня обслуживания Организации — определение требований к производительности и отказоустойчивости для сервера и базы данных MED-V, а также репозитория изображений.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-107">The organization’s service level expectations—to determine the performance and fault-tolerance requirements for the MED-V server and database as well as the image repository.</span></span>

4.  <span data-ttu-id="c1ca9-108">Проверка с учетом бизнеса — убедитесь в том, как запланированная инфраструктура влияет на бизнес.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-108">Validate with the business—ensure there is a complete understanding of how the planned infrastructure affects the business.</span></span>

## <span data-ttu-id="c1ca9-109">Определение конечных пользователей для MED-V</span><span class="sxs-lookup"><span data-stu-id="c1ca9-109">Define the MED-V End Users</span></span>


<span data-ttu-id="c1ca9-110">Сначала определите, где находятся конечные пользователи, а также количество пользователей в каждом расположении.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-110">First, determine where the end users are located, as well as the number of users in each location.</span></span> <span data-ttu-id="c1ca9-111">Во-вторых, получите схему сетевой инфраструктуры, в которой отображаются расположения пользователей и доступная пропускная способность в этих расположениях.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-111">Second, obtain a network infrastructure diagram that displays the user locations and the available bandwidth to those locations.</span></span> <span data-ttu-id="c1ca9-112">Кроме того, Узнайте, перемещаются ли пользователи между местами.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-112">Third, find out if users travel between locations.</span></span> <span data-ttu-id="c1ca9-113">Если пользователи перемещаются в дорогу, для проектирования серверной инфраструктуры и репозиторией изображений может потребоваться дополнительная мощность.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-113">If users travel, additional capacity may be required in the design of the server infrastructure and image repositories.</span></span>

## <span data-ttu-id="c1ca9-114">Определение изображений MED-V для управления с помощью MED-V</span><span class="sxs-lookup"><span data-stu-id="c1ca9-114">Determine the MED-V Images to Be Managed by MED-V</span></span>


<span data-ttu-id="c1ca9-115">После определения конечных пользователей MED-V определите, какие виртуальные машины будут управляться MED-V для пользователей в каждом расположении.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-115">After the MED-V end users have been defined, determine which VMs will be managed by MED-V for the users in each location.</span></span>

<span data-ttu-id="c1ca9-116">Если какая-либо из виртуальных машин хранится в централизованной библиотеке, определите расположение библиотеки, чтобы ее можно было использовать в качестве репозитория MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-116">If any of the VMs are stored in a centralized library, determine the location of the library so that it may be evaluated for use as a MED-V repository.</span></span>

## <a href="" id="determine-the-organization-s-service-level-expectations"></a><span data-ttu-id="c1ca9-117">Определение ожидаемых для Организации ожиданий на уровне обслуживания</span><span class="sxs-lookup"><span data-stu-id="c1ca9-117">Determine the Organization’s Service Level Expectations</span></span>


<span data-ttu-id="c1ca9-118">Для каждой рабочей области MED-V Обратите внимание на допустимое время для загрузки нового изображения и временной интервал для развертывания критических обновлений.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-118">For each MED-V workspace, note the acceptable time for a new image to load and the timeframe for critical updates to be deployed.</span></span>

<span data-ttu-id="c1ca9-119">Если применимо, запишите ожидаемые уровни обслуживания для отчетности MED-V, которые будут использоваться при проектировании инфраструктуры сервера.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-119">If applicable, record the service level expectations for MED-V reporting, to be used in the design of the server infrastructure.</span></span>

## <span data-ttu-id="c1ca9-120">Проверка с учетом бизнеса</span><span class="sxs-lookup"><span data-stu-id="c1ca9-120">Validate with the Business</span></span>


<span data-ttu-id="c1ca9-121">Спросите заинтересованных лиц и владельцев приложений на следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="c1ca9-121">Ask business stakeholders and application owners the following questions:</span></span>

-   <span data-ttu-id="c1ca9-122">Можно ли объединить уже существующие изображения?</span><span class="sxs-lookup"><span data-stu-id="c1ca9-122">Are there any existing images that can be combined?</span></span> <span data-ttu-id="c1ca9-123">Например, если приложение A на WindowsXP — это один образ VPC и приложение B на WindowsXP является другим VPC-изображением, возможно, один образ может содержать оба приложения, тем самым уменьшая пространство для репозитория и пропускную способность, необходимую для загрузки изображения.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-123">For example, if application A on WindowsXP is one VPC image and application B on WindowsXP is another VPC image, perhaps a single image can contain both applications, thereby reducing repository space and bandwidth required for image download.</span></span>

-   <span data-ttu-id="c1ca9-124">Являются ли приложения, которые находятся в области, как поддерживающие, так и поддерживаемые, если они доставляются в виртуальной машине с помощью MED-V?</span><span class="sxs-lookup"><span data-stu-id="c1ca9-124">Are the in-scope applications licensable and supportable if delivered in a VM by MED-V?</span></span> <span data-ttu-id="c1ca9-125">Обратитесь к поставщику приложения, чтобы убедиться в том, что условия лицензирования и поддержки не нарушаются путем поставки приложения в MED-V.</span><span class="sxs-lookup"><span data-stu-id="c1ca9-125">Check with the application supplier to ensure that licensing and support terms will not be violated by delivering the application through MED-V.</span></span>

 

 





