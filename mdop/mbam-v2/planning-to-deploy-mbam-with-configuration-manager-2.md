---
title: Планирование развертывания MBAM с помощью диспетчера конфигураций
description: Планирование развертывания MBAM с помощью диспетчера конфигураций
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825629"
---
# <span data-ttu-id="bd3b9-103">Планирование развертывания MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="bd3b9-103">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="bd3b9-104">Для развертывания MBAM с топологией Configuration Manager рекомендуются архитектура с тремя серверами, поддерживающая клиенты 200 000.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-104">To deploy MBAM with the Configuration Manager topology, a three-server architecture, which supports 200,000 clients, is recommended.</span></span> <span data-ttu-id="bd3b9-105">Используйте отдельный сервер для запуска Configuration Manager и устанавливайте основные возможности администрирования и наблюдения на двух серверах, как показано на рисунке архитектуры в разделе [Приступая к работе с помощью диспетчера конфигураций](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="bd3b9-105">Use a separate server to run Configuration Manager, and install the basic Administration and Monitoring features on two servers, as shown in the architecture image in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span>

**<span data-ttu-id="bd3b9-106">Важно.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-106">Important</span></span>**  
<span data-ttu-id="bd3b9-107">Windows To Go не поддерживается при установке интегрированной топологии MBAM с Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-107">Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>



## <span data-ttu-id="bd3b9-108">Предварительные требования к развертыванию для установки MBAM с помощью Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-108">Deployment Prerequisites for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="bd3b9-109">Перед установкой MBAM с помощью Configuration Manager убедитесь, что выполнены следующие предварительные требования:</span><span class="sxs-lookup"><span data-stu-id="bd3b9-109">Ensure that you have met the following prerequisites before you install MBAM with Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bd3b9-110">Предварительные</span><span class="sxs-lookup"><span data-stu-id="bd3b9-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="bd3b9-111">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="bd3b9-111">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd3b9-112">Убедитесь, что сервер Configuration Manager является основным сайтом в системе Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-112">Ensure that the Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-113">Н/Д</span><span class="sxs-lookup"><span data-stu-id="bd3b9-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bd3b9-114">Включите агент клиента инвентаризации оборудования на сервере Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-114">Enable the Hardware Inventory Client Agent on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-115">В Configuration Manager 2007 вы можете узнать, <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> как настроить инвентаризацию оборудования для сайта </a> .</span><span class="sxs-lookup"><span data-stu-id="bd3b9-115">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p>
<p><span data-ttu-id="bd3b9-116">Инструкции для System Center 2012 Configuration Manager можно найти <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> в разделе Настройка инвентаризации оборудования в Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="bd3b9-116">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd3b9-117">Включите агент управления требуемой конфигурацией (DCM) или параметры соответствия требованиям в зависимости от используемой версии Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-117">Enable the Desired Configuration Management (DCM) agent or the compliance settings, depending on the version of Configuration Manager that you are using.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-118">В Configuration Manager 2007 включите раздел Просмотр <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> свойств агента клиента управления требуемой конфигурацией </a> .</span><span class="sxs-lookup"><span data-stu-id="bd3b9-118">For Configuration Manager 2007, enable the see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p>
<p><span data-ttu-id="bd3b9-119">Сведения о System Center 2012 Configuration Manager можно найти <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> в разделе Настройка параметров соответствия в Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="bd3b9-119">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bd3b9-120">Определите точку служб Reporting Services в диспетчере конфигураций.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-120">Define a reporting services point in Configuration Manager.</span></span> <span data-ttu-id="bd3b9-121">Требуется для служб отчетов SQL.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-121">Required for SQL Reporting Services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-122">В Configuration Manager 2007 вы узнаете, <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> как создать точку служб Reporting Services для служб отчетов SQL </a> .</span><span class="sxs-lookup"><span data-stu-id="bd3b9-122">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p>
<p><span data-ttu-id="bd3b9-123">Для System Center 2012 Configuration Manager ознакомьтесь с разделами <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> Предварительные требования для создания отчетов в Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="bd3b9-123">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> <span data-ttu-id="bd3b9-124">Поддерживаемые версии Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-124">Configuration Manager Supported Versions</span></span>


