---
title: Управление BitLocker с помощью MBAM
description: Управление BitLocker с помощью MBAM
author: dansimp
ms.assetid: 2d24390a-87bf-48b3-96a9-3882d6f2a15c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d0de3711d5b7c3696783a054ee7c7f8220b5356
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825892"
---
# <span data-ttu-id="466a8-103">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="466a8-103">Performing BitLocker Management with MBAM</span></span>


<span data-ttu-id="466a8-104">После развертывания администрирования и мониторинга Microsoft BitLocker вы можете настроить и использовать MBAM для управления шифрованием Enterprise BitLocker.</span><span class="sxs-lookup"><span data-stu-id="466a8-104">After you deploy Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use MBAM to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="466a8-105">В этом разделе описаны задачи по управлению шифрованием, выполняемые после установки, которые можно выполнить с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="466a8-105">This section describes post-installation, day-to-day BitLocker encryption management tasks that can be accomplished by using MBAM.</span></span>

## <span data-ttu-id="466a8-106">Сброс блокировки доверенного платформенного модуля с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="466a8-106">Reset a TPM Lockout with MBAM</span></span>


<span data-ttu-id="466a8-107">Микрочип доверенного платформенного модуля (TPM) предоставляет базовые функции, связанные с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="466a8-107">A Trusted Platform Module (TPM) microchip provides basic security-related functions.</span></span> <span data-ttu-id="466a8-108">Эти функции выполняются преимущественно с помощью ключей шифрования.</span><span class="sxs-lookup"><span data-stu-id="466a8-108">These functions are accomplished primarily by the use of encryption keys.</span></span> <span data-ttu-id="466a8-109">Доверенный платформенный модуль обычно устанавливается на материнской плате компьютера или ноутбука и связывается с другими системами с помощью аппаратной шины.</span><span class="sxs-lookup"><span data-stu-id="466a8-109">The TPM is typically installed on the motherboard of a computer or laptop and communicates with the rest of the system by using a hardware bus.</span></span> <span data-ttu-id="466a8-110">Компьютеры, которые включают доверенный платформенный модуль, могут создавать криптографические ключи, которые могут быть расшифрованы только доверенным платформенным модулем.</span><span class="sxs-lookup"><span data-stu-id="466a8-110">Computers that incorporate a TPM can create cryptographic keys that can be decrypted only by the TPM.</span></span> <span data-ttu-id="466a8-111">Блокировка доверенного платформенного модуля может возникнуть, если пользователь ввел неверный ПИН-код слишком много раз.</span><span class="sxs-lookup"><span data-stu-id="466a8-111">A TPM lockout can occur if a user enters an incorrect PIN too many times.</span></span> <span data-ttu-id="466a8-112">Количество случаев, когда пользователь может ввести неверный ПИН-код, прежде чем блокировки доверенного платформенного модуля будут различаться от производителя к изготовителю.</span><span class="sxs-lookup"><span data-stu-id="466a8-112">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span> <span data-ttu-id="466a8-113">Система данных для восстановления ключа на веб-сайте администрирования MBAM позволяет получить файл пароля владельца сброса доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="466a8-113">The Key Recovery data system on the MBAM administration website enables you to obtain a reset TPM owner password file.</span></span>

[<span data-ttu-id="466a8-114">Сброс блокировки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="466a8-114">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-1.md)

## <span data-ttu-id="466a8-115">Восстановление дисков с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="466a8-115">Recover drives with MBAM</span></span>


<span data-ttu-id="466a8-116">Убедитесь в том, что вы знаете, как попытаться восстановить данные с зашифрованных дисков в случае сбоя оборудования, изменения персонала или других ситуаций, когда ключи шифрования будут утрачены.</span><span class="sxs-lookup"><span data-stu-id="466a8-116">Make sure that you know how to attempt data recovery from encrypted drives in the event of hardware failure, changes in personnel, or other situations in which encryption keys are lost.</span></span> <span data-ttu-id="466a8-117">Возможности восстановления зашифрованных дисков в MBAM обеспечивают сбор и хранение данных и доступность средств, необходимых для доступа к тому, защищенному BitLocker, при переходе в режим восстановления, если том перемещается или повреждается.</span><span class="sxs-lookup"><span data-stu-id="466a8-117">The Encrypted Drive Recovery features of MBAM provide the capture and storage of data and availability of tools required to access a BitLocker-protected volume when the volume goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="466a8-118">Восстановление диска в режиме восстановления</span><span class="sxs-lookup"><span data-stu-id="466a8-118">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-1.md)

[<span data-ttu-id="466a8-119">Восстановление перемещенного диска</span><span class="sxs-lookup"><span data-stu-id="466a8-119">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-1.md)

[<span data-ttu-id="466a8-120">Восстановление поврежденного диска</span><span class="sxs-lookup"><span data-stu-id="466a8-120">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-1.md)

## <span data-ttu-id="466a8-121">Определение состояния шифрования BitLocker для потерянных компьютеров с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="466a8-121">Determine BitLocker Encryption State of lost computers by Using MBAM</span></span>


<span data-ttu-id="466a8-122">Если вы используете MBAM, вы можете определить Последнее известное состояние шифрования BitLocker для компьютеров, которые были утрачены или украдены.</span><span class="sxs-lookup"><span data-stu-id="466a8-122">When you use MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="466a8-123">Определение состояния шифрования BitLocker утерянных компьютеров</span><span class="sxs-lookup"><span data-stu-id="466a8-123">How to Determine the BitLocker Encryption State of a Lost Computers</span></span>](how-to-determine-the-bitlocker-encryption-state-of-a-lost-computers-mbam-1.md)

## <span data-ttu-id="466a8-124">Другие ресурсы для управления BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="466a8-124">Other resources for performing BitLocker Management with MBAM</span></span>


[<span data-ttu-id="466a8-125">Операции MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="466a8-125">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





