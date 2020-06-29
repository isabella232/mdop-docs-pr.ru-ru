---
title: Поддерживаемые конфигурации MBAM 1.0
description: Поддерживаемые конфигурации MBAM 1.0
author: dansimp
ms.assetid: 1f5ac58e-6a3f-47df-8a9b-4b57631ab9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2c72320379d1c9328a6b40537d37998402b1b38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825939"
---
# <span data-ttu-id="de26d-103">Поддерживаемые конфигурации MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="de26d-103">MBAM 1.0 Supported Configurations</span></span>


<span data-ttu-id="de26d-104">В этой статье указаны необходимые требования для установки и запуска администрирования и мониторинга Microsoft BitLocker (MBAM) в среде.</span><span class="sxs-lookup"><span data-stu-id="de26d-104">This topic specifies the necessary requirements to install and run Microsoft BitLocker Administration and Monitoring (MBAM) in your environment.</span></span>

## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="de26d-105">Требования к серверной системе MBAM</span><span class="sxs-lookup"><span data-stu-id="de26d-105">MBAM server system Requirements</span></span>


### <span data-ttu-id="de26d-106">Требования к серверной операционной системе</span><span class="sxs-lookup"><span data-stu-id="de26d-106">Server operating system requirements</span></span>

<span data-ttu-id="de26d-107">В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="de26d-107">The following table lists the operating systems that are supported for the Microsoft BitLocker Administration and Monitoring Server installation.</span></span>

**<span data-ttu-id="de26d-108">Примечание.</span><span class="sxs-lookup"><span data-stu-id="de26d-108">Note</span></span>**  
<span data-ttu-id="de26d-109">Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="de26d-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="de26d-110">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="de26d-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="de26d-111">Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="de26d-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="de26d-112">Операционная система</span><span class="sxs-lookup"><span data-stu-id="de26d-112">Operating System</span></span></th>
<th align="left"><span data-ttu-id="de26d-113">Выпуск</span><span class="sxs-lookup"><span data-stu-id="de26d-113">Edition</span></span></th>
<th align="left"><span data-ttu-id="de26d-114">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="de26d-114">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="de26d-115">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="de26d-115">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de26d-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de26d-116">Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-117">Стандартная, Корпоративная, для центра обработки данных или веб-сервера</span><span class="sxs-lookup"><span data-stu-id="de26d-117">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-118">Только SP2</span><span class="sxs-lookup"><span data-stu-id="de26d-118">SP2 only</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-119">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="de26d-119">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de26d-120">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="de26d-120">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-121">Стандартная, Корпоративная, для центра обработки данных или веб-сервера</span><span class="sxs-lookup"><span data-stu-id="de26d-121">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="de26d-122">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="de26d-122">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="de26d-123">Warning</span><span class="sxs-lookup"><span data-stu-id="de26d-123">Warning</span></span>**  
<span data-ttu-id="de26d-124">Установка служб MBAM, отчетов и баз данных на компьютере контроллера домена не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="de26d-124">There is no support for installing MBAM services, reports, or databases on a domain controller computer.</span></span>



### <a href="" id="server-random-access-memory--ram--requirements-"></a><span data-ttu-id="de26d-125">Требования к оперативной памяти (RAM) сервера</span><span class="sxs-lookup"><span data-stu-id="de26d-125">Server random access memory (RAM) requirements</span></span>

<span data-ttu-id="de26d-126">Нет требований к ОЗУ, которые относятся к установке сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="de26d-126">There are no RAM requirements that are specific to MBAM Server installation.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="de26d-127">Требования к базам данных SQL Server</span><span class="sxs-lookup"><span data-stu-id="de26d-127">SQL Server Database requirements</span></span>

