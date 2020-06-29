---
title: Класс WMI пакета App-V
description: Класс WMI пакета App-V
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819799"
---
# <span data-ttu-id="1acd9-103">Класс WMI пакета App-V</span><span class="sxs-lookup"><span data-stu-id="1acd9-103">App-V Package WMI Class</span></span>


<span data-ttu-id="1acd9-104">В клиенте Application Virtualization (App-V) класс **Package** является классом инструментария управления Windows (WMI), который представляет все виртуальные пакеты на клиенте.</span><span class="sxs-lookup"><span data-stu-id="1acd9-104">In the Application Virtualization (App-V) Client, the **Package** class is a Windows Management Instrumentation (WMI) class that represents all the virtual packages on the client.</span></span> <span data-ttu-id="1acd9-105">Виртуальные пакеты могут содержать множество виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="1acd9-105">The virtual packages can contain many virtual applications.</span></span>

## <span data-ttu-id="1acd9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1acd9-106">Syntax</span></span>


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## <span data-ttu-id="1acd9-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="1acd9-107">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="1acd9-108">Имя</span><span class="sxs-lookup"><span data-stu-id="1acd9-108">Name</span></span>**  
<span data-ttu-id="1acd9-109">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1acd9-109">Data type: **String**</span></span>

<span data-ttu-id="1acd9-110">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="1acd9-110">Access type: Read-only</span></span>

<span data-ttu-id="1acd9-111">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="1acd9-111">Qualifiers: None</span></span>

<span data-ttu-id="1acd9-112">Понятное имя виртуального пакета.</span><span class="sxs-lookup"><span data-stu-id="1acd9-112">The user-friendly name of the virtual package.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="1acd9-113">Версия</span><span class="sxs-lookup"><span data-stu-id="1acd9-113">Version</span></span>**  
<span data-ttu-id="1acd9-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1acd9-114">Data type: **String**</span></span>

<span data-ttu-id="1acd9-115">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="1acd9-115">Access type: Read-only</span></span>

<span data-ttu-id="1acd9-116">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="1acd9-116">Qualifiers: None</span></span>

<span data-ttu-id="1acd9-117">Версия виртуального пакета.</span><span class="sxs-lookup"><span data-stu-id="1acd9-117">The version of the virtual package.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="1acd9-118">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="1acd9-118">PackageGUID</span></span>**  
<span data-ttu-id="1acd9-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1acd9-119">Data type: **String**</span></span>

<span data-ttu-id="1acd9-120">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="1acd9-120">Access type: Read-only</span></span>

<span data-ttu-id="1acd9-121">Квалификаторы: Key</span><span class="sxs-lookup"><span data-stu-id="1acd9-121">Qualifiers: Key</span></span>

<span data-ttu-id="1acd9-122">Идентификатор GUID конфигурации пакета и исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="1acd9-122">The GUID identifier of the package configuration and source files.</span></span>

<a href="" id="sftpath"></a>**<span data-ttu-id="1acd9-123">SftPath</span><span class="sxs-lookup"><span data-stu-id="1acd9-123">SftPath</span></span>**  
<span data-ttu-id="1acd9-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1acd9-124">Data type: **String**</span></span>

<span data-ttu-id="1acd9-125">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="1acd9-125">Access type: Read-only</span></span>

<span data-ttu-id="1acd9-126">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="1acd9-126">Qualifiers: None</span></span>

<span data-ttu-id="1acd9-127">Путь к файлу SFT.</span><span class="sxs-lookup"><span data-stu-id="1acd9-127">The file path of the SFT file.</span></span>

<a href="" id="totalsize"></a>**<span data-ttu-id="1acd9-128">TotalSize</span><span class="sxs-lookup"><span data-stu-id="1acd9-128">TotalSize</span></span>**  
<span data-ttu-id="1acd9-129">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1acd9-129">Data type: **UInt64**</span></span>

<span data-ttu-id="1acd9-130">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="1acd9-130">Access type: Read-only</span></span>

<span data-ttu-id="1acd9-131">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="1acd9-131">Qualifiers: None</span></span>