<span data-ttu-id="bd3b9-125">MBAM поддерживает следующие версии Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="bd3b9-125">MBAM supports the following versions of Configuration Manager:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bd3b9-126">Поддерживаемая версия</span><span class="sxs-lookup"><span data-stu-id="bd3b9-126">Supported version</span></span></th>
<th align="left"><span data-ttu-id="bd3b9-127">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="bd3b9-127">Service pack</span></span></th>
<th align="left"><span data-ttu-id="bd3b9-128">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="bd3b9-128">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd3b9-129">Microsoft System Center Configuration Manager 2007 R2</span><span class="sxs-lookup"><span data-stu-id="bd3b9-129">Microsoft System Center Configuration Manager 2007 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-130">SP1 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="bd3b9-130">SP1 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-131">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="bd3b9-131">64-bit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="bd3b9-132">Примечание.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-132">Note</span></span></strong><br/><p><span data-ttu-id="bd3b9-133">Несмотря на то, что Configuration Manager 2007 имеет значение 32, необходимо установить его и SQL Server на 64-разрядную версию операционной системы, чтобы обеспечить соответствие с программным обеспечением 64-bit MBAM.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-133">Although Configuration Manager 2007 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bd3b9-134">Microsoft System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-134">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-135">SP1</span><span class="sxs-lookup"><span data-stu-id="bd3b9-135">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-136">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="bd3b9-136">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="bd3b9-137">Список поддерживаемых конфигураций для сервера Configuration Manager можно найти на соответствующей веб-странице для используемой версии Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-137">For a list of supported configurations for the Configuration Manager Server, see the appropriate webpage for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="bd3b9-138">В MBAM отсутствуют дополнительные требования к системе для сервера Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-138">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> <span data-ttu-id="bd3b9-139">Требования к системе для MBAM и SQL Server</span><span class="sxs-lookup"><span data-stu-id="bd3b9-139">MBAM and SQL Server System Requirements</span></span>


<span data-ttu-id="bd3b9-140">Поддерживаемые конфигурации и требования к системе для серверов MBAM и SQL Server для топологии Configuration Manager совпадают с параметрами изолированной топологии.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-140">The supported configurations and system requirements for the MBAM servers and SQL Server for the Configuration Manager topology are the same as those for the Stand-alone topology.</span></span> <span data-ttu-id="bd3b9-141">Требования к отдельным системам можно найти в разделе [Поддерживаемые конфигурации MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="bd3b9-141">For the Stand-alone system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="bd3b9-142">Сведения о требованиях к MBAM серверу и процессору SQL Server, ОЗУ и дисковому пространству для топологии Configuration Manager можно найти в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-142">For the MBAM Server and SQL Server processor, RAM, and disk space requirements for the Configuration Manager topology, see the following sections.</span></span>

## <span data-ttu-id="bd3b9-143">Требования к MBAM процессору, ОЗУ и дисковому пространству для MBAM</span><span class="sxs-lookup"><span data-stu-id="bd3b9-143">MBAM Server Processor, RAM, and Disk Space Requirements for MBAM</span></span>


<span data-ttu-id="bd3b9-144">В таблице ниже перечислены требования к серверному процессору, ОЗУ и дисковому пространству для серверов MBAM при использовании топологии интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-144">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bd3b9-145">Аппаратный компонент</span><span class="sxs-lookup"><span data-stu-id="bd3b9-145">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="bd3b9-146">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="bd3b9-146">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="bd3b9-147">Рекомендуемое требование</span><span class="sxs-lookup"><span data-stu-id="bd3b9-147">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd3b9-148">Процессор</span><span class="sxs-lookup"><span data-stu-id="bd3b9-148">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-149">2,33 ГГц</span><span class="sxs-lookup"><span data-stu-id="bd3b9-149">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-150">2,33 ГГц или выше</span><span class="sxs-lookup"><span data-stu-id="bd3b9-150">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bd3b9-151">ОЗУ</span><span class="sxs-lookup"><span data-stu-id="bd3b9-151">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-152">4 ГБ</span><span class="sxs-lookup"><span data-stu-id="bd3b9-152">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-153">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="bd3b9-153">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd3b9-154">Свободное место на диске</span><span class="sxs-lookup"><span data-stu-id="bd3b9-154">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-155">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="bd3b9-155">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-156">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="bd3b9-156">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bd3b9-157">Требования для процессора SQL Server, ОЗУ и места на диске</span><span class="sxs-lookup"><span data-stu-id="bd3b9-157">SQL Server Processor, RAM, and Disk Space Requirements</span></span>


