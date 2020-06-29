---
title: Планирование развертывания сервера MBAM 2.0 Server
description: Планирование развертывания сервера MBAM 2.0 Server
author: dansimp
ms.assetid: b57f1a42-134f-4997-8697-7fbed08e2fc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57e6510556522dce029c958172bd89a361e06b83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812613"
---
# <span data-ttu-id="74a1b-103">Планирование развертывания сервера MBAM 2.0 Server</span><span class="sxs-lookup"><span data-stu-id="74a1b-103">Planning for MBAM 2.0 Server Deployment</span></span>


<span data-ttu-id="74a1b-104">Серверная инфраструктура администрирования и мониторинга Microsoft BitLocker (MBAM) зависит от набора функций сервера, которые можно установить на одном или нескольких компьютерах, основываясь на требованиях предприятия.</span><span class="sxs-lookup"><span data-stu-id="74a1b-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="74a1b-105">Если вы устанавливаете администрирование и мониторинг Microsoft BitLocker с топологией Configuration Manager, ознакомьтесь с [Разпланированием развертывания MBAM с помощью Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="74a1b-105">If you are installing Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="74a1b-106">**Примечание**  Установка администрирования и мониторинга Microsoft BitLocker на одном сервере рекомендуется только для тестовых сред.</span><span class="sxs-lookup"><span data-stu-id="74a1b-106">**Note** Installations of Microsoft BitLocker Administration and Monitoring on a single server are recommended only for test environments.</span></span>

 

## <span data-ttu-id="74a1b-107">Планирование развертывания сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="74a1b-107">Planning for MBAM Server Deployment</span></span>


<span data-ttu-id="74a1b-108">Инфраструктура для развертывания сервера MBAM включает следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="74a1b-108">The infrastructure for an MBAM Server deployment includes the following features:</span></span>

-   <span data-ttu-id="74a1b-109">База данных восстановления</span><span class="sxs-lookup"><span data-stu-id="74a1b-109">Recovery Database</span></span>

-   <span data-ttu-id="74a1b-110">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="74a1b-110">Compliance and Audit Database</span></span>

-   <span data-ttu-id="74a1b-111">Отчеты о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="74a1b-111">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="74a1b-112">Портал самообслуживания</span><span class="sxs-lookup"><span data-stu-id="74a1b-112">Self-Service Portal</span></span>

-   <span data-ttu-id="74a1b-113">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="74a1b-113">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="74a1b-114">Шаблон групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="74a1b-114">MBAM Group Policy Template</span></span>

<span data-ttu-id="74a1b-115">Базы данных и компоненты сервера MBAM можно устанавливать в разных конфигурациях в зависимости от требований к масштабируемости.</span><span class="sxs-lookup"><span data-stu-id="74a1b-115">MBAM Server databases and features can be installed in different configurations, depending on your scalability requirements.</span></span> <span data-ttu-id="74a1b-116">Все возможности сервера MBAM могут быть установлены на одном сервере или распределены между несколькими серверами.</span><span class="sxs-lookup"><span data-stu-id="74a1b-116">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="74a1b-117">Мы рекомендуем использовать конфигурацию из двух серверов для рабочих сред, несмотря на то, что в зависимости от требований к компьютерам можно использовать конфигурации двух и четырех серверов.</span><span class="sxs-lookup"><span data-stu-id="74a1b-117">We recommend that you use a two-server configuration for production environments, although configurations of two to four servers can also be used, depending on your computing requirements.</span></span>

