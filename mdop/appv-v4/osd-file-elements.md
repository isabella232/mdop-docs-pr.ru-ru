---
title: Элементы файлов OSD
description: Элементы файлов OSD
author: dansimp
ms.assetid: 8211b562-7549-4331-8321-144f52574e99
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8e3ebcf53ff39ecd2ef7ad0feec0bbbcae199db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816109"
---
# <span data-ttu-id="91c44-103">Элементы файлов OSD</span><span class="sxs-lookup"><span data-stu-id="91c44-103">OSD File Elements</span></span>


<span data-ttu-id="91c44-104">Каталог установки Sequencer содержит файл схемы XML, **Softricity. xsd**, который определяет допустимую структуру открытого файла дескриптора программного обеспечения (OSD).</span><span class="sxs-lookup"><span data-stu-id="91c44-104">The Sequencer installation directory contains an XML schema file, **Softricity.xsd**, which defines the valid structure of an Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="91c44-105">Ниже перечислены некоторые из наиболее часто используемых элементов OSD.</span><span class="sxs-lookup"><span data-stu-id="91c44-105">Following are some of the more frequently used OSD elements.</span></span>

<a href="" id="softpkg"></a><span data-ttu-id="91c44-106">SOFTPKG</span><span class="sxs-lookup"><span data-stu-id="91c44-106">SOFTPKG</span></span>  
<span data-ttu-id="91c44-107">Корневой элемент OSD файла, который содержит все элементы, определяющие пакет программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="91c44-107">The root element of the OSD file containing all elements defining the software package.</span></span>

<a href="" id="codebase"></a><span data-ttu-id="91c44-108">БАЗА</span><span class="sxs-lookup"><span data-stu-id="91c44-108">CODEBASE</span></span>  
<span data-ttu-id="91c44-109">Сведения о SFT – файле для этого пакета, включая атрибуты HREF, FILENAME и GUID.</span><span class="sxs-lookup"><span data-stu-id="91c44-109">Information about the .sft file for this package, including the HREF, FILENAME, and GUID attributes.</span></span> <span data-ttu-id="91c44-110">Вы можете изменить атрибут HREF, если вы изменили точку распространения в этом конкретном пакете.</span><span class="sxs-lookup"><span data-stu-id="91c44-110">You can edit the HREF attribute if you change the distribution point of this particular package.</span></span>

<a href="" id="os"></a><span data-ttu-id="91c44-111">ОС</span><span class="sxs-lookup"><span data-stu-id="91c44-111">OS</span></span>  
<span data-ttu-id="91c44-112">Определяет, какие операционные системы может запускать это приложение на основании значений, которые изначально заданы в мастере виртуализации.</span><span class="sxs-lookup"><span data-stu-id="91c44-112">Defines on what operating systems this application can run based on values that are initially set in the Sequencing Wizard.</span></span> <span data-ttu-id="91c44-113">Это значение может содержать только значения, определенные в **Softricity. xsd**.</span><span class="sxs-lookup"><span data-stu-id="91c44-113">This value can contain only the values defined in **Softricity.xsd**.</span></span>

<a href="" id="local-interaction-allowed"></a><span data-ttu-id="91c44-114">ЛОКАЛЬНЫЙ \ _INTERACTION \ _ALLOWED</span><span class="sxs-lookup"><span data-stu-id="91c44-114">LOCAL\_INTERACTION\_ALLOWED</span></span>  
<span data-ttu-id="91c44-115">Если задано значение "TRUE", это позволяет создавать именованные объекты (события, мьютексы, семафоры, сопоставления файлов и mailslots) и COM-объекты в глобальном пространстве имен, а не изолированные внутри конкретной виртуальной среды, которая позволяет виртуальным приложениям взаимодействовать с приложениями операционной системы хоста.</span><span class="sxs-lookup"><span data-stu-id="91c44-115">Set to TRUE, this enables creation of named objects (events, mutexes, semaphores, file mappings, and mailslots) and COM objects in the global namespace rather than isolated inside a particular virtual environment, which allows virtual applications to interact with the host operating system's applications.</span></span>

<span data-ttu-id="91c44-116">Пример: &lt; &gt; &lt; Реализация SOFTPKG&gt;</span><span class="sxs-lookup"><span data-stu-id="91c44-116">Example:&lt;SOFTPKG&gt;&lt;IMPLEMENTATION&gt;</span></span>

<span data-ttu-id="91c44-117">&lt;&gt; &lt; политики VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="91c44-117">&lt;VIRTUALENV&gt;&lt;POLICIES&gt;</span></span>

<span data-ttu-id="91c44-118">&lt;ЛОКАЛЬНЫЙ \ _INTERACTION \ _ALLOWED &gt; Истина</span><span class="sxs-lookup"><span data-stu-id="91c44-118">&lt;LOCAL\_INTERACTION\_ALLOWED&gt;TRUE</span></span>

<span data-ttu-id="91c44-119">&lt;/LOCAL\ _INTERACTION "_ALLOWED&gt;</span><span class="sxs-lookup"><span data-stu-id="91c44-119">&lt;/LOCAL\_INTERACTION\_ALLOWED&gt;</span></span>

<span data-ttu-id="91c44-120">&lt;/POLICIES &gt; &lt; /VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="91c44-120">&lt;/POLICIES&gt;&lt;/VIRTUALENV&gt;</span></span>

