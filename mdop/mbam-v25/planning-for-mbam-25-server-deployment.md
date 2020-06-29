---
title: Планирование развертывания сервера MBAM 2.5 Server
description: Планирование развертывания сервера MBAM 2.5 Server
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826212"
---
# <span data-ttu-id="3e788-103">Планирование развертывания сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="3e788-103">Planning for MBAM 2.5 Server Deployment</span></span>


<span data-ttu-id="3e788-104">В этом разделе описаны возможности, которые вы развертываете для изолированных топологий MBAM и топологии Configuration Manager, и перечислены заказы, в которых они должны развертываться.</span><span class="sxs-lookup"><span data-stu-id="3e788-104">This topic lists the features that you deploy for the MBAM Stand-alone and Configuration Manager topologies and lists the order in which you need to deploy them.</span></span> <span data-ttu-id="3e788-105">Рекомендуемая конфигурация для каждой топологии.</span><span class="sxs-lookup"><span data-stu-id="3e788-105">There is a recommended configuration for each topology.</span></span> <span data-ttu-id="3e788-106">Однако вы можете настроить базы данных и компоненты сервера MBAM в различных конфигурациях и на нескольких серверах, в зависимости от требований к масштабируемости.</span><span class="sxs-lookup"><span data-stu-id="3e788-106">However, you can configure MBAM server databases and features in different configurations and across multiple servers, depending on your scalability requirements.</span></span>

## <span data-ttu-id="3e788-107">Важные вопросы планирования для обеих топологий</span><span class="sxs-lookup"><span data-stu-id="3e788-107">Important planning considerations for both topologies</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3e788-108">Довод</span><span class="sxs-lookup"><span data-stu-id="3e788-108">Considerations</span></span></th>
<th align="left"><span data-ttu-id="3e788-109">Сведения или цель</span><span class="sxs-lookup"><span data-stu-id="3e788-109">Details or purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3e788-110">Прежде чем приступить к развертыванию, проверьте следующее:</span><span class="sxs-lookup"><span data-stu-id="3e788-110">Review the following before you start the deployment:</span></span></p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="3e788-111">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="3e788-111">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="3e788-112">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="3e788-112">MBAM 2.5 Supported Configurations</span></span></a></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="3e788-113">Каждая функция MBAM имеет определенные предварительные требования, которые должны быть выполнены перед началом установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="3e788-113">Each MBAM feature has specific prerequisites that must be met before you start the MBAM installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3e788-114">Ключи восстановления BitLocker в MBAM истекает после одного использования.</span><span class="sxs-lookup"><span data-stu-id="3e788-114">BitLocker recovery keys in MBAM expire after a single use.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e788-115">Это означает, что ключ восстановления был получен с помощью веб-сайта администрирования и мониторинга (также известного как служба поддержки), портала самообслуживания или с помощью <strong> </strong> командлета Windows PowerShell Get-MbamBitLockerRecoveryKey.</span><span class="sxs-lookup"><span data-stu-id="3e788-115">A single use means that the recovery key has been retrieved through the Administration and Monitoring Website (also known as Help Desk), Self-Service Portal, or by using the Get-<strong>MbamBitLockerRecoveryKey</strong> Windows PowerShell cmdlet.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3e788-116">Следите за именами компьютеров, на которых настраивается каждая из этих функций.</span><span class="sxs-lookup"><span data-stu-id="3e788-116">Keep track of the names of the computers on which you configure each feature.</span></span> <span data-ttu-id="3e788-117">Эти сведения будут использоваться в ходе настройки.</span><span class="sxs-lookup"><span data-stu-id="3e788-117">You will use this information throughout the configuration process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e788-118">Вы можете использовать <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"> Контрольный список развертывания MBAM 2,5 </a> для этой цели.</span><span class="sxs-lookup"><span data-stu-id="3e788-118">You may want to use the <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)">MBAM 2.5 Deployment Checklist</a> for this purpose.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3e788-119">Настройте только параметры групповой политики на узле MDOP MBAM (Управление BitLocker).</span><span class="sxs-lookup"><span data-stu-id="3e788-119">Configure only the Group Policy settings in the MDOP MBAM (BitLocker Management) node.</span></span> <span data-ttu-id="3e788-120">Не изменяйте параметры групповой политики в узле шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3e788-120">Do not change the Group Policy settings in the BitLocker Drive Encryption node.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e788-121">Если изменить параметры групповой политики в узле шифрования диска BitLocker, MBAM не будет работать.</span><span class="sxs-lookup"><span data-stu-id="3e788-121">If you change the Group Policy settings in the BitLocker Drive Encryption node, MBAM will not work.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a><span data-ttu-id="3e788-122">Планирование развертывания сервера MBAM — изолированная топология</span><span class="sxs-lookup"><span data-stu-id="3e788-122">Planning for MBAM Server deployment – Stand-alone topology</span></span>


