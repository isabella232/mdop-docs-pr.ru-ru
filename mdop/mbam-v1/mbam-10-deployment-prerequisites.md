---
title: Необходимые компоненты развертывания MBAM 1.0
description: Необходимые компоненты развертывания MBAM 1.0
author: dansimp
ms.assetid: bd9e1010-7d25-43e7-8dc6-b521226a659d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ed14343d37a859364bcabbe6ca72c041502a23c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822662"
---
# <span data-ttu-id="0dbb2-103">Необходимые компоненты развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0dbb2-103">MBAM 1.0 Deployment Prerequisites</span></span>


<span data-ttu-id="0dbb2-104">Прежде чем приступить к установке Microsoft BitLocker Administration и Monitoring (MBAM), убедитесь в том, что вы отвечаете необходимым предварительным требованиям для установки продукта.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-104">Before you begin the Microsoft BitLocker Administration and Monitoring (MBAM) Setup, make sure that you meet the necessary prerequisites to install the product.</span></span> <span data-ttu-id="0dbb2-105">В этом разделе содержится информация, которая поможет вам успешно подготовить рабочую среду перед развертыванием клиентов MBAM и функций сервера.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-105">This section contains information to help you successfully prepare your computing environment before you deploy the MBAM Clients and Server features.</span></span>

## <span data-ttu-id="0dbb2-106">Требования для установки функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="0dbb2-106">Installation prerequisites for MBAM Server features</span></span>


<span data-ttu-id="0dbb2-107">Каждый из функций сервера MBAM имеет определенные предварительные требования, которые должны быть выполнены, прежде чем их можно будет успешно установить.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-107">Each of the MBAM server features has specific prerequisites that must be met before they can be successfully installed.</span></span> <span data-ttu-id="0dbb2-108">Программа установки MBAM проверяет, выполнены ли все необходимые условия перед началом установки.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-108">MBAM Setup verifies if all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="0dbb2-109">Необходимые условия для установки на сервере администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="0dbb2-109">Installation prerequisites for Administration and Monitoring Server</span></span>

<span data-ttu-id="0dbb2-110">В следующей таблице приведены требования к установке сервера администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-110">The following table contains the installation prerequisites for the MBAM Administration and Monitoring Server:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0dbb2-111">Предварительные</span><span class="sxs-lookup"><span data-stu-id="0dbb2-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="0dbb2-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="0dbb2-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0dbb2-113">Роль сервера Windows ServerWeb</span><span class="sxs-lookup"><span data-stu-id="0dbb2-113">Windows ServerWeb Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0dbb2-114">Эту роль необходимо добавить в серверную операционную систему, поддерживаемую компонентом сервера администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-114">This role must be added to a server operating system supported for the mbam Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0dbb2-115">Средства управления веб-сервером (IIS)</span><span class="sxs-lookup"><span data-stu-id="0dbb2-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="0dbb2-116">Сценарии и инструменты управления IIS</span><span class="sxs-lookup"><span data-stu-id="0dbb2-116">IIS Management Scripts and Tools</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0dbb2-117">Службы ролей веб-сервера</span><span class="sxs-lookup"><span data-stu-id="0dbb2-117">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="0dbb2-118">Основные возможности HTTP:</span><span class="sxs-lookup"><span data-stu-id="0dbb2-118">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="0dbb2-119">Статическое содержимое</span><span class="sxs-lookup"><span data-stu-id="0dbb2-119">Static Content</span></span></p></li>
<li><p><span data-ttu-id="0dbb2-120">Документ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0dbb2-120">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="0dbb2-121">Разработка приложений.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-121">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="0dbb2-122">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="0dbb2-122">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="0dbb2-123">Расширяемость .NET</span><span class="sxs-lookup"><span data-stu-id="0dbb2-123">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="0dbb2-124">Расширения ISAPI</span><span class="sxs-lookup"><span data-stu-id="0dbb2-124">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="0dbb2-125">Фильтры ISAPI</span><span class="sxs-lookup"><span data-stu-id="0dbb2-125">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="0dbb2-126">Разрешения</span><span class="sxs-lookup"><span data-stu-id="0dbb2-126">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="0dbb2-127">Проверка подлинности Windows</span><span class="sxs-lookup"><span data-stu-id="0dbb2-127">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="0dbb2-128">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="0dbb2-128">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0dbb2-129">Возможности Windows Server</span><span class="sxs-lookup"><span data-stu-id="0dbb2-129">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="0dbb2-130">Компоненты Microsoft .NET Framework 3.5.1:</span><span class="sxs-lookup"><span data-stu-id="0dbb2-130">Microsoft .NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="0dbb2-131">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="0dbb2-131">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="0dbb2-132">Активация WCF</span><span class="sxs-lookup"><span data-stu-id="0dbb2-132">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="0dbb2-133">Активация по HTTP</span><span class="sxs-lookup"><span data-stu-id="0dbb2-133">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="0dbb2-134">Активация не по протоколу HTTP</span><span class="sxs-lookup"><span data-stu-id="0dbb2-134">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="0dbb2-135">Служба активации процессов Windows</span><span class="sxs-lookup"><span data-stu-id="0dbb2-135">Windows Process Activation Service</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="0dbb2-136">Модель процесса</span><span class="sxs-lookup"><span data-stu-id="0dbb2-136">Process Model</span></span></p></li>
<li><p><span data-ttu-id="0dbb2-137">Среда .NET</span><span class="sxs-lookup"><span data-stu-id="0dbb2-137">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="0dbb2-138">API конфигурации</span><span class="sxs-lookup"><span data-stu-id="0dbb2-138">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0dbb2-139">**Примечание**  Список поддерживаемых операционных систем можно найти в разделе [Поддерживаемые конфигурации MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="0dbb2-139">**Note** For a list of supported operating systems, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="0dbb2-140">Требования для установки для отчетов о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="0dbb2-140">Installation prerequisites for the Compliance and Audit Reports</span></span>

