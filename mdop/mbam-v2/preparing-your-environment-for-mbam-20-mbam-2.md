---
title: Подготовка среды для развертывания MBAM 2.0
description: Подготовка среды для развертывания MBAM 2.0
author: dansimp
ms.assetid: 5fb01da9-620e-4992-9e54-2ed3fb69e6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1be989112d456064db302952d50159d00b5597a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825609"
---
# <span data-ttu-id="57e85-103">Подготовка среды для развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="57e85-103">Preparing your Environment for MBAM 2.0</span></span>


<span data-ttu-id="57e85-104">Прежде чем приступить к установке Microsoft BitLocker Administration и Monitoring (MBAM), убедитесь, что для установки продукта выполнены необходимые условия.</span><span class="sxs-lookup"><span data-stu-id="57e85-104">Before beginning Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should make sure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="57e85-105">Если вы знаете, что предварительные условия загружаются заранее, вы можете эффективно развернуть продукт и включить его функции, чтобы он эффективно поддерживал бизнес-цели вашей организации.</span><span class="sxs-lookup"><span data-stu-id="57e85-105">When you know what the prerequisites are ahead of time, you can efficiently deploy the product and enable its features so that it most effectively supports your organization’s business objectives.</span></span>

<span data-ttu-id="57e85-106">Если вы развертываете администрирование и мониторинг Microsoft BitLocker с помощью Microsoft System Center Configuration Manager 2007 или MicrosoftSystemCenter2012 ConfigurationManager, ознакомьтесь с [Разпланированием для развертывания MBAM с помощью Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="57e85-106">If you are deploying Microsoft BitLocker Administration and Monitoring with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

## <span data-ttu-id="57e85-107">Проверка требований к развертыванию MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="57e85-107">Review MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="57e85-108">Клиент MBAM и каждая из функций сервера MBAM имеют определенные предварительные требования, которые должны быть выполнены, прежде чем их можно будет успешно установить.</span><span class="sxs-lookup"><span data-stu-id="57e85-108">The MBAM Client and each of the MBAM Server features have specific prerequisites that must be met before they can be successfully installed.</span></span>

<span data-ttu-id="57e85-109">Чтобы убедиться в успешной установке MBAM клиентов и функций сервера MBAM, убедитесь в том, что компьютеры, указанные в MBAM клиентском компьютере или MBAM компонентах сервера, правильно подготовлены для установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="57e85-109">To ensure successful installation of MBAM Clients and MBAM Server features, ensure that computers specified for MBAM Client or MBAM Server feature installation are properly prepared for MBAM Setup.</span></span>

<span data-ttu-id="57e85-110">**Примечание**  Программа установки MBAM проверяет, выполнены ли все необходимые условия перед началом установки.</span><span class="sxs-lookup"><span data-stu-id="57e85-110">**Note** MBAM Setup checks that all prerequisites are met before installation starts.</span></span> <span data-ttu-id="57e85-111">Если все требования не выполнены, программа установки завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="57e85-111">If all prerequisites are not met, Setup will fail.</span></span>

 

[<span data-ttu-id="57e85-112">Необходимые условия для развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="57e85-112">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

## <span data-ttu-id="57e85-113">Планирование требований к групповой политике для MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="57e85-113">Plan for MBAM 2.0 Group Policy Requirements</span></span>


<span data-ttu-id="57e85-114">Перед тем как MBAM сможет управлять клиентами в масштабах предприятия, необходимо задать групповую политику для требований к шифрованию вашей среды.</span><span class="sxs-lookup"><span data-stu-id="57e85-114">Before MBAM can manage clients in the enterprise, you must define Group Policy for the encryption requirements of your environment.</span></span>

<span data-ttu-id="57e85-115">**Важно!**  MBAM не будет работать с политиками для автономного шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="57e85-115">**Important** MBAM will not work with policies for stand-alone BitLocker drive encryption.</span></span> <span data-ttu-id="57e85-116">Параметры групповой политики должны быть определены для MBAM, а шифрование BitLocker и принудительное выполнение будут завершаться сбоем.</span><span class="sxs-lookup"><span data-stu-id="57e85-116">Group Policy settings must be defined for MBAM, or BitLocker encryption and enforcement will fail.</span></span>

 

[<span data-ttu-id="57e85-117">Планирование требований групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="57e85-117">Planning for MBAM 2.0 Group Policy Requirements</span></span>](planning-for-mbam-20-group-policy-requirements-mbam-2.md)

## <span data-ttu-id="57e85-118">Планирование ролей администратора для MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="57e85-118">Plan for MBAM 2.0 Administrator Roles</span></span>


<span data-ttu-id="57e85-119">Роли администратора MBAM управляются локальными группами, созданными при настройке MBAM при установке сервера администрирования и мониторинга BitLocker, функции отчетов о соответствии и аудита, а также базы данных состояния соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="57e85-119">MBAM administrator roles are managed by local groups that are created by MBAM Setup when you install the BitLocker Administration and Monitoring Server, the Compliance and Audit Reports feature, and the Compliance and Audit Status Database.</span></span>

<span data-ttu-id="57e85-120">Вы можете лучше управлять членством в ролях администрирования и мониторинга Microsoft BitLocker, создавая группы безопасности в ActiveDirectoryDomainServices, добавляя в них учетные записи администраторов и добавляя эти группы безопасности в администрирование BitLocker и отслеживая локальные группы.</span><span class="sxs-lookup"><span data-stu-id="57e85-120">The membership of Microsoft BitLocker Administration and Monitoring roles can best be managed by creating security groups in ActiveDirectoryDomainServices, adding the appropriate administrator accounts to those groups, and then adding those security groups to the BitLocker Administration and Monitoring local groups.</span></span> <span data-ttu-id="57e85-121">Дополнительные сведения [можно найти в разделе Управление ролями администратора MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="57e85-121">For more information, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

## <span data-ttu-id="57e85-122">Другие ресурсы для планирования MBAM</span><span class="sxs-lookup"><span data-stu-id="57e85-122">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="57e85-123">Планирование для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="57e85-123">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="57e85-124">Поддерживаемые конфигурации MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="57e85-124">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

 

 





