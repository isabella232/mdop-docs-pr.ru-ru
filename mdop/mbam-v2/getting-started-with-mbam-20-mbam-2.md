---
title: Начало работы с MBAM 2.0
description: Начало работы с MBAM 2.0
author: dansimp
ms.assetid: 29f5c9af-5bbf-4d37-aa0f-0716046904af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7c683e3d8718da24ebd2164328bda0dab0123037
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825649"
---
# <span data-ttu-id="8b0df-103">Начало работы с MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="8b0df-103">Getting Started with MBAM 2.0</span></span>


<span data-ttu-id="8b0df-104">Microsoft BitLockerAdministration и Monitoring (MBAM) 2.0 требуют тщательного планирования перед развертыванием и использованием ее функций.</span><span class="sxs-lookup"><span data-stu-id="8b0df-104">Microsoft BitLockerAdministration and Monitoring(MBAM)2.0 requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="8b0df-105">Поскольку этот продукт может повлиять на все компьютеры в вашей организации, вы можете помешать всей сети, если вы не планируете развертывание с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="8b0df-105">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="8b0df-106">Однако если вы тщательно планируете развертывание и хотите управлять им, чтобы оно соответствовало бизнес-требованиям, BitLockerAdministration и мониторинг 2.0 помогут уменьшить затраты на администрирование и общую стоимость владения.</span><span class="sxs-lookup"><span data-stu-id="8b0df-106">However, if you plan your deployment carefully and manage it so that it meets your business requirements, BitLockerAdministration and Monitoring2.0 can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="8b0df-107">Если вы не знакомы с этим продуктом, мы рекомендуем вам внимательно ознакомиться с документацией.</span><span class="sxs-lookup"><span data-stu-id="8b0df-107">If you are new to this product, we recommend that you read the documentation carefully.</span></span> <span data-ttu-id="8b0df-108">Инструкции по получению программного обеспечения MBAM можно найти в [статье как получить MDOP?](https://go.microsoft.com/fwlink/p/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="8b0df-108">To get the MBAM software, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span> <span data-ttu-id="8b0df-109">Прежде чем развертывать MBAM в рабочей среде, мы рекомендуем вам проверить план развертывания в тестовой среде.</span><span class="sxs-lookup"><span data-stu-id="8b0df-109">Before you deploy MBAM to a production environment, we also recommend that you validate your deployment plan in a test environment.</span></span> <span data-ttu-id="8b0df-110">Вы также можете воспользоваться классом, чтобы узнать о необходимых технологиях.</span><span class="sxs-lookup"><span data-stu-id="8b0df-110">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="8b0df-111">Дополнительные сведения о возможностях обучения Microsoft можно найти в разделе Общие сведения о Microsoft Training <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="8b0df-111">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="8b0df-112">Этот раздел руководства администратора MBAM 2.0 содержит подробные сведения о MBAM 2.0 для обеспечения базового понимания продукта до начала планирования развертывания.</span><span class="sxs-lookup"><span data-stu-id="8b0df-112">This section of the MBAM2.0 Administrator’s Guide includes high-level information about MBAM2.0 to provide a basic understanding of the product before you begin to plan deployment.</span></span> <span data-ttu-id="8b0df-113">Подробные сведения о развертывании MBAM с помощью интегрированной топологии Configuration Manager можно найти [в разделе Использование MBAM в Configuration Manager](using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="8b0df-113">For specific information about deploying MBAM with the Configuration Manager integrated topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="8b0df-114">Дополнительные сведения о MBAM можно найти в документации по ресурсам администрирования и мониторинга Microsoft BitLocker (MBAM) на странице загрузки <https://go.microsoft.com/fwlink/p/?LinkId=258391> .</span><span class="sxs-lookup"><span data-stu-id="8b0df-114">You can find additional MBAM documentation on the Microsoft BitLocker Administration and Monitoring (MBAM) Documentation Resources Download Page at <https://go.microsoft.com/fwlink/p/?LinkId=258391>.</span></span>

## <span data-ttu-id="8b0df-115">Начало работы с MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="8b0df-115">Getting Started with MBAM2.0</span></span>


-   [<span data-ttu-id="8b0df-116">Сведения о MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="8b0df-116">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)

    <span data-ttu-id="8b0df-117">В этой статье представлен общий обзор MBAM 2.0 и описано, как он может использоваться в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="8b0df-117">Provides a high-level overview of MBAM2.0 and describes how it can be used in your organization.</span></span>

-   [<span data-ttu-id="8b0df-118">Оценка MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="8b0df-118">Evaluating MBAM 2.0</span></span>](evaluating-mbam-20-mbam-2.md)

    <span data-ttu-id="8b0df-119">Содержит сведения о том, как лучше оценить MBAM 2.0 для использования в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="8b0df-119">Provides information about how you can best evaluate MBAM2.0 for use in your organization.</span></span>

-   [<span data-ttu-id="8b0df-120">Высокоуровневая архитектура для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="8b0df-120">High-Level Architecture for MBAM 2.0</span></span>](high-level-architecture-for-mbam-20-mbam-2.md)

    <span data-ttu-id="8b0df-121">Описаны функции MBAM 2.0 и рекомендуемая архитектура для производственной среды.</span><span class="sxs-lookup"><span data-stu-id="8b0df-121">Describes the MBAM2.0 features and the recommended architecture for a production environment.</span></span>

-   [<span data-ttu-id="8b0df-122">Специальные возможности для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="8b0df-122">Accessibility for MBAM 2.0</span></span>](accessibility-for-mbam-20-mbam-2.md)

    <span data-ttu-id="8b0df-123">В этой статье описаны сочетания клавиш, доступные для MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="8b0df-123">Describes the keyboard shortcuts that are available for MBAM2.0.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="8b0df-124">Другие ресурсы для этого продукта</span><span class="sxs-lookup"><span data-stu-id="8b0df-124">Other Resources for this Product</span></span>


[<span data-ttu-id="8b0df-125">Руководство администратора для администрирования Microsoft BitLocker и мониторинга 2</span><span class="sxs-lookup"><span data-stu-id="8b0df-125">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>](index.md)

[<span data-ttu-id="8b0df-126">Планирование для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="8b0df-126">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="8b0df-127">Развертывание MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="8b0df-127">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

[<span data-ttu-id="8b0df-128">Операции MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="8b0df-128">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

[<span data-ttu-id="8b0df-129">Устранение неполадок MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="8b0df-129">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

 

 





