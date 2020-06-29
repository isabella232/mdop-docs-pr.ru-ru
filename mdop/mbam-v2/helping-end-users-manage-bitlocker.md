---
title: Помощь конечным пользователям в управлении BitLocker
description: Помощь конечным пользователям в управлении BitLocker
author: dansimp
ms.assetid: 47776fb3-2d94-4970-b687-c35ec3dd6c64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26ef2bc33a75ff7773b75807ab0e10e5aa67b109
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824779"
---
# <span data-ttu-id="f7e6b-103">Помощь конечным пользователям в управлении BitLocker</span><span class="sxs-lookup"><span data-stu-id="f7e6b-103">Helping End Users Manage BitLocker</span></span>


<span data-ttu-id="f7e6b-104">Содержимое потерянного или украденного компьютера уязвимо для несанкционированного доступа, что может представлять угрозу безопасности как для людей, так и для компаний.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-104">Content on a lost or stolen computer is vulnerable to unauthorized access, which can present a security risk to both people and companies.</span></span> <span data-ttu-id="f7e6b-105">Администрирование и мониторинг Microsoft BitLocker (MBAM) использует BitLocker, чтобы предотвратить несанкционированный доступ, заблокируя компьютер, чтобы защитить конфиденциальные данные от вредоносных пользователей.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-105">Microsoft BitLocker Administration and Monitoring (MBAM) uses BitLocker to help prevent unauthorized access by locking your computer to help protect sensitive data from malicious users.</span></span>

## <span data-ttu-id="f7e6b-106">Что такое BitLocker?</span><span class="sxs-lookup"><span data-stu-id="f7e6b-106">What is BitLocker?</span></span>


<span data-ttu-id="f7e6b-107">Шифрование диска BitLocker обеспечивает защиту дисков операционной системы, дисков данных и съемных носителей (например, USB-накопителей), шифруя диски.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-107">BitLocker Drive Encryption can provide protection for operating system drives, data drives, and removable drives (such as a USB thumb drive) by encrypting the drives.</span></span> <span data-ttu-id="f7e6b-108">В зависимости от того, как настроена программа BitLocker, пользователям может потребоваться предоставить ключ (пароль или ПИН-код), чтобы разблокировать данные, хранящиеся на зашифрованных дисках.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-108">Depending on how BitLocker is configured, users may have to provide a key (a password or PIN) to unlock the information that is stored on the encrypted drives.</span></span>

<span data-ttu-id="f7e6b-109">При добавлении новых файлов на диск, зашифрованный с помощью BitLocker, BitLocker шифрует их автоматически.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-109">When you add new files to a drive that is encrypted with BitLocker, BitLocker encrypts them automatically.</span></span> <span data-ttu-id="f7e6b-110">Файлы будут зашифрованы только в том случае, если они хранятся на зашифрованном диске.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-110">Files remain encrypted only while they are stored in the encrypted drive.</span></span> <span data-ttu-id="f7e6b-111">Файлы, которые копируются на другой диск или компьютер, расшифровываются.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-111">Files that are copied to another drive or computer are decrypted.</span></span> <span data-ttu-id="f7e6b-112">Если вы предоставляете общий доступ к файлам другим пользователям, например по сети, эти файлы шифруются при сохранении на зашифрованном диске, но доступ к ним можно получить с помощью уполномоченных пользователей.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-112">If you share files with other users, such as through a network, these files are encrypted while stored on the encrypted drive, but they can be accessed normally by authorized users.</span></span>

<span data-ttu-id="f7e6b-113">Если вы зашифруете диск операционной системы, при запуске BitLocker проверяет его во время запуска, чтобы убедиться, что это может представлять угрозу безопасности (например, изменение BIOS или изменение любых файлов автозагрузки).</span><span class="sxs-lookup"><span data-stu-id="f7e6b-113">If you encrypt the operating system drive, BitLocker checks the computer during startup for any conditions that could represent a security risk (for example, a change to the BIOS or changes to any startup files).</span></span> <span data-ttu-id="f7e6b-114">Если обнаружена потенциальная угроза безопасности, BitLocker блокирует диск операционной системы и требует специального ключа восстановления BitLocker, чтобы разблокировать его.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-114">If a potential security risk is detected, BitLocker will lock the operating system drive and require a special BitLocker recovery key to unlock it.</span></span> <span data-ttu-id="f7e6b-115">Убедитесь, что вы создали этот ключ восстановления при первом запуске BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-115">Make sure that you create this recovery key when you turn on BitLocker for the first time.</span></span> <span data-ttu-id="f7e6b-116">В противном случае доступ к своим файлам будет потерян.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-116">Otherwise, you could permanently lose access to your files.</span></span>

