---
title: Поддерживаемые конфигурации MED-V 1.0
description: Поддерживаемые конфигурации MED-V 1.0
author: dansimp
ms.assetid: 74643de6-549e-4177-a559-6407e156ed3a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3b8ffdfb6e34fe7888ea5ace0ff7264bd978a548
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812608"
---
# <span data-ttu-id="ff600-103">Поддерживаемые конфигурации MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ff600-103">MED-V 1.0 Supported Configurations</span></span>


<span data-ttu-id="ff600-104">В этой статье указаны требования, необходимые для установки и запуска Microsoft Enterprise Virtualization (MED-V) 1,0 в среде.</span><span class="sxs-lookup"><span data-stu-id="ff600-104">This topic specifies the requirements necessary to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 in your environment.</span></span>

## <span data-ttu-id="ff600-105">Требования к системе для клиента MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ff600-105">MED-V 1.0 Client System Requirements</span></span>


### <span data-ttu-id="ff600-106">Требования клиентской операционной системы для MED-V</span><span class="sxs-lookup"><span data-stu-id="ff600-106">MED-V Client Operating System Requirements</span></span>

<span data-ttu-id="ff600-107">В таблице ниже перечислены операционные системы, которые поддерживаются при установке клиента MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="ff600-107">The following table lists the operating systems that are supported for MED-V 1.0 client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff600-108">Операционная система</span><span class="sxs-lookup"><span data-stu-id="ff600-108">Operating System</span></span></th>
<th align="left"><span data-ttu-id="ff600-109">Выпуск</span><span class="sxs-lookup"><span data-stu-id="ff600-109">Edition</span></span></th>
<th align="left"><span data-ttu-id="ff600-110">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="ff600-110">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ff600-111">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="ff600-111">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff600-112">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ff600-112">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-113">Профессиональный выпуск</span><span class="sxs-lookup"><span data-stu-id="ff600-113">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-114">SP2 или 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="ff600-114">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-115">x86</span><span class="sxs-lookup"><span data-stu-id="ff600-115">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff600-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff600-116">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-117">Бизнес, Корпоративная или максимальная выпускная версия</span><span class="sxs-lookup"><span data-stu-id="ff600-117">Business, Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-118">Пакет обновления 1 (SP1) или 2</span><span class="sxs-lookup"><span data-stu-id="ff600-118">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-119">x86</span><span class="sxs-lookup"><span data-stu-id="ff600-119">x86</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ff600-120">Примечание.</span><span class="sxs-lookup"><span data-stu-id="ff600-120">Note</span></span>**  
<span data-ttu-id="ff600-121">Клиент MED-V не работает в режиме собственного 64-разрядного режима.</span><span class="sxs-lookup"><span data-stu-id="ff600-121">MED-V client does not run in native x64 mode.</span></span> <span data-ttu-id="ff600-122">Вместо этого MED-V работает в режиме Windows в Windows 64-bit (WOW64) на 64-разрядных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="ff600-122">Instead, MED-V runs in Windows on Windows 64-bit (WOW64) mode on 64-bit computers.</span></span>



### <a href="" id="med-v-1-0-client-configuration-"></a><span data-ttu-id="ff600-123">Конфигурация клиента для MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ff600-123">MED-V 1.0 Client Configuration</span></span>

**<span data-ttu-id="ff600-124">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="ff600-124">.NET Framework Version</span></span>**

<span data-ttu-id="ff600-125">Для установки клиента MED-V 1,0 поддерживаются следующие версии Microsoft .NET Framework:</span><span class="sxs-lookup"><span data-stu-id="ff600-125">The following versions of the Microsoft .NET Framework are supported for MED-V 1.0 client installation:</span></span>

-   <span data-ttu-id="ff600-126">.NET Framework 2,0 или .NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ff600-126">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="ff600-127">.NET Framework 3,0 или .NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ff600-127">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="ff600-128">.NET Framework 3,5 или .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="ff600-128">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="ff600-129">Модуль виртуализации</span><span class="sxs-lookup"><span data-stu-id="ff600-129">Virtualization Engine</span></span>**

<span data-ttu-id="ff600-130">Microsoft Virtual PC 2007 с пакетом обновления 1 (SP1) с исправлением, описанным в статье Microsoft Knowledge Base 974918, поддерживается для установки клиента MED-V 1,0 в указанных ниже конфигурациях.</span><span class="sxs-lookup"><span data-stu-id="ff600-130">Microsoft Virtual PC 2007 SP1 with the hotfix that is described in Microsoft Knowledge Base article 974918 is supported for MED-V 1.0 client installation in the following configurations:</span></span>

-   <span data-ttu-id="ff600-131">Статический файл виртуального жесткого диска (VHD)</span><span class="sxs-lookup"><span data-stu-id="ff600-131">Static Virtual Hard Disk (VHD) file</span></span>

-   <span data-ttu-id="ff600-132">Несколько файлов VHD, расположенных в одном и том же каталоге</span><span class="sxs-lookup"><span data-stu-id="ff600-132">Multiple VHD files located within the same directory</span></span>

