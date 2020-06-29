---
title: Планирование развертывания клиента MBAM 1.0
description: Планирование развертывания клиента MBAM 1.0
author: dansimp
ms.assetid: 3af2e7f3-134b-4ab9-9847-b07474ca6ac3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d58d6420febd2da9ee9cd4074fc8b5870285b0b4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825879"
---
# <span data-ttu-id="e1b6f-103">Планирование развертывания клиента MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e1b6f-103">Planning for MBAM 1.0 Client Deployment</span></span>


<span data-ttu-id="e1b6f-104">В зависимости от того, когда вы развертываете клиент администрирования и мониторинга Microsoft BitLocker (MBAM), вы можете включить шифрование BitLocker на компьютере в вашей организации до того, как пользователь получит компьютер или затем.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="e1b6f-105">Чтобы включить шифрование BitLocker после получения конечным пользователем компьютера, настройте групповую политику.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-105">To enable BitLocker encryption after the end user receives the computer, configure Group Policy.</span></span> <span data-ttu-id="e1b6f-106">Чтобы включить шифрование BitLocker до того, как пользователь получит компьютер, разверните клиентское программное обеспечение MBAM с помощью корпоративной системы развертывания программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-106">To enable BitLocker encryption before the end user receives the computer, deploy the MBAM Client software by using an enterprise software deployment system.</span></span>

<span data-ttu-id="e1b6f-107">Вы можете использовать один из этих методов в своей организации.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-107">You can use one or both methods in your organization.</span></span> <span data-ttu-id="e1b6f-108">Если вы используете оба способа, вы можете улучшить соответствие требованиям, создавать отчеты и поддерживать восстановление ключей.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-108">If you use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

<span data-ttu-id="e1b6f-109">**Примечание**  Сведения о требованиях к системе клиента MBAM можно найти в разделе [Поддерживаемые конфигурации MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="e1b6f-109">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="e1b6f-110">Развертывание клиента MBAM для включения шифрования BitLocker после распространения компьютера для конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="e1b6f-110">Deploying the MBAM Client to enable BitLocker encryption after computer distribution to end users</span></span>


<span data-ttu-id="e1b6f-111">После того как вы настроили групповую политику, вы можете развернуть файлы установщика Windows на целевые компьютеры на компьютере с помощью системы развертывания корпоративного программного обеспечения, например Microsoft System Center Configuration Manager 2012 или доменных служб Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-111">After you configure the Group Policy, you can use an enterprise software deployment system product, such as Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services, to deploy the MBAM Client installation Windows Installer files to the target computers.</span></span> <span data-ttu-id="e1b6f-112">Два установочных файла клиента MBAM: MBAMClient-64bit.msi и MBAMClient-32bit.msi, которые предоставляются вместе с программным обеспечением MBAM.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-112">The two MBAM Client installation Windows Installer files are MBAMClient-64bit.msi and MBAMClient-32bit.msi, which are provided with the MBAM software.</span></span> <span data-ttu-id="e1b6f-113">Дополнительные сведения о том, как развертывать объекты групповой политики MBAM, можно найти в разделе [развертывание MBAM 1,0 объектов групповой политики](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e1b6f-113">For more information about how to deploy MBAM Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

<span data-ttu-id="e1b6f-114">При развертывании клиента MBAM после распространения компьютеров конечным пользователям, конечные пользователи будут получать запрос на шифрование компьютеров.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-114">When you deploy the MBAM Client, after you distribute the computers to end users, the end users are prompted to encrypt their computers.</span></span> <span data-ttu-id="e1b6f-115">Это позволит MBAM собрать данные, добавить PIN-код и пароль, а затем начать процесс шифрования.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-115">This lets MBAM collect the data, to include the PIN and password, and then begin the encryption process.</span></span>

<span data-ttu-id="e1b6f-116">**Примечание**  При использовании этого подхода пользователи получают запрос на активацию и инициализацию микросхемы доверенного платформенного модуля (TPM), если он еще не активирован.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-116">**Note** In this approach, users are prompted to activate and initialize the Trusted Platform Module (TPM) chip, if it has not been previously activated.</span></span>

 

## <span data-ttu-id="e1b6f-117">Использование клиента MBAM для включения шифрования BitLocker перед распространением компьютера для конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="e1b6f-117">Using the MBAM Client to enable BitLocker encryption before computer distribution to end users</span></span>


<span data-ttu-id="e1b6f-118">В организациях, где компьютеры принимают и настраиваются централизованно, вы можете установить клиент MBAM для управления шифрованием BitLocker на каждом компьютере, прежде чем на него будут записываться пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-118">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written on it.</span></span> <span data-ttu-id="e1b6f-119">Преимущество этого процесса состоит в том, что все компьютеры будут соответствовать шифрованию BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-119">The benefit of this process is that every computer will then be compliant with the BitLocker encryption.</span></span> <span data-ttu-id="e1b6f-120">Этот метод не полагается на действия пользователя, так как администратор уже зашифровал компьютер.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="e1b6f-121">Ключевым допущением для этого сценария является то, что политика Организации устанавливает корпоративный образ Windows до того, как компьютер будет доставлен пользователю.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="e1b6f-122">Если в вашей организации требуется использовать доверенный платформенный модуль для шифрования компьютеров, администратор должен зашифровать том операционной системы компьютера с помощью предохранителя доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-122">If your organization wants to use (TPM) to encrypt computers, the administrator must encrypt the operating system volume of the computer with TPM protector.</span></span> <span data-ttu-id="e1b6f-123">Если в вашей организации требуется использование микросхемы TPM и предохранителя PIN-кода, администратор должен зашифровать системный том с помощью предохранителя доверенного платформенного модуля, а затем выбрать ПИН-код при первом входе.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-123">If your organization wants to use the TPM chip and a PIN protector, the administrator must encrypt the system volume with the TPM protector, and then the users select a PIN the first time they log on.</span></span> <span data-ttu-id="e1b6f-124">Если в вашей организации используется только предохранитель PIN-кода, администратору не нужно зашифровывать том первыми.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="e1b6f-125">Когда пользователи проводят вход на свои компьютеры, MBAM предложит ввести ПИН-код или PIN-код и пароль, который будет использоваться при перезагрузке компьютера позже.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-125">When users log on their computers, MBAM prompts them to provide a PIN or a PIN and a password that they will use when they restart their computer later.</span></span>

<span data-ttu-id="e1b6f-126">**Примечание**  Для включения и инициализации доверенного платформенного модуля перед поставкой компьютера пользователю параметру предохранителя TPM требуется, чтобы администратор принимал запрос BIOS.</span><span class="sxs-lookup"><span data-stu-id="e1b6f-126">**Note** The TPM protector option requires for the administrator to accept the BIOS prompt to activate and initialize the TPM before delivering the computer to the user.</span></span>

 

## <span data-ttu-id="e1b6f-127">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e1b6f-127">Related topics</span></span>


[<span data-ttu-id="e1b6f-128">Планирование развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e1b6f-128">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="e1b6f-129">Развертывание клиента MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e1b6f-129">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 





