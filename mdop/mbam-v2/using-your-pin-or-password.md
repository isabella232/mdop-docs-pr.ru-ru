---
title: Использование PIN-кода или пароля
description: Использование PIN-кода или пароля
author: dansimp
ms.assetid: 7fe2aef4-d3e0-49c8-877d-7fee13dc5b7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8c4b894b8f3e14d2a5cfb39e744fa43874c6753
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823792"
---
# <span data-ttu-id="4b302-103">Использование PIN-кода или пароля</span><span class="sxs-lookup"><span data-stu-id="4b302-103">Using Your PIN or Password</span></span>


<span data-ttu-id="4b302-104">BitLocker помогает защитить компьютер, если требуется персональный идентификационный номер (ПИН-код) или пароль, чтобы разблокировать данные, хранящиеся на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4b302-104">BitLocker helps secure your computer by requiring a personal identification number (PIN) or password to unlock the information that is stored on your computer.</span></span> <span data-ttu-id="4b302-105">Требования к ПИН-коду или паролю задаются вашей организацией и зависят от типа диска, на котором производится шифрование.</span><span class="sxs-lookup"><span data-stu-id="4b302-105">The PIN or password requirements are set by your organization and depend on the kind of drive being encrypted.</span></span> <span data-ttu-id="4b302-106">Данные на зашифрованных дисках нельзя просматривать без ввода PIN-кода или пароля.</span><span class="sxs-lookup"><span data-stu-id="4b302-106">Data on the encrypted drives cannot be viewed without entering the PIN or password.</span></span> <span data-ttu-id="4b302-107">Если на вашем компьютере используется включенный доверенный платформенный модуль, перед запуском Windows на компьютере будет предложено ввести ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="4b302-107">If your computer hardware includes an enabled Trusted Platform Module (TPM), the TPM chip prompts you for your PIN before Windows starts on your computer.</span></span>

## <span data-ttu-id="4b302-108">О ПИН-коде BitLocker и паролях</span><span class="sxs-lookup"><span data-stu-id="4b302-108">About Your BitLocker PIN and Passwords</span></span>


<span data-ttu-id="4b302-109">Ваша организация определяет сложность, требуемую для ПИН-кода или пароля.</span><span class="sxs-lookup"><span data-stu-id="4b302-109">Your company specifies the complexity required for your PIN or password.</span></span> <span data-ttu-id="4b302-110">Эти требования для ПИН-кода или пароля описаны в процессе настройки BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4b302-110">These requirements for your PIN or password are explained during the BitLocker setup process.</span></span>

<span data-ttu-id="4b302-111">Пароль используется для разблокировки дисков на компьютере, не содержащих операционную систему.</span><span class="sxs-lookup"><span data-stu-id="4b302-111">The password is used to unlock drives on your computer that do not contain the operating system.</span></span> <span data-ttu-id="4b302-112">BitLocker запросит пароль после запроса ПИН-кода во время запуска.</span><span class="sxs-lookup"><span data-stu-id="4b302-112">BitLocker will ask for your password after the PIN is requested during startup.</span></span> <span data-ttu-id="4b302-113">Каждому жесткому диску, защищенному BitLocker на компьютере, назначен собственный уникальный пароль.</span><span class="sxs-lookup"><span data-stu-id="4b302-113">Each BitLocker protected hard disk on your computer has its own unique password.</span></span> <span data-ttu-id="4b302-114">Разблокировать диск, защищенный BitLocker, невозможно, пока вы не задаете пароль.</span><span class="sxs-lookup"><span data-stu-id="4b302-114">You cannot unlock a BitLocker protected drive until you provide your password.</span></span>

<span data-ttu-id="4b302-115">**Примечание**  В службе поддержки может быть настроено автоматическое снятие блокировки дисков.</span><span class="sxs-lookup"><span data-stu-id="4b302-115">**Note** Your Help Desk may set drives to unlock automatically.</span></span> <span data-ttu-id="4b302-116">Это избавляет от необходимости вводить PIN-код или пароль для просмотра информации на дисках.</span><span class="sxs-lookup"><span data-stu-id="4b302-116">This eliminates the need to provide a PIN or password to view the information on the drives.</span></span>

 

