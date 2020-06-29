---
title: Управление исключениями шифрования BitLocker для пользователя
description: Управление исключениями шифрования BitLocker для пользователя
author: dansimp
ms.assetid: f582ab82-5bb5-4cd3-ad7c-483240533cf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4224a0fb6d905c2362659efe7cf05e16756f7c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826792"
---
# <span data-ttu-id="30137-103">Управление исключениями шифрования BitLocker для пользователя</span><span class="sxs-lookup"><span data-stu-id="30137-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="30137-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) позволяет исключить пользователей из требований к шифрованию диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30137-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="30137-105">Чтобы исключить пользователей из системы защиты BitLocker, необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="30137-105">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30137-106">Задача</span><span class="sxs-lookup"><span data-stu-id="30137-106">Task</span></span></th>
<th align="left"><span data-ttu-id="30137-107">Сведения</span><span class="sxs-lookup"><span data-stu-id="30137-107">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30137-108">Создание инфраструктуры для поддержки исключенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="30137-108">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30137-109">Ниже приведены примеры этой инфраструктуры: предоставление пользователям телефонного номера, веб-страницы или почтового адреса, которые можно использовать для запроса освобождения.</span><span class="sxs-lookup"><span data-stu-id="30137-109">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30137-110">Добавьте исключенного пользователя в группу безопасности для объекта групповой политики, настроенного специально для исключенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="30137-110">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30137-111">Когда участники этой группы безопасности входят в систему на компьютере, параметр групповой политики пользователя исключается из защиты BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30137-111">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="30137-112">Параметр групповой политики пользователя перезапишет политику компьютера, и компьютер останется без шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30137-112">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="30137-113">Примечание.</span><span class="sxs-lookup"><span data-stu-id="30137-113">Note</span></span></strong><br/><p><span data-ttu-id="30137-114">MBAM не действует на политику шифрования, если на компьютере уже установлена защита с помощью BitLocker и пользователь не исключен.</span><span class="sxs-lookup"><span data-stu-id="30137-114">MBAM does not enact the encryption policy if the computer is already BitLocker-protected and the user is exempted.</span></span> <span data-ttu-id="30137-115">Тем не менее, если другой пользователь, не исключающий из политики шифрования, входит в систему, будет происходить шифрование.</span><span class="sxs-lookup"><span data-stu-id="30137-115">However, if another user who is not exempt from the encryption policy signs in to the computer, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="30137-116">Ниже описаны действия, которые следует выполнить, если конечные пользователи запрашивают исключение из процесса освобождения от шифрования диска BitLocker с помощью клиента MBAM или любого процесса, используемого в Организации.</span><span class="sxs-lookup"><span data-stu-id="30137-116">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="30137-117">Необходимо настроить параметры групповой политики MBAM, чтобы разрешить пользователям запрашивать исключение из шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30137-117">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="30137-118">Когда конечные пользователи входят на компьютер, необходимый для шифрования, они получают уведомление о том, что их компьютеры будут зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="30137-118">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="30137-119">Они могут выбрать **исключение запросов** и отложить шифрование с помощью команды " **отложить**" или выбрать команду **Начать шифрование** для подтверждения шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30137-119">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="30137-120">Примечание.</span><span class="sxs-lookup"><span data-stu-id="30137-120">Note</span></span>**  
    <span data-ttu-id="30137-121">Выбор **исключения** откладывает защиту BitLocker, пока не будет задано максимальное значение, заданное в политике исключения пользователей.</span><span class="sxs-lookup"><span data-stu-id="30137-121">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="30137-122">Если конечные пользователи выбирают **исключение запросов**, они получают уведомление о том, что они должны обратиться в группу администрирования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30137-122">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="30137-123">В зависимости от того, как настроена **Настройка политики исключения пользователей** , пользователи предоставляют один или несколько из следующих способов связи:</span><span class="sxs-lookup"><span data-stu-id="30137-123">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="30137-124">Номер телефона</span><span class="sxs-lookup"><span data-stu-id="30137-124">Phone number</span></span>

    -   <span data-ttu-id="30137-125">URL-адрес веб-страницы</span><span class="sxs-lookup"><span data-stu-id="30137-125">Webpage URL</span></span>

    -   <span data-ttu-id="30137-126">Почтовый адрес</span><span class="sxs-lookup"><span data-stu-id="30137-126">Mailing address</span></span>

