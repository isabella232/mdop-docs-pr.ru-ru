---
title: Сведения о микросхеме доверенного платформенного модуля компьютера
description: Сведения о микросхеме доверенного платформенного модуля компьютера
author: dansimp
ms.assetid: 6f1cf18c-277a-4932-886d-14202ca8d175
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6df54dc8085c398bacc508fdbbb79a30b0e4204
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823532"
---
# <span data-ttu-id="15592-103">Сведения о микросхеме доверенного платформенного модуля компьютера</span><span class="sxs-lookup"><span data-stu-id="15592-103">About the Computer TPM Chip</span></span>


<span data-ttu-id="15592-104">BitLocker обеспечивает дополнительную защиту при использовании с микросхемой доверенного платформенного модуля (TPM).</span><span class="sxs-lookup"><span data-stu-id="15592-104">BitLocker provides additional protection when it is used with a Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="15592-105">Микросхема доверенного платформенного модуля — это аппаратный компонент, устанавливаемый на многих современных компьютерах производителем компьютера.</span><span class="sxs-lookup"><span data-stu-id="15592-105">The TPM chip is a hardware component that is installed in many newer computers by the computer manufacturers.</span></span> <span data-ttu-id="15592-106">Администрирование и мониторинг Microsoft BitLocker (MBAM) использует BitLocker в дополнение к микросхеме доверенного платформенного модуля, чтобы обеспечить дополнительную защиту данных и убедиться, что ваш компьютер не был изменен.</span><span class="sxs-lookup"><span data-stu-id="15592-106">Microsoft BitLocker Administration and Monitoring (MBAM) uses BitLocker, in addition to the TPM chip, to help provide additional protection of your data and to make sure that your computer has not been tampered with.</span></span>

## <span data-ttu-id="15592-107">Настройка доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="15592-107">How to Set Up Your TPM</span></span>


<span data-ttu-id="15592-108">Когда вы запускаете мастер шифрования диска BitLocker на своем компьютере, BitLocker проверяет наличие микросхемы TPM, если в вашей организации настроена функция BitLocker для использования микросхемы TPM.</span><span class="sxs-lookup"><span data-stu-id="15592-108">When you start the BitLocker Drive Encryption wizard on your computer, BitLocker checks for a TPM chip if your organization has configured BitLocker to use a TPM chip.</span></span> <span data-ttu-id="15592-109">Если BitLocker находит совместимую микросхему доверенного платформенного модуля, вам может быть предложено перезагрузить компьютер, чтобы включить микросхему TPM для использования.</span><span class="sxs-lookup"><span data-stu-id="15592-109">If BitLocker finds a compatible TPM chip, you may be prompted to restart your computer to enable the TPM chip for use.</span></span> <span data-ttu-id="15592-110">После перезапуска компьютера следуйте инструкциям по настройке микросхемы TPM в BIOS (BIOS — это предварительная версия программного обеспечения вашего компьютера).</span><span class="sxs-lookup"><span data-stu-id="15592-110">As soon as your computer has restarted, follow the instructions to configure the TPM chip in the BIOS (the BIOS is a pre-Windows layer of your computer software).</span></span>

<span data-ttu-id="15592-111">После настройки BitLocker вы можете получить доступ к дополнительным сведениям о микросхеме доверенного платформенного модуля, открыв средство "параметры шифрования BitLocker" на панели управления Windows, а затем выбрав **Администрирование TPM**.</span><span class="sxs-lookup"><span data-stu-id="15592-111">After BitLocker is configured, you can access additional information about the TPM chip by opening the BitLocker Encryption Options tool in the Windows Control Panel, and then selecting **TPM Administration**.</span></span>

<span data-ttu-id="15592-112">**Примечание**  Чтобы получить доступ к этому средству, необходимо обладать правами администратора на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="15592-112">**Note** You must have administrative credentials on your computer to access this tool.</span></span>

 

<span data-ttu-id="15592-113">В случае сбоя доверенного платформенного модуля, изменения в BIOS или некоторых обновлений Windows BitLocker заблокирует компьютер и потребует обратиться в службу поддержки, чтобы разблокировать ее.</span><span class="sxs-lookup"><span data-stu-id="15592-113">In a TPM failure, a change in the BIOS, or certain Windows Updates, BitLocker will lock your computer and require you to contact your Help Desk to unlock it.</span></span> <span data-ttu-id="15592-114">Вам необходимо предоставить имя компьютера и домен компьютера.</span><span class="sxs-lookup"><span data-stu-id="15592-114">You have to provide the name of your computer as well as your computer’s domain.</span></span> <span data-ttu-id="15592-115">Службы поддержки могут предоставить вам файл пароля, который можно использовать для разблокировки компьютера.</span><span class="sxs-lookup"><span data-stu-id="15592-115">Help Desk can give you a password file that can be used to unlock your computer.</span></span>

## <span data-ttu-id="15592-116">Устранение проблем с TPM</span><span class="sxs-lookup"><span data-stu-id="15592-116">Troubleshooting TPM Issues</span></span>


<span data-ttu-id="15592-117">Если произошел сбой TPM, изменить BIOS или некоторые обновления Windows, BitLocker заблокирует компьютер и попросит вас обратиться в службу поддержки, чтобы разблокировать ее.</span><span class="sxs-lookup"><span data-stu-id="15592-117">If a TPM failure, change in the BIOS, or certain Windows Updates occur, BitLocker will lock your computer and require you to contact your Help Desk to unlock it.</span></span> <span data-ttu-id="15592-118">Вам необходимо предоставить имя компьютера и домен компьютера.</span><span class="sxs-lookup"><span data-stu-id="15592-118">You have to provide the name of your computer as well as your computer’s domain.</span></span> <span data-ttu-id="15592-119">В службе поддержки может быть предоставлен файл пароля, который можно использовать для разблокировки компьютера.</span><span class="sxs-lookup"><span data-stu-id="15592-119">The Help Desk can give you a password file that you can use to unlock your computer.</span></span>

## <span data-ttu-id="15592-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="15592-120">Related topics</span></span>


[<span data-ttu-id="15592-121">Помощь конечным пользователям в управлении BitLocker</span><span class="sxs-lookup"><span data-stu-id="15592-121">Helping End Users Manage BitLocker</span></span>](helping-end-users-manage-bitlocker.md)

[<span data-ttu-id="15592-122">Использование PIN-кода или пароля</span><span class="sxs-lookup"><span data-stu-id="15592-122">Using Your PIN or Password</span></span>](using-your-pin-or-password.md)

 

 