## <span data-ttu-id="4b302-117">Снятие блокировки компьютера в случае, если вы забыли свой ПИН-код или пароль</span><span class="sxs-lookup"><span data-stu-id="4b302-117">Unlocking Your Computer if You Forget Your PIN or Password</span></span>


<span data-ttu-id="4b302-118">Если вы забыли свой ПИН-код или пароль, вы можете воспользоваться службой поддержки, чтобы разблокировать диски, защищенные с помощью BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4b302-118">If you forget your PIN or password, your Help Desk can help you unlock BitLocker protected drives.</span></span> <span data-ttu-id="4b302-119">Чтобы разблокировать диск, защищенный BitLocker, обратитесь в службу поддержки, если вам нужна помощь.</span><span class="sxs-lookup"><span data-stu-id="4b302-119">To unlock a drive protected with BitLocker, contact your Help Desk if you need help.</span></span>

**<span data-ttu-id="4b302-120">Как разблокировать компьютер, если вы забыли свой ПИН-код или пароль</span><span class="sxs-lookup"><span data-stu-id="4b302-120">How to unlock your computer if you forget your PIN or password</span></span>**

1.  <span data-ttu-id="4b302-121">При обращении в службу поддержки вам потребуется указать следующие данные:</span><span class="sxs-lookup"><span data-stu-id="4b302-121">When you contact your Help Desk, you will need to provide them with the following information:</span></span>

    -   <span data-ttu-id="4b302-122">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="4b302-122">Your user name</span></span>

    -   <span data-ttu-id="4b302-123">Ваш домен</span><span class="sxs-lookup"><span data-stu-id="4b302-123">Your domain</span></span>

    -   <span data-ttu-id="4b302-124">Первые восемь цифр идентификатора ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="4b302-124">The first eight digits of your recovery key ID.</span></span> <span data-ttu-id="4b302-125">Это 32-значный код, который будет отображаться в BitLocker, если вы забыли свой ПИН-код или пароль.</span><span class="sxs-lookup"><span data-stu-id="4b302-125">This is a 32-digit code that BitLocker will display if you forget your PIN or password.</span></span>

        -   <span data-ttu-id="4b302-126">Если вы забыли свой ПИН-код, вы должны ввести первые восемь цифр идентификатора ключа восстановления, который будет отображаться в консоли восстановления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4b302-126">If you forget your PIN, you will have to enter the first eight digits of the recovery key ID, which will appear in the BitLocker Recovery console.</span></span> <span data-ttu-id="4b302-127">Консоль восстановления BitLocker — это экран предварительного экрана, который будет отображаться, если ПИН-код не введен правильно.</span><span class="sxs-lookup"><span data-stu-id="4b302-127">The BitLocker Recovery console is a pre-Windows screen that will be displayed if you do not enter the correct PIN.</span></span>

        -   <span data-ttu-id="4b302-128">Если вы забыли свой пароль, найдите его с помощью идентификатора ключа восстановления в приложении панели управления "параметры шифрования BitLocker".</span><span class="sxs-lookup"><span data-stu-id="4b302-128">If you forget your password, look for the recovery key ID in the BitLocker Encryption Options Control Panel application.</span></span> <span data-ttu-id="4b302-129">Выберите **разблокировать диск** и щелкните **я не могу запомнить пароль**.</span><span class="sxs-lookup"><span data-stu-id="4b302-129">Select **Unlock Drive** and then click **I cannot remember my password**.</span></span> <span data-ttu-id="4b302-130">Затем приложение параметров шифрования BitLocker выведет идентификатор ключа восстановления, который вы предоставляете в службу технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="4b302-130">The BitLocker Encryption Options application will then display a recovery key ID that you provide to Help Desk.</span></span>

