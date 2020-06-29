---
title: Планирование развертывания MBAM 1.0
description: Планирование развертывания MBAM 1.0
author: dansimp
ms.assetid: 30ad4304-45c6-427d-8e33-ebe8053c7871
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2ff25e705717db5086150ed08a5640335bbacb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823189"
---
# <span data-ttu-id="98400-103">Планирование развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98400-103">Planning to Deploy MBAM 1.0</span></span>


<span data-ttu-id="98400-104">Перед созданием плана развертывания Microsoft BitLocker и мониторинга (MBAM) 1,0 вы должны решить ряд различных конфигураций и предварительных требований.</span><span class="sxs-lookup"><span data-stu-id="98400-104">You should consider a number of different deployment configurations and prerequisites before you create your Microsoft BitLocker Administration and Monitoring (MBAM) 1.0 deployment plan.</span></span> <span data-ttu-id="98400-105">В этом разделе содержатся сведения о том, как собрать сведения, необходимые для формулировки плана развертывания, который наилучшим образом соответствует вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="98400-105">This section includes information that can help you gather the information that you must have to formulate a deployment plan that best meets your business requirements.</span></span>

## <span data-ttu-id="98400-106">Проверка конфигураций, поддерживаемых MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="98400-106">Review the MBAM 1.0 supported configurations</span></span>


<span data-ttu-id="98400-107">После подготовки рабочей среды для установки компонентов клиента и сервера MBAM убедитесь, что вы просматриваете сведения о поддерживаемых конфигурациях для MBAM, чтобы убедиться в том, что компьютеры, на которых вы установили MBAM, соответствуют минимальным требованиям к оборудованию и операционной системе.</span><span class="sxs-lookup"><span data-stu-id="98400-107">After you prepare your computing environment for the MBAM Client and Server feature installation, make sure that you review the Supported Configurations information for MBAM to confirm that the computers on which you install MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="98400-108">Дополнительные сведения о требованиях к развертыванию MBAM можно найти в статьях требования к развертыванию [MBAM 1,0](mbam-10-deployment-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="98400-108">For more information about MBAM deployment prerequisites, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md).</span></span>

[<span data-ttu-id="98400-109">Поддерживаемые конфигурации MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98400-109">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)

## <span data-ttu-id="98400-110">Планирование развертывания сервера и клиента для MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="98400-110">Plan for MBAM 1.0 Server and Client deployment</span></span>


<span data-ttu-id="98400-111">Инфраструктура сервера MBAM зависит от набора функций сервера, которые можно установить на одном или нескольких серверных компьютерах в соответствии с требованиями предприятия.</span><span class="sxs-lookup"><span data-stu-id="98400-111">The MBAM server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="98400-112">Эти возможности можно установить на одном сервере или распределены между несколькими серверами.</span><span class="sxs-lookup"><span data-stu-id="98400-112">These features can be installed on a single server or distributed across multiple servers.</span></span>

<span data-ttu-id="98400-113">Клиент MBAM позволяет администраторам принудительно применять и отслеживать шифрование диска BitLocker на компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="98400-113">The MBAM Client enables administrators to enforce and monitor the BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="98400-114">Клиент BitLocker можно интегрировать в организацию, развертывая клиент с помощью таких средств, как доменные службы Active Directory, или напрямую зашифровывать клиентские компьютеры как часть исходного процесса обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="98400-114">The BitLocker client can be integrated into an organization by deploying the client through tools like Active Directory Domain Services or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="98400-115">С помощью MBAM вы можете зашифровать компьютер в своей организации до того, как пользователь получит компьютер или затем, используя групповую политику.</span><span class="sxs-lookup"><span data-stu-id="98400-115">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer or afterwards, by using Group Policy.</span></span> <span data-ttu-id="98400-116">Вы можете использовать один из этих методов в своей организации.</span><span class="sxs-lookup"><span data-stu-id="98400-116">You can use one or both methods in your organization.</span></span> <span data-ttu-id="98400-117">Если вы решили использовать оба способа, вы можете улучшить соответствие требованиям, создавать отчеты и поддерживать восстановление ключей.</span><span class="sxs-lookup"><span data-stu-id="98400-117">If you choose to use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

[<span data-ttu-id="98400-118">Планирование развертывания сервера MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98400-118">Planning for MBAM 1.0 Server Deployment</span></span>](planning-for-mbam-10-server-deployment.md)

[<span data-ttu-id="98400-119">Планирование развертывания клиента MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98400-119">Planning for MBAM 1.0 Client Deployment</span></span>](planning-for-mbam-10-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="98400-120">Другие ресурсы для планирования MBAM</span><span class="sxs-lookup"><span data-stu-id="98400-120">Other resources for MBAM planning</span></span>


-   [<span data-ttu-id="98400-121">Планирование для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98400-121">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

 

 





