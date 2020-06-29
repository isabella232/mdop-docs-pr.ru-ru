---
title: Сведения о программе Application Virtualization Sequencer
description: Сведения о программе Application Virtualization Sequencer
author: dansimp
ms.assetid: bee193ca-58bd-40c9-b41a-310435633895
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83709bcceabe3312fba34512b47d28a24b4dc52c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819999"
---
# <span data-ttu-id="d2de2-103">Сведения о программе Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="d2de2-103">About the Application Virtualization Sequencer</span></span>


<span data-ttu-id="d2de2-104">Секвенсор Microsoft Application Virtualization (App-V) осуществляет мониторинг и записывает все процессы установки и настройки для приложения и создает следующие файлы: **ICO**, **OSD**, **SFT**и **SPRJ**.</span><span class="sxs-lookup"><span data-stu-id="d2de2-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records all installation and setup processes for an application and creates the following files: **ICO**, **OSD**, **SFT**, and **SPRJ**.</span></span> <span data-ttu-id="d2de2-105">Эти файлы содержат все необходимые сведения о приложении, чтобы приложение могло работать в виртуальной среде на конечных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="d2de2-105">These files contain all the necessary information about an application so the application can run in a virtual environment on target computers.</span></span> <span data-ttu-id="d2de2-106">Для создания виртуальных приложений можно использовать секвенсор Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="d2de2-106">You can use the Microsoft Application Virtualization (App-V) Sequencer to create virtual applications.</span></span> <span data-ttu-id="d2de2-107">После того как вы перепланируете приложение, оно может быть перенаправлено на целевые компьютеры, или целевые компьютеры могут запускать виртуальное приложение, загружая содержимое виртуального пакета приложения и локально запуская приложение.</span><span class="sxs-lookup"><span data-stu-id="d2de2-107">After you sequence an application, it can be streamed to target computers, or target computers can run the virtual application by downloading the contents of the virtual application package and running the application locally.</span></span>

<span data-ttu-id="d2de2-108">**Важно!**  Для запуска виртуального пакета приложений на целевом компьютере должна быть установлена соответствующая версия клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="d2de2-108">**Important** To run a virtual application package the target computer must be running the appropriate version of the App-V client.</span></span>

 

<span data-ttu-id="d2de2-109">Пакеты виртуальных приложений выполняются на целевых компьютерах без взаимодействия с базовой операционной системой на целевом компьютере, так как каждое приложение запускается в виртуальной среде и изолируется от других приложений, установленных или запущенных на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="d2de2-109">Virtual application packages run on target computers without interacting with the underlying operating system on the target computer because each application runs in a virtual environment and is isolated from other applications that are installed or running on the target computer.</span></span> <span data-ttu-id="d2de2-110">Эта изоляция может снизить конфликты приложений и уменьшить требуемый объем тестирования перед развертыванием приложения.</span><span class="sxs-lookup"><span data-stu-id="d2de2-110">This isolation can reduce application conflicts and can help decrease the required amount of application pre-deployment testing.</span></span>

## <span data-ttu-id="d2de2-111">Терминология секвенсора</span><span class="sxs-lookup"><span data-stu-id="d2de2-111">Sequencer Terminology</span></span>


<a href="" id="application-virtualization-drive"></a><span data-ttu-id="d2de2-112">Диск Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="d2de2-112">Application Virtualization drive</span></span>  
<span data-ttu-id="d2de2-113">Диск Application Virtualization — это диск по умолчанию (Q:\) на целевом компьютере, с которого выполняются последовательные приложения.</span><span class="sxs-lookup"><span data-stu-id="d2de2-113">The application virtualization drive is the default drive (Q:\) on the target computer from which sequenced applications are run.</span></span>