3.  <span data-ttu-id="30137-127">После получения запроса на исключение администратор MBAM определяет, нужно ли добавить пользователя в группу исключений BitLocker в доменных службах Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="30137-127">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="30137-128">После того как пользователь отправил запрос на исключение, клиент MBAM сообщит пользователю "временно исключить".</span><span class="sxs-lookup"><span data-stu-id="30137-128">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="30137-129">Затем клиент ждет указанное количество дней, которое ИТ-администраторы настраивают, прежде чем снова проверить соответствие компьютера.</span><span class="sxs-lookup"><span data-stu-id="30137-129">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="30137-130">Если администратор MBAM отклоняет запрос на исключение, параметр запроса на исключение деактивируется, что предотвращает повторный запрос исключения пользователем.</span><span class="sxs-lookup"><span data-stu-id="30137-130">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

<span data-ttu-id="30137-131">Администрирование и мониторинг Microsoft BitLocker (MBAM) позволяет исключить пользователей из требований к шифрованию диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30137-131">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="30137-132">Чтобы исключить пользователей из системы защиты BitLocker, необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="30137-132">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30137-133">Задача</span><span class="sxs-lookup"><span data-stu-id="30137-133">Task</span></span></th>
<th align="left"><span data-ttu-id="30137-134">Сведения</span><span class="sxs-lookup"><span data-stu-id="30137-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30137-135">Создание инфраструктуры для поддержки исключенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="30137-135">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30137-136">Ниже приведены примеры этой инфраструктуры: предоставление пользователям телефонного номера, веб-страницы или почтового адреса, которые можно использовать для запроса освобождения.</span><span class="sxs-lookup"><span data-stu-id="30137-136">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30137-137">Добавьте исключенного пользователя в группу безопасности для объекта групповой политики, настроенного специально для исключенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="30137-137">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="30137-138">Когда участники этой группы безопасности входят в систему на компьютере, параметр групповой политики пользователя исключается из защиты BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30137-138">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="30137-139">Параметр групповой политики пользователя перезапишет политику компьютера, и компьютер останется без шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30137-139">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="30137-140">Примечание.</span><span class="sxs-lookup"><span data-stu-id="30137-140">Note</span></span></strong><br/><p><span data-ttu-id="30137-141">Если на компьютере уже установлена защита с помощью BitLocker, политика исключения пользователя не действует.</span><span class="sxs-lookup"><span data-stu-id="30137-141">If the computer is already BitLocker-protected, the User Exemption Policy has no effect.</span></span> <span data-ttu-id="30137-142">Кроме того, если другой пользователь входит в систему на компьютере, который не исключен из политики шифрования, будет происходить шифрование.</span><span class="sxs-lookup"><span data-stu-id="30137-142">In addition, if another user signs in to a computer that is not exempt from the encryption policy, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="30137-143">Ниже описаны действия, которые следует выполнить, если конечные пользователи запрашивают исключение из процесса освобождения от шифрования диска BitLocker с помощью клиента MBAM или любого процесса, используемого в Организации.</span><span class="sxs-lookup"><span data-stu-id="30137-143">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="30137-144">Необходимо настроить параметры групповой политики MBAM, чтобы разрешить пользователям запрашивать исключение из шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30137-144">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="30137-145">Когда конечные пользователи входят на компьютер, необходимый для шифрования, они получают уведомление о том, что их компьютеры будут зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="30137-145">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="30137-146">Они могут выбрать **исключение запросов** и отложить шифрование с помощью команды " **отложить**" или выбрать команду **Начать шифрование** для подтверждения шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30137-146">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="30137-147">Примечание.</span><span class="sxs-lookup"><span data-stu-id="30137-147">Note</span></span>**  
    <span data-ttu-id="30137-148">Выбор **исключения** откладывает защиту BitLocker, пока не будет задано максимальное значение, заданное в политике исключения пользователей.</span><span class="sxs-lookup"><span data-stu-id="30137-148">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="30137-149">Если конечные пользователи выбирают **исключение запросов**, они получают уведомление о том, что они должны обратиться в группу администрирования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30137-149">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="30137-150">В зависимости от того, как настроена **Настройка политики исключения пользователей** , пользователи предоставляют один или несколько из следующих способов связи:</span><span class="sxs-lookup"><span data-stu-id="30137-150">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="30137-151">Номер телефона</span><span class="sxs-lookup"><span data-stu-id="30137-151">Phone number</span></span>

    -   <span data-ttu-id="30137-152">URL-адрес веб-страницы</span><span class="sxs-lookup"><span data-stu-id="30137-152">Webpage URL</span></span>

    -   <span data-ttu-id="30137-153">Почтовый адрес</span><span class="sxs-lookup"><span data-stu-id="30137-153">Mailing address</span></span>

