---
title: Подготовка среды для развертывания MBAM 1.0
description: Подготовка среды для развертывания MBAM 1.0
author: dansimp
ms.assetid: 915f7c3c-70ad-4a90-a434-73e7fba97ecb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a2de4e825d5c89aeabcf57d78dc856bacb03e11
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823192"
---
# <span data-ttu-id="a875e-103">Подготовка среды для развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a875e-103">Preparing your Environment for MBAM 1.0</span></span>


<span data-ttu-id="a875e-104">Прежде чем приступить к установке Microsoft BitLocker Administration и Monitoring (MBAM), убедитесь в том, что вы удовлетворены необходимыми требованиями для установки продукта.</span><span class="sxs-lookup"><span data-stu-id="a875e-104">Before you begin the Microsoft BitLocker Administration and Monitoring (MBAM) Setup, make sure that you have met the necessary prerequisites to install the product.</span></span> <span data-ttu-id="a875e-105">Если вы заранее знаете предварительные требования, вы можете эффективно развернуть продукт и включить его функции, которые могут более эффективно поддерживать бизнес-цели вашей организации.</span><span class="sxs-lookup"><span data-stu-id="a875e-105">If you know the prerequisites in advance, you can efficiently deploy the product and enable its features, which can support the business objectives of your organization more effectively.</span></span>

## <span data-ttu-id="a875e-106">Проверка требований к развертыванию MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="a875e-106">Review MBAM 1.0 deployment prerequisites</span></span>


<span data-ttu-id="a875e-107">Клиент MBAM и каждая из функций сервера MBAM имеют определенные предварительные требования, которые должны быть выполнены, прежде чем их можно будет успешно установить.</span><span class="sxs-lookup"><span data-stu-id="a875e-107">The MBAM Client and each of the MBAM Server features have specific prerequisites that must be met before they can be successfully installed.</span></span>

<span data-ttu-id="a875e-108">Чтобы убедиться в успешной установке MBAM клиентов и функций сервера MBAM, необходимо убедиться в том, что компьютеры, указанные в MBAM клиентском компьютере или MBAM компонентах сервера, правильно подготавливаются для установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="a875e-108">To ensure successful installation of MBAM Clients and MBAM Server features, you should plan to ensure that computers specified for MBAM Client or MBAM Server feature installation are properly prepared for MBAM Setup.</span></span>

<span data-ttu-id="a875e-109">**Примечание**  Программа установки MBAM проверяет, выполнены ли все необходимые условия перед началом установки.</span><span class="sxs-lookup"><span data-stu-id="a875e-109">**Note** MBAM Setup verifies if all prerequisites are met before installation starts.</span></span> <span data-ttu-id="a875e-110">Если это не так, программа установки завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="a875e-110">If they are not met, Setup will fail.</span></span>

 

[<span data-ttu-id="a875e-111">Необходимые компоненты развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a875e-111">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)

## <span data-ttu-id="a875e-112">Планирование требований к групповой политике для MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="a875e-112">Plan for MBAM 1.0 Group Policy requirements</span></span>


<span data-ttu-id="a875e-113">Перед тем как MBAM сможет управлять клиентами в масштабах предприятия, необходимо задать групповую политику для требований к шифрованию вашей среды.</span><span class="sxs-lookup"><span data-stu-id="a875e-113">Before MBAM can manage clients in the enterprise, you must define the Group Policy for the encryption requirements of your environment.</span></span>

<span data-ttu-id="a875e-114">**Важно!**  MBAM не будет работать с политиками для автономного шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a875e-114">**Important** MBAM will not work with policies for stand-alone BitLocker drive encryption.</span></span> <span data-ttu-id="a875e-115">Групповая политика должна быть определена для MBAM; в противном случае шифрование и принудительное использование BitLocker завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="a875e-115">Group Policy must be defined for MBAM; otherwise, the BitLocker encryption and enforcement will fail.</span></span>

 

[<span data-ttu-id="a875e-116">Планирование требований групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a875e-116">Planning for MBAM 1.0 Group Policy Requirements</span></span>](planning-for-mbam-10-group-policy-requirements.md)

## <span data-ttu-id="a875e-117">Планирование ролей администратора для MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="a875e-117">Plan for MBAM 1.0 administrator roles</span></span>


<span data-ttu-id="a875e-118">Роли администратора MBAM управляются локальными группами, созданными при установке MBAM, когда устанавливаются следующие компоненты: Сервер администрирования и мониторинга системы BitLocker, функция отчетов о соответствии и аудите, а также база данных состояния соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="a875e-118">MBAM administrator roles are managed by local groups that are created by MBAM Setup when you install the following: BitLocker Administration and Monitoring Server, the Compliance and Audit Reports feature, and the Compliance and Audit Status Database.</span></span>

<span data-ttu-id="a875e-119">Управлять членством в ролях MBAM более эффективно при создании групп безопасности в ActiveDirectoryDomainServices, добавлять в них соответствующие учетные записи администратора, а затем добавлять эти группы безопасности в локальные группы MBAM.</span><span class="sxs-lookup"><span data-stu-id="a875e-119">The membership of MBAM roles can be managed more effectively if you create security groups in ActiveDirectoryDomainServices, add the appropriate administrator accounts to those groups, and then add those security groups to the MBAM local groups.</span></span> <span data-ttu-id="a875e-120">Дополнительные сведения [можно найти в разделе Управление ролями администратора MBAM](how-to-manage-mbam-administrator-roles-mbam-1.md).</span><span class="sxs-lookup"><span data-stu-id="a875e-120">For more information, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md).</span></span>

[<span data-ttu-id="a875e-121">Планирование ролей администратора MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a875e-121">Planning for MBAM 1.0 Administrator Roles</span></span>](planning-for-mbam-10-administrator-roles.md)

## <span data-ttu-id="a875e-122">Другие ресурсы для планирования MBAM</span><span class="sxs-lookup"><span data-stu-id="a875e-122">Other resources for MBAM planning</span></span>


[<span data-ttu-id="a875e-123">Планирование для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a875e-123">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

 

 