<span data-ttu-id="0dbb2-141">Отчеты о соответствии и аудите должны устанавливаться в поддерживаемой версии SQLServer.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-141">The Compliance and Audit Reports must be installed on a supported version of SQLServer.</span></span> <span data-ttu-id="0dbb2-142">Предварительные требования к установке для этой функции включают службы SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="0dbb2-142">Installation prerequisites for this feature include SQL Server Reporting Services (SSRS).</span></span>

<span data-ttu-id="0dbb2-143">Службы SSRS должны быть установлены и запущены во время установки сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-143">SSRS must be installed and running during MBAM server installation.</span></span> <span data-ttu-id="0dbb2-144">Кроме того, службы SSRS следует настроить в режиме "машинный", а не в режиме "не настроено" или "SharePoint".</span><span class="sxs-lookup"><span data-stu-id="0dbb2-144">SSRS should also be configured in “native” mode, not in the “unconfigured” or “SharePoint” mode.</span></span>

<span data-ttu-id="0dbb2-145">**Примечание**  Список поддерживаемых операционных систем и версий SQLServer можно найти в разделе [Поддерживаемые конфигурации MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="0dbb2-145">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="0dbb2-146">Предварительные требования к установке для базы данных восстановления и оборудования</span><span class="sxs-lookup"><span data-stu-id="0dbb2-146">Installation prerequisites for the Recovery and Hardware Database</span></span>

<span data-ttu-id="0dbb2-147">База данных восстановления и оборудования должна быть установлена в поддерживаемой версии SQLServer.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-147">The Recovery and Hardware Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="0dbb2-148">При установке сервера MBAM на сервере SQL Server должны быть установлены и запущены службы ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-148">SQL Server must have Database Engine Services installed and running during the MBAM server installation.</span></span> <span data-ttu-id="0dbb2-149">Функция шифрования прозрачных данных (TDE) должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-149">The Transparent Data Encryption (TDE) feature must be enabled.</span></span>

<span data-ttu-id="0dbb2-150">**Примечание**  Список поддерживаемых операционных систем и версий SQLServer можно найти в разделе [Поддерживаемые конфигурации MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="0dbb2-150">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

<span data-ttu-id="0dbb2-151">Функция SQLServer TDE выполняет шифрование и расшифровку данных и файлов журнала в режиме реального времени (I/O).</span><span class="sxs-lookup"><span data-stu-id="0dbb2-151">The TDE SQLServer feature performs real-time input/output (I/O) encryption and decryption of the data and log files.</span></span> <span data-ttu-id="0dbb2-152">TDE защищает данные, которые находятся в разных частях, включая данные и файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-152">TDE protects data that is "at rest,” which include the data and the log files.</span></span> <span data-ttu-id="0dbb2-153">Она обеспечивает соответствие множеству законов, нормативных актов и руководств, которые устанавливаются в различных отраслях.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-153">It provides the ability to comply with many laws, regulations, and guidelines that are established in various industries.</span></span>

<span data-ttu-id="0dbb2-154">**Примечание**  Поскольку TDE выполняет расшифровку сведений о базе данных в режиме реального времени, сведения о ключе восстановления будут видны, если учетная запись, в которой вы вошли в систему, имеет разрешения на доступ к базе данных при просмотре таблиц SQL для данных ключа восстановления.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-154">**Note** Because TDE performs real-time decryption of database information, the recovery key information will be visible if the account under which you are logged in has permissions to the database when you view the recovery key information SQL tables.</span></span>

 

### <span data-ttu-id="0dbb2-155">Требования для установки базы данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="0dbb2-155">Installation prerequisites for the Compliance and Audit Database</span></span>

<span data-ttu-id="0dbb2-156">База данных соответствия требованиям и аудита должна быть установлена в поддерживаемой версии SQLServer.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-156">The Compliance and Audit Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="0dbb2-157">При установке сервера MBAM на сервере SQL Server должны быть установлены и запущены службы ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-157">SQL Server must have Database Engine Services installed and running during MBAM server installation.</span></span>

<span data-ttu-id="0dbb2-158">**Примечание**  Список поддерживаемых операционных систем и версий SQLServer можно найти в разделе [Поддерживаемые конфигурации MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="0dbb2-158">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="0dbb2-159">Требования для установки для клиентов MBAM</span><span class="sxs-lookup"><span data-stu-id="0dbb2-159">Installation prerequisites for MBAM Clients</span></span>


<span data-ttu-id="0dbb2-160">Прежде чем приступить к установке клиента MBAM, необходимо выполнить следующие требования:</span><span class="sxs-lookup"><span data-stu-id="0dbb2-160">The necessary prerequisites that you must meet before you begin the MBAM Client installation are the following:</span></span>

-   <span data-ttu-id="0dbb2-161">Возможность доверенного платформенного модуля (TPM) версии 1.2</span><span class="sxs-lookup"><span data-stu-id="0dbb2-161">Trusted Platform Module (TPM) v1.2 capability</span></span>

-   <span data-ttu-id="0dbb2-162">Микросхема TPM должна быть включена в BIOS и должна быть переустановлена из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-162">The TPM chip must be turned on in the BIOS and it must be resettable from the operating system.</span></span> <span data-ttu-id="0dbb2-163">Дополнительные сведения можно найти в документации по BIOS.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-163">For more information, see the BIOS documentation.</span></span>

<span data-ttu-id="0dbb2-164">**Предупреждение**  Убедитесь, что клавиатура, мышь и видео прямо подключены к компьютеру, а не коммутатор клавиатуры, видео, мыши (KVM).</span><span class="sxs-lookup"><span data-stu-id="0dbb2-164">**Warning** Ensure that the keyboard, mouse, and video are directly connected to the computer, instead of to a keyboard, video, mouse (KVM) switch.</span></span> <span data-ttu-id="0dbb2-165">КВМ-коммутатор может взаимодействовать с возможностями компьютера, чтобы обнаружить физическое присутствие оборудования.</span><span class="sxs-lookup"><span data-stu-id="0dbb2-165">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span>

 

## <span data-ttu-id="0dbb2-166">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0dbb2-166">Related topics</span></span>


[<span data-ttu-id="0dbb2-167">Планирование развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0dbb2-167">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="0dbb2-168">Поддерживаемые конфигурации MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0dbb2-168">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)

 

 