<span data-ttu-id="f7e6b-117">Если вы записываете данные на съемные диски (стационарные или сменные), вы можете разблокировать зашифрованный диск с помощью пароля или смарт-карты или настроить автоматическое снятие блокировки при входе в систему на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-117">If you encrypt data drives (fixed or removable), you can unlock an encrypted drive with a password or a smart card, or set the drive to automatically unlock when you log on to the computer.</span></span>

<span data-ttu-id="f7e6b-118">В дополнение к паролям и контактам, BitLocker может использовать микросхему доверенного платформенного модуля (TPM), которая предоставляется на многих современных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-118">In addition to passwords and PINs, BitLocker can use the Trusted Platform Module (TPM) chip that is provided in many newer computers.</span></span> <span data-ttu-id="f7e6b-119">Микросхема TPM используется для того, чтобы убедиться в том, что компьютер не был подменен, пока BitLocker не заблокирует диск операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-119">The TPM chip is used to ensure that your computer has not been tampered with before BitLocker will unlock the operating system drive.</span></span> <span data-ttu-id="f7e6b-120">В процессе шифрования может потребоваться включить микросхему доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-120">During the encryption process, you may have to enable the TPM chip.</span></span> <span data-ttu-id="f7e6b-121">При запуске компьютера BitLocker запрашивает у доверенного платформенного модуля ключи на диск и разблокирует его.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-121">When you start your computer, BitLocker asks the TPM for the keys to the drive and unlocks it.</span></span> <span data-ttu-id="f7e6b-122">Для включения микросхемы TPM вам потребуется перезагрузить компьютер, а затем изменить параметры в BIOS (предварительно установленный уровень программного обеспечения компьютера).</span><span class="sxs-lookup"><span data-stu-id="f7e6b-122">To enable the TPM chip, you will have to restart your computer and then change a setting in the BIOS, a pre-Windows layer of your computer software.</span></span> <span data-ttu-id="f7e6b-123">Дополнительные сведения о TPM можно найти в разделе [о микросхеме TPM компьютера](about-the-computer-tpm-chip.md).</span><span class="sxs-lookup"><span data-stu-id="f7e6b-123">For more information about the TPM, see [About the Computer TPM Chip](about-the-computer-tpm-chip.md).</span></span>

<span data-ttu-id="f7e6b-124">После того как компьютер защищен BitLocker, вам может потребоваться ввести ПИН-код или пароль при каждом выходе компьютера из спящего режима или с самого начала.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-124">Once your computer is protected by BitLocker, you may have to enter a PIN or password every time that the computer wakes from hibernation or starts.</span></span> <span data-ttu-id="f7e6b-125">Если вы забыли свой ПИН-код или пароль, вы можете помочь службе поддержки компании или организации.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-125">The Help Desk for your company or organization can help if you ever forget your PIN or password.</span></span>

<span data-ttu-id="f7e6b-126">Вы можете отключать BitLocker, временно приостанавливать или постоянно, выполнив расшифровку диска.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-126">You can turn off BitLocker, either temporarily, by suspending it, or permanently, by decrypting the drive.</span></span>

<span data-ttu-id="f7e6b-127">**Примечание**  Поскольку BitLocker шифрует весь диск, а не только отдельные файлы, будьте внимательны при перемещении конфиденциальных данных между дисками.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-127">**Note** Because BitLocker encrypts the whole drive and not just the individual files themselves, be careful when you move sensitive data between drives.</span></span> <span data-ttu-id="f7e6b-128">Если вы перемещаете файл с диска, защищенного BitLocker, на незашифрованный диск, он больше не будет зашифрован.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-128">If you move a file from a BitLocker-protected drive to a nonencrypted drive, the file will no longer be encrypted.</span></span>

 

## <span data-ttu-id="f7e6b-129">О приложении параметров шифрования BitLocker</span><span class="sxs-lookup"><span data-stu-id="f7e6b-129">About the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="f7e6b-130">Чтобы разблокировать жесткие диски на компьютере, а также управлять PIN-кодом и паролями, используйте приложение параметров шифрования BitLocker на панели управления Windows, выполнив описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-130">To unlock hard disk drives on your computer and to manage your PIN and passwords, use the BitLocker Encryption Options application in the Windows Control Panel by following the procedure outlined here.</span></span> <span data-ttu-id="f7e6b-131">Вы можете ввести пароли, чтобы разблокировать защищенные диски и проверить состояние BitLocker подключенных дисков с помощью этого приложения.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-131">You can enter passwords to unlock protected drives and can check the BitLocker status of attached drives by using this application.</span></span>

