---
title: Развертывание клиента MBAM 1.0
description: Развертывание клиента MBAM 1.0
author: dansimp
ms.assetid: f7ca233f-5035-4ff9-ab3a-f2453b4929d1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dee8c2f4a9b398c9f0797ada35e4c36610c755b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822902"
---
# <span data-ttu-id="57246-103">Развертывание клиента MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="57246-103">Deploying the MBAM 1.0 Client</span></span>


<span data-ttu-id="57246-104">Клиент администрирования и мониторинга Microsoft BitLocker (MBAM) позволяет администраторам принудительно применять и отслеживать шифрование диска BitLocker на компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="57246-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="57246-105">Клиент BitLocker можно интегрировать в организацию, развертывая клиент с помощью таких средств, как доменные службы Active Directory, или напрямую зашифровывать клиентские компьютеры как часть исходного процесса обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="57246-105">The BitLocker client can be integrated into an organization by deploying the client through tools like Active Directory Domain Services or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="57246-106">В зависимости от того, когда вы развертываете клиент MBAM, вы можете включить шифрование BitLocker на компьютере в вашей организации как до, так и после того, как пользователь получит компьютер.</span><span class="sxs-lookup"><span data-stu-id="57246-106">Depending on when you deploy the MBAM Client, you can enable BitLocker encryption on a computer in your organization either before or after the end user receives the computer.</span></span> <span data-ttu-id="57246-107">Чтобы управлять этим временем, вы можете настроить групповую политику и развернуть клиентское программное обеспечение MBAM с помощью корпоративной системы развертывания программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="57246-107">To control this timing, you configure Group Policy and deploy the MBAM Client software by using an enterprise software deployment system.</span></span>

<span data-ttu-id="57246-108">Вы можете использовать любой из этих методов в своей организации.</span><span class="sxs-lookup"><span data-stu-id="57246-108">You can use either or both of these methods in your organization.</span></span> <span data-ttu-id="57246-109">Если вы используете оба способа, вы можете улучшить соответствие требованиям, создавать отчеты и поддерживать восстановление ключей.</span><span class="sxs-lookup"><span data-stu-id="57246-109">If you use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

## <span data-ttu-id="57246-110">Развертывание клиента MBAM на настольных компьютерах и ноутбуках</span><span class="sxs-lookup"><span data-stu-id="57246-110">Deploy the MBAM Client to desktop or laptop computers</span></span>


<span data-ttu-id="57246-111">После того как вы настроили групповую политику, вы можете развернуть файлы установщика Windows для установки клиента MBAM на целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="57246-111">After you have configured Group Policy, you can deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="57246-112">Это можно сделать с помощью корпоративной системы развертывания программного обеспечения, например Microsoft System Center 2012 Configuration Manager или доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="57246-112">You can do this by use of an enterprise software deployment system product like Microsoft System Center 2012 Configuration Manager or Active Directory Domain Services.</span></span> <span data-ttu-id="57246-113">Два доступных установочных файла MBAM Windows: MBAMClient-64bit.msi и MBAMClient-32bit.msi.</span><span class="sxs-lookup"><span data-stu-id="57246-113">The two available MBAM Client installation Windows Installer files are MBAMClient-64bit.msi and MBAMClient-32bit.msi.</span></span> <span data-ttu-id="57246-114">Эти файлы предоставляются вместе с программным обеспечением MBAM.</span><span class="sxs-lookup"><span data-stu-id="57246-114">These files are provided with the MBAM software.</span></span> <span data-ttu-id="57246-115">Дополнительные сведения о том, как развертывать объекты групповой политики MBAM, можно найти в разделе [развертывание MBAM 1,0 объектов групповой политики](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="57246-115">For more information about how to deploy MBAM Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

[<span data-ttu-id="57246-116">Развертывание клиента MBAM на настольных компьютерах и ноутбуках</span><span class="sxs-lookup"><span data-stu-id="57246-116">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-1.md)

## <span data-ttu-id="57246-117">Развертывание клиента MBAM в рамках развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="57246-117">Deploy the MBAM Client as part of a Windows deployment</span></span>


<span data-ttu-id="57246-118">В некоторых организациях новые компьютеры принимаются и настраиваются централизованно.</span><span class="sxs-lookup"><span data-stu-id="57246-118">In some organizations, new computers are received and configured centrally.</span></span> <span data-ttu-id="57246-119">Эта ситуация позволяет администраторам устанавливать клиент MBAM для управления шифрованием BitLocker на каждом компьютере до того, как на компьютере будут записываться данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="57246-119">This situation enables administrators to install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to the computer.</span></span> <span data-ttu-id="57246-120">Этот подход позволяет удостовериться в том, что компьютеры должным образом зашифрованы, так как администратор выполняет действие без использования действий конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="57246-120">This approach helps to ensure that computers are properly encrypted because the administrator performs the action without reliance on end-user action.</span></span> <span data-ttu-id="57246-121">Ключевым допущением для этого сценария является то, что политика Организации устанавливает корпоративный образ Windows до того, как компьютер будет доставлен пользователю.</span><span class="sxs-lookup"><span data-stu-id="57246-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

[<span data-ttu-id="57246-122">Развертывание клиента MBAM в рамках развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="57246-122">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-1.md)

## <span data-ttu-id="57246-123">Другие ресурсы для развертывания клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="57246-123">Other resources for deploying the MBAM Client</span></span>


[<span data-ttu-id="57246-124">Развертывание MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="57246-124">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

[<span data-ttu-id="57246-125">Планирование развертывания клиента MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="57246-125">Planning for MBAM 1.0 Client Deployment</span></span>](planning-for-mbam-10-client-deployment.md)

 

 





