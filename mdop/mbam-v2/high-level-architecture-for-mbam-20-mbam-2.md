---
title: Высокоуровневая архитектура для MBAM 2.0
description: Высокоуровневая архитектура для MBAM 2.0
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824702"
---
# <span data-ttu-id="596e1-103">Высокоуровневая архитектура для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="596e1-103">High-Level Architecture for MBAM 2.0</span></span>


<span data-ttu-id="596e1-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) — это решение между клиентом и сервером, которое помогает упростить подготовку и развертывание BitLocker, улучшить соответствие требованиям и создавать отчеты на BitLocker и сократить расходы на поддержку.</span><span class="sxs-lookup"><span data-stu-id="596e1-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server solution that can help you simplify BitLocker provisioning and deployment, improve compliance and reporting on BitLocker, and reduce support costs.</span></span> <span data-ttu-id="596e1-105">Администрирование и мониторинг Microsoft BitLocker включают функции, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="596e1-105">Microsoft BitLocker Administration and Monitoring includes the features that are described in this topic.</span></span>

<span data-ttu-id="596e1-106">Администрирование и мониторинг Microsoft BitLocker можно развертывать в изолированной топологии или в топологии, интегрированной с Microsoft System Center Configuration Manager 2007 или MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="596e1-106">Microsoft BitLocker Administration and Monitoring can be deployed in the Stand-alone topology, or in a topology that is integrated with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="596e1-107">В этом разделе описана архитектура изолированной топологии.</span><span class="sxs-lookup"><span data-stu-id="596e1-107">This topic describes the architecture for the Stand-alone topology.</span></span> <span data-ttu-id="596e1-108">Сведения о развертывании в топологии интегрированного Configuration Manager можно найти в разделе [Использование MBAM в Configuration Manager](using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="596e1-108">For information about deploying in the integrated Configuration Manager topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span>

<span data-ttu-id="596e1-109">На приведенной ниже схеме показана Рекомендуемая архитектура MBAM для рабочей среды, которая состоит из двух серверов и рабочей станции управления.</span><span class="sxs-lookup"><span data-stu-id="596e1-109">The following diagram shows the MBAM recommended architecture for a production environment, which consists of two servers and a management workstation.</span></span> <span data-ttu-id="596e1-110">Эта архитектура поддерживает до 200 000 MBAM клиентов.</span><span class="sxs-lookup"><span data-stu-id="596e1-110">This architecture supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="596e1-111">Серверные функции и базы данных на изображении архитектуры описаны в следующем разделе и указаны в списке под компьютером или сервером, где они рекомендуются для их установки.</span><span class="sxs-lookup"><span data-stu-id="596e1-111">The server features and databases in the architecture image are described in the following section and are listed under the computer or server where we recommend that you install them.</span></span>

<span data-ttu-id="596e1-112">**Примечание**  Архитектура с одним сервером следует использовать только в тестовых средах.</span><span class="sxs-lookup"><span data-stu-id="596e1-112">**Note** A single-server architecture should be used only in test environments.</span></span>

 

![MBAM 2 2 — топология развертывания сервера](images/mbam2-3-servers.gif)

## <span data-ttu-id="596e1-114">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="596e1-114">Administration and Monitoring Server</span></span>


<span data-ttu-id="596e1-115">На этом сервере установлены следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="596e1-115">The following features are installed on this server:</span></span>

-   <span data-ttu-id="596e1-116">**Сервер администрирования и наблюдения**.</span><span class="sxs-lookup"><span data-stu-id="596e1-116">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="596e1-117">Сервер администрирования и мониторинга установлен на сервере Windows и включает веб-сайт администрирования и наблюдения, включающий отчеты и портал службы поддержки и веб-службы мониторинга.</span><span class="sxs-lookup"><span data-stu-id="596e1-117">The Administration and Monitoring Server feature is installed on a Windows server and consists of the Administration and Monitoring website, which includes the reports and the Help Desk Portal, and the monitoring web services.</span></span>

-   <span data-ttu-id="596e1-118">**Портал самообслуживания**.</span><span class="sxs-lookup"><span data-stu-id="596e1-118">**Self-Service Portal**.</span></span> <span data-ttu-id="596e1-119">Портал самообслуживания установлен на сервере Windows.</span><span class="sxs-lookup"><span data-stu-id="596e1-119">The Self-Service Portal is installed on a Windows server.</span></span> <span data-ttu-id="596e1-120">Портал самообслуживания позволяет конечным пользователям на клиентских компьютерах независимо входить на веб-сайт, где они могут получить ключ восстановления для восстановления заблокированного тома BitLocker.</span><span class="sxs-lookup"><span data-stu-id="596e1-120">The Self-Service Portal enables end users on client computers to independently log on to a website, where they can obtain a recovery key to recover a locked BitLocker volume.</span></span>

## <span data-ttu-id="596e1-121">Сервер базы данных</span><span class="sxs-lookup"><span data-stu-id="596e1-121">Database Server</span></span>


<span data-ttu-id="596e1-122">На этом сервере установлены следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="596e1-122">The following features are installed on this server:</span></span>

-   <span data-ttu-id="596e1-123">**Базу данных восстановления**.</span><span class="sxs-lookup"><span data-stu-id="596e1-123">**Recovery Database**.</span></span> <span data-ttu-id="596e1-124">База данных восстановления устанавливается на сервере Windows и поддерживаемом экземпляре Microsoft SQLServer.</span><span class="sxs-lookup"><span data-stu-id="596e1-124">The Recovery Database is installed on a Windows server and a supported instance of Microsoft SQLServer.</span></span> <span data-ttu-id="596e1-125">Эта база данных хранит данные для восстановления, собранные из клиентских компьютеров MBAM.</span><span class="sxs-lookup"><span data-stu-id="596e1-125">This database stores recovery data that is collected from MBAM client computers.</span></span>

-   <span data-ttu-id="596e1-126">**База данных соответствия требованиям и аудита**.</span><span class="sxs-lookup"><span data-stu-id="596e1-126">**Compliance and Audit Database**.</span></span> <span data-ttu-id="596e1-127">База данных соответствия и аудита установлена на сервере Windows и поддерживаемом экземпляром SQLServer.</span><span class="sxs-lookup"><span data-stu-id="596e1-127">The Compliance and Audit Database is installed on a Windows server and a supported instance of SQLServer.</span></span> <span data-ttu-id="596e1-128">Эта база данных хранит данные соответствия требованиям для клиентских компьютеров MBAM.</span><span class="sxs-lookup"><span data-stu-id="596e1-128">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="596e1-129">Эти данные используются преимущественно для отчетов, которые являются узлами служб SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="596e1-129">This data is used primarily for reports that SQL Server Reporting Services (SSRS) hosts.</span></span>

-   <span data-ttu-id="596e1-130">**Отчеты о соответствии и аудите**.</span><span class="sxs-lookup"><span data-stu-id="596e1-130">**Compliance and Audit Reports**.</span></span> <span data-ttu-id="596e1-131">Отчеты о соответствии и аудите устанавливаются на сервере Windows и поддерживаемом экземпляром SQLServer, на котором установлена функция служб SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="596e1-131">The Compliance and Audit Reports are installed on a Windows server and a supported instance of SQLServer that has the SQL Server Reporting Services (SSRS) feature installed.</span></span> <span data-ttu-id="596e1-132">Эти отчеты предоставляют отчеты MBAM, к которым можно получить доступ с веб-сайта администрирования и мониторинга либо непосредственно с сервера служб SSRS.</span><span class="sxs-lookup"><span data-stu-id="596e1-132">These reports provide MBAM reports that you can access from the Administration and Monitoring website or directly from the SSRS server.</span></span>

## <span data-ttu-id="596e1-133">Рабочая станция для управления</span><span class="sxs-lookup"><span data-stu-id="596e1-133">Management Workstation</span></span>


<span data-ttu-id="596e1-134">Следующий компонент установлен на рабочей станции управления, которая может быть Windows Server или клиентским компьютером.</span><span class="sxs-lookup"><span data-stu-id="596e1-134">The following feature is installed on the Management workstation, which can be a Windows server or a client computer.</span></span>

-   <span data-ttu-id="596e1-135">**Шаблон политики**.</span><span class="sxs-lookup"><span data-stu-id="596e1-135">**Policy Template**.</span></span> <span data-ttu-id="596e1-136">Шаблон политики состоит из параметров групповой политики, которые определяют параметры реализации MBAM для шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="596e1-136">The Policy Template consists of Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="596e1-137">Вы можете установить шаблон политики на любой сервер или рабочую станцию, но это значит, что он обычно установлен на рабочей станции управления, который является поддерживаемым сервером Windows или клиентским компьютером.</span><span class="sxs-lookup"><span data-stu-id="596e1-137">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation, which is a supported Windows server or client computer.</span></span> <span data-ttu-id="596e1-138">Рабочая станция не должна быть выделенным компьютером.</span><span class="sxs-lookup"><span data-stu-id="596e1-138">The workstation does not have to be a dedicated computer.</span></span>

## <a href="" id="---------mbam-client"></a> <span data-ttu-id="596e1-139">Клиент MBAM</span><span class="sxs-lookup"><span data-stu-id="596e1-139">MBAM Client</span></span>


<span data-ttu-id="596e1-140">Клиент MBAM установлен на компьютере с Windows и обладает следующими характеристиками:</span><span class="sxs-lookup"><span data-stu-id="596e1-140">The MBAM Client is installed on a Windows computer and has the following characteristics:</span></span>

-   <span data-ttu-id="596e1-141">Использование групповой политики для принудительного шифрования диска BitLocker на клиентских компьютерах в сети.</span><span class="sxs-lookup"><span data-stu-id="596e1-141">Uses Group Policy to enforce the BitLocker drive encryption of client computers in the enterprise.</span></span>

-   <span data-ttu-id="596e1-142">Собирает ключ восстановления для трех типов дисков данных BitLocker: диски операционной системы, несъемные диски с данными и съемные носители данных (USB).</span><span class="sxs-lookup"><span data-stu-id="596e1-142">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

-   <span data-ttu-id="596e1-143">Собирает данные о соответствии для компьютера и передает их в систему отчетности.</span><span class="sxs-lookup"><span data-stu-id="596e1-143">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

## <span data-ttu-id="596e1-144">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="596e1-144">Related topics</span></span>


[<span data-ttu-id="596e1-145">Начало работы с MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="596e1-145">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





