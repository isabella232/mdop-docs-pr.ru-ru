---
title: Вкладка "Сведения о свойствах"
description: Вкладка "Сведения о свойствах"
author: dansimp
ms.assetid: a6cf6f51-3778-4c8d-9632-3af4005775d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b2d6c3e01dde48fdd6701984f66610ea0333b74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819922"
---
# <span data-ttu-id="eb9de-103">Вкладка "Сведения о свойствах"</span><span class="sxs-lookup"><span data-stu-id="eb9de-103">About the Properties Tab</span></span>


<span data-ttu-id="eb9de-104">Вкладка **Свойства** используется для просмотра основных статистических данных о упорядоченном пакете приложения.</span><span class="sxs-lookup"><span data-stu-id="eb9de-104">Use the **Properties** tab to view basic statistical information about a sequenced application package.</span></span> <span data-ttu-id="eb9de-105">Информация будет автоматически создана, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="eb9de-105">The information is automatically generated unless otherwise noted.</span></span> <span data-ttu-id="eb9de-106">На этой вкладке есть указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="eb9de-106">This tab contains the following elements.</span></span>

## <span data-ttu-id="eb9de-107">Сведения о пакете</span><span class="sxs-lookup"><span data-stu-id="eb9de-107">Package Information</span></span>


