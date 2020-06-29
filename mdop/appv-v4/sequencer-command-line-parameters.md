---
title: Параметры командной строки программы Sequencer
description: Параметры командной строки программы Sequencer
author: dansimp
ms.assetid: 28fb875a-c302-4d95-b2e0-8dc0c5dbb0f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ecfa269de04cf3dcba30cbb4a40f9176f03f6571
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815552"
---
# <span data-ttu-id="4cb7c-103">Параметры командной строки программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="4cb7c-103">Sequencer Command-Line Parameters</span></span>


<span data-ttu-id="4cb7c-104">Вы можете использовать следующие параметры Application Virtualization (App-V) для упорядочения приложения и обновления существующего виртуального приложения с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-104">You can use the following Application Virtualization (App-V) Sequencer parameters to sequence an application and to upgrade an existing virtual application by using a command line.</span></span> <span data-ttu-id="4cb7c-105">Дополнительные сведения о том, как подать заявку на приложение с помощью командной строки, можно найти [в разделе Упорядочение нового приложения с помощью командной строки](how-to-sequence-a-new-application-by-using-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="4cb7c-105">For more information about sequencing an application by using a command line, see [How to Sequence a New Application by Using the Command Line](how-to-sequence-a-new-application-by-using-the-command-line.md).</span></span>

## <span data-ttu-id="4cb7c-106">Параметры командной строки программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="4cb7c-106">Sequencer Command-Line Parameters</span></span>


<a href="" id="-help-or---"></a>**<span data-ttu-id="4cb7c-107">/HELP или/?</span><span class="sxs-lookup"><span data-stu-id="4cb7c-107">/HELP or /?</span></span>**  
<span data-ttu-id="4cb7c-108">Отображает сведения о параметрах, которые можно использовать для последовательности приложений с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-108">Displays information about parameters that are available for using a command line to sequence applications.</span></span>

<a href="" id="-installpackage-or--i"></a>**<span data-ttu-id="4cb7c-109">/INSTALLPACKAGE или/I</span><span class="sxs-lookup"><span data-stu-id="4cb7c-109">/INSTALLPACKAGE or /I</span></span>**  
<span data-ttu-id="4cb7c-110">Указывает установщик Windows или пакетный файл, который будет использоваться для установки приложения, чтобы его можно было последовательно использовать.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-110">Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a>**<span data-ttu-id="4cb7c-111">/INSTALLPATH или/P</span><span class="sxs-lookup"><span data-stu-id="4cb7c-111">/INSTALLPATH or /P</span></span>**  
<span data-ttu-id="4cb7c-112">Указывает корневой каталог пакета для приложения.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-112">Specifies the package root directory for an application.</span></span>

<a href="" id="-outputfile-or--o"></a>**<span data-ttu-id="4cb7c-113">/OUTPUTFILE или/O</span><span class="sxs-lookup"><span data-stu-id="4cb7c-113">/OUTPUTFILE or /O</span></span>**  
<span data-ttu-id="4cb7c-114">Указывает путь и имя файла SPRJ, который будет создан.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-114">Specifies the path and file name of the SPRJ file that will be generated.</span></span>

<a href="" id="-fullload-or--f"></a>**<span data-ttu-id="4cb7c-115">/FULLLOAD или/F</span><span class="sxs-lookup"><span data-stu-id="4cb7c-115">/FULLLOAD or /F</span></span>**  
<span data-ttu-id="4cb7c-116">Указывает, будут ли все файлы содержаться в основном блоке функций.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-116">Specifies whether all files will be contained in the primary feature block.</span></span> <span data-ttu-id="4cb7c-117">Если в командной строке указан параметр **/FULLLOAD** , все связанные данные приложения добавляются в основной блок функций.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-117">If the **/FULLLOAD** parameter is specified on the command line, all of the associated application data is added to primary feature block.</span></span> <span data-ttu-id="4cb7c-118">Если параметр **/FULLLOAD** не указан в командной строке, то ни один из связанных данных приложения не добавляется в основной блок функций.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-118">If the **/FULLLOAD** parameter is not specified on the command line, then none of the associated application data is added to the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a>**<span data-ttu-id="4cb7c-119">/PACKAGENAME или/K</span><span class="sxs-lookup"><span data-stu-id="4cb7c-119">/PACKAGENAME or /K</span></span>**  
<span data-ttu-id="4cb7c-120">Указывает имя пакета, которое будет присвоено упорядоченному приложению.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-120">Specifies the package name that will be assigned to the sequenced application.</span></span>

