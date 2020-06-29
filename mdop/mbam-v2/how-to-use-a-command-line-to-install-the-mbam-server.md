---
title: Использование командной строки для установки сервера MBAM
description: Использование командной строки для установки сервера MBAM
author: dansimp
ms.assetid: 6ffc6d41-a793-42c2-b997-95ba47550648
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a689a2df77300300073b2731281004feac87305f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825642"
---
# <span data-ttu-id="fdf66-103">Использование командной строки для установки сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="fdf66-103">How to Use a Command Line to Install the MBAM Server</span></span>


<span data-ttu-id="fdf66-104">Вы можете использовать командную строку для установки сервера MBAM с помощью изолированной топологии или Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fdf66-104">You can use a command line to install the MBAM Server with either the Stand-alone or Configuration Manager topology.</span></span> <span data-ttu-id="fdf66-105">Следующий пример командной строки предназначен для развертывания MBAM на одном сервере, который является архитектурой, которая должна использоваться только в тестовой среде.</span><span class="sxs-lookup"><span data-stu-id="fdf66-105">The following command line example is for deploying MBAM on a single server, which is an architecture that should be used only in a test environment.</span></span> <span data-ttu-id="fdf66-106">При развертывании MBAM в рабочей среде, которая должна иметь несколько серверов, необходимо изменить командную строку соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="fdf66-106">You will need to change the command line accordingly when you deploy MBAM to a production environment, which should have multiple servers.</span></span>

## <span data-ttu-id="fdf66-107">Командная строка для развертывания сервера MBAM 2.0 с изолированной топологией</span><span class="sxs-lookup"><span data-stu-id="fdf66-107">Command Line for Deploying the MBAM2.0 Server with the Stand-alone Topology</span></span>


<span data-ttu-id="fdf66-108">Чтобы установить сервер MBAM с изолированной топологией, можно использовать командную строку, подобную приведенной ниже.</span><span class="sxs-lookup"><span data-stu-id="fdf66-108">You can use a command line that is similar to the following to install the MBAM Server with the Stand-alone topology.</span></span>

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="fdf66-109">В приведенной ниже таблице описаны параметры командной строки для развертывания сервера MBAM с изолированной топологией.</span><span class="sxs-lookup"><span data-stu-id="fdf66-109">The following table describes the command line parameters for deploying the MBAM Server with the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fdf66-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="fdf66-110">Parameter</span></span></th>
<th align="left"><span data-ttu-id="fdf66-111">Значение параметра</span><span class="sxs-lookup"><span data-stu-id="fdf66-111">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="fdf66-112">Описание</span><span class="sxs-lookup"><span data-stu-id="fdf66-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdf66-113">TOPOLOGY</span><span class="sxs-lookup"><span data-stu-id="fdf66-113">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-114">до</span><span class="sxs-lookup"><span data-stu-id="fdf66-114">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-115">0 — изолированная топология</span><span class="sxs-lookup"><span data-stu-id="fdf66-115">0 – Stand-alone topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdf66-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="fdf66-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-117">ведение</span><span class="sxs-lookup"><span data-stu-id="fdf66-117">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-118">0 – не принимайте лицензию agreement1 – принимайте условия лицензионного соглашения</span><span class="sxs-lookup"><span data-stu-id="fdf66-118">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdf66-119">ADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="fdf66-119">ADDLOCAL</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fdf66-120">Компоненты, устанавливаемые на сервере</span><span class="sxs-lookup"><span data-stu-id="fdf66-120">Features to be installed on the Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fdf66-121">KeyDatabase</span><span class="sxs-lookup"><span data-stu-id="fdf66-121">KeyDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-122">База данных восстановления</span><span class="sxs-lookup"><span data-stu-id="fdf66-122">Recovery Database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fdf66-123">ReportsDatabase</span><span class="sxs-lookup"><span data-stu-id="fdf66-123">ReportsDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-124">База данных отчетов о сертификации и аудите</span><span class="sxs-lookup"><span data-stu-id="fdf66-124">Compliance and Audit Reports Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fdf66-125">Отчеты</span><span class="sxs-lookup"><span data-stu-id="fdf66-125">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-126">Отчеты о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="fdf66-126">Compliance and Audit Reports</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fdf66-127">AdministrationMonitoringServer</span><span class="sxs-lookup"><span data-stu-id="fdf66-127">AdministrationMonitoringServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-128">Веб-сайт администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="fdf66-128">Administration and Monitoring website</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fdf66-129">SelfServiceServer</span><span class="sxs-lookup"><span data-stu-id="fdf66-129">SelfServiceServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-130">Портал самообслуживания</span><span class="sxs-lookup"><span data-stu-id="fdf66-130">Self-Service Portal</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fdf66-131">PolicyTemplate</span><span class="sxs-lookup"><span data-stu-id="fdf66-131">PolicyTemplate</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-132">Шаблон групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="fdf66-132">MBAM Group Policy template</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdf66-133">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="fdf66-133">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-134">[UserDomain] [UserName1]</span><span class="sxs-lookup"><span data-stu-id="fdf66-134">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-135">Домен и учетная запись пользователя для учетной записи служб Reporting Services, которая будет обращаться к базе данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="fdf66-135">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdf66-136">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="fdf66-136">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-137">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="fdf66-137">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-138">Пароль учетной записи служб Reporting Services, которая будет обращаться к базе данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="fdf66-138">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdf66-139">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="fdf66-139">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-140">ComputerName</span><span class="sxs-lookup"><span data-stu-id="fdf66-140">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-141">Имя экземпляра SQL Server для базы данных соответствия требованиям и аудита — замените <strong> % ComputerName% </strong> именем компьютера</span><span class="sxs-lookup"><span data-stu-id="fdf66-141">SQL Server instance name for the Compliance and Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdf66-142">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="fdf66-142">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-143">ComputerName</span><span class="sxs-lookup"><span data-stu-id="fdf66-143">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-144">Имя экземпляра SQL Server для базы данных восстановления — замените <strong> % ComputerName% </strong> именем компьютера</span><span class="sxs-lookup"><span data-stu-id="fdf66-144">SQL Server instance name for the Recovery Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdf66-145">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="fdf66-145">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-146">ComputerName</span><span class="sxs-lookup"><span data-stu-id="fdf66-146">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-147">Экземпляр сервера SQL Server Reporting Server, на котором будут установлены отчеты о соответствии и аудите — замените <strong> % ComputerName% на </strong> имя компьютера</span><span class="sxs-lookup"><span data-stu-id="fdf66-147">SQL Server Reporting Server instance where the Compliance and Audit reports will be installed – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdf66-148">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="fdf66-148">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-149">83</span><span class="sxs-lookup"><span data-stu-id="fdf66-149">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-150">Порт для веб-сайта администрирования и наблюдения; "83" — это только пример</span><span class="sxs-lookup"><span data-stu-id="fdf66-150">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdf66-151">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="fdf66-151">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-152">83</span><span class="sxs-lookup"><span data-stu-id="fdf66-152">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-153">Порт для веб-сайта портала самообслуживания; "83" — это только пример</span><span class="sxs-lookup"><span data-stu-id="fdf66-153">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fdf66-154">Командная строка для развертывания сервера MBAM 2.0 с топологией Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="fdf66-154">Command Line for Deploying the MBAM2.0 Server with the Configuration Manager Topology</span></span>


