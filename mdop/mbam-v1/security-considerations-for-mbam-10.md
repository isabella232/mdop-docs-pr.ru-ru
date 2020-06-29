---
title: Рекомендации по безопасности для MBAM 1.0
description: Рекомендации по безопасности для MBAM 1.0
author: dansimp
ms.assetid: 5e1c8b8c-235b-4a92-8b0b-da50dca17353
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b06c343c8193293dde91bc7af2541f35f332d261
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826192"
---
# <span data-ttu-id="cbbfe-103">Рекомендации по безопасности для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="cbbfe-103">Security Considerations for MBAM 1.0</span></span>


<span data-ttu-id="cbbfe-104">В этой статье содержится краткий обзор учетных записей и групп, файлов журналов и других вопросов, связанных с безопасностью, для администрирования и мониторинга Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="cbbfe-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="cbbfe-105">Чтобы получить дополнительные сведения, воспользуйтесь ссылками, приведенными в этой статье.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-105">For more information, follow the links in this article.</span></span>

## <span data-ttu-id="cbbfe-106">Общие рекомендации по безопасности</span><span class="sxs-lookup"><span data-stu-id="cbbfe-106">General security considerations</span></span>


**<span data-ttu-id="cbbfe-107">Общие сведения о рисках для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-107">Understand the security risks.</span></span>** <span data-ttu-id="cbbfe-108">Наиболее серьезный риск для MBAM заключается в том, что его функциональность может захватить неавторизованный пользователь, который может затем заново настроить шифрование BitLocker и получить данные ключа шифрования BitLocker на клиентах MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-108">The most serious risk to MBAM is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="cbbfe-109">Однако утрата функций MBAM в течение короткого промежутка времени из-за атаки типа "отказ в обслуживании" обычно не вызывает катастрофического воздействия.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-109">However, the loss of MBAM functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="cbbfe-110">**Физическая защита компьютеров**.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-110">**Physically secure your computers**.</span></span> <span data-ttu-id="cbbfe-111">Безопасность не завершена без физического обеспечения безопасности.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-111">Security is incomplete without physical security.</span></span> <span data-ttu-id="cbbfe-112">Любой пользователь, имеющий физический доступ к серверу MBAM, может вызвать атаку на всю клиентскую базу.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-112">Anyone with physical access to an MBAM Server could potentially attack the entire client base.</span></span> <span data-ttu-id="cbbfe-113">Любые потенциальные физические атаки следует учитывать в случае высокой опасности и устранения соответствующих проблем.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-113">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="cbbfe-114">Серверы MBAM должны храниться в физически надежной серверной комнате с управляемым доступом.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-114">MBAM servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="cbbfe-115">Защитите эти компьютеры, если администраторы не находятся в физическом режиме, с помощью операционной системы и запирания компьютера или защищенной экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="cbbfe-116">**Установка последних обновлений для системы безопасности на всех компьютерах**.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="cbbfe-117">Получайте сведения о новых обновлениях для операционных систем, Microsoft SQL Server и MBAM, подписавшись на службу уведомлений системы безопасности ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="cbbfe-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="cbbfe-118">**Используйте надежные пароли и передавайте фразы**.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="cbbfe-119">Для всех учетных записей администраторов MBAM и MBAM следует использовать надежные пароли с 15 и более знаками.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="cbbfe-120">Никогда не используйте пустые пароли.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-120">Never use blank passwords.</span></span> <span data-ttu-id="cbbfe-121">Дополнительные сведения о концепциях паролей можно найти в статье "пароли и политики учетных записей" на сайте TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="cbbfe-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="cbbfe-122">Учетные записи и группы в MBAM</span><span class="sxs-lookup"><span data-stu-id="cbbfe-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="cbbfe-123">Рекомендации по управлению учетными записями пользователей — это создание глобальных групп домена и добавление в них учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-123">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="cbbfe-124">Затем добавьте глобальные учетные записи домена в необходимые локальные группы MBAM на серверах MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="cbbfe-125">Группы ActiveDirectoryDomainServices</span><span class="sxs-lookup"><span data-stu-id="cbbfe-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="cbbfe-126">Группы не создаются автоматически при настройке MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-126">No groups are created automatically during MBAM Setup.</span></span> <span data-ttu-id="cbbfe-127">Однако для управления операциями MBAM следует создать следующие глобальные группы ActiveDirectoryDomainServices.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-127">However, you should create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cbbfe-128">Имя группы</span><span class="sxs-lookup"><span data-stu-id="cbbfe-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="cbbfe-129">Сведения</span><span class="sxs-lookup"><span data-stu-id="cbbfe-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbbfe-130">MBAM опытных пользователей службы поддержки</span><span class="sxs-lookup"><span data-stu-id="cbbfe-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-131">Создайте эту группу, чтобы управлять членами локальной группы пользователей MBAM расширенной поддержки, созданной в ходе настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbbfe-132">Доступ к базе данных аудита для проверки соответствия MBAM</span><span class="sxs-lookup"><span data-stu-id="cbbfe-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-133">Создайте эту группу для управления участниками локальной группы доступа аудита соответствия MBAM, созданной в ходе настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbbfe-134">Пользователи MBAM оборудования</span><span class="sxs-lookup"><span data-stu-id="cbbfe-134">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-135">Создайте эту группу, чтобы управлять членами локальной группы пользователей MBAM оборудования, созданной в ходе настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-135">Create this group to manage members of the MBAM Hardware Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbbfe-136">Пользователи службы поддержки MBAM</span><span class="sxs-lookup"><span data-stu-id="cbbfe-136">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-137">Создайте эту группу, чтобы управлять членами локальной группы пользователей службы поддержки MBAM, созданной в ходе настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-137">Create this group to manage members of the MBAM Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbbfe-138">MBAM восстановления и доступа к БД оборудования</span><span class="sxs-lookup"><span data-stu-id="cbbfe-138">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-139">Создайте эту группу, чтобы управлять членами локальной группы доступа к восстановлению MBAM и данными об оборудовании, созданной в ходе настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-139">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbbfe-140">Пользователи отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="cbbfe-140">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-141">Создайте эту группу, чтобы управлять членами локальной группы пользователей отчета MBAM, созданной в ходе настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-141">Create this group to manage members of the MBAM Report Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbbfe-142">Системные администраторы MBAM</span><span class="sxs-lookup"><span data-stu-id="cbbfe-142">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-143">Создайте эту группу для управления членами локальной группы администраторов MBAM, созданной в ходе настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-143">Create this group to manage members of the MBAM System Administrators local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbbfe-144">Исключения шифрования BitLocker</span><span class="sxs-lookup"><span data-stu-id="cbbfe-144">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-145">Создайте эту группу для управления учетными записями пользователей, которые должны исключаться из шифрования BitLocker, начиная с компьютеров, на которых они вошли.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-145">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="cbbfe-146">Локальные группы сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="cbbfe-146">MBAM Server Local Groups</span></span>

