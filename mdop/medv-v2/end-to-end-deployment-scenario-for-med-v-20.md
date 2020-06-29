---
title: Комплексный сценарий развертывания MED-V 2.0
description: Комплексный сценарий развертывания MED-V 2.0
author: dansimp
ms.assetid: 91bb5a9a-5fb1-4743-8494-9d4dee2ec222
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6d56e70ad359ebf2d76cf3f30f54f73cd9ca1c66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826172"
---
# <span data-ttu-id="6f08a-103">Комплексный сценарий развертывания MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="6f08a-103">End-to-End Deployment Scenario for MED-V 2.0</span></span>


<span data-ttu-id="6f08a-104">Этот пример сценария для Microsoft Enterprise Virtualization (MED-V) 2,0 помогает развертывать компоненты MED-V в Организации с помощью нескольких сценариев.</span><span class="sxs-lookup"><span data-stu-id="6f08a-104">This sample scenario for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 helps you deploy the MED-V components in your enterprise by using multiple scenarios end-to-end.</span></span> <span data-ttu-id="6f08a-105">Вы можете представить этот образец сценария как пример исследования, который помогает поместить отдельные сценарии и процедуры в контекст.</span><span class="sxs-lookup"><span data-stu-id="6f08a-105">You can think of this sample scenario as a case study that helps put the individual scenarios and procedures in context.</span></span>

<span data-ttu-id="6f08a-106">В этом разделе приведены основные сведения и инструкции по развертыванию компонентов MED-V в качестве комплексного решения в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="6f08a-106">This section provides basic information and directions for deploying MED-V components as an end-to-end solution in your enterprise.</span></span>

## <span data-ttu-id="6f08a-107">Пошаговые инструкции по развертыванию MED-V</span><span class="sxs-lookup"><span data-stu-id="6f08a-107">MED-V Deployment Step-by-step Scenario</span></span>


<span data-ttu-id="6f08a-108">Ниже приведены разделы, посвященные этим пошаговым сценарием.</span><span class="sxs-lookup"><span data-stu-id="6f08a-108">The topics in this step-by-step scenario include the following:</span></span>

-   <span data-ttu-id="6f08a-109">[Конфигурации, поддерживаемые med-v 2,0](med-v-20-supported-configurations.md) , обсуждают требования, необходимые для установки и запуска Microsoft Enterprise VIRTUALIZATION (MED-V) 2.0 в среде.</span><span class="sxs-lookup"><span data-stu-id="6f08a-109">[MED-V 2.0 Supported Configurations](med-v-20-supported-configurations.md) discusses the requirements that you must have to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0in your environment.</span></span> <span data-ttu-id="6f08a-110">В этой статье указаны требования к операционной системе, требования к конфигурации и требования к рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="6f08a-110">This topic specifies the operating system requirements, configuration requirements, and MED-V workspace requirements.</span></span> <span data-ttu-id="6f08a-111">В этой статье также содержатся сведения о локализации для языков, поддерживаемых MED-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="6f08a-111">This topic also includes localization information about the languages that MED-V 2.0 supports.</span></span>

-   <span data-ttu-id="6f08a-112">[Обзор развертывания MED-v 2,0](med-v-20-deployment-overview.md) содержит общую информацию и инструкции, которые помогут вам установить и развернуть MED-V во всей Организации.</span><span class="sxs-lookup"><span data-stu-id="6f08a-112">[MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md) discusses general information and instructions to help you install and deploy MED-V throughout your enterprise.</span></span> <span data-ttu-id="6f08a-113">Компоненты MED-V являются клиентскими и доставляются и управляются с помощью существующей инфраструктуры и процессов предприятия.</span><span class="sxs-lookup"><span data-stu-id="6f08a-113">The MED-V components are client-based and are delivered and managed by using your existing enterprise infrastructure and processes.</span></span> <span data-ttu-id="6f08a-114">В этой статье приведены общие сведения о решении MED-V, в том числе сведения о файлах установки для MED-V и развертываемых компонентах MED-V.</span><span class="sxs-lookup"><span data-stu-id="6f08a-114">This topic provides an overview of the MED-V solution that includes information about the MED-V installation files and the MED-V components that you deploy.</span></span> <span data-ttu-id="6f08a-115">В этом разделе также приводится общий обзор процесса установки и развертывания для MED-V.</span><span class="sxs-lookup"><span data-stu-id="6f08a-115">This topic also provides a high-level overview of the MED-V installation and deployment process.</span></span>

