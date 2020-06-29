---
title: Ошибки командной строки
description: Ошибки командной строки
author: dansimp
ms.assetid: eea62568-4e90-4877-9cc7-e27ef5c05068
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab29a77dc15a8c7bd3590b918a7ca8c1ca6e8c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819409"
---
# <span data-ttu-id="4f932-103">Ошибки командной строки</span><span class="sxs-lookup"><span data-stu-id="4f932-103">Command-Line Errors</span></span>


<span data-ttu-id="4f932-104">С помощью приведенного ниже списка ошибок можно определить причины, по которым выполнение последовательности команд в командной строке не работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="4f932-104">Use the following list of errors to identify the reasons why command-line sequencing is not working properly.</span></span> <span data-ttu-id="4f932-105">Кроме того, вы можете просмотреть эти ошибки, просмотрев файл журнала секвенсора.</span><span class="sxs-lookup"><span data-stu-id="4f932-105">You can also see these errors by viewing the sequencer log file.</span></span>

<span data-ttu-id="4f932-106">**Примечание**  При выполнении последовательности может отображаться более одной ошибки.</span><span class="sxs-lookup"><span data-stu-id="4f932-106">**Note** More than one error might be displayed when sequencing.</span></span> <span data-ttu-id="4f932-107">Кроме того, отображаемый код ошибки может представлять собой сумму двух кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="4f932-107">Furthermore, the error code displayed might be the sum of two error codes.</span></span> <span data-ttu-id="4f932-108">Например, если отсутствуют параметры */INSTALLPATH* и */OutputFile* , программа Microsoft System Center Application Virtualization возвращает 96 — сумму двух кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="4f932-108">For example, if the */InstallPath* and */OutputFile* parameters are missing, the Microsoft System Center Application Virtualization Sequencer will return 96—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="4f932-109">ведение</span><span class="sxs-lookup"><span data-stu-id="4f932-109">01</span></span>  
<span data-ttu-id="4f932-110">Неопределенное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4f932-110">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="4f932-111">баланс</span><span class="sxs-lookup"><span data-stu-id="4f932-111">02</span></span>  
<span data-ttu-id="4f932-112">Указан недопустимый каталог для установки (/INSTALLPACKAGE).</span><span class="sxs-lookup"><span data-stu-id="4f932-112">The specified installation directory (/INSTALLPACKAGE) specified is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="4f932-113">мая</span><span class="sxs-lookup"><span data-stu-id="4f932-113">04</span></span>  
<span data-ttu-id="4f932-114">Указан недопустимый корневой каталог пакета (/INSTALLPATH).</span><span class="sxs-lookup"><span data-stu-id="4f932-114">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="4f932-115">08</span><span class="sxs-lookup"><span data-stu-id="4f932-115">08</span></span>  
<span data-ttu-id="4f932-116">Указан недопустимый параметр */OutputFile* .</span><span class="sxs-lookup"><span data-stu-id="4f932-116">The */OutputFile* parameter that was specified is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="4f932-117">шестнадцат</span><span class="sxs-lookup"><span data-stu-id="4f932-117">16</span></span>  
<span data-ttu-id="4f932-118">Не указан каталог установки (/INSTALLPACKAGE).</span><span class="sxs-lookup"><span data-stu-id="4f932-118">The installation directory (/INSTALLPACKAGE) was not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="4f932-119">32</span><span class="sxs-lookup"><span data-stu-id="4f932-119">32</span></span>  
<span data-ttu-id="4f932-120">Не указан корневой каталог пакета (/INSTALLPATH).</span><span class="sxs-lookup"><span data-stu-id="4f932-120">The package root directory (/INSTALLPATH) was not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="4f932-121">64</span><span class="sxs-lookup"><span data-stu-id="4f932-121">64</span></span>  
<span data-ttu-id="4f932-122">Параметр */OutputFile* не указан.</span><span class="sxs-lookup"><span data-stu-id="4f932-122">The */OutputFile* parameter was not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="4f932-123">128</span><span class="sxs-lookup"><span data-stu-id="4f932-123">128</span></span>  
<span data-ttu-id="4f932-124">Указан недопустимый диск Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="4f932-124">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="4f932-125">256</span><span class="sxs-lookup"><span data-stu-id="4f932-125">256</span></span>  
<span data-ttu-id="4f932-126">Сбой установщика.</span><span class="sxs-lookup"><span data-stu-id="4f932-126">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="4f932-127">512</span><span class="sxs-lookup"><span data-stu-id="4f932-127">512</span></span>  
<span data-ttu-id="4f932-128">Не удалось выполнить виртуализацию приложения.</span><span class="sxs-lookup"><span data-stu-id="4f932-128">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="4f932-129">1024</span><span class="sxs-lookup"><span data-stu-id="4f932-129">1024</span></span>  
<span data-ttu-id="4f932-130">Не удалось выполнить оценку установленных сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="4f932-130">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="4f932-131">2048</span><span class="sxs-lookup"><span data-stu-id="4f932-131">2048</span></span>  
<span data-ttu-id="4f932-132">Невозможно сохранить пакет упорядоченной программы.</span><span class="sxs-lookup"><span data-stu-id="4f932-132">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="4f932-133">4096</span><span class="sxs-lookup"><span data-stu-id="4f932-133">4096</span></span>  
<span data-ttu-id="4f932-134">Указанное имя пакета (/PACKAGENAME) является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="4f932-134">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="4f932-135">8192</span><span class="sxs-lookup"><span data-stu-id="4f932-135">8192</span></span>  
<span data-ttu-id="4f932-136">Указан недопустимый размер блока (/BLOCKSIZE <em> ) </em> .</span><span class="sxs-lookup"><span data-stu-id="4f932-136">The specified block size (/BLOCKSIZE<em>)</em> is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="4f932-137">16384</span><span class="sxs-lookup"><span data-stu-id="4f932-137">16384</span></span>  
<span data-ttu-id="4f932-138">Указан недопустимый тип сжатия (/COMPRESSION).</span><span class="sxs-lookup"><span data-stu-id="4f932-138">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="4f932-139">32768</span><span class="sxs-lookup"><span data-stu-id="4f932-139">32768</span></span>  
<span data-ttu-id="4f932-140">Указан недопустимый путь к проекту.</span><span class="sxs-lookup"><span data-stu-id="4f932-140">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="4f932-141">65536</span><span class="sxs-lookup"><span data-stu-id="4f932-141">65536</span></span>  
<span data-ttu-id="4f932-142">Указан недопустимый параметр обновления.</span><span class="sxs-lookup"><span data-stu-id="4f932-142">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="4f932-143">131072</span><span class="sxs-lookup"><span data-stu-id="4f932-143">131072</span></span>  
<span data-ttu-id="4f932-144">Указан недопустимый параметр проекта обновления.</span><span class="sxs-lookup"><span data-stu-id="4f932-144">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="4f932-145">262144</span><span class="sxs-lookup"><span data-stu-id="4f932-145">262144</span></span>  
<span data-ttu-id="4f932-146">Указан недопустимый параметр пути декодирования.</span><span class="sxs-lookup"><span data-stu-id="4f932-146">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="4f932-147">525288</span><span class="sxs-lookup"><span data-stu-id="4f932-147">525288</span></span>  
<span data-ttu-id="4f932-148">Не указано имя пакета.</span><span class="sxs-lookup"><span data-stu-id="4f932-148">The package name was not specified.</span></span>

## <span data-ttu-id="4f932-149">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4f932-149">Related topics</span></span>


[<span data-ttu-id="4f932-150">Сведения об использовании командной строки программы Sequencer</span><span class="sxs-lookup"><span data-stu-id="4f932-150">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="4f932-151">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="4f932-151">Command-Line Parameters</span></span>](command-line-parameters.md)

 

 





