---
title: Заметки о выпуске для DaRT 8.0 с пакетом обновления 1 (SP1)
description: Заметки о выпуске для DaRT 8.0 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: fa7512d8-fb00-4c27-8f65-c15f3a8ff1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a4c49d12fed07f507d2db4d56969d8e7b0559c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824772"
---
# <span data-ttu-id="92618-103">Заметки о выпуске для DaRT 8.0 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="92618-103">Release Notes for DaRT 8.0 SP1</span></span>


**<span data-ttu-id="92618-104">Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="92618-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="92618-105">Внимательно прочитайте эти заметки о выпуске, прежде чем устанавливать набор средств диагностики и восстановления Microsoft (DaRT) 8,0 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="92618-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Service Pack 1 (SP1).</span></span>

<span data-ttu-id="92618-106">Эти заметки о выпуске содержат сведения, необходимые для успешной установки средств диагностики и восстановления с пакетом обновления 1 (SP1) 8,0.</span><span class="sxs-lookup"><span data-stu-id="92618-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 8.0 SP1.</span></span> <span data-ttu-id="92618-107">Заметки о выпуске также содержат сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="92618-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="92618-108">Если между этими заметками о выпуске и документацией для DaRT имеется разница, Последнее изменение должно считаться полномочным.</span><span class="sxs-lookup"><span data-stu-id="92618-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="92618-109">Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.</span><span class="sxs-lookup"><span data-stu-id="92618-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="92618-110">Сведения о документации по продукту</span><span class="sxs-lookup"><span data-stu-id="92618-110">About the product documentation</span></span>


<span data-ttu-id="92618-111">Сведения о документации по DaRT можно найти на [домашней странице DART](https://go.microsoft.com/fwlink/?LinkID=252096) в Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="92618-111">For information about documentation for DaRT, see the [DaRT home page](https://go.microsoft.com/fwlink/?LinkID=252096) on Microsoft TechNet.</span></span>

## <span data-ttu-id="92618-112">Известные проблемы, возникающие при использовании DaRT 8,0 SP1</span><span class="sxs-lookup"><span data-stu-id="92618-112">Known issues with DaRT 8.0 SP1</span></span>


### <span data-ttu-id="92618-113">При запуске Locksmith или редактора реестра происходит сбой восстановления системы</span><span class="sxs-lookup"><span data-stu-id="92618-113">System restore fails when you run Locksmith or Registry Editor</span></span>

<span data-ttu-id="92618-114">Если вы запускаете Locksmith, редактор реестра и другие инструменты, восстановление системы завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="92618-114">If you run Locksmith, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="92618-115">**Временное решение:** Закройте и перезапустите DaRT, а затем запустите восстановление системы.</span><span class="sxs-lookup"><span data-stu-id="92618-115">**Workaround:** Close and restart DaRT and then start System Restore.</span></span>

### <span data-ttu-id="92618-116">После запуска и закрытия Locksmith или управления компьютером не запускается проверка SFC</span><span class="sxs-lookup"><span data-stu-id="92618-116">SFC scan fails to run after you launch and close Locksmith or Computer Management</span></span>

<span data-ttu-id="92618-117">Если запустить и закрыть средства управления Locksmith или компьютером, не удается запустить средство проверки системных файлов.</span><span class="sxs-lookup"><span data-stu-id="92618-117">If you start and then close the Locksmith or Computer Management tools, System File Checker fails to run.</span></span>

<span data-ttu-id="92618-118">**Временное решение:** Закройте и перезапустите DaRT, а затем запустите SFC.</span><span class="sxs-lookup"><span data-stu-id="92618-118">**Workaround:** Close and restart DaRT and then start SFC.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> <span data-ttu-id="92618-119">Установщик DaRT не завершается сбоем, если не установлен ADK</span><span class="sxs-lookup"><span data-stu-id="92618-119">DaRT installer does not fail when ADK has not been installed</span></span>

<span data-ttu-id="92618-120">Если вы установили DaRT 8,0 SP1, используя командную строку для запуска MSI, а ADK не установлен, установка DaRT завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="92618-120">If you install DaRT 8.0 SP1 by using the command line to run the MSI, and the ADK has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="92618-121">В настоящее время установщик DaRT 8,0 SP1 устанавливает все компоненты, кроме изображения для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="92618-121">Currently, the DaRT 8.0 SP1 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="92618-122">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="92618-122">**Workaround:** None.</span></span>

### <span data-ttu-id="92618-123">Не удается запустить защитник после запуска Locksmith, Regedit, Crash Analyzer и управления компьютером</span><span class="sxs-lookup"><span data-stu-id="92618-123">Defender cannot be launched after Locksmith, RegEdit, Crash Analyzer, and Computer Management are launched</span></span>

<span data-ttu-id="92618-124">Если вы уже запустили Locksmith, Regedit, Crash Analyzer и Управление компьютером, защитник не запускается.</span><span class="sxs-lookup"><span data-stu-id="92618-124">Defender does not launch if you have already launched Locksmith, RegEdit, Crash Analyzer, and Computer Management.</span></span>

<span data-ttu-id="92618-125">**Временное решение:** Закройте и перезапустите DaRT, а затем запустите защитник.</span><span class="sxs-lookup"><span data-stu-id="92618-125">**Workaround:** Close and restart DaRT and then launch Defender.</span></span>

### <span data-ttu-id="92618-126">Защитник может замедленно запускаться</span><span class="sxs-lookup"><span data-stu-id="92618-126">Defender may be slow to launch</span></span>

<span data-ttu-id="92618-127">Иногда для запуска защитника потребуется несколько минут.</span><span class="sxs-lookup"><span data-stu-id="92618-127">Defender sometimes takes a few minutes to launch.</span></span> <span data-ttu-id="92618-128">Индикатор выполнения показывает текущее состояние загрузки.</span><span class="sxs-lookup"><span data-stu-id="92618-128">The progress bar indicates the current loading status.</span></span>

<span data-ttu-id="92618-129">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="92618-129">**Workaround:** None.</span></span>

## <span data-ttu-id="92618-130">Сведения о заметках об авторском праве</span><span class="sxs-lookup"><span data-stu-id="92618-130">Release notes copyright information</span></span>


<span data-ttu-id="92618-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune и WindowsPowerShell являются товарными знаками группы компании Microsoft.</span><span class="sxs-lookup"><span data-stu-id="92618-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="92618-132">Все прочие товарные знаки являются собственностью соответствующих владельцев.</span><span class="sxs-lookup"><span data-stu-id="92618-132">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="92618-133">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="92618-133">Related topics</span></span>


[<span data-ttu-id="92618-134">Сведения о DaRT 8.0 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="92618-134">About DaRT 8.0 SP1</span></span>](about-dart-80-sp1.md)

 

 





