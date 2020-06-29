---
title: Необходимые условия для клиентов MBAM 2.5
description: Необходимые условия для клиентов MBAM 2.5
author: dansimp
ms.assetid: fc230679-9c84-4b99-a77c-bae7e7bf8145
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: ac5e211e5ea038f47db3d5e68155eb5af38aa231
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826969"
---
# <span data-ttu-id="4a5a9-103">Необходимые условия для клиентов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4a5a9-103">Prerequisites for MBAM 2.5 Clients</span></span>


<span data-ttu-id="4a5a9-104">Перед установкой клиентского программного обеспечения MBAM на компьютерах конечных пользователей убедитесь, что ваша среда и клиентские компьютеры соответствуют следующим требованиям.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-104">Before you install the MBAM Client software on end users' computers, ensure that your environment and the client computers meet the following prerequisites.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4a5a9-105">Предварительные</span><span class="sxs-lookup"><span data-stu-id="4a5a9-105">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="4a5a9-106">Сведения</span><span class="sxs-lookup"><span data-stu-id="4a5a9-106">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4a5a9-107">Корпоративный домен должен содержать по крайней мере один контроллер домена Windows Server 2008 (или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="4a5a9-107">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4a5a9-108">Клиентский компьютер должен войти в корпоративную интрасеть.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-108">The client computer must be logged on to the enterprise intranet.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4a5a9-109">Только для клиентских компьютеров с Windows 7: каждый клиент должен иметь возможность доверенного платформенного модуля (TPM) (TPM 1,2 или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="4a5a9-109">For Windows 7 client computers only: Each client must have Trusted Platform Module (TPM) capability (TPM 1.2 or later).</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4a5a9-110">Для Windows 8,1, Windows 10 RTM или Windows 10 версии 1511 только на клиентских компьютерах: Если вы хотите, чтобы MBAM мог хранить ключи восстановления доверенного платформенного модуля и управлять ими, необходимо отключить автоматическое наполнение TPM и MBAM, который должен быть указан в качестве владельца доверенного платформенного модуля перед развертыванием MBAM.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-110">For Windows 8.1, Windows 10 RTM or Windows 10 version 1511 client computers only: If you want MBAM to be able to store and manage the TPM recovery keys, TPM auto-provisioning must be turned off, and MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span></p>
<p><span data-ttu-id="4a5a9-111">В MBAM 2,5 с пакетом обновления 1 (SP1) вам больше не нужно включать автоматическое предоставление TPM, но необходимо убедиться в том, что для объектов групповой политики доверенного платформенного модуля не задано криптоключ OwnerAuth в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-111">In MBAM 2.5 SP1 only, you no longer need to turn off TPM auto-provisioning, but you must make sure that the TPM Group Policy Objects are set to not escrow TPM OwnerAuth to Active Directory.</span></span></p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md#bkmk-tpm" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm)"><span data-ttu-id="4a5a9-112">Процедуры безопасности MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4a5a9-112">MBAM 2.5 Security Considerations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4a5a9-113">В Windows 10 версии 1607 или более поздней права собственности на этот доверенный платформенный модуль могут получить только Windows.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-113">For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="4a5a9-114">В addiiton при подготовке доверенного платформенного модуля Windows не сохранит пароль владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-114">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span></p>
<p><span data-ttu-id="4a5a9-115">В MBAM 2,5 с пакетом обновления 1 (SP1) необходимо включить функцию автоматического конфигурирования.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-115">In MBAM 2.5 SP1, you must turn on auto-provisioning.</span></span></p>
</p></td>
<td align="left"><p><span data-ttu-id="4a5a9-116">Дополнительные <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)"> сведения приведены в разделе пароль владельца доверенного платформенного модуля </a> .</span><span class="sxs-lookup"><span data-stu-id="4a5a9-116">See <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)">TPM owner password</a> for further details.</span></span>
</p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4a5a9-117">Микросхема TPM должна быть включена в BIOS и может быть переустановлена из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-117">The TPM chip must be turned on in the BIOS and be resettable from the operating system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4a5a9-118">Дополнительные сведения приведены в документации по BIOS.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-118">See the BIOS documentation for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4a5a9-119">На жестком диске компьютера должны быть по крайней мере два раздела, которые необходимо отформатировать с помощью файловой системы NTFS.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-119">The computer’s hard disk must have at least two partitions and must be formatted with the NTFS file system.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4a5a9-120">На жестком диске компьютера должна быть установлена BIOS, совместимая с TPM и поддерживающая USB-устройства во время запуска компьютера.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-120">The computer’s hard disk must have a BIOS that is compatible with TPM and that supports USB devices during computer startup.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="4a5a9-121">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-121">Note</span></span></strong><br/><p><span data-ttu-id="4a5a9-122">Убедитесь, что клавиатура, видео или мышь подключены напрямую и не управляются с помощью клавиатуры, видео или мыши (KVM) Switch.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-122">Ensure that the keyboard, video, or mouse are directly connected and not managed through a keyboard, video, or mouse (KVM) switch.</span></span> <span data-ttu-id="4a5a9-123">КВМ-коммутатор может взаимодействовать с возможностями компьютера, чтобы обнаружить физическое присутствие оборудования.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-123">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4a5a9-124">Если вы используете прокси-сервер, он должен быть видимым в контексте системы.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-124">If you use a proxy, it must be visible in the system context.</span></span> <span data-ttu-id="4a5a9-125">MBAM выполняется под контекстом системы, а не контекстом пользователя.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-125">MBAM runs under the system context, not the user context.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="4a5a9-126">Важно.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-126">Important</span></span>**  
<span data-ttu-id="4a5a9-127">Если вы используете BitLocker без MBAM, то MBAM можно установить и использовать существующие данные TPM.</span><span class="sxs-lookup"><span data-stu-id="4a5a9-127">If BitLocker was used without MBAM, MBAM can be installed and utilize the existing TPM information.</span></span>




## <span data-ttu-id="4a5a9-128">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4a5a9-128">Related topics</span></span>


[<span data-ttu-id="4a5a9-129">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4a5a9-129">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

[<span data-ttu-id="4a5a9-130">Планирование развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4a5a9-130">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)


## <span data-ttu-id="4a5a9-131">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="4a5a9-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4a5a9-132">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="4a5a9-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="4a5a9-133">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4a5a9-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






