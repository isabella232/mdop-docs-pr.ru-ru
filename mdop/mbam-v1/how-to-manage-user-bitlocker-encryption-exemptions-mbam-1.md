---
title: Управление исключениями шифрования BitLocker для пользователя
description: Управление исключениями шифрования BitLocker для пользователя
author: dansimp
ms.assetid: 48d69721-504f-4524-8a04-b9ce213ac9b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c3d70558a65c3288174413d6c36cc9c77bc9eaa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812965"
---
# <span data-ttu-id="f3448-103">Управление исключениями шифрования BitLocker для пользователя</span><span class="sxs-lookup"><span data-stu-id="f3448-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="f3448-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) можно использовать для управления защитой BitLocker путем исключения пользователей, которые не нуждаются в шифровании.</span><span class="sxs-lookup"><span data-stu-id="f3448-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="f3448-105">Чтобы исключить пользователей из системы защиты BitLocker, Организация должна сначала создать инфраструктуру для поддержки таких исключений.</span><span class="sxs-lookup"><span data-stu-id="f3448-105">To exempt users from BitLocker protection, an organization must first create an infrastructure to support such exemptions.</span></span> <span data-ttu-id="f3448-106">Поддерживающая инфраструктура может включать в себя номер контактного телефона, веб-страницы или почтового адреса для исключения запроса.</span><span class="sxs-lookup"><span data-stu-id="f3448-106">The supporting infrastructure might include a contact telephone number, webpage, or mailing address to request exemption.</span></span> <span data-ttu-id="f3448-107">Кроме того, пользователи, которые не могут быть исключены, должны быть добавлены в группу безопасности для групповых политик, созданных специально для исключенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="f3448-107">Also, any exempt user will have to be added to a security group for Group Policy created specifically for exempted users.</span></span> <span data-ttu-id="f3448-108">Когда участники этой группы безопасности входят на компьютер, групповая политика пользователя показывает, что пользователь исключен из системы защиты BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f3448-108">When members of this security group log on to a computer, the user Group Policy shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="f3448-109">Политика пользователя перезапишет политику компьютера, и компьютер останется без шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f3448-109">The user policy overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="f3448-110">**Примечание**  Если на компьютере уже установлена защита с помощью BitLocker, политика исключения пользователя не действует.</span><span class="sxs-lookup"><span data-stu-id="f3448-110">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="f3448-111">В следующей таблице показано, как применяется защита BitLocker в зависимости от того, как устанавливаются исключения.</span><span class="sxs-lookup"><span data-stu-id="f3448-111">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f3448-112">Состояние пользователя</span><span class="sxs-lookup"><span data-stu-id="f3448-112">User Status</span></span></th>
<th align="left"><span data-ttu-id="f3448-113">Компьютер не исключен</span><span class="sxs-lookup"><span data-stu-id="f3448-113">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="f3448-114">Освобождение от компьютера</span><span class="sxs-lookup"><span data-stu-id="f3448-114">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f3448-115">Пользователь не исключен</span><span class="sxs-lookup"><span data-stu-id="f3448-115">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f3448-116">На компьютере принудительно применяется защита BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f3448-116">BitLocker protection is enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3448-117">Защита BitLocker на компьютере не обеспечивается принудительно.</span><span class="sxs-lookup"><span data-stu-id="f3448-117">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f3448-118">Освобождение от пользователя</span><span class="sxs-lookup"><span data-stu-id="f3448-118">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f3448-119">Защита BitLocker на компьютере не обеспечивается принудительно.</span><span class="sxs-lookup"><span data-stu-id="f3448-119">BitLocker protection is not enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3448-120">Защита BitLocker на компьютере не обеспечивается принудительно.</span><span class="sxs-lookup"><span data-stu-id="f3448-120">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f3448-121">Исключение пользователя из шифрования BitLocker</span><span class="sxs-lookup"><span data-stu-id="f3448-121">To exempt a user from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="f3448-122">Создайте группу безопасности ActiveDirectoryDomainServices, которая будет использоваться для управления исключениями пользователей из шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f3448-122">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption.</span></span>

