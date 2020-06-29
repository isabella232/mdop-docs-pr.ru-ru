---
title: Планирование развертывания клиента MBAM 2.5
description: Планирование развертывания клиента MBAM 2.5
author: dansimp
ms.assetid: 23c89976-af24-4753-9412-ce0ea42d1964
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ff03b58da0985b2f57308c99a9bc15f4a0554623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825992"
---
# <span data-ttu-id="d53e8-103">Планирование развертывания клиента MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d53e8-103">Planning for MBAM 2.5 Client Deployment</span></span>


<span data-ttu-id="d53e8-104">В зависимости от того, когда вы развертываете клиентское программное обеспечение Microsoft BitLocker Administration и Monitoring (MBAM), вы можете включить шифрование диска BitLocker на компьютере в вашей организации до того, как пользователь получит компьютер или позже.</span><span class="sxs-lookup"><span data-stu-id="d53e8-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client software, you can enable BitLocker Drive Encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="d53e8-105">Для обеих MBAM и топологий интеграции System Center Configuration Manager необходимо настроить параметры групповой политики для MBAM.</span><span class="sxs-lookup"><span data-stu-id="d53e8-105">For both the MBAM Stand-alone and the System Center Configuration Manager Integration topologies, you have to configure Group Policy settings for MBAM.</span></span>

<span data-ttu-id="d53e8-106">Если вы используете изолированную топологию MBAM, мы рекомендуем использовать корпоративную систему развертывания программного обеспечения для развертывания клиентского программного обеспечения MBAM на компьютерах конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="d53e8-106">If you are using the MBAM Stand-alone topology, we recommend that you use an enterprise software deployment system to deploy the MBAM Client software to end-user computers.</span></span>

<span data-ttu-id="d53e8-107">Если вы развертываете MBAM с топологией интеграции Configuration Manager, вы можете использовать Configuration Manager для развертывания клиентского программного обеспечения MBAM на компьютерах конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="d53e8-107">If you deploy MBAM with the Configuration Manager Integration topology, you can use Configuration Manager to deploy the MBAM Client software to end-user computers.</span></span> <span data-ttu-id="d53e8-108">В Configuration Manager при установке MBAM создается набор компьютеров, которыми MBAM можно управлять.</span><span class="sxs-lookup"><span data-stu-id="d53e8-108">In Configuration Manager, the MBAM installation creates a collection of computers that MBAM can manage.</span></span> <span data-ttu-id="d53e8-109">В этой коллекции есть рабочие станции и устройства, у которых нет доверенного платформенного модуля (TPM), но под управлением Windows 8, Windows 8,1 или Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d53e8-109">This collection includes workstations and devices that do not have a Trusted Platform Module (TPM), but that are running Windows 8, Windows 8.1, or Windows 10.</span></span>

<span data-ttu-id="d53e8-110">**Примечание**  Windows To Go не поддерживается при установке топологии интеграции Configuration Manager при использовании Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="d53e8-110">**Note** Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="d53e8-111">Развертывание клиента MBAM для включения шифрования диска BitLocker после распространения компьютера для конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="d53e8-111">Deploying the MBAM Client to enable BitLocker Drive Encryption after computer distribution to end users</span></span>


<span data-ttu-id="d53e8-112">После того как вы настроили групповую политику, вы можете развернуть файлы установщика Windows на целевые компьютеры с помощью системы развертывания корпоративного программного обеспечения, например Microsoft System Center Configuration Manager или доменных служб Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="d53e8-112">After you configure Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager or Active Directory Domain Services (AD DS) to deploy the Windows Installer files of the MBAM Client installation to target computers.</span></span> <span data-ttu-id="d53e8-113">Чтобы развернуть клиент MBAM, вы можете использовать 32 или 64-разрядную MbamClientSetup.exe файлов или MBAMClient.msi файлов, которые предоставляются в клиентском программном обеспечении MBAM.</span><span class="sxs-lookup"><span data-stu-id="d53e8-113">To deploy the MBAM Client, you can use either the 32-bit or 64-bit MbamClientSetup.exe files or MBAMClient.msi files, which are provided with the MBAM Client software.</span></span>

<span data-ttu-id="d53e8-114">**Примечание**  Начиная с MBAM 2,5 с пакетом обновления 1 (SP1), отдельный MSI больше не входит в состав продукта MBAM.</span><span class="sxs-lookup"><span data-stu-id="d53e8-114">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="d53e8-115">Тем не менее, вы можете извлечь MSI из исполняемого файла (exe), который входит в состав продукта.</span><span class="sxs-lookup"><span data-stu-id="d53e8-115">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

 

<span data-ttu-id="d53e8-116">При развертывании клиента MBAM после распространения компьютеров на клиентские компьютеры конечные пользователи будут получать запрос на шифрование компьютера.</span><span class="sxs-lookup"><span data-stu-id="d53e8-116">When you deploy the MBAM Client after you distribute computers to client computers, end users are prompted to encrypt their computer.</span></span> <span data-ttu-id="d53e8-117">Это действие позволяет MBAM собирать данные, в том числе PIN-код и пароль (если это требуется политикой), а затем начать процесс шифрования.</span><span class="sxs-lookup"><span data-stu-id="d53e8-117">This action enables MBAM to collect the data, which includes the PIN and password (if required by policy), and then to begin the encryption process.</span></span>

