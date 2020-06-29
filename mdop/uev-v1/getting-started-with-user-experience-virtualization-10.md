---
title: Начало работы с User Experience Virtualization 1.0
description: Начало работы с User Experience Virtualization 1.0
author: dansimp
ms.assetid: 74a068dc-4f87-4cb4-b114-8ca2a37149f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 010cefc42c8f2d65ac7f815eff51ec2df42df4d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827119"
---
# <span data-ttu-id="e226c-103">Начало работы с User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="e226c-103">Getting Started With User Experience Virtualization 1.0</span></span>


<span data-ttu-id="e226c-104">Виртуализация взаимодействия с пользователем Microsoft (UE-V) захватывает и централизует параметры приложения и параметры операционной системы Windows для пользователя.</span><span class="sxs-lookup"><span data-stu-id="e226c-104">Microsoft User Experience Virtualization (UE-V) captures and centralizes application settings and Windows operating system settings for the user.</span></span> <span data-ttu-id="e226c-105">Затем эти параметры применяются к разным компьютерам, к которым пользователь обращается, включая настольные компьютеры, Ноутбуки и сеансы инфраструктуры виртуальных рабочих столов (VDI).</span><span class="sxs-lookup"><span data-stu-id="e226c-105">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="e226c-106">UE-V поддерживает синхронизацию параметров для распространенных приложений Microsoft и параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="e226c-106">UE-V offers settings synchronization for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="e226c-107">Она также предоставляет параметры пользователя в любое время, где бы ни находились пользователи в рамках всего предприятия.</span><span class="sxs-lookup"><span data-stu-id="e226c-107">It also delivers user settings at any time to wherever users work throughout the enterprise.</span></span> <span data-ttu-id="e226c-108">UE-V позволяет администраторам указывать, какие параметры приложения и параметры Windows перемещаются.</span><span class="sxs-lookup"><span data-stu-id="e226c-108">UE-V allows administrators to specify which application settings and Windows settings roam.</span></span> <span data-ttu-id="e226c-109">UE-V позволяет администраторам создавать пользовательские шаблоны расположения параметров для сторонних или бизнес-приложений, используемых в Организации.</span><span class="sxs-lookup"><span data-stu-id="e226c-109">UE-V helps administrators to create custom settings location templates for third-party or line-of-business applications that are used in the enterprise.</span></span>

<span data-ttu-id="e226c-110">Виртуализация взаимодействия с пользователем обеспечивает улучшенное взаимодействие с виртуализацией пользовательского состояния.</span><span class="sxs-lookup"><span data-stu-id="e226c-110">User Experience Virtualization delivers an enhanced user state virtualization experience.</span></span> <span data-ttu-id="e226c-111">Он обеспечивает единую настройку параметров пользователя в указанных ниже случаях.</span><span class="sxs-lookup"><span data-stu-id="e226c-111">It provides consistent personalization of the user’s settings in the following scenarios:</span></span>

-   <span data-ttu-id="e226c-112">Перемещаемые пользовательские приложения и параметры Windows между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="e226c-112">Roaming user application and Windows settings between computers.</span></span>