<a href="" id="ico-file"></a><span data-ttu-id="d2de2-114">ICO файл</span><span class="sxs-lookup"><span data-stu-id="d2de2-114">ICO file</span></span>  
<span data-ttu-id="d2de2-115">Файл значка на клиентском компьютере, который используется для запуска упорядоченного приложения.</span><span class="sxs-lookup"><span data-stu-id="d2de2-115">The icon file on the client desktop which is used to launch a sequenced application.</span></span>

<a href="" id="installation-directory"></a><span data-ttu-id="d2de2-116">Каталог установки</span><span class="sxs-lookup"><span data-stu-id="d2de2-116">Installation directory</span></span>  
<span data-ttu-id="d2de2-117">Каталог, используемый секвенсором для размещения установочных файлов во время установки.</span><span class="sxs-lookup"><span data-stu-id="d2de2-117">The directory used by the sequencer to place installation files during setup.</span></span>

<a href="" id="open-software-descriptor--osd--file"></a><span data-ttu-id="d2de2-118">Открыть файл дескриптора программного обеспечения (OSD)</span><span class="sxs-lookup"><span data-stu-id="d2de2-118">Open Software Descriptor (OSD) file</span></span>  
<span data-ttu-id="d2de2-119">XML-файл, который указывает клиенту App-V, как получить упорядоченное приложение из потокового сервера App-V и как запускать упорядоченное приложение в виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="d2de2-119">An XML-based file that instructs the App-V client how to retrieve the sequenced application from the App-V streaming server and how to run the sequenced application in the virtual environment.</span></span>

<a href="" id="package-root-directory"></a><span data-ttu-id="d2de2-120">Корневой каталог пакета</span><span class="sxs-lookup"><span data-stu-id="d2de2-120">Package root directory</span></span>  
<span data-ttu-id="d2de2-121">Каталог на компьютере виртуализации, на котором установлены файлы для пакета последовательного приложения.</span><span class="sxs-lookup"><span data-stu-id="d2de2-121">The directory on the sequencing computer on which files for the sequenced application package are installed.</span></span> <span data-ttu-id="d2de2-122">Этот каталог также существует практически на компьютере, на котором поток будет передаваться последовательным приложением.</span><span class="sxs-lookup"><span data-stu-id="d2de2-122">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span>

<a href="" id="sequenced-application"></a><span data-ttu-id="d2de2-123">Упорядоченное приложение</span><span class="sxs-lookup"><span data-stu-id="d2de2-123">Sequenced application</span></span>  
<span data-ttu-id="d2de2-124">Приложение, отслеживаемое секвенсором, разработано в основном и дополнительном блоках, переводится на целевой компьютер, на котором запущен клиент App-V, и выполняет виртуальную среду.</span><span class="sxs-lookup"><span data-stu-id="d2de2-124">An application that has been monitored by the sequencer, broken up into primary and secondary feature blocks, streamed to a target computer running the App-V client t, and runs a virtual environment.</span></span>

<a href="" id="sequenced-application-package"></a><span data-ttu-id="d2de2-125">Пакет последовательных приложений</span><span class="sxs-lookup"><span data-stu-id="d2de2-125">Sequenced application package</span></span>  
<span data-ttu-id="d2de2-126">Файлы, которые составляют виртуальное приложение и позволяют запускать виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="d2de2-126">The files that comprise a virtual application and allow a virtual application to run.</span></span> <span data-ttu-id="d2de2-127">Эти файлы создаются после упорядочивания и специально включают в себя файлы **. OSD**, **SFT**, **SPRJ**и **ICO** .</span><span class="sxs-lookup"><span data-stu-id="d2de2-127">These files are created after sequencing and specifically include **.osd**, **.sft**, **.sprj**, and **.ico** files.</span></span>

