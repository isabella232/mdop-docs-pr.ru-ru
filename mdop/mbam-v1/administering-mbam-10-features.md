---
title: Администрирование компонентов MBAM 1.0
description: Администрирование компонентов MBAM 1.0
author: dansimp
ms.assetid: dd9a9eff-f1ad-4af3-85d9-c19131a4ad22
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a99ac556227c0f113fb20f3aca32d21c204877b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821222"
---
# <span data-ttu-id="84809-103">Администрирование компонентов MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="84809-103">Administering MBAM 1.0 Features</span></span>


<span data-ttu-id="84809-104">После того как вы закончите все необходимые планирование и развертывание Microsoft BitLocker (MBAM), вы можете настроить и использовать MBAM для управления шифрованием Enterprise BitLocker.</span><span class="sxs-lookup"><span data-stu-id="84809-104">After you complete all necessary Microsoft BitLocker Administration and Monitoring (MBAM) planning and deployment, you can configure and use MBAM to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="84809-105">В этом разделе приведены сведения о действиях, выполняемых после установки MBAMных функций.</span><span class="sxs-lookup"><span data-stu-id="84809-105">The information in this section describes post-installation day-to-day MBAM feature operations tasks.</span></span>

## <span data-ttu-id="84809-106">Управление ролями администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="84809-106">Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="84809-107">После завершения настройки MBAM для всех функций сервера пользователи должны иметь права доступа к этим функциям сервера.</span><span class="sxs-lookup"><span data-stu-id="84809-107">After MBAM Setup is complete for all server features, administrative users must be granted access to these server features.</span></span> <span data-ttu-id="84809-108">Рекомендуется, чтобы администраторы, которые будут управлять и использовать функции сервера MBAM, были назначены группам безопасности Active Directory, а затем эти группы должны быть добавлены в соответствующую административную локальную группу MBAM.</span><span class="sxs-lookup"><span data-stu-id="84809-108">As a best practice, administrators who will manage or use MBAM server features, should be assigned to Active Directory security groups and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

[<span data-ttu-id="84809-109">Управление ролями администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="84809-109">How to Manage MBAM Administrator Roles</span></span>](how-to-manage-mbam-administrator-roles-mbam-1.md)

## <span data-ttu-id="84809-110">Управление совместимостью оборудования</span><span class="sxs-lookup"><span data-stu-id="84809-110">Manage Hardware Compatibility</span></span>


<span data-ttu-id="84809-111">Функция совместимости оборудования MBAM поможет вам убедиться в том, что только оборудование компьютера, которое вы указали в качестве поддержки BitLocker, будет шифроваться.</span><span class="sxs-lookup"><span data-stu-id="84809-111">The MBAM Hardware Compatibility feature can help you to ensure that only the computer hardware that you specify as supporting BitLocker will be encrypted.</span></span> <span data-ttu-id="84809-112">Если эта функция включена, бит \ _admmontla будет шифровать только компьютеры, помеченные как совместимые.</span><span class="sxs-lookup"><span data-stu-id="84809-112">When this feature is turned on, bit\_admmontla will encrypt only computers that are marked as Compatible.</span></span>

<span data-ttu-id="84809-113">**Важно!**  Если эта функция отключена, будут зашифрованы все компьютеры, на которых развернута политика MBAM.</span><span class="sxs-lookup"><span data-stu-id="84809-113">**Important** When this feature is turned off, all computers where the MBAM policy is deployed will be encrypted.</span></span>

 

<span data-ttu-id="84809-114">MBAM может собирать сведения о том, как создавать и моделировать клиентские компьютеры при развертывании групповой политики "разрешить проверку совместимости оборудования".</span><span class="sxs-lookup"><span data-stu-id="84809-114">MBAM can collect information on both the make and model of client computers if you deploy the “Allow Hardware Compatibility Checking” Group Policy.</span></span> <span data-ttu-id="84809-115">Если вы настраиваете этот параметр политики, агент MBAM сообщает сведения о том, что и на компьютере, на сервере MBAM, когда клиент MBAM развертывается на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="84809-115">If you configure this policy, the MBAM agent reports the computer make and model information to the MBAM Server when the MBAM Client is deployed on a client computer.</span></span>

