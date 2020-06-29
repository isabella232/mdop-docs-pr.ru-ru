---
title: Планирование развертывания клиента MBAM 2.0
description: Планирование развертывания клиента MBAM 2.0
author: dansimp
ms.assetid: 3a92cf29-092f-4cad-bdfa-d5f6aafe554b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c3a7383188d4064247d8e493c8e6125fc24a1d2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812621"
---
# <span data-ttu-id="06648-103">Планирование развертывания клиента MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="06648-103">Planning for MBAM 2.0 Client Deployment</span></span>


<span data-ttu-id="06648-104">В зависимости от того, когда вы развертываете клиент администрирования и мониторинга Microsoft BitLocker (MBAM), вы можете включить шифрование диска BitLocker на компьютере в вашей организации до того, как пользователь получит компьютер или затем.</span><span class="sxs-lookup"><span data-stu-id="06648-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker drive encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="06648-105">Для обеих MBAM и топологий Configuration Manager необходимо настроить параметры групповой политики для MBAM.</span><span class="sxs-lookup"><span data-stu-id="06648-105">For both the MBAM Stand-alone and the Configuration Manager topologies, you have to configure Group Policy settings for MBAM.</span></span>

<span data-ttu-id="06648-106">Если вы используете изолированную топологию MBAM, рекомендуется использовать корпоративную систему развертывания программного обеспечения для развертывания клиентского программного обеспечения MBAM на компьютерах конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="06648-106">If you are using the MBAM Stand-alone topology, it is recommended that you use an enterprise software deployment system to deploy the MBAM Client software to end-user computers.</span></span>

<span data-ttu-id="06648-107">Если вы развертываете MBAM с топологией Configuration Manager, вы можете использовать Configuration Manager для развертывания клиентского программного обеспечения MBAM на компьютерах конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="06648-107">If you deploy MBAM with the Configuration Manager topology, you can use Configuration Manager to deploy the MBAM Client software to end-user computers.</span></span> <span data-ttu-id="06648-108">В Configuration Manager при установке MBAM создается набор компьютеров, которыми MBAM можно управлять.</span><span class="sxs-lookup"><span data-stu-id="06648-108">In Configuration Manager, the MBAM installation creates a collection of computers that MBAM can manage.</span></span> <span data-ttu-id="06648-109">В этой коллекции есть рабочие станции и устройства, у которых нет доверенного платформенного модуля (TPM), но под управлением Windows 8.</span><span class="sxs-lookup"><span data-stu-id="06648-109">This collection includes workstations and devices that do not have a Trusted Platform Module (TPM), but that are running Windows 8.</span></span>

<span data-ttu-id="06648-110">**Примечание**  Windows To Go не поддерживается для интегрированных экземпляров Configuration Manager для MBAM, если вы используете Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="06648-110">**Note** Windows To Go is not supported for integrated Configuration Manager installations of MBAM if you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="06648-111">Развертывание клиента MBAM для включения шифрования BitLocker после распространения компьютера для конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="06648-111">Deploying the MBAM Client to Enable BitLocker Encryption After Computer Distribution to End Users</span></span>


<span data-ttu-id="06648-112">После того как вы настроили групповую политику, вы можете развернуть файлы установщика Windows на целевые компьютеры с помощью системы развертывания корпоративного программного обеспечения, например Microsoft System Center Configuration Manager или доменных служб Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="06648-112">After you configure Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager or Active Directory Domain Services (AD DS) to deploy the Windows Installer files of the MBAM Client installation to target computers.</span></span> <span data-ttu-id="06648-113">Чтобы развернуть клиент MBAM, вы можете использовать 32 или 64-разрядный MbamClientSetup.exe файлов или MBAMClient.msi файлов, которые предоставляются вместе с программным обеспечением MBAM.</span><span class="sxs-lookup"><span data-stu-id="06648-113">To deploy the MBAM Client, you can use either the 32-bit or 64-bit MbamClientSetup.exe files or MBAMClient.msi files, which are provided with the MBAM software.</span></span>

