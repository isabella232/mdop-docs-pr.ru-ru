---
title: Управление исключениями шифрования BitLocker для пользователя
description: Управление исключениями шифрования BitLocker для пользователя
author: dansimp
ms.assetid: 1bfd9d66-6a9a-4d0e-b54a-e5a6627f5ada
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d5530701fd208d42dc1f6774fac11ee9ca2036b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825072"
---
# <span data-ttu-id="37a5d-103">Управление исключениями шифрования BitLocker для пользователя</span><span class="sxs-lookup"><span data-stu-id="37a5d-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="37a5d-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) можно использовать для управления защитой BitLocker путем исключения пользователей, которые не нуждаются в шифровании и не требуют шифрования своих дисков.</span><span class="sxs-lookup"><span data-stu-id="37a5d-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users if there are users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="37a5d-105">Чтобы исключить пользователей из системы защиты BitLocker, организациям потребуется создать инфраструктуру для поддержки исключенных пользователей, например предоставить пользователю номер телефона, веб-страницу или почтовый адрес, которые будут использоваться для запроса освобождения.</span><span class="sxs-lookup"><span data-stu-id="37a5d-105">To exempt users from BitLocker protection, an organization will have to create an infrastructure to support exempted users, such as giving the user a contact telephone number, webpage, or mailing address to use to request an exemption.</span></span> <span data-ttu-id="37a5d-106">Кроме того, исключенный пользователь должен быть добавлен в группу безопасности для объекта групповой политики, созданного специально для исключенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="37a5d-106">Also, an exempt user will have to be added to a security group for a Group Policy Object that was created specifically for exempted users.</span></span> <span data-ttu-id="37a5d-107">Когда участники этой группы безопасности входят на компьютер, параметр групповой политики пользователя показывает, что пользователь исключен из системы защиты BitLocker.</span><span class="sxs-lookup"><span data-stu-id="37a5d-107">When members of this security group log on to a computer, the user’s Group Policy setting shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="37a5d-108">Параметр групповой политики пользователя перезапишет политику компьютера, и компьютер останется без шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="37a5d-108">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="37a5d-109">**Примечание**  Если на компьютере уже установлена защита с помощью BitLocker, политика исключения пользователя не действует.</span><span class="sxs-lookup"><span data-stu-id="37a5d-109">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="37a5d-110">В следующей таблице показано, как применяется защита BitLocker в зависимости от того, как устанавливаются исключения.</span><span class="sxs-lookup"><span data-stu-id="37a5d-110">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="37a5d-111">Состояние пользователя</span><span class="sxs-lookup"><span data-stu-id="37a5d-111">User Status</span></span></th>
<th align="left"><span data-ttu-id="37a5d-112">Компьютер не исключен</span><span class="sxs-lookup"><span data-stu-id="37a5d-112">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="37a5d-113">Освобождение от компьютера</span><span class="sxs-lookup"><span data-stu-id="37a5d-113">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="37a5d-114">Пользователь не исключен</span><span class="sxs-lookup"><span data-stu-id="37a5d-114">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="37a5d-115">Защита BitLocker принудительно применяется на компьютере.</span><span class="sxs-lookup"><span data-stu-id="37a5d-115">BitLocker protection is enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a5d-116">Защита BitLocker не применяется принудительно на компьютере</span><span class="sxs-lookup"><span data-stu-id="37a5d-116">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="37a5d-117">Освобождение от пользователя</span><span class="sxs-lookup"><span data-stu-id="37a5d-117">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="37a5d-118">Защита BitLocker не применяется принудительно на компьютере</span><span class="sxs-lookup"><span data-stu-id="37a5d-118">BitLocker protection is not enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a5d-119">Защита BitLocker не применяется принудительно на компьютере</span><span class="sxs-lookup"><span data-stu-id="37a5d-119">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="37a5d-120">Исключение пользователя из шифрования BitLocker</span><span class="sxs-lookup"><span data-stu-id="37a5d-120">To exempt a user from BitLocker encryption</span></span>**