2.  <span data-ttu-id="f3448-123">Создание параметров объекта групповой политики с помощью шаблона групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="f3448-123">Create a Group Policy Object setting by using the MBAM Group Policy template.</span></span> <span data-ttu-id="f3448-124">Свяжите объект групповой политики с группой Active Directory, созданной на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="f3448-124">Associate the Group Policy Object with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="f3448-125">Чтобы получить дополнительные сведения о параметрах политики, которые позволят пользователям запрашивать исключение из шифрования BitLocker, ознакомьтесь с разделом "Настройка политики исключения пользователей" в разделе [планирование MBAM 1,0 с учетом требований групповой политики](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f3448-125">For more information about the necessary policy settings to enable users to request exemption from BitLocker encryption, see the Configure User Exemption Policy section in [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

3.  <span data-ttu-id="f3448-126">После создания группы безопасности для пользователей, исключенных с помощью BitLocker, добавьте в эту группу имена пользователей, которые запрашивают исключение.</span><span class="sxs-lookup"><span data-stu-id="f3448-126">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting exemption.</span></span> <span data-ttu-id="f3448-127">Когда пользователь входит на компьютер, управляемый BitLocker, клиент MBAM проверит параметр политики исключения пользователей и приостановит защиту в зависимости от того, входит ли пользователь в группу безопасности исключений BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f3448-127">When a user logs on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="f3448-128">**Примечание**  Сценарии для общедоступного компьютера требуют особого рассмотрения в отношении освобождения пользователей.</span><span class="sxs-lookup"><span data-stu-id="f3448-128">**Note** Shared computer scenarios require special consideration regarding user exemption.</span></span> <span data-ttu-id="f3448-129">Если пользователь без исключения входит в систему на компьютере, к которому предоставлен общий доступ, компьютер может быть зашифрован.</span><span class="sxs-lookup"><span data-stu-id="f3448-129">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="f3448-130">Разрешение пользователям запрашивать исключение из шифрования BitLocker</span><span class="sxs-lookup"><span data-stu-id="f3448-130">To enable users to request exemption from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="f3448-131">После того как вы настроили политики исключения пользователей, usingwith шаблон политики MBAM, пользователь может запросить исключение из системы защиты BitLocker с помощью клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="f3448-131">After you have configured user-exemption policies by usingwith the MBAM Policy template, a user can request exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="f3448-132">Когда пользователь входит на компьютер, помеченный как **совместимый** в списке совместимого оборудования MBAM, система предоставляет пользователю уведомление о том, что компьютер будет зашифрован.</span><span class="sxs-lookup"><span data-stu-id="f3448-132">When a user logs on to a computer that is marked as **Compatible** in the MBAM Hardware Compatibility list, the system presents the user with a notification that the computer is going to be encrypted.</span></span> <span data-ttu-id="f3448-133">Пользователь может выбрать **исключение запросов** и отложить шифрование, выбрав параметр **позже**, или нажмите кнопку **начать** , чтобы сохранить шифрование BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f3448-133">The user can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="f3448-134">**Примечание**  Выбор **исключения запросов** откладывает защиту BitLocker, пока не будет достигнуто максимальное значение, заданное в политике исключения пользователей.</span><span class="sxs-lookup"><span data-stu-id="f3448-134">**Note** Selecting **Request Exemption** will postpone the BitLocker protection until the maximum time set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="f3448-135">Когда пользователь выбирает **исключение запросов**, пользователь получит уведомление о необходимости обратиться в группу администрирования BitLocker Организации.</span><span class="sxs-lookup"><span data-stu-id="f3448-135">When a user selects **Request Exemption**, the user is notified to contact the organization's BitLocker administration group.</span></span> <span data-ttu-id="f3448-136">В зависимости от того, как настроена Настройка политики исключения пользователей, пользователи предоставляют один или несколько из следующих способов связи:</span><span class="sxs-lookup"><span data-stu-id="f3448-136">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="f3448-137">Номер телефона</span><span class="sxs-lookup"><span data-stu-id="f3448-137">Phone Number</span></span>

    -   <span data-ttu-id="f3448-138">URL-адрес веб-страницы</span><span class="sxs-lookup"><span data-stu-id="f3448-138">Webpage URL</span></span>

    -   <span data-ttu-id="f3448-139">Почтовый адрес</span><span class="sxs-lookup"><span data-stu-id="f3448-139">Mailing Address</span></span>

    <span data-ttu-id="f3448-140">После отправки запроса администратор MBAM может решить, нужно ли добавить пользователя в группу исключения BitLocker Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f3448-140">After submittal of the request, the MBAM Administrator can decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="f3448-141">**Примечание**  После истечения срока отсрочки из политики исключения пользователя, пользователи не смогут запросить исключение для политики шифрования.</span><span class="sxs-lookup"><span data-stu-id="f3448-141">**Note** Once the postpone time limit from the User Exemption Policy has expired, users will not see the option to request exemption to the encryption policy.</span></span> <span data-ttu-id="f3448-142">На этом этапе пользователи должны обратиться к администратору MBAM напрямую, чтобы получить исключение из защиты BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f3448-142">At this point, users must contact the MBAM administrator directly in order to receive exemption from BitLocker Protection.</span></span>

     

## <span data-ttu-id="f3448-143">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f3448-143">Related topics</span></span>


[<span data-ttu-id="f3448-144">Администрирование компонентов MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="f3448-144">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