<span data-ttu-id="cbbfe-147">Программа установки MBAM создает локальные группы для поддержки операций MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-147">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="cbbfe-148">Вы должны добавить глобальные группы ActiveDirectoryDomainServices в соответствующие локальные группы MBAM, чтобы настроить безопасность MBAM и разрешения на доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-148">You should add the ActiveDirectoryDomainServices Global Groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cbbfe-149">Имя группы</span><span class="sxs-lookup"><span data-stu-id="cbbfe-149">Group Name</span></span></th>
<th align="left"><span data-ttu-id="cbbfe-150">Сведения</span><span class="sxs-lookup"><span data-stu-id="cbbfe-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbbfe-151">MBAM опытных пользователей службы поддержки</span><span class="sxs-lookup"><span data-stu-id="cbbfe-151">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-152">Участники этой группы имеют расширенный доступ к функциям службы поддержки администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-152">Members of this group have expanded access to the Helpdesk features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbbfe-153">Доступ к базе данных аудита для проверки соответствия MBAM</span><span class="sxs-lookup"><span data-stu-id="cbbfe-153">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-154">В этой группе содержатся компьютеры, у которых есть доступ к базе данных аудита соответствия MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-154">This group contains the machines that have access to the MBAM Compliance Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbbfe-155">Пользователи MBAM оборудования</span><span class="sxs-lookup"><span data-stu-id="cbbfe-155">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-156">Участники этой группы имеют доступ к некоторым функциям аппаратных возможностей, имеющимся в разделе Администрирование и мониторинг Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-156">Members of this group have access to some of the Hardware Capability features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbbfe-157">Пользователи службы поддержки MBAM</span><span class="sxs-lookup"><span data-stu-id="cbbfe-157">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-158">Участники этой группы имеют доступ к некоторым функциям службы поддержки в центре администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-158">Members of this group have access to some of the Helpdesk features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbbfe-159">MBAM восстановления и доступа к БД оборудования</span><span class="sxs-lookup"><span data-stu-id="cbbfe-159">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-160">Эта группа содержит компьютеры, у которых есть доступ к базе данных восстановления MBAM и оборудованию.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-160">This group contains the computers that have access to the MBAM Recovery and Hardware Database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbbfe-161">Пользователи отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="cbbfe-161">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-162">Участники этой группы имеют доступ к отчетам о соответствии и аудиту в средствах администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-162">Members of this group have access to the Compliance and Audit reports from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbbfe-163">Системные администраторы MBAM</span><span class="sxs-lookup"><span data-stu-id="cbbfe-163">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbbfe-164">Участники этой группы имеют доступ ко всем функциям администрирования и наблюдения Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-164">Members of this group have access to all the features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="cbbfe-165">Учетная запись для доступа к отчетам SSRS</span><span class="sxs-lookup"><span data-stu-id="cbbfe-165">SSRS Reports Access Account</span></span>

