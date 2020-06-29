---
title: Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций
description: Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825999"
---
# <span data-ttu-id="039d6-103">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="039d6-103">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>


<span data-ttu-id="039d6-104">Прежде чем приступить к установке Microsoft BitLocker Administration и Monitoring (MBAM), необходимо выполнить необходимые требования, описанные в этой статье.</span><span class="sxs-lookup"><span data-stu-id="039d6-104">Before starting the Microsoft BitLocker Administration and Monitoring (MBAM) installation, you must complete the prerequisites listed in this topic.</span></span> <span data-ttu-id="039d6-105">Эти требования применимы к изолированной топологии MBAM и топологии интеграции System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="039d6-105">These prerequisites apply to the MBAM Stand-alone topology and System Center Configuration Manager Integration topology.</span></span>

<span data-ttu-id="039d6-106">Если вы развертываете MBAM с помощью System Center Configuration Manager, необходимо выполнить дополнительные требования, которые указаны в [требованиях к топологии интеграции Configuration Manager для MBAM 2,5 Server](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="039d6-106">If you are deploying MBAM with System Center Configuration Manager, you must complete additional prerequisites, which are listed in [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="039d6-107">Список поддерживаемых аппаратных и операционных систем для MBAM можно найти в разделе [Поддерживаемые конфигурации MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="039d6-107">For a list of the supported hardware and operating systems for MBAM, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="039d6-108">Важно.</span><span class="sxs-lookup"><span data-stu-id="039d6-108">Important</span></span>**  
<span data-ttu-id="039d6-109">Если вы используете BitLocker без MBAM, необходимо дешифровать диск и затем очистить TPM с помощью TPM. msc.</span><span class="sxs-lookup"><span data-stu-id="039d6-109">If BitLocker was used without MBAM, you must decrypt the drive and then clear TPM using tpm.msc.</span></span> <span data-ttu-id="039d6-110">MBAM не может сменить владельца доверенного платформенного модуля, если клиентский компьютер уже зашифрован и пароль владельца доверенного платформенного модуля создан.</span><span class="sxs-lookup"><span data-stu-id="039d6-110">MBAM cannot take ownership of TPM if the client PC is already encrypted and the TPM owner password created.</span></span>



## <span data-ttu-id="039d6-111">Обязательные роли MBAM и учетные записи</span><span class="sxs-lookup"><span data-stu-id="039d6-111">Required MBAM roles and accounts</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="039d6-112">Предварительные</span><span class="sxs-lookup"><span data-stu-id="039d6-112">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="039d6-113">Сведения</span><span class="sxs-lookup"><span data-stu-id="039d6-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-114">Группы, созданные в доменных службах Active Directory (AD DS)</span><span class="sxs-lookup"><span data-stu-id="039d6-114">Groups created in Active Directory Domain Services (AD DS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-115"><a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"> </a> Описание этих групп и учетных записей MBAM в разделе планирование групп 2,5 и учетных записей.</span><span class="sxs-lookup"><span data-stu-id="039d6-115">See <a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)">Planning for MBAM 2.5 Groups and Accounts</a> for a description of these groups and accounts.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="039d6-116">Предварительные условия для базы данных восстановления</span><span class="sxs-lookup"><span data-stu-id="039d6-116">Prerequisites for the Recovery Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="039d6-117">Предварительные</span><span class="sxs-lookup"><span data-stu-id="039d6-117">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="039d6-118">Сведения</span><span class="sxs-lookup"><span data-stu-id="039d6-118">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-119">Поддерживаемая версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="039d6-119">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-120">Установка Microsoft SQL Server с SQL_Latin1_General_CP1_CI_AS параметрами сортировки.</span><span class="sxs-lookup"><span data-stu-id="039d6-120">Install Microsoft SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="039d6-121">Поддерживаемые <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="039d6-121">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="039d6-122">Требуемые разрешения SQL Server</span><span class="sxs-lookup"><span data-stu-id="039d6-122">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-123">Необходимые разрешения:</span><span class="sxs-lookup"><span data-stu-id="039d6-123">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="039d6-124">Роли сервера входа для экземпляра SQL Server:</span><span class="sxs-lookup"><span data-stu-id="039d6-124">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="039d6-125">dbcreator</span><span class="sxs-lookup"><span data-stu-id="039d6-125">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="039d6-126">processadmin</span><span class="sxs-lookup"><span data-stu-id="039d6-126">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="039d6-127">Права экземпляра служб SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="039d6-127">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="039d6-128">Создание папок</span><span class="sxs-lookup"><span data-stu-id="039d6-128">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="039d6-129">Публикация отчетов</span><span class="sxs-lookup"><span data-stu-id="039d6-129">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-130">Необязательный-Установка компонента прозрачного шифрования данных (TDE), доступного в SQL Server</span><span class="sxs-lookup"><span data-stu-id="039d6-130">Optional - Install the Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-131">Функция TDE SQL Server осуществляет шифрование и расшифровку данных и файлов журнала в режиме реального времени, что поможет вам соблюдать законы, правила и положения, применимые к различным отраслям.</span><span class="sxs-lookup"><span data-stu-id="039d6-131">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="039d6-132">Примечание.</span><span class="sxs-lookup"><span data-stu-id="039d6-132">Note</span></span></strong><br/><p><span data-ttu-id="039d6-133">TDE выполняет расшифровку сведений о базе данных в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="039d6-133">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="039d6-134">Это означает, что если вы просматриваете данные ключа восстановления в базе данных SQL Server и вошли в систему под учетной записью, обладающей разрешениями для базы данных, отображается информация ключа для восстановления.</span><span class="sxs-lookup"><span data-stu-id="039d6-134">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="039d6-135">Подробнее об TDEах можно узнать в статье <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> рекомендации по безопасности в MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="039d6-135">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="039d6-136">Службы ядра СУБД SQL Server</span><span class="sxs-lookup"><span data-stu-id="039d6-136">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-137">Службы SQL Server Database Engine должны быть установлены и запущены во время установки сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="039d6-137">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-138">Windows PowerShell 3,0 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="039d6-138">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-139">Windows PowerShell не нужно устанавливать на сервере базы данных восстановления, если вы используете Windows PowerShell для настройки базы данных с удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="039d6-139">Windows PowerShell does not have to be installed on the Recovery Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="039d6-140">Предварительные условия для базы данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="039d6-140">Prerequisites for the Compliance and Audit Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="039d6-141">Предварительные</span><span class="sxs-lookup"><span data-stu-id="039d6-141">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="039d6-142">Сведения</span><span class="sxs-lookup"><span data-stu-id="039d6-142">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-143">Поддерживаемая версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="039d6-143">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-144">Установка SQL Server с SQL_Latin1_General_CP1_CI_AS параметрами сортировки.</span><span class="sxs-lookup"><span data-stu-id="039d6-144">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="039d6-145">Поддерживаемые <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="039d6-145">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="039d6-146">Требуемые разрешения SQL Server</span><span class="sxs-lookup"><span data-stu-id="039d6-146">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-147">Необходимые разрешения:</span><span class="sxs-lookup"><span data-stu-id="039d6-147">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="039d6-148">Роли сервера входа для экземпляра SQL Server:</span><span class="sxs-lookup"><span data-stu-id="039d6-148">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="039d6-149">dbcreator</span><span class="sxs-lookup"><span data-stu-id="039d6-149">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="039d6-150">processadmin</span><span class="sxs-lookup"><span data-stu-id="039d6-150">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="039d6-151">Права экземпляра служб SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="039d6-151">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="039d6-152">Создание папок</span><span class="sxs-lookup"><span data-stu-id="039d6-152">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="039d6-153">Публикация отчетов</span><span class="sxs-lookup"><span data-stu-id="039d6-153">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-154">Необязательный-Установка функции шифрования прозрачных данных (TDE) в SQL Server</span><span class="sxs-lookup"><span data-stu-id="039d6-154">Optional - Install the Transparent Data Encryption (TDE) feature in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-155">Функция TDE SQL Server осуществляет шифрование и расшифровку данных и файлов журнала в режиме реального времени, что поможет вам соблюдать законы, правила и положения, применимые к различным отраслям.</span><span class="sxs-lookup"><span data-stu-id="039d6-155">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<p><span data-ttu-id="039d6-156">TDE выполняет расшифровку сведений о базе данных в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="039d6-156">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="039d6-157">Это означает, что если вы просматриваете данные ключа восстановления в базе данных SQL Server и вошли в систему под учетной записью, обладающей разрешениями для базы данных, отображается информация ключа для восстановления.</span><span class="sxs-lookup"><span data-stu-id="039d6-157">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="039d6-158">Подробнее об TDEах можно узнать в статье <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> рекомендации по безопасности в MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="039d6-158">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="039d6-159">Службы ядра СУБД SQL Server</span><span class="sxs-lookup"><span data-stu-id="039d6-159">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-160">Службы SQL Server Database Engine должны быть установлены и запущены во время установки сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="039d6-160">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span> <span data-ttu-id="039d6-161">Однако SQL Server можно запускать удаленно. Он не должен находиться на том же сервере, на котором выполняется установка программного обеспечения сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="039d6-161">However, SQL Server can be running remotely; it doesn’t have to be on the same server on which you are installing the MBAM Server software.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-162">Windows PowerShell 3,0 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="039d6-162">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-163">Если вы используете Windows PowerShell для настройки базы данных с удаленного компьютера, не нужно устанавливать Windows PowerShell на сервер базы данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="039d6-163">Windows PowerShell does not have to be installed on the Compliance and Audit Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="039d6-164">Предварительные требования для отчетов</span><span class="sxs-lookup"><span data-stu-id="039d6-164">Prerequisites for the Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="039d6-165">Предварительные</span><span class="sxs-lookup"><span data-stu-id="039d6-165">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="039d6-166">Сведения</span><span class="sxs-lookup"><span data-stu-id="039d6-166">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-167">Поддерживаемая версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="039d6-167">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-168">Установка SQL Server с SQL_Latin1_General_CP1_CI_AS параметрами сортировки.</span><span class="sxs-lookup"><span data-stu-id="039d6-168">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="039d6-169">Поддерживаемые <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="039d6-169">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="039d6-170">Службы SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="039d6-170">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-171">Службы SSRS должны быть установлены и запущены во время установки сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="039d6-171">SSRS must be installed and running during the MBAM Server installation.</span></span></p>
<p><span data-ttu-id="039d6-172">Настройка SSRS в &quot; основном &quot; режиме, а не в режиме "в конфигурации" или в &quot; SharePoint &quot; .</span><span class="sxs-lookup"><span data-stu-id="039d6-172">Configure SSRS in &quot;native&quot; mode and not in unconfigured or &quot;SharePoint&quot; mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-173">Права экземпляра служб SSRS — необходимы для настройки отчетов только в том случае, если вы устанавливаете базы данных на отдельном сервере с сервера, на котором настроены отчеты.</span><span class="sxs-lookup"><span data-stu-id="039d6-173">SSRS instance rights – required for configuring Reports only if you are installing databases on a separate server from the server where Reports are configured.</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-174">Необходимые права для экземпляра:</span><span class="sxs-lookup"><span data-stu-id="039d6-174">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="039d6-175">Создание папок</span><span class="sxs-lookup"><span data-stu-id="039d6-175">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="039d6-176">Публикация отчетов</span><span class="sxs-lookup"><span data-stu-id="039d6-176">Publish Reports</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="039d6-177">Windows PowerShell 3,0 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="039d6-177">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-178">Если вы используете Windows PowerShell для настройки базы данных с удаленного компьютера, вам не нужно устанавливать Windows PowerShell на этом сервере базы данных.</span><span class="sxs-lookup"><span data-stu-id="039d6-178">Windows PowerShell does not have to be installed on this Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a><span data-ttu-id="039d6-179">Предварительные требования для сервера администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="039d6-179">Prerequisites for the Administration and Monitoring Server</span></span>


<span data-ttu-id="039d6-180">В следующей таблице перечислены требования к установке сервера администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="039d6-180">The following table lists the installation prerequisites for the MBAM Administration and Monitoring Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="039d6-181">Предварительные</span><span class="sxs-lookup"><span data-stu-id="039d6-181">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="039d6-182">Сведения</span><span class="sxs-lookup"><span data-stu-id="039d6-182">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-183">Роль веб-сервера Windows Server</span><span class="sxs-lookup"><span data-stu-id="039d6-183">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-184">Эту роль необходимо добавить в серверную операционную систему, которая поддерживается для компонента администрирования и мониторинга сервера.</span><span class="sxs-lookup"><span data-stu-id="039d6-184">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="039d6-185">Средства управления веб-сервером (IIS)</span><span class="sxs-lookup"><span data-stu-id="039d6-185">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-186">Выберите пункт <strong> сценарии и инструменты управления IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="039d6-186">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="039d6-187">SSL-сертификат</span><span class="sxs-lookup"><span data-stu-id="039d6-187">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="039d6-188">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="039d6-188">Optional.</span></span> <span data-ttu-id="039d6-189">Для безопасной связи между клиентскими компьютерами и веб-службами необходимо получить и установить сертификат, подписанный надежным центром безопасности.</span><span class="sxs-lookup"><span data-stu-id="039d6-189">To secure communication between the client computers and the web services, you must obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="039d6-190">Службы ролей веб-сервера</span><span class="sxs-lookup"><span data-stu-id="039d6-190">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="039d6-191">Основные возможности HTTP:</span><span class="sxs-lookup"><span data-stu-id="039d6-191">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="039d6-192">Статическое содержимое</span><span class="sxs-lookup"><span data-stu-id="039d6-192">Static Content</span></span></p></li>
<li><p><span data-ttu-id="039d6-193">Документ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="039d6-193">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="039d6-194">Разработка приложений.</span><span class="sxs-lookup"><span data-stu-id="039d6-194">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="039d6-195">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="039d6-195">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="039d6-196">Расширяемость .NET</span><span class="sxs-lookup"><span data-stu-id="039d6-196">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="039d6-197">Расширения ISAPI</span><span class="sxs-lookup"><span data-stu-id="039d6-197">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="039d6-198">Фильтры ISAPI</span><span class="sxs-lookup"><span data-stu-id="039d6-198">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="039d6-199">Разрешения</span><span class="sxs-lookup"><span data-stu-id="039d6-199">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="039d6-200">Проверка подлинности Windows</span><span class="sxs-lookup"><span data-stu-id="039d6-200">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="039d6-201">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="039d6-201">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-202">Возможности Windows Server</span><span class="sxs-lookup"><span data-stu-id="039d6-202">Windows Server Features</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="039d6-203">Возможности .NET Framework 4,5:</span><span class="sxs-lookup"><span data-stu-id="039d6-203">.NET Framework 4.5 features:</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="039d6-204">Платформа .NET Framework 4,5 или 4,6</span><span class="sxs-lookup"><span data-stu-id="039d6-204">.NET Framework 4.5 or 4.6</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="039d6-205">Платформа Windows Server 2016 </strong> - .net Framework 4,6 уже установлена для этих версий Windows Server, но ее необходимо включить.</span><span class="sxs-lookup"><span data-stu-id="039d6-205">Windows Server 2016</strong> - .NET Framework 4.6 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>  
<li><p><strong><span data-ttu-id="039d6-206">Windows Server 2012 или Windows Server 2012 R2 </strong> - .net Framework 4,5 уже установлены для этих версий Windows Server, но необходимо включить ее.</span><span class="sxs-lookup"><span data-stu-id="039d6-206">Windows Server 2012 or Windows Server 2012 R2</strong> - .NET Framework 4.5 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>
<li><p><strong><span data-ttu-id="039d6-207">Windows Server 2008 R2 </strong> - .net Framework 4,5 не входит в состав windows Server 2008 R2, поэтому необходимо <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> загрузить Microsoft .NET Framework 4,5 </a> и установить его отдельно.</span><span class="sxs-lookup"><span data-stu-id="039d6-207">Windows Server 2008 R2</strong> - .NET Framework 4.5 is not included with Windows Server 2008 R2, so you must <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)">download Microsoft .NET Framework 4.5</a> and install it separately.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="039d6-208">Примечание.</span><span class="sxs-lookup"><span data-stu-id="039d6-208">Note</span></span></strong><br/><p><span data-ttu-id="039d6-209">Если вы выполняете обновление с MBAM 2,0 или MBAM 2,0 SP1 и вам нужно установить .NET Framework 4,5, ознакомьтесь с <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> заметками о выпуске для MBAM 2,5 </a> для получения дополнительных необходимых шагов по выполнению веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="039d6-209">If you are upgrading from MBAM 2.0 or MBAM 2.0 SP1 and need to install .NET Framework 4.5, see <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)">Release Notes for MBAM 2.5</a> for an additional required step to make the websites work.</span></span></p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong><span data-ttu-id="039d6-210">Активация WCF</span><span class="sxs-lookup"><span data-stu-id="039d6-210">WCF Activation</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="039d6-211">Активация по HTTP</span><span class="sxs-lookup"><span data-stu-id="039d6-211">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="039d6-212">Активация не по протоколу HTTP (только для Windows Server 2008, 2012 и 2012 R2)</span><span class="sxs-lookup"><span data-stu-id="039d6-212">Non-HTTP Activation (Only for Windows Server 2008, 2012, and 2012 R2)</span></span></p>
<p></p></li>
</ul></li>
<li><p><strong><span data-ttu-id="039d6-213">Активация по протоколу TCP</span><span class="sxs-lookup"><span data-stu-id="039d6-213">TCP Activation</span></span></strong></p></li>
</ul>
<p><strong><span data-ttu-id="039d6-214">Служба активации процессов Windows.</span><span class="sxs-lookup"><span data-stu-id="039d6-214">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="039d6-215">Модель процесса</span><span class="sxs-lookup"><span data-stu-id="039d6-215">Process Model</span></span></p></li>
<li><p><span data-ttu-id="039d6-216">Среда .NET Framework</span><span class="sxs-lookup"><span data-stu-id="039d6-216">.NET Framework Environment</span></span></p></li>
<li><p><span data-ttu-id="039d6-217">API конфигурации</span><span class="sxs-lookup"><span data-stu-id="039d6-217">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="039d6-218">ASP.NET MVC 4,0</span><span class="sxs-lookup"><span data-stu-id="039d6-218">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="039d6-219">Загрузка ASP.NET MVC 4</span><span class="sxs-lookup"><span data-stu-id="039d6-219">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-220">Имя субъекта-службы (SPN)</span><span class="sxs-lookup"><span data-stu-id="039d6-220">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-221">Для веб-приложений требуется имя SPN для имени виртуального узла под учетной записью домена, которую вы используете для пулов веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="039d6-221">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="039d6-222">Если ваши административные права разрешают вам создавать SPN в доменных службах Active Directory, MBAM создает имя участника-службы.</span><span class="sxs-lookup"><span data-stu-id="039d6-222">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="039d6-223"><a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> </a> Сведения о правах, необходимых для создания SPN, можно найти в SetSPN.</span><span class="sxs-lookup"><span data-stu-id="039d6-223">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="039d6-224">Если у вас нет прав администратора для создания SPN, вы должны обратиться к администраторам Active Directory в вашей организации, чтобы создать для вас SPN, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="039d6-224">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="039d6-225">В примере кода имя виртуального узла — mbamvirtual.contoso.com, а учетная запись домена, используемая для пулов веб-приложений, — contoso\mbamapppooluser.</span><span class="sxs-lookup"><span data-stu-id="039d6-225">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="039d6-226">Примечание.</span><span class="sxs-lookup"><span data-stu-id="039d6-226">Note</span></span></strong><br/><p><span data-ttu-id="039d6-227">При настройке балансировки нагрузки используйте одну и ту же учетную запись пула приложений на всех серверах.</span><span class="sxs-lookup"><span data-stu-id="039d6-227">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="039d6-228">Дополнительные сведения о регистрации SPN для полных, NetBIOS-и настраиваемых имен узлов вы можете найти <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> в разделе Планирование защиты сайтов MBAM </a> .</span><span class="sxs-lookup"><span data-stu-id="039d6-228">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="039d6-229">Предварительные требования для портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="039d6-229">Prerequisites for the Self-Service Portal</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="039d6-230">Предварительные</span><span class="sxs-lookup"><span data-stu-id="039d6-230">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="039d6-231">Сведения</span><span class="sxs-lookup"><span data-stu-id="039d6-231">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-232">Поддерживаемая версия Windows Server</span><span class="sxs-lookup"><span data-stu-id="039d6-232">Supported version of Windows Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-233">Поддерживаемые <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="039d6-233">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="039d6-234">ASP.NET MVC 4,0</span><span class="sxs-lookup"><span data-stu-id="039d6-234">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="039d6-235">Загрузка ASP.NET MVC 4</span><span class="sxs-lookup"><span data-stu-id="039d6-235">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-236">Средства управления IIS для веб-служб</span><span class="sxs-lookup"><span data-stu-id="039d6-236">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="039d6-237">Имя субъекта-службы (SPN)</span><span class="sxs-lookup"><span data-stu-id="039d6-237">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-238">Для веб-приложений требуется имя SPN для имени виртуального узла под учетной записью домена, которую вы используете для пулов веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="039d6-238">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="039d6-239">Если ваши административные права разрешают вам создавать SPN в доменных службах Active Directory, MBAM создает имя участника-службы.</span><span class="sxs-lookup"><span data-stu-id="039d6-239">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="039d6-240"><a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> </a> Сведения о правах, необходимых для создания SPN, можно найти в SetSPN.</span><span class="sxs-lookup"><span data-stu-id="039d6-240">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="039d6-241">Если у вас нет прав администратора для создания имен участников-служб, вы должны обратиться к администраторам Active Directory в своей организации, чтобы создать для вас SPN, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="039d6-241">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="039d6-242">В примере кода имя виртуального узла — mbamvirtual.contoso.com, а учетная запись домена, используемая для пулов веб-приложений, — contoso\mbamapppooluser.</span><span class="sxs-lookup"><span data-stu-id="039d6-242">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="039d6-243">Примечание.</span><span class="sxs-lookup"><span data-stu-id="039d6-243">Note</span></span></strong><br/><p><span data-ttu-id="039d6-244">При настройке балансировки нагрузки используйте одну и ту же учетную запись пула приложений на всех серверах.</span><span class="sxs-lookup"><span data-stu-id="039d6-244">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="039d6-245">Дополнительные сведения о регистрации SPN для полных, NetBIOS-и настраиваемых имен узлов вы можете найти <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> в разделе Планирование защиты сайтов MBAM </a> .</span><span class="sxs-lookup"><span data-stu-id="039d6-245">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="039d6-246">Предварительные требования для рабочей станции управления</span><span class="sxs-lookup"><span data-stu-id="039d6-246">Prerequisites for the Management Workstation</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="039d6-247">Предварительные</span><span class="sxs-lookup"><span data-stu-id="039d6-247">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="039d6-248">Сведения</span><span class="sxs-lookup"><span data-stu-id="039d6-248">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-249">Перед установкой клиента MBAM Скачайте шаблоны групповой политики MBAM, <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> чтобы получить шаблоны групповой политики для MDOP, </a> и настройте их с помощью параметров, которые вы хотите реализовать на вашем предприятии для шифрования диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="039d6-249">Before installing the MBAM Client, download the MBAM Group Policy Templates from <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)">How to Get MDOP Group Policy (.admx) Templates</a> and configure them with the settings that you want to implement in your enterprise for BitLocker Drive Encryption.</span></span></p></td>
<td align="left"><p><span data-ttu-id="039d6-250">Прежде чем устанавливать клиент MBAM, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="039d6-250">Before installing the MBAM Client, do the following:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="039d6-251">Что делать</span><span class="sxs-lookup"><span data-stu-id="039d6-251">What to do</span></span></th>
<th align="left"><span data-ttu-id="039d6-252">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="039d6-252">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="039d6-253">Копирование шаблонов групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="039d6-253">Copy the MBAM Group Policy Templates</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="039d6-254">Копирование шаблонов групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="039d6-254">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="039d6-255">Изменение параметров групповой политики</span><span class="sxs-lookup"><span data-stu-id="039d6-255">Edit the Group Policy settings</span></span></p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"><span data-ttu-id="039d6-256">Изменение параметров групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="039d6-256">Editing the MBAM 2.5 Group Policy Settings</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## <span data-ttu-id="039d6-257">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="039d6-257">Related topics</span></span>


[<span data-ttu-id="039d6-258">Подготовка среды для развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="039d6-258">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="039d6-259">Планирование развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="039d6-259">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="039d6-260">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="039d6-260">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)




## <span data-ttu-id="039d6-261">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="039d6-261">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="039d6-262">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="039d6-262">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="039d6-263">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="039d6-263">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




