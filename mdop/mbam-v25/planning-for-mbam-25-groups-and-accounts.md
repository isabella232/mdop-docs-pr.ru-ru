---
title: Планирование групп и учетных записей MBAM 2.5
description: Планирование групп и учетных записей MBAM 2.5
author: dansimp
ms.assetid: 73bb9fe5-5900-4b6f-b271-ade62991fca1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 3431c3602685a4f96cb4c1333700107ba9c38b96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825802"
---
# <span data-ttu-id="dc279-103">Планирование групп и учетных записей MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="dc279-103">Planning for MBAM 2.5 Groups and Accounts</span></span>


<span data-ttu-id="dc279-104">В этой статье перечислены роли и учетные записи, которые необходимо создать в доменных службах Active Directory (AD DS) для предоставления доступа к базам данных администрирования и отчетов Microsoft BitLocker (MBAM), а также для просмотра и работы с отчетами и веб-приложениями.</span><span class="sxs-lookup"><span data-stu-id="dc279-104">This topic lists the roles and accounts that you must create in Active Directory Domain Services (AD DS) to provide security and access rights for the Microsoft BitLocker Administration and Monitoring (MBAM) databases, reports, and web applications.</span></span> <span data-ttu-id="dc279-105">Для каждой роли и учетной записи предоставляется соответствующее поле в мастере настройки сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc279-105">For each role and account, the corresponding field in the MBAM Server Configuration wizard is provided.</span></span> <span data-ttu-id="dc279-106">Список командлетов Windows PowerShell и параметров, соответствующих этим учетным записям, можно найти в разделе [Настройка функций сервера MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).</span><span class="sxs-lookup"><span data-stu-id="dc279-106">For a list of Windows PowerShell cmdlets and parameters that correspond to these accounts, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).</span></span>

**<span data-ttu-id="dc279-107">Примечание.</span><span class="sxs-lookup"><span data-stu-id="dc279-107">Note</span></span>**  
<span data-ttu-id="dc279-108">MBAM не поддерживает использование управляемых учетных записей служб.</span><span class="sxs-lookup"><span data-stu-id="dc279-108">MBAM does not support the use of managed service accounts.</span></span>



## <span data-ttu-id="dc279-109">Учетные записи базы данных</span><span class="sxs-lookup"><span data-stu-id="dc279-109">Database accounts</span></span>


