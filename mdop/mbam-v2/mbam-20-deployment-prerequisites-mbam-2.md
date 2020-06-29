---
title: Необходимые условия для развертывания MBAM 2.0
description: Необходимые условия для развертывания MBAM 2.0
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826012"
---
# <span data-ttu-id="5f276-103">Необходимые условия для развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5f276-103">MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="5f276-104">Перед запуском настройки администрирования и мониторинга Microsoft BitLocker (MBAM) необходимо убедиться в соблюдении необходимых условий для установки продукта.</span><span class="sxs-lookup"><span data-stu-id="5f276-104">Before you start Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should ensure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="5f276-105">В этом разделе содержится информация, которая поможет вам успешно спланировать вычислительную среду перед развертыванием администрирования Microsoft BitLocker и наблюдения за функциями и клиентами сервера.</span><span class="sxs-lookup"><span data-stu-id="5f276-105">This section contains information to help you successfully plan your computing environment before you deploy Microsoft BitLocker Administration and Monitoring Server features and Clients.</span></span> <span data-ttu-id="5f276-106">Если вы устанавливаете MBAM с помощью Configuration Manager, ознакомьтесь со сведениями о том, [как развернуть MBAM с помощью Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) для дополнительных необходимых компонентов.</span><span class="sxs-lookup"><span data-stu-id="5f276-106">If you are installing MBAM with Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional prerequisites.</span></span>

## <span data-ttu-id="5f276-107">Требования для установки функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="5f276-107">Installation Prerequisites for MBAM Server Features</span></span>


