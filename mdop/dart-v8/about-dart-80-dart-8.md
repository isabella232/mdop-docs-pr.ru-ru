---
title: Сведения о DaRT 8.0
description: Сведения о DaRT 8.0
author: dansimp
ms.assetid: ce91efd6-7d78-44cb-bb8f-1f43f768ebaa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e70816425dc4775b11596b91d7b5c0045830c6ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821282"
---
# <span data-ttu-id="37a5b-103">Сведения о DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="37a5b-103">About DaRT 8.0</span></span>


<span data-ttu-id="37a5b-104">Набор средств диагностики и восстановления Microsoft (DaRT) 8,0 поможет вам устранить неполадки и восстановить компьютеры под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="37a5b-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 helps you troubleshoot and repair Windows-based computers.</span></span> <span data-ttu-id="37a5b-105">Сюда входят компьютеры, которые не могут быть запущены.</span><span class="sxs-lookup"><span data-stu-id="37a5b-105">This includes those computers that cannot be started.</span></span> <span data-ttu-id="37a5b-106">DaRT 8,0 — это мощный набор инструментов, расширяющий среду восстановления Windows (WinRE).</span><span class="sxs-lookup"><span data-stu-id="37a5b-106">DaRT 8.0 is a powerful set of tools that extend the Windows Recovery Environment (WinRE).</span></span> <span data-ttu-id="37a5b-107">С помощью DaRT вы можете проанализировать проблемы, чтобы определить ее причину, например, проверив журнал событий компьютера или системный реестр.</span><span class="sxs-lookup"><span data-stu-id="37a5b-107">By using DaRT, you can analyze an issue to determine its cause, for example, by inspecting the computer’s event log or system registry.</span></span> <span data-ttu-id="37a5b-108">DaRT поддерживает восстановление основных жестких дисков, содержащих разделы, например основные разделы и логические диски, и поддерживает восстановление томов.</span><span class="sxs-lookup"><span data-stu-id="37a5b-108">DaRT supports the recovery of basic hard disks that contain partitions, for example, primary partitions and logical drives, and supports the recovery of volumes.</span></span>

<span data-ttu-id="37a5b-109">**Примечание**  DaRT не поддерживает восстановление динамических дисков.</span><span class="sxs-lookup"><span data-stu-id="37a5b-109">**Note** DaRT does not support the recovery of dynamic disks.</span></span>

 

<span data-ttu-id="37a5b-110">DaRT также содержит инструменты, которые помогут вам устранить проблему, как только вы определите ее причину.</span><span class="sxs-lookup"><span data-stu-id="37a5b-110">DaRT also provides tools to help you fix a problem as soon as you determine the cause.</span></span> <span data-ttu-id="37a5b-111">Например, с помощью средств DaRT вы можете отключить неисправный драйвер устройства, удалить исправления, восстановить удаленные файлы и проверить компьютер на наличие вредоносных программ, даже если вы не можете запускать установленную операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="37a5b-111">For example, you can use the tools in DaRT to disable a faulty device driver, remove hotfixes, restore deleted files, and scan the computer for malware even when you cannot or should not start the installed Windows operating system.</span></span>

<span data-ttu-id="37a5b-112">DaRT помогает быстро восстанавливать компьютеры под управлением Windows 8 64 или более чем с 32-разрядных версий, обычно за меньшее время, чем при переобразе компьютера.</span><span class="sxs-lookup"><span data-stu-id="37a5b-112">DaRT can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 8, typically in less time than it would take to reimage the computer.</span></span>

<span data-ttu-id="37a5b-113">Функция DaRT позволяет создавать образы для восстановления.</span><span class="sxs-lookup"><span data-stu-id="37a5b-113">Functionality in DaRT lets you create a recovery image.</span></span> <span data-ttu-id="37a5b-114">Образ восстановления запускает среду восстановления Windows (Windows RE), из которой можно запустить окно **инструментария диагностики и восстановления** и получить доступ к средствам DART.</span><span class="sxs-lookup"><span data-stu-id="37a5b-114">The recovery image starts Windows Recovery Environment (Windows RE), from which you can start the **Diagnostics and Recovery Toolset** window and access the DaRT tools.</span></span>