<span data-ttu-id="06648-114">При развертывании клиента MBAM после распространения компьютеров на клиентские компьютеры конечные пользователи будут получать запрос на шифрование компьютера.</span><span class="sxs-lookup"><span data-stu-id="06648-114">When you deploy the MBAM Client after you distribute computers to client computers, end users are prompted to encrypt their computer.</span></span> <span data-ttu-id="06648-115">Это позволяет MBAM собирать данные, в том числе PIN-код и пароль, а затем начать процесс шифрования.</span><span class="sxs-lookup"><span data-stu-id="06648-115">This enables MBAM to collect the data, which includes the PIN and password, and then to begin the encryption process.</span></span>

<span data-ttu-id="06648-116">**Примечание**  При использовании этого подхода пользователи, у которых есть компьютеры с микросхемой TPM, получают запрос на активацию и инициализацию микросхемы TPM, если микросхема не была активирована ранее.</span><span class="sxs-lookup"><span data-stu-id="06648-116">**Note** In this approach, users who have computers with a TPM chip are prompted to activate and initialize the TPM chip if the chip has not been previously activated.</span></span>

 

## <span data-ttu-id="06648-117">Использование клиента MBAM для включения шифрования BitLocker перед распространением компьютера для конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="06648-117">Using the MBAM Client to Enable BitLocker Encryption Before Computer Distribution to End Users</span></span>


<span data-ttu-id="06648-118">В организациях, где установлены и настроены компьютеры, на которых находятся соответствующие микросхемы TPM, вы можете установить клиент MBAM для управления шифрованием BitLocker на каждом компьютере до того, как в него будут записываться пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="06648-118">In organizations where computers are received and configured centrally, and where computers have a compliant TPM chip, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="06648-119">Преимущество этого процесса состоит в том, что все компьютеры будут соответствовать требованиям шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="06648-119">The benefit of this process is that every computer will then be BitLocker encryption-compliant.</span></span> <span data-ttu-id="06648-120">Этот метод не полагается на действия пользователя, так как администратор уже зашифровал компьютер.</span><span class="sxs-lookup"><span data-stu-id="06648-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="06648-121">Ключевым допущением для этого сценария является то, что политика Организации устанавливает корпоративный образ Windows до того, как компьютер будет доставлен пользователю.</span><span class="sxs-lookup"><span data-stu-id="06648-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="06648-122">Если в вашей организации требуется использовать микросхему TPM для шифрования компьютеров, администратор добавляет предохранитель доверенного платформенного модуля для шифрования тома операционной системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="06648-122">If your organization wants to use the TPM chip to encrypt computers, the administrator adds the TPM protector to encrypt the operating system volume of the computer.</span></span> <span data-ttu-id="06648-123">Если в вашей организации требуется использование микросхемы TPM и предохранителя PIN-кода, администратор шифрует том операционной системы с предохранителем доверенного платформенного модуля, после чего пользователь выбирает ПИН-код при первом входе.</span><span class="sxs-lookup"><span data-stu-id="06648-123">If your organization wants to use the TPM chip and a PIN protector, the administrator encrypts the operating system volume with the TPM protector, and then users select a PIN when they log on for the first time.</span></span> <span data-ttu-id="06648-124">Если в вашей организации используется только предохранитель PIN-кода, администратору не нужно зашифровывать том первыми.</span><span class="sxs-lookup"><span data-stu-id="06648-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="06648-125">Когда пользователь входит в систему, администратор Microsoft BitLocker и контроль попросит их предоставить ПИН-код, а также ПИН-код и пароль, которые будут использоваться при перезапуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="06648-125">When users log on, Microsoft BitLocker Administration and Monitoring prompts them to provide a PIN, or a PIN and password to be used on later computer restarts.</span></span>

<span data-ttu-id="06648-126">**Примечание**  Для активации и инициализации доверенного платформенного модуля перед доставкой компьютера пользователю параметр предохранителя доверенного платформенного модуля требует от администратора приема запроса BIOS.</span><span class="sxs-lookup"><span data-stu-id="06648-126">**Note** The TPM protector option requires the administrator to accept the BIOS prompt to activate and initialize the TPM before the computer is delivered to the user.</span></span>

 

## <span data-ttu-id="06648-127">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="06648-127">Related topics</span></span>


[<span data-ttu-id="06648-128">Планирование развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="06648-128">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="06648-129">Развертывание клиента MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="06648-129">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 





