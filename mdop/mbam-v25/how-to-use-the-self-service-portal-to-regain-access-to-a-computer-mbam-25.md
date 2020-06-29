---
title: Восстановление доступа к компьютеру с помощью портала самообслуживания
description: Восстановление доступа к компьютеру с помощью портала самообслуживания
author: dansimp
ms.assetid: 3c24b13a-d1b1-4763-8ac0-0b2db46267e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cde9c71a957a5270d69aa8388455895f1cb2432b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826702"
---
# <span data-ttu-id="2a8c9-103">Восстановление доступа к компьютеру с помощью портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="2a8c9-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="2a8c9-104">Портал самообслуживания — это веб-сайт, который администраторы настраивают в рамках развертывания Microsoft BitLocker для администрирования и мониторинга (MBAM) 2,5.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-104">The Self-Service Portal is a website that IT administrators configure as part of their Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 deployment.</span></span> <span data-ttu-id="2a8c9-105">Этот веб-сайт позволяет конечным пользователям не получать доступ к своим компьютерам независимо от того, насколько они заблокированы для Windows.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-105">The website enables end users to independently regain access to their computers if they get locked out of Windows.</span></span> <span data-ttu-id="2a8c9-106">На портале самообслуживания не требуется помощь сотрудникам службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-106">The Self-Service Portal requires no assistance from Help Desk staff.</span></span>

<span data-ttu-id="2a8c9-107">Указанные ниже инструкции написаны с точки зрения конечных пользователей, но они могут оказаться полезными для понимания ИТ – администраторами.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-107">The following instructions are written from the perspective of end users, but the information may be useful for IT administrators to understand.</span></span>

<span data-ttu-id="2a8c9-108">**Важно!**  Конечный пользователь должен быть физически подключен к компьютеру (не удаленно), хотя бы один раз успешно смог восстановить свой ключ с помощью портала самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-108">**Important** An end user must have physically logged on to the computer (not remotely) at least one time successfully to be able to recover their key using the Self-Service Portal.</span></span> <span data-ttu-id="2a8c9-109">В противном случае они должны использовать портал службы поддержки для восстановления ключей.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-109">Otherwise, they must use the Helpdesk Portal for key recovery.</span></span>

 

<span data-ttu-id="2a8c9-110">Конечные пользователи могут столкнуться с блокировкой в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="2a8c9-110">End users may experience lockouts if they:</span></span>

-   <span data-ttu-id="2a8c9-111">Забыли свой пароль или ПИН-код</span><span class="sxs-lookup"><span data-stu-id="2a8c9-111">Forget their password or PIN</span></span>

-   <span data-ttu-id="2a8c9-112">Изменение файлов операционной системы, BIOS или доверенного платформенного модуля (TPM)</span><span class="sxs-lookup"><span data-stu-id="2a8c9-112">Change operating system files, the BIOS, or the Trusted Platform Module (TPM)</span></span>

<span data-ttu-id="2a8c9-113">**Примечание**  Если администратор настроил состояние сеанса IIS на время ожидания, сообщение отображается в средстве самообслуживания на портале 60 секунд до истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-113">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed in the Self-Service Portal 60 seconds prior to the time-out.</span></span>

 

**<span data-ttu-id="2a8c9-114">Использование портала самообслуживания для восстановления доступа к компьютеру</span><span class="sxs-lookup"><span data-stu-id="2a8c9-114">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="2a8c9-115">В поле **Recovery KeyID (восстановление** ) введите минимум восемь кодов ключа BitLocker, 32 цифр, которые отображаются на экране восстановления BitLocker на компьютере.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-115">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span> <span data-ttu-id="2a8c9-116">Если первые восемь цифр соответствуют нескольким клавишам, появится сообщение, в котором необходимо ввести все 32 цифры идентификатора ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-116">If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

2.  <span data-ttu-id="2a8c9-117">В поле **Reason (причина** ) выберите причину для запроса ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-117">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="2a8c9-118">Нажмите кнопку **получить ключ**.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-118">Click **Get Key**.</span></span> <span data-ttu-id="2a8c9-119">Ключ восстановления BitLocker отображается в поле **ключа восстановления BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="2a8c9-119">Your BitLocker recovery key is displayed in the **Your BitLocker Recovery Key** field.</span></span>

4.  <span data-ttu-id="2a8c9-120">Введите 48-значный код на экран восстановления BitLocker на компьютере, чтобы восстановить доступ к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-120">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>



## <span data-ttu-id="2a8c9-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2a8c9-121">Related topics</span></span>


[<span data-ttu-id="2a8c9-122">Управление BitLocker с помощью MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2a8c9-122">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="2a8c9-123">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="2a8c9-123">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="2a8c9-124">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="2a8c9-124">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="2a8c9-125">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="2a8c9-125">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





