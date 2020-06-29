---
title: Коды ошибок командной строки программы Sequencer
description: Коды ошибок командной строки программы Sequencer
author: dansimp
ms.assetid: 3d491314-4923-45fd-9839-c541c5e620bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74f5bd0c1b66656ac6891dcc1c019254fa36fdac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815559"
---
# <span data-ttu-id="b3da2-103">Коды ошибок командной строки программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="b3da2-103">Sequencer Command-Line Error Codes</span></span>


<span data-ttu-id="b3da2-104">Следующий список поможет выявить ошибки, связанные с последовательностью приложений, с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="b3da2-104">Use the following list to help identify errors that are related to sequencing applications by using the command line.</span></span> <span data-ttu-id="b3da2-105">Вы также можете просмотреть эту информацию, просмотрев соответствующий файл журнала секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="b3da2-105">You can also see this information by viewing the associated App-V Sequencer log file.</span></span>

<span data-ttu-id="b3da2-106">**Примечание**  При выполнении последовательности может возникнуть несколько ошибок, и в этом случае код ошибки может выводиться в виде суммы двух кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="b3da2-106">**Note** Multiple errors can occur during sequencing, and if this happens, the error code that is displayed might be the sum of two error codes.</span></span> <span data-ttu-id="b3da2-107">Например, если отсутствуют параметры */INSTALLPATH* и */OutputFile* , программа Sequencer App-V возвращает **96**— сумму этих двух кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="b3da2-107">For example, if the */InstallPath* and */OutputFile* parameters are missing, the App-V Sequencer will return **96**—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="b3da2-108">ведение</span><span class="sxs-lookup"><span data-stu-id="b3da2-108">01</span></span>  
<span data-ttu-id="b3da2-109">Неопределенное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b3da2-109">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="b3da2-110">баланс</span><span class="sxs-lookup"><span data-stu-id="b3da2-110">02</span></span>  
<span data-ttu-id="b3da2-111">Указан недопустимый каталог для установки (/INSTALLPACKAGE).</span><span class="sxs-lookup"><span data-stu-id="b3da2-111">The specified installation directory (/INSTALLPACKAGE) is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="b3da2-112">мая</span><span class="sxs-lookup"><span data-stu-id="b3da2-112">04</span></span>  
<span data-ttu-id="b3da2-113">Указан недопустимый корневой каталог пакета (/INSTALLPATH).</span><span class="sxs-lookup"><span data-stu-id="b3da2-113">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="b3da2-114">08</span><span class="sxs-lookup"><span data-stu-id="b3da2-114">08</span></span>  
<span data-ttu-id="b3da2-115">Указан недопустимый параметр */OutputFile* .</span><span class="sxs-lookup"><span data-stu-id="b3da2-115">The specified */OutputFile* parameter is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="b3da2-116">шестнадцат</span><span class="sxs-lookup"><span data-stu-id="b3da2-116">16</span></span>  
<span data-ttu-id="b3da2-117">Не указан каталог установки (/INSTALLPACKAGE).</span><span class="sxs-lookup"><span data-stu-id="b3da2-117">The installation directory (/INSTALLPACKAGE) is not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="b3da2-118">32</span><span class="sxs-lookup"><span data-stu-id="b3da2-118">32</span></span>  
<span data-ttu-id="b3da2-119">Не указан корневой каталог пакета (/INSTALLPATH).</span><span class="sxs-lookup"><span data-stu-id="b3da2-119">The package root directory (/INSTALLPATH) is not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="b3da2-120">64</span><span class="sxs-lookup"><span data-stu-id="b3da2-120">64</span></span>  
<span data-ttu-id="b3da2-121">Параметр */OutputFile* не указан.</span><span class="sxs-lookup"><span data-stu-id="b3da2-121">The */OutputFile* parameter is not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="b3da2-122">128</span><span class="sxs-lookup"><span data-stu-id="b3da2-122">128</span></span>  
<span data-ttu-id="b3da2-123">Указан недопустимый диск Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="b3da2-123">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="b3da2-124">256</span><span class="sxs-lookup"><span data-stu-id="b3da2-124">256</span></span>  
<span data-ttu-id="b3da2-125">Сбой установщика.</span><span class="sxs-lookup"><span data-stu-id="b3da2-125">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="b3da2-126">512</span><span class="sxs-lookup"><span data-stu-id="b3da2-126">512</span></span>  
<span data-ttu-id="b3da2-127">Не удалось выполнить виртуализацию приложения.</span><span class="sxs-lookup"><span data-stu-id="b3da2-127">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="b3da2-128">1024</span><span class="sxs-lookup"><span data-stu-id="b3da2-128">1024</span></span>  
<span data-ttu-id="b3da2-129">Не удалось выполнить оценку установленных сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="b3da2-129">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="b3da2-130">2048</span><span class="sxs-lookup"><span data-stu-id="b3da2-130">2048</span></span>  
<span data-ttu-id="b3da2-131">Невозможно сохранить пакет упорядоченной программы.</span><span class="sxs-lookup"><span data-stu-id="b3da2-131">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="b3da2-132">4096</span><span class="sxs-lookup"><span data-stu-id="b3da2-132">4096</span></span>  
<span data-ttu-id="b3da2-133">Указанное имя пакета (/PACKAGENAME) является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="b3da2-133">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="b3da2-134">8192</span><span class="sxs-lookup"><span data-stu-id="b3da2-134">8192</span></span>  
<span data-ttu-id="b3da2-135">Указан недопустимый размер блока (/BLOCKSIZE).</span><span class="sxs-lookup"><span data-stu-id="b3da2-135">The specified block size (/BLOCKSIZE) is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="b3da2-136">16384</span><span class="sxs-lookup"><span data-stu-id="b3da2-136">16384</span></span>  
<span data-ttu-id="b3da2-137">Указан недопустимый тип сжатия (/COMPRESSION).</span><span class="sxs-lookup"><span data-stu-id="b3da2-137">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="b3da2-138">32768</span><span class="sxs-lookup"><span data-stu-id="b3da2-138">32768</span></span>  
<span data-ttu-id="b3da2-139">Указан недопустимый путь к проекту.</span><span class="sxs-lookup"><span data-stu-id="b3da2-139">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="b3da2-140">65536</span><span class="sxs-lookup"><span data-stu-id="b3da2-140">65536</span></span>  
<span data-ttu-id="b3da2-141">Указан недопустимый параметр обновления.</span><span class="sxs-lookup"><span data-stu-id="b3da2-141">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="b3da2-142">131072</span><span class="sxs-lookup"><span data-stu-id="b3da2-142">131072</span></span>  
<span data-ttu-id="b3da2-143">Указан недопустимый параметр проекта обновления.</span><span class="sxs-lookup"><span data-stu-id="b3da2-143">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="b3da2-144">262144</span><span class="sxs-lookup"><span data-stu-id="b3da2-144">262144</span></span>  
<span data-ttu-id="b3da2-145">Указан недопустимый параметр пути декодирования.</span><span class="sxs-lookup"><span data-stu-id="b3da2-145">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="b3da2-146">525288</span><span class="sxs-lookup"><span data-stu-id="b3da2-146">525288</span></span>  
<span data-ttu-id="b3da2-147">Не указано имя пакета.</span><span class="sxs-lookup"><span data-stu-id="b3da2-147">The package name is not specified.</span></span>

## <span data-ttu-id="b3da2-148">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b3da2-148">Related topics</span></span>


[<span data-ttu-id="b3da2-149">Справка по программе Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="b3da2-149">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

[<span data-ttu-id="b3da2-150">Параметры командной строки программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="b3da2-150">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)

 

 