<a href="" id="-blocksize"></a>**<span data-ttu-id="4cb7c-121">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="4cb7c-121">/BLOCKSIZE</span></span>**  
<span data-ttu-id="4cb7c-122">Указывает размер блока SFT файла, который будет использоваться для потоковой передачи пакета на клиентские компьютеры.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-122">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="4cb7c-123">Вы можете выбрать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4cb7c-123">You can select one of the following values:</span></span>

-   <span data-ttu-id="4cb7c-124">4 КБ</span><span class="sxs-lookup"><span data-stu-id="4cb7c-124">4 KB</span></span>

-   <span data-ttu-id="4cb7c-125">16 КБ</span><span class="sxs-lookup"><span data-stu-id="4cb7c-125">16 KB</span></span>

-   <span data-ttu-id="4cb7c-126">32 КБ</span><span class="sxs-lookup"><span data-stu-id="4cb7c-126">32 KB</span></span>

-   <span data-ttu-id="4cb7c-127">64 КБ</span><span class="sxs-lookup"><span data-stu-id="4cb7c-127">64 KB</span></span>

<span data-ttu-id="4cb7c-128">При указании размера блока вы должны оценить размер SFT – файла.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-128">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="4cb7c-129">Файл с меньшим размером блока занимает больше времени для потоковой передачи по сети, но менее интенсивно использует пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-129">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="4cb7c-130">Файлы с более крупными размерами блоков используют дополнительную пропускную способность сети.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-130">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>**<span data-ttu-id="4cb7c-131">/COMPRESSION</span><span class="sxs-lookup"><span data-stu-id="4cb7c-131">/COMPRESSION</span></span>**  
<span data-ttu-id="4cb7c-132">Задает способ сжатия SFT файла, который будет передаваться клиенту в потоке.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-132">Specifies the method for compressing the SFT file that will be streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a>**<span data-ttu-id="4cb7c-133">/MSI или/M</span><span class="sxs-lookup"><span data-stu-id="4cb7c-133">/MSI or /M</span></span>**  
<span data-ttu-id="4cb7c-134">Указывает, следует ли создавать установщик Windows для упорядоченного приложения.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-134">Specifies whether a Windows Installer for the sequenced application should be created.</span></span>

<a href="" id="-default"></a>**<span data-ttu-id="4cb7c-135">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="4cb7c-135">/DEFAULT</span></span>**  
<span data-ttu-id="4cb7c-136">Указывает файл SPRJ по умолчанию, который будет использоваться при создании виртуального пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-136">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="4cb7c-137">Этот файл используется в качестве шаблона. SPRJ, когда приложение выполняется в первый раз.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-137">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>**<span data-ttu-id="4cb7c-138">/UPGRADE</span><span class="sxs-lookup"><span data-stu-id="4cb7c-138">/UPGRADE</span></span>**  
<span data-ttu-id="4cb7c-139">Указывает путь и имя файла SPRJ, который будет обновлен.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-139">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>**<span data-ttu-id="4cb7c-140">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="4cb7c-140">/DECODEPATH</span></span>**  
<span data-ttu-id="4cb7c-141">Указывает каталог на компьютере виртуализации, на котором установлены файлы, связанные с пакетом упорядоченного приложения.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-141">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="4cb7c-142">При указании каталога используйте один из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="4cb7c-142">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="4cb7c-143">/DECODEPATH: Q:</span><span class="sxs-lookup"><span data-stu-id="4cb7c-143">/decodepath:Q:</span></span>

-   <span data-ttu-id="4cb7c-144">/decodepath:Q:.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-144">/decodepath:Q:.</span></span>

-   <span data-ttu-id="4cb7c-145">/decodepath:"Q:."</span><span class="sxs-lookup"><span data-stu-id="4cb7c-145">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="4cb7c-146">/DECODEPATH: "Q:"</span><span class="sxs-lookup"><span data-stu-id="4cb7c-146">/decodepath:”Q:”</span></span>

## <span data-ttu-id="4cb7c-147">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4cb7c-147">Related topics</span></span>


[<span data-ttu-id="4cb7c-148">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="4cb7c-148">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

[<span data-ttu-id="4cb7c-149">Коды ошибок командной строки программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="4cb7c-149">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

 

 





