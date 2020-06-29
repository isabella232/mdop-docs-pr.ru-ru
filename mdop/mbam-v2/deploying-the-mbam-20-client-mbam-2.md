---
title: Развертывание клиента MBAM 2.0
description: Развертывание клиента MBAM 2.0
author: dansimp
ms.assetid: 3dd584fe-2a54-40f0-9bab-13ea74040b01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa42c8ab3adc273f0e00ba56a59f487deba89c6f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823449"
---
# <span data-ttu-id="0f049-103">Развертывание клиента MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0f049-103">Deploying the MBAM 2.0 Client</span></span>


<span data-ttu-id="0f049-104">Клиент администрирования и мониторинга Microsoft BitLocker (MBAM) позволяет администраторам принудительно применять и отслеживать шифрование диска BitLocker на компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="0f049-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="0f049-105">Клиент BitLocker можно интегрировать в организацию, развертывая клиент с помощью электронной системы распространения программного обеспечения, например доменных служб Active Directory или напрямую шифруя клиентские компьютеры в рамках первоначального процесса обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="0f049-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="0f049-106">В зависимости от того, когда вы развертываете клиент администрирования и мониторинга Microsoft BitLocker, вы можете включить шифрование BitLocker на компьютере в вашей организации до того, как пользователь получит компьютер или попозже настроить групповую политику и развернуть клиентское программное обеспечение MBAM с помощью корпоративной системы развертывания программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="0f049-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="0f049-107">Развертывание клиента MBAM на настольных компьютерах и ноутбуках</span><span class="sxs-lookup"><span data-stu-id="0f049-107">Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="0f049-108">После настройки групповой политики вы можете использовать корпоративную систему развертывания программного обеспечения, например Microsoft System Center Configuration Manager 2012 или доменные службы Active Directory, для развертывания файлов установщика Windows на целевые компьютеры в клиенте MBAM.</span><span class="sxs-lookup"><span data-stu-id="0f049-108">After configuring Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="0f049-109">Вы можете развернуть клиент с помощью 32 или 64-разрядных MbamClientSetup.exe файлов либо 32-bit или 64-bit MBAMClient.msi файлов, которые предоставляются вместе с программным обеспечением MBAM.</span><span class="sxs-lookup"><span data-stu-id="0f049-109">You can deploy the client by using either the 32-bit or 64-bit MbamClientSetup.exe files, or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM software.</span></span> <span data-ttu-id="0f049-110">Дополнительные сведения о развертывании объектов групповой политики MBAM см. в разделе [развертывание MBAM 2,0 объектов групповой политики](deploying-mbam-20-group-policy-objects-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="0f049-110">For more information about deploying MBAM Group Policy Objects, see [Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md).</span></span>

[<span data-ttu-id="0f049-111">Развертывание клиента MBAM на настольных компьютерах и ноутбуках</span><span class="sxs-lookup"><span data-stu-id="0f049-111">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-2.md)

## <span data-ttu-id="0f049-112">Развертывание клиента MBAM в рамках развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="0f049-112">Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="0f049-113">В организациях, где компьютеры принимают и настраиваются централизованно, вы можете установить клиент MBAM для управления шифрованием BitLocker на каждом компьютере до того, как в него будут записываться пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="0f049-113">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="0f049-114">Преимущество этого процесса состоит в том, что все компьютеры будут соответствовать требованиям шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0f049-114">The benefit of this process is that every computer is then BitLocker encryption compliant.</span></span> <span data-ttu-id="0f049-115">Этот метод не полагается на действия пользователя, так как администратор уже зашифровал компьютер.</span><span class="sxs-lookup"><span data-stu-id="0f049-115">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="0f049-116">Ключевым допущением для этого сценария является то, что политика Организации устанавливает корпоративный образ Windows до того, как компьютер будет доставлен пользователю.</span><span class="sxs-lookup"><span data-stu-id="0f049-116">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="0f049-117">Если для групповой политики требуется ПИН-код, пользователи получат запрос на установку PIN-кода после того, как он получит групповую политику.</span><span class="sxs-lookup"><span data-stu-id="0f049-117">If the Group Policy has been configured to require a PIN, users are prompted to set a PIN after they receive the Group Policy.</span></span>

[<span data-ttu-id="0f049-118">Развертывание клиента MBAM в рамках развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="0f049-118">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-2.md)

## <span data-ttu-id="0f049-119">Использование командной строки для установки клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="0f049-119">How to Use a Command Line to Install the MBAM Client</span></span>


<span data-ttu-id="0f049-120">В этом разделе объясняется, как установить клиент MBAM с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="0f049-120">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="0f049-121">Использование командной строки для установки клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="0f049-121">How to Use a Command Line to Install the MBAM Client</span></span>](how-to-use-a-command-line-to-install-the-mbam-client.md)

## <span data-ttu-id="0f049-122">Другие ресурсы для развертывания клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="0f049-122">Other Resources for Deploying the MBAM Client</span></span>


<span data-ttu-id="0f049-123">[Развертывание MBAM 2,0](deploying-mbam-20-mbam-2.md)[планирование для развертывания клиента MBAM 2,0](planning-for-mbam-20-client-deployment-mbam-2.md)</span><span class="sxs-lookup"><span data-stu-id="0f049-123">[Deploying MBAM 2.0](deploying-mbam-20-mbam-2.md)[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)</span></span>

 

 