-   <span data-ttu-id="e226c-113">Перемещаемые параметры пользователя между экземплярами приложения, которые развертываются разными способами.</span><span class="sxs-lookup"><span data-stu-id="e226c-113">Roaming user settings between the instances of an application that are deployed by using different methods:</span></span>

    -   <span data-ttu-id="e226c-114">Установленные приложения</span><span class="sxs-lookup"><span data-stu-id="e226c-114">Installed applications</span></span>

    -   <span data-ttu-id="e226c-115">Упорядоченные приложения Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="e226c-115">Application Virtualization (App-V) sequenced applications</span></span>

    -   <span data-ttu-id="e226c-116">Приложения RemoteApp (виртуализация удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="e226c-116">RemoteApp (Remote Desktop Virtualization) applications</span></span>

-   <span data-ttu-id="e226c-117">Восстановление параметров компьютера после замены, обновления оборудования или пересоздания образа.</span><span class="sxs-lookup"><span data-stu-id="e226c-117">Recovering settings for a computer after replacement, hardware upgrade, or reimage.</span></span>

<span data-ttu-id="e226c-118">Для использования этого продукта необходимо тщательное планирование перед развертыванием и использованием его функций.</span><span class="sxs-lookup"><span data-stu-id="e226c-118">This product requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="e226c-119">Поскольку этот продукт может повлиять на все компьютеры в вашей организации, вы можете помешать всей сети, если вы не планируете развертывание с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="e226c-119">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="e226c-120">Однако если вы тщательно планируете развертывание и хотите управлять им в соответствии с бизнес-потребностями, этот продукт поможет вам уменьшить затраты на администрирование и общую стоимость владения.</span><span class="sxs-lookup"><span data-stu-id="e226c-120">However, if you plan your deployment carefully and manage it so that it meets your business needs, this product can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="e226c-121">Если вы не знакомы с этим продуктом, мы рекомендуем вам внимательно ознакомиться с документацией.</span><span class="sxs-lookup"><span data-stu-id="e226c-121">If you are new to this product, we recommend that you read the documentation carefully.</span></span> <span data-ttu-id="e226c-122">Перед развертыванием продукта в рабочей среде мы рекомендуем проверить план развертывания в среде тестовой сети.</span><span class="sxs-lookup"><span data-stu-id="e226c-122">Before you deploy the product to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="e226c-123">Вы также можете воспользоваться классом, чтобы узнать о необходимых технологиях.</span><span class="sxs-lookup"><span data-stu-id="e226c-123">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="e226c-124">Дополнительные сведения о возможностях обучения Microsoft можно найти в разделе Общие сведения о Microsoft Training <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="e226c-124">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="e226c-125">**Примечание**  Недоступна загружаемая версия руководства администратора.</span><span class="sxs-lookup"><span data-stu-id="e226c-125">**Note** A downloadable version of this administrator’s guide is not available.</span></span> <span data-ttu-id="e226c-126">Тем не менее, вы можете узнать о специальных режимах библиотеки TechNet, где можно выбрать статьи, сгруппировать их в коллекцию, распечатать или экспортировать в файл по адресу <https://go.microsoft.com/fwlink/?LinkId=272497> ( https://go.microsoft.com/fwlink/?LinkId=272497) .</span><span class="sxs-lookup"><span data-stu-id="e226c-126">However, you can learn about a special mode of the TechNet Library that allows you to select articles, group them in a collection, and print them or export them to a file at <https://go.microsoft.com/fwlink/?LinkId=272497> (https://go.microsoft.com/fwlink/?LinkId=272497).</span></span>

 

## <span data-ttu-id="e226c-127">Приступая к работе с темами Microsoft User Experience Virtualization</span><span class="sxs-lookup"><span data-stu-id="e226c-127">Getting started with Microsoft User Experience Virtualization topics</span></span>


-   [<span data-ttu-id="e226c-128">Сведения о User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="e226c-128">About User Experience Virtualization 1.0</span></span>](about-user-experience-virtualization-10.md)

    <span data-ttu-id="e226c-129">В этой статье описаны функциональные возможности и функции виртуализации взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="e226c-129">Describes the functionality and features of User Experience Virtualization.</span></span>

-   [<span data-ttu-id="e226c-130">Высокоуровневая архитектура для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="e226c-130">High-Level Architecture for UE-V 1.0</span></span>](high-level-architecture-for-ue-v-10.md)

    <span data-ttu-id="e226c-131">В этой статье описаны функции виртуализации взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="e226c-131">Explains the features of User Experience Virtualization.</span></span>

-   [<span data-ttu-id="e226c-132">Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="e226c-132">Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--10-release-notes.md)

    <span data-ttu-id="e226c-133">В этой статье описаны известные проблемы, возникающие для UE-V.</span><span class="sxs-lookup"><span data-stu-id="e226c-133">Describes the known issues for UE-V.</span></span>

-   [<span data-ttu-id="e226c-134">Специальные возможности для UE-V</span><span class="sxs-lookup"><span data-stu-id="e226c-134">Accessibility for UE-V</span></span>](accessibility-for-ue-v.md)

    <span data-ttu-id="e226c-135">В этой статье описаны сочетания клавиш и сведения о специальных возможностях для UE-V.</span><span class="sxs-lookup"><span data-stu-id="e226c-135">Describes the keyboard shortcuts and accessibility information for UE-V.</span></span>

## <span data-ttu-id="e226c-136">Другие ресурсы для этого продукта</span><span class="sxs-lookup"><span data-stu-id="e226c-136">Other resources for this product</span></span>


-   [<span data-ttu-id="e226c-137">Microsoft User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="e226c-137">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

-   [<span data-ttu-id="e226c-138">Планирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="e226c-138">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

-   [<span data-ttu-id="e226c-139">Развертывание UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="e226c-139">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

-   [<span data-ttu-id="e226c-140">Операции в UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="e226c-140">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

-   [<span data-ttu-id="e226c-141">Устранение неполадок UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="e226c-141">Troubleshooting UE-V 1.0</span></span>](troubleshooting-ue-v-10.md)

 

 





