---
title: Администрирование компонентов MBAM 2.0
description: Администрирование компонентов MBAM 2.0
author: dansimp
ms.assetid: 065e0704-069e-4372-9b86-0b57dd7638dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35bb855e185ad8e3fa6880853938074cf6185a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823509"
---
# <span data-ttu-id="5a187-103">Администрирование компонентов MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5a187-103">Administering MBAM 2.0 Features</span></span>


<span data-ttu-id="5a187-104">После того как вы заполните все необходимое планирование, а затем разворачиваете администрирование и мониторинг Microsoft BitLocker (MBAM), вы можете настроить и использовать его для управления шифрованием BitLocker по всему предприятию. в этом разделе описаны повседневные задачи администрирования Microsoft BitLocker и наблюдение за работой функций, выполняемые после установки.</span><span class="sxs-lookup"><span data-stu-id="5a187-104">After completing all necessary planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage BitLocker encryption across the enterprise The information in this section describes post-installation day-to-day Microsoft BitLocker Administration and Monitoring feature operations tasks.</span></span>

## <span data-ttu-id="5a187-105">Управление ролями администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="5a187-105">Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="5a187-106">После завершения настройки MBAM для всех функций сервера пользователи должны будут получить доступ к ним.</span><span class="sxs-lookup"><span data-stu-id="5a187-106">After MBAM Setup is complete for all server features, administrative users have to be granted access to them.</span></span> <span data-ttu-id="5a187-107">Рекомендуется, чтобы администраторы, которые будут управлять или использовать возможности сервера MBAM, были назначены группам безопасности доменных служб Active Directory, а затем эти группы должны быть добавлены в соответствующую административную локальную группу MBAM.</span><span class="sxs-lookup"><span data-stu-id="5a187-107">As a best practice, administrators who will manage or use MBAM server features should be assigned to Active Directory Domain Services security groups, and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

[<span data-ttu-id="5a187-108">Управление ролями администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="5a187-108">How to Manage MBAM Administrator Roles</span></span>](how-to-manage-mbam-administrator-roles-mbam-2.md)

## <span data-ttu-id="5a187-109">Управление исключениями шифрования BitLocker</span><span class="sxs-lookup"><span data-stu-id="5a187-109">Manage BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="5a187-110">MBAM позволяет предоставлять исключения для шифрования определенным пользователям, которые не нуждаются в шифровании и не должны шифровать их диски.</span><span class="sxs-lookup"><span data-stu-id="5a187-110">MBAM lets you grant encryption exemptions to specific users who do not need or want their drives encrypted.</span></span> <span data-ttu-id="5a187-111">Освобождение от компьютера обычно используется в том случае, если в компании есть компьютеры, которые не должны быть зашифрованы, например компьютеры, которые используются при разработке или тестировании, или на более ранних компьютерах, не поддерживающих BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5a187-111">Computer exemption is typically used when a company has computers that do not have to be encrypted, such as computers that are used in development or testing, or older computers that do not support BitLocker.</span></span> <span data-ttu-id="5a187-112">В некоторых случаях местным законодательством также может потребоваться, чтобы определенные компьютеры не шифровались.</span><span class="sxs-lookup"><span data-stu-id="5a187-112">In some cases, local law may also require that certain computers are not encrypted.</span></span>

[<span data-ttu-id="5a187-113">Управление исключениями шифрования BitLocker для пользователя</span><span class="sxs-lookup"><span data-stu-id="5a187-113">How to Manage User BitLocker Encryption Exemptions</span></span>](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)

## <span data-ttu-id="5a187-114">Управление параметрами шифрования BitLocker для клиента MBAM с помощью панели управления</span><span class="sxs-lookup"><span data-stu-id="5a187-114">Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="5a187-115">MBAM — это настраиваемая панель управления, называемая параметрами шифрования BitLocker, которая появится в разделе **система и безопасность**.</span><span class="sxs-lookup"><span data-stu-id="5a187-115">MBAM provides a custom control panel, called BitLocker Encryption Options, that will appear under **System and Security**.</span></span> <span data-ttu-id="5a187-116">Панель управления MBAM можно использовать для разблокировки зашифрованных фиксированных и съемных дисков, а также управлять PIN-кодом или паролем.</span><span class="sxs-lookup"><span data-stu-id="5a187-116">The MBAM control panel can be used to unlock encrypted fixed and removable drives, and also manage your PIN or password.</span></span>

<span data-ttu-id="5a187-117">**Примечание**  Эта настройка панели управления не заменяет стандартную панель управления Windows BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5a187-117">**Note** This customized control panel does not replace the default Windows BitLocker control panel.</span></span>

 

[<span data-ttu-id="5a187-118">Управление параметрами шифрования BitLocker клиента MBAM с помощью панели управления</span><span class="sxs-lookup"><span data-stu-id="5a187-118">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-2.md)

## <span data-ttu-id="5a187-119">Другие ресурсы для администрирования функций MBAM</span><span class="sxs-lookup"><span data-stu-id="5a187-119">Other Resources for Administering MBAM Features</span></span>


[<span data-ttu-id="5a187-120">Операции MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5a187-120">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





