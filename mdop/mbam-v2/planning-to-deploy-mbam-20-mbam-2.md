---
title: Планирование развертывания MBAM 2.0
description: Планирование развертывания MBAM 2.0
author: dansimp
ms.assetid: 2dc05fcd-aed9-4315-aeaf-92aaa9e0e955
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c7f065e52655212261dfe8b6b3f081f697142473
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825632"
---
# <span data-ttu-id="83835-103">Планирование развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="83835-103">Planning to Deploy MBAM 2.0</span></span>


<span data-ttu-id="83835-104">Прежде чем создавать план развертывания для администрирования и мониторинга Microsoft BitLocker (MBAM), необходимо принять ряд различных конфигураций и предварительных требований для развертывания.</span><span class="sxs-lookup"><span data-stu-id="83835-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="83835-105">В этом разделе приведены сведения, которые помогут вам собрать необходимые сведения для формулировки плана развертывания, который наилучшим образом соответствует вашим бизнес-требованиям.</span><span class="sxs-lookup"><span data-stu-id="83835-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span> <span data-ttu-id="83835-106">Если вы устанавливаете MBAM с топологией Configuration Manager, ознакомьтесь с [Разпланированием развертывания MBAM с помощью Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) для получения дополнительных сведений о планировании.</span><span class="sxs-lookup"><span data-stu-id="83835-106">If you are installing MBAM with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional planning information.</span></span>

## <span data-ttu-id="83835-107">Проверка конфигураций, поддерживаемых MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="83835-107">Review the MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="83835-108">После подготовки компьютерной среды для установки компонентов сервера MBAM и клиента убедитесь в том, что вы просматриваете поддерживаемые конфигурации, чтобы убедиться в том, что компьютеры, на которых выполняется установка MBAM, соответствуют минимальным требованиям к оборудованию и операционной системе.</span><span class="sxs-lookup"><span data-stu-id="83835-108">After preparing your computing environment for the MBAM Server and Client feature installation, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="83835-109">Дополнительные сведения о требованиях к развертыванию MBAM можно найти в статьях требования к развертыванию [MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="83835-109">For more information about MBAM deployment prerequisites, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md).</span></span>

[<span data-ttu-id="83835-110">Поддерживаемые конфигурации MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="83835-110">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

## <span data-ttu-id="83835-111">Планирование развертывания сервера и клиента для MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="83835-111">Plan for MBAM 2.0 Server and Client Deployment</span></span>


<span data-ttu-id="83835-112">Инфраструктура сервера MBAM зависит от набора функций сервера, которые можно установить на одном или нескольких серверных компьютерах в соответствии с требованиями предприятия.</span><span class="sxs-lookup"><span data-stu-id="83835-112">The MBAM Server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="83835-113">Эти возможности можно установить в распределенной конфигурации на нескольких серверах.</span><span class="sxs-lookup"><span data-stu-id="83835-113">These features can be installed in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="83835-114">**Примечание**  Установка MBAM на одном сервере рекомендуется только для лабораторных сред.</span><span class="sxs-lookup"><span data-stu-id="83835-114">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="83835-115">Клиент MBAM позволяет администраторам принудительно применять и отслеживать шифрование диска BitLocker на компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="83835-115">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="83835-116">Клиент BitLocker можно интегрировать в организацию, развертывая клиент с помощью корпоративной системы доставки программного обеспечения или установив клиентский агент на клиентских компьютерах в ходе первоначального процесса обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="83835-116">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the client agent on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="83835-117">С помощью MBAM вы можете зашифровать компьютер в своей организации до того, как пользователь получит компьютер, или позже, используя групповую политику.</span><span class="sxs-lookup"><span data-stu-id="83835-117">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="83835-118">Планирование развертывания сервера MBAM 2.0 Server</span><span class="sxs-lookup"><span data-stu-id="83835-118">Planning for MBAM 2.0 Server Deployment</span></span>](planning-for-mbam-20-server-deployment-mbam-2.md)

[<span data-ttu-id="83835-119">Планирование развертывания клиента MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="83835-119">Planning for MBAM 2.0 Client Deployment</span></span>](planning-for-mbam-20-client-deployment-mbam-2.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="83835-120">Другие ресурсы для планирования MBAM</span><span class="sxs-lookup"><span data-stu-id="83835-120">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="83835-121">Планирование для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="83835-121">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

 

 





