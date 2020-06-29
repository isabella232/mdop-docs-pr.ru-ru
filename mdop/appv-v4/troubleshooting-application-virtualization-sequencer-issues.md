---
title: Устранение неполадок в работе программы Application Virtualization Sequencer
description: Устранение неполадок в работе программы Application Virtualization Sequencer
author: dansimp
ms.assetid: 2712094b-a0bc-4643-aced-5415535f3fec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8b84f37217f29ff2c08a2254d7f54ce74348d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815242"
---
# <span data-ttu-id="ba013-103">Устранение неполадок в работе программы Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="ba013-103">Troubleshooting Application Virtualization Sequencer Issues</span></span>


<span data-ttu-id="ba013-104">Этот раздел содержит сведения, которые можно использовать для устранения общих проблем, возникающих в секвенсоре Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="ba013-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="ba013-105">Создание файла SFTD с помощью секвенсора App-V приводит к неожиданному увеличению номера версии</span><span class="sxs-lookup"><span data-stu-id="ba013-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="ba013-106">Используйте командную строку для создания нового SFT-файла.</span><span class="sxs-lookup"><span data-stu-id="ba013-106">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="ba013-107">Чтобы создать SFT-файл с помощью командной строки, введите в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ba013-107">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="ba013-108">mkdiffpkg.exe &lt; имя базового SFT — имя &gt; &lt; файла SFT&gt;</span><span class="sxs-lookup"><span data-stu-id="ba013-108">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="ba013-109">После обновления пакета имя файла в OSD не поддается исправлению</span><span class="sxs-lookup"><span data-stu-id="ba013-109">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="ba013-110">Когда вы открываете пакет для обновления, вы должны указать корневой диск Q:\\ в качестве расположения выходных данных для пакета.</span><span class="sxs-lookup"><span data-stu-id="ba013-110">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="ba013-111">Не указывайте имя файла, связанного с расположением выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ba013-111">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="ba013-112">Установка Microsoft Word2003 по умолчанию приводит к ошибке при потоковой передаче клиенту.</span><span class="sxs-lookup"><span data-stu-id="ba013-112">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="ba013-113">При потоковой передаче клиенту Microsoft Word2003 возвращается сообщение об ошибке, но Microsoft Word продолжает работу.</span><span class="sxs-lookup"><span data-stu-id="ba013-113">When you stream Microsoft Word2003 to a client, an error is returned, but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="ba013-114">Решение</span><span class="sxs-lookup"><span data-stu-id="ba013-114">Solution</span></span>**

<span data-ttu-id="ba013-115">Переупорядочение пакета виртуального приложения и выбор **полной установки**.</span><span class="sxs-lookup"><span data-stu-id="ba013-115">Resequence the virtual application package and select **Full Install**.</span></span>

## <span data-ttu-id="ba013-116">Активное обновление не работает при создании зависимого пакета</span><span class="sxs-lookup"><span data-stu-id="ba013-116">Active Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="ba013-117">Когда вы создаете зависимый пакет с помощью активного обновления и добавляете новые записи в реестре, она будет работать правильно, но обновленные элементы реестра не будут доступны.</span><span class="sxs-lookup"><span data-stu-id="ba013-117">When you create a dependent package by using active upgrade and add new registry entries, it appears to function correctly, but the updated registry entries are not available.</span></span>

**<span data-ttu-id="ba013-118">Решение</span><span class="sxs-lookup"><span data-stu-id="ba013-118">Solution</span></span>**

<span data-ttu-id="ba013-119">Параметры реестра всегда хранятся вместе с исходной версией пакета, поэтому обновления пакета не будут доступны, пока вы не восстановите первоначальный пакет.</span><span class="sxs-lookup"><span data-stu-id="ba013-119">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="ba013-120">Подробные сведения не отображаются для документов Microsoft office2007 с помощью страницы "Свойства"</span><span class="sxs-lookup"><span data-stu-id="ba013-120">Detailed information is not visible for Microsoft Office2007 documents by using the properties page</span></span>


<span data-ttu-id="ba013-121">При попытке просмотреть подробную информацию, связанную с документом Microsoft office2007 с помощью страницы свойств, подробные сведения не отображаются.</span><span class="sxs-lookup"><span data-stu-id="ba013-121">When you try to view detailed information associated with a Microsoft Office2007 document by using the properties page, the detailed information is not visible.</span></span>

**<span data-ttu-id="ba013-122">Решение</span><span class="sxs-lookup"><span data-stu-id="ba013-122">Solution</span></span>**

<span data-ttu-id="ba013-123">Приложение App-V не поддерживает необходимые расширения оболочки для этих страниц свойств.</span><span class="sxs-lookup"><span data-stu-id="ba013-123">App-V does not support the required shell extensions for these property pages.</span></span>

## <span data-ttu-id="ba013-124">Некоторые разделы реестра не регистрируются при последовательности 16-разрядных приложений.</span><span class="sxs-lookup"><span data-stu-id="ba013-124">Some registry keys are not captured when you sequence 16-bit applications</span></span>


<span data-ttu-id="ba013-125">В App-V 4,5 подключение к реестру перемещается из режима ядра в пользовательский режим.</span><span class="sxs-lookup"><span data-stu-id="ba013-125">In App-V 4.5, registry hooking has been moved from kernel mode to user mode.</span></span> <span data-ttu-id="ba013-126">Если вы хотите поочередно использовать 16-разрядное приложение или приложение, использующее 16-разрядную программу установки, необходимо сначала настроить компьютер Sequencer так, чтобы процесс выполнялся в собственной копии виртуальной машины Windows NT (NTVDM).</span><span class="sxs-lookup"><span data-stu-id="ba013-126">If you want to sequence a 16-bit application or an application that uses a 16-bit installer, you must first configure the sequencer computer so that the process runs in its own copy of the Windows NT Virtual DOS Machine (NTVDM).</span></span>

**<span data-ttu-id="ba013-127">Решение</span><span class="sxs-lookup"><span data-stu-id="ba013-127">Solution</span></span>**

<span data-ttu-id="ba013-128">Перед последовательностью приложения задайте для параметра реестра Global REGSZ значение "Да" на компьютере виртуализации:</span><span class="sxs-lookup"><span data-stu-id="ba013-128">Before you sequence the application, set the following global REGSZ registry key value to "yes" on the sequencing computer:</span></span>

<span data-ttu-id="ba013-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span><span class="sxs-lookup"><span data-stu-id="ba013-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span></span>

<span data-ttu-id="ba013-130">Перед тем как это вступит в силу, необходимо перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="ba013-130">You must restart the computer before this takes effect.</span></span>

## <span data-ttu-id="ba013-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ba013-131">Related topics</span></span>


[<span data-ttu-id="ba013-132">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="ba013-132">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