<span data-ttu-id="37a5b-115">С помощью **мастера изображений для восстановления** DART вы можете создать изображение для восстановления стрелок.</span><span class="sxs-lookup"><span data-stu-id="37a5b-115">Use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span> <span data-ttu-id="37a5b-116">По умолчанию мастер создает файл изображения Международной организации по стандартизации (ISO) и файл Windows Imaging Format (WIM), а также позволяет записать изображение на компакт-диск, DVD-диск или USB-порт.</span><span class="sxs-lookup"><span data-stu-id="37a5b-116">By default, the wizard creates an International Organization for Standardization (ISO) image file and a Windows Imaging Format (WIM) file and let you burn the image to a CD, DVD, or USB.</span></span> <span data-ttu-id="37a5b-117">Вы можете развертывать изображение локально на компьютерах конечных пользователей, а также развертывать его из удаленного сетевого раздела или раздела восстановления на локальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="37a5b-117">You can deploy the image locally at end user’s computers, or you can deploy it from a remote network partition or a recovery partition on the local hard drive.</span></span>

## <a href="" id="what-s-new-in-dart-8-0"></a><span data-ttu-id="37a5b-118">Новые возможности DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="37a5b-118">What’s new in DaRT 8.0</span></span>


<span data-ttu-id="37a5b-119">DaRT 8,0 поможет быстро восстановить компьютеры, на которых запущены 32-или 64-разрядные версии Windows 8, обычно за меньшее время, чем потребуется для переустановки образа компьютера.</span><span class="sxs-lookup"><span data-stu-id="37a5b-119">DaRT 8.0 can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 8, typically in less time than it would take to reimage the computer.</span></span> <span data-ttu-id="37a5b-120">На DaRT 8,0 описаны новые возможности.</span><span class="sxs-lookup"><span data-stu-id="37a5b-120">DaRT 8.0 has the following new features.</span></span>

### <span data-ttu-id="37a5b-121">Создание изображений для DaRT с помощью Windows 8 или Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37a5b-121">Create DaRT images by using Windows 8 or Windows Server 2012</span></span>

<span data-ttu-id="37a5b-122">DaRT 8,0 позволяет создавать изображения DaRT с помощью Windows® 8 или Windows Server® 2012.</span><span class="sxs-lookup"><span data-stu-id="37a5b-122">DaRT 8.0 enables you to create DaRT images using either Windows® 8 or Windows Server® 2012.</span></span> <span data-ttu-id="37a5b-123">Для более ранних версий Windows, чем Windows 8 и Windows Server 2012, пользователи должны продолжать использовать более ранние версии DaRT.</span><span class="sxs-lookup"><span data-stu-id="37a5b-123">For versions of Windows earlier than Windows 8 and Windows Server 2012, customers should continue to use earlier versions of DaRT.</span></span>

### <span data-ttu-id="37a5b-124">Создание как 32, так и 64-разрядных изображений с одного компьютера</span><span class="sxs-lookup"><span data-stu-id="37a5b-124">Generate both 32- and 64-bit images from one computer</span></span>

<span data-ttu-id="37a5b-125">DaRT 8,0 позволяет создавать как 32-, так и 64-разрядные изображения с одного компьютера, на котором работает DaRT, независимо от того, является ли компьютер 32-битным или 64-битным компьютером.</span><span class="sxs-lookup"><span data-stu-id="37a5b-125">DaRT 8.0 enables you to generate both 32-bit and 64-bit images from a single computer that is running DaRT, regardless of whether the computer is a 32-bit or 64-bit computer.</span></span> <span data-ttu-id="37a5b-126">В DaRT7 изображение, которое было создано, должно быть одинаковым и побитовым для компьютера, на котором выполнялась DaRT.</span><span class="sxs-lookup"><span data-stu-id="37a5b-126">In DaRT7, the image that was created had to be the same, bit-wise, as the computer that was running DaRT.</span></span>

