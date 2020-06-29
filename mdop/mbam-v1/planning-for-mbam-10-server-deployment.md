---
title: Планирование развертывания сервера MBAM 1.0
description: Планирование развертывания сервера MBAM 1.0
author: dansimp
ms.assetid: 3cbef284-3092-4c42-9234-2826b18ddef1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 76ff9c444ce3f9c39161341610fb0cd9a763dc6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812429"
---
# <span data-ttu-id="84fce-103">Планирование развертывания сервера MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="84fce-103">Planning for MBAM 1.0 Server Deployment</span></span>


<span data-ttu-id="84fce-104">Серверная инфраструктура Microsoft BitLocker Administration and Monitoring (MBAM) зависит от набора функций сервера, которые можно установить на одном или нескольких компьютерах, основываясь на требованиях вашей организации.</span><span class="sxs-lookup"><span data-stu-id="84fce-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of your enterprise.</span></span>

## <span data-ttu-id="84fce-105">Планирование развертывания сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="84fce-105">Planning for MBAM Server deployment</span></span>


<span data-ttu-id="84fce-106">Ниже перечислены функции MBAM, представляющие инфраструктуру сервера для развертывания MBAM сервера.</span><span class="sxs-lookup"><span data-stu-id="84fce-106">The following MBAM features represent the server infrastructure for an MBAM server deployment:</span></span>

-   <span data-ttu-id="84fce-107">База данных восстановления и оборудования</span><span class="sxs-lookup"><span data-stu-id="84fce-107">Recovery and Hardware Database</span></span>

-   <span data-ttu-id="84fce-108">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="84fce-108">Compliance and Audit Database</span></span>

-   <span data-ttu-id="84fce-109">Отчеты о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="84fce-109">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="84fce-110">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="84fce-110">Administration and Monitoring Server</span></span>

<span data-ttu-id="84fce-111">Базы данных и компоненты сервера MBAM можно устанавливать в разных конфигурациях в зависимости от требований к масштабируемости.</span><span class="sxs-lookup"><span data-stu-id="84fce-111">MBAM server databases and features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="84fce-112">Все возможности сервера MBAM могут быть установлены на одном сервере или распределены между несколькими серверами.</span><span class="sxs-lookup"><span data-stu-id="84fce-112">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="84fce-113">Как правило, мы рекомендуем использовать конфигурацию с тремя или пятью серверами для рабочих сред, хотя конфигурации двух или четырех серверов также можно использовать в зависимости от потребностей вашего компьютера.</span><span class="sxs-lookup"><span data-stu-id="84fce-113">Generally, we recommend that you use a three-server or five-server configuration for production environments, although configurations of two or four servers can also be used, depending on your computing needs.</span></span>

<span data-ttu-id="84fce-114">**Примечание**  Дополнительные сведения о масштабируемости MBAM и рекомендуемой топологии развертывания можно найти в статье Руководство по масштабируемости MBAM и высокой доступности <https://go.microsoft.com/fwlink/p/?LinkId=258314> .</span><span class="sxs-lookup"><span data-stu-id="84fce-114">**Note** For more information about performance scalability of MBAM and recommended deployment topologies, see the MBAM Scalability and High-Availability Guide white paper at <https://go.microsoft.com/fwlink/p/?LinkId=258314>.</span></span>

 

<span data-ttu-id="84fce-115">Каждая функция MBAM имеет особые требования.</span><span class="sxs-lookup"><span data-stu-id="84fce-115">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="84fce-116">Полный список обязательных компонентов сервера и требования к оборудованию и программному обеспечению можно найти в разделе Требования к [развертыванию MBAM 1,0](mbam-10-deployment-prerequisites.md) и [поддерживаемые конфигурации MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="84fce-116">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="84fce-117">В дополнение к MBAM функциям, связанным с сервером, приложение настройки сервера включает шаблон групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="84fce-117">In addition to the server-related MBAM features, the server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="84fce-118">Этот шаблон можно установить на любом компьютере, на котором может выполняться консоль управления групповыми политиками (GPMC) или расширенное управление групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="84fce-118">This template can be installed on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

## <span data-ttu-id="84fce-119">Порядок развертывания функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="84fce-119">Order of deployment of MBAM Server Features</span></span>


<span data-ttu-id="84fce-120">При развертывании функций сервера MBAM установите компоненты в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="84fce-120">When you deploy the MBAM Server features, install the features in the following order:</span></span>

1.  <span data-ttu-id="84fce-121">База данных восстановления и оборудования</span><span class="sxs-lookup"><span data-stu-id="84fce-121">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="84fce-122">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="84fce-122">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="84fce-123">Аудит соответствия требованиям и отчеты</span><span class="sxs-lookup"><span data-stu-id="84fce-123">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="84fce-124">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="84fce-124">Administration and Monitoring Server</span></span>

5.  <span data-ttu-id="84fce-125">Шаблон политики</span><span class="sxs-lookup"><span data-stu-id="84fce-125">Policy Template</span></span>

<span data-ttu-id="84fce-126">**Примечание**  Следите за именами компьютеров, на которых устанавливаются все компоненты.</span><span class="sxs-lookup"><span data-stu-id="84fce-126">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="84fce-127">Эти данные будут использоваться во время установки.</span><span class="sxs-lookup"><span data-stu-id="84fce-127">You will use this information throughout the installation process.</span></span> <span data-ttu-id="84fce-128">Вы можете напечатать и использовать контрольный список развертывания, который поможет вам в процессе установки.</span><span class="sxs-lookup"><span data-stu-id="84fce-128">You can print and use a deployment checklist to assist you in the installation process.</span></span> <span data-ttu-id="84fce-129">Дополнительные сведения о контрольном списке развертывания MBAM можно найти в разделе [Контрольный список развертывания MBAM 1,0](mbam-10-deployment-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="84fce-129">For more information about the MBAM deployment checklist, see [MBAM 1.0 Deployment Checklist](mbam-10-deployment-checklist.md).</span></span>

 

## <span data-ttu-id="84fce-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="84fce-130">Related topics</span></span>


[<span data-ttu-id="84fce-131">Планирование развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="84fce-131">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="84fce-132">Развертывание инфраструктуры сервера MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="84fce-132">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





