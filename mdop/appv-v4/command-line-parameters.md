---
title: Параметры командной строки
description: Параметры командной строки
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819402"
---
# <span data-ttu-id="478cd-103">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="478cd-103">Command-Line Parameters</span></span>


<span data-ttu-id="478cd-104">Используйте следующие параметры Sequencer Application Virtualization для последовательного приложения и для обновления серийного пакета приложения в командной строке.</span><span class="sxs-lookup"><span data-stu-id="478cd-104">Use the following Application Virtualization Sequencer parameters to sequence an application and to upgrade a sequenced application package at the command prompt.</span></span> <span data-ttu-id="478cd-105">В каталоге Microsoft Application Virtualization Sequencer введите **SFTSequencer**, а затем соответствующий параметр.</span><span class="sxs-lookup"><span data-stu-id="478cd-105">In the Microsoft Application Virtualization Sequencer directory, you would enter **SFTSequencer**, followed by the appropriate parameter.</span></span>

<a href="" id="-help-or---"></a><span data-ttu-id="478cd-106">*/Help* или */?*</span><span class="sxs-lookup"><span data-stu-id="478cd-106">*/HELP* or */?*</span></span>  
<span data-ttu-id="478cd-107">Используется для отображения списка параметров, доступных для последовательностей командной строки.</span><span class="sxs-lookup"><span data-stu-id="478cd-107">Use to display the list of parameters available for command-line sequencing.</span></span>

<a href="" id="-installpackage-or--i"></a><span data-ttu-id="478cd-108">*/INSTALLPACKAGE* или */i*</span><span class="sxs-lookup"><span data-stu-id="478cd-108">*/INSTALLPACKAGE* or */I*</span></span>  
<span data-ttu-id="478cd-109">Используется для указания установщика или пакетного файла для упорядочения приложения.</span><span class="sxs-lookup"><span data-stu-id="478cd-109">Use to specify the installer or a batch file for the application to be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a><span data-ttu-id="478cd-110">*/INSTALLPATH* или */p*</span><span class="sxs-lookup"><span data-stu-id="478cd-110">*/INSTALLPATH* or */P*</span></span>  
<span data-ttu-id="478cd-111">Используется для указания корневого каталога пакета.</span><span class="sxs-lookup"><span data-stu-id="478cd-111">Use to specify the package root directory.</span></span>

<a href="" id="-outputfile-or--o"></a><span data-ttu-id="478cd-112">*/OutputFile* или */o*</span><span class="sxs-lookup"><span data-stu-id="478cd-112">*/OUTPUTFILE* or */O*</span></span>  
<span data-ttu-id="478cd-113">Позволяет указать путь и имя файла SPRJ, который будет создан.</span><span class="sxs-lookup"><span data-stu-id="478cd-113">Use to specify the path and file name of the SPRJ file that will be generated.</span></span>

<span data-ttu-id="478cd-114">**Важно!**  Параметр */OutputFile* недоступен при открытии пакета, который вы не планируете обновлять.</span><span class="sxs-lookup"><span data-stu-id="478cd-114">**Important** The */OUTPUTFILE* parameter is not available when opening a package that you do not intend to upgrade.</span></span>

 

<a href="" id="-fullload-or--f"></a><span data-ttu-id="478cd-115">*/FULLLOAD* или */f*</span><span class="sxs-lookup"><span data-stu-id="478cd-115">*/FULLLOAD* or */F*</span></span>  
<span data-ttu-id="478cd-116">Используется, чтобы указать, нужно ли размещать все в основном блоке функций.</span><span class="sxs-lookup"><span data-stu-id="478cd-116">Use to specify whether to put everything in the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a><span data-ttu-id="478cd-117">*/PACKAGENAME* или */k*</span><span class="sxs-lookup"><span data-stu-id="478cd-117">*/PACKAGENAME* or */K*</span></span>  
<span data-ttu-id="478cd-118">Используется для указания имени пакета для упорядоченного приложения.</span><span class="sxs-lookup"><span data-stu-id="478cd-118">Use to specify the package name of the sequenced application.</span></span>

<a href="" id="-blocksize"></a>*<span data-ttu-id="478cd-119">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="478cd-119">/BLOCKSIZE</span></span>*  
<span data-ttu-id="478cd-120">Указывает размер блока SFT файла, который будет использоваться для потоковой передачи пакета на клиентские компьютеры.</span><span class="sxs-lookup"><span data-stu-id="478cd-120">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="478cd-121">Вы можете выбрать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="478cd-121">You can select one of the following values:</span></span>