-   <span data-ttu-id="ff600-133">Динамический файл виртуального жесткого диска</span><span class="sxs-lookup"><span data-stu-id="ff600-133">Dynamic VHD file</span></span>

**<span data-ttu-id="ff600-134">Интернет-браузер</span><span class="sxs-lookup"><span data-stu-id="ff600-134">Internet Browser</span></span>**

<span data-ttu-id="ff600-135">Windows Internet Explorer 7 и Windows Internet Explorer 8 поддерживаются для установки клиента MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="ff600-135">Windows Internet Explorer 7 and Windows Internet Explorer 8 are supported for MED-V 1.0 client installation.</span></span>

**<span data-ttu-id="ff600-136">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="ff600-136">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="ff600-137">Клиент MED-V не поддерживается в среде сервера Microsoft Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ff600-137">The MED-V client is not supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="ff600-138">Системные требования для рабочих областей MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ff600-138">MED-V 1.0 Workspace System Requirements</span></span>


### <span data-ttu-id="ff600-139">Требования к операционной системе для рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="ff600-139">MED-V Workspace Operating System Requirements</span></span>

<span data-ttu-id="ff600-140">В таблице ниже перечислены операционные системы, поддерживаемые в рабочих областях для MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="ff600-140">The following table lists the operating systems supported for MED-V 1.0 workspaces.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff600-141">Операционная система</span><span class="sxs-lookup"><span data-stu-id="ff600-141">Operating System</span></span></th>
<th align="left"><span data-ttu-id="ff600-142">Выпуск</span><span class="sxs-lookup"><span data-stu-id="ff600-142">Edition</span></span></th>
<th align="left"><span data-ttu-id="ff600-143">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="ff600-143">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ff600-144">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="ff600-144">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff600-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ff600-145">Windows 2000</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-146">Профессиональная</span><span class="sxs-lookup"><span data-stu-id="ff600-146">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-147">Сервис</span><span class="sxs-lookup"><span data-stu-id="ff600-147">SP4</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-148">Выпуск</span><span class="sxs-lookup"><span data-stu-id="ff600-148">X86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff600-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ff600-149">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-150">Профессиональный выпуск</span><span class="sxs-lookup"><span data-stu-id="ff600-150">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-151">SP2 или 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="ff600-151">SP2 or SP3</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ff600-152">Примечание.</span><span class="sxs-lookup"><span data-stu-id="ff600-152">Note</span></span></strong><br/><p><span data-ttu-id="ff600-153">Для обеспечения совместимости рабочей области MED-V с будущими версиями MED-V рекомендуется использовать пакет обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="ff600-153">SP3 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="ff600-154">x86</span><span class="sxs-lookup"><span data-stu-id="ff600-154">x86</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-workspace-configuration-"></a><span data-ttu-id="ff600-155">Настройка рабочей области для MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ff600-155">MED-V 1.0 Workspace Configuration</span></span>

**<span data-ttu-id="ff600-156">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="ff600-156">.NET Framework Version</span></span>**

<span data-ttu-id="ff600-157">Для использования MED-V требуется одна из указанных ниже поддерживаемых версий Microsoft .NET Framework для MED-V 1,0 Workspace:</span><span class="sxs-lookup"><span data-stu-id="ff600-157">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="ff600-158">.NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ff600-158">.NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="ff600-159">.NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ff600-159">.NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="ff600-160">.NET Framework 3,5 или .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="ff600-160">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="ff600-161">Примечание.</span><span class="sxs-lookup"><span data-stu-id="ff600-161">Note</span></span>**  
<span data-ttu-id="ff600-162">.NET Framework 3,5 с пакетом обновления 1 (SP1) рекомендуется использовать для обеспечения совместимости рабочей области MED-V с будущими версиями MED-V.</span><span class="sxs-lookup"><span data-stu-id="ff600-162">.NET Framework 3.5 SP1 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span>



**<span data-ttu-id="ff600-163">Интернет-браузер</span><span class="sxs-lookup"><span data-stu-id="ff600-163">Internet Browser</span></span>**

<span data-ttu-id="ff600-164">Windows Internet Explorer 6 с пакетом обновления 2 (SP2) и Windows Internet Explorer 7 поддерживаются для установки рабочей области MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="ff600-164">Windows Internet Explorer 6 SP2 and Windows Internet Explorer 7 are supported for the MED-V 1.0 workspace installation.</span></span>

### <a href="" id="med-v-workspace-images-"></a><span data-ttu-id="ff600-165">Образы рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="ff600-165">MED-V Workspace Images</span></span>

<span data-ttu-id="ff600-166">Образы рабочих областей для MED-V должны создаваться с помощью Virtual PC 2007 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ff600-166">MED-V workspace images must be created by using Virtual PC 2007 SP1.</span></span>

## <span data-ttu-id="ff600-167">Требования к серверной системе для MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ff600-167">MED-V 1.0 Server System Requirements</span></span>