<span data-ttu-id="74a1b-118">Каждая функция MBAM имеет особые требования.</span><span class="sxs-lookup"><span data-stu-id="74a1b-118">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="74a1b-119">Полный список обязательных компонентов сервера и требования к оборудованию и программному обеспечению можно найти в разделе Требования к [развертыванию MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) и [поддерживаемые конфигурации MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="74a1b-119">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

<span data-ttu-id="74a1b-120">В дополнение к MBAM функциям, связанным с сервером, приложение настройки сервера включает шаблон групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="74a1b-120">In addition to the server-related MBAM features, the Server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="74a1b-121">Шаблон включает параметры объекта групповой политики (GPO), которые вы настраиваете для управления шифрованием диска BitLocker в корпоративной среде.</span><span class="sxs-lookup"><span data-stu-id="74a1b-121">The template contains Group Policy Object (GPO) settings that you configure to manage BitLocker Drive Encryption in the enterprise.</span></span> <span data-ttu-id="74a1b-122">Этот шаблон можно установить на любом компьютере, на котором может выполняться консоль управления групповыми политиками (GPMC) или расширенное управление групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="74a1b-122">You can install this template on any computer that can run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="74a1b-123">Если вы планируете развертывание сервера MBAM, рассматривайте ключи восстановления BitLocker в MBAM предназначены только для единственного использования, после которого истечет срок действия ключей восстановления.</span><span class="sxs-lookup"><span data-stu-id="74a1b-123">As you plan the MBAM Server deployment, consider that BitLocker recovery keys in MBAM are intended for single use only, after which recovery keys expire.</span></span> <span data-ttu-id="74a1b-124">Для того чтобы ключи могли быть просрочены после использования, их необходимо получить на портале службы поддержки или портале самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="74a1b-124">In order for the keys to expire after use, they must be retrieved through the Help Desk Portal or the Self-Service Portal.</span></span>

## <span data-ttu-id="74a1b-125">Порядок развертывания функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="74a1b-125">Order of Deployment of MBAM Server Features</span></span>


<span data-ttu-id="74a1b-126">Для развертывания функций MBAM на нескольких серверах необходимо установить компоненты в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="74a1b-126">To deploy MBAM features on multiple servers, you have to install the features in the following order:</span></span>

1.  <span data-ttu-id="74a1b-127">База данных восстановления</span><span class="sxs-lookup"><span data-stu-id="74a1b-127">Recovery Database</span></span>

2.  <span data-ttu-id="74a1b-128">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="74a1b-128">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="74a1b-129">Аудит соответствия требованиям и отчеты</span><span class="sxs-lookup"><span data-stu-id="74a1b-129">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="74a1b-130">Портал самообслуживания</span><span class="sxs-lookup"><span data-stu-id="74a1b-130">Self-Service Portal</span></span>

5.  <span data-ttu-id="74a1b-131">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="74a1b-131">Administration and Monitoring Server</span></span>

6.  <span data-ttu-id="74a1b-132">Шаблон групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="74a1b-132">MBAM Group Policy Template</span></span>

<span data-ttu-id="74a1b-133">**Примечание**  Следите за именами компьютеров, на которых устанавливаются все компоненты.</span><span class="sxs-lookup"><span data-stu-id="74a1b-133">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="74a1b-134">Вы должны использовать эти сведения во время установки.</span><span class="sxs-lookup"><span data-stu-id="74a1b-134">You have to use this information throughout the installation process.</span></span> <span data-ttu-id="74a1b-135">Вы можете напечатать и использовать контрольный список развертывания, который поможет вам выполнить эти усилия.</span><span class="sxs-lookup"><span data-stu-id="74a1b-135">You can print and use a deployment checklist to assist in this effort.</span></span> <span data-ttu-id="74a1b-136">Дополнительные сведения о контрольном списке развертывания MBAM можно найти в разделе [Контрольный список развертывания MBAM 2,0](mbam-20-deployment-checklist-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="74a1b-136">For more information about the MBAM Deployment Checklist, see [MBAM 2.0 Deployment Checklist](mbam-20-deployment-checklist-mbam-2.md).</span></span>

 

## <span data-ttu-id="74a1b-137">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="74a1b-137">Related topics</span></span>


[<span data-ttu-id="74a1b-138">Планирование развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="74a1b-138">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="74a1b-139">Развертывание инфраструктуры сервера MBAM 2.0 Server</span><span class="sxs-lookup"><span data-stu-id="74a1b-139">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





