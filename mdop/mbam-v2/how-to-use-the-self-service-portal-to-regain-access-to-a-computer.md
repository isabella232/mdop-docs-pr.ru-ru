---
title: Восстановление доступа к компьютеру с помощью портала самообслуживания
description: Восстановление доступа к компьютеру с помощью портала самообслуживания
author: dansimp
ms.assetid: bcf095de-0237-4bb0-b450-da8fb6d6f3d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4abcffcf35e09bd5e24f4715a38dca74518ba29e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826079"
---
# <span data-ttu-id="8f064-103">Восстановление доступа к компьютеру с помощью портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="8f064-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="8f064-104">Если конечные пользователи будут заблокированы для Windows с помощью BitLocker, так как они забыли пароль или ПИН-код или изменили файлы операционной системы либо изменили BIOS или доверенный ПЛАТФОРМЕНный модуль, они смогут использовать портал самообслуживания для восстановления доступа к Windows без необходимости запрашивать помощь в службе поддержки.</span><span class="sxs-lookup"><span data-stu-id="8f064-104">If end users get locked out of Windows by BitLocker because they forgot their password or PIN, or because they changed operating system files or changed the BIOS or the Trusted Platform Module (TPM), they can use the Self-Service Portal to regain access to Windows without having to ask their Help Desk for assistance.</span></span>

<span data-ttu-id="8f064-105">**Примечание**  Если администратор настроил состояние сеанса IIS на время ожидания, появится 60 секунд до истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="8f064-105">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed 60 seconds prior to the time-out.</span></span>

 

<span data-ttu-id="8f064-106">**Примечание**  Эти инструкции написаны для конечных пользователей и с них в перспективе.</span><span class="sxs-lookup"><span data-stu-id="8f064-106">**Note** These instructions are written for and from the perspective of end users.</span></span>

 

**<span data-ttu-id="8f064-107">Использование портала самообслуживания для восстановления доступа к компьютеру</span><span class="sxs-lookup"><span data-stu-id="8f064-107">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="8f064-108">В поле **Recovery KeyID (восстановление** ) введите минимум восемь кодов ключа BitLocker, 32 цифр, которые отображаются на экране восстановления BitLocker на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8f064-108">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span>

    <span data-ttu-id="8f064-109">**Примечание**  Если первые восемь цифр соответствуют нескольким клавишам, появится сообщение, в котором необходимо ввести все 32 цифры идентификатора ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="8f064-109">**Note** If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

     

2.  <span data-ttu-id="8f064-110">В поле **Reason (причина** ) выберите причину для запроса ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="8f064-110">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="8f064-111">Нажмите кнопку **получить ключ**.</span><span class="sxs-lookup"><span data-stu-id="8f064-111">Click **Get Key**.</span></span> <span data-ttu-id="8f064-112">Ключ восстановления BitLocker отображается в поле "ключ восстановления BitLocker".</span><span class="sxs-lookup"><span data-stu-id="8f064-112">Your BitLocker recovery key is displayed in the “Your BitLocker Recovery Key” field.</span></span>

4.  <span data-ttu-id="8f064-113">Введите 48-значный код на экран восстановления BitLocker на компьютере, чтобы восстановить доступ к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="8f064-113">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>

## <span data-ttu-id="8f064-114">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8f064-114">Related topics</span></span>


[<span data-ttu-id="8f064-115">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="8f064-115">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





