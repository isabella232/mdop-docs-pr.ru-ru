---
title: Развертывание инфраструктуры сервера MBAM 1.0
description: Развертывание инфраструктуры сервера MBAM 1.0
author: dansimp
ms.assetid: 90529379-b70e-4c92-b188-3d7aaf1844af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de136db557233a097d95f47ef0a1bba5996798c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825179"
---
# <span data-ttu-id="1ec2c-103">Развертывание инфраструктуры сервера MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1ec2c-103">Deploying the MBAM 1.0 Server Infrastructure</span></span>


<span data-ttu-id="1ec2c-104">Вы можете установить компоненты сервера администрирования и мониторинга Microsoft BitLocker (MBAM) в различных конфигурациях с помощью одного или пяти серверов.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-104">You can install Microsoft BitLocker Administration and Monitoring (MBAM) Server features in different configurations by using one to five servers.</span></span> <span data-ttu-id="1ec2c-105">Как правило, следует использовать конфигурацию от трех до пяти серверов для рабочих сред, в зависимости от требований к масштабируемости.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-105">Generally, you should use a configuration of three to five servers for production environments, depending on your scalability needs.</span></span> <span data-ttu-id="1ec2c-106">Дополнительные сведения о масштабируемости MBAM и рекомендуемой топологии развертывания можно найти в [статье Руководство по масштабируемости MBAM и высокой доступности](https://go.microsoft.com/fwlink/p/?LinkId=258314).</span><span class="sxs-lookup"><span data-stu-id="1ec2c-106">For more information about performance scalability of MBAM and recommended deployment topologies, see the [MBAM Scalability and High-Availability Guide White Paper](https://go.microsoft.com/fwlink/p/?LinkId=258314).</span></span>

## <span data-ttu-id="1ec2c-107">Развертывание всех MBAM 1,0 на одном сервере</span><span class="sxs-lookup"><span data-stu-id="1ec2c-107">Deploy all MBAM 1.0 on a single server</span></span>


<span data-ttu-id="1ec2c-108">В этой конфигурации все функции MBAM устанавливаются на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-108">In this configuration, all MBAM features are installed on a single server.</span></span> <span data-ttu-id="1ec2c-109">Эта топология развертывания для инфраструктуры сервера MBAM будет поддерживать до 21 000 MBAM клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-109">This deployment topology for MBAM server infrastructure will support up to 21,000 MBAM client computers.</span></span>

<span data-ttu-id="1ec2c-110">**Важно!**  Эта конфигурация поддерживается, но мы рекомендуем использовать ее только для тестирования.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-110">**Important** This configuration is supported, but we recommend it for testing only.</span></span>

 

<span data-ttu-id="1ec2c-111">Процедуры, описанные в этом разделе, описывают полную установку функций MBAM на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-111">The procedures in this section describe the full installation of the MBAM features on a single server.</span></span>

[<span data-ttu-id="1ec2c-112">Установка и настройка MBAM на одном сервере</span><span class="sxs-lookup"><span data-stu-id="1ec2c-112">How to Install and Configure MBAM on a Single Server</span></span>](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## <span data-ttu-id="1ec2c-113">Развертывание MBAM 1,0 на распределенных серверах</span><span class="sxs-lookup"><span data-stu-id="1ec2c-113">Deploy MBAM 1.0 on distributed servers</span></span>


<span data-ttu-id="1ec2c-114">Возможности MBAM могут устанавливаться в различных конфигурациях в зависимости от требований к масштабируемости.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-114">MBAM features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="1ec2c-115">Дополнительные сведения о планировании развертывания компонентов сервера MBAM можно найти в разделе [Планирование развертывания сервера MBAM 1,0](planning-for-mbam-10-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="1ec2c-115">For more information about how to plan for MBAM server feature deployment, see [Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md).</span></span>

<span data-ttu-id="1ec2c-116">Процедуры, описанные в этом разделе, описывают полную установку функций MBAM на распределенных серверах.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-116">The procedures in this section describe the full installation of the MBAM features on distributed servers.</span></span>

### <span data-ttu-id="1ec2c-117">Конфигурация с тремя компьютерами</span><span class="sxs-lookup"><span data-stu-id="1ec2c-117">Three-computer configuration</span></span>

<span data-ttu-id="1ec2c-118">На приведенной ниже схеме показана топология развертывания на основе трех компьютеров для MBAM.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-118">The following diagram displays the three-computer deployment topology for MBAM.</span></span> <span data-ttu-id="1ec2c-119">Мы рекомендуем использовать эту топологию для рабочих сред, поддерживающих до 55 000 MBAM клиентов.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-119">We recommend this topology for production environments that support up to 55,000 MBAM Clients.</span></span>

![топология развертывания MBAM на компьютере с тремя компьютерами](images/mbam-3-server.jpg)

<span data-ttu-id="1ec2c-121">В этой конфигурации функции MBAM устанавливаются в следующей конфигурации:</span><span class="sxs-lookup"><span data-stu-id="1ec2c-121">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="1ec2c-122">База данных восстановления, базы данных соответствия требованиям и проверки соответствия требованиям и аудита устанавливаются на сервере.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-122">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="1ec2c-123">Компонент сервера администрирования и мониторинга установлен на сервере.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-123">Administration and Monitoring Server feature is installed on a server.</span></span>

3.  <span data-ttu-id="1ec2c-124">Шаблон групповой политики MBAM установлен на компьютере, способном изменять объекты групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="1ec2c-124">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects (GPO).</span></span>

### <span data-ttu-id="1ec2c-125">Конфигурация с четырьмя компьютерами</span><span class="sxs-lookup"><span data-stu-id="1ec2c-125">Four-computer configuration</span></span>

<span data-ttu-id="1ec2c-126">На приведенной ниже схеме показана топология развертывания для четырех компьютеров для MBAM.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-126">The following diagram displays the four-computer deployment topology for MBAM.</span></span> <span data-ttu-id="1ec2c-127">Мы рекомендуем использовать эту топологию для рабочих сред, поддерживающих до 110 000 MBAM клиентов.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-127">We recommended this topology for production environments that support up to 110,000 MBAM Clients.</span></span>

![MBAM. 4 топология развертывания компьютера.](images/mbam-4-computer.jpg)

<span data-ttu-id="1ec2c-129">В этой конфигурации функции MBAM устанавливаются в следующей конфигурации:</span><span class="sxs-lookup"><span data-stu-id="1ec2c-129">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="1ec2c-130">База данных восстановления, базы данных соответствия требованиям и проверки соответствия требованиям и аудита устанавливаются на сервере.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-130">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="1ec2c-131">Сервер администрирования и мониторинга установлен на сервере, настроенном в кластере серверов балансировки сетевой нагрузки (NLB).</span><span class="sxs-lookup"><span data-stu-id="1ec2c-131">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

3.  <span data-ttu-id="1ec2c-132">Шаблон групповой политики MBAM установлен на компьютере, способном изменять объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-132">MBAM Group Policy template is installed on a computer that is capable of modifying the Group Policy Objects.</span></span>

### <span data-ttu-id="1ec2c-133">Конфигурация с пятью компьютерами</span><span class="sxs-lookup"><span data-stu-id="1ec2c-133">Five-computer configuration</span></span>

<span data-ttu-id="1ec2c-134">На приведенной ниже схеме показана топология развертывания на пяти компьютерах для MBAM.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-134">The following diagram displays the five-computer deployment topology for MBAM.</span></span> <span data-ttu-id="1ec2c-135">Мы рекомендуем использовать эту топологию для рабочих сред, поддерживающих до 135 000 MBAM клиентов.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-135">We recommend this topology for production environments that support up to 135,000 MBAM Clients.</span></span>

![MBAM. 5 топология развертывания компьютера.](images/mbam-5-computer.jpg)

<span data-ttu-id="1ec2c-137">В этой конфигурации функции MBAM устанавливаются в следующей конфигурации:</span><span class="sxs-lookup"><span data-stu-id="1ec2c-137">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="1ec2c-138">База данных восстановления и оборудования установлены на сервере.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-138">Recovery and Hardware Database is installed on a server.</span></span>

2.  <span data-ttu-id="1ec2c-139">База данных соответствия требованиям и проверки соответствия и аудита устанавливаются на сервере.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-139">The Compliance and Audit Database and Compliance and Audit Reports are installed on a server.</span></span>

3.  <span data-ttu-id="1ec2c-140">Сервер администрирования и мониторинга установлен на сервере, настроенном в кластере серверов балансировки сетевой нагрузки (NLB).</span><span class="sxs-lookup"><span data-stu-id="1ec2c-140">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

4.  <span data-ttu-id="1ec2c-141">Шаблон групповой политики MBAM установлен на компьютере, способном изменять объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1ec2c-141">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects.</span></span>

[<span data-ttu-id="1ec2c-142">Установка и настройка MBAM на распределенных серверах</span><span class="sxs-lookup"><span data-stu-id="1ec2c-142">How to Install and Configure MBAM on Distributed Servers</span></span>](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[<span data-ttu-id="1ec2c-143">Настройка балансировки сетевой нагрузки для MBAM</span><span class="sxs-lookup"><span data-stu-id="1ec2c-143">How to Configure Network Load Balancing for MBAM</span></span>](how-to-configure-network-load-balancing-for-mbam.md)

## <span data-ttu-id="1ec2c-144">Другие ресурсы для развертывания функций сервера MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="1ec2c-144">Other resources for MBAM 1.0 Server features deployment</span></span>


[<span data-ttu-id="1ec2c-145">Развертывание MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1ec2c-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