2.  <span data-ttu-id="4b302-131">После получения службой поддержки необходимой информации она предоставит вам ключ восстановления на телефоне или по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="4b302-131">Once your Help Desk receives the necessary information, it will provide you with a recovery key over the phone or through e-mail.</span></span>

    -   <span data-ttu-id="4b302-132">Если вы забыли свой ПИН-код, введите ключ восстановления на консоли восстановления BitLocker, чтобы разблокировать компьютер.</span><span class="sxs-lookup"><span data-stu-id="4b302-132">If you forgot your PIN, enter the recovery key in the BitLocker Recovery console to unlock your computer.</span></span>

    -   <span data-ttu-id="4b302-133">Если вы забыли свой пароль, введите его в том же расположении, в котором вы нашли код ключа восстановления, в разделе Параметры шифрования BitLocker в приложении панели управления.</span><span class="sxs-lookup"><span data-stu-id="4b302-133">If you forgot your password, enter the recovery key in the BitLocker Encryption Options Control Panel application, in the same location where you found the recovery key ID earlier.</span></span> <span data-ttu-id="4b302-134">Это заблокирует защищенный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="4b302-134">This will unlock the protected hard drive.</span></span>

## <span data-ttu-id="4b302-135">Изменение ПИН-кода или пароля</span><span class="sxs-lookup"><span data-stu-id="4b302-135">Changing your PIN or Password</span></span>


<span data-ttu-id="4b302-136">Прежде чем вы сможете изменить пароль на диске, защищенном с помощью BitLocker, необходимо разблокировать диск.</span><span class="sxs-lookup"><span data-stu-id="4b302-136">Before you can change the password on a BitLocker protected drive, you must unlock the drive.</span></span> <span data-ttu-id="4b302-137">Если диск не разблокирован, выберите **разблокировать диск**и введите текущий пароль.</span><span class="sxs-lookup"><span data-stu-id="4b302-137">If the drive is not unlocked, select **Unlock Drive**, and then enter your current password.</span></span> <span data-ttu-id="4b302-138">Как только диск разблокируется, вы можете выбрать **Управление паролем** , чтобы изменить текущий пароль.</span><span class="sxs-lookup"><span data-stu-id="4b302-138">As soon as the drive is unlocked, you can select **Manage your Password** to change your current password.</span></span>

**<span data-ttu-id="4b302-139">Как изменить ПИН-код или пароль</span><span class="sxs-lookup"><span data-stu-id="4b302-139">How to Change your PIN or password</span></span>**

1.  <span data-ttu-id="4b302-140">Нажмите кнопку **Пуск**и выберите пункт **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="4b302-140">Click **Start**, and then select **Control Panel**.</span></span> <span data-ttu-id="4b302-141">В новом окне откроется панель управления.</span><span class="sxs-lookup"><span data-stu-id="4b302-141">Control Panel opens in a new window.</span></span>

2.  <span data-ttu-id="4b302-142">Выберите пункт **система и безопасность**, а затем — пункт **Параметры шифрования BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="4b302-142">Select **System and Security**, and then select **BitLocker Encryption Options**.</span></span>

    -   <span data-ttu-id="4b302-143">Чтобы изменить ПИН-код, выберите пункт **Управление PIN-кодом**.</span><span class="sxs-lookup"><span data-stu-id="4b302-143">To change your PIN, select **Manage Your PIN**.</span></span> <span data-ttu-id="4b302-144">Введите новый ПИН-код в оба поля и нажмите кнопку **сбросить PIN-код**.</span><span class="sxs-lookup"><span data-stu-id="4b302-144">Type your new PIN into both fields and select **Reset PIN**.</span></span>

    -   <span data-ttu-id="4b302-145">Чтобы изменить пароль, выберите " **Управление паролем**".</span><span class="sxs-lookup"><span data-stu-id="4b302-145">To change your password, select **Manage Your Password**.</span></span> <span data-ttu-id="4b302-146">Введите новый пароль в оба поля и нажмите кнопку **сбросить пароль**.</span><span class="sxs-lookup"><span data-stu-id="4b302-146">Enter your new password into both fields and select **Reset Password**.</span></span>

 

 