<span data-ttu-id="cbbfe-166">Учетная запись службы отчетов служб SQL Server Reporting Services (SSRS) предоставляет контекст безопасности для выполнения отчетов MBAM, доступных через службы SSRS.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-166">The SQL Server Reporting Services (SSRS) Reports Service Account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="cbbfe-167">Эта учетная запись настраивается при настройке MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-167">This account is configured during MBAM Setup.</span></span>

## <span data-ttu-id="cbbfe-168">Файлы журнала MBAM</span><span class="sxs-lookup"><span data-stu-id="cbbfe-168">MBAM Log Files</span></span>


<span data-ttu-id="cbbfe-169">В процессе настройки MBAM в папке% TEMP% для пользователя, устанавливающего эту версию, создаются следующие файлы журнала установки.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-169">During MBAM Setup, the following MBAM Setup log files are created in the %temp% folder of the user who installs the</span></span>

**<span data-ttu-id="cbbfe-170">Файлы журнала установки MBAM Server</span><span class="sxs-lookup"><span data-stu-id="cbbfe-170">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="cbbfe-171">MSI <em> &lt; пять случайных знаков &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="cbbfe-171">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="cbbfe-172">Записываются в журнал действия, выполненные во время установки MBAM и установки компонентов сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-172">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="cbbfe-173">InstallComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="cbbfe-173">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="cbbfe-174">Заносит в журнал действия, предпринятые для создания настройки базы данных "состояние соответствия MBAM".</span><span class="sxs-lookup"><span data-stu-id="cbbfe-174">Logs the actions taken to create the MBAM Compliance Status database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="cbbfe-175">InstallKeyComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="cbbfe-175">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="cbbfe-176">Заносит в журнал действия, предпринятые для создания базы данных восстановления MBAM и конфигурации оборудования.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-176">Logs the actions taken to create the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="cbbfe-177">AddHelpDeskDbAuditUsers. log</span><span class="sxs-lookup"><span data-stu-id="cbbfe-177">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="cbbfe-178">Заносит в журнал действия, предпринятые для создания имен входа SQL Server в базе данных состояния соответствия MBAM и авторизации веб-службы поддержки в базу данных для отчетов.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-178">Logs the actions taken to create the SQL Server logins on the MBAM Compliance Status database and authorize helpdesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="cbbfe-179">AddHelpDeskDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="cbbfe-179">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="cbbfe-180">Заносит в журнал действия, предпринятые для авторизации веб-служб в базу данных для восстановления ключей и создают имена для входа в базу данных восстановления MBAM и оборудования.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-180">Logs the actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="cbbfe-181">AddKeyComplianceDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="cbbfe-181">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="cbbfe-182">Заносит в журнал действия, предпринятые для авторизации веб-служб на MBAM базы данных состояния соответствия требованиям для создания отчетов о соответствии.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-182">Logs the actions taken to authorize web services to MBAM Compliance Status database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="cbbfe-183">AddRecoveryAndHardwareDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="cbbfe-183">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="cbbfe-184">Заносит в журнал действия, предпринятые для авторизации веб-служб для MBAM восстановления и резервной конфигурации оборудования для восстановления ключей.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-184">Logs the actions taken to authorize web services to MBAM Recovery and Hardware database for key recovery.</span></span>

