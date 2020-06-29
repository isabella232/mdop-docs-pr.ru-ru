---
title: Проверка разделов реестра перед установкой сервера App-V 5.x
description: Проверка разделов реестра перед установкой сервера App-V 5.x
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814709"
---
# <span data-ttu-id="958b3-103">Проверка разделов реестра перед установкой сервера App-V 5.x</span><span class="sxs-lookup"><span data-stu-id="958b3-103">Check Registry Keys before installing App-V 5.x Server</span></span>

<span data-ttu-id="958b3-104">Если вы обновляете приложение App-V 5,0 с пакетом обновления 1 (SP1) или более поздней версии, выполните действия, описанные в этом разделе, перед установкой сервера App-V 5. x</span><span class="sxs-lookup"><span data-stu-id="958b3-104">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in this section before installing the App-V 5.x Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="958b3-105">Если это действие является обязательным</span><span class="sxs-lookup"><span data-stu-id="958b3-105">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="958b3-106">Вы обновляете приложение App-V 5,0 SP1 со всеми последующими пакетами исправлений, которые вы установили с помощью MSP-файла.</span><span class="sxs-lookup"><span data-stu-id="958b3-106">You are upgrading from App-V 5.0 SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="958b3-107">В каких компонентах требуется выполнить это действие</span><span class="sxs-lookup"><span data-stu-id="958b3-107">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="958b3-108">Только обновляемые серверные компоненты App-V.</span><span class="sxs-lookup"><span data-stu-id="958b3-108">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="958b3-109">Если вам понадобится это действие</span><span class="sxs-lookup"><span data-stu-id="958b3-109">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="958b3-110">Перед обновлением сервера App-V на App-V 5. x</span><span class="sxs-lookup"><span data-stu-id="958b3-110">Before you upgrade the App-V Server to App-V 5.x</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="958b3-111">Что вам нужно сделать?</span><span class="sxs-lookup"><span data-stu-id="958b3-111">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="958b3-112">С помощью сведений, указанных в приведенных ниже таблицах, обновите значение каждого раздела реестра в соответствии <code>HKLM\Software\Microsoft\AppV\Server</code> со значением, которое вы указали при первоначальной установке сервера.</span><span class="sxs-lookup"><span data-stu-id="958b3-112">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="958b3-113">При выполнении этого шага восстанавливаются значения реестра, которые могут быть удалены, если установлены пакеты исправлений App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="958b3-113">Completing this step restores registry values that may have been removed when App-V 5.0 SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="958b3-114">Клавиша ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="958b3-114">ManagementDatabase key</span></span>**