-   <span data-ttu-id="478cd-122">4 КБ</span><span class="sxs-lookup"><span data-stu-id="478cd-122">4 KB</span></span>

-   <span data-ttu-id="478cd-123">16 КБ</span><span class="sxs-lookup"><span data-stu-id="478cd-123">16 KB</span></span>

-   <span data-ttu-id="478cd-124">32 КБ</span><span class="sxs-lookup"><span data-stu-id="478cd-124">32 KB</span></span>

-   <span data-ttu-id="478cd-125">64 КБ</span><span class="sxs-lookup"><span data-stu-id="478cd-125">64 KB</span></span>

<span data-ttu-id="478cd-126">При указании размера блока вы должны оценить размер SFT – файла.</span><span class="sxs-lookup"><span data-stu-id="478cd-126">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="478cd-127">Файл с меньшим размером блока занимает больше времени для потоковой передачи по сети, но менее интенсивно использует пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="478cd-127">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="478cd-128">Файлы с более крупными размерами блоков используют дополнительную пропускную способность сети.</span><span class="sxs-lookup"><span data-stu-id="478cd-128">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>*<span data-ttu-id="478cd-129">/COMPRESSION</span><span class="sxs-lookup"><span data-stu-id="478cd-129">/COMPRESSION</span></span>*  
<span data-ttu-id="478cd-130">Используется для указания метода сжатия SFT файла в процессе его потоковой передачи клиенту.</span><span class="sxs-lookup"><span data-stu-id="478cd-130">Use to specify the method for compressing the SFT file as it is streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a><span data-ttu-id="478cd-131">*/MSI* или */m*</span><span class="sxs-lookup"><span data-stu-id="478cd-131">*/MSI* or */M*</span></span>  
<span data-ttu-id="478cd-132">Используется для указания создания пакета установщика Microsoft Windows для упорядоченного приложения.</span><span class="sxs-lookup"><span data-stu-id="478cd-132">Use to specify generating a Microsoft Windows Installer package for the sequenced application.</span></span>

<a href="" id="-default"></a>*<span data-ttu-id="478cd-133">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="478cd-133">/DEFAULT</span></span>*  
<span data-ttu-id="478cd-134">Указывает файл SPRJ по умолчанию, который будет использоваться при создании виртуального пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="478cd-134">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="478cd-135">Этот файл используется в качестве шаблона. SPRJ, когда приложение выполняется в первый раз.</span><span class="sxs-lookup"><span data-stu-id="478cd-135">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>*<span data-ttu-id="478cd-136">/UPGRADE</span><span class="sxs-lookup"><span data-stu-id="478cd-136">/UPGRADE</span></span>*  
<span data-ttu-id="478cd-137">Указывает путь и имя файла SPRJ, который будет обновлен.</span><span class="sxs-lookup"><span data-stu-id="478cd-137">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>*<span data-ttu-id="478cd-138">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="478cd-138">/DECODEPATH</span></span>*  
<span data-ttu-id="478cd-139">Указывает каталог на компьютере виртуализации, на котором установлены файлы, связанные с пакетом упорядоченного приложения.</span><span class="sxs-lookup"><span data-stu-id="478cd-139">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="478cd-140">При указании каталога используйте один из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="478cd-140">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="478cd-141">/DECODEPATH: Q:</span><span class="sxs-lookup"><span data-stu-id="478cd-141">/decodepath:Q:</span></span>

-   <span data-ttu-id="478cd-142">/decodepath:Q:.</span><span class="sxs-lookup"><span data-stu-id="478cd-142">/decodepath:Q:.</span></span>

-   <span data-ttu-id="478cd-143">/decodepath:"Q:."</span><span class="sxs-lookup"><span data-stu-id="478cd-143">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="478cd-144">/DECODEPATH: "Q:"</span><span class="sxs-lookup"><span data-stu-id="478cd-144">/decodepath:”Q:”</span></span>

## <span data-ttu-id="478cd-145">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="478cd-145">Related topics</span></span>


[<span data-ttu-id="478cd-146">Сведения об использовании командной строки программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="478cd-146">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="478cd-147">Открытие виртуализированного приложения с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="478cd-147">How to Open a Sequenced Application Using the Command Line</span></span>](how-to-open-a-sequenced-application-using-the-command-line.md)

[<span data-ttu-id="478cd-148">Обновление пакета с помощью команды "Открыть пакет"</span><span class="sxs-lookup"><span data-stu-id="478cd-148">How to Upgrade a Package Using the Open Package Command</span></span>](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 





