---
title: Развертывание инфраструктуры сервера MBAM 2.0 Server
description: Развертывание инфраструктуры сервера MBAM 2.0 Server
author: dansimp
ms.assetid: 52e68d94-e2b4-4b06-ae55-f900ea6cc59f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22a69fe8f6853c02a818bb026b36771cd09632f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824759"
---
# <span data-ttu-id="fd4ea-103">Развертывание инфраструктуры сервера MBAM 2.0 Server</span><span class="sxs-lookup"><span data-stu-id="fd4ea-103">Deploying the MBAM 2.0 Server Infrastructure</span></span>


<span data-ttu-id="fd4ea-104">Компоненты сервера администрирования и мониторинга Microsoft BitLocker (MBAM) для изолированной топологии можно установить в разных конфигурациях на нескольких серверах в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-104">Microsoft BitLocker Administration and Monitoring (MBAM) Server features for the Stand-alone topology can be installed in different configurations on two or more servers in a production environment.</span></span> <span data-ttu-id="fd4ea-105">Рекомендуемая конфигурация — это два сервера для производственной среды в зависимости от требований к масштабируемости.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-105">The recommended configuration is two servers for a production environment, depending on your scalability requirements.</span></span> <span data-ttu-id="fd4ea-106">Используйте один сервер для установки MBAM только в тестовых средах.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-106">Use a single server for an MBAM installation only in test environments.</span></span> <span data-ttu-id="fd4ea-107">Дополнительные сведения о планировании развертывания компонентов сервера MBAM можно найти в разделе [Планирование развертывания сервера MBAM 2,0](planning-for-mbam-20-server-deployment-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="fd4ea-107">For more information about planning for the MBAM Server feature deployment, see [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md).</span></span>

<span data-ttu-id="fd4ea-108">На приведенной ниже схеме показан пример настройки рекомендуемого развертывания MBAM для двух серверов.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-108">The following diagram shows an example of how you can configure the recommended two-server MBAM deployment.</span></span> <span data-ttu-id="fd4ea-109">Эта конфигурация поддерживает до 200 000 MBAM клиентов в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-109">This configuration supports up to 200,000 MBAM clients in a production environment.</span></span> <span data-ttu-id="fd4ea-110">Серверные функции и базы данных на изображении архитектуры описаны в следующем разделе и указаны в списке под компьютером или сервером, где они рекомендуются для их установки.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-110">The server features and databases in the architecture image are described in the following section and are listed under the computer or server where we recommend that you install them.</span></span>

![MBAM 2 2 — топология развертывания сервера](images/mbam2-3-servers.gif)

## <span data-ttu-id="fd4ea-112">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="fd4ea-112">Administration and Monitoring Server</span></span>


<span data-ttu-id="fd4ea-113">На этом сервере установлены следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="fd4ea-113">The following features are installed on this server:</span></span>

-   <span data-ttu-id="fd4ea-114">**Сервер администрирования и наблюдения**.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-114">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="fd4ea-115">Сервер администрирования и мониторинга установлен на сервере Windows и состоит из веб-сайта службы поддержки и веб-служб мониторинга.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-115">The Administration and Monitoring Server feature is installed on a Windows server and consists of the Help Desk website and the monitoring web services.</span></span>

-   <span data-ttu-id="fd4ea-116">**Портал самообслуживания**.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-116">**Self-Service Portal**.</span></span> <span data-ttu-id="fd4ea-117">Портал самообслуживания установлен на сервере Windows.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-117">The Self-Service Portal is installed on a Windows server.</span></span> <span data-ttu-id="fd4ea-118">Портал самообслуживания позволяет конечным пользователям на клиентских компьютерах независимо входить на веб-сайт, где они могут получить ключ восстановления для восстановления заблокированного тома BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-118">The Self-Service Portal enables end users on client computers to independently log on to a website, where they can obtain a recovery key to recover a locked BitLocker volume.</span></span>

## <span data-ttu-id="fd4ea-119">Сервер базы данных</span><span class="sxs-lookup"><span data-stu-id="fd4ea-119">Database Server</span></span>


<span data-ttu-id="fd4ea-120">На этом сервере установлены следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="fd4ea-120">The following features are installed on this server:</span></span>

-   <span data-ttu-id="fd4ea-121">**Базу данных восстановления**.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-121">**Recovery Database**.</span></span> <span data-ttu-id="fd4ea-122">База данных восстановления устанавливается на сервере Windows и поддерживаемом экземпляре Microsoft SQLServer.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-122">The Recovery Database is installed on a Windows server and a supported instance of Microsoft SQLServer.</span></span> <span data-ttu-id="fd4ea-123">Эта база данных хранит данные для восстановления, собранные из клиентских компьютеров MBAM.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-123">This database stores recovery data that is collected from MBAM client computers.</span></span>