<span data-ttu-id="5f276-108">Каждый из функций сервера MBAM имеет определенные предварительные требования, которые должны быть выполнены, прежде чем можно будет успешно установить компоненты MBAM.</span><span class="sxs-lookup"><span data-stu-id="5f276-108">Each of the MBAM Server features has specific prerequisites that must be met before the MBAM features can be successfully installed.</span></span> <span data-ttu-id="5f276-109">Программа установки MBAM проверяет, выполнены ли все необходимые условия перед началом установки.</span><span class="sxs-lookup"><span data-stu-id="5f276-109">MBAM Setup checks that all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="5f276-110">Предварительные требования для сервера администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="5f276-110">Prerequisites for Administration and Monitoring Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f276-111">Предварительные</span><span class="sxs-lookup"><span data-stu-id="5f276-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5f276-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="5f276-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f276-113">Роль веб-сервера Windows Server</span><span class="sxs-lookup"><span data-stu-id="5f276-113">Windows Server Web Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5f276-114">Эту роль необходимо добавить в серверную операционную систему, которая поддерживается для компонента администрирования и мониторинга сервера.</span><span class="sxs-lookup"><span data-stu-id="5f276-114">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5f276-115">Средства управления веб-сервером (IIS)</span><span class="sxs-lookup"><span data-stu-id="5f276-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5f276-116">Выберите <strong> сценарии управления IIS и инструменты </strong> .</span><span class="sxs-lookup"><span data-stu-id="5f276-116">Select <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f276-117">SSL-сертификат</span><span class="sxs-lookup"><span data-stu-id="5f276-117">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5f276-118">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="5f276-118">Optional.</span></span> <span data-ttu-id="5f276-119">Для безопасной связи между клиентами и веб-службами необходимо получить и установить сертификат, подписанный надежным центром безопасности.</span><span class="sxs-lookup"><span data-stu-id="5f276-119">To secure communication between the clients and the web services, you have to obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5f276-120">Службы ролей веб-сервера</span><span class="sxs-lookup"><span data-stu-id="5f276-120">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="5f276-121">Основные возможности HTTP:</span><span class="sxs-lookup"><span data-stu-id="5f276-121">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="5f276-122">Статическое содержимое</span><span class="sxs-lookup"><span data-stu-id="5f276-122">Static Content</span></span></p></li>
<li><p><span data-ttu-id="5f276-123">Документ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5f276-123">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="5f276-124">Разработка приложений.</span><span class="sxs-lookup"><span data-stu-id="5f276-124">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="5f276-125">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="5f276-125">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="5f276-126">Расширяемость .NET</span><span class="sxs-lookup"><span data-stu-id="5f276-126">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="5f276-127">Расширения ISAPI</span><span class="sxs-lookup"><span data-stu-id="5f276-127">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="5f276-128">Фильтры ISAPI</span><span class="sxs-lookup"><span data-stu-id="5f276-128">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="5f276-129">Разрешения</span><span class="sxs-lookup"><span data-stu-id="5f276-129">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="5f276-130">Проверка подлинности Windows</span><span class="sxs-lookup"><span data-stu-id="5f276-130">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="5f276-131">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="5f276-131">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f276-132">Возможности Windows Server</span><span class="sxs-lookup"><span data-stu-id="5f276-132">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="5f276-133">Компоненты .NET Framework 3.5.1:</span><span class="sxs-lookup"><span data-stu-id="5f276-133">.NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="5f276-134">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="5f276-134">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="5f276-135">Активация WCF</span><span class="sxs-lookup"><span data-stu-id="5f276-135">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="5f276-136">Активация по HTTP</span><span class="sxs-lookup"><span data-stu-id="5f276-136">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="5f276-137">Активация не по протоколу HTTP</span><span class="sxs-lookup"><span data-stu-id="5f276-137">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="5f276-138">Служба активации процессов Windows.</span><span class="sxs-lookup"><span data-stu-id="5f276-138">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="5f276-139">Модель процесса</span><span class="sxs-lookup"><span data-stu-id="5f276-139">Process Model</span></span></p></li>
<li><p><span data-ttu-id="5f276-140">Среда .NET</span><span class="sxs-lookup"><span data-stu-id="5f276-140">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="5f276-141">API конфигурации</span><span class="sxs-lookup"><span data-stu-id="5f276-141">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="5f276-142">Примечание.</span><span class="sxs-lookup"><span data-stu-id="5f276-142">Note</span></span>**  
<span data-ttu-id="5f276-143">Список поддерживаемых операционных систем можно найти в разделе [Поддерживаемые конфигурации MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="5f276-143">For a list of supported operating systems, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



### <span data-ttu-id="5f276-144">Предварительные требования для отчетов о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="5f276-144">Prerequisites for the Compliance and Audit Reports</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f276-145">Предварительные</span><span class="sxs-lookup"><span data-stu-id="5f276-145">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5f276-146">Сведения</span><span class="sxs-lookup"><span data-stu-id="5f276-146">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f276-147">Поддерживаемая версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="5f276-147">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="5f276-148">Поддерживаемые <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="5f276-148">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f276-149">Установка SQL Server с помощью:</span><span class="sxs-lookup"><span data-stu-id="5f276-149">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="5f276-150">SQL_Latin1_General_CP1_CI_AS параметры сортировки</span><span class="sxs-lookup"><span data-stu-id="5f276-150">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f276-151">Службы SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="5f276-151">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f276-152">Права экземпляра SSRS — необходимы для установки отчетов, только если вы устанавливаете базы данных на отдельном сервере из отчетов.</span><span class="sxs-lookup"><span data-stu-id="5f276-152">SSRS instance rights – required for installing reports only if you are installing databases on a separate server from the reports.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f276-153">Необходимые права для экземпляра:</span><span class="sxs-lookup"><span data-stu-id="5f276-153">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="5f276-154">Создание папок</span><span class="sxs-lookup"><span data-stu-id="5f276-154">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="5f276-155">Публикация отчетов</span><span class="sxs-lookup"><span data-stu-id="5f276-155">Publish Reports</span></span></p></li>
</ul>
<p><span data-ttu-id="5f276-156">Службы SSRS должны быть установлены и запущены во время установки сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="5f276-156">SSRS must be installed and running during the MBAM Server installation.</span></span> <span data-ttu-id="5f276-157">Настройка SSRS в режиме "машинный", а не в ненастроенном режиме или "SharePoint".</span><span class="sxs-lookup"><span data-stu-id="5f276-157">Configure SSRS in “native” mode and not in unconfigured or “SharePoint” mode.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="5f276-158">Предварительные условия для базы данных восстановления</span><span class="sxs-lookup"><span data-stu-id="5f276-158">Prerequisites for the Recovery Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f276-159">Предварительные</span><span class="sxs-lookup"><span data-stu-id="5f276-159">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5f276-160">Сведения</span><span class="sxs-lookup"><span data-stu-id="5f276-160">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f276-161">Поддерживаемая версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="5f276-161">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="5f276-162">Поддерживаемые <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="5f276-162">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f276-163">Установка SQL Server с помощью:</span><span class="sxs-lookup"><span data-stu-id="5f276-163">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="5f276-164">SQL_Latin1_General_CP1_CI_AS параметры сортировки</span><span class="sxs-lookup"><span data-stu-id="5f276-164">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="5f276-165">Средства управления SQL Server</span><span class="sxs-lookup"><span data-stu-id="5f276-165">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f276-166">Требуемые разрешения SQL Server</span><span class="sxs-lookup"><span data-stu-id="5f276-166">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f276-167">Необходимые разрешения:</span><span class="sxs-lookup"><span data-stu-id="5f276-167">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="5f276-168">Роли сервера входа для экземпляра SQL:</span><span class="sxs-lookup"><span data-stu-id="5f276-168">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="5f276-169">dbcreator</span><span class="sxs-lookup"><span data-stu-id="5f276-169">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="5f276-170">processadmin</span><span class="sxs-lookup"><span data-stu-id="5f276-170">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="5f276-171">Права экземпляра служб SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="5f276-171">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="5f276-172">Создание папок</span><span class="sxs-lookup"><span data-stu-id="5f276-172">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="5f276-173">Публикация отчетов</span><span class="sxs-lookup"><span data-stu-id="5f276-173">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f276-174">Необязательный параметр-Установка прозрачного шифрования данных (TDE), доступные в SQL Server</span><span class="sxs-lookup"><span data-stu-id="5f276-174">Optional - Install Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f276-175">Функция TDE SQL Server осуществляет шифрование и расшифровку данных и файлов журнала в режиме реального времени, что поможет вам соблюдать многочисленные законы, правила и правила, определенные в разных отраслях.</span><span class="sxs-lookup"><span data-stu-id="5f276-175">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5f276-176">Примечание.</span><span class="sxs-lookup"><span data-stu-id="5f276-176">Note</span></span></strong><br/><p><span data-ttu-id="5f276-177">TDE выполняет расшифровку сведений о базе данных в режиме реального времени, что означает, что если учетная запись, под которой вы вошли в систему, имеет разрешения на доступ к базе данных, когда вы просматриваете данные ключа восстановления в таблицах SQL Server, отображаются сведения о ключе восстановления.</span><span class="sxs-lookup"><span data-stu-id="5f276-177">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="5f276-178">Дополнительные сведения о TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 в вопросах безопасности </a> .</span><span class="sxs-lookup"><span data-stu-id="5f276-178">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="5f276-179">Предварительные условия для базы данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="5f276-179">Prerequisites for the Compliance and Audit Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f276-180">Предварительные</span><span class="sxs-lookup"><span data-stu-id="5f276-180">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5f276-181">Сведения</span><span class="sxs-lookup"><span data-stu-id="5f276-181">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f276-182">Поддерживаемая версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="5f276-182">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="5f276-183">Поддерживаемые <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="5f276-183">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f276-184">Установка SQL Server с помощью:</span><span class="sxs-lookup"><span data-stu-id="5f276-184">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="5f276-185">SQL_Latin1_General_CP1_CI_AS параметры сортировки</span><span class="sxs-lookup"><span data-stu-id="5f276-185">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="5f276-186">Средства управления SQL Server</span><span class="sxs-lookup"><span data-stu-id="5f276-186">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f276-187">Требуемые разрешения SQL Server</span><span class="sxs-lookup"><span data-stu-id="5f276-187">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f276-188">Необходимые разрешения:</span><span class="sxs-lookup"><span data-stu-id="5f276-188">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="5f276-189">Роли сервера входа для экземпляра SQL:</span><span class="sxs-lookup"><span data-stu-id="5f276-189">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="5f276-190">dbcreator</span><span class="sxs-lookup"><span data-stu-id="5f276-190">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="5f276-191">processadmin</span><span class="sxs-lookup"><span data-stu-id="5f276-191">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="5f276-192">Права экземпляра служб SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="5f276-192">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="5f276-193">Создание папок</span><span class="sxs-lookup"><span data-stu-id="5f276-193">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="5f276-194">Публикация отчетов</span><span class="sxs-lookup"><span data-stu-id="5f276-194">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f276-195">Необязательный параметр-Установка прозрачного шифрования данных (TDE) в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5f276-195">Optional - Install Transparent Data Encryption (TDE) feature in SQL Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f276-196">Функция TDE SQL Server осуществляет шифрование и расшифровку данных и файлов журнала в режиме реального времени, что поможет вам соблюдать многочисленные законы, правила и правила, определенные в разных отраслях.</span><span class="sxs-lookup"><span data-stu-id="5f276-196">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5f276-197">Примечание.</span><span class="sxs-lookup"><span data-stu-id="5f276-197">Note</span></span></strong><br/><p><span data-ttu-id="5f276-198">TDE выполняет расшифровку сведений о базе данных в режиме реального времени, что означает, что если учетная запись, под которой вы вошли в систему, имеет разрешения на доступ к базе данных, когда вы просматриваете данные ключа восстановления в таблицах SQL Server, отображаются сведения о ключе восстановления.</span><span class="sxs-lookup"><span data-stu-id="5f276-198">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="5f276-199">Дополнительные сведения о TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 вопросы безопасности</span><span class="sxs-lookup"><span data-stu-id="5f276-199">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f276-200">При установке сервера MBAM на сервере SQL Server должны быть установлены и запущены службы ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="5f276-200">SQL Server must have Database Engine Services installed and running during MBAM Server installation.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f276-201">Служба агента SQL Server должна быть запущена и настроена на автоматическое начало для выбранных экземпляров SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5f276-201">The SQL Server Agent service must be running and set to auto-start on the selected instances of SQL Server.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="5f276-202">Предварительные требования для портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="5f276-202">Prerequisites for the Self-Service Portal</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f276-203">Предварительные</span><span class="sxs-lookup"><span data-stu-id="5f276-203">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5f276-204">Сведения</span><span class="sxs-lookup"><span data-stu-id="5f276-204">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f276-205">Поддерживаемая версия Windows Server</span><span class="sxs-lookup"><span data-stu-id="5f276-205">Supported version of Windows Server</span></span></p>
<p><span data-ttu-id="5f276-206">Поддерживаемые <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> конфигурации </a> для поддерживаемых версий MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="5f276-206">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f276-207">ASP.NET MVC 2,0</span><span class="sxs-lookup"><span data-stu-id="5f276-207">ASP.NET MVC 2.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)"><span data-ttu-id="5f276-208">Загрузка ASP.NET MVC 2</span><span class="sxs-lookup"><span data-stu-id="5f276-208">ASP.NET MVC 2 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f276-209">Средства управления IIS для веб-служб</span><span class="sxs-lookup"><span data-stu-id="5f276-209">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5f276-210">Предварительные требования для клиентов MBAM</span><span class="sxs-lookup"><span data-stu-id="5f276-210">Prerequisites for MBAM Clients</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f276-211">Предварительные</span><span class="sxs-lookup"><span data-stu-id="5f276-211">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5f276-212">Сведения</span><span class="sxs-lookup"><span data-stu-id="5f276-212">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f276-213">Для клиентов Windows 7 </strong> - требуется возможность доверенного платформенного модуля (TPM).</span><span class="sxs-lookup"><span data-stu-id="5f276-213">Windows 7 clients only</strong> - must have Trusted Platform Module (TPM) capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f276-214">Версия доверенного платформенного модуля должна быть 1,2 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="5f276-214">TPM version must be 1.2 or later.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f276-215">Микросхема TPM должна быть включена в BIOS и может быть переустановлена из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5f276-215">The TPM chip must be turned on in the BIOS and be resettable from the operating system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f276-216">Дополнительные сведения можно найти в документации по BIOS.</span><span class="sxs-lookup"><span data-stu-id="5f276-216">For more information, see the BIOS documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f276-217">Только для клиентов Windows 8 </strong> : MBAM хранение и управление ключами восстановления доверенного платформенного модуля: необходимо отключить автоматическое наполнение TPM, и перед развертыванием MBAM необходимо назначить MBAM в качестве владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="5f276-217">Windows 8 clients only</strong>: To have MBAM store and manage the TPM recovery keys: TPM auto-provisioning must be turned off, and MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span> <span data-ttu-id="5f276-218">Сведения о том, как отключить автоматическое предоставление TPM, можно найти в разделе <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</span><span class="sxs-lookup"><span data-stu-id="5f276-218">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<ul>
<li><p><span data-ttu-id="5f276-219">Автоматическое конфигурирование TPM должно быть отключено.</span><span class="sxs-lookup"><span data-stu-id="5f276-219">TPM auto-provisioning must be turned off.</span></span></p></li>
<li><p><span data-ttu-id="5f276-220">Перед развертыванием MBAM необходимо назначить MBAM в качестве владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="5f276-220">MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="5f276-221">Сведения о том, как отключить автоматическое предоставление TPM, можно найти в разделе <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</span><span class="sxs-lookup"><span data-stu-id="5f276-221">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5f276-222">Примечание.</span><span class="sxs-lookup"><span data-stu-id="5f276-222">Note</span></span></strong><br/><p><span data-ttu-id="5f276-223">Убедитесь, что клавиатура, видео или мышь подключены напрямую и не управляются с помощью клавиатуры, видео или мыши (KVM) Switch.</span><span class="sxs-lookup"><span data-stu-id="5f276-223">Ensure that the keyboard, video, or mouse are directly connected and not managed through a keyboard, video, or mouse (KVM) switch.</span></span> <span data-ttu-id="5f276-224">КВМ-коммутатор может взаимодействовать с возможностями компьютера, чтобы обнаружить физическое присутствие оборудования.</span><span class="sxs-lookup"><span data-stu-id="5f276-224">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5f276-225">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5f276-225">Related topics</span></span>


[<span data-ttu-id="5f276-226">Планирование развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5f276-226">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="5f276-227">Поддерживаемые конфигурации MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5f276-227">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)