<span data-ttu-id="de26d-128">В следующей таблице перечислены версии SQL Server, которые поддерживаются при установке компонентов сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="de26d-128">The following table lists the SQL Server versions that are supported for the MBAM Server feature installation.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="de26d-129">Компонент сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="de26d-129">MBAM Server Feature</span></span></th>
<th align="left"><span data-ttu-id="de26d-130">Версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="de26d-130">SQL Server Version</span></span></th>
<th align="left"><span data-ttu-id="de26d-131">Выпуск</span><span class="sxs-lookup"><span data-stu-id="de26d-131">Edition</span></span></th>
<th align="left"><span data-ttu-id="de26d-132">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="de26d-132">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="de26d-133">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="de26d-133">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de26d-134">Отчеты о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="de26d-134">Compliance and Audit Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-135">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="de26d-135">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="de26d-136">R2, Стандартный, корпоративный, центр обработки данных или выпуск для разработчиков</span><span class="sxs-lookup"><span data-stu-id="de26d-136">R2, Standard, Enterprise, Datacenter, or Developer Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-137">SP2</span><span class="sxs-lookup"><span data-stu-id="de26d-137">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-138">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="de26d-138">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de26d-139">База данных восстановления и оборудования</span><span class="sxs-lookup"><span data-stu-id="de26d-139">Recovery and Hardware Database</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-140">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="de26d-140">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="de26d-141">R2, Enterprise, Datacenter или Developer Edition</span><span class="sxs-lookup"><span data-stu-id="de26d-141">R2, Enterprise, Datacenter, or Developer Edition</span></span></p>
<div class="alert">
<strong><span data-ttu-id="de26d-142">Важно.</span><span class="sxs-lookup"><span data-stu-id="de26d-142">Important</span></span></strong><br/><p><span data-ttu-id="de26d-143">Стандартные выпуски SQL Server не поддерживаются для восстановления MBAM и установки компонента сервера базы данных оборудования.</span><span class="sxs-lookup"><span data-stu-id="de26d-143">SQL Server Standard Editions are not supported for MBAM Recovery and Hardware Database Server feature installation.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="de26d-144">SP2</span><span class="sxs-lookup"><span data-stu-id="de26d-144">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-145">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="de26d-145">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de26d-146">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="de26d-146">Compliance and Audit Database</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-147">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="de26d-147">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="de26d-148">R2, Стандартный, корпоративный, центр обработки данных или выпуск для разработчиков</span><span class="sxs-lookup"><span data-stu-id="de26d-148">R2, Standard, Enterprise, Datacenter, or Developer Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-149">SP2</span><span class="sxs-lookup"><span data-stu-id="de26d-149">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-150">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="de26d-150">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="de26d-151">Требования к системе клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="de26d-151">MBAM Client system requirements</span></span>


### <span data-ttu-id="de26d-152">Требования к операционной системе клиента</span><span class="sxs-lookup"><span data-stu-id="de26d-152">Client operating system requirements</span></span>

<span data-ttu-id="de26d-153">В таблице ниже перечислены операционные системы, которые поддерживаются при установке клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="de26d-153">The following table lists the operating systems that are supported for MBAM Client installation.</span></span>

**<span data-ttu-id="de26d-154">Примечание.</span><span class="sxs-lookup"><span data-stu-id="de26d-154">Note</span></span>**  
<span data-ttu-id="de26d-155">Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="de26d-155">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="de26d-156">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="de26d-156">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="de26d-157">Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="de26d-157">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="de26d-158">Операционная система</span><span class="sxs-lookup"><span data-stu-id="de26d-158">Operating System</span></span></th>
<th align="left"><span data-ttu-id="de26d-159">Выпуск</span><span class="sxs-lookup"><span data-stu-id="de26d-159">Edition</span></span></th>
<th align="left"><span data-ttu-id="de26d-160">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="de26d-160">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="de26d-161">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="de26d-161">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de26d-162">Windows 7;</span><span class="sxs-lookup"><span data-stu-id="de26d-162">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-163">выпуск Корпоративная</span><span class="sxs-lookup"><span data-stu-id="de26d-163">Enterprise Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-164">Нет, SP1</span><span class="sxs-lookup"><span data-stu-id="de26d-164">None, SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-165">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="de26d-165">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de26d-166">Windows 7;</span><span class="sxs-lookup"><span data-stu-id="de26d-166">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-167">Максимальная выпускная версия</span><span class="sxs-lookup"><span data-stu-id="de26d-167">Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-168">Нет, SP1</span><span class="sxs-lookup"><span data-stu-id="de26d-168">None, SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="de26d-169">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="de26d-169">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="de26d-170">Требования к ОЗУ для клиента</span><span class="sxs-lookup"><span data-stu-id="de26d-170">Client RAM requirements</span></span>

<span data-ttu-id="de26d-171">Нет требований к ОЗУ, которые относятся к установке клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="de26d-171">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <span data-ttu-id="de26d-172">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="de26d-172">Related topics</span></span>


[<span data-ttu-id="de26d-173">Планирование развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="de26d-173">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="de26d-174">Необходимые компоненты развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="de26d-174">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)









