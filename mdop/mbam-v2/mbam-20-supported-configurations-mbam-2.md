---
title: Поддерживаемые конфигурации MBAM 2.0
description: Поддерживаемые конфигурации MBAM 2.0
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823909"
---
# <span data-ttu-id="1fe52-103">Поддерживаемые конфигурации MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="1fe52-103">MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="1fe52-104">В этой статье указаны требования для установки и запуска администрирования и мониторинга Microsoft BitLocker (MBAM) 2,0 в среде с помощью изолированной топологии.</span><span class="sxs-lookup"><span data-stu-id="1fe52-104">This topic specifies the requirements to install and run Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in your environment by using the Stand-alone topology.</span></span> <span data-ttu-id="1fe52-105">Для поддерживаемых конфигураций, которые относятся к более поздним выпускам, ознакомьтесь с документацией по соответствующему выпуску.</span><span class="sxs-lookup"><span data-stu-id="1fe52-105">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="1fe52-106">Если вы планируете установить MBAM 2,0 с помощью топологии Configuration Manager и хотите просмотреть список требований к системе, ознакомьтесь с [Разпланированием развертывания MBAM с помощью Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="1fe52-106">If you plan to install MBAM 2.0 by using the Configuration Manager topology and want to review a list of the system requirements, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="1fe52-107">Рекомендуемая конфигурация для запуска MBAM в рабочей среде состоит из двух серверов, в зависимости от требований к масштабируемости.</span><span class="sxs-lookup"><span data-stu-id="1fe52-107">The recommended configuration for running MBAM in a production environment is with two servers, depending on your scalability requirements.</span></span> <span data-ttu-id="1fe52-108">Эта конфигурация поддерживает до 200 000 MBAM клиентов.</span><span class="sxs-lookup"><span data-stu-id="1fe52-108">This configuration supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="1fe52-109">Изображение и описания изолированной инфраструктуры сервера MBAM можно найти в разделе [архитектура высокого уровня для MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1fe52-109">For an image and descriptions of the Stand-alone MBAM server infrastructure, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="1fe52-110">**Примечание**  Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="1fe52-110">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="1fe52-111">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="1fe52-111">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="1fe52-112">Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="1fe52-112">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="1fe52-113">Требования к серверной системе MBAM</span><span class="sxs-lookup"><span data-stu-id="1fe52-113">MBAM Server System Requirements</span></span>


### <span data-ttu-id="1fe52-114">Требования к серверной операционной системе</span><span class="sxs-lookup"><span data-stu-id="1fe52-114">Server Operating System Requirements</span></span>

<span data-ttu-id="1fe52-115">В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1fe52-115">The following table lists the operating systems that are supported for the Microsoft BitLocker Administration and Monitoring Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fe52-116">Операционная система</span><span class="sxs-lookup"><span data-stu-id="1fe52-116">Operating system</span></span></th>
<th align="left"><span data-ttu-id="1fe52-117">Выпуск</span><span class="sxs-lookup"><span data-stu-id="1fe52-117">Edition</span></span></th>
<th align="left"><span data-ttu-id="1fe52-118">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="1fe52-118">Service pack</span></span></th>
<th align="left"><span data-ttu-id="1fe52-119">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="1fe52-119">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fe52-120">WindowsServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="1fe52-120">WindowsServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-121">Standard, Enterprise и Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="1fe52-121">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-122">SP1</span><span class="sxs-lookup"><span data-stu-id="1fe52-122">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-123">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="1fe52-123">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fe52-124">WindowsServer2012</span><span class="sxs-lookup"><span data-stu-id="1fe52-124">WindowsServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-125">Standard или Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="1fe52-125">Standard or Datacenter Edition</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="1fe52-126">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="1fe52-126">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1fe52-127">**Примечание**  Установка служб MBAM, отчетов и баз данных на компьютере контроллера домена не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1fe52-127">**Note** There is no support for installing MBAM services, reports, or databases on a domain controller computer.</span></span>

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a><span data-ttu-id="1fe52-128">Требования к серверному процессору, ОЗУ и дисковому пространству</span><span class="sxs-lookup"><span data-stu-id="1fe52-128">Server Processor, RAM, and Disk Space Requirements</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fe52-129">Аппаратный компонент</span><span class="sxs-lookup"><span data-stu-id="1fe52-129">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="1fe52-130">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="1fe52-130">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="1fe52-131">Рекомендуемое требование</span><span class="sxs-lookup"><span data-stu-id="1fe52-131">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fe52-132">Процессор</span><span class="sxs-lookup"><span data-stu-id="1fe52-132">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-133">2,33 ГГц</span><span class="sxs-lookup"><span data-stu-id="1fe52-133">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-134">2,33 ГГц или выше</span><span class="sxs-lookup"><span data-stu-id="1fe52-134">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fe52-135">ОЗУ</span><span class="sxs-lookup"><span data-stu-id="1fe52-135">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-136">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="1fe52-136">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-137">12 ГБ</span><span class="sxs-lookup"><span data-stu-id="1fe52-137">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fe52-138">Свободное место на диске</span><span class="sxs-lookup"><span data-stu-id="1fe52-138">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-139">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="1fe52-139">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-140">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="1fe52-140">2 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="1fe52-141">Требования к базам данных SQLServer</span><span class="sxs-lookup"><span data-stu-id="1fe52-141">SQLServer Database Requirements</span></span>