<span data-ttu-id="cbbfe-185">**Примечание**  Для получения дополнительных файлов журнала установки MBAM необходимо установить администрирование и мониторинг Microsoft BitLocker с помощью пакета **msiexec** и параметра **/l** &lt; Location &gt; .</span><span class="sxs-lookup"><span data-stu-id="cbbfe-185">**Note** In order to obtain additional MBAM Setup log files, you must install Microsoft BitLocker Administration and Monitoring by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="cbbfe-186">Файлы журнала создаются в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-186">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="cbbfe-187">Файлы журнала установки клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="cbbfe-187">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="cbbfe-188">MSI <em> &lt; пять случайных знаков &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="cbbfe-188">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="cbbfe-189">Записываются в журнал действия, выполненные во время установки клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-189">Logs the actions taken during MBAM Client installation.</span></span>

## <span data-ttu-id="cbbfe-190">Вопросы TDE базы данных MBAM</span><span class="sxs-lookup"><span data-stu-id="cbbfe-190">MBAM Database TDE considerations</span></span>


<span data-ttu-id="cbbfe-191">Функция шифрования прозрачных данных (TDE), доступная в SQL Server 2008, является обязательным условием установки для экземпляров базы данных, которые будут размещаться в MBAMных функциях базы данных.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-191">The Transparent Data Encryption (TDE) feature available in SQL Server 2008 is a required installation prerequisite for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="cbbfe-192">С помощью TDE можно выполнять полное шифрование на уровне базы данных в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-192">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="cbbfe-193">TDE является наилучшим вариантом массового шифрования для соответствия требованиям законодательства и корпоративным стандартам безопасности данных.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-193">TDE is a well-suited choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="cbbfe-194">TDE работает на уровне файла, который аналогичен двум функциям Windows: шифрованной файловой системе (EFS) и шифрованию диска BitLocker, в которых также шифруются данные на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-194">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="cbbfe-195">TDE не заменяет шифрование на уровне ячейки, EFS и BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-195">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="cbbfe-196">Если в базе данных включена TDE, все резервные копии шифруются.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-196">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="cbbfe-197">Таким образом, чтобы убедиться в том, что сертификат, использовавшийся для защиты ключа шифрования базы данных (DEK), должен быть архивирован и поддерживаться в резервной копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-197">Thus, special care must be taken to ensure that the certificate that was used to protect the Database Encryption Key (DEK) is backed up and maintained with the database backup.</span></span> <span data-ttu-id="cbbfe-198">Без сертификата данные будут нечитаемы.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-198">Without a certificate, the data will be unreadable.</span></span> <span data-ttu-id="cbbfe-199">Создавайте резервные копии сертификата вместе с базой данных.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-199">Back up the certificate along with the database.</span></span> <span data-ttu-id="cbbfe-200">Каждая резервная копия сертификата должна иметь два файла; Оба этих файла должны быть архивированы. Рекомендуется архивировать их отдельно от файла резервной копии базы данных для обеспечения безопасности.</span><span class="sxs-lookup"><span data-stu-id="cbbfe-200">Each certificate backup should have two files; both of these files should be archived .It is best to archive them separately from the database backup file for security.</span></span>

<span data-ttu-id="cbbfe-201">Пример включения TDE для экземпляров базы данных MBAM можно найти в разделе [Оценка MBAM 1,0](evaluating-mbam-10.md).</span><span class="sxs-lookup"><span data-stu-id="cbbfe-201">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 1.0](evaluating-mbam-10.md).</span></span>

<span data-ttu-id="cbbfe-202">Дополнительные сведения о TDE в SQLServer 2008 можно найти [в разделе Шифрование базы данных в SQL server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).</span><span class="sxs-lookup"><span data-stu-id="cbbfe-202">For more information about TDE in SQLServer 2008, see [Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).</span></span>

## <span data-ttu-id="cbbfe-203">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="cbbfe-203">Related topics</span></span>


[<span data-ttu-id="cbbfe-204">Безопасность и конфиденциальность для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="cbbfe-204">Security and Privacy for MBAM 1.0</span></span>](security-and-privacy-for-mbam-10.md)

 

 





