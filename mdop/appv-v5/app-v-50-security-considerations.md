---
title: Рекомендации по безопасности в App-V 5.0
description: Рекомендации по безопасности в App-V 5.0
author: dansimp
ms.assetid: 1e7292a0-7972-4b4f-85a9-eaf33f6c563a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fcd740345be7f532502b8996d8d2b1f4437ed6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814808"
---
# <span data-ttu-id="1bcda-103">Рекомендации по безопасности в App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="1bcda-103">App-V 5.0 Security Considerations</span></span>


<span data-ttu-id="1bcda-104">В этой статье содержится краткий обзор учетных записей и групп, файлов журналов и других вопросов, связанных с безопасностью для App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1bcda-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for App-V 5.0.</span></span>

**<span data-ttu-id="1bcda-105">Важно.</span><span class="sxs-lookup"><span data-stu-id="1bcda-105">Important</span></span>**  
<span data-ttu-id="1bcda-106">Приложение App-V 5,0 не является продуктом для обеспечения безопасности и не предоставляет никаких гарантий для безопасной среды.</span><span class="sxs-lookup"><span data-stu-id="1bcda-106">App-V 5.0 is not a security product and does not provide any guarantees for a secure environment.</span></span>



## <span data-ttu-id="1bcda-107">Функция PackageStoreAccessControl (PSAC) устарела</span><span class="sxs-lookup"><span data-stu-id="1bcda-107">PackageStoreAccessControl (PSAC) feature has been deprecated</span></span>


<span data-ttu-id="1bcda-108">В июне 2014 функция PackageStoreAccessControl (PSAC), которая была введена в Microsoft Application Virtualization (App-V) 5,0 с пакетом обновления 2 (SP2), устарела как для однопользовательского, так и для многопользовательского окружения.</span><span class="sxs-lookup"><span data-stu-id="1bcda-108">Effective as of June, 2014, the PackageStoreAccessControl (PSAC) feature that was introduced in Microsoft Application Virtualization (App-V) 5.0 Service Pack 2 (SP2) has been deprecated in both single-user and multi-user environments.</span></span>

## <span data-ttu-id="1bcda-109">Общие рекомендации по безопасности</span><span class="sxs-lookup"><span data-stu-id="1bcda-109">General security considerations</span></span>


**<span data-ttu-id="1bcda-110">Общие сведения о рисках для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="1bcda-110">Understand the security risks.</span></span>** <span data-ttu-id="1bcda-111">Наиболее серьезный риск для App-V 5,0 заключается в том, что его функции могут быть перехвачены неавторизованным пользователем, который затем может заново настроить данные ключа на клиентах App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1bcda-111">The most serious risk to App-V 5.0 is that its functionality could be hijacked by an unauthorized user who could then reconfigure key data on App-V 5.0 clients.</span></span> <span data-ttu-id="1bcda-112">Прекращение функциональных возможностей App-V 5,0 в течение короткого промежутка времени из-за атаки типа "отказ в обслуживании" обычно не вызывает катастрофического воздействия.</span><span class="sxs-lookup"><span data-stu-id="1bcda-112">The loss of App-V 5.0 functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="1bcda-113">**Физическая защита компьютеров**.</span><span class="sxs-lookup"><span data-stu-id="1bcda-113">**Physically secure your computers**.</span></span> <span data-ttu-id="1bcda-114">Безопасность не завершена без физического обеспечения безопасности.</span><span class="sxs-lookup"><span data-stu-id="1bcda-114">Security is incomplete without physical security.</span></span> <span data-ttu-id="1bcda-115">Любой пользователь, имеющий физический доступ к приложению App-V 5,0, может вызвать атаку на всю клиентскую базу.</span><span class="sxs-lookup"><span data-stu-id="1bcda-115">Anyone with physical access to an App-V 5.0 server could potentially attack the entire client base.</span></span> <span data-ttu-id="1bcda-116">Любые потенциальные физические атаки следует учитывать в случае высокой опасности и устранения соответствующих проблем.</span><span class="sxs-lookup"><span data-stu-id="1bcda-116">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="1bcda-117">Серверы App-V 5,0 должны храниться в физически надежной серверной комнате с управляемым доступом.</span><span class="sxs-lookup"><span data-stu-id="1bcda-117">App-V 5.0 servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="1bcda-118">Защитите эти компьютеры, если администраторы не находятся в физическом режиме, с помощью операционной системы и запирания компьютера или защищенной экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="1bcda-118">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="1bcda-119">**Установка последних обновлений для системы безопасности на всех компьютерах**.</span><span class="sxs-lookup"><span data-stu-id="1bcda-119">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="1bcda-120">Чтобы получать сведения о последних обновлениях для операционных систем, Microsoft SQL Server и App-V 5,0, подпишитесь на службу уведомлений системы безопасности ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="1bcda-120">To stay informed about the latest updates for operating systems, Microsoft SQL Server, and App-V 5.0, subscribe to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="1bcda-121">**Используйте надежные пароли и передавайте фразы**.</span><span class="sxs-lookup"><span data-stu-id="1bcda-121">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="1bcda-122">Всегда используйте надежные пароли с 15 и более знаками для всех учетных записей администраторов App-V 5,0 и App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1bcda-122">Always use strong passwords with 15 or more characters for all App-V 5.0 and App-V 5.0 administrator accounts.</span></span> <span data-ttu-id="1bcda-123">Никогда не используйте пустые пароли.</span><span class="sxs-lookup"><span data-stu-id="1bcda-123">Never use blank passwords.</span></span> <span data-ttu-id="1bcda-124">Дополнительные сведения о концепциях паролей можно найти в статье "пароли и политики учетных записей" на сайте TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="1bcda-124">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="1bcda-125">Учетные записи и группы в App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1bcda-125">Accounts and groups in App-V 5.0</span></span>


