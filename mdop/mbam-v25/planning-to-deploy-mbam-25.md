---
title: Планирование развертывания MBAM 2.5
description: Планирование развертывания MBAM 2.5
author: dansimp
ms.assetid: 1343b80c-d87a-42e7-b912-e84ba997d7e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e955b426b00539aa2a4ef0b7c3a6650b05633a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826692"
---
# <span data-ttu-id="10c83-103">Планирование развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="10c83-103">Planning to Deploy MBAM 2.5</span></span>


<span data-ttu-id="10c83-104">Прежде чем создавать план развертывания для администрирования и мониторинга Microsoft BitLocker (MBAM), необходимо принять ряд различных конфигураций и предварительных требований для развертывания.</span><span class="sxs-lookup"><span data-stu-id="10c83-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="10c83-105">В этом разделе приведены сведения, которые помогут вам собрать необходимые сведения для формулировки плана развертывания, который наилучшим образом соответствует вашим бизнес-требованиям.</span><span class="sxs-lookup"><span data-stu-id="10c83-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span>

## <span data-ttu-id="10c83-106">Проверка конфигураций, поддерживаемых MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="10c83-106">Review the MBAM 2.5 supported configurations</span></span>


<span data-ttu-id="10c83-107">После подготовки вычислительной среды для развертывания MBAM сервера и клиента убедитесь, что вы просматриваете поддерживаемые конфигурации, чтобы убедиться в том, что компьютеры, на которых выполняется установка MBAM, соответствуют минимальным требованиям к оборудованию и операционной системе.</span><span class="sxs-lookup"><span data-stu-id="10c83-107">After preparing your computing environment for the MBAM Server and Client feature deployment, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="10c83-108">Дополнительные сведения о требованиях к развертыванию MBAM можно найти в статьях требования к развертыванию [MBAM 2,5](mbam-25-deployment-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="10c83-108">For more information about MBAM deployment prerequisites, see [MBAM 2.5 Deployment Prerequisites](mbam-25-deployment-prerequisites.md).</span></span>

[<span data-ttu-id="10c83-109">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="10c83-109">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

## <span data-ttu-id="10c83-110">Планирование развертывания сервера и клиента для MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="10c83-110">Plan for MBAM 2.5 Server and Client deployment</span></span>


<span data-ttu-id="10c83-111">Инфраструктура сервера MBAM зависит от набора функций сервера, которые можно настроить на одном или нескольких компьютерах, основываясь на требованиях предприятия.</span><span class="sxs-lookup"><span data-stu-id="10c83-111">The MBAM Server infrastructure depends on a set of server features that can be configured on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="10c83-112">Эти возможности можно настроить в распределенной конфигурации на нескольких серверах.</span><span class="sxs-lookup"><span data-stu-id="10c83-112">These features can be configured in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="10c83-113">**Примечание**  Установка MBAM на одном сервере рекомендуется только для лабораторных сред.</span><span class="sxs-lookup"><span data-stu-id="10c83-113">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="10c83-114">Клиент MBAM позволяет администраторам принудительно применять и отслеживать шифрование диска BitLocker на компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="10c83-114">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="10c83-115">Клиент BitLocker может быть интегрирован в организацию путем развертывания клиента через корпоративную систему доставки программного обеспечения или установки клиента на клиентские компьютеры в ходе первоначального процесса обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="10c83-115">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the Client on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="10c83-116">С помощью MBAM вы можете зашифровать компьютер в своей организации до того, как пользователь получит компьютер, или позже, используя групповую политику.</span><span class="sxs-lookup"><span data-stu-id="10c83-116">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="10c83-117">Планирование развертывания сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="10c83-117">Planning for MBAM 2.5 Server Deployment</span></span>](planning-for-mbam-25-server-deployment.md)

[<span data-ttu-id="10c83-118">Планирование развертывания клиента MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="10c83-118">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="10c83-119">Другие ресурсы для планирования MBAM</span><span class="sxs-lookup"><span data-stu-id="10c83-119">Other resources for MBAM planning</span></span>


[<span data-ttu-id="10c83-120">Планирование для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="10c83-120">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

## <span data-ttu-id="10c83-121">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="10c83-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="10c83-122">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="10c83-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="10c83-123">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="10c83-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





