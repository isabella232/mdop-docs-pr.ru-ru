---
title: Подготовка среды для развертывания MBAM 2.5
description: Подготовка среды для развертывания MBAM 2.5
author: dansimp
ms.assetid: 7552ba08-9dbf-40cd-8920-203d733fd242
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b18c9853035018c2e36dd447fbf0effbf49c45cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825492"
---
# <span data-ttu-id="2b8fa-103">Подготовка среды для развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2b8fa-103">Preparing your Environment for MBAM 2.5</span></span>


<span data-ttu-id="2b8fa-104">Прежде чем приступить к установке Microsoft BitLocker Administration и Monitoring (MBAM), убедитесь, что для установки продукта выполнены необходимые условия.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-104">Before beginning Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should make sure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="2b8fa-105">Если вы знаете, что предварительные условия загружаются заранее, вы можете эффективно развернуть продукт и включить его функции, чтобы он эффективно поддерживал бизнес-цели вашей организации.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-105">When you know what the prerequisites are ahead of time, you can efficiently deploy the product and enable its features so that it most effectively supports your organization’s business objectives.</span></span>

<span data-ttu-id="2b8fa-106">Если вы развертываете администрирование и мониторинг Microsoft BitLocker с помощью Configuration Manager, убедитесь в том, что вы отвечаете дополнительным требованиям Configuration Manager, которые перечислены далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-106">If you are deploying Microsoft BitLocker Administration and Monitoring with Configuration Manager, ensure that you meet the additional requirements for Configuration Manager, which are listed later in this topic.</span></span>

## <span data-ttu-id="2b8fa-107">Проверка требований к развертыванию MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="2b8fa-107">Review MBAM 2.5 deployment prerequisites</span></span>


<span data-ttu-id="2b8fa-108">Чтобы убедиться в том, что развертывание MBAM успешно, убедитесь, что вы просматриваете и завершаете необходимые требования к программному обеспечению перед установкой клиента MBAM и настройте компоненты сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-108">To ensure that your MBAM deployment is successful, make sure that you review and complete the required software prerequisites before you install the MBAM Client and configure the MBAM Server features.</span></span>

[<span data-ttu-id="2b8fa-109">Необходимые условия для развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2b8fa-109">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)

## <span data-ttu-id="2b8fa-110">Планирование требований к групповой политике для MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="2b8fa-110">Plan for MBAM 2.5 Group Policy requirements</span></span>


<span data-ttu-id="2b8fa-111">Перед тем как MBAM смогут управлять клиентами в корпоративной сети, необходимо скачать и настроить шаблоны групповой политики, которые относятся к MBAM, а затем настроить параметры групповой политики для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-111">Before MBAM can manage clients in the enterprise, you must download and configure Group Policy templates that are specific to MBAM, and then configure the Group Policy settings that you want for your environment.</span></span>

[<span data-ttu-id="2b8fa-112">Планирование требований групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2b8fa-112">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)

## <span data-ttu-id="2b8fa-113">Планирование ролей и учетных записей MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="2b8fa-113">Plan for MBAM 2.5 roles and accounts</span></span>


<span data-ttu-id="2b8fa-114">В рамках предварительных требований вы должны определить определенные роли и учетные записи, которые используются в MBAM для предоставления доступа к определенным серверам и функциям, таким как базы данных SQL Server и веб-приложения, запущенные на сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-114">As part of the prerequisites, you must define certain roles and accounts, which are used in MBAM to provide security and access rights to specific servers and features, such as the databases running on SQL Server and the web applications running on the Administration and Monitoring Server.</span></span>

[<span data-ttu-id="2b8fa-115">Планирование групп и учетных записей MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2b8fa-115">Planning for MBAM 2.5 Groups and Accounts</span></span>](planning-for-mbam-25-groups-and-accounts.md)

## <span data-ttu-id="2b8fa-116">Другие ресурсы для планирования MBAM</span><span class="sxs-lookup"><span data-stu-id="2b8fa-116">Other resources for MBAM planning</span></span>


[<span data-ttu-id="2b8fa-117">Планирование для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2b8fa-117">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

[<span data-ttu-id="2b8fa-118">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2b8fa-118">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

## <span data-ttu-id="2b8fa-119">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="2b8fa-119">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="2b8fa-120">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="2b8fa-120">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="2b8fa-121">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="2b8fa-121">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