<span data-ttu-id="1bcda-126">Рекомендации по управлению учетными записями пользователей — это создание глобальных групп домена и добавление в них учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="1bcda-126">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="1bcda-127">Затем добавьте глобальные учетные записи домена в необходимые локальные группы App-V 5,0 на серверах App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1bcda-127">Then, add the domain global accounts to the necessary App-V 5.0 local groups on the App-V 5.0 servers.</span></span>

**<span data-ttu-id="1bcda-128">Примечание.</span><span class="sxs-lookup"><span data-stu-id="1bcda-128">Note</span></span>**  
<span data-ttu-id="1bcda-129">Учетные записи клиентских компьютеров App-V, которые должны подключаться к серверу публикаций, должны входить в локальную группу " **Пользователи** сервера публикаций".</span><span class="sxs-lookup"><span data-stu-id="1bcda-129">App-V client computer accounts that need to connect to the publishing server must be part of the publishing server’s **Users** local group.</span></span> <span data-ttu-id="1bcda-130">По умолчанию все компьютеры домена входят в группу " **Авторизованные пользователи** ", которая входит в локальную группу " **Пользователи** ".</span><span class="sxs-lookup"><span data-stu-id="1bcda-130">By default, all computers in the domain are part of the **Authorized Users** group, which is part of the **Users** local group.</span></span>



### <a href="" id="-------------app-v-5-0-server-security"></a> <span data-ttu-id="1bcda-131">Безопасность App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="1bcda-131">App-V 5.0 server security</span></span>

<span data-ttu-id="1bcda-132">При установке App-V 5,0 группы не создаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="1bcda-132">No groups are created automatically during App-V 5.0 Setup.</span></span> <span data-ttu-id="1bcda-133">Вы должны создать следующие глобальные группы доменных служб Active Directory для управления работой сервера App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1bcda-133">You should create the following Active Directory Domain Services global groups to manage App-V 5.0 server operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1bcda-134">Имя группы</span><span class="sxs-lookup"><span data-stu-id="1bcda-134">Group name</span></span></th>
<th align="left"><span data-ttu-id="1bcda-135">Сведения</span><span class="sxs-lookup"><span data-stu-id="1bcda-135">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bcda-136">Группа администраторов управления App-V</span><span class="sxs-lookup"><span data-stu-id="1bcda-136">App-V Management Admin group</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bcda-137">Используется для управления сервером управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1bcda-137">Used to manage the App-V 5.0 management server.</span></span> <span data-ttu-id="1bcda-138">Эта группа создается при установке сервера управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1bcda-138">This group is created during the App-V 5.0 Management Server installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1bcda-139">Важно.</span><span class="sxs-lookup"><span data-stu-id="1bcda-139">Important</span></span></strong><br/><p><span data-ttu-id="1bcda-140">После завершения установки вы не сможете создать группу с помощью консоли управления.</span><span class="sxs-lookup"><span data-stu-id="1bcda-140">There is no method to create the group using the management console after you have completed the installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1bcda-141">Учетная запись службы управления для чтения и записи базы данных</span><span class="sxs-lookup"><span data-stu-id="1bcda-141">Database read/write for Management Service account</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bcda-142">Предоставляет доступ к базе данных управления для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1bcda-142">Provides read/write access to the management database.</span></span> <span data-ttu-id="1bcda-143">Эта учетная запись должна создаваться во время установки базы данных системы управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1bcda-143">This account should be created during the App-V 5.0 management database installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bcda-144">Учетная запись администратора для установки службы управления App-V</span><span class="sxs-lookup"><span data-stu-id="1bcda-144">App-V Management Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1bcda-145">Примечание.</span><span class="sxs-lookup"><span data-stu-id="1bcda-145">Note</span></span></strong><br/><p><span data-ttu-id="1bcda-146">Это необходимо только в том случае, если база данных управления устанавливается отдельно от службы.</span><span class="sxs-lookup"><span data-stu-id="1bcda-146">This is only required if management database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="1bcda-147">Предоставляет общий доступ к таблице схемы-версии в базе данных управления.</span><span class="sxs-lookup"><span data-stu-id="1bcda-147">Provides public access to schema-version table in management database.</span></span> <span data-ttu-id="1bcda-148">Эта учетная запись должна создаваться во время установки базы данных системы управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1bcda-148">This account should be created during the App-V 5.0 management database installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1bcda-149">Учетная запись администратора установки службы отчетов App-V</span><span class="sxs-lookup"><span data-stu-id="1bcda-149">App-V Reporting Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1bcda-150">Примечание.</span><span class="sxs-lookup"><span data-stu-id="1bcda-150">Note</span></span></strong><br/><p><span data-ttu-id="1bcda-151">Это необходимо только в том случае, если база данных отчетов устанавливается отдельно от службы.</span><span class="sxs-lookup"><span data-stu-id="1bcda-151">This is only required if reporting database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="1bcda-152">Открытый доступ к таблице схемы-версии в базе данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="1bcda-152">Public access to schema-version table in reporting database.</span></span> <span data-ttu-id="1bcda-153">Эта учетная запись должна создаваться при установке базы данных Reporting App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1bcda-153">This account should be created during the App-V 5.0 reporting database installation.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="1bcda-154">Рассматривайте следующие дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="1bcda-154">Consider the following additional information:</span></span>

