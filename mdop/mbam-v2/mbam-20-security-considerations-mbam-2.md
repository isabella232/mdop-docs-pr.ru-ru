---
title: Процедуры безопасности MBAM 2.0
description: Процедуры безопасности MBAM 2.0
author: dansimp
ms.assetid: 0aa5c6e2-d92c-4e30-9f6a-b48abb667ae5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 04dc9b667faddecab629b50f4c5d909fd7b2829e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823912"
---
# <span data-ttu-id="20c54-103">Процедуры безопасности MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="20c54-103">MBAM 2.0 Security Considerations</span></span>


<span data-ttu-id="20c54-104">В этой статье содержится краткий обзор учетных записей и групп, файлов журналов и других вопросов, связанных с безопасностью, для администрирования и мониторинга Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="20c54-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="20c54-105">Чтобы получить дополнительные сведения, воспользуйтесь ссылками, приведенными в этой статье.</span><span class="sxs-lookup"><span data-stu-id="20c54-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="20c54-106">Общие рекомендации по безопасности</span><span class="sxs-lookup"><span data-stu-id="20c54-106">General Security Considerations</span></span>


**<span data-ttu-id="20c54-107">Общие сведения о рисках для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="20c54-107">Understand the security risks.</span></span>** <span data-ttu-id="20c54-108">Наиболее серьезным риском для администратора Microsoft BitLocker и наблюдения является то, что его функциональность может захватить неавторизованный пользователь, который может затем заново настроить шифрование BitLocker и получить данные ключа шифрования BitLocker на клиентах MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-108">The most serious risk from Microsoft BitLocker Administration and Monitoring is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="20c54-109">Тем не менее, в течение короткого промежутка времени MBAM функция может быть неблагоприятно из-за того, что в связи с отказом в обслуживании (например, электронная почта, сетевая связь, источник света и мощь) не имеет катастрофического воздействия.</span><span class="sxs-lookup"><span data-stu-id="20c54-109">However, the loss of MBAM functionality for a short period of time, due to a denial-of-service attack, does not generally have a catastrophic impact, unlike, for example, e-mail, network communications, light, and power.</span></span>

<span data-ttu-id="20c54-110">**Физическая защита компьютеров**.</span><span class="sxs-lookup"><span data-stu-id="20c54-110">**Physically secure your computers**.</span></span> <span data-ttu-id="20c54-111">Безопасность не имеет физического уровня безопасности.</span><span class="sxs-lookup"><span data-stu-id="20c54-111">There is no security without physical security.</span></span> <span data-ttu-id="20c54-112">Злоумышленник, которому удается получить доступ к серверу MBAM, может использовать его для атаки на всю клиентскую базу.</span><span class="sxs-lookup"><span data-stu-id="20c54-112">An attacker who gets physical access to an MBAM Server could potentially use it to attack the entire client base.</span></span> <span data-ttu-id="20c54-113">Все потенциальные физическая атака должны считаться очень риском и соответствующим образом устранены.</span><span class="sxs-lookup"><span data-stu-id="20c54-113">All potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="20c54-114">Серверы MBAM должны храниться в надежной серверной комнате с управляемым доступом.</span><span class="sxs-lookup"><span data-stu-id="20c54-114">MBAM servers should be stored in a secure server room with controlled access.</span></span> <span data-ttu-id="20c54-115">Защитите эти компьютеры, если администраторы не находятся в физическом режиме, с помощью операционной системы и запирания компьютера или защищенной экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="20c54-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="20c54-116">**Установка последних обновлений для системы безопасности на всех компьютерах**.</span><span class="sxs-lookup"><span data-stu-id="20c54-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="20c54-117">Получайте сведения о новых обновлениях для операционных систем, Microsoft SQL Server и MBAM, подписавшись на службу уведомлений системы безопасности ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="20c54-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