<span data-ttu-id="dc279-110">Создайте следующие учетные записи для базы данных соответствия требованиям и аудита и базы данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="dc279-110">Create the following accounts for the Compliance and Audit Database and the Recovery Database.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dc279-111">Имя и назначение учетной записи</span><span class="sxs-lookup"><span data-stu-id="dc279-111">Account name and purpose</span></span></th>
<th align="left"><span data-ttu-id="dc279-112">Тип учетной записи</span><span class="sxs-lookup"><span data-stu-id="dc279-112">Account type</span></span></th>
<th align="left"><span data-ttu-id="dc279-113">Поле мастера конфигурации сервера MBAM, соответствующее данной учетной записи</span><span class="sxs-lookup"><span data-stu-id="dc279-113">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="dc279-114">Описание поля мастера конфигурации сервера MBAM, соответствующего данной учетной записи</span><span class="sxs-lookup"><span data-stu-id="dc279-114">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc279-115">Сведения о соответствии и аудите базы данных и базы данных для восстановления учетной записи пользователя или группы для отчетов</span><span class="sxs-lookup"><span data-stu-id="dc279-115">Compliance and Audit Database and Recovery Database read/write user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-116">Пользователь или группа</span><span class="sxs-lookup"><span data-stu-id="dc279-116">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-117">Пользователь или группа доступа для чтения и записи</span><span class="sxs-lookup"><span data-stu-id="dc279-117">Read/write access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-118">Пользователь или группа домена, у которых есть доступ на чтение и запись для базы данных соответствия и аудита, а также для базы данных восстановления, чтобы разрешить веб-приложениям доступ к данным и отчетам в этих базах данных.</span><span class="sxs-lookup"><span data-stu-id="dc279-118">Domain user or group that has read/write access to the Compliance and Audit Database and the Recovery Database to enable the web applications to access the data and reports in these databases.</span></span></p>
<p><span data-ttu-id="dc279-119">Если ввести имя пользователя в это поле, оно должно быть таким же, как значение в <strong> поле Учетная запись домена пула приложений веб-службы </strong> на <strong> странице Настройка веб-приложений </strong> .</span><span class="sxs-lookup"><span data-stu-id="dc279-119">If you enter a user name in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
<p><span data-ttu-id="dc279-120">Если в это поле вводится имя группы, значение в <strong> поле Учетная запись домена пула приложений веб-службы </strong> на <strong> странице Настройка веб-приложений </strong> должно быть членом группы, введенной в это поле.</span><span class="sxs-lookup"><span data-stu-id="dc279-120">If you enter a group name in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc279-121">Соответствие требованиям и аудит для базы данных пользователей и групп только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc279-121">Compliance and Audit Database read-only user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-122">Пользователь или группа</span><span class="sxs-lookup"><span data-stu-id="dc279-122">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-123">Пользователь или группа домена "доступ только для чтения"</span><span class="sxs-lookup"><span data-stu-id="dc279-123">Read-only access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-124">Имя пользователя или группы, которые будут иметь доступ к базе данных соответствия и аудита для доступа только для чтения, чтобы предоставить отчетам доступ к данным о соответствии и аудиту в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="dc279-124">Name of the user or group that will have read-only access to the Compliance and Audit Database to enable the reports to access the compliance and audit data in this database.</span></span></p>
<p><span data-ttu-id="dc279-125">Если ввести имя пользователя в это поле, оно должно быть тем же пользователем, который указан в <strong> поле Учетная запись домена базы данных "соответствие требованиям" и "Аудит" </strong> на <strong> странице "Настройка отчетов" </strong> .</span><span class="sxs-lookup"><span data-stu-id="dc279-125">If you enter a user name in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
<p><span data-ttu-id="dc279-126">Если ввести в это поле Имя группы, значение, указанное в <strong> поле Учетная запись домена базы данных "соответствие требованиям и аудиту" </strong> на <strong> странице "Настройка отчетов", </strong> должно входить в группу, указанную в этом поле.</span><span class="sxs-lookup"><span data-stu-id="dc279-126">If you enter a group name in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="dc279-127">Учетные записи отчетов</span><span class="sxs-lookup"><span data-stu-id="dc279-127">Reporting accounts</span></span>


<span data-ttu-id="dc279-128">Создайте следующие учетные записи для компонента Reports.</span><span class="sxs-lookup"><span data-stu-id="dc279-128">Create the following accounts for the Reports feature.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dc279-129">Имя или назначение учетной записи</span><span class="sxs-lookup"><span data-stu-id="dc279-129">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="dc279-130">Тип учетной записи</span><span class="sxs-lookup"><span data-stu-id="dc279-130">Account type</span></span></th>
<th align="left"><span data-ttu-id="dc279-131">Поле мастера конфигурации сервера MBAM, соответствующее данной учетной записи</span><span class="sxs-lookup"><span data-stu-id="dc279-131">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="dc279-132">Описание поля мастера конфигурации сервера MBAM, соответствующего данной учетной записи</span><span class="sxs-lookup"><span data-stu-id="dc279-132">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc279-133">Отчетная Группа доступа к домену, доступная только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc279-133">Reports read-only domain access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-134">Группа</span><span class="sxs-lookup"><span data-stu-id="dc279-134">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-135">Группа домена "роль отчета"</span><span class="sxs-lookup"><span data-stu-id="dc279-135">Reporting role domain group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-136">Указывает группу пользователей домена, которая имеет доступ к отчетам только для чтения на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="dc279-136">Specifies the domain user group that has read-only access to the reports in the Administration and Monitoring Website.</span></span> <span data-ttu-id="dc279-137">Указанная вами группа должна совпадать с группой, указанной в параметре "доступ только для чтения" для параметра "Группа доступа", если включены веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="dc279-137">The group you specify must be the same group you specified for the Reports Read Only Access Group parameter when the web apps are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc279-138">Учетная запись пользователя домена базы данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="dc279-138">Compliance and Audit Database domain user account</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-139">Пользователь</span><span class="sxs-lookup"><span data-stu-id="dc279-139">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-140">Учетная запись домена базы данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="dc279-140">Compliance and Audit Database domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-141">Учетная запись пользователя домена и пароль, которые локальный экземпляр служб SQL Server Reporting Services использует для доступа к базе данных соответствия и аудита.</span><span class="sxs-lookup"><span data-stu-id="dc279-141">Domain user account and password that the local SQL Server Reporting Services instance uses to access the Compliance and Audit Database.</span></span> <span data-ttu-id="dc279-142">Для этой учетной записи требуется <strong> Вход в качестве пакетных </strong> прав на сервере служб SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="dc279-142">This account requires <strong>Log On as Batch</strong> rights to the SQL Server Reporting Services server.</span></span></p>
<p><span data-ttu-id="dc279-143">Если значение, введенное в <strong> поле пользователя или группы домена "доступ только для чтения" </strong> на <strong> странице "Настройка баз данных" </strong> , является именем пользователя, необходимо ввести это же значение в это поле.</span><span class="sxs-lookup"><span data-stu-id="dc279-143">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user name, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="dc279-144">Если значение, введенное в <strong> поле пользователя или группы домена "доступ только для чтения" </strong> на <strong> странице "Настройка баз данных" </strong> , является именем группы, то значение, введенное в этом поле, должно быть членом этой группы.</span><span class="sxs-lookup"><span data-stu-id="dc279-144">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group name, the value that you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="dc279-145">Настройка пароля для этой учетной записи бессрочна.</span><span class="sxs-lookup"><span data-stu-id="dc279-145">Configure the password for this account to never expire.</span></span> <span data-ttu-id="dc279-146">Учетная запись пользователя должна иметь доступ ко всем данным, доступным группе "Пользователи отчетов MBAM".</span><span class="sxs-lookup"><span data-stu-id="dc279-146">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-helpdesk-roles"></a><span data-ttu-id="dc279-147">Учетные записи веб-сайта администрирования и мониторинга (службы поддержки)</span><span class="sxs-lookup"><span data-stu-id="dc279-147">Administration and Monitoring Website (Help Desk) accounts</span></span>


