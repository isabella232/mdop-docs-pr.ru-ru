---
title: Начало работы с MBAM 1.0
description: Начало работы с MBAM 1.0
author: dansimp
ms.assetid: 4fab4e4a-d25e-4661-b235-2b45bf5ac3e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0bbbcabfb25cfc8b24cbb4cbc3d344d4e7f209b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825272"
---
# <span data-ttu-id="71d7c-103">Начало работы с MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="71d7c-103">Getting Started with MBAM 1.0</span></span>

> <span data-ttu-id="71d7c-104">**Важно!** MBAM 1,0 подйдет к окончанию поддержки 14 сентября 2021 г.</span><span class="sxs-lookup"><span data-stu-id="71d7c-104">**IMPORTANT** MBAM 1.0 will reach end of support on September 14, 2021.</span></span> 
> <span data-ttu-id="71d7c-105">Дополнительные сведения вы найдете на [странице жизненный цикл](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) .</span><span class="sxs-lookup"><span data-stu-id="71d7c-105">See our [lifecycle page](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) for more information.</span></span> <span data-ttu-id="71d7c-106">Рекомендуем [Переход на MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) или другую поддерживаемую версию MBAM или перенос управления BitLocker в [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager).</span><span class="sxs-lookup"><span data-stu-id="71d7c-106">We recommend [migrating to MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) or another supported version of MBAM, or migrating your BitLocker management to [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager).</span></span>


<span data-ttu-id="71d7c-107">Администрирование и мониторинг Microsoft BitLocker (MBAM) требует тщательного планирования перед развертыванием и использованием ее функций.</span><span class="sxs-lookup"><span data-stu-id="71d7c-107">Microsoft BitLocker Administration and Monitoring (MBAM) requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="71d7c-108">Поскольку этот продукт может повлиять на все компьютеры в вашей организации, вы можете помешать всей сети, если вы не планируете развертывание с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="71d7c-108">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="71d7c-109">Однако если вы тщательно планируете развертывание и хотите управлять им так, чтобы оно соответствовало потребностям бизнеса, MBAM помогает уменьшить затраты на администрирование и общую стоимость владения.</span><span class="sxs-lookup"><span data-stu-id="71d7c-109">However, if you plan your deployment carefully and manage it so that it meets your business needs, MBAM can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="71d7c-110">Если вы не знакомы с этим продуктом, рекомендуем вам внимательно ознакомиться с документацией.</span><span class="sxs-lookup"><span data-stu-id="71d7c-110">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="71d7c-111">Перед развертыванием в рабочей среде мы также рекомендуем проверить план развертывания в среде тестовой сети.</span><span class="sxs-lookup"><span data-stu-id="71d7c-111">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="71d7c-112">Вы также можете воспользоваться классом, чтобы узнать о необходимых технологиях.</span><span class="sxs-lookup"><span data-stu-id="71d7c-112">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="71d7c-113">Дополнительные сведения о возможностях обучения Microsoft можно найти в разделе Общие сведения о Microsoft Training <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="71d7c-113">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="71d7c-114">**Примечание**  Вы можете найти загружаемую версию этой документации и руководство по ознакомлению с MBAM по адресу <https://go.microsoft.com/fwlink/p/?LinkId=225356> .</span><span class="sxs-lookup"><span data-stu-id="71d7c-114">**Note** You can find a downloadable version of this documentation and the MBAM Evaluation Guide at <https://go.microsoft.com/fwlink/p/?LinkId=225356>.</span></span>

 

<span data-ttu-id="71d7c-115">Этот раздел руководства администратора MBAM содержит сведения о высоком уровне MBAM, которые помогут вам понять, как ознакомиться с продуктом перед планированием развертывания.</span><span class="sxs-lookup"><span data-stu-id="71d7c-115">This section of the MBAM Administrator’s Guide includes high-level information about MBAM to provide you with a basic understanding of the product before you begin the deployment planning.</span></span> <span data-ttu-id="71d7c-116">Дополнительную документацию по MBAM можно найти на странице Загрузка ресурсов документации MBAM <https://go.microsoft.com/fwlink/p/?LinkId=258391> .</span><span class="sxs-lookup"><span data-stu-id="71d7c-116">Additional MBAM documentation can be found on the MBAM Documentation Resources Download page at <https://go.microsoft.com/fwlink/p/?LinkId=258391>.</span></span>

## <span data-ttu-id="71d7c-117">Начало работы с MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="71d7c-117">Getting started with MBAM 1.0</span></span>


-   [<span data-ttu-id="71d7c-118">Сведения о MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="71d7c-118">About MBAM 1.0</span></span>](about-mbam-10.md)

    <span data-ttu-id="71d7c-119">Высокоуровневый обзор MBAM и его использования в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="71d7c-119">Provides a high-level overview of MBAM and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="71d7c-120">Оценка MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="71d7c-120">Evaluating MBAM 1.0</span></span>](evaluating-mbam-10.md)

    <span data-ttu-id="71d7c-121">Сведения о том, как наилучшим образом оценить MBAM для использования в Организации.</span><span class="sxs-lookup"><span data-stu-id="71d7c-121">Provides information about how you can best evaluate MBAM for use in your organization.</span></span>

-   [<span data-ttu-id="71d7c-122">Высокоуровневая архитектура для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="71d7c-122">High Level Architecture for MBAM 1.0</span></span>](high-level-architecture-for-mbam-10.md)

    <span data-ttu-id="71d7c-123">Содержит описание функций MBAM и их совместной работы.</span><span class="sxs-lookup"><span data-stu-id="71d7c-123">Provides a description of the MBAM features and how they work together.</span></span>

-   [<span data-ttu-id="71d7c-124">Специальные возможности для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="71d7c-124">Accessibility for MBAM 1.0</span></span>](accessibility-for-mbam-10.md)

    <span data-ttu-id="71d7c-125">Сведения о функциях и службах, которые делают этот продукт и соответствующую документацию более удобной для людей с ограниченными возможностями.</span><span class="sxs-lookup"><span data-stu-id="71d7c-125">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="71d7c-126">Другие ресурсы для этого продукта</span><span class="sxs-lookup"><span data-stu-id="71d7c-126">Other resources for this product</span></span>


-   [<span data-ttu-id="71d7c-127">Руководство администратора для администрирования Microsoft BitLocker и мониторинга 1</span><span class="sxs-lookup"><span data-stu-id="71d7c-127">Microsoft BitLocker Administration and Monitoring 1 Administrator's Guide</span></span>](index.md)

-   [<span data-ttu-id="71d7c-128">Планирование для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="71d7c-128">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

-   [<span data-ttu-id="71d7c-129">Развертывание MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="71d7c-129">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

-   [<span data-ttu-id="71d7c-130">Операции MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="71d7c-130">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

-   [<span data-ttu-id="71d7c-131">Устранение неполадок MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="71d7c-131">Troubleshooting MBAM 1.0</span></span>](troubleshooting-mbam-10.md)

 

 