-   <span data-ttu-id="6f08a-116">[Подготовка среды развертывания для MED-v](prepare-the-deployment-environment-for-med-v.md) обсуждает процесс подготовки среды для развертывания MED-v 2,0.</span><span class="sxs-lookup"><span data-stu-id="6f08a-116">[Prepare the Deployment Environment for MED-V](prepare-the-deployment-environment-for-med-v.md) discusses how to prepare your environment for a MED-V 2.0 deployment.</span></span> <span data-ttu-id="6f08a-117">В этом разделе описаны необходимые условия, необходимые для среды MED-V, например Microsoft Windows 7 и инфраструктура Active Directory, в которой вы используете групповую политику для централизованного управления и настройки операционных систем, приложений и параметров пользователей.</span><span class="sxs-lookup"><span data-stu-id="6f08a-117">This section describes the prerequisites that are required for the MED-V environment, such as Microsoft Windows 7 and an Active Directory infrastructure in which you use Group Policy to provide centralized management and configuration of operating systems, applications, and users' settings.</span></span> <span data-ttu-id="6f08a-118">В этом разделе также описаны необходимые условия для установки и развертывания MED-V 2,0 для всего предприятия (например, Windows Virtual PC и обязательное обновление виртуальных компьютеров Windows).</span><span class="sxs-lookup"><span data-stu-id="6f08a-118">This section also describes the prerequisites that you must have for installing and deploying MED-V 2.0 throughout your enterprise, such as Windows Virtual PC and the required Windows Virtual PC update.</span></span>

-   <span data-ttu-id="6f08a-119">[Развертывание компонентов MED-v](deploy-the-med-v-components.md) описывает различные способы установки всех необходимых файлов установки и компонентов MED-v во всей Организации.</span><span class="sxs-lookup"><span data-stu-id="6f08a-119">[Deploy the MED-V Components](deploy-the-med-v-components.md) discusses the different ways you can install all of the necessary installation files and MED-V components throughout your enterprise.</span></span> <span data-ttu-id="6f08a-120">Для установки и развертывания MED-V обычно выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6f08a-120">To install and deploy MED-V, you typically follow these steps:</span></span>

    1.  <span data-ttu-id="6f08a-121">Установите **упаковщик рабочих областей med-v** на компьютере администратора, который будет использоваться для создания пакетов рабочей области для MED-v.</span><span class="sxs-lookup"><span data-stu-id="6f08a-121">Install the **MED-V Workspace Packager** on the administrator computer that you will use to build the MED-V workspace packages.</span></span> <span data-ttu-id="6f08a-122">Дополнительные сведения можно найти [в разделе Установка диспетчера рабочих областей MED-V](how-to-install-the-med-v-workspace-packager.md).</span><span class="sxs-lookup"><span data-stu-id="6f08a-122">For more information, see [How to Install the MED-V Workspace Packager](how-to-install-the-med-v-workspace-packager.md).</span></span>

    2.  <span data-ttu-id="6f08a-123">Создание и тестирование пакетов рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="6f08a-123">Create and test your MED-V workspace packages.</span></span> <span data-ttu-id="6f08a-124">Дополнительные сведения можно найти в разделе [Создание пакета рабочей области для MED-v](create-a-med-v-workspace-package.md) и [Тестирование пакета рабочей области MED-v](testing-the-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="6f08a-124">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md) and [Testing the MED-V Workspace Package](testing-the-med-v-workspace-package.md).</span></span>

    3.  <span data-ttu-id="6f08a-125">Развертывание MED-V в масштабах Организации с помощью существующего метода компании для развертывания приложений.</span><span class="sxs-lookup"><span data-stu-id="6f08a-125">Deploy MED-V throughout your enterprise by using your company’s existing method for deploying applications.</span></span> <span data-ttu-id="6f08a-126">Дополнительные сведения можно найти [в разделе Развертывание пакета рабочей области для MED-V](deploying-the-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="6f08a-126">For more information, see [Deploying the MED-V Workspace Package](deploying-the-med-v-workspace-package.md).</span></span>

## <span data-ttu-id="6f08a-127">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="6f08a-127">Related topics</span></span>


[<span data-ttu-id="6f08a-128">Развертывание MED-V</span><span class="sxs-lookup"><span data-stu-id="6f08a-128">Deployment of MED-V</span></span>](deployment-of-med-v.md)

[<span data-ttu-id="6f08a-129">Комплексный сценарий планирования MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="6f08a-129">End-to-End Planning Scenario for MED-V 2.0</span></span>](end-to-end-planning-scenario-for-med-v-20.md)

[<span data-ttu-id="6f08a-130">Комплексный сценарий эксплуатации MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="6f08a-130">End-to-End Operations Scenario for MED-V 2.0</span></span>](end-to-end-operations-scenario-for-med-v-20.md)

 

 