<a href="" id="package-name"></a>**<span data-ttu-id="eb9de-108">Имя пакета</span><span class="sxs-lookup"><span data-stu-id="eb9de-108">Package Name</span></span>**  
<span data-ttu-id="eb9de-109">Единственное имя, используемое для пакета упорядоченного приложения, которое может содержать одно или несколько приложений (например, Microsoft Office может использоваться для обозначения последовательного пакета приложения, содержащего Microsoft Word и приложения Microsoft Excel, которые выполняются в той же виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="eb9de-109">The single name used for a sequenced application package that might contain one or more applications—for example, Microsoft Office could be used to label a sequenced application package that contains Microsoft Word and Microsoft Excel applications that run in the same virtual environment.</span></span>

<a href="" id="comments"></a>**<span data-ttu-id="eb9de-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb9de-110">Comments</span></span>**  
<span data-ttu-id="eb9de-111">Отображает краткое описание пакета программного обеспечения, который будет отображаться в элементе ABSTRACT файла Open дескриптора программного обеспечения (OSD).</span><span class="sxs-lookup"><span data-stu-id="eb9de-111">Displays a short description of the software package that will appear in the Open Software Descriptor (OSD) file ABSTRACT element.</span></span> <span data-ttu-id="eb9de-112">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="eb9de-112">This item is optional.</span></span>

<a href="" id="package-version"></a>**<span data-ttu-id="eb9de-113">Версия пакета</span><span class="sxs-lookup"><span data-stu-id="eb9de-113">Package Version</span></span>**  
<span data-ttu-id="eb9de-114">Версия последовательного пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="eb9de-114">The sequenced application package version.</span></span>

<a href="" id="package-guid"></a>**<span data-ttu-id="eb9de-115">GUID пакета</span><span class="sxs-lookup"><span data-stu-id="eb9de-115">Package GUID</span></span>**  
<span data-ttu-id="eb9de-116">Глобальный уникальный идентификатор (GUID) автоматически назначается упорядоченному пакету приложения, чтобы отличать его от других последовательных пакетов приложения, которые могут выполняться на компьютере, на котором поток помещается последовательный пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="eb9de-116">The globally unique identifier (GUID) automatically assigned to the sequenced application package to distinguish it from other sequenced application packages that might be running on the computer to which a sequenced application package is streamed.</span></span>

<a href="" id="package-version-guid"></a>**<span data-ttu-id="eb9de-117">Идентификатор GUID версии пакета</span><span class="sxs-lookup"><span data-stu-id="eb9de-117">Package Version GUID</span></span>**  
<span data-ttu-id="eb9de-118">Идентификатор GUID версии пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="eb9de-118">The sequenced application package version GUID.</span></span>

<a href="" id="root-directory"></a>**<span data-ttu-id="eb9de-119">Корневой каталог</span><span class="sxs-lookup"><span data-stu-id="eb9de-119">Root Directory</span></span>**  
<span data-ttu-id="eb9de-120">Каталог на компьютере виртуализации, на котором установлены файлы для пакета последовательного приложения.</span><span class="sxs-lookup"><span data-stu-id="eb9de-120">The directory on the sequencing computer in which files for the sequenced application package are installed.</span></span> <span data-ttu-id="eb9de-121">Этот каталог также создается на компьютере, на который будет передаваться последовательный пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="eb9de-121">This directory is also created on the computer to which a sequenced application package will be streamed.</span></span> <span data-ttu-id="eb9de-122">Рекомендуется для обеспечения обратной совместимости, что это имя каталога формата 8,3 в корне диска Q, например Q:\\MyApp.1\\.</span><span class="sxs-lookup"><span data-stu-id="eb9de-122">It is recommended for backwards compatibility that this be an 8.3 format directory name at the root of the Q drive, such as Q:\\MyApp.1\\.</span></span>

<a href="" id="created"></a>**<span data-ttu-id="eb9de-123">Созданные</span><span class="sxs-lookup"><span data-stu-id="eb9de-123">Created</span></span>**  
<span data-ttu-id="eb9de-124">Дата и время создания пакета упорядоченного приложения.</span><span class="sxs-lookup"><span data-stu-id="eb9de-124">The date and time the sequenced application package was created.</span></span>

<a href="" id="modified"></a>**<span data-ttu-id="eb9de-125">Изменено</span><span class="sxs-lookup"><span data-stu-id="eb9de-125">Modified</span></span>**  
<span data-ttu-id="eb9de-126">Дата и время последнего изменения упорядоченного пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="eb9de-126">The date and time the sequenced application package was last modified.</span></span>

<a href="" id="package-size"></a>**<span data-ttu-id="eb9de-127">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="eb9de-127">Package Size</span></span>**  
<span data-ttu-id="eb9de-128">Размер пакета (в мегабайтах).</span><span class="sxs-lookup"><span data-stu-id="eb9de-128">The size of the package in megabytes.</span></span>

<a href="" id="launch-size"></a>**<span data-ttu-id="eb9de-129">Размер запуска</span><span class="sxs-lookup"><span data-stu-id="eb9de-129">Launch Size</span></span>**  
<span data-ttu-id="eb9de-130">Размер (в мегабайтах) части файла SFT, необходимого для запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="eb9de-130">The size in megabytes of the portion of the SFT file that is required to start the application.</span></span>

## <span data-ttu-id="eb9de-131">Параметры виртуализации</span><span class="sxs-lookup"><span data-stu-id="eb9de-131">Sequencing Parameters</span></span>


<a href="" id="block-size"></a>**<span data-ttu-id="eb9de-132">Размер блока</span><span class="sxs-lookup"><span data-stu-id="eb9de-132">Block Size</span></span>**  
<span data-ttu-id="eb9de-133">Задает размер основного и дополнительного блоков, в которые делится файл SFT для потоковой передачи по сети.</span><span class="sxs-lookup"><span data-stu-id="eb9de-133">Specifies the size of the primary and secondary feature blocks into which the SFT file is divided for streaming across a network.</span></span> <span data-ttu-id="eb9de-134">Все блоки, размер которых равен указанному значению; Однако последний блок может быть меньше указанного.</span><span class="sxs-lookup"><span data-stu-id="eb9de-134">All blocks equal the specified size; however, the last block might be smaller than specified.</span></span> <span data-ttu-id="eb9de-135">Вы увидите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="eb9de-135">You will see one of the following values:</span></span>

-   <span data-ttu-id="eb9de-136">4 КБ</span><span class="sxs-lookup"><span data-stu-id="eb9de-136">4 KB</span></span>

-   <span data-ttu-id="eb9de-137">16 КБ</span><span class="sxs-lookup"><span data-stu-id="eb9de-137">16 KB</span></span>

-   <span data-ttu-id="eb9de-138">32 КБ</span><span class="sxs-lookup"><span data-stu-id="eb9de-138">32 KB</span></span>

-   <span data-ttu-id="eb9de-139">64 КБ</span><span class="sxs-lookup"><span data-stu-id="eb9de-139">64 KB</span></span>

<span data-ttu-id="eb9de-140">**Примечание**  После создания первоначального пакета значение размера блока не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="eb9de-140">**Note** After the initial package has been created, the block size value is not changeable.</span></span>

 

## <span data-ttu-id="eb9de-141">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="eb9de-141">Related topics</span></span>


[<span data-ttu-id="eb9de-142">Изменение свойств пакета</span><span class="sxs-lookup"><span data-stu-id="eb9de-142">How to Change Package Properties</span></span>](how-to-change-package-properties.md)

[<span data-ttu-id="eb9de-143">Консоль Sequencer</span><span class="sxs-lookup"><span data-stu-id="eb9de-143">Sequencer Console</span></span>](sequencer-console.md)

 

 





