---
title: Комплексный сценарий планирования MED-V 2.0
description: Комплексный сценарий планирования MED-V 2.0
author: dansimp
ms.assetid: e7833883-be93-4b42-9fa3-5c4d9a919058
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f34dcccade7987b8b01269caa667018a74d020c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827179"
---
# <span data-ttu-id="2822f-103">Комплексный сценарий планирования MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="2822f-103">End-to-End Planning Scenario for MED-V 2.0</span></span>


<span data-ttu-id="2822f-104">Этот пример сценария для Microsoft Enterprise Virtualization (MED-V) 2,0 поможет вам достичь целей планирования развертывания MED-V с использованием нескольких сценариев.</span><span class="sxs-lookup"><span data-stu-id="2822f-104">This sample scenario for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 helps you achieve your goal of planning your MED-V deployment by using multiple scenarios end-to-end.</span></span> <span data-ttu-id="2822f-105">Вы можете представить этот образец сценария как пример исследования, который помогает поместить отдельные сценарии и процедуры в контекст.</span><span class="sxs-lookup"><span data-stu-id="2822f-105">You can think of this sample scenario as a case study that helps put the individual scenarios and procedures in context.</span></span>

<span data-ttu-id="2822f-106">В этом разделе приведены основные сведения и инструкции по планированию развертывания для MED-V в качестве сквозного решения в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="2822f-106">This section provides basic information and directions for planning you MED-V deployment as an end-to-end solution in your enterprise.</span></span>

## <span data-ttu-id="2822f-107">Пошаговый сценарий для планирования MED-V</span><span class="sxs-lookup"><span data-stu-id="2822f-107">MED-V Planning Step-by-Step Scenario</span></span>


<span data-ttu-id="2822f-108">Ниже приведены разделы, посвященные этим пошаговым сценарием.</span><span class="sxs-lookup"><span data-stu-id="2822f-108">The topics in this step-by-step scenario include the following:</span></span>

-   <span data-ttu-id="2822f-109">[Архитектура высокого уровня](high-level-architecturemedv2.md) описывает архитектуру системы высокого уровня и проектирование компонентов MED-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="2822f-109">[High-Level Architecture](high-level-architecturemedv2.md) discusses the high-level system architecture and component design of MED-V 2.0.</span></span> <span data-ttu-id="2822f-110">MED-V расширяет возможности Virtual PC для Windows, чтобы работать с двумя операционными системами на одном устройстве, добавлять виртуальные образы, подготавливать их и централизованно управлять.</span><span class="sxs-lookup"><span data-stu-id="2822f-110">MED-V enhances Windows Virtual PC to run two operating systems on one device, adding virtual image delivery, Group Policy-based provisioning, and centralized management.</span></span> <span data-ttu-id="2822f-111">С помощью MED-V вы можете легко настраивать, развертывать и управлять корпоративными изображениями виртуальных ПК под управлением Windows на компьютерах под управлением Windows 7 Профессиональная, Enterprise и Windows 7 Ultimate.</span><span class="sxs-lookup"><span data-stu-id="2822f-111">By using MED-V, you can easily configure, deploy, and manage corporate Windows Virtual PC images on any Windows-based desktop running Windows 7 Professional, Enterprise, or Windows 7 Ultimate.</span></span>

-   <span data-ttu-id="2822f-112">[Определение и планирование развертывания MED-v](define-and-plan-your-med-v-deployment.md) обсуждение вопросов, которые следует учитывать при планировании развертывания MED-v 2,0.</span><span class="sxs-lookup"><span data-stu-id="2822f-112">[Define and Plan your MED-V Deployment](define-and-plan-your-med-v-deployment.md) discusses the considerations for planning your MED-V 2.0 deployment.</span></span> <span data-ttu-id="2822f-113">В этой статье описано, как идентифицировать системы в Организации, которые получают MED-V и рассчитывают требования к дисковому пространству.</span><span class="sxs-lookup"><span data-stu-id="2822f-113">This topic provides direction about identifying the systems in your enterprise that receive MED-V and calculating disk space requirements.</span></span> <span data-ttu-id="2822f-114">Этот раздел также помогает оценить текущую инфраструктуру и определить, как она может использоваться для развертывания MED-V.</span><span class="sxs-lookup"><span data-stu-id="2822f-114">This topic also helps evaluate your existing infrastructure and determines how it can be used for MED-V deployment.</span></span>

-   <span data-ttu-id="2822f-115">[Рекомендации для MED-v 2,0](med-v-20-best-practices.md) обсуждаются Рекомендуемые рекомендации по планированию, установке, развертыванию и управлению MED-V 2,0 в среде.</span><span class="sxs-lookup"><span data-stu-id="2822f-115">[MED-V 2.0 Best Practices](med-v-20-best-practices.md) discusses the recommended best practices for planning, installing, deploying, and managing MED-V 2.0 in your environment.</span></span> <span data-ttu-id="2822f-116">Эти рекомендации включают рекомендации, обеспечивающие более быструю работу, более эффективное использование при первом запуске, повышенную производительность и улучшенное управление виртуальными машинами.</span><span class="sxs-lookup"><span data-stu-id="2822f-116">These best practices include recommendations that produce faster run times, better operability during first time setup, increased performance, and better virtual machine management.</span></span>

## <span data-ttu-id="2822f-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2822f-117">Related topics</span></span>


[<span data-ttu-id="2822f-118">Планирование MED-V</span><span class="sxs-lookup"><span data-stu-id="2822f-118">Planning for MED-V</span></span>](planning-for-med-v.md)

[<span data-ttu-id="2822f-119">Комплексный сценарий развертывания MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="2822f-119">End-to-End Deployment Scenario for MED-V 2.0</span></span>](end-to-end-deployment-scenario-for-med-v-20.md)

[<span data-ttu-id="2822f-120">Комплексный сценарий эксплуатации MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="2822f-120">End-to-End Operations Scenario for MED-V 2.0</span></span>](end-to-end-operations-scenario-for-med-v-20.md)

 

 