<span data-ttu-id="bd3b9-158">В таблице ниже перечислены требования к серверному процессору, ОЗУ и дисковому пространству для компьютера SQL Server при использовании топологии интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-158">The following table lists the server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bd3b9-159">Аппаратный компонент</span><span class="sxs-lookup"><span data-stu-id="bd3b9-159">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="bd3b9-160">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="bd3b9-160">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="bd3b9-161">Рекомендуемое требование</span><span class="sxs-lookup"><span data-stu-id="bd3b9-161">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd3b9-162">Процессор</span><span class="sxs-lookup"><span data-stu-id="bd3b9-162">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-163">2,33 ГГц</span><span class="sxs-lookup"><span data-stu-id="bd3b9-163">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-164">2,33 ГГц или выше</span><span class="sxs-lookup"><span data-stu-id="bd3b9-164">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bd3b9-165">ОЗУ</span><span class="sxs-lookup"><span data-stu-id="bd3b9-165">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-166">4 ГБ</span><span class="sxs-lookup"><span data-stu-id="bd3b9-166">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-167">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="bd3b9-167">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd3b9-168">Свободное место на диске</span><span class="sxs-lookup"><span data-stu-id="bd3b9-168">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-169">5 ГБ</span><span class="sxs-lookup"><span data-stu-id="bd3b9-169">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-170">5 ГБ или больше</span><span class="sxs-lookup"><span data-stu-id="bd3b9-170">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bd3b9-171">Необходимые разрешения для установки сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="bd3b9-171">Required permissions to install the MBAM Server</span></span>


<span data-ttu-id="bd3b9-172">Чтобы установить MBAM с помощью Configuration Manager, необходимо обладать правами администратора в Configuration Manager, у которого есть роль безопасности с минимальными разрешениями, указанными в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-172">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="bd3b9-173">Кроме того, для установки сервера MBAM в таблице также выводятся права, выходящие за основные права администратора компьютера.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-173">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bd3b9-174">Разрешения</span><span class="sxs-lookup"><span data-stu-id="bd3b9-174">Permissions</span></span></th>
<th align="left"><span data-ttu-id="bd3b9-175">Компонент сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="bd3b9-175">MBAM Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd3b9-176">Роли сервера для входа в экземпляр SQL:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="bd3b9-176">SQL instance Login Server Roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="bd3b9-177">База данных для восстановления — база данных аудита</span><span class="sxs-lookup"><span data-stu-id="bd3b9-177">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bd3b9-178">Права экземпляра служб SQL Server Reporting Services:-создание папок — публикация отчетов</span><span class="sxs-lookup"><span data-stu-id="bd3b9-178">SQL Server Reporting Services instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="bd3b9-179">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-179">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="bd3b9-180">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-180">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bd3b9-181">Разрешения</span><span class="sxs-lookup"><span data-stu-id="bd3b9-181">Permissions</span></span></th>
<th align="left"><span data-ttu-id="bd3b9-182">Компонент сервера Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-182">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd3b9-183">Права доступа к сайту Configuration Manager:-Read</span><span class="sxs-lookup"><span data-stu-id="bd3b9-183">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-184">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-184">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bd3b9-185">Права на сбор Configuration Manager:-создание элементов конфигурации и развертывание</span><span class="sxs-lookup"><span data-stu-id="bd3b9-185">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-186">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-186">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd3b9-187">Разрешения элемента конфигурации Configuration Manager:-Create-Delete-Read</span><span class="sxs-lookup"><span data-stu-id="bd3b9-187">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-188">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-188">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="bd3b9-189">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="bd3b9-189">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bd3b9-190">Разрешения</span><span class="sxs-lookup"><span data-stu-id="bd3b9-190">Permissions</span></span></th>
<th align="left"><span data-ttu-id="bd3b9-191">Компонент сервера Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-191">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd3b9-192">Права доступа к сайту Configuration Manager:-Read</span><span class="sxs-lookup"><span data-stu-id="bd3b9-192">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-193">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-193">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bd3b9-194">Права на сбор Configuration Manager:-Create-Delete-Read-ReadResource</span><span class="sxs-lookup"><span data-stu-id="bd3b9-194">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-195">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-195">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd3b9-196">Права конфигурации Configuration Manager:-создание-удаление-чтение и распространение</span><span class="sxs-lookup"><span data-stu-id="bd3b9-196">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-197">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-197">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bd3b9-198">Порядок развертывания функций MBAM для топологии Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-198">Order of Deployment of MBAM Features for the Configuration Manager Topology</span></span>