### <span data-ttu-id="ff600-168">Требования к серверной операционной системе для MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ff600-168">MED-V 1.0 Server Operating System Requirements</span></span>

<span data-ttu-id="ff600-169">В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="ff600-169">The following table lists the operating systems supported for MED-V 1.0 server installations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff600-170">Операционная система</span><span class="sxs-lookup"><span data-stu-id="ff600-170">Operating System</span></span></th>
<th align="left"><span data-ttu-id="ff600-171">Выпуск</span><span class="sxs-lookup"><span data-stu-id="ff600-171">Edition</span></span></th>
<th align="left"><span data-ttu-id="ff600-172">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="ff600-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ff600-173">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="ff600-173">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff600-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff600-174">Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-175">Standard или Enterprise</span><span class="sxs-lookup"><span data-stu-id="ff600-175">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-176">Нет</span><span class="sxs-lookup"><span data-stu-id="ff600-176">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-177">X86 или x64</span><span class="sxs-lookup"><span data-stu-id="ff600-177">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-server-configuration-"></a><span data-ttu-id="ff600-178">Конфигурация сервера MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ff600-178">MED-V 1.0 Server Configuration</span></span>

**<span data-ttu-id="ff600-179">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="ff600-179">.NET Framework Version</span></span>**

<span data-ttu-id="ff600-180">Для использования MED-V требуется одна из указанных ниже поддерживаемых версий Microsoft .NET Framework для MED-V 1,0 Workspace:</span><span class="sxs-lookup"><span data-stu-id="ff600-180">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="ff600-181">.NET Framework 2,0 или .NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ff600-181">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="ff600-182">.NET Framework 3,0 или .NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ff600-182">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="ff600-183">.NET Framework 3,5 или .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="ff600-183">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="ff600-184">Версия Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="ff600-184">Microsoft SQL Server Version</span></span>**

<span data-ttu-id="ff600-185">Следующие версии Microsoft SQL Server поддерживаются для MED-V 1,0, когда SQL Server установлен локально или удаленно с сервера MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="ff600-185">The following versions of Microsoft SQL Server are supported for MED-V 1.0 when SQL Server is installed locally or remotely from the MED-V 1.0 Server:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff600-186">Версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="ff600-186">SQL Server Version</span></span></th>
<th align="left"><span data-ttu-id="ff600-187">Выпуск</span><span class="sxs-lookup"><span data-stu-id="ff600-187">Edition</span></span></th>
<th align="left"><span data-ttu-id="ff600-188">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="ff600-188">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ff600-189">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="ff600-189">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff600-190">SQL Server 2005</span><span class="sxs-lookup"><span data-stu-id="ff600-190">SQL Server 2005</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-191">Экспресс, стандартная или Корпоративная выпускная версия</span><span class="sxs-lookup"><span data-stu-id="ff600-191">Express, Standard, or Enterprise Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-192">SP2</span><span class="sxs-lookup"><span data-stu-id="ff600-192">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-193">X86 или x64</span><span class="sxs-lookup"><span data-stu-id="ff600-193">X86 or x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff600-194">SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff600-194">SQL Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-195">Экспресс, стандартная или Корпоративная</span><span class="sxs-lookup"><span data-stu-id="ff600-195">Express, Standard, or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-196">Нет</span><span class="sxs-lookup"><span data-stu-id="ff600-196">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff600-197">X86 или x64</span><span class="sxs-lookup"><span data-stu-id="ff600-197">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ff600-198">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="ff600-198">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="ff600-199">Сервер MED-V поддерживается в среде Microsoft Hyper-V Server.</span><span class="sxs-lookup"><span data-stu-id="ff600-199">The MED-V server is supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="ff600-200">Сведения о глобализации для MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ff600-200">MED-V 1.0 Globalization Information</span></span>


<span data-ttu-id="ff600-201">Несмотря на то что MED-V не выпускается на языках, отличных от английского, для установки клиента, рабочей области и сервера MED-V 1,0 поддерживаются следующие языковые версии операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="ff600-201">Although MED-V is not released in languages other than English, the following Windows operating system language versions are supported for the MED-V 1.0 client, workspace, and server installations:</span></span>

-   <span data-ttu-id="ff600-202">Английский</span><span class="sxs-lookup"><span data-stu-id="ff600-202">English</span></span>

-   <span data-ttu-id="ff600-203">Французский</span><span class="sxs-lookup"><span data-stu-id="ff600-203">French</span></span>

-   <span data-ttu-id="ff600-204">Немецкий</span><span class="sxs-lookup"><span data-stu-id="ff600-204">German</span></span>

-   <span data-ttu-id="ff600-205">Итальянский</span><span class="sxs-lookup"><span data-stu-id="ff600-205">Italian</span></span>

-   <span data-ttu-id="ff600-206">Испанский</span><span class="sxs-lookup"><span data-stu-id="ff600-206">Spanish</span></span>

-   <span data-ttu-id="ff600-207">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="ff600-207">Portuguese (Brazil)</span></span>