<span data-ttu-id="958b3-115">Если вы устанавливаете базу данных управления, настройте эти разделы реестра в разделе `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .</span><span class="sxs-lookup"><span data-stu-id="958b3-115">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="958b3-116">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="958b3-116">Key name</span></span></th>
<th align="left"><span data-ttu-id="958b3-117">Описание</span><span class="sxs-lookup"><span data-stu-id="958b3-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="958b3-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="958b3-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-119">Указывает, требуется ли учетной записи Public Access для доступа к нелокальным базам данных управления.</span><span class="sxs-lookup"><span data-stu-id="958b3-119">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="958b3-120">Если требуется, для параметра value задано значение "1".</span><span class="sxs-lookup"><span data-stu-id="958b3-120">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="958b3-121">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="958b3-121">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-122">Имя базы данных управления.</span><span class="sxs-lookup"><span data-stu-id="958b3-122">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="958b3-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="958b3-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-124">Учетная запись, используемая для чтения (общедоступной) доступа к базе данных управления.</span><span class="sxs-lookup"><span data-stu-id="958b3-124">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="958b3-125">Используется, если <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="958b3-125">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="958b3-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="958b3-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-127">Идентификатор безопасности (SID) учетной записи, используемой для чтения (общедоступного) доступа к базе данных управления.</span><span class="sxs-lookup"><span data-stu-id="958b3-127">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="958b3-128">Используется, если <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="958b3-128">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="958b3-129">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="958b3-129">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-130">Экземпляр SQL Server для базы данных управления.</span><span class="sxs-lookup"><span data-stu-id="958b3-130">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="958b3-131">Если значение пусто, используется экземпляр базы данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="958b3-131">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="958b3-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="958b3-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-133">Учетная запись, используемая для доступа на запись (администратора) к базе данных управления.</span><span class="sxs-lookup"><span data-stu-id="958b3-133">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="958b3-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="958b3-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-135">Идентификатор безопасности (SID) учетной записи, используемой для доступа записи (администратора) к базе данных управления.</span><span class="sxs-lookup"><span data-stu-id="958b3-135">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="958b3-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="958b3-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-137">Учетная запись удаленного компьютера сервера управления (домен \ учетная_запись).</span><span class="sxs-lookup"><span data-stu-id="958b3-137">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="958b3-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="958b3-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-139">Учетная запись администратора установки для сервера управления (домен \ учетная_запись).</span><span class="sxs-lookup"><span data-stu-id="958b3-139">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="958b3-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="958b3-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-141">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="958b3-141">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="958b3-142">1 </strong> – Служба управления находится на локальном компьютере, то есть MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT пуста.</span><span class="sxs-lookup"><span data-stu-id="958b3-142">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="958b3-143">0 </strong> - Служба управления находится на другом компьютере, а не на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="958b3-143">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="958b3-144">Клавиша ManagementService</span><span class="sxs-lookup"><span data-stu-id="958b3-144">ManagementService key</span></span>**

<span data-ttu-id="958b3-145">Если вы устанавливаете сервер управления, настройте эти разделы реестра в разделе `HKLM\Software\Microsoft\AppV\Server\ManagementService` .</span><span class="sxs-lookup"><span data-stu-id="958b3-145">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="958b3-146">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="958b3-146">Key name</span></span></th>
<th align="left"><span data-ttu-id="958b3-147">Описание</span><span class="sxs-lookup"><span data-stu-id="958b3-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="958b3-148">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="958b3-148">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-149">Группа доменных служб Active Directory (AD DS) или учетная запись, которой разрешено управлять App-V (домен \ учетная_запись).</span><span class="sxs-lookup"><span data-stu-id="958b3-149">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="958b3-150">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="958b3-150">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-151">Экземпляр SQL Server, содержащий базу данных управления.</span><span class="sxs-lookup"><span data-stu-id="958b3-151">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="958b3-152">Если значение пусто, используется экземпляр базы данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="958b3-152">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="958b3-153">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="958b3-153">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-154">Имя удаленного сервера SQL Server с базой данных управления.</span><span class="sxs-lookup"><span data-stu-id="958b3-154">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="958b3-155">Если значение пусто, используется локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="958b3-155">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="958b3-156">Клавиша ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="958b3-156">ReportingDatabase key</span></span>**

<span data-ttu-id="958b3-157">Если вы устанавливаете базу данных отчетов, настройте эти разделы реестра в разделе `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .</span><span class="sxs-lookup"><span data-stu-id="958b3-157">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="958b3-158">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="958b3-158">Key name</span></span></th>
<th align="left"><span data-ttu-id="958b3-159">Описание</span><span class="sxs-lookup"><span data-stu-id="958b3-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="958b3-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="958b3-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-161">Указывает, требуется ли учетной записи Public Access для доступа к нелокальным базам данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="958b3-161">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="958b3-162">Если требуется, для параметра value задано значение "1".</span><span class="sxs-lookup"><span data-stu-id="958b3-162">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="958b3-163">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="958b3-163">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-164">Имя базы данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="958b3-164">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="958b3-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="958b3-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-166">Учетная запись, используемая для чтения (общего доступа) к базе данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="958b3-166">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="958b3-167">Используется, если <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="958b3-167">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="958b3-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="958b3-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-169">Идентификатор безопасности (SID) учетной записи, используемой для чтения (общедоступного) доступа к базе данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="958b3-169">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="958b3-170">Используется, если <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="958b3-170">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="958b3-171">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="958b3-171">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-172">Экземпляр SQL Server для базы данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="958b3-172">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="958b3-173">Если значение пусто, используется экземпляр базы данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="958b3-173">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="958b3-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="958b3-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="958b3-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="958b3-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="958b3-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="958b3-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-177">Учетная запись удаленного компьютера сервера отчетов (домен \ учетная_запись).</span><span class="sxs-lookup"><span data-stu-id="958b3-177">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="958b3-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="958b3-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-179">Учетная запись администратора установки для сервера отчетов (домен \ учетная_запись).</span><span class="sxs-lookup"><span data-stu-id="958b3-179">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="958b3-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="958b3-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-181">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="958b3-181">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="958b3-182">1 </strong> – Служба отчетов находится на локальном компьютере, то есть REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT пустая.</span><span class="sxs-lookup"><span data-stu-id="958b3-182">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="958b3-183">0 </strong> - Служба отчетов находится на другом компьютере, а не на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="958b3-183">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="958b3-184">Клавиша ReportingService</span><span class="sxs-lookup"><span data-stu-id="958b3-184">ReportingService key</span></span>**

<span data-ttu-id="958b3-185">Если вы устанавливаете сервер отчетов, настройте эти разделы реестра в разделе `HKLM\Software\Microsoft\AppV\Server\ReportingService` .</span><span class="sxs-lookup"><span data-stu-id="958b3-185">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="958b3-186">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="958b3-186">Key name</span></span></th>
<th align="left"><span data-ttu-id="958b3-187">Описание</span><span class="sxs-lookup"><span data-stu-id="958b3-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="958b3-188">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="958b3-188">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-189">Экземпляр SQL Server для базы данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="958b3-189">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="958b3-190">Если значение пусто, используется экземпляр базы данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="958b3-190">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="958b3-191">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="958b3-191">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="958b3-192">Имя удаленного сервера SQL Server с базой данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="958b3-192">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="958b3-193">Если значение пусто, используется локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="958b3-193">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>