<span data-ttu-id="bd3b9-199">При развертывании MBAM на сервере Configuration Manager необходимо выполнить задачи развертывания в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-199">When deploying MBAM on the Configuration Manager Server, you must complete the deployment tasks in the following order:</span></span>

1.  <span data-ttu-id="bd3b9-200">Измените файл Configuration. mof на сервере Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-200">Edit the configuration.mof file on the Configuration Manager Server.</span></span>

2.  <span data-ttu-id="bd3b9-201">Создайте или измените сервер конфигурации SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-201">Create or edit the sms\_def.mof file Configuration Manager Server.</span></span>

3.  <span data-ttu-id="bd3b9-202">Установите MBAM на сервере Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-202">Install MBAM on the Configuration Manager Server.</span></span>

4.  <span data-ttu-id="bd3b9-203">Установите базу данных восстановления и базу данных аудита на сервере базы данных.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-203">Install the Recovery Database and the Audit Database on the Database server.</span></span>

5.  <span data-ttu-id="bd3b9-204">Установите компоненты MBAM на сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-204">Install the MBAM features on the Administration and Monitoring Server.</span></span>

## <span data-ttu-id="bd3b9-205">Контрольный список планирования для установки MBAM с помощью Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bd3b9-205">Planning Checklist for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="bd3b9-206">В этом контрольном списке описаны рекомендуемые шаги и высокоуровневый список элементов, которые следует принимать во время планирования развертывания администрирования Microsoft BitLocker и мониторинга с помощью Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-206">This checklist outlines the recommended steps and a high-level list of items to consider when planning for an Microsoft BitLocker Administration and Monitoring deployment with Configuration Manager.</span></span> <span data-ttu-id="bd3b9-207">Рекомендуется скопировать этот контрольный список в программу для работы с электронными таблицами и настроить ее для использования.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-207">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="bd3b9-208">Задача</span><span class="sxs-lookup"><span data-stu-id="bd3b9-208">Task</span></span></th>
<th align="left"><span data-ttu-id="bd3b9-209">Ссылки</span><span class="sxs-lookup"><span data-stu-id="bd3b9-209">References</span></span></th>
<th align="left"><span data-ttu-id="bd3b9-210">Заметки</span><span class="sxs-lookup"><span data-stu-id="bd3b9-210">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bd3b9-211">Ознакомьтесь со сведениями о начале работы, в котором описано, как работает Configuration Manager, в MBAM и показана Рекомендуемая архитектура высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-211">Review the getting started information, which describes how Configuration Manager works with MBAM and shows the recommended high-level architecture.</span></span></p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)"><span data-ttu-id="bd3b9-212">Начало работы — использование MBAM с диспетчером конфигураций</span><span class="sxs-lookup"><span data-stu-id="bd3b9-212">Getting Started - Using MBAM with Configuration Manager</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bd3b9-213">Ознакомьтесь с информацией по планированию, которая описывает требования к развертыванию, Поддерживаемые конфигурации, необходимые разрешения и порядок развертывания для каждой функции.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-213">Review the planning information, which describes the deployment prerequisites, supported configurations, required permissions, and deployment order for each feature.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd3b9-214">Планирование развертывания MBAM с помощью диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="bd3b9-214">Planning to Deploy MBAM with Configuration Manager</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bd3b9-215">Спланируйте и настройте требования к групповой политике MBAM.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-215">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="bd3b9-216">Планирование требований групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="bd3b9-216">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bd3b9-217">Планируйте и создавайте необходимые группы безопасности доменных служб Active Directory и планируйте требования к членству в локальной группе безопасности MBAM.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-217">Plan for and create necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="bd3b9-218">Планирование ролей администратора MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="bd3b9-218">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bd3b9-219">Планируйте развертывание клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="bd3b9-219">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="bd3b9-220">Планирование развертывания клиента MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="bd3b9-220">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bd3b9-221">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="bd3b9-221">Related topics</span></span>


[<span data-ttu-id="bd3b9-222">Использование MBAM с диспетчером конфигураций</span><span class="sxs-lookup"><span data-stu-id="bd3b9-222">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)









