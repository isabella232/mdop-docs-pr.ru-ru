---
title: Управление BitLocker с помощью MBAM
description: Управление BitLocker с помощью MBAM
author: dansimp
ms.assetid: 9bfc6c67-f12c-4daa-8f08-5884fb47443c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d261ec4fa789cd331209afe1c2f1858d627209a3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826499"
---
# <span data-ttu-id="724b9-103">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="724b9-103">Performing BitLocker Management with MBAM</span></span>


<span data-ttu-id="724b9-104">После планирования и развертывания администрирования и мониторинга Microsoft BitLocker (MBAM) вы можете настроить и использовать его для управления шифрованием в корпоративной среде BitLocker.</span><span class="sxs-lookup"><span data-stu-id="724b9-104">After planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="724b9-105">В этом разделе приведены сведения о задачах управления шифрованием, выполняемых после установки, которые выполняются с помощью администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="724b9-105">The information in this section describes post-installation day-to-day BitLocker encryption management tasks that are accomplished by using Microsoft BitLocker Administration and Monitoring.</span></span>

## <span data-ttu-id="724b9-106">Сброс блокировки доверенного платформенного модуля с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="724b9-106">Reset a TPM Lockout by Using MBAM</span></span>


<span data-ttu-id="724b9-107">Доверенный платформенный модуль (TPM) — это микрочип, разработанный для обеспечения основных функций, связанных с безопасностью, в основном включающих ключи шифрования.</span><span class="sxs-lookup"><span data-stu-id="724b9-107">A Trusted Platform Module (TPM) is a microchip that is designed to provide basic security-related functions, primarily involving encryption keys.</span></span> <span data-ttu-id="724b9-108">Доверенный платформенный модуль обычно устанавливается на материнской плате компьютера или ноутбука и связывается с другими системами с помощью аппаратной шины.</span><span class="sxs-lookup"><span data-stu-id="724b9-108">The TPM is usually installed on the motherboard of a computer or laptop, and communicates with the rest of the system by using a hardware bus.</span></span> <span data-ttu-id="724b9-109">Компьютеры, содержащие доверенный платформенный модуль, имеют возможность создавать криптографические ключи и шифровать их, чтобы их можно было расшифровать только с помощью доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="724b9-109">Computers that incorporate a TPM have the ability to create cryptographic keys and encrypt them so that they can be decrypted only by the TPM.</span></span>

<span data-ttu-id="724b9-110">Блокировка доверенного платформенного модуля может возникнуть, если пользователь ввел неверный ПИН-код слишком много раз.</span><span class="sxs-lookup"><span data-stu-id="724b9-110">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="724b9-111">Количество случаев, когда пользователь может ввести неверный ПИН-код, прежде чем блокировки доверенного платформенного модуля будут различаться от производителя к изготовителю.</span><span class="sxs-lookup"><span data-stu-id="724b9-111">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span> <span data-ttu-id="724b9-112">Вы можете использовать MBAM для доступа к централизованной системе данных восстановления ключей на веб-сайте администрирования и мониторинга, где вы можете получить пароль владельца доверенного платформенного модуля при указании идентификатора компьютера и соответствующего идентификатора пользователя.</span><span class="sxs-lookup"><span data-stu-id="724b9-112">You can use MBAM to access the centralized Key Recovery data system in the Administration and Monitoring website, where you can retrieve a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

[<span data-ttu-id="724b9-113">Сброс блокировки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="724b9-113">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

## <span data-ttu-id="724b9-114">Восстановление дисков с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="724b9-114">Recover Drives with MBAM</span></span>


<span data-ttu-id="724b9-115">При работе с шифрованием данных, особенно в корпоративной среде, учитывайте, как эти данные могут быть восстановлены в случае сбоя оборудования, изменения персонала или других ситуаций, в которых могут быть утрачены ключи шифрования.</span><span class="sxs-lookup"><span data-stu-id="724b9-115">When you are dealing with the encryption of data, especially in an enterprise environment, consider how that data can be recovered in the event of a hardware failure, changes in personnel, or other situations in which encryption keys can be lost.</span></span>

<span data-ttu-id="724b9-116">Возможности восстановления зашифрованных дисков MBAM гарантируют, что данные могут быть записаны и сохранены, а необходимые средства доступны для доступа к тому, защищенному с помощью BitLocker, когда BitLocker переходит в режим восстановления, перемещается или повреждается.</span><span class="sxs-lookup"><span data-stu-id="724b9-116">The encrypted drive recovery features of MBAM ensure that data can be captured and stored and that the required tools are available to access a BitLocker-protected volume when BitLocker goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="724b9-117">Восстановление диска в режиме восстановления</span><span class="sxs-lookup"><span data-stu-id="724b9-117">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

[<span data-ttu-id="724b9-118">Восстановление перемещенного диска</span><span class="sxs-lookup"><span data-stu-id="724b9-118">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

[<span data-ttu-id="724b9-119">Восстановление поврежденного диска</span><span class="sxs-lookup"><span data-stu-id="724b9-119">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

## <span data-ttu-id="724b9-120">Определение состояния шифрования BitLocker для потерянных компьютеров с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="724b9-120">Determine BitLocker Encryption State of Lost Computers by Using MBAM</span></span>


<span data-ttu-id="724b9-121">С помощью MBAM вы можете определить Последнее известное состояние шифрования BitLocker для компьютеров, которые были утрачены или украдены.</span><span class="sxs-lookup"><span data-stu-id="724b9-121">Using MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="724b9-122">Определение состояния шифрования BitLocker утерянных компьютеров</span><span class="sxs-lookup"><span data-stu-id="724b9-122">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

## <span data-ttu-id="724b9-123">Использование портала самообслуживания для восстановления доступа к компьютеру</span><span class="sxs-lookup"><span data-stu-id="724b9-123">Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="724b9-124">Если конечные пользователи заблокировали Windows с помощью BitLocker, они могут использовать инструкции, описанные в этом разделе, чтобы получить ключ восстановления BitLocker, чтобы восстановить доступ к своему компьютеру.</span><span class="sxs-lookup"><span data-stu-id="724b9-124">If end users get locked out of Windows by BitLocker, they can use the instructions in this section to get a BitLocker recovery key to regain access to their computer.</span></span>

[<span data-ttu-id="724b9-125">Восстановление доступа к компьютеру с помощью портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="724b9-125">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>](how-to-use-the-self-service-portal-to-regain-access-to-a-computer.md)

## <span data-ttu-id="724b9-126">Другие ресурсы для управления BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="724b9-126">Other Resources for Performing BitLocker Management with MBAM</span></span>


[<span data-ttu-id="724b9-127">Операции MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="724b9-127">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