<span data-ttu-id="fdf66-155">Для установки сервера MBAM с топологией Configuration Manager можно использовать командную строку, подобную приведенной ниже.</span><span class="sxs-lookup"><span data-stu-id="fdf66-155">You can use a command line that is similar to the following to install the MBAM Server with the Configuration Manager topology.</span></span>

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="fdf66-156">В приведенной ниже таблице описаны параметры командной строки для установки сервера MBAM 2.0 с топологией Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fdf66-156">The following table describes the command line parameters for installing the MBAM2.0 Server with the Configuration Manager topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fdf66-157">Параметр</span><span class="sxs-lookup"><span data-stu-id="fdf66-157">Parameter</span></span></th>
<th align="left"><span data-ttu-id="fdf66-158">Значение параметра</span><span class="sxs-lookup"><span data-stu-id="fdf66-158">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="fdf66-159">Описание</span><span class="sxs-lookup"><span data-stu-id="fdf66-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdf66-160">TOPOLOGY</span><span class="sxs-lookup"><span data-stu-id="fdf66-160">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-161">1,1</span><span class="sxs-lookup"><span data-stu-id="fdf66-161">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-162">1 — топология Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="fdf66-162">1 – Configuration Manager topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdf66-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="fdf66-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-164">ведение</span><span class="sxs-lookup"><span data-stu-id="fdf66-164">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-165">0 – не принимайте лицензию agreement1 – принимайте условия лицензионного соглашения</span><span class="sxs-lookup"><span data-stu-id="fdf66-165">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdf66-166">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="fdf66-166">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-167">ComputerName</span><span class="sxs-lookup"><span data-stu-id="fdf66-167">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-168">Имя экземпляра SQL Server для базы данных аудита — замените <strong> % ComputerName% </strong> именем компьютера</span><span class="sxs-lookup"><span data-stu-id="fdf66-168">SQL Server instance name for the Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdf66-169">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="fdf66-169">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-170">ComputerName</span><span class="sxs-lookup"><span data-stu-id="fdf66-170">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-171">Имя экземпляра SQL Server для базы данных восстановления — замените <strong> % ComputerName% </strong> именем компьютера</span><span class="sxs-lookup"><span data-stu-id="fdf66-171">SQL Server instance name for the Recovery Database - replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdf66-172">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="fdf66-172">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-173">ComputerName</span><span class="sxs-lookup"><span data-stu-id="fdf66-173">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-174">Экземпляр сервера SQL Server Reporting Server, на котором будут установлены отчеты аудита — замена% ComputerName% на имя компьютера</span><span class="sxs-lookup"><span data-stu-id="fdf66-174">SQL Server Reporting Server instance where the Audit reports will be installed – replace %computername% with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdf66-175">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="fdf66-175">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-176">[UserDomain] [UserName1]</span><span class="sxs-lookup"><span data-stu-id="fdf66-176">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-177">Домен и учетная запись пользователя для учетной записи служб Reporting Services, которая будет обращаться к базе данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="fdf66-177">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdf66-178">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="fdf66-178">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-179">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="fdf66-179">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-180">Пароль учетной записи служб Reporting Services, которая будет обращаться к базе данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="fdf66-180">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdf66-181">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="fdf66-181">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-182">83</span><span class="sxs-lookup"><span data-stu-id="fdf66-182">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-183">Порт для веб-сайта администрирования и наблюдения; "83" — это только пример</span><span class="sxs-lookup"><span data-stu-id="fdf66-183">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdf66-184">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="fdf66-184">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-185">83</span><span class="sxs-lookup"><span data-stu-id="fdf66-185">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdf66-186">Порт для веб-сайта портала самообслуживания; "83" — это только пример</span><span class="sxs-lookup"><span data-stu-id="fdf66-186">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fdf66-187">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="fdf66-187">Related topics</span></span>


[<span data-ttu-id="fdf66-188">Развертывание инфраструктуры сервера MBAM 2.0 Server</span><span class="sxs-lookup"><span data-stu-id="fdf66-188">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