<span data-ttu-id="1fe52-142">В приведенной ниже таблице перечислены версии SQLServer, которые поддерживаются при установке компонентов сервера администрирования и мониторинга, включая базу данных восстановления, базу данных соответствия требованиям и сведения о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="1fe52-142">The following table lists the SQLServer versions that are supported for the Administration and Monitoring Server feature installation, which includes the Recovery Database, Compliance and Audit Database, and Compliance and Audit Reports.</span></span> <span data-ttu-id="1fe52-143">Кроме того, для баз данных дополнительно требуется установка средств управления SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1fe52-143">The databases additionally require the installation of SQL Server Management Tools.</span></span>

<span data-ttu-id="1fe52-144">**Примечание**  MBAM изначально не поддерживает группы кластеризации, зеркального отображения и доступности SQL.</span><span class="sxs-lookup"><span data-stu-id="1fe52-144">**Note** MBAM does not natively support SQL clustering, mirroring, or Availability Groups.</span></span> <span data-ttu-id="1fe52-145">Чтобы установить базу данных, необходимо выполнить установку сервера MBAM на отдельном сервере SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1fe52-145">To install the databases, you must run the MBAM Server installation on a stand-alone SQL server.</span></span>

 

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fe52-146">Версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="1fe52-146">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="1fe52-147">Выпуск</span><span class="sxs-lookup"><span data-stu-id="1fe52-147">Edition</span></span></th>
<th align="left"><span data-ttu-id="1fe52-148">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="1fe52-148">Service pack</span></span></th>
<th align="left"><span data-ttu-id="1fe52-149">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="1fe52-149">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fe52-150">MicrosoftSQLServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="1fe52-150">MicrosoftSQLServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-151">Standard, Enterprise и Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="1fe52-151">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-152">SP1</span><span class="sxs-lookup"><span data-stu-id="1fe52-152">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-153">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="1fe52-153">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fe52-154">MicrosoftSQLServer2012</span><span class="sxs-lookup"><span data-stu-id="1fe52-154">MicrosoftSQLServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-155">Standard, Enterprise и Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="1fe52-155">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-156">SP1</span><span class="sxs-lookup"><span data-stu-id="1fe52-156">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-157">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="1fe52-157">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fe52-158">Аппаратный компонент</span><span class="sxs-lookup"><span data-stu-id="1fe52-158">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="1fe52-159">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="1fe52-159">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="1fe52-160">Рекомендуемое требование</span><span class="sxs-lookup"><span data-stu-id="1fe52-160">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fe52-161">Процессор</span><span class="sxs-lookup"><span data-stu-id="1fe52-161">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-162">2,33 ГГц</span><span class="sxs-lookup"><span data-stu-id="1fe52-162">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-163">2,33 ГГц или выше</span><span class="sxs-lookup"><span data-stu-id="1fe52-163">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fe52-164">ОЗУ</span><span class="sxs-lookup"><span data-stu-id="1fe52-164">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-165">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="1fe52-165">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-166">12 ГБ</span><span class="sxs-lookup"><span data-stu-id="1fe52-166">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fe52-167">Свободное место на диске</span><span class="sxs-lookup"><span data-stu-id="1fe52-167">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-168">5 ГБ</span><span class="sxs-lookup"><span data-stu-id="1fe52-168">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-169">5 ГБ или больше</span><span class="sxs-lookup"><span data-stu-id="1fe52-169">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="1fe52-170">Требования к системе клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="1fe52-170">MBAM Client System Requirements</span></span>