-   <span data-ttu-id="fd4ea-124">**База данных соответствия требованиям и аудита**.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-124">**Compliance and Audit Database**.</span></span> <span data-ttu-id="fd4ea-125">База данных соответствия и аудита установлена на сервере Windows и поддерживаемом экземпляром SQLServer.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-125">The Compliance and Audit Database is installed on a Windows server and a supported instance of SQLServer.</span></span> <span data-ttu-id="fd4ea-126">Эта база данных хранит данные соответствия требованиям для клиентских компьютеров MBAM.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-126">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="fd4ea-127">Эти данные используются преимущественно для отчетов, которые являются узлами служб SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="fd4ea-127">This data is used primarily for reports that SQL Server Reporting Services (SSRS) hosts.</span></span>

-   <span data-ttu-id="fd4ea-128">**Отчеты о соответствии и аудите**.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-128">**Compliance and Audit Reports**.</span></span> <span data-ttu-id="fd4ea-129">Отчеты о соответствии и аудите устанавливаются на сервере Windows и поддерживаемом экземпляром SQLServer, на котором установлена функция служб SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="fd4ea-129">The Compliance and Audit Reports are installed on a Windows server and a supported instance of SQLServer that has the SQL Server Reporting Services (SSRS) feature installed.</span></span> <span data-ttu-id="fd4ea-130">Эти отчеты предоставляют отчеты MBAM, доступ к которым можно получить на веб-сайте службы поддержки или непосредственно с сервера служб SSRS.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-130">These reports provide MBAM reports that you can access from the Help Desk website or directly from the SSRS server.</span></span>

## <span data-ttu-id="fd4ea-131">Рабочая станция для управления</span><span class="sxs-lookup"><span data-stu-id="fd4ea-131">Management Workstation</span></span>


<span data-ttu-id="fd4ea-132">Следующий компонент установлен на рабочей станции управления, которая может быть Windows Server или клиентским компьютером.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-132">The following feature is installed on the Management Workstation, which can be a Windows server or a client computer.</span></span>

-   <span data-ttu-id="fd4ea-133">**Шаблон политики**.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-133">**Policy Template**.</span></span> <span data-ttu-id="fd4ea-134">Шаблон политики состоит из групповых политик, которые определяют параметры реализации MBAM для шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-134">The Policy Template consists of Group Policies that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="fd4ea-135">Вы можете установить шаблон политики на любой сервер или рабочую станцию, но это значит, что он обычно установлен на рабочей станции управления, который является поддерживаемым сервером Windows или клиентским компьютером.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-135">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation, which is a supported Windows server or client computer.</span></span> <span data-ttu-id="fd4ea-136">Рабочая станция не должна быть выделенным компьютером.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-136">The workstation does not have to be a dedicated computer.</span></span>

## <a href="" id="---------mbam-client"></a> <span data-ttu-id="fd4ea-137">Клиент MBAM</span><span class="sxs-lookup"><span data-stu-id="fd4ea-137">MBAM Client</span></span>


<span data-ttu-id="fd4ea-138">Клиент MBAM установлен на компьютере с Windows и обладает следующими характеристиками:</span><span class="sxs-lookup"><span data-stu-id="fd4ea-138">The MBAM Client is installed on a Windows computer and has the following characteristics:</span></span>

-   <span data-ttu-id="fd4ea-139">Использование групповой политики для принудительного шифрования диска BitLocker на клиентских компьютерах в сети.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-139">Uses Group Policy to enforce the BitLocker drive encryption of client computers in the enterprise.</span></span>

-   <span data-ttu-id="fd4ea-140">Собирает ключ восстановления для трех типов дисков данных BitLocker: диски операционной системы, несъемные диски с данными и съемные носители данных (USB).</span><span class="sxs-lookup"><span data-stu-id="fd4ea-140">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

-   <span data-ttu-id="fd4ea-141">Собирает данные о соответствии для компьютера и передает их в систему отчетности.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-141">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

## <span data-ttu-id="fd4ea-142">Другие ресурсы по развертыванию функций сервера MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="fd4ea-142">Other Resources for Deploying MBAM 2.0 Server Features</span></span>


[<span data-ttu-id="fd4ea-143">Развертывание MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="fd4ea-143">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