<span data-ttu-id="1acd9-132">Общий размер виртуального пакета (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="1acd9-132">The total size of the virtual package, in kilobytes.</span></span>

<a href="" id="cachedsize"></a>**<span data-ttu-id="1acd9-133">CachedSize</span><span class="sxs-lookup"><span data-stu-id="1acd9-133">CachedSize</span></span>**  
<span data-ttu-id="1acd9-134">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1acd9-134">Data type: **UInt64**</span></span>

<span data-ttu-id="1acd9-135">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="1acd9-135">Access type: Read-only</span></span>

<span data-ttu-id="1acd9-136">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="1acd9-136">Qualifiers: None</span></span>

<span data-ttu-id="1acd9-137">Общий размер кэша для виртуального пакета (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="1acd9-137">The total size of the cache for the virtual package, in kilobytes.</span></span>

<a href="" id="launchsize"></a>**<span data-ttu-id="1acd9-138">LaunchSize</span><span class="sxs-lookup"><span data-stu-id="1acd9-138">LaunchSize</span></span>**  
<span data-ttu-id="1acd9-139">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1acd9-139">Data type: **UInt64**</span></span>

<span data-ttu-id="1acd9-140">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="1acd9-140">Access type: Read-only</span></span>

<span data-ttu-id="1acd9-141">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="1acd9-141">Qualifiers: None</span></span>

<span data-ttu-id="1acd9-142">Общий размер основного блока компонентов виртуального пакета в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="1acd9-142">The total size of the virtual package’s primary feature block, in kilobytes.</span></span>

<a href="" id="cachedlaunchsize"></a>**<span data-ttu-id="1acd9-143">CachedLaunchSize</span><span class="sxs-lookup"><span data-stu-id="1acd9-143">CachedLaunchSize</span></span>**  
<span data-ttu-id="1acd9-144">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1acd9-144">Data type: **UInt64**</span></span>

<span data-ttu-id="1acd9-145">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="1acd9-145">Access type: Read-only</span></span>

<span data-ttu-id="1acd9-146">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="1acd9-146">Qualifiers: None</span></span>

<span data-ttu-id="1acd9-147">Общий размер основного блока функций виртуального пакета, который был кэширован (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="1acd9-147">Total size of the virtual package’s primary feature block that has been cached, in kilobytes.</span></span>

<a href="" id="inuse"></a>**<span data-ttu-id="1acd9-148">InUse</span><span class="sxs-lookup"><span data-stu-id="1acd9-148">InUse</span></span>**  
<span data-ttu-id="1acd9-149">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1acd9-149">Data type: **Boolean**</span></span>

<span data-ttu-id="1acd9-150">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="1acd9-150">Access type: Read-only</span></span>

<span data-ttu-id="1acd9-151">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="1acd9-151">Qualifiers: None</span></span>

<span data-ttu-id="1acd9-152">**значение true** , если любое виртуальное приложение в виртуальном пакете запущено; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1acd9-152">**true** if any virtual application in the virtual package is running; otherwise **false**.</span></span>

<a href="" id="locked"></a>**<span data-ttu-id="1acd9-153">Заблокировано</span><span class="sxs-lookup"><span data-stu-id="1acd9-153">Locked</span></span>**  
<span data-ttu-id="1acd9-154">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1acd9-154">Data type: **Boolean**</span></span>

<span data-ttu-id="1acd9-155">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="1acd9-155">Access type: Read-only</span></span>

<span data-ttu-id="1acd9-156">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="1acd9-156">Qualifiers: None</span></span>

<span data-ttu-id="1acd9-157">**значение true** , если виртуальный пакет заблокирован; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1acd9-157">**true** if the virtual package is locked; otherwise **false**.</span></span>

<a href="" id="cachedpercentage"></a>**<span data-ttu-id="1acd9-158">CachedPercentage</span><span class="sxs-lookup"><span data-stu-id="1acd9-158">CachedPercentage</span></span>**  
<span data-ttu-id="1acd9-159">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1acd9-159">Data type: **UInt16**</span></span>

<span data-ttu-id="1acd9-160">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="1acd9-160">Access type: Read-only</span></span>

<span data-ttu-id="1acd9-161">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="1acd9-161">Qualifiers: None</span></span>

<span data-ttu-id="1acd9-162">Процент файлов кэша.</span><span class="sxs-lookup"><span data-stu-id="1acd9-162">The percentage of the cache files.</span></span> <span data-ttu-id="1acd9-163">В соответствии с приведенной ниже формулой: CachedSize/TotalSize × 100.</span><span class="sxs-lookup"><span data-stu-id="1acd9-163">Based on the following formula: CachedSize / TotalSize × 100.</span></span>

<a href="" id="versionguid"></a>**<span data-ttu-id="1acd9-164">VersionGUID</span><span class="sxs-lookup"><span data-stu-id="1acd9-164">VersionGUID</span></span>**  
<span data-ttu-id="1acd9-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1acd9-165">Data type: **String**</span></span>

<span data-ttu-id="1acd9-166">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="1acd9-166">Access type: Read-only</span></span>

<span data-ttu-id="1acd9-167">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="1acd9-167">Qualifiers: None</span></span>

<span data-ttu-id="1acd9-168">Идентификатор GUID версии пакета.</span><span class="sxs-lookup"><span data-stu-id="1acd9-168">The GUID identifier of the package version.</span></span>

 

 