<span data-ttu-id="dc279-148">Создайте следующие учетные записи для веб-сайта администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="dc279-148">Create the following accounts for the Administration and Monitoring Website.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dc279-149">Имя или назначение учетной записи</span><span class="sxs-lookup"><span data-stu-id="dc279-149">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="dc279-150">Тип учетной записи</span><span class="sxs-lookup"><span data-stu-id="dc279-150">Account type</span></span></th>
<th align="left"><span data-ttu-id="dc279-151">Поле мастера конфигурации сервера MBAM, соответствующее данной учетной записи</span><span class="sxs-lookup"><span data-stu-id="dc279-151">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="dc279-152">Описание поля мастера конфигурации сервера MBAM, соответствующего данной учетной записи</span><span class="sxs-lookup"><span data-stu-id="dc279-152">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc279-153">Учетная запись домена пула приложений веб-службы</span><span class="sxs-lookup"><span data-stu-id="dc279-153">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-154">Пользователь</span><span class="sxs-lookup"><span data-stu-id="dc279-154">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-155">Учетная запись домена пула приложений веб-службы</span><span class="sxs-lookup"><span data-stu-id="dc279-155">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-156">Учетная запись пользователя домена, используемая пулом приложений для веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="dc279-156">Domain user account to be used by the application pool for the web applications.</span></span></p>
<p><span data-ttu-id="dc279-157">Если вы ввели имя пользователя в поле " <strong> пользователь или группа домена доступа для чтения и записи" </strong> на <strong> странице "Настройка баз данных" </strong> , необходимо ввести это же значение в это поле.</span><span class="sxs-lookup"><span data-stu-id="dc279-157">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="dc279-158">Если вы ввели имя группы в <strong> поле пользователя или группы домена "доступ для чтения и записи" </strong> на <strong> странице "Настройка баз данных" </strong> , то значение, введенное в этом поле, должно быть членом этой группы.</span><span class="sxs-lookup"><span data-stu-id="dc279-158">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="dc279-159">Если вы не указали учетные данные, будет использоваться учетная запись, указанная для любого ранее включенного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="dc279-159">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="dc279-160">Все веб-приложения должны использовать одни и те же учетные данные пула приложений.</span><span class="sxs-lookup"><span data-stu-id="dc279-160">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="dc279-161">Если вы укажете разные учетные данные для разных веб-приложений, будет использоваться Последнее указанное значение.</span><span class="sxs-lookup"><span data-stu-id="dc279-161">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="dc279-162">Важно.</span><span class="sxs-lookup"><span data-stu-id="dc279-162">Important</span></span></strong><br/><p><span data-ttu-id="dc279-163">Для повышения безопасности настройте учетную запись, указанную в учетных данных, с ограниченными правами пользователя.</span><span class="sxs-lookup"><span data-stu-id="dc279-163">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc279-164">Группа "MBAM" для опытных пользователей в службе поддержки</span><span class="sxs-lookup"><span data-stu-id="dc279-164">MBAM Advanced Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-165">Группа</span><span class="sxs-lookup"><span data-stu-id="dc279-165">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-166">MBAM опытных пользователей службы поддержки</span><span class="sxs-lookup"><span data-stu-id="dc279-166">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-167">Группа пользователей домена, у участников которой есть доступ ко всем областям восстановления на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="dc279-167">Domain user group whose members have access to all recovery areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="dc279-168">Пользователи с этой ролью должны вводить только ключ восстановления, а не домен и имя пользователя конечного пользователя, при помощи которых пользователи смогут восстановить свои диски.</span><span class="sxs-lookup"><span data-stu-id="dc279-168">Users who have this role have to enter only the recovery key, and not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="dc279-169">Если пользователь является членом обеих групп "Пользователи службы поддержки MBAM" и "Пользователи расширенной справочной службы", то разрешения группы "Пользователи расширенной поддержки" переопределяют разрешения для группы поддержки MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc279-169">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc279-170">Группа доступа пользователей службы поддержки MBAM</span><span class="sxs-lookup"><span data-stu-id="dc279-170">MBAM Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-171">Группа</span><span class="sxs-lookup"><span data-stu-id="dc279-171">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-172">Пользователи службы поддержки MBAM</span><span class="sxs-lookup"><span data-stu-id="dc279-172">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-173">Группа пользователей домена, у которых есть доступ к разделу Управление областями восстановления доверенных платформенных устройств и дисков на веб-сайте администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc279-173">Domain user group whose members have access to the Manage TPM and Drive Recovery areas of the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="dc279-174">Пользователи, которым назначена эта роль, должны заполнить все поля, включая домен и имя учетной записи пользователя, при использовании любого из этих параметров.</span><span class="sxs-lookup"><span data-stu-id="dc279-174">Individuals who have this role must fill-in all fields, including the end-user’s domain and account name, when they use either option.</span></span></p>
<p><span data-ttu-id="dc279-175">Если пользователь является членом обеих групп "Пользователи службы поддержки MBAM" и "Пользователи расширенной справочной службы", то разрешения группы "Пользователи расширенной поддержки" переопределяют разрешения для группы поддержки MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc279-175">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc279-176">Группа "Пользователи отчетов MBAM"</span><span class="sxs-lookup"><span data-stu-id="dc279-176">MBAM Report Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-177">Группа</span><span class="sxs-lookup"><span data-stu-id="dc279-177">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-178">Пользователи отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="dc279-178">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-179">Группа пользователей домена, у которой есть доступ только для чтения к отчетам в области "отчеты" на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="dc279-179">Domain user group whose members have read-only access to the reports in the Reports area of the Administration and Monitoring Website.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc279-180">Группа пользователей для миграции данных MBAM</span><span class="sxs-lookup"><span data-stu-id="dc279-180">MBAM Data Migration User Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-181">Группа</span><span class="sxs-lookup"><span data-stu-id="dc279-181">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-182">Пользователи MBAM миграции данных</span><span class="sxs-lookup"><span data-stu-id="dc279-182">MBAM Data Migration Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc279-183">Необязательная группа пользователей домена, у участников которой есть разрешения на запись данных в MBAM с помощью службы восстановления MBAM и оборудования, запущенного на сервере MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc279-183">Optional domain user group whose members have permissions to write data to MBAM by using the MBAM Recovery and Hardware Service running on the MBAM server.</span></span> <span data-ttu-id="dc279-184">Эта учетная запись обычно используется вместе с командлетами Write-MBAM \* для записи данных восстановления и доверенного платформенного модуля из Active Directory в базу данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc279-184">This account is generally used with the Write-Mbam\* cmdlets to write recovery and TPM data from Active Directory into the MBAM database.</span></span></p>
<p><span data-ttu-id="dc279-185">Дополнительные сведения можно найти в разделе <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> рекомендации по безопасности в MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="dc279-185">For more information, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="dc279-186">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="dc279-186">Related topics</span></span>


[<span data-ttu-id="dc279-187">Подготовка среды для развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="dc279-187">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="dc279-188">Необходимые условия для развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="dc279-188">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)



## <span data-ttu-id="dc279-189">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="dc279-189">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="dc279-190">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="dc279-190">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="dc279-191">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="dc279-191">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





