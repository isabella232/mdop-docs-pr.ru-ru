---
title: Управление BitLocker с помощью MBAM 2.5
description: Управление BitLocker с помощью MBAM 2.5
author: dansimp
ms.assetid: 068f3ee0-300c-4083-ba18-7065eef997ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a0ee5802f945176914c56659e0ff7e34e93a969
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826009"
---
# <span data-ttu-id="d5420-103">Управление BitLocker с помощью MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d5420-103">Performing BitLocker Management with MBAM 2.5</span></span>


<span data-ttu-id="d5420-104">После планирования и развертывания администрирования и мониторинга Microsoft BitLocker (MBAM) вы можете настроить и использовать его для управления шифрованием диска BitLocker на предприятии.</span><span class="sxs-lookup"><span data-stu-id="d5420-104">After planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage BitLocker Drive Encryption across your enterprise.</span></span> <span data-ttu-id="d5420-105">Сведения в этом разделе описывают задачи управления шифрованием, выполняемые после установки, которые выполняются с помощью администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d5420-105">The information in this section describes post-installation, day-to-day BitLocker encryption management tasks that are accomplished by using Microsoft BitLocker Administration and Monitoring.</span></span>

## <span data-ttu-id="d5420-106">Сброс блокировки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="d5420-106">Reset a TPM lockout</span></span>


<span data-ttu-id="d5420-107">Доверенный платформенный модуль (TPM) — это микрочип, разработанный для обеспечения основных функций, связанных с безопасностью, в основном включающих ключи шифрования.</span><span class="sxs-lookup"><span data-stu-id="d5420-107">A Trusted Platform Module (TPM) is a microchip that is designed to provide basic security-related functions, primarily involving encryption keys.</span></span> <span data-ttu-id="d5420-108">Доверенный платформенный модуль обычно устанавливается на материнской плате компьютера и связывается с другими компонентами системы с помощью адаптера шины хоста.</span><span class="sxs-lookup"><span data-stu-id="d5420-108">The TPM is usually installed on the motherboard of a computer, and it communicates with the rest of the system by using a host bus adapter.</span></span> <span data-ttu-id="d5420-109">На компьютерах, включающих доверенный платформенный модуль, вы можете создавать криптографические ключи и зашифровывать их так, чтобы они могли расшифровываться только доверенным платформенным модулем.</span><span class="sxs-lookup"><span data-stu-id="d5420-109">On computers that incorporate a TPM, you can create cryptographic keys and encrypt them so that they can be decrypted only by the TPM.</span></span>

<span data-ttu-id="d5420-110">Блокировка доверенного платформенного модуля может возникнуть, если пользователь ввел неверный ПИН-код слишком много раз.</span><span class="sxs-lookup"><span data-stu-id="d5420-110">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="d5420-111">Количество случаев, когда пользователь может ввести неверный ПИН-код, прежде чем блокировки доверенного платформенного модуля зависят от производителя.</span><span class="sxs-lookup"><span data-stu-id="d5420-111">The number of times that a user can enter an incorrect PIN before the TPM locks varies by manufacturer.</span></span> <span data-ttu-id="d5420-112">Вы можете использовать MBAM для доступа к системе данных для восстановления ключей на веб-сайте администрирования и мониторинга, где вы можете получить файл пароля владельца доверенного платформенного модуля, когда вы предоставляете идентификатор компьютера и соответствующий идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="d5420-112">You can use MBAM to access the centralized key recovery data system on the Administration and Monitoring Website, where you can retrieve a TPM owner password file when you supply a computer ID and an associated user identifier.</span></span>

[<span data-ttu-id="d5420-113">Сброс блокировки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="d5420-113">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-25.md)

## <span data-ttu-id="d5420-114">Восстановление дисков</span><span class="sxs-lookup"><span data-stu-id="d5420-114">Recover drives</span></span>


<span data-ttu-id="d5420-115">При работе с шифрованием данных, особенно в корпоративной среде, учитывайте, как эти данные могут быть восстановлены в случае сбоя оборудования, изменения персонала или других ситуаций, в которых могут быть утрачены ключи шифрования.</span><span class="sxs-lookup"><span data-stu-id="d5420-115">When you are dealing with the encryption of data, especially in an enterprise environment, consider how that data can be recovered in the event of a hardware failure, changes in personnel, or other situations in which encryption keys can be lost.</span></span>

<span data-ttu-id="d5420-116">Функции восстановления зашифрованных дисков в MBAM обеспечивают запись и сохранение данных и доступность необходимых средств для доступа к тому, защищенному с помощью BitLocker, когда BitLocker переходит в режим восстановления, перемещается или повреждается.</span><span class="sxs-lookup"><span data-stu-id="d5420-116">The encrypted drive recovery features in MBAM ensure that data can be captured and stored and that the required tools are available to access a BitLocker-protected volume when BitLocker goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="d5420-117">Восстановление диска в режиме восстановления</span><span class="sxs-lookup"><span data-stu-id="d5420-117">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)

[<span data-ttu-id="d5420-118">Восстановление перемещенного диска</span><span class="sxs-lookup"><span data-stu-id="d5420-118">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-25.md)

[<span data-ttu-id="d5420-119">Восстановление поврежденного диска</span><span class="sxs-lookup"><span data-stu-id="d5420-119">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-25.md)

## <span data-ttu-id="d5420-120">Определение состояния шифрования BitLocker для потерянных компьютеров</span><span class="sxs-lookup"><span data-stu-id="d5420-120">Determine BitLocker encryption state of lost computers</span></span>


<span data-ttu-id="d5420-121">С помощью MBAM вы можете определить Последнее известное состояние шифрования BitLocker для компьютеров, которые были утрачены или украдены.</span><span class="sxs-lookup"><span data-stu-id="d5420-121">By using MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="d5420-122">Определение состояния шифрования BitLocker утерянных компьютеров</span><span class="sxs-lookup"><span data-stu-id="d5420-122">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)

## <span data-ttu-id="d5420-123">Использование портала самообслуживания для восстановления доступа к компьютеру</span><span class="sxs-lookup"><span data-stu-id="d5420-123">Use the Self-Service Portal to regain access to a computer</span></span>


<span data-ttu-id="d5420-124">Если конечные пользователи заблокировали Windows с помощью BitLocker, они могут использовать инструкции, описанные в этом разделе, чтобы получить ключ восстановления BitLocker, чтобы восстановить доступ к своему компьютеру.</span><span class="sxs-lookup"><span data-stu-id="d5420-124">If end users get locked out of Windows by BitLocker, they can use the instructions in this section to get a BitLocker recovery key to regain access to their computer.</span></span>

[<span data-ttu-id="d5420-125">Восстановление доступа к компьютеру с помощью портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="d5420-125">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>](how-to-use-the-self-service-portal-to-regain-access-to-a-computer-mbam-25.md)



## <span data-ttu-id="d5420-126">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d5420-126">Related topics</span></span>


[<span data-ttu-id="d5420-127">Операции MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d5420-127">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)

 

## <span data-ttu-id="d5420-128">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="d5420-128">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d5420-129">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="d5420-129">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="d5420-130">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="d5420-130">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