<span data-ttu-id="d53e8-118">**Примечание**  При использовании этого подхода конечные пользователи, у которых есть компьютеры с микросхемой TPM, получают запрос на активацию и инициализацию микросхемы TPM, если микросхема не была активирована ранее.</span><span class="sxs-lookup"><span data-stu-id="d53e8-118">**Note** In this approach, end users who have computers with a TPM chip are prompted to activate and initialize the TPM chip if the chip has not been previously activated.</span></span>

 

## <span data-ttu-id="d53e8-119">Использование клиента MBAM для включения шифрования диска BitLocker перед распространением компьютера для конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="d53e8-119">Using the MBAM Client to enable BitLocker Drive Encryption before computer distribution to end users</span></span>


<span data-ttu-id="d53e8-120">В организациях, где будут централизованно получены и настраиваться компьютеры, и где компьютеры имеют соответствующие микросхемы TPM, вы можете использовать клиент MBAM для управления шифрованием диска BitLocker на каждом компьютере перед записью в него данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="d53e8-120">In organizations where computers are received and configured centrally, and where computers have a compliant TPM chip, you can use the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="d53e8-121">Преимущество этого процесса состоит в том, что все компьютеры удовлетворяют требованиям.</span><span class="sxs-lookup"><span data-stu-id="d53e8-121">The benefit of this process is that every computer is then compliant.</span></span> <span data-ttu-id="d53e8-122">Этот метод не полагается на действия пользователя, так как администратор уже зашифровал компьютер.</span><span class="sxs-lookup"><span data-stu-id="d53e8-122">This method does not rely on end-user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="d53e8-123">Ключевым допущением для этого сценария является то, что политика Организации устанавливает корпоративный образ Windows до того, как компьютер будет доставлен конечному пользователю.</span><span class="sxs-lookup"><span data-stu-id="d53e8-123">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the end user.</span></span>

<span data-ttu-id="d53e8-124">Если в вашей организации требуется использовать микросхему TPM для шифрования компьютеров, администратор добавляет предохранитель доверенного платформенного модуля для шифрования тома операционной системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="d53e8-124">If your organization wants to use the TPM chip to encrypt computers, the administrator adds the TPM protector to encrypt the operating system volume of the computer.</span></span> <span data-ttu-id="d53e8-125">Если в вашей организации требуется использование микросхемы TPM и предохранителя PIN-кода, администратор шифрует том операционной системы с предохранителем доверенного платформенного модуля, а затем конечные пользователи выбирают ПИН-код при первом входе.</span><span class="sxs-lookup"><span data-stu-id="d53e8-125">If your organization wants to use the TPM chip and a PIN protector, the administrator encrypts the operating system volume with the TPM protector, and then end users select a PIN when they log on for the first time.</span></span> <span data-ttu-id="d53e8-126">Если в вашей организации используется только предохранитель PIN-кода, администратору не нужно зашифровывать том первыми.</span><span class="sxs-lookup"><span data-stu-id="d53e8-126">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="d53e8-127">При входе в систему конечных пользователей система администрирования и мониторинга Microsoft BitLocker предлагает им ввести ПИН-код или ПИН-код и пароль, которые будут использоваться при перезапуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="d53e8-127">When end users log on, Microsoft BitLocker Administration and Monitoring prompts them to provide a PIN, or a PIN and password to be used on later computer restarts.</span></span>

<span data-ttu-id="d53e8-128">**Примечание**  Параметр предохранителя доверенного платформенного модуля требует от администратора приема запроса BIOS для активации и инициализации TPM перед доставкой компьютера конечному пользователю.</span><span class="sxs-lookup"><span data-stu-id="d53e8-128">**Note** The TPM protector option requires the administrator to accept the BIOS prompt to activate and initialize the TPM before the computer is delivered to the end user.</span></span>

 

## <span data-ttu-id="d53e8-129">Поддержка зашифрованных жестких дисков в клиенте MBAM</span><span class="sxs-lookup"><span data-stu-id="d53e8-129">MBAM Client support for Encrypted Hard Drives</span></span>


<span data-ttu-id="d53e8-130">MBAM поддерживает BitLocker на зашифрованных жестких дисках, отвечающих требованиям к спецификации TCG для Opalis и стандарту IEEE 1667.</span><span class="sxs-lookup"><span data-stu-id="d53e8-130">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="d53e8-131">Если на этих устройствах включена функция BitLocker, она будет создавать ключи и выполнять функции управления на зашифрованном диске.</span><span class="sxs-lookup"><span data-stu-id="d53e8-131">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="d53e8-132">Более подробную информацию вы видите на [жестком диске с шифрованием](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d53e8-132">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>


## <span data-ttu-id="d53e8-133">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d53e8-133">Related topics</span></span>


[<span data-ttu-id="d53e8-134">Планирование развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d53e8-134">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="d53e8-135">Развертывание клиента MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d53e8-135">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

 

 
## <span data-ttu-id="d53e8-136">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="d53e8-136">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d53e8-137">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="d53e8-137">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="d53e8-138">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="d53e8-138">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




