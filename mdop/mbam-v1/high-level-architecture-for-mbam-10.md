---
title: Высокоуровневая архитектура для MBAM 1.0
description: Высокоуровневая архитектура для MBAM 1.0
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de3529fdb565859fcc212d1a9a614ac4ef4b183e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825239"
---
# <span data-ttu-id="7c59a-103">Высокоуровневая архитектура для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="7c59a-103">High Level Architecture for MBAM 1.0</span></span>


<span data-ttu-id="7c59a-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) — это решение для шифрования данных между клиентом и сервером, которое помогает упростить подготовку и развертывание BitLocker, улучшить соответствие BitLocker и создавать отчеты, а также сократить расходы на поддержку.</span><span class="sxs-lookup"><span data-stu-id="7c59a-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server data encryption solution that can help you simplify BitLocker provisioning and deployment, improve BitLocker compliance and reporting, and reduce support costs.</span></span> <span data-ttu-id="7c59a-105">MBAM включает в себя функции, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="7c59a-105">MBAM includes the features that are described in this topic.</span></span>

<span data-ttu-id="7c59a-106">Кроме того, в этом видеоролике представлен обзор архитектуры MBAM и MBAM настройки.</span><span class="sxs-lookup"><span data-stu-id="7c59a-106">Additionally, there is a video that provides an overview of the MBAM architecture and MBAM Setup.</span></span> <span data-ttu-id="7c59a-107">Дополнительные сведения можно найти в статье [Обзор развертывания и архитектуры MBAM](https://go.microsoft.com/fwlink/p/?LinkId=258392).</span><span class="sxs-lookup"><span data-stu-id="7c59a-107">For more information, see [MBAM Deployment and Architecture Overview](https://go.microsoft.com/fwlink/p/?LinkId=258392).</span></span>

## <span data-ttu-id="7c59a-108">Общие сведения об архитектуре</span><span class="sxs-lookup"><span data-stu-id="7c59a-108">Architecture Overview</span></span>


<span data-ttu-id="7c59a-109">На приведенной ниже схеме показана архитектура MBAM.</span><span class="sxs-lookup"><span data-stu-id="7c59a-109">The following diagram displays the MBAM architecture.</span></span> <span data-ttu-id="7c59a-110">Односерверная топология развертывания MBAM, в которой представлены функции MBAM.</span><span class="sxs-lookup"><span data-stu-id="7c59a-110">The single-server MBAM deployment topology is shown to introduce the MBAM features.</span></span> <span data-ttu-id="7c59a-111">Однако эта топология развертывания MBAM рекомендуется только для лабораторных сред.</span><span class="sxs-lookup"><span data-stu-id="7c59a-111">However, this MBAM deployment topology is recommended only for lab environments.</span></span>

<span data-ttu-id="7c59a-112">**Примечание**  Для рабочего развертывания рекомендуется по крайней мере MBAM топология развертывания на основе трех компьютеров.</span><span class="sxs-lookup"><span data-stu-id="7c59a-112">**Note** At least a three-computer MBAM deployment topology is recommended for a production deployment.</span></span> <span data-ttu-id="7c59a-113">Дополнительные сведения о топологиях развертывания MBAM см. [в разделе Развертывание инфраструктуры сервера MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="7c59a-113">For more information about MBAM deployment topologies, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

![топология развертывания на едином сервере MBAM](images/mbam-1-server.jpg)

1.  <span data-ttu-id="7c59a-115">**Сервер администрирования и наблюдения**.</span><span class="sxs-lookup"><span data-stu-id="7c59a-115">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="7c59a-116">Сервер администрирования и мониторинга MBAM установлен на сервере Windows и размещает веб-сайт администрирования и управления MBAM и веб-службы мониторинга.</span><span class="sxs-lookup"><span data-stu-id="7c59a-116">The MBAM Administration and Monitoring Server is installed on a Windows server and hosts the MBAM Administration and Management website and the monitoring web services.</span></span> <span data-ttu-id="7c59a-117">Веб-сайт администрирования и управления MBAM используется для определения состояния соответствия требованиям предприятия, для проверки активности, для управления возможностями оборудования и для доступа к данным восстановления, таким как ключи восстановления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7c59a-117">The MBAM Administration and Management website is used to determine enterprise compliance status, to audit activity, to manage hardware capability, and to access recovery data, such as the BitLocker recovery keys.</span></span> <span data-ttu-id="7c59a-118">Сервер администрирования и наблюдения подключается к следующим базам данных и службам:</span><span class="sxs-lookup"><span data-stu-id="7c59a-118">The Administration and Monitoring Server connects to the following databases and services:</span></span>

    -   <span data-ttu-id="7c59a-119">База данных восстановления и оборудования.</span><span class="sxs-lookup"><span data-stu-id="7c59a-119">Recovery and Hardware Database.</span></span> <span data-ttu-id="7c59a-120">База данных восстановления и оборудования устанавливается на сервер под управлением Windows и поддерживаемый экземпляр SQLServer.</span><span class="sxs-lookup"><span data-stu-id="7c59a-120">The Recovery and Hardware database is installed on a Windows-based server and supported SQLServer instance.</span></span> <span data-ttu-id="7c59a-121">Эта база данных хранит данные для восстановления и сведения об оборудовании, полученные с клиентских компьютеров MBAM.</span><span class="sxs-lookup"><span data-stu-id="7c59a-121">This database stores recovery data and hardware information that is collected from MBAM client computers.</span></span>

    -   <span data-ttu-id="7c59a-122">База данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="7c59a-122">Compliance and Audit Database.</span></span> <span data-ttu-id="7c59a-123">База данных соответствия и аудита установлена на сервере Windows и поддерживаемом экземпляре SQLServer.</span><span class="sxs-lookup"><span data-stu-id="7c59a-123">The Compliance and Audit Database is installed on a Windows server and supported SQLServer instance.</span></span> <span data-ttu-id="7c59a-124">Эта база данных хранит данные соответствия требованиям для клиентских компьютеров MBAM.</span><span class="sxs-lookup"><span data-stu-id="7c59a-124">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="7c59a-125">Эти данные используются преимущественно для отчетов, размещенных службами SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="7c59a-125">This data is used primarily for reports that are hosted by SQL Server Reporting Services (SSRS).</span></span>

    -   <span data-ttu-id="7c59a-126">Отчеты о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="7c59a-126">Compliance and Audit Reports.</span></span> <span data-ttu-id="7c59a-127">Отчеты о соответствии и аудите устанавливаются на сервере под управлением Windows и поддерживает экземпляр SQLServer, на котором установлен компонент SSRS.</span><span class="sxs-lookup"><span data-stu-id="7c59a-127">The Compliance and Audit Reports are installed on a Windows-based server and supported SQLServer instance that has the SSRS feature installed.</span></span> <span data-ttu-id="7c59a-128">Эти отчеты обеспечивают администрирование и мониторинг отчетов Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7c59a-128">These reports provide Microsoft BitLocker Administration and Monitoring reports.</span></span> <span data-ttu-id="7c59a-129">Эти отчеты можно получить на веб-сайте администрирования и управления MBAM или непосредственно с сервера SSRS.</span><span class="sxs-lookup"><span data-stu-id="7c59a-129">These reports can be accessed from the MBAM Administration and Management website or directly from the SSRS Server.</span></span>

2.  <span data-ttu-id="7c59a-130">**Клиент MBAM**.</span><span class="sxs-lookup"><span data-stu-id="7c59a-130">**MBAM Client**.</span></span> <span data-ttu-id="7c59a-131">Клиент администрирования и мониторинга Microsoft BitLocker выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="7c59a-131">The Microsoft BitLocker Administration and Monitoring Client performs the following tasks:</span></span>

    -   <span data-ttu-id="7c59a-132">Использует групповую политику для принудительного шифрования BitLocker клиентских компьютеров в корпоративной среде.</span><span class="sxs-lookup"><span data-stu-id="7c59a-132">Uses Group Policy to enforce the BitLocker encryption of client computers in the enterprise.</span></span>

    -   <span data-ttu-id="7c59a-133">Собирает ключ восстановления для трех типов дисков данных BitLocker: диски операционной системы, несъемные диски с данными и съемные носители данных (USB).</span><span class="sxs-lookup"><span data-stu-id="7c59a-133">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

    -   <span data-ttu-id="7c59a-134">Сбор сведений о восстановлении и сведений об оборудовании для клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="7c59a-134">Collects recovery information and hardware information about the client computers.</span></span>

    -   <span data-ttu-id="7c59a-135">Собирает данные о соответствии для компьютера и передает их в систему отчетности.</span><span class="sxs-lookup"><span data-stu-id="7c59a-135">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

3.  <span data-ttu-id="7c59a-136">**Шаблон политики**.</span><span class="sxs-lookup"><span data-stu-id="7c59a-136">**Policy Template**.</span></span> <span data-ttu-id="7c59a-137">Шаблон групповой политики MBAM установлен на поддерживаемом сервере или клиентском компьютере под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="7c59a-137">The MBAM Group Policy template is installed on a supported Windows-based server or client computer.</span></span> <span data-ttu-id="7c59a-138">Этот шаблон используется для указания параметров реализации MBAM для шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7c59a-138">This template is used to specify the MBAM implementation settings for BitLocker drive encryption.</span></span>

## <span data-ttu-id="7c59a-139">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7c59a-139">Related topics</span></span>


[<span data-ttu-id="7c59a-140">Начало работы с MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="7c59a-140">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)

 

 





