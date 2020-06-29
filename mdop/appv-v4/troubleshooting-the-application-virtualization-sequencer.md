---
title: Устранение неполадок в программе Application Virtualization Sequencer
description: Устранение неполадок в программе Application Virtualization Sequencer
author: dansimp
ms.assetid: 12ea8367-0b84-44e1-a885-e0539486556b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60c47b853c74d90afc21e9ca172c0eec2a2c7a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815182"
---
# <span data-ttu-id="613d3-103">Устранение неполадок в программе Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="613d3-103">Troubleshooting the Application Virtualization Sequencer</span></span>


<span data-ttu-id="613d3-104">Этот раздел содержит сведения, которые можно использовать для устранения общих проблем, возникающих в секвенсоре Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="613d3-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="613d3-105">Создание файла SFTD с помощью секвенсора App-V приводит к неожиданному увеличению номера версии</span><span class="sxs-lookup"><span data-stu-id="613d3-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="613d3-106">Номер версии, связанный с файлом SFTD, будет неожиданно увеличиваться.</span><span class="sxs-lookup"><span data-stu-id="613d3-106">The version number associated with an SFTD file increases unexpectedly.</span></span>

**<span data-ttu-id="613d3-107">Решение</span><span class="sxs-lookup"><span data-stu-id="613d3-107">Solution</span></span>**

<span data-ttu-id="613d3-108">Используйте командную строку для создания нового SFT-файла.</span><span class="sxs-lookup"><span data-stu-id="613d3-108">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="613d3-109">Чтобы создать SFT-файл с помощью командной строки, введите в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="613d3-109">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="613d3-110">mkdiffpkg.exe &lt; имя базового SFT — имя &gt; &lt; файла SFT&gt;</span><span class="sxs-lookup"><span data-stu-id="613d3-110">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="613d3-111">После обновления пакета имя файла в OSD не поддается исправлению</span><span class="sxs-lookup"><span data-stu-id="613d3-111">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="613d3-112">После обновления существующего пакета его имя не подходит.</span><span class="sxs-lookup"><span data-stu-id="613d3-112">After you upgrade an existing package, the file name is not correct.</span></span>

**<span data-ttu-id="613d3-113">Решение</span><span class="sxs-lookup"><span data-stu-id="613d3-113">Solution</span></span>**

<span data-ttu-id="613d3-114">Когда вы открываете пакет для обновления, вы должны указать корневой диск Q:\\ в качестве расположения выходных данных для пакета.</span><span class="sxs-lookup"><span data-stu-id="613d3-114">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="613d3-115">Не указывайте имя файла, связанного с расположением выходных данных.</span><span class="sxs-lookup"><span data-stu-id="613d3-115">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="613d3-116">Установка Microsoft Word2003 по умолчанию приводит к ошибке при потоковой передаче клиенту.</span><span class="sxs-lookup"><span data-stu-id="613d3-116">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="613d3-117">При потоковой передаче на клиент Microsoft Word2003 возвращается сообщение об ошибке, но Microsoft Word продолжает работу.</span><span class="sxs-lookup"><span data-stu-id="613d3-117">When you stream Microsoft Word2003 to a client, an error is returned but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="613d3-118">Решение</span><span class="sxs-lookup"><span data-stu-id="613d3-118">Solution</span></span>**

<span data-ttu-id="613d3-119">Переупорядочение виртуального пакета приложения и выбор пункта **полная установка**.</span><span class="sxs-lookup"><span data-stu-id="613d3-119">Resequence the virtual application package, and select **Full Install**.</span></span>

## <span data-ttu-id="613d3-120">Обновление пакета не работает при создании зависимого пакета</span><span class="sxs-lookup"><span data-stu-id="613d3-120">Package Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="613d3-121">Когда вы создаете зависимый пакет с помощью обновления пакетов и добавляете новые записи в реестре, он работает правильно, но обновленные элементы реестра недоступны.</span><span class="sxs-lookup"><span data-stu-id="613d3-121">When you create a dependent package by using package upgrade and add new registry entries, it appears to function correctly but the updated registry entries are not available.</span></span>

**<span data-ttu-id="613d3-122">Решение</span><span class="sxs-lookup"><span data-stu-id="613d3-122">Solution</span></span>**

<span data-ttu-id="613d3-123">Параметры реестра всегда хранятся вместе с исходной версией пакета, поэтому обновления пакета не будут доступны, пока вы не восстановите первоначальный пакет.</span><span class="sxs-lookup"><span data-stu-id="613d3-123">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="613d3-124">Ошибка при попытке последовательного выполнения последовательности. NET 2.0</span><span class="sxs-lookup"><span data-stu-id="613d3-124">Error When Trying to Sequence .NET2.0</span></span>


<span data-ttu-id="613d3-125">При упорядочении пакета, который требуется. NET 2.0 появляется сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="613d3-125">When you sequence a package that requires .NET2.0, you get an error.</span></span>

**<span data-ttu-id="613d3-126">Решение</span><span class="sxs-lookup"><span data-stu-id="613d3-126">Solution</span></span>**

<span data-ttu-id="613d3-127">Упорядочение пакетов, для которых требуется. NET 2.0 не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="613d3-127">Sequencing packages that require .NET2.0 is not supported.</span></span>

## <span data-ttu-id="613d3-128">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="613d3-128">Related topics</span></span>


[<span data-ttu-id="613d3-129">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="613d3-129">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