<span data-ttu-id="3e788-123">Для изолированной топологии рекомендуется использовать конфигурацию из двух серверов для рабочих сред, несмотря на то, что могут использоваться конфигурации с тремя и четырьмя серверами.</span><span class="sxs-lookup"><span data-stu-id="3e788-123">For the Stand-alone topology, a two-server configuration is recommended for production environments, although configurations of three to four servers can be used.</span></span>

<span data-ttu-id="3e788-124">Инфраструктура сервера для изолированной топологии MBAM включает следующие функции, которые должны быть настроены в указанном порядке:</span><span class="sxs-lookup"><span data-stu-id="3e788-124">The Server infrastructure for the MBAM Stand-alone topology contains the following features, which must be configured in the order listed:</span></span>

1.  <span data-ttu-id="3e788-125">Базы данных (соответствие требованиям и база данных для проверки соответствия и базы данных восстановления)</span><span class="sxs-lookup"><span data-stu-id="3e788-125">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="3e788-126">Отчеты</span><span class="sxs-lookup"><span data-stu-id="3e788-126">Reports</span></span>

3.  <span data-ttu-id="3e788-127">Веб-приложения (и соответствующие им веб-службы)</span><span class="sxs-lookup"><span data-stu-id="3e788-127">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="3e788-128">Веб-сайт администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="3e788-128">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="3e788-129">Портал самообслуживания</span><span class="sxs-lookup"><span data-stu-id="3e788-129">Self-Service Portal</span></span>

<span data-ttu-id="3e788-130">Описание этих функций приведено в разделе [архитектура высокого уровня MBAM 2,5 с изолированной топологией](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span><span class="sxs-lookup"><span data-stu-id="3e788-130">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a><span data-ttu-id="3e788-131">Планирование развертывания сервера MBAM — топология Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="3e788-131">Planning for MBAM Server deployment – Configuration Manager topology</span></span>


<span data-ttu-id="3e788-132">Для топологии интеграции Configuration Manager для рабочих сред рекомендуется настроить конфигурацию с тремя серверами, но можно использовать настройки дополнительных серверов.</span><span class="sxs-lookup"><span data-stu-id="3e788-132">For the Configuration Manager Integration topology, a three-server configuration is recommended for production environments, although configurations of additional servers can be used.</span></span>

<span data-ttu-id="3e788-133">Серверная инфраструктура для топологии Configuration Manager MBAM включает следующие функции, которые необходимо настроить или выполнить в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="3e788-133">The Server infrastructure for the MBAM Configuration Manager topology contains the following features, which must be configured or performed in the order listed:</span></span>

1.  <span data-ttu-id="3e788-134">Базы данных (соответствие требованиям и база данных для проверки соответствия и базы данных восстановления)</span><span class="sxs-lookup"><span data-stu-id="3e788-134">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="3e788-135">Отчеты</span><span class="sxs-lookup"><span data-stu-id="3e788-135">Reports</span></span>

3.  <span data-ttu-id="3e788-136">Веб-приложения (и соответствующие им веб-службы)</span><span class="sxs-lookup"><span data-stu-id="3e788-136">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="3e788-137">Веб-сайт администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="3e788-137">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="3e788-138">Портал самообслуживания</span><span class="sxs-lookup"><span data-stu-id="3e788-138">Self-Service Portal</span></span>

4.  <span data-ttu-id="3e788-139">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="3e788-139">System Center Configuration Manager Integration</span></span>

<span data-ttu-id="3e788-140">Описание этих функций приведено в разделе [архитектура высокого уровня MBAM 2,5 с топологией интеграции Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="3e788-140">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="3e788-141">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3e788-141">Related topics</span></span>


[<span data-ttu-id="3e788-142">Планирование развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="3e788-142">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="3e788-143">Развертывание инфраструктуры сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="3e788-143">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)

 

## <span data-ttu-id="3e788-144">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="3e788-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="3e788-145">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="3e788-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="3e788-146">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="3e788-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