1.  <span data-ttu-id="37a5d-121">Создайте группу безопасности ActiveDirectoryDomainServices, которая будет использоваться для управления исключениями пользователей из требований шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="37a5d-121">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="37a5d-122">Создайте параметр групповой политики с помощью шаблона групповой политики администрирования и мониторинга Microsoft BitLocker и свяжите его с группой Active Directory, созданной на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="37a5d-122">Create a Group Policy Object setting by using the Microsoft BitLocker Administration and Monitoring Group Policy template and associate it with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="37a5d-123">Параметры политики для исключения пользователей можно найти в разделе **UserConfiguration\\Administrative Templates\\Windows COMPONENTS\\MDOP MBAM (Управление BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="37a5d-123">The policy settings to exempt users can be found under **UserConfiguration\\Administrative Templates\\Windows Components\\MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="37a5d-124">После создания группы безопасности для пользователей, исключенных с помощью BitLocker, добавьте в эту группу имена пользователей, которые запрашивают исключение.</span><span class="sxs-lookup"><span data-stu-id="37a5d-124">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting an exemption.</span></span> <span data-ttu-id="37a5d-125">Когда пользователи входят на компьютер, управляемый BitLocker, клиент MBAM проверит параметр политики исключения пользователей и приостановит защиту в зависимости от того, входит ли пользователь в группу безопасности исключений BitLocker.</span><span class="sxs-lookup"><span data-stu-id="37a5d-125">When users log on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="37a5d-126">**Важно!**  Сценарии для общего компьютера требуют особой важности при использовании исключений пользователей.</span><span class="sxs-lookup"><span data-stu-id="37a5d-126">**Important** Shared computer scenarios require special consideration when using user exemptions.</span></span> <span data-ttu-id="37a5d-127">Если пользователь без исключения входит в систему на компьютере, к которому предоставлен общий доступ, компьютер может быть зашифрован.</span><span class="sxs-lookup"><span data-stu-id="37a5d-127">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="37a5d-128">Разрешение пользователям запрашивать исключение из шифрования BitLocker</span><span class="sxs-lookup"><span data-stu-id="37a5d-128">To enable users to request an exemption from BitLocker encryption</span></span>**

1.  <span data-ttu-id="37a5d-129">Если вы настроили политики освобождения от пользователей с помощью шаблона политики MBAM, пользователь может запросить исключение из системы защиты BitLocker с помощью клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a5d-129">If you have configured user exemption policies by using the MBAM policy template, a user can request an exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="37a5d-130">При входе пользователей на компьютер, для которого требуется шифрование, они получают уведомление о том, что их компьютеры будут зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="37a5d-130">When users log on to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="37a5d-131">Они могут выбрать **исключение запросов** и отложить шифрование, выбрав параметр **позже**, или нажмите кнопку **начать** , чтобы сохранить шифрование BitLocker.</span><span class="sxs-lookup"><span data-stu-id="37a5d-131">They can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="37a5d-132">**Примечание**  Выбор **исключения** откладывает защиту BitLocker, пока не будет задано максимальное значение, заданное в политике исключения пользователей.</span><span class="sxs-lookup"><span data-stu-id="37a5d-132">**Note** Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="37a5d-133">Если пользователь выберет **исключение запросов**, он получит уведомление о том, что они будут обращаться к группе администрирования BitLocker своей организации.</span><span class="sxs-lookup"><span data-stu-id="37a5d-133">If users select **Request Exemption**, they receive a notification telling them to contact your organization’s BitLocker administration group.</span></span> <span data-ttu-id="37a5d-134">В зависимости от того, как настроена Настройка политики исключения пользователей, пользователи предоставляют один или несколько из следующих способов связи:</span><span class="sxs-lookup"><span data-stu-id="37a5d-134">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="37a5d-135">Номер телефона</span><span class="sxs-lookup"><span data-stu-id="37a5d-135">Phone Number</span></span>

    -   <span data-ttu-id="37a5d-136">URL-адрес веб-страницы</span><span class="sxs-lookup"><span data-stu-id="37a5d-136">Webpage URL</span></span>

    -   <span data-ttu-id="37a5d-137">Почтовый адрес</span><span class="sxs-lookup"><span data-stu-id="37a5d-137">Mailing Address</span></span>

    <span data-ttu-id="37a5d-138">После получения запроса на исключение администратор MBAM может решить, нужно ли добавить пользователя в группу исключения BitLocker Active Directory.</span><span class="sxs-lookup"><span data-stu-id="37a5d-138">After the exemption request is received, the MBAM Administrator can take decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="37a5d-139">**Примечание**  После того как пользователь отправил запрос на исключение, агент MBAM сообщит пользователю "временно исключить", а затем ждет, пока не проверит соответствие требованиям компьютера.</span><span class="sxs-lookup"><span data-stu-id="37a5d-139">**Note** Once a user submits an exemption request, the MBAM agent reports the user as “temporarily exempt” and then waits a configurable number of days before it checks the computer’s compliance again.</span></span> <span data-ttu-id="37a5d-140">Если администратор MBAM отклонил запрос на исключение, параметр запроса на исключение деактивируется, что предотвращает повторный запрос исключения пользователем.</span><span class="sxs-lookup"><span data-stu-id="37a5d-140">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from being able to request the exemption again.</span></span>

     

## <span data-ttu-id="37a5d-141">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="37a5d-141">Related topics</span></span>


[<span data-ttu-id="37a5d-142">Администрирование компонентов MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="37a5d-142">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