[<span data-ttu-id="84809-116">Управление совместимостью оборудования</span><span class="sxs-lookup"><span data-stu-id="84809-116">How to Manage Hardware Compatibility</span></span>](how-to-manage-hardware-compatibility-mbam-1.md)

[<span data-ttu-id="84809-117">Управление исключениями шифрования BitLocker для пользователя</span><span class="sxs-lookup"><span data-stu-id="84809-117">How to Manage User BitLocker Encryption Exemptions</span></span>](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)

## <span data-ttu-id="84809-118">Управление исключениями шифрования BitLocker</span><span class="sxs-lookup"><span data-stu-id="84809-118">Manage BitLocker encryption exemptions</span></span>


<span data-ttu-id="84809-119">MBAM может предоставлять два вида исключений из шифрования BitLocker: исключение компьютера и освобождение от пользователя.</span><span class="sxs-lookup"><span data-stu-id="84809-119">MBAM can grant two forms of exemption from BitLocker encryption: computer exemption and user exemption.</span></span> <span data-ttu-id="84809-120">Освобождение от компьютера обычно используется в том случае, если в компании есть компьютеры, которые не должны быть зашифрованы, например компьютеры, которые используются при разработке или тестировании, или на более ранних компьютерах, не поддерживающих BitLocker.</span><span class="sxs-lookup"><span data-stu-id="84809-120">Computer exemption is typically used when a company has computers that do not have to be encrypted, such as computers that are used in development or testing, or older computers that do not support BitLocker.</span></span> <span data-ttu-id="84809-121">В некоторых случаях местным законодательством также может потребоваться, чтобы определенные компьютеры не шифровались.</span><span class="sxs-lookup"><span data-stu-id="84809-121">In some cases, local law may also require that certain computers are not encrypted.</span></span> <span data-ttu-id="84809-122">Кроме того, вы можете исключить пользователей, которые не нуждаются в шифровании и не хотят, чтобы их диски были зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="84809-122">You may also choose to exempt users who do not need or want their drives encrypted.</span></span>

[<span data-ttu-id="84809-123">Управление исключениями шифрования BitLocker для компьютера</span><span class="sxs-lookup"><span data-stu-id="84809-123">How to Manage Computer BitLocker Encryption Exemptions</span></span>](how-to-manage-computer-bitlocker-encryption-exemptions.md)

## <span data-ttu-id="84809-124">Управление параметрами шифрования BitLocker для клиента MBAM с помощью панели управления</span><span class="sxs-lookup"><span data-stu-id="84809-124">Manage MBAM Client BitLocker Encryption Options by using the Control Panel</span></span>


<span data-ttu-id="84809-125">Если эта возможность включена с помощью объектов групповой политики (GPO), в разделе **система и безопасность**будут доступны пользовательские панели управления MBAM с именем параметры шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="84809-125">If enabled through a Group Policy Objects (GPO), a custom MBAM control panel that is named BitLocker Encryption Options will be available under **System and Security**.</span></span> <span data-ttu-id="84809-126">Эта настройка панели управления заменяет стандартную панель управления Windows BitLocker.</span><span class="sxs-lookup"><span data-stu-id="84809-126">This customized control panel replaces the default Windows BitLocker control panel.</span></span> <span data-ttu-id="84809-127">Панель управления MBAM позволяет разблокировать зашифрованные диски (стационарные и съемные), а также управлять PIN-кодом или паролем.</span><span class="sxs-lookup"><span data-stu-id="84809-127">The MBAM control panel enables you to unlock encrypted drives (fixed and removable), and also helps you manage your PIN or password.</span></span>

[<span data-ttu-id="84809-128">Управление параметрами шифрования BitLocker клиента MBAM с помощью панели управления</span><span class="sxs-lookup"><span data-stu-id="84809-128">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-1.md)

## <span data-ttu-id="84809-129">Другие ресурсы для администрирования функций MBAM</span><span class="sxs-lookup"><span data-stu-id="84809-129">Other resources for Administering MBAM features</span></span>


[<span data-ttu-id="84809-130">Операции MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="84809-130">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





