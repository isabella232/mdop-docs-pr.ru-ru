---
title: Администрирование компонентов MBAM 2.5
description: Администрирование компонентов MBAM 2.5
author: dansimp
ms.assetid: ca15f818-cf07-4437-8ffa-425af603a3c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a365442c11479563d43159e6ef9859c252ce28b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824199"
---
# <span data-ttu-id="904dc-103">Администрирование компонентов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="904dc-103">Administering MBAM 2.5 Features</span></span>


<span data-ttu-id="904dc-104">После того как вы заполните все необходимое планирование, а затем разворачиваете администрирование и мониторинг Microsoft BitLocker (MBAM), вы можете настроить и использовать его для управления шифрованием BitLocker по всему предприятию. в этом разделе описаны повседневные задачи администрирования Microsoft BitLocker и наблюдение за работой функций, выполняемые после установки.</span><span class="sxs-lookup"><span data-stu-id="904dc-104">After completing all necessary planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage BitLocker encryption across the enterprise The information in this section describes post-installation day-to-day Microsoft BitLocker Administration and Monitoring feature operations tasks.</span></span>

## <span data-ttu-id="904dc-105">Управление исключениями шифрования BitLocker</span><span class="sxs-lookup"><span data-stu-id="904dc-105">Manage BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="904dc-106">MBAM позволяет предоставлять исключения для шифрования определенным пользователям, которые не нуждаются в шифровании и не должны шифровать их диски.</span><span class="sxs-lookup"><span data-stu-id="904dc-106">MBAM lets you grant encryption exemptions to specific users who do not need or want their drives encrypted.</span></span> <span data-ttu-id="904dc-107">Освобождение от компьютера обычно используется в том случае, если в компании есть компьютеры, которые не должны быть зашифрованы, например компьютеры, которые используются при разработке или тестировании, или на более ранних компьютерах, не поддерживающих BitLocker.</span><span class="sxs-lookup"><span data-stu-id="904dc-107">Computer exemption is typically used when a company has computers that do not have to be encrypted, such as computers that are used in development or testing, or older computers that do not support BitLocker.</span></span> <span data-ttu-id="904dc-108">В некоторых случаях местным законодательством также может потребоваться, чтобы определенные компьютеры не шифровались.</span><span class="sxs-lookup"><span data-stu-id="904dc-108">In some cases, local law may also require that certain computers are not encrypted.</span></span>

[<span data-ttu-id="904dc-109">Управление исключениями шифрования BitLocker для пользователя</span><span class="sxs-lookup"><span data-stu-id="904dc-109">How to Manage User BitLocker Encryption Exemptions</span></span>](how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md)

## <span data-ttu-id="904dc-110">Общие сведения о параметрах шифрования BitLocker и элементах шифрования диска BitLocker на панели управления</span><span class="sxs-lookup"><span data-stu-id="904dc-110">Understand the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel</span></span>


<span data-ttu-id="904dc-111">MBAM — это настраиваемая панель управления, называемая параметрами шифрования BitLocker, которая отображается в разделе **система и безопасность**.</span><span class="sxs-lookup"><span data-stu-id="904dc-111">MBAM provides a custom control panel, called BitLocker Encryption Options, that appears under **System and Security**.</span></span> <span data-ttu-id="904dc-112">Панель управления MBAM можно использовать для разблокировки зашифрованных фиксированных и съемных дисков, а также управлять PIN-кодом или паролем.</span><span class="sxs-lookup"><span data-stu-id="904dc-112">The MBAM control panel can be used to unlock encrypted fixed and removable drives, and also manage your PIN or password.</span></span>

<span data-ttu-id="904dc-113">**Примечание**  Эта настройка панели управления не заменяет стандартную панель управления Windows BitLocker.</span><span class="sxs-lookup"><span data-stu-id="904dc-113">**Note** This customized control panel does not replace the default Windows BitLocker control panel.</span></span>

 

[<span data-ttu-id="904dc-114">Общие сведения о параметрах шифрования BitLocker и шифровании дисков BitLocker в панели управления</span><span class="sxs-lookup"><span data-stu-id="904dc-114">Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel</span></span>](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

## <span data-ttu-id="904dc-115">Другие ресурсы для администрирования функций MBAM</span><span class="sxs-lookup"><span data-stu-id="904dc-115">Other Resources for Administering MBAM Features</span></span>


[<span data-ttu-id="904dc-116">Операции MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="904dc-116">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)

## <span data-ttu-id="904dc-117">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="904dc-117">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="904dc-118">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="904dc-118">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="904dc-119">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="904dc-119">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





