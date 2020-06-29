---
title: Управление параметрами шифрования BitLocker клиента MBAM с помощью панели управления
description: Управление параметрами шифрования BitLocker клиента MBAM с помощью панели управления
author: dansimp
ms.assetid: e2ff153e-5770-4a12-b79d-cda998b8a8ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a42901ac9d8a1a3527712f4cf342b5c0ca9ffdfd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825109"
---
# <span data-ttu-id="34bbb-103">Управление параметрами шифрования BitLocker клиента MBAM с помощью панели управления</span><span class="sxs-lookup"><span data-stu-id="34bbb-103">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="34bbb-104">Приложение панели управления Microsoft BitLocker "Администрирование и мониторинг" (MBAM), именуемое параметрами шифрования BitLocker, будет доступно в разделе " **система и безопасность** " при установленном клиенте администрирования Microsoft BitLocker и клиентском мониторе.</span><span class="sxs-lookup"><span data-stu-id="34bbb-104">A Microsoft BitLocker Administration and Monitoring (MBAM) control panel application, called BitLocker Encryption Options, will be available under **System and Security** when the Microsoft BitLocker Administration and Monitoring Client is installed.</span></span> <span data-ttu-id="34bbb-105">Эта настраиваемая панель управления MBAM является дополнительной панелью управления.</span><span class="sxs-lookup"><span data-stu-id="34bbb-105">This custom MBAM control panel is an additional control panel.</span></span> <span data-ttu-id="34bbb-106">Она не заменяет стандартную панель управления Windows BitLocker.</span><span class="sxs-lookup"><span data-stu-id="34bbb-106">It does not replace the default Windows BitLocker control panel.</span></span> <span data-ttu-id="34bbb-107">Панель управления MBAM можно использовать для разблокировки зашифрованных фиксированных и съемных дисков, а также управлять PIN-кодом или паролем.</span><span class="sxs-lookup"><span data-stu-id="34bbb-107">The MBAM control panel can be used to unlock encrypted fixed and removable drives, and also manage your PIN or password.</span></span> <span data-ttu-id="34bbb-108">Дополнительные сведения о том, как включить панель управления MBAM, приведены в разделе [как скрыть шифрование BitLocker по умолчанию на панели управления Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="34bbb-108">For more information about enabling the MBAM control panel, see [How to Hide Default BitLocker Encryption in the Windows Control Panel](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).</span></span>

**<span data-ttu-id="34bbb-109">Использование панели управления клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="34bbb-109">To use the MBAM Client Control Panel</span></span>**

1.  <span data-ttu-id="34bbb-110">Чтобы открыть параметры шифрования BitLocker, нажмите кнопку **Пуск** и выберите пункт **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="34bbb-110">To open BitLocker Encryption Options, click **Start** and then select **Control Panel**.</span></span> <span data-ttu-id="34bbb-111">В открывшемся диалоговом **панели управления** выберите пункт **система и безопасность**.</span><span class="sxs-lookup"><span data-stu-id="34bbb-111">When **Control Panel** opens, select **System and Security**.</span></span>

2.  <span data-ttu-id="34bbb-112">Дважды щелкните **Параметры шифрования BitLocker** , чтобы открыть настроенную панель управления MBAM.</span><span class="sxs-lookup"><span data-stu-id="34bbb-112">Double-click **BitLocker Encryption Options** to open the customized MBAM control panel.</span></span> <span data-ttu-id="34bbb-113">Вы увидите список всех жестких дисков на компьютере и их состояние шифрования в дополнение к параметру для управления PIN-кодом или паролями.</span><span class="sxs-lookup"><span data-stu-id="34bbb-113">You will see a list of all the hard disk drives on the computer and their encryption status, in addition to an option to manage your PIN or passwords.</span></span>

    <span data-ttu-id="34bbb-114">Список жестких дисков на компьютере можно использовать для проверки состояния шифрования, разблокировки диска или запроса исключения для защиты BitLocker, если политики исключения для пользователей и компьютеров развернуты.</span><span class="sxs-lookup"><span data-stu-id="34bbb-114">The list of hard disk drives on the computer can be used to verify encryption status, unlock a drive, or request an exemption for BitLocker protection if the User and Computer Exemption policies have been deployed.</span></span>

    <span data-ttu-id="34bbb-115">Панель управления "параметры шифрования BitLocker" также позволяет пользователям, не являющимся администраторами, управлять их PIN-кодом и паролями.</span><span class="sxs-lookup"><span data-stu-id="34bbb-115">The BitLocker Encryption Options control panel also allows for non-administrator users to manage their PIN or passwords.</span></span> <span data-ttu-id="34bbb-116">Выбрав пункт **Управление ПИН-кодом**, пользователи будут получать запрос на ввод как текущего, так и нового ПИН-кода (в дополнение к подтверждению нового ПИН-кода).</span><span class="sxs-lookup"><span data-stu-id="34bbb-116">By selecting **Manage PIN**, users are prompted to enter both a current PIN and a new PIN (in addition to confirming the new PIN).</span></span> <span data-ttu-id="34bbb-117">Выбор пункта **Обновить ПИН** -код приведет к сбросу контакта на новый, выбранный пользователем.</span><span class="sxs-lookup"><span data-stu-id="34bbb-117">Selecting **Update PIN** will reset the PIN to the new one that the users selected.</span></span>

    <span data-ttu-id="34bbb-118">Чтобы управлять паролем, выберите **разблокировать диск** и введите текущий пароль.</span><span class="sxs-lookup"><span data-stu-id="34bbb-118">To manage your password, select **Unlock drive** and enter your current password.</span></span> <span data-ttu-id="34bbb-119">Как только диск будет разблокирован, нажмите кнопку **сбросить пароль** , чтобы изменить текущий пароль.</span><span class="sxs-lookup"><span data-stu-id="34bbb-119">As soon as the drive is unlocked, select **Reset Password** to change your current password.</span></span>

## <span data-ttu-id="34bbb-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="34bbb-120">Related topics</span></span>


[<span data-ttu-id="34bbb-121">Администрирование компонентов MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="34bbb-121">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





