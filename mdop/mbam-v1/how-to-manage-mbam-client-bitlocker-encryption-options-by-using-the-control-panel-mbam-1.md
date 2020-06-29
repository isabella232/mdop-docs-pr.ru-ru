---
title: Управление параметрами шифрования BitLocker клиента MBAM с помощью панели управления
description: Управление параметрами шифрования BitLocker клиента MBAM с помощью панели управления
author: dansimp
ms.assetid: c08077e1-5529-468f-9370-c3b33fc258f3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 271147d0e5581f6ce49fe0b46aa83dae6ae4556b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812957"
---
# <span data-ttu-id="5fd52-103">Управление параметрами шифрования BitLocker клиента MBAM с помощью панели управления</span><span class="sxs-lookup"><span data-stu-id="5fd52-103">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="5fd52-104">Приложение панели управления Microsoft BitLocker "Администрирование и мониторинг" (MBAM), именуемое параметрами шифрования BitLocker, будет доступно в разделе " **система и безопасность** ", если установлен клиент MBAM.</span><span class="sxs-lookup"><span data-stu-id="5fd52-104">A Microsoft BitLocker Administration and Monitoring (MBAM) control panel application, called BitLocker Encryption Options, will be available under **System and Security** when the MBAM Client is installed.</span></span> <span data-ttu-id="5fd52-105">Эта настраиваемая панель управления MBAM заменяет стандартную панель управления Windows BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5fd52-105">This customized MBAM control panel replaces the default Windows BitLocker control panel.</span></span> <span data-ttu-id="5fd52-106">Панель управления MBAM позволяет разблокировать зашифрованные диски (стационарные и съемные), а также управлять PIN-кодом или паролем.</span><span class="sxs-lookup"><span data-stu-id="5fd52-106">The MBAM control panel enables you to unlock encrypted drives (fixed and removable), and also helps you manage your PIN or password.</span></span> <span data-ttu-id="5fd52-107">Дополнительные сведения о том, как включить панель управления MBAM, приведены в разделе [как скрыть шифрование BitLocker по умолчанию на панели управления Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).</span><span class="sxs-lookup"><span data-stu-id="5fd52-107">For more information about enabling the MBAM control panel, see [How to Hide Default BitLocker Encryption in The Windows Control Panel](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).</span></span>

<span data-ttu-id="5fd52-108">**Примечание**  Для клиента BitLocker файлы журнала администрирования и операционные журналы находятся в окне просмотра событий, в разделе **журналы приложений и служб**под заголовком  /  **Microsoft**  /  **Windows**  /  **BitLockerManagement**.</span><span class="sxs-lookup"><span data-stu-id="5fd52-108">**Note** For the BitLocker client, the Admin and Operational log files are located in Event Viewer, under **Application and Services Logs** / **Microsoft** / **Windows** / **BitLockerManagement**.</span></span>

 

**<span data-ttu-id="5fd52-109">Использование панели управления клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="5fd52-109">To use the MBAM Client Control Panel</span></span>**

1.  <span data-ttu-id="5fd52-110">Чтобы открыть параметры шифрования BitLocker, нажмите кнопку **Пуск**и выберите пункт **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="5fd52-110">To open BitLocker Encryption Options, click **Start**, and then select **Control Panel**.</span></span> <span data-ttu-id="5fd52-111">В открывшемся диалоговом **панели управления** выберите пункт **система и безопасность**.</span><span class="sxs-lookup"><span data-stu-id="5fd52-111">When **Control Panel** opens, select **System and Security**.</span></span>

2.  <span data-ttu-id="5fd52-112">Дважды щелкните **Параметры шифрования BitLocker** , чтобы открыть настроенную панель управления MBAM.</span><span class="sxs-lookup"><span data-stu-id="5fd52-112">Double-click **BitLocker Encryption Options** to open the customized MBAM control panel.</span></span> <span data-ttu-id="5fd52-113">Вы увидите список всех жестких дисков на компьютере и их состояние шифрования.</span><span class="sxs-lookup"><span data-stu-id="5fd52-113">You will see a list of all the hard disk drives on the computer and their encryption status.</span></span> <span data-ttu-id="5fd52-114">Кроме того, вы увидите параметр для управления PIN-кодом или паролями.</span><span class="sxs-lookup"><span data-stu-id="5fd52-114">You will also see an option to manage your PIN or passwords.</span></span>

3.  <span data-ttu-id="5fd52-115">С помощью списка жестких дисков на компьютере проверьте состояние шифрования, разблокируйте диск или запросите исключение для защиты BitLocker, если вы развернули политики исключения пользователей и компьютеров.</span><span class="sxs-lookup"><span data-stu-id="5fd52-115">Use the list of hard disk drives on the computer to verify the encryption status, unlock a drive, or request an exemption for BitLocker protection if the User and Computer Exemption policies have been deployed.</span></span>

4.  <span data-ttu-id="5fd52-116">Для управления контактами и паролями, не являющимися администраторами, можно использовать панель управления "параметры шифрования BitLocker".</span><span class="sxs-lookup"><span data-stu-id="5fd52-116">Non-administrators can use the BitLocker Encryption Options control panel to manage PINs or passwords.</span></span> <span data-ttu-id="5fd52-117">Пользователь может выбрать пункт **Управление ПИН-кодом,** а затем ввести как текущий, так и новый ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="5fd52-117">A user can select **Manage PIN,** and then enter both a current PIN and a new PIN.</span></span> <span data-ttu-id="5fd52-118">Пользователи также могут подтвердить свой новый ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="5fd52-118">Users can also confirm their new PIN.</span></span> <span data-ttu-id="5fd52-119">Функция **обновления PIN** -кода будет сбрасывать закрепление к новому, выбранному пользователем.</span><span class="sxs-lookup"><span data-stu-id="5fd52-119">The **Update PIN** function will reset the PIN to the new one that the user selects.</span></span>

5.  <span data-ttu-id="5fd52-120">Чтобы управлять паролем, выберите **разблокировать диск** и введите текущий пароль.</span><span class="sxs-lookup"><span data-stu-id="5fd52-120">To manage your password, select **Unlock drive** and enter your current password.</span></span> <span data-ttu-id="5fd52-121">Как только диск будет разблокирован, нажмите кнопку **сбросить пароль** , чтобы изменить текущий пароль.</span><span class="sxs-lookup"><span data-stu-id="5fd52-121">As soon as the drive is unlocked, select **Reset Password** to change your current password.</span></span>

## <span data-ttu-id="5fd52-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5fd52-122">Related topics</span></span>


[<span data-ttu-id="5fd52-123">Администрирование компонентов MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5fd52-123">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





