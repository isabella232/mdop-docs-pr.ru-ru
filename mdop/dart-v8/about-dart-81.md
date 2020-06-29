---
title: Сведения о DaRT 8.1
description: Сведения о DaRT 8.1
author: dansimp
ms.assetid: dcaddc57-0111-4a9d-8be9-f5ada0eefa7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 29c7522b4f5a5da3b451b23f2fd200db44bb9481
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821262"
---
# <span data-ttu-id="cd651-103">Сведения о DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="cd651-103">About DaRT 8.1</span></span>


<span data-ttu-id="cd651-104">Набор средств диагностики и восстановления Microsoft (DaRT) 8,1 содержит следующие улучшенные возможности, описанные в этой статье.</span><span class="sxs-lookup"><span data-stu-id="cd651-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.1 provides the following enhancements, which are described in this topic.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="cd651-105">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="cd651-105">What’s new</span></span>


-   **<span data-ttu-id="cd651-106">Поддержка WIMBoot</span><span class="sxs-lookup"><span data-stu-id="cd651-106">Support for WIMBoot</span></span>**

    <span data-ttu-id="cd651-107">Набор средств диагностики и восстановления 8,1 поддерживает среду загрузки файлов изображений Windows (WIMBoot), если выполняются следующие условия:</span><span class="sxs-lookup"><span data-stu-id="cd651-107">Diagnostics and Recovery Toolset 8.1 supports the Windows image file boot (WIMBoot) environment if these conditions are met:</span></span>

    -   <span data-ttu-id="cd651-108">WIMBoot базируется на Windows 8,1 с обновлением 1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="cd651-108">WIMBoot is based on Windows 8.1 Update 1 or later.</span></span>

    -   <span data-ttu-id="cd651-109">Рисунок DaRT 8,1 создан на основе обновления 1 или более поздней версии для Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="cd651-109">The DaRT 8.1 image is built on Windows 8.1 Update 1 or later.</span></span>

    <span data-ttu-id="cd651-110">Дополнительные сведения о WIMBoot можно найти в статье [Обзор загрузки файлов изображений Windows (WIMBoot)](https://go.microsoft.com/fwlink/?LinkId=517536).</span><span class="sxs-lookup"><span data-stu-id="cd651-110">For more information about WIMBoot, see [Windows Image File Boot (WIMBoot) Overview](https://go.microsoft.com/fwlink/?LinkId=517536).</span></span>

-   **<span data-ttu-id="cd651-111">Поддержка Windows Server 2012 R2 и Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="cd651-111">Support for Windows Server 2012 R2 and Windows 8.1</span></span>**

    <span data-ttu-id="cd651-112">Вы можете создавать изображения DaRT с помощью Windows Server 2012 R2 или Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="cd651-112">You can create DaRT images by using Windows Server 2012 R2 or Windows 8.1.</span></span>

    **<span data-ttu-id="cd651-113">Примечание.</span><span class="sxs-lookup"><span data-stu-id="cd651-113">Note</span></span>**  
    <span data-ttu-id="cd651-114">Для более ранних версий операционных систем Windows Server и Windows продолжайте использовать более ранние версии DaRT.</span><span class="sxs-lookup"><span data-stu-id="cd651-114">For earlier versions of the Windows Server and Windows operating systems, continue to use the earlier versions of DaRT.</span></span>



-   **<span data-ttu-id="cd651-115">Отзывы пользователей</span><span class="sxs-lookup"><span data-stu-id="cd651-115">Customer feedback</span></span>**

    <span data-ttu-id="cd651-116">DaRT 8,1 содержит обновления, которые устраняют проблемы, обнаруженные с момента выпуска DaRT 8,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="cd651-116">DaRT 8.1 includes updates that address issues found since the DaRT 8.0 SP1 release.</span></span>

-   **<span data-ttu-id="cd651-117">Защитник Windows</span><span class="sxs-lookup"><span data-stu-id="cd651-117">Windows Defender</span></span>**

    <span data-ttu-id="cd651-118">Защитник Windows в Windows 8,1 содержит улучшенную защиту.</span><span class="sxs-lookup"><span data-stu-id="cd651-118">Windows Defender in Windows 8.1 includes improved protection.</span></span> <span data-ttu-id="cd651-119">Изменения не влияют на использование DaRT с защитником Windows.</span><span class="sxs-lookup"><span data-stu-id="cd651-119">The changes do not impact how you use DaRT with Windows Defender.</span></span>

## <span data-ttu-id="cd651-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cd651-120">Requirements</span></span>


-   **<span data-ttu-id="cd651-121">Комплект средств для разработки и оценки Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="cd651-121">Windows Assessment and Development Kit 8.1</span></span>**

    <span data-ttu-id="cd651-122">Комплект средств для оценки и разработки Windows (ADK) 8,1 является обязательным условием для мастера создания изображений для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="cd651-122">Windows Assessment and Development Kit (ADK) 8.1 is a required prerequisite for the DaRT Recovery Image Wizard.</span></span> <span data-ttu-id="cd651-123">Windows ADK 8,1 включает инструменты развертывания, которые используются для настройки, развертывания и обслуживания образов Windows.</span><span class="sxs-lookup"><span data-stu-id="cd651-123">Windows ADK 8.1 contains deployment tools that are used to customize, deploy, and service Windows images.</span></span> <span data-ttu-id="cd651-124">Она также включает среду предустановки Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="cd651-124">It also contains the Windows Preinstallation Environment (Windows PE).</span></span>

    **<span data-ttu-id="cd651-125">Примечание.</span><span class="sxs-lookup"><span data-stu-id="cd651-125">Note</span></span>**  
    <span data-ttu-id="cd651-126">Windows ADK 8,1 не требуется, если вы устанавливаете только средство просмотра удаленных подключений или аварийный анализ.</span><span class="sxs-lookup"><span data-stu-id="cd651-126">Windows ADK 8.1 is not required if you are installing only Remote Connection Viewer or Crash Analyzer.</span></span>



~~~
To download Windows ADK 8.1, see [Windows Assessment and Deployment Kit (Windows ADK) for Windows 8.1](https://www.microsoft.com/download/details.aspx?id=39982) in the Microsoft Download Center.
~~~

-   **<span data-ttu-id="cd651-127">Microsoft .NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="cd651-127">Microsoft .NET Framework 4.5.1</span></span>**

    <span data-ttu-id="cd651-128">Для DaRT 8,1 требуется установка .NET Framework 4.5.1.</span><span class="sxs-lookup"><span data-stu-id="cd651-128">DaRT 8.1 requires that .NET Framework 4.5.1 is installed.</span></span> <span data-ttu-id="cd651-129">Для загрузки ознакомьтесь с [разMicrosoft.NET Framework 4.5.1](https://go.microsoft.com/fwlink/?LinkId=329038) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="cd651-129">To download, see [Microsoft.NET Framework 4.5.1](https://go.microsoft.com/fwlink/?LinkId=329038) in the Microsoft Download Center.</span></span>

-   **<span data-ttu-id="cd651-130">Средства отладки Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="cd651-130">Windows 8.1 Debugging Tools</span></span>**

    <span data-ttu-id="cd651-131">Чтобы воспользоваться анализатором аварийного анализа для DaRT 8,1, вам понадобятся необходимые инструменты для отладки, доступные в пакете средств разработки программного обеспечения для Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="cd651-131">To use the Crash Analyzer tool in DaRT 8.1, you need the required debugging tools, which are available in the Software Development Kit for Windows 8.1.</span></span>

    <span data-ttu-id="cd651-132">Загрузить пакет [средств разработки программного обеспечения для Windows (SDK) для windows 8,1](https://msdn.microsoft.com/library/windows/desktop/bg162891.aspx) можно в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="cd651-132">To download, see [Windows Software Development Kit (SDK) for Windows 8.1](https://msdn.microsoft.com/library/windows/desktop/bg162891.aspx) in the Microsoft Download Center.</span></span>

## <span data-ttu-id="cd651-133">Доступность языков</span><span class="sxs-lookup"><span data-stu-id="cd651-133">Language availability</span></span>


<span data-ttu-id="cd651-134">DaRT 8,1 доступен на следующих языках:</span><span class="sxs-lookup"><span data-stu-id="cd651-134">DaRT 8.1 is available in the following languages:</span></span>

-   <span data-ttu-id="cd651-135">Английский (США) EN-US</span><span class="sxs-lookup"><span data-stu-id="cd651-135">English (United States) en-US</span></span>

-   <span data-ttu-id="cd651-136">Французский (Франция) fr-FR</span><span class="sxs-lookup"><span data-stu-id="cd651-136">French (France) fr-FR</span></span>

-   <span data-ttu-id="cd651-137">Итальянский (Италия) IT-IT</span><span class="sxs-lookup"><span data-stu-id="cd651-137">Italian (Italy) it-IT</span></span>

-   <span data-ttu-id="cd651-138">Немецкий (Германия) de-DE</span><span class="sxs-lookup"><span data-stu-id="cd651-138">German (Germany) de-DE</span></span>

-   <span data-ttu-id="cd651-139">Испанский, Международная Сортировка (Испания) ES-ES</span><span class="sxs-lookup"><span data-stu-id="cd651-139">Spanish, International Sort (Spain) es-ES</span></span>

-   <span data-ttu-id="cd651-140">Корейский (Корея) ko-KR</span><span class="sxs-lookup"><span data-stu-id="cd651-140">Korean (Korea) ko-KR</span></span>

-   <span data-ttu-id="cd651-141">Японский (Япония) ja-JP</span><span class="sxs-lookup"><span data-stu-id="cd651-141">Japanese (Japan) ja-JP</span></span>

-   <span data-ttu-id="cd651-142">Португальский (Бразилия) Пт — BR</span><span class="sxs-lookup"><span data-stu-id="cd651-142">Portuguese (Brazil) pt-BR</span></span>

-   <span data-ttu-id="cd651-143">Русский (Россия) ru-RU</span><span class="sxs-lookup"><span data-stu-id="cd651-143">Russian (Russia) ru-RU</span></span>

-   <span data-ttu-id="cd651-144">Китайская традиционная zh-TW</span><span class="sxs-lookup"><span data-stu-id="cd651-144">Chinese Traditional zh-TW</span></span>

-   <span data-ttu-id="cd651-145">Китайский (упрощенное письмо) — CN</span><span class="sxs-lookup"><span data-stu-id="cd651-145">Chinese Simplified zh-CN</span></span>

## <span data-ttu-id="cd651-146">Получение технологий для MDOP</span><span class="sxs-lookup"><span data-stu-id="cd651-146">How to Get MDOP Technologies</span></span>


<span data-ttu-id="cd651-147">DaRT 8,1 является частью пакета оптимизации рабочего стола Майкрософт (MDOP).</span><span class="sxs-lookup"><span data-stu-id="cd651-147">DaRT 8.1 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="cd651-148">MDOP входит в состав Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="cd651-148">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="cd651-149">Дополнительные сведения о программе Software Assurance и приобретении MDOP можно найти в [статьях получение MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="cd651-149">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="cd651-150">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="cd651-150">Related topics</span></span>


[<span data-ttu-id="cd651-151">Заметки о выпуске для DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="cd651-151">Release Notes for DaRT 8.1</span></span>](release-notes-for-dart-81.md)