<a href="" id="sequencing"></a><span data-ttu-id="d2de2-128">Последовательность</span><span class="sxs-lookup"><span data-stu-id="d2de2-128">Sequencing</span></span>  
<span data-ttu-id="d2de2-129">Процесс создания пакета приложения с помощью секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="d2de2-129">The process of creating an application package using the App-V Sequencer.</span></span> <span data-ttu-id="d2de2-130">В этом процессе отслеживается приложение, настраиваются его ярлыки, а также создается последовательный пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="d2de2-130">In this process, an application is monitored, its shortcuts are configured, and a sequenced application package is created.</span></span>

<a href="" id="sequencing-computer"></a><span data-ttu-id="d2de2-131">Последовательность компьютеров</span><span class="sxs-lookup"><span data-stu-id="d2de2-131">Sequencing computer</span></span>  
<span data-ttu-id="d2de2-132">Компьютер, используемый для упорядочения приложения.</span><span class="sxs-lookup"><span data-stu-id="d2de2-132">The computer used to sequence an application.</span></span>

<a href="" id="virtual-application"></a><span data-ttu-id="d2de2-133">Виртуальное приложение</span><span class="sxs-lookup"><span data-stu-id="d2de2-133">Virtual application</span></span>  
<span data-ttu-id="d2de2-134">Приложение, упакованное секвенсором для работы в автономной виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="d2de2-134">An application packaged by the Sequencer to run in a self-contained, virtual environment.</span></span> <span data-ttu-id="d2de2-135">Виртуальная среда включает сведения, необходимые для запуска приложения на клиенте, не устанавливая локальное приложение.</span><span class="sxs-lookup"><span data-stu-id="d2de2-135">The virtual environment contains the information necessary to run the application on the client without installing the application locally.</span></span>

<a href="" id="primary-feature-block"></a><span data-ttu-id="d2de2-136">Основной блок функций</span><span class="sxs-lookup"><span data-stu-id="d2de2-136">Primary feature block</span></span>  
<span data-ttu-id="d2de2-137">Минимальное содержимое пакета виртуальных приложений, необходимое для работы приложения на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="d2de2-137">The minimum content in a virtual application package that is necessary for an application to run on a target computer.</span></span> <span data-ttu-id="d2de2-138">Содержимое основного функционального блока идентифицировано на этапе приложения последовательности и обычно состоит из содержимого наиболее используемых функций приложения.</span><span class="sxs-lookup"><span data-stu-id="d2de2-138">The content in the primary feature block is identified during the application phase of sequencing and typically consists of the content for the most used application features.</span></span>

## <a href="" id="sequencing-applications-"></a><span data-ttu-id="d2de2-139">Виртуализация приложений</span><span class="sxs-lookup"><span data-stu-id="d2de2-139">Sequencing Applications</span></span>