<span data-ttu-id="91c44-121">&lt;/IMPLEMENTATION &gt; &lt; /SOFTPKG&gt;</span><span class="sxs-lookup"><span data-stu-id="91c44-121">&lt;/IMPLEMENTATION&gt;&lt;/SOFTPKG&gt;</span></span>

<a href="" id="dependencies"></a><span data-ttu-id="91c44-122">НЕЗАВИСИМО</span><span class="sxs-lookup"><span data-stu-id="91c44-122">DEPENDENCIES</span></span>  
<span data-ttu-id="91c44-123">Определяет композицию динамического набора (зависимостей в других пакетах), используя тег CODEBASE из другого пакета.</span><span class="sxs-lookup"><span data-stu-id="91c44-123">Defines Dynamic Suite Composition (dependencies on other packages) by using a CODEBASE tag from another package.</span></span>

<span data-ttu-id="91c44-124">Пример: &lt; Dependencies &gt; &lt; CODEBASE HREF = "RTSPS://Server/Package.SFT" GUID = "7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE = "pkg. 1 \ \ osguard. CP" size = "6572748" обязательный = "ложь"/ &gt; &lt; /Dependencies&gt;</span><span class="sxs-lookup"><span data-stu-id="91c44-124">Example:&lt;DEPENDENCIES&gt;&lt;CODEBASE HREF="rtsps://server/package.sft" GUID="7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE="pkg.1\\osguard.cp" SIZE="6572748" MANDATORY="FALSE"/&gt;&lt;/DEPENDENCIES&gt;</span></span>

<a href="" id="package-name"></a><span data-ttu-id="91c44-125">ИМЯ ПАКЕТА</span><span class="sxs-lookup"><span data-stu-id="91c44-125">PACKAGE NAME</span></span>  
<span data-ttu-id="91c44-126">Обычное имя пакета, введенное на странице **сведения о пакете** мастера виртуализации, которое позволяет указать одно имя, используемое для упорядоченного приложения, которое содержит несколько приложений.</span><span class="sxs-lookup"><span data-stu-id="91c44-126">A common name for the package entered into the Sequencing Wizard **Package Information** page, which enables you to specify a single name used for a sequenced application containing multiple applications.</span></span>

<a href="" id="title"></a><span data-ttu-id="91c44-127">Название</span><span class="sxs-lookup"><span data-stu-id="91c44-127">TITLE</span></span>  
<span data-ttu-id="91c44-128">Необязательное описательное имя приложения, которое вы собираетесь поочередно.</span><span class="sxs-lookup"><span data-stu-id="91c44-128">Optional descriptive name of the application you are sequencing.</span></span>

<a href="" id="abstract"></a><span data-ttu-id="91c44-129">ВЫДЕЛЯЕТ</span><span class="sxs-lookup"><span data-stu-id="91c44-129">ABSTRACT</span></span>  
<span data-ttu-id="91c44-130">Краткое описание пакета программного обеспечения, указанного в поле **Примечания** на странице **сведения о пакете** мастера виртуализации.</span><span class="sxs-lookup"><span data-stu-id="91c44-130">Short description of the software package entered in the **Comments** field in the Sequencing Wizard **Package Information** page.</span></span> <span data-ttu-id="91c44-131">Рекомендуется указывать такие сведения, как версия операционной системы и пакета обновления для рабочей станции Sequencer, версия секвенсора и название инженера по виртуализации.</span><span class="sxs-lookup"><span data-stu-id="91c44-131">A best practice is to specify information such as the operating system and service-pack level of the Sequencer workstation, Sequencer version, and the sequencing engineer’s name.</span></span>

<a href="" id="script"></a><span data-ttu-id="91c44-132">ДЕЛА</span><span class="sxs-lookup"><span data-stu-id="91c44-132">SCRIPT</span></span>  
<span data-ttu-id="91c44-133">Определяет определенные события сценария, которые должны происходить при запуске, завершении работы или потоковой передаче.</span><span class="sxs-lookup"><span data-stu-id="91c44-133">Defines specific scripted events to occur during startup, shutdown, or streaming.</span></span>

<a href="" id="mgmt-shortcutlist"></a><span data-ttu-id="91c44-134">РУКОВОДСТВА \ _SHORTCUTLIST</span><span class="sxs-lookup"><span data-stu-id="91c44-134">MGMT\_SHORTCUTLIST</span></span>  
<span data-ttu-id="91c44-135">Список всех сочетаний клавиш, определенных в мастере.</span><span class="sxs-lookup"><span data-stu-id="91c44-135">List of all shortcuts defined in the wizard.</span></span>

<a href="" id="mgmt-fileassociations"></a><span data-ttu-id="91c44-136">РУКОВОДСТВА \ _FILEASSOCIATIONS</span><span class="sxs-lookup"><span data-stu-id="91c44-136">MGMT\_FILEASSOCIATIONS</span></span>  
<span data-ttu-id="91c44-137">Список типов файлов, указанных в мастере.</span><span class="sxs-lookup"><span data-stu-id="91c44-137">List of the file types specified in the wizard.</span></span>

## <span data-ttu-id="91c44-138">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="91c44-138">Related topics</span></span>


[<span data-ttu-id="91c44-139">Вкладка "Сведения об OSD"</span><span class="sxs-lookup"><span data-stu-id="91c44-139">About the OSD Tab</span></span>](about-the-osd-tab.md)

 

 