### <span data-ttu-id="1fe52-171">Требования к операционной системе клиента</span><span class="sxs-lookup"><span data-stu-id="1fe52-171">Client Operating System Requirements</span></span>

<span data-ttu-id="1fe52-172">В таблице ниже перечислены операционные системы, которые поддерживаются для администрирования Microsoft BitLocker и наблюдения за установкой клиентов.</span><span class="sxs-lookup"><span data-stu-id="1fe52-172">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fe52-173">Операционная система</span><span class="sxs-lookup"><span data-stu-id="1fe52-173">Operating system</span></span></th>
<th align="left"><span data-ttu-id="1fe52-174">Выпуск</span><span class="sxs-lookup"><span data-stu-id="1fe52-174">Edition</span></span></th>
<th align="left"><span data-ttu-id="1fe52-175">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="1fe52-175">Service pack</span></span></th>
<th align="left"><span data-ttu-id="1fe52-176">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="1fe52-176">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fe52-177">Windows7</span><span class="sxs-lookup"><span data-stu-id="1fe52-177">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-178">Корпоративная или максимальная выпускная версия</span><span class="sxs-lookup"><span data-stu-id="1fe52-178">Enterprise or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-179">SP1</span><span class="sxs-lookup"><span data-stu-id="1fe52-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-180">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="1fe52-180">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fe52-181">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1fe52-181">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-182">выпуск Корпоративная</span><span class="sxs-lookup"><span data-stu-id="1fe52-182">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="1fe52-183">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="1fe52-183">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fe52-184">Windows с собой</span><span class="sxs-lookup"><span data-stu-id="1fe52-184">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-185">Windows 8 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="1fe52-185">Windows 8 Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="1fe52-186">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="1fe52-186">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="1fe52-187">Требования к ОЗУ для клиента</span><span class="sxs-lookup"><span data-stu-id="1fe52-187">Client RAM Requirements</span></span>

<span data-ttu-id="1fe52-188">Нет требований к ОЗУ, которые относятся к установке и мониторингу клиента Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1fe52-188">There are no RAM requirements that are specific to the Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="1fe52-189">Системные требования для групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="1fe52-189">MBAM Group Policy System Requirements</span></span>


<span data-ttu-id="1fe52-190">В таблице ниже перечислены операционные системы, которые поддерживаются для администрирования Microsoft BitLocker и наблюдения за установкой шаблонов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1fe52-190">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Group Policy template installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fe52-191">Операционная система</span><span class="sxs-lookup"><span data-stu-id="1fe52-191">Operating system</span></span></th>
<th align="left"><span data-ttu-id="1fe52-192">Выпуск</span><span class="sxs-lookup"><span data-stu-id="1fe52-192">Edition</span></span></th>
<th align="left"><span data-ttu-id="1fe52-193">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="1fe52-193">Service pack</span></span></th>
<th align="left"><span data-ttu-id="1fe52-194">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="1fe52-194">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fe52-195">Windows7</span><span class="sxs-lookup"><span data-stu-id="1fe52-195">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-196">Корпоративная или максимальная выпускная версия</span><span class="sxs-lookup"><span data-stu-id="1fe52-196">Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-197">SP1</span><span class="sxs-lookup"><span data-stu-id="1fe52-197">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-198">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="1fe52-198">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fe52-199">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1fe52-199">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-200">выпуск Корпоративная</span><span class="sxs-lookup"><span data-stu-id="1fe52-200">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="1fe52-201">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="1fe52-201">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fe52-202">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="1fe52-202">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-203">Standard, Enterprise и Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="1fe52-203">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-204">SP1</span><span class="sxs-lookup"><span data-stu-id="1fe52-204">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-205">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="1fe52-205">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fe52-206">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1fe52-206">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fe52-207">Standard или Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="1fe52-207">Standard or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="1fe52-208">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="1fe52-208">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1fe52-209">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1fe52-209">Related topics</span></span>


[<span data-ttu-id="1fe52-210">Планирование развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="1fe52-210">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="1fe52-211">Необходимые условия для развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="1fe52-211">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