<span data-ttu-id="20c54-118">**Используйте надежные пароли и передавайте фразы**.</span><span class="sxs-lookup"><span data-stu-id="20c54-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="20c54-119">Для всех учетных записей администраторов MBAM и MBAM следует использовать надежные пароли с 15 и более знаками.</span><span class="sxs-lookup"><span data-stu-id="20c54-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="20c54-120">Никогда не используйте пустые пароли.</span><span class="sxs-lookup"><span data-stu-id="20c54-120">Never use blank passwords.</span></span> <span data-ttu-id="20c54-121">Дополнительные сведения о концепциях паролей можно найти в статье "пароли и политики учетных записей" на сайте TechNet ( <https://go.microsoft.com/fwlink/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="20c54-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/?LinkId=30009>).</span></span>

## <span data-ttu-id="20c54-122">Учетные записи и группы в MBAM</span><span class="sxs-lookup"><span data-stu-id="20c54-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="20c54-123">Рекомендации по управлению учетными записями пользователей — это создание глобальных групп домена и добавление в них учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="20c54-123">The best practice for managing user accounts is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="20c54-124">Затем добавьте глобальные учетные записи домена в необходимые локальные группы MBAM на серверах MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="20c54-125">Группы ActiveDirectoryDomainServices</span><span class="sxs-lookup"><span data-stu-id="20c54-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="20c54-126">В процессе настройки MBAM никакие группы Active Directory не создаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="20c54-126">No Active Directory groups are created automatically during the MBAM setup process.</span></span> <span data-ttu-id="20c54-127">Тем не менее, для управления операциями MBAM рекомендуется создать следующие глобальные группы ActiveDirectoryDomainServices.</span><span class="sxs-lookup"><span data-stu-id="20c54-127">However, it is recommended that you create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="20c54-128">Имя группы</span><span class="sxs-lookup"><span data-stu-id="20c54-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="20c54-129">Сведения</span><span class="sxs-lookup"><span data-stu-id="20c54-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="20c54-130">MBAM опытных пользователей службы поддержки</span><span class="sxs-lookup"><span data-stu-id="20c54-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="20c54-131">Создавайте эту группу, чтобы управлять членами локальной группы пользователей MBAM Advanced, созданной в ходе настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="20c54-132">Доступ к базе данных аудита для проверки соответствия MBAM</span><span class="sxs-lookup"><span data-stu-id="20c54-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="20c54-133">Создайте эту группу для управления членами локальной группы доступа аудита соответствия MBAM, созданной в ходе настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="20c54-134">Пользователи службы поддержки MBAM</span><span class="sxs-lookup"><span data-stu-id="20c54-134">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="20c54-135">Создайте эту группу, чтобы управлять членами локальной группы "Пользователи службы поддержки MBAM", созданной в ходе настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-135">Create this group to manage members of the MBAM Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="20c54-136">MBAM восстановления и доступа к БД оборудования</span><span class="sxs-lookup"><span data-stu-id="20c54-136">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="20c54-137">Создайте эту группу, чтобы управлять членами локальной группы доступа к восстановлению MBAM и данными оборудования в базе данных, созданной во время настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-137">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="20c54-138">Пользователи отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="20c54-138">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="20c54-139">Создавайте эту группу, чтобы управлять членами локальной группы пользователей отчета MBAM, созданной в ходе настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-139">Create this group to manage members of the MBAM Report Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="20c54-140">Системные администраторы MBAM</span><span class="sxs-lookup"><span data-stu-id="20c54-140">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="20c54-141">Создайте эту группу для управления членами локальной группы администраторов MBAM, созданной в ходе настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-141">Create this group to manage members of the MBAM System Administrators local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="20c54-142">Исключения шифрования BitLocker</span><span class="sxs-lookup"><span data-stu-id="20c54-142">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="20c54-143">Создайте эту группу для управления учетными записями пользователей, которые должны исключаться из шифрования BitLocker, начиная с компьютеров, на которых они вошли.</span><span class="sxs-lookup"><span data-stu-id="20c54-143">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------mbam-server-local-groups"></a> <span data-ttu-id="20c54-144">Локальные группы сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="20c54-144">MBAM Server Local Groups</span></span>

<span data-ttu-id="20c54-145">Программа установки MBAM создает локальные группы для поддержки операций MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-145">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="20c54-146">Вы должны добавить глобальные группы ActiveDirectoryDomainServices в соответствующие локальные группы MBAM, чтобы настроить безопасность MBAM и разрешения на доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="20c54-146">You should add the ActiveDirectoryDomainServices global groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="20c54-147">Имя группы</span><span class="sxs-lookup"><span data-stu-id="20c54-147">Group Name</span></span></th>
<th align="left"><span data-ttu-id="20c54-148">Сведения</span><span class="sxs-lookup"><span data-stu-id="20c54-148">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="20c54-149">MBAM опытных пользователей службы поддержки</span><span class="sxs-lookup"><span data-stu-id="20c54-149">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="20c54-150">Участники этой группы увеличивают доступ к возможностям службы поддержки в MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-150">Members of this group have increased access to the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="20c54-151">Доступ к базе данных аудита для проверки соответствия MBAM</span><span class="sxs-lookup"><span data-stu-id="20c54-151">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="20c54-152">Содержит компьютеры, имеющие доступ к базе данных проверки соответствия MBAM и аудита.</span><span class="sxs-lookup"><span data-stu-id="20c54-152">Contains the machines that have access to the MBAM Compliance and Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="20c54-153">Пользователи службы поддержки MBAM</span><span class="sxs-lookup"><span data-stu-id="20c54-153">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="20c54-154">Участники этой группы имеют доступ к некоторым функциям службы поддержки в MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-154">Members of this group have access to some of the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="20c54-155">MBAM восстановления и доступа к БД оборудования</span><span class="sxs-lookup"><span data-stu-id="20c54-155">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="20c54-156">Содержит компьютеры, у которых есть доступ к базе данных восстановления MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-156">Contains the machines that have access to the MBAM Recovery Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="20c54-157">Пользователи отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="20c54-157">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="20c54-158">Участники этой группы имеют доступ к отчетам о соответствии и аудиту в MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-158">Members of this group have access to the Compliance and Audit reports from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="20c54-159">Системные администраторы MBAM</span><span class="sxs-lookup"><span data-stu-id="20c54-159">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="20c54-160">Участники этой группы имеют доступ ко всем функциям MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-160">Members of this group have access to all MBAM features.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="20c54-161">Учетная запись службы SSRS Reports</span><span class="sxs-lookup"><span data-stu-id="20c54-161">SSRS Reports Service Account</span></span>

<span data-ttu-id="20c54-162">Учетная запись службы отчетов SSRS предоставляет контекст безопасности для запуска отчетов MBAM, доступных через службы SSRS.</span><span class="sxs-lookup"><span data-stu-id="20c54-162">The SSRS Reports service account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="20c54-163">Оно настроено во время настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-163">It is configured during MBAM Setup.</span></span>

<span data-ttu-id="20c54-164">Когда вы настраиваете учетную запись службы отчетов SSRS, укажите учетную запись пользователя домена и настройте пароль на бессрочную настройку.</span><span class="sxs-lookup"><span data-stu-id="20c54-164">When you configure the SSRS Reports service account, specify a domain user account, and configure the password to never expire.</span></span>

<span data-ttu-id="20c54-165">**Примечание**  Если вы измените имя учетной записи службы после развертывания MBAM, необходимо заново настроить источник данных отчетов, чтобы использовать новые учетные данные учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="20c54-165">**Note** If you change the name of the service account after you deploy MBAM, you must reconfigure the reporting data source to use the new service account credentials.</span></span> <span data-ttu-id="20c54-166">В противном случае вы не сможете получить доступ к порталу службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="20c54-166">Otherwise, you will not be able to access the Help Desk Portal.</span></span>

 

## <a href="" id="---------mbam-log-files"></a> <span data-ttu-id="20c54-167">Файлы журнала MBAM</span><span class="sxs-lookup"><span data-stu-id="20c54-167">MBAM Log Files</span></span>


<span data-ttu-id="20c54-168">Следующие файлы журнала установки MBAM создаются в папке "% Temp%" пользователя при настройке MBAM:</span><span class="sxs-lookup"><span data-stu-id="20c54-168">The following MBAM Setup log files are created in the installing user’s %temp% folder during MBAM Setup:</span></span>

**<span data-ttu-id="20c54-169">Файлы журнала установки MBAM Server</span><span class="sxs-lookup"><span data-stu-id="20c54-169">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="20c54-170">MSI <em> &lt; пять случайных знаков &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="20c54-170">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="20c54-171">Записываются в журнал действия, выполненные во время установки MBAM и установки компонентов сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-171">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="20c54-172">InstallComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="20c54-172">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="20c54-173">Записываются в журнал действия, предпринятые для создания настройки соответствия MBAM и проверки базы данных аудита.</span><span class="sxs-lookup"><span data-stu-id="20c54-173">Logs actions taken to create the MBAM Compliance and Audit Database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="20c54-174">InstallKeyComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="20c54-174">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="20c54-175">Записываются в журнал действия, предпринятые для создания базы данных восстановления MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-175">Logs actions taken to create the MBAM Recovery Database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="20c54-176">AddHelpDeskDbAuditUsers. log</span><span class="sxs-lookup"><span data-stu-id="20c54-176">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="20c54-177">Заносит в журнал действия, предпринятые для создания имен входа SQL Server в базе данных соответствия требованиям MBAM и аудита, а также для авторизации веб-службы поддержки в базу данных для отчетов.</span><span class="sxs-lookup"><span data-stu-id="20c54-177">Logs actions taken to create the SQL Server logins on the MBAM Compliance and Audit database and authorize the HelpDesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="20c54-178">AddHelpDeskDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="20c54-178">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="20c54-179">Записываются в журнал действия, предпринятые для авторизации веб-служб в базу данных для восстановления ключей и создания имен для входа в базу данных восстановления MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-179">Logs actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery Database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="20c54-180">AddKeyComplianceDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="20c54-180">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="20c54-181">Записываются в журнал действия, предпринятые для авторизации веб-служб на соответствие MBAM требованиям и базам данных аудита для отчетов о соответствии</span><span class="sxs-lookup"><span data-stu-id="20c54-181">Logs actions taken to authorize web services to MBAM Compliance and Audit Database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="20c54-182">AddRecoveryAndHardwareDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="20c54-182">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="20c54-183">Записываются в журнал действия, предпринятые для авторизации веб-служб в базу данных восстановления MBAM для восстановления ключей.</span><span class="sxs-lookup"><span data-stu-id="20c54-183">Logs actions taken to authorize web services to the MBAM Recovery database for key recovery.</span></span>

<span data-ttu-id="20c54-184">**Примечание**  Чтобы получить дополнительные файлы журнала установки MBAM, необходимо установить MBAM с помощью пакета msiexec и &lt; параметра/l Location &gt; .</span><span class="sxs-lookup"><span data-stu-id="20c54-184">**Note** In order to obtain additional MBAM Setup log files, you have to install MBAM by using the msiexec package and the /L &lt;location&gt; option.</span></span> <span data-ttu-id="20c54-185">Файлы журнала создаются в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="20c54-185">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="20c54-186">Файлы журнала установки клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="20c54-186">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="20c54-187">MSI <em> &lt; пять случайных знаков &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="20c54-187">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="20c54-188">Записываются в журнал действия, выполненные во время установки клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="20c54-188">Logs the actions taken during MBAM Client installation.</span></span>

## <a href="" id="---------mbam-database-tde-considerations"></a> <span data-ttu-id="20c54-189">Вопросы TDE базы данных MBAM</span><span class="sxs-lookup"><span data-stu-id="20c54-189">MBAM Database TDE Considerations</span></span>


<span data-ttu-id="20c54-190">Функция шифрования прозрачных данных (TDE), доступная в SQL Server, является необязательной установкой для экземпляров базы данных, которые будут размещаться в MBAMных функциях базы данных.</span><span class="sxs-lookup"><span data-stu-id="20c54-190">The transparent data encryption (TDE) feature that is available in SQL Server is an optional installation for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="20c54-191">С помощью TDE можно выполнять полное шифрование на уровне базы данных в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="20c54-191">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="20c54-192">TDE — это оптимальный вариант массового шифрования для соответствия требованиям законодательства и корпоративным стандартам безопасности данных.</span><span class="sxs-lookup"><span data-stu-id="20c54-192">TDE is the optimal choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="20c54-193">TDE работает на уровне файла, который аналогичен двум функциям Windows: шифрованной файловой системе (EFS) и шифрованию диска BitLocker, в которых также шифруются данные на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="20c54-193">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="20c54-194">TDE не заменяет шифрование на уровне ячейки, EFS и BitLocker.</span><span class="sxs-lookup"><span data-stu-id="20c54-194">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="20c54-195">Если в базе данных включена TDE, все резервные копии шифруются.</span><span class="sxs-lookup"><span data-stu-id="20c54-195">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="20c54-196">Таким образом, чтобы убедиться в том, что сертификат, использовавшийся для защиты ключа шифрования базы данных, должен быть архивирован и поддерживаться с резервной копией базы данных.</span><span class="sxs-lookup"><span data-stu-id="20c54-196">Thus, special care must be taken to ensure that the certificate that was used to protect the database encryption key is backed up and maintained with the database backup.</span></span> <span data-ttu-id="20c54-197">Если сертификат (или сертификаты) теряется, данные не будут прочитаны.</span><span class="sxs-lookup"><span data-stu-id="20c54-197">If this certificate (or certificates) is lost, the data will be unreadable.</span></span> <span data-ttu-id="20c54-198">Создавайте резервные копии сертификата вместе с базой данных.</span><span class="sxs-lookup"><span data-stu-id="20c54-198">Back up the certificate along with the database.</span></span> <span data-ttu-id="20c54-199">Каждая резервная копия сертификата должна содержать два файла.</span><span class="sxs-lookup"><span data-stu-id="20c54-199">Each certificate backup should have two files.</span></span> <span data-ttu-id="20c54-200">Оба этих файла следует архивировать (в идеале отдельно от файла резервной копии базы данных для обеспечения безопасности).</span><span class="sxs-lookup"><span data-stu-id="20c54-200">Both of these files should be archived (ideally separately from the database backup file for security).</span></span> <span data-ttu-id="20c54-201">Вы также можете использовать функцию расширенного управления ключами (Extensible Key Management) (расширенное управление ключами) для хранения и обслуживания ключей, используемых для TDE.</span><span class="sxs-lookup"><span data-stu-id="20c54-201">You can alternatively consider using the extensible key management (EKM) feature (see Extensible Key Management) for storage and maintenance of keys used for TDE.</span></span>

<span data-ttu-id="20c54-202">Пример включения TDE для экземпляров базы данных MBAM можно найти в разделе [Оценка MBAM 2,0](evaluating-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="20c54-202">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 2.0](evaluating-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="20c54-203">Дополнительные сведения о TDE в SQLServer 2008 можно найти в разделе [шифрование SQL Server]( https://go.microsoft.com/fwlink/?LinkId=299883).</span><span class="sxs-lookup"><span data-stu-id="20c54-203">For more information about TDE in SQLServer 2008, see [SQL Server Encryption]( https://go.microsoft.com/fwlink/?LinkId=299883).</span></span>

## <span data-ttu-id="20c54-204">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="20c54-204">Related topics</span></span>


[<span data-ttu-id="20c54-205">Безопасность и конфиденциальность для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="20c54-205">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)

 

 





