---
title: Класс WMI приложения App-V
description: Класс WMI приложения App-V
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822322"
---
# <span data-ttu-id="80ce1-103">Класс WMI приложения App-V</span><span class="sxs-lookup"><span data-stu-id="80ce1-103">App-V Application WMI Class</span></span>


<span data-ttu-id="80ce1-104">В клиенте Application Virtualization (App-V) класс **Application** является классом инструментария управления Windows (WMI), который представляет все виртуальные приложения на клиенте.</span><span class="sxs-lookup"><span data-stu-id="80ce1-104">In the Application Virtualization (App-V) Client, the **Application** class is a Windows Management Instrumentation (WMI) class that represents all the virtual applications on the client.</span></span>

<span data-ttu-id="80ce1-105">Следующий синтаксис упрощен из кода MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="80ce1-105">The following syntax is simplified from Managed Object Format (MOF) code.</span></span> <span data-ttu-id="80ce1-106">Код включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="80ce1-106">The code includes all the inherited properties.</span></span>

## <span data-ttu-id="80ce1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80ce1-107">Syntax</span></span>


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## <span data-ttu-id="80ce1-108">Требования</span><span class="sxs-lookup"><span data-stu-id="80ce1-108">Requirements</span></span>


## <span data-ttu-id="80ce1-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="80ce1-109">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="80ce1-110">Имя</span><span class="sxs-lookup"><span data-stu-id="80ce1-110">Name</span></span>**  
<span data-ttu-id="80ce1-111">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80ce1-111">Data type: **String**</span></span>

<span data-ttu-id="80ce1-112">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="80ce1-112">Access type: Read-only</span></span>

<span data-ttu-id="80ce1-113">Квалификаторы: Key</span><span class="sxs-lookup"><span data-stu-id="80ce1-113">Qualifiers: Key</span></span>

<span data-ttu-id="80ce1-114">Отображаемое имя виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="80ce1-114">The display name of the virtual application.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="80ce1-115">Версия</span><span class="sxs-lookup"><span data-stu-id="80ce1-115">Version</span></span>**  
<span data-ttu-id="80ce1-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80ce1-116">Data type: **String**</span></span>

<span data-ttu-id="80ce1-117">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="80ce1-117">Access type: Read-only</span></span>

<span data-ttu-id="80ce1-118">Квалификаторы: Key</span><span class="sxs-lookup"><span data-stu-id="80ce1-118">Qualifiers: Key</span></span>

<span data-ttu-id="80ce1-119">Версия виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="80ce1-119">The version of the virtual application.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="80ce1-120">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="80ce1-120">PackageGUID</span></span>**  
<span data-ttu-id="80ce1-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80ce1-121">Data type: **String**</span></span>

<span data-ttu-id="80ce1-122">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="80ce1-122">Access type: Read-only</span></span>

<span data-ttu-id="80ce1-123">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="80ce1-123">Qualifiers: None</span></span>

<span data-ttu-id="80ce1-124">Идентификатор GUID пакета, с которым связано виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="80ce1-124">The GUID of the package that the virtual application is associated with.</span></span>

<a href="" id="lastlaunchonsystem"></a>**<span data-ttu-id="80ce1-125">LastLaunchOnSystem</span><span class="sxs-lookup"><span data-stu-id="80ce1-125">LastLaunchOnSystem</span></span>**  
<span data-ttu-id="80ce1-126">Тип данных: **Дата и время**</span><span class="sxs-lookup"><span data-stu-id="80ce1-126">Data type: **DateTime**</span></span>

<span data-ttu-id="80ce1-127">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="80ce1-127">Access type: Read-only</span></span>

<span data-ttu-id="80ce1-128">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="80ce1-128">Qualifiers: None</span></span>

<span data-ttu-id="80ce1-129">Дата и время последнего запуска виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="80ce1-129">The last date and time that the virtual application was launched.</span></span>

<a href="" id="globalrunningcount"></a>**<span data-ttu-id="80ce1-130">GlobalRunningCount</span><span class="sxs-lookup"><span data-stu-id="80ce1-130">GlobalRunningCount</span></span>**  
<span data-ttu-id="80ce1-131">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80ce1-131">Data type: **UInt32**</span></span>

<span data-ttu-id="80ce1-132">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="80ce1-132">Access type: Read-only</span></span>

<span data-ttu-id="80ce1-133">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="80ce1-133">Qualifiers: None</span></span>

<span data-ttu-id="80ce1-134">Количество работающих экземпляров виртуального приложения, которые были запущены напрямую.</span><span class="sxs-lookup"><span data-stu-id="80ce1-134">A count of the running instances of the virtual application that were started directly.</span></span>

<a href="" id="loading"></a>**<span data-ttu-id="80ce1-135">Загрузка</span><span class="sxs-lookup"><span data-stu-id="80ce1-135">Loading</span></span>**  
<span data-ttu-id="80ce1-136">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="80ce1-136">Data type: **Boolean**</span></span>

<span data-ttu-id="80ce1-137">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="80ce1-137">Access type: Read-only</span></span>

<span data-ttu-id="80ce1-138">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="80ce1-138">Qualifiers: None</span></span>

<span data-ttu-id="80ce1-139">**значение true** , если виртуальное приложение запускается; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="80ce1-139">**true** if the virtual application is being started; otherwise **false**.</span></span>

<a href="" id="originalosdpath"></a>**<span data-ttu-id="80ce1-140">OriginalOsdPath</span><span class="sxs-lookup"><span data-stu-id="80ce1-140">OriginalOsdPath</span></span>**  
<span data-ttu-id="80ce1-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80ce1-141">Data type: **String**</span></span>

<span data-ttu-id="80ce1-142">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="80ce1-142">Access type: Read-only</span></span>

<span data-ttu-id="80ce1-143">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="80ce1-143">Qualifiers: None</span></span>

<span data-ttu-id="80ce1-144">Исходный путь файла OSD, зарегистрированного в клиенте App-V.</span><span class="sxs-lookup"><span data-stu-id="80ce1-144">The original file path of the OSD file that was registered with the App-V Client.</span></span>

<a href="" id="cachedosdpath"></a>**<span data-ttu-id="80ce1-145">CachedOsdPath</span><span class="sxs-lookup"><span data-stu-id="80ce1-145">CachedOsdPath</span></span>**  
<span data-ttu-id="80ce1-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80ce1-146">Data type: **String**</span></span>

<span data-ttu-id="80ce1-147">Тип доступа "только для чтения"</span><span class="sxs-lookup"><span data-stu-id="80ce1-147">Access type: Read-only</span></span>

<span data-ttu-id="80ce1-148">Квалификаторы: None</span><span class="sxs-lookup"><span data-stu-id="80ce1-148">Qualifiers: None</span></span>

<span data-ttu-id="80ce1-149">Путь к файлу OSD, если клиент App-V кэширует файл OSD локально.</span><span class="sxs-lookup"><span data-stu-id="80ce1-149">The file path of the OSD file if the App-V Client has cached the OSD file locally.</span></span>

 

 