<span data-ttu-id="d2de2-140">Существует два способа создания и изменения виртуальных пакетов приложений в среде.</span><span class="sxs-lookup"><span data-stu-id="d2de2-140">There are two methods to create and modify virtual application packages in your environment.</span></span> <span data-ttu-id="d2de2-141">Первый способ — с помощью мастера **упорядочения** .</span><span class="sxs-lookup"><span data-stu-id="d2de2-141">The first method is by using the **Sequencing** wizard.</span></span> <span data-ttu-id="d2de2-142">Мастер **виртуализации** позволяет создавать новые или изменять существующие пакеты виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="d2de2-142">The **Sequencing** wizard allows you to create new, or modify existing virtual application packages.</span></span> <span data-ttu-id="d2de2-143">Дополнительные сведения о том, как использовать мастер **виртуализации** , [можно найти в разделе Упорядочение нового приложения](how-to-sequence-a-new-application.md).</span><span class="sxs-lookup"><span data-stu-id="d2de2-143">For more information about using the **Sequencing** wizard see, [How to Sequence a New Application](how-to-sequence-a-new-application.md).</span></span> <span data-ttu-id="d2de2-144">Второй способ — с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="d2de2-144">The second method is by using the command-line.</span></span> <span data-ttu-id="d2de2-145">С помощью командной строки вы можете создавать новые или изменять существующие пакеты виртуальных приложений, используя командную строку.</span><span class="sxs-lookup"><span data-stu-id="d2de2-145">The command-line allows you to create new, or modify existing virtual application packages using the command prompt.</span></span> <span data-ttu-id="d2de2-146">Дополнительные сведения об использовании командной строки см. в разделе [Управление виртуальными приложениями с помощью командной строки](how-to-manage-virtual-applications-using-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="d2de2-146">For more information about using the command line see, [How to Manage Virtual Applications Using the Command Line](how-to-manage-virtual-applications-using-the-command-line.md).</span></span>

<span data-ttu-id="d2de2-147">Мастер **виртуализации** предоставляет следующие функции для создания пакетов виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="d2de2-147">The **Sequencing** wizard provides the following functions for creating virtual application packages:</span></span>

1.  <span data-ttu-id="d2de2-148">**Конфигурация пакета**: мастер **упорядочивания** запрашивает сведения о конфигурации пакета, необходимые для завершения работы с файлом дескриптора программного обеспечения (OSD), который является обязательным файлом для запуска упорядоченного пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="d2de2-148">**Package Configuration**: The **Sequencing** Wizard prompts for package configuration information necessary to complete the Open Software Descriptor (OSD) file, which is a required file for starting a sequenced application package.</span></span>

2.  <span data-ttu-id="d2de2-149">**Установка приложения**: мастер **виртуализации** собирает сведения о конфигурации и конфигурациях запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="d2de2-149">**Application Installation**: The **Sequencing** Wizard gathers information about an application’s installation and startup configurations.</span></span> <span data-ttu-id="d2de2-150">В нем отслеживаются и записываются сведения об установке и запуске, связанные с приложением, для создания файлов, необходимых для виртуального пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="d2de2-150">It monitors and records the installation and startup information associated with the application to create the files necessary for a virtual application package.</span></span>

3.  <span data-ttu-id="d2de2-151">**Запуск приложения**: мастер **виртуализации** собирает сведения для компиляции и сортировки блоков кода, необходимых для первоначального запуска упорядоченного пакета приложения на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="d2de2-151">**Application Startup**: The **Sequencing** Wizard gathers information for compiling and ordering the blocks of code necessary to perform the initial startup of the sequenced application package on the target computer.</span></span> <span data-ttu-id="d2de2-152">Компиляция блока кода называется основным блоком функций.</span><span class="sxs-lookup"><span data-stu-id="d2de2-152">The compilation of the code block is referred to as the primary feature block.</span></span>

## <span data-ttu-id="d2de2-153">Вопросы безопасности Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="d2de2-153">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="d2de2-154">Программа Sequencer App-V выполняет все службы, обнаруженные во время последовательности, с помощью локальной системной учетной записи и не использует дескрипторы безопасности для запросов на управление службами.</span><span class="sxs-lookup"><span data-stu-id="d2de2-154">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="d2de2-155">Если служба была установлена с помощью другой учетной записи пользователя или дескрипторы безопасности предназначены для предоставления различным группам пользователей конкретных разрешений, следует тщательно продумать, следует ли выполнять виртуализацию службы.</span><span class="sxs-lookup"><span data-stu-id="d2de2-155">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="d2de2-156">В некоторых случаях необходимо установить локальную службу, чтобы убедиться в том, что безопасность служб сохраняется.</span><span class="sxs-lookup"><span data-stu-id="d2de2-156">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

<span data-ttu-id="d2de2-157">**Важно!**  Вы всегда должны сохранять пакеты виртуальных приложений в безопасном месте.</span><span class="sxs-lookup"><span data-stu-id="d2de2-157">**Important** You should always save virtual application packages in a secure location.</span></span>

 

## <span data-ttu-id="d2de2-158">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d2de2-158">Related topics</span></span>


[<span data-ttu-id="d2de2-159">Обзор программы Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="d2de2-159">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