3.  <span data-ttu-id="30137-154">После получения запроса на исключение администратор MBAM определяет, нужно ли добавить пользователя в группу исключений BitLocker в доменных службах Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="30137-154">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="30137-155">После того как пользователь отправил запрос на исключение, клиент MBAM сообщит пользователю "временно исключить".</span><span class="sxs-lookup"><span data-stu-id="30137-155">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="30137-156">Затем клиент ждет указанное количество дней, которое ИТ-администраторы настраивают, прежде чем снова проверить соответствие компьютера.</span><span class="sxs-lookup"><span data-stu-id="30137-156">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="30137-157">Если администратор MBAM отклоняет запрос на исключение, параметр запроса на исключение деактивируется, что предотвращает повторный запрос исключения пользователем.</span><span class="sxs-lookup"><span data-stu-id="30137-157">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

**<span data-ttu-id="30137-158">Исключение пользователя из шифрования диска BitLocker</span><span class="sxs-lookup"><span data-stu-id="30137-158">To exempt a user from BitLocker Drive Encryption</span></span>**

1.  <span data-ttu-id="30137-159">Создайте группу безопасности AD DS, которая будет использоваться для управления исключениями пользователей из требований шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="30137-159">Create an AD DS security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="30137-160">Создание объекта групповой политики с помощью шаблонов групповой политики администрирования Microsoft BitLocker и наблюдения за ними.</span><span class="sxs-lookup"><span data-stu-id="30137-160">Create a Group Policy Object by using the Microsoft BitLocker Administration and Monitoring Group Policy Templates.</span></span>

3.  <span data-ttu-id="30137-161">Свяжите объект групповой политики с группой доменных служб Active Directory, созданной на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="30137-161">Associate the Group Policy Object with the AD DS group that you created in the previous step.</span></span> <span data-ttu-id="30137-162">Параметры политики, позволяющие исключить пользователей, находятся по адресу: **UserConfiguration** &gt; **Административные шаблоны** &gt; **компоненты Windows** &gt; **MDOP MBAM (Управление BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="30137-162">The policy settings to exempt users are located at: **UserConfiguration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

4.  <span data-ttu-id="30137-163">В группу безопасности, созданную для пользователей, исключенных с помощью BitLocker, добавьте имена пользователей, которые запрашивают исключение.</span><span class="sxs-lookup"><span data-stu-id="30137-163">To the security group you created for BitLocker exempted users, add the names of the users who are requesting an exemption.</span></span>

    <span data-ttu-id="30137-164">Когда пользователь входит на компьютер, управляемый BitLocker, клиент MBAM проверяет параметр политики исключения пользователей.</span><span class="sxs-lookup"><span data-stu-id="30137-164">When a user signs in to a computer controlled by BitLocker, the MBAM Client checks the User Exemption Policy setting.</span></span> <span data-ttu-id="30137-165">Если компьютер уже зашифрован, защита BitLocker не приостанавливается.</span><span class="sxs-lookup"><span data-stu-id="30137-165">If the computer is already encrypted, BitLocker protection is not suspended.</span></span> <span data-ttu-id="30137-166">Если компьютер не зашифрован, MBAM не будет запрашивать шифрование пользователем.</span><span class="sxs-lookup"><span data-stu-id="30137-166">If the computer is not encrypted, MBAM does not prompt the user to encrypt.</span></span>

    **<span data-ttu-id="30137-167">Важно.</span><span class="sxs-lookup"><span data-stu-id="30137-167">Important</span></span>**  
    <span data-ttu-id="30137-168">При использовании исключений пользователей BitLocker в сценариях общего компьютера требуется учитывать особые особенности.</span><span class="sxs-lookup"><span data-stu-id="30137-168">Shared computer scenarios require special consideration when you are using BitLocker user exemptions.</span></span> <span data-ttu-id="30137-169">Если пользователь без исключения не входит в компьютер, к которому предоставлен общий доступ для пользователей с исключениями, компьютер может быть зашифрован.</span><span class="sxs-lookup"><span data-stu-id="30137-169">If a non-exempt user signs in to a computer that is shared with an exempt user, the computer may be encrypted.</span></span>




## <span data-ttu-id="30137-170">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="30137-170">Related topics</span></span>


[<span data-ttu-id="30137-171">Администрирование компонентов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="30137-171">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="30137-172">Планирование требований групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="30137-172">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)




## <span data-ttu-id="30137-173">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="30137-173">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="30137-174">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="30137-174">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="30137-175">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="30137-175">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




