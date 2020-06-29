---
title: Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций
description: Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812565"
---
# <span data-ttu-id="13f66-103">Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="13f66-103">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="13f66-104">Если вы устанавливаете администрирование и мониторинг Microsoft BitLocker (MBAM) 2,5 с помощью функции интеграции System Center Configuration Manager, необходимо выполнить предварительные требования, описанные в этой статье, в дополнение к [требованиям для топологии интеграции с отдельными службами и топологией Configuration Manager для MBAM 2,5 Server](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="13f66-104">If you are installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 by using the System Center Configuration Manager Integration feature, you must complete the prerequisites described in this topic, in addition to those in [MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md).</span></span> <span data-ttu-id="13f66-105">Кроме того, необходимо создать или изменить файлы. mof, необходимые для топологии интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="13f66-105">You must also create or modify .mof files that are needed for the Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="13f66-106">Необходимые условия для компонента интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="13f66-106">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="13f66-107">Если вы настраиваете MBAM с помощью топологии интеграции System Center Configuration Manager, необходимо выполнить дополнительные требования, необходимые для Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="13f66-107">If you are configuring MBAM with the System Center Configuration Manager Integration topology, you must complete additional prerequisites that are required for Configuration Manager.</span></span>

[<span data-ttu-id="13f66-108">Необходимые условия для компонента интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="13f66-108">Prerequisites for the Configuration Manager Integration Feature</span></span>](prerequisites-for-the-configuration-manager-integration-feature.md)

## <span data-ttu-id="13f66-109">Изменение файла Configuration. mof</span><span class="sxs-lookup"><span data-stu-id="13f66-109">Edit the Configuration.mof file</span></span>


<span data-ttu-id="13f66-110">Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker с помощью отчетов Configuration Manager MBAM, необходимо изменить файл Configuration. mof для SystemCenter2012 ConfigurationManager и Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="13f66-110">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager Reports, you have to edit the Configuration.mof file for SystemCenter2012 ConfigurationManager and Microsoft System Center Configuration Manager 2007.</span></span>

[<span data-ttu-id="13f66-111">Изменение файла Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="13f66-111">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="13f66-112">Создание и изменение файла SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="13f66-112">Create or edit the Sms\_def.mof file</span></span>


<span data-ttu-id="13f66-113">Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker в отчетах Configuration Manager MBAM, необходимо создать или изменить файл SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="13f66-113">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager Reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="13f66-114">Если вы используете SystemCenter2012 ConfigurationManager, необходимо создать файл.</span><span class="sxs-lookup"><span data-stu-id="13f66-114">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="13f66-115">В Configuration Manager 2007 файл уже существует, поэтому вы должны изменить существующий файл, но не перезаписать его.</span><span class="sxs-lookup"><span data-stu-id="13f66-115">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span>

[<span data-ttu-id="13f66-116">Создание и изменение файла SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="13f66-116">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file-mbam-25.md)


## <span data-ttu-id="13f66-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="13f66-117">Related topics</span></span>


[<span data-ttu-id="13f66-118">Подготовка среды для развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13f66-118">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="13f66-119">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13f66-119">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

[<span data-ttu-id="13f66-120">Планирование развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13f66-120">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="13f66-121">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="13f66-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="13f66-122">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="13f66-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="13f66-123">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="13f66-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




