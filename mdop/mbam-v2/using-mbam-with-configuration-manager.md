---
title: Использование MBAM с диспетчером конфигураций
description: Использование MBAM с диспетчером конфигураций
author: dansimp
ms.assetid: 03868717-4aa7-4897-8166-9a3df5e9519e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e3c5dd199010ac758ab701b0753d913ea323efd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823789"
---
# <span data-ttu-id="b902f-103">Использование MBAM с диспетчером конфигураций</span><span class="sxs-lookup"><span data-stu-id="b902f-103">Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="b902f-104">При установке средства администрирования и мониторинга Microsoft BitLocker (MBAM) можно выбрать установку, которая интегрирует администрирование и мониторинг Microsoft BitLocker с помощью System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b902f-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM), you can choose an installation that integrates Microsoft BitLocker Administration and Monitoring with System Center Configuration Manager.</span></span> <span data-ttu-id="b902f-105">Список поддерживаемых версий Configuration Manager можно найти [в разделе Планирование развертывания MBAM с помощью Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="b902f-105">For a list of the supported versions of Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="b902f-106">Эта интеграция переносит инфраструктуру соответствия требованиям администрирования и мониторинга Microsoft BitLocker в собственную среду Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b902f-106">This integration moves the Microsoft BitLocker Administration and Monitoring compliance and reporting infrastructure into the native environment of Microsoft System Center Configuration Manager.</span></span> <span data-ttu-id="b902f-107">С помощью топологии Configuration Manager ИТ администраторы могут просматривать отчеты и состояние соответствия требованиям своей организации с помощью консоли управления Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b902f-107">With the Configuration Manager topology, IT administrators can view reports and the compliance status of their enterprise from the Configuration Manager Management Console.</span></span>

<span data-ttu-id="b902f-108">**Важно!**  Windows To Go не поддерживается при установке интегрированной топологии MBAM с Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="b902f-108">**Important** Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>

 

## <a href="" id="getting-started---using-mbam-with-configuration-manager"></a><span data-ttu-id="b902f-109">Приступая к работе: использование MBAM с помощью Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b902f-109">Getting Started – Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="b902f-110">В этом разделе объясняется, как MBAM работает с диспетчером конфигураций и объясняется Рекомендуемая архитектура для развертывания MBAM с помощью топологии интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b902f-110">This section describes how MBAM works with Configuration Manager and explains the recommended architecture for deploying MBAM with the Configuration Manager Integration topology.</span></span>

[<span data-ttu-id="b902f-111">Начало работы — использование MBAM с диспетчером конфигураций</span><span class="sxs-lookup"><span data-stu-id="b902f-111">Getting Started - Using MBAM with Configuration Manager</span></span>](getting-started---using-mbam-with-configuration-manager.md)

## <span data-ttu-id="b902f-112">Планирование развертывания MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="b902f-112">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="b902f-113">В этом разделе описаны требования для установки, Поддерживаемые конфигурации, а также аппаратные и программное обеспечение, которое необходимо принять перед установкой MBAM с топологией Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b902f-113">This section describes the installation prerequisites, supported configurations, and hardware and software requirements that you need to consider before you install MBAM with the Configuration Manager topology.</span></span>

[<span data-ttu-id="b902f-114">Планирование развертывания MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="b902f-114">Planning to Deploy MBAM with Configuration Manager</span></span>](planning-to-deploy-mbam-with-configuration-manager-2.md)

## <span data-ttu-id="b902f-115">Развертывание MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="b902f-115">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="b902f-116">В этом разделе описано, как развернуть MBAM с помощью Configuration Manager и инструкции по установке и настройке MBAM на сервере администрирования и сервере Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b902f-116">This section describes how to deploy MBAM with Configuration Manager, and includes instructions for installing and configuring the MBAM on the Administration and Monitoring Server and Configuration Manager Server.</span></span>

[<span data-ttu-id="b902f-117">Развертывание MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="b902f-117">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

## <span data-ttu-id="b902f-118">Расшифровка отчетов MBAM в диспетчере конфигураций</span><span class="sxs-lookup"><span data-stu-id="b902f-118">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="b902f-119">В этом разделе описаны отчеты MBAM, которые можно запустить из Configuration Manager, чтобы показать соответствие требованиям организации и требованиям конкретных компьютеров предприятия.</span><span class="sxs-lookup"><span data-stu-id="b902f-119">This section describes the MBAM reports that you can run from Configuration Manager to show the compliance of your enterprise and compliance of individual computers in your enterprise.</span></span>

[<span data-ttu-id="b902f-120">Расшифровка отчетов MBAM в диспетчере конфигураций</span><span class="sxs-lookup"><span data-stu-id="b902f-120">Understanding MBAM Reports in Configuration Manager</span></span>](understanding-mbam-reports-in-configuration-manager.md)

## <span data-ttu-id="b902f-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b902f-121">Related topics</span></span>


[<span data-ttu-id="b902f-122">Операции MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b902f-122">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