### <span data-ttu-id="37a5b-127">Создание одного изображения, поддерживающего компьютеры с интерфейсом BIOS или UEFI</span><span class="sxs-lookup"><span data-stu-id="37a5b-127">Create one image that supports computers that have either a BIOS or UEFI interface</span></span>

<span data-ttu-id="37a5b-128">DaRT 8.0 поддержка интерфейса UEFI и интерфейсов BIOS позволяет создавать только одно изображение, которое работает на компьютерах с любыми интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="37a5b-128">DaRT 8.0’s support for both the Unified Extensible Firmware Interface (UEFI) and BIOS interfaces enables you to create just one image that works with computers that have either interface.</span></span>

### <span data-ttu-id="37a5b-129">Использование таблицы разделов GUID для секционирования</span><span class="sxs-lookup"><span data-stu-id="37a5b-129">Use a GUID partition table (GPT) for partitioning</span></span>

<span data-ttu-id="37a5b-130">Инструменты DaRT 8,0 теперь поддерживают GPT-диски Windows 8, которые предоставляют более гибкий механизм разделения дисков, чем устаревшая схема секционирования основной загрузочной записи (MBR).</span><span class="sxs-lookup"><span data-stu-id="37a5b-130">DaRT 8.0 tools now support Windows 8 GPT disks, which provide a more flexible mechanism for partitioning disks than the older master boot record (MBR) partitioning scheme.</span></span> <span data-ttu-id="37a5b-131">Инструменты DaRT 8,0 продолжат поддерживать разделение MBR.</span><span class="sxs-lookup"><span data-stu-id="37a5b-131">DaRT 8.0 tools continue to support MBR partitioning.</span></span>

### <span data-ttu-id="37a5b-132">Установка Windows 8 и Windows Server 2012 на локальном жестком диске</span><span class="sxs-lookup"><span data-stu-id="37a5b-132">Install Windows 8 and Windows Server 2012 on the local hard disk</span></span>

<span data-ttu-id="37a5b-133">Инструменты DaRT 8,0 можно использовать только в том случае, если Windows 8 и Windows Server 2012 установлены на локальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="37a5b-133">DaRT 8.0 tools can be used only when Windows 8 and Windows Server 2012 are installed on the local hard disk.</span></span> <span data-ttu-id="37a5b-134">В настоящее время нет поддержки Windows to go.</span><span class="sxs-lookup"><span data-stu-id="37a5b-134">Currently, there is no support for Windows To Go.</span></span>

### <a href="" id="-------------dart-8-0-release-notes"></a> <span data-ttu-id="37a5b-135">DaRT 8,0 заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="37a5b-135">DaRT 8.0 release notes</span></span>

<span data-ttu-id="37a5b-136">Чтобы получить дополнительные сведения и последние новости, которые не были внесены в документацию, ознакомьтесь с [заметками о выпуске DaRT 8,0](release-notes-for-dart-80--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="37a5b-136">For more information, and for late-breaking news that did not make it into the documentation, see the [Release Notes for DaRT 8.0](release-notes-for-dart-80--dart-8.md).</span></span>

## <span data-ttu-id="37a5b-137">Как получить DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="37a5b-137">How to Get DaRT 8.0</span></span>


<span data-ttu-id="37a5b-138">Эта технология является частью пакета оптимизации рабочего стола Майкрософт (MDOP).</span><span class="sxs-lookup"><span data-stu-id="37a5b-138">This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="37a5b-139">MDOP входит в состав Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="37a5b-139">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="37a5b-140">Дополнительные сведения о программе Software Assurance и приобретении MDOP можно найти в [статьях получение MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="37a5b-140">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="37a5b-141">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="37a5b-141">Related topics</span></span>


[<span data-ttu-id="37a5b-142">Начало работы с DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="37a5b-142">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

[<span data-ttu-id="37a5b-143">Заметки о выпуске для DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="37a5b-143">Release Notes for DaRT 8.0</span></span>](release-notes-for-dart-80--dart-8.md)

 

 