-   <span data-ttu-id="1bcda-155">Доступ к общим ресурсам пакета: Если общий доступ находится на том же компьютере, что и сервер управления, **Сетевая** служба должна иметь доступ на чтение к общему ресурсу.</span><span class="sxs-lookup"><span data-stu-id="1bcda-155">Access to the package shares - If a share exists on the same computer as the management Server, the **Network** service requires read access to the share.</span></span> <span data-ttu-id="1bcda-156">Кроме того, на каждом клиентском компьютере App-V должен быть доступ на чтение к общему доступу к пакету.</span><span class="sxs-lookup"><span data-stu-id="1bcda-156">In addition, each App-V client computer must have read access to the package share.</span></span>

    **<span data-ttu-id="1bcda-157">Примечание.</span><span class="sxs-lookup"><span data-stu-id="1bcda-157">Note</span></span>**  
    <span data-ttu-id="1bcda-158">В предыдущих версиях App-V общий доступ к пакетам назывался общим контентом.</span><span class="sxs-lookup"><span data-stu-id="1bcda-158">In previous versions of App-V, package share was referred to as content share.</span></span>



-   <span data-ttu-id="1bcda-159">Регистрация серверов публикаций с помощью сервера управления: сервер публикаций должен быть зарегистрирован на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="1bcda-159">Registering publishing servers with Management Server - A publishing server must be registered with the Management server.</span></span> <span data-ttu-id="1bcda-160">Например, его необходимо добавить в базу данных, чтобы учетные записи сервера публикации могли обращаться к API-интерфейсу службы управления.</span><span class="sxs-lookup"><span data-stu-id="1bcda-160">For example, it must be added to the database, so that the Publishing server machine accounts are able to call into the Management service API.</span></span>

### <a href="" id="-------------app-v-5-0-package-security"></a> <span data-ttu-id="1bcda-161">Безопасность пакета App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1bcda-161">App-V 5.0 package security</span></span>

<span data-ttu-id="1bcda-162">Ниже приведены сведения о том, как обеспечить безопасность виртуализированных пакетов.</span><span class="sxs-lookup"><span data-stu-id="1bcda-162">The following will help you plan how to ensure that virtualized packages are secure.</span></span>

-   <span data-ttu-id="1bcda-163">Если установщик приложения применяет список управления доступом (ACL) к файлу или каталогу, этот список ACL не сохраняется в пакете.</span><span class="sxs-lookup"><span data-stu-id="1bcda-163">If an application installer applies an access control list (ACL) to a file or directory, then that ACL is not persisted in the package.</span></span> <span data-ttu-id="1bcda-164">Если при развертывании пакета этот файл или каталог изменяется пользователем, он либо наследует список ACL от **% UserProfile%** , либо наследует список ACL для каталога целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="1bcda-164">When the package is deployed, if the file or directory is modified by a user it will either inherit the ACL in the **%userprofile%** or inherit the ACL of the target computer’s directory.</span></span> <span data-ttu-id="1bcda-165">Первый случай происходит в том случае, если файл или каталог не существует в виртуальной файловой системе. в последнем случае это случается, если файл или каталог находятся в папке виртуальной файловой системы, например **% WINDIR%**.</span><span class="sxs-lookup"><span data-stu-id="1bcda-165">The former case occurs if the file or directory does not exist in a virtual file system location; the latter case occurs if the file or directory exists in a virtual file system location, for example **%windir%**.</span></span>

## <a href="" id="---------app-v-5-0-log-files"></a> <span data-ttu-id="1bcda-166">Файлы журнала App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1bcda-166">App-V 5.0 log files</span></span>


<span data-ttu-id="1bcda-167">Во время установки App-V 5,0 файлы журнала программы установки создаются в папке **% TEMP%** для пользователя, выполняющего установку.</span><span class="sxs-lookup"><span data-stu-id="1bcda-167">During App-V 5.0 Setup, setup log files are created in the **%temp%** folder of the installing user.</span></span>
