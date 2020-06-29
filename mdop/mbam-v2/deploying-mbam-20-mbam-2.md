---
title: Развертывание MBAM 2.0
description: Развертывание MBAM 2.0
author: dansimp
ms.assetid: 4b0eaf10-81b4-427e-9d43-eb833de935a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba4423de5306e1ca204ef3b9fd31424bb8f2630f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823472"
---
# <span data-ttu-id="28264-103">Развертывание MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="28264-103">Deploying MBAM 2.0</span></span>


<span data-ttu-id="28264-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) поддерживает ряд различных конфигураций развертывания.</span><span class="sxs-lookup"><span data-stu-id="28264-104">Microsoft BitLocker Administration and Monitoring (MBAM) supports a number of different deployment configurations.</span></span> <span data-ttu-id="28264-105">Этот раздел содержит сведения о развертывании MBAM и пошаговых процедур, которые помогут вам успешно выполнять задачи, которые необходимо выполнить на разных этапах развертывания.</span><span class="sxs-lookup"><span data-stu-id="28264-105">This section includes information that you should consider about the deployment of MBAM and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

<span data-ttu-id="28264-106">Вы можете развернуть MBAM либо в изолированной топологии, либо с топологией, которая интегрирует MBAM с Microsoft System Center Configuration Manager 2007 или MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="28264-106">You can deploy MBAM either in a Stand-alone topology, or with a topology that integrates MBAM with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="28264-107">Сведения об установке MBAM с топологией с интегрированной конфигурацией Configuration Manager можно найти [в разделе Использование MBAM в Configuration Manager](using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="28264-107">For information about installing MBAM with the Configuration Manager integrated topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span>

## <span data-ttu-id="28264-108">Сведения о развертывании</span><span class="sxs-lookup"><span data-stu-id="28264-108">Deployment Information</span></span>


-   [<span data-ttu-id="28264-109">Развертывание инфраструктуры сервера MBAM 2.0 Server</span><span class="sxs-lookup"><span data-stu-id="28264-109">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

    <span data-ttu-id="28264-110">В этом разделе описаны различные параметры топологии развертывания MBAM и использование настройки MBAM для развертывания функций сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="28264-110">This section describes the different MBAM deployment topology options and how to use MBAM Setup to deploy MBAM Server features.</span></span>

-   [<span data-ttu-id="28264-111">Развертывание объектов групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="28264-111">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

    <span data-ttu-id="28264-112">В этом разделе объясняется, как создавать и развертывать объекты групповой политики MBAM, необходимые для управления клиентами MBAM и политиками шифрования BitLocker в масштабах всего предприятия.</span><span class="sxs-lookup"><span data-stu-id="28264-112">This section describes how to create and deploy MBAM Group Policy Objects that are required for managing MBAM Clients and BitLocker encryption policies throughout the enterprise.</span></span>

-   [<span data-ttu-id="28264-113">Развертывание клиента MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="28264-113">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

    <span data-ttu-id="28264-114">В этом разделе объясняется, как использовать файлы установщика клиента MBAM для развертывания программного обеспечения клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="28264-114">This section describes how to use the MBAM Client Installer files to deploy the MBAM Client software.</span></span>

-   [<span data-ttu-id="28264-115">Контрольный список необходимых компонентов развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="28264-115">MBAM 2.0 Deployment Checklist</span></span>](mbam-20-deployment-checklist-mbam-2.md)

    <span data-ttu-id="28264-116">В этом разделе представлен контрольный список развертывания, который можно использовать для развертывания функций сервера MBAM и MBAM клиента.</span><span class="sxs-lookup"><span data-stu-id="28264-116">This section provides a deployment checklist that can be used to assist in MBAM Server feature and MBAM Client deployment.</span></span>

-   [<span data-ttu-id="28264-117">Обновление с предыдущих версий MBAM</span><span class="sxs-lookup"><span data-stu-id="28264-117">Upgrading from Previous Versions of MBAM</span></span>](upgrading-from-previous-versions-of-mbam.md)

    <span data-ttu-id="28264-118">В этом разделе приводятся инструкции по обновлению MBAM из предыдущих версий.</span><span class="sxs-lookup"><span data-stu-id="28264-118">This section provides instructions for upgrading MBAM from previous versions.</span></span>

## <span data-ttu-id="28264-119">Другие ресурсы для развертывания MBAM</span><span class="sxs-lookup"><span data-stu-id="28264-119">Other Resources for Deploying MBAM</span></span>


[<span data-ttu-id="28264-120">Руководство администратора для администрирования Microsoft BitLocker и мониторинга 2</span><span class="sxs-lookup"><span data-stu-id="28264-120">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>](index.md)

[<span data-ttu-id="28264-121">Начало работы с MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="28264-121">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

[<span data-ttu-id="28264-122">Планирование для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="28264-122">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="28264-123">Операции MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="28264-123">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

[<span data-ttu-id="28264-124">Устранение неполадок MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="28264-124">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

 

 