**<span data-ttu-id="f7e6b-132">Открытие приложения параметров шифрования BitLocker</span><span class="sxs-lookup"><span data-stu-id="f7e6b-132">To open the BitLocker Encryption Options application</span></span>**

1.  <span data-ttu-id="f7e6b-133">Нажмите кнопку **Пуск**и выберите пункт **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-133">Click **Start**, and select **Control Panel**.</span></span> <span data-ttu-id="f7e6b-134">Панель управления откроется в новом окне.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-134">The Control Panel opens in a new window.</span></span>

2.  <span data-ttu-id="f7e6b-135">На **панели управления**выберите элемент **система и безопасность**.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-135">In **Control Panel**, select **System and Security**.</span></span>

3.  <span data-ttu-id="f7e6b-136">Выберите **Параметры шифрования BitLocker** , чтобы открыть приложение параметров шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-136">Select **BitLocker Encryption Options** to open the BitLocker Encryption Options application.</span></span>

    <span data-ttu-id="f7e6b-137">Описание доступных параметров можно найти в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-137">For a description of the available options, see the following section.</span></span>

## <span data-ttu-id="f7e6b-138">Параметры в приложении параметров шифрования BitLocker</span><span class="sxs-lookup"><span data-stu-id="f7e6b-138">Options on the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="f7e6b-139">Приложение "параметры шифрования BitLocker" на панели управления позволяет управлять PIN-кодом и паролями, которые BitLocker использует для защиты компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-139">The BitLocker Encryption Options application on Control Panel lets you manage your PIN and passwords, which BitLocker uses to protect your computer.</span></span>

**<span data-ttu-id="f7e6b-140">Шифрование диска BitLocker — несъемные диски:</span><span class="sxs-lookup"><span data-stu-id="f7e6b-140">BitLocker Drive Encryption – Fixed Disk Drives:</span></span>**

<span data-ttu-id="f7e6b-141">В этом разделе вы можете просмотреть сведения о жестких дисках, подключенных к компьютеру, а также о текущем состоянии шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-141">In this section, you can view information about hard disk drives connected to your computer and their current BitLocker Encryption status.</span></span>

-   <span data-ttu-id="f7e6b-142">**Управление ПИН** -кодом — меняет ПИН-код, используемый BitLocker, для разблокировки диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-142">**Manage your PIN** - changes the PIN used by BitLocker to unlock your operating system drive.</span></span>

-   <span data-ttu-id="f7e6b-143">**Управление паролем** — изменяет пароль, который используется программой BitLocker для разблокировки других внутренних дисков.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-143">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="f7e6b-144">Шифрование диска BitLocker — внешние диски:</span><span class="sxs-lookup"><span data-stu-id="f7e6b-144">BitLocker Drive Encryption - External Drives:</span></span>**

<span data-ttu-id="f7e6b-145">В этом разделе вы можете просмотреть сведения о внешних дисках (например, USB-накопителе, подключенных к компьютеру) и о текущем состоянии шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-145">In this section, you can view information about external drives (such as a USB thumb drive) connected to your computer, and their current BitLocker encryption status.</span></span>

-   <span data-ttu-id="f7e6b-146">**Управление паролем** — изменяет пароль, который используется программой BitLocker для разблокировки других внутренних дисков.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-146">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="f7e6b-147">Дополнительно</span><span class="sxs-lookup"><span data-stu-id="f7e6b-147">Advanced:</span></span>**

-   <span data-ttu-id="f7e6b-148">**Администрирование доверенного платформенного модуля** — открывает средство администрирования TPM в отдельном окне.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-148">**TPM Administration** - opens the TPM Administration tool in a separate window.</span></span> <span data-ttu-id="f7e6b-149">Здесь вы можете настроить общие задачи TPM и получить сведения о наборе микросхем TPM.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-149">From here you can configure common TPM tasks and obtain information about the TPM chipset.</span></span> <span data-ttu-id="f7e6b-150">Чтобы получить доступ к этому средству, необходимо обладать правами администратора на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-150">You must have administrative permissions on your computer to access this tool.</span></span>

-   <span data-ttu-id="f7e6b-151">**Управление дисками** : Откройте средство управления дисками.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-151">**Disk Management** -open the Disk Management tool.</span></span> <span data-ttu-id="f7e6b-152">Здесь вы можете просмотреть сведения обо всех жестких дисках, подключенных к компьютеру, и настроить разделы и параметры диска.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-152">From here you can view the information for all hard drives connected to the computer and configure partitions and drive options.</span></span> <span data-ttu-id="f7e6b-153">Чтобы получить доступ к этому средству, необходимо иметь права администратора на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="f7e6b-153">You must have administrative rights on your computer to access this tool.</span></span>

 

 





