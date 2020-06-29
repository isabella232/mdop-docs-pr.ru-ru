---
title: Развертывание клиента MBAM 2.5
description: Развертывание клиента MBAM 2.5
author: dansimp
ms.assetid: 0a96a0ee-f280-49d9-a244-88f4147fe9fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 375af8966c8e66a58baec5065d065891187899fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826279"
---
# <span data-ttu-id="18ed2-103">Развертывание клиента MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="18ed2-103">Deploying the MBAM 2.5 Client</span></span>


<span data-ttu-id="18ed2-104">Клиентское программное обеспечение Microsoft BitLocker Administration и Monitoring (MBAM) позволяет администраторам принудительно применять и отслеживать шифрование диска BitLocker на компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="18ed2-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client software enables administrators to enforce and monitor BitLocker Drive Encryption on computers in the enterprise.</span></span> <span data-ttu-id="18ed2-105">Клиент BitLocker можно интегрировать в организацию, развертывая клиент с помощью электронной системы распространения программного обеспечения, например доменных служб Active Directory или напрямую шифруя клиентские компьютеры в рамках первоначального процесса обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="18ed2-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="18ed2-106">В зависимости от того, как вы развертываете клиентское программное обеспечение для администрирования Microsoft BitLocker и наблюдения за ним, вы можете включить шифрование диска BitLocker на компьютере в вашей организации до того, как пользователь получит компьютер или попозже настроить групповую политику и развернуть клиентское программное обеспечение MBAM с помощью корпоративной системы развертывания программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="18ed2-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client software, you can enable BitLocker Drive Encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="18ed2-107">Развертывание клиента MBAM на настольных компьютерах и ноутбуках</span><span class="sxs-lookup"><span data-stu-id="18ed2-107">Deploy the MBAM Client to desktop or laptop computers</span></span>


<span data-ttu-id="18ed2-108">После настройки параметров групповой политики вы можете использовать корпоративную систему развертывания программного обеспечения, например MicrosoftSystemCenter2012 ConfigurationManager или доменные службы Active Directory, для развертывания файлов установщика Windows MBAM на целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="18ed2-108">After configuring Group Policy settings, you can use an enterprise software deployment system product like MicrosoftSystemCenter2012 ConfigurationManager or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="18ed2-109">Вы можете использовать либо 32-разрядный, либо 64-разрядный MbamClientSetup.exe, либо файлы 32-bit или 64-bit MBAMClient.msi, которые предоставляются в клиентском программном обеспечении MBAM.</span><span class="sxs-lookup"><span data-stu-id="18ed2-109">You can use either the 32-bit or 64-bit MbamClientSetup.exe files or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM Client software.</span></span> <span data-ttu-id="18ed2-110">Дополнительные сведения о развертывании параметров групповой политики MBAM см. в разделе [Развертывание объектов групповой политики MBAM 2,5](deploying-mbam-25-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="18ed2-110">For more information about deploying MBAM Group Policy settings, see [Deploying MBAM 2.5 Group Policy Objects](deploying-mbam-25-group-policy-objects.md).</span></span>

<span data-ttu-id="18ed2-111">**Примечание**  Начиная с MBAM 2,5 с пакетом обновления 1 (SP1), отдельный MSI больше не входит в состав продукта MBAM.</span><span class="sxs-lookup"><span data-stu-id="18ed2-111">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="18ed2-112">Тем не менее, вы можете извлечь MSI из исполняемого файла (exe), который входит в состав продукта.</span><span class="sxs-lookup"><span data-stu-id="18ed2-112">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

 

[<span data-ttu-id="18ed2-113">Развертывание клиента MBAM на настольных компьютерах и ноутбуках</span><span class="sxs-lookup"><span data-stu-id="18ed2-113">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25.md)

## <span data-ttu-id="18ed2-114">Развертывание клиента MBAM в рамках развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="18ed2-114">Deploy the MBAM Client as part of a Windows deployment</span></span>


<span data-ttu-id="18ed2-115">В организациях, где компьютеры принимают и настраиваются централизованно, вы можете установить клиент MBAM для управления шифрованием диска BitLocker на каждом компьютере, прежде чем на него будут записываться пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="18ed2-115">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="18ed2-116">Преимущество этого процесса состоит в том, что каждый из компьютеров является совместимым с шифрованием диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="18ed2-116">The benefit of this process is that every computer is then BitLocker Drive Encryption-compliant.</span></span> <span data-ttu-id="18ed2-117">Этот метод не полагается на действия пользователя, так как администратор уже зашифровал компьютер.</span><span class="sxs-lookup"><span data-stu-id="18ed2-117">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="18ed2-118">Ключевым допущением для этого сценария является то, что политика Организации устанавливает корпоративный образ Windows до того, как компьютер будет доставлен пользователю.</span><span class="sxs-lookup"><span data-stu-id="18ed2-118">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="18ed2-119">Если параметрам групповой политики требуется ПИН-код, пользователи получат запрос на установку PIN-кода после того, как он получит эту политику.</span><span class="sxs-lookup"><span data-stu-id="18ed2-119">If the Group Policy settings has been configured to require a PIN, users are prompted to set a PIN after they receive the policy.</span></span>

[<span data-ttu-id="18ed2-120">Включение BitLocker с помощью MBAM в составе развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="18ed2-120">How to Enable BitLocker by Using MBAM as Part of a Windows Deployment</span></span>](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

## <span data-ttu-id="18ed2-121">Развертывание клиента MBAM с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="18ed2-121">How to deploy the MBAM Client by using a command line</span></span>


<span data-ttu-id="18ed2-122">В этом разделе объясняется, как установить клиент MBAM с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="18ed2-122">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="18ed2-123">Развертывание клиента MBAM с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="18ed2-123">How to Deploy the MBAM Client by Using a Command Line</span></span>](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

## <span data-ttu-id="18ed2-124">Другие ресурсы для развертывания клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="18ed2-124">Other resources for deploying the MBAM Client</span></span>


[<span data-ttu-id="18ed2-125">Развертывание MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="18ed2-125">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)



## <span data-ttu-id="18ed2-126">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="18ed2-126">Related topics</span></span>


[<span data-ttu-id="18ed2-127">Развертывание MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="18ed2-127">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="18ed2-128">Планирование для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="18ed2-128">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

 
## <span data-ttu-id="18ed2-129">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="18ed2-129">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="18ed2-130">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="18ed2-130">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="18ed2-131">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="18ed2-131">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





