---
title: Обзор консоли Application Virtualization Sequencer
description: Обзор консоли Application Virtualization Sequencer
author: dansimp
ms.assetid: 681bb40d-2937-4645-82aa-4a44775232d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2f977fccaaded0309181a1d74c16b749498abb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822192"
---
# <span data-ttu-id="c10ad-103">Обзор консоли Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="c10ad-103">Application Virtualization Sequencer Console Overview</span></span>


<span data-ttu-id="c10ad-104">Секвенсор Application Virtualization (App-V) создает приложения, чтобы их можно было выполнять в виртуальной среде в качестве виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="c10ad-104">The Application Virtualization (App-V) Sequencer creates applications so that they can be run in a virtual environment, as virtual applications.</span></span> <span data-ttu-id="c10ad-105">После того как приложение будет упорядочено, оно может быть запущено с сервера App-V на целевые компьютеры, на которых запущен клиент App-V Desktop, или клиент App-V для служб удаленных рабочих столов (ранее — службы терминалов) с помощью процесса, который называется Streaming.</span><span class="sxs-lookup"><span data-stu-id="c10ad-105">After an application has been sequenced, it can run from an App-V Server to target computers that are running the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using a process called streaming.</span></span> <span data-ttu-id="c10ad-106">Секвенсор App-V отслеживает процесс установки и настройки приложений и записывает все сведения, необходимые для запуска приложения в виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="c10ad-106">The App-V Sequencer monitors the installation and setup process for applications, and it records all the information necessary for the application to run in the virtual environment.</span></span> <span data-ttu-id="c10ad-107">Кроме того, этот процесс определяет, какие файлы и конфигурации применимы ко всем пользователям, а также о том, какие конфигурации пользователи могут настраивать.</span><span class="sxs-lookup"><span data-stu-id="c10ad-107">This process also determines which files and configurations are applicable to all users and which configurations users can customize.</span></span> <span data-ttu-id="c10ad-108">Виртуальные приложения выполняются на конечных компьютерах и не влияют на операционную систему, установленную на целевом компьютере, или на любом из приложений, установленных на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="c10ad-108">Virtual applications run on target computers and have no effect on the operating system running on the target computer or on any applications that are installed on the target computer.</span></span>

## <span data-ttu-id="c10ad-109">Вопросы безопасности Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="c10ad-109">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="c10ad-110">Программа Sequencer App-V выполняет все службы, обнаруженные во время последовательности, с помощью локальной системной учетной записи и не использует дескрипторы безопасности для запросов на управление службами.</span><span class="sxs-lookup"><span data-stu-id="c10ad-110">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="c10ad-111">Если служба была установлена с помощью другой учетной записи пользователя или дескрипторы безопасности предназначены для предоставления различным группам пользователей конкретных разрешений, следует тщательно продумать, следует ли выполнять виртуализацию службы.</span><span class="sxs-lookup"><span data-stu-id="c10ad-111">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="c10ad-112">В некоторых случаях необходимо установить локальную службу, чтобы убедиться в том, что безопасность служб сохраняется.</span><span class="sxs-lookup"><span data-stu-id="c10ad-112">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

## <span data-ttu-id="c10ad-113">Параметры меню консоли Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="c10ad-113">Application Virtualization Sequencer Console Menu Options</span></span>


<span data-ttu-id="c10ad-114">Следующие элементы меню доступны на консоли секвенсора App-V:</span><span class="sxs-lookup"><span data-stu-id="c10ad-114">The following menu items are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="c10ad-115">**Файл**— в нем содержатся различные команды, помогающие создавать, открывать, изменять и сохранять последовательное приложения.</span><span class="sxs-lookup"><span data-stu-id="c10ad-115">**File**—Contains various commands to help create, open, modify, and save sequenced applications.</span></span>

-   <span data-ttu-id="c10ad-116">**Редактирование**— включает различные команды для редактирования существующих виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="c10ad-116">**Edit**—Contains various commands for editing existing virtual applications.</span></span>

-   <span data-ttu-id="c10ad-117">**Представление**— в нем содержатся различные команды для просмотра свойств виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="c10ad-117">**View**—Contains various commands for viewing properties of a virtual application.</span></span>

-   <span data-ttu-id="c10ad-118">**Инструменты**— содержат различные инструменты и диагностику для настройки виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="c10ad-118">**Tools**—Contains various tools and diagnostics for configuring virtual applications.</span></span>

## <span data-ttu-id="c10ad-119">Параметры панели инструментов консоли Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="c10ad-119">Application Virtualization Sequencer Console Toolbar Options</span></span>


<span data-ttu-id="c10ad-120">На консоли App-V Sequencer доступны следующие кнопки на панели инструментов:</span><span class="sxs-lookup"><span data-stu-id="c10ad-120">The following toolbar buttons are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="c10ad-121">**Новый пакет**— щелкните, чтобы создать новое упорядоченное приложение.</span><span class="sxs-lookup"><span data-stu-id="c10ad-121">**New Package**—Click to create a new sequenced application.</span></span>

-   <span data-ttu-id="c10ad-122">**Открыть**— щелкните, чтобы открыть пакет последовательных приложений на консоли секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="c10ad-122">**Open**—Click to open a sequenced application package in the App-V Sequencer Console.</span></span>

-   <span data-ttu-id="c10ad-123">**Откройте для обновления**и щелкните, чтобы открыть последовательное приложение, чтобы обновить или применить обновление.</span><span class="sxs-lookup"><span data-stu-id="c10ad-123">**Open for Upgrade**—Click to open a sequenced application to upgrade or apply an update.</span></span>

-   <span data-ttu-id="c10ad-124">**Сохранить**— щелкните, чтобы сохранить виртуализированное виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="c10ad-124">**Save**—Click to save a sequenced virtual application.</span></span>

-   <span data-ttu-id="c10ad-125">**Мастер последовательностей**— щелкните, чтобы открыть мастер упорядочения.</span><span class="sxs-lookup"><span data-stu-id="c10ad-125">**Sequencing Wizard**—Click to open the Sequencing Wizard.</span></span> <span data-ttu-id="c10ad-126">Если вы вносите изменения на вкладке " **Общие** " в разделе Параметры **меню "Сервис**", вы должны использовать эту кнопку для запуска мастера упорядочивания  /  **Options**.</span><span class="sxs-lookup"><span data-stu-id="c10ad-126">You should use this button to start the Sequencing Wizard if you make any changes on the **General** tab under **Tools** / **Options**.</span></span>

## <span data-ttu-id="c10ad-127">Вкладки виртуальных приложений</span><span class="sxs-lookup"><span data-stu-id="c10ad-127">Virtual Application Tabs</span></span>


<span data-ttu-id="c10ad-128">При просмотре виртуального приложения на консоли секвенсора App-V отображаются следующие вкладки:</span><span class="sxs-lookup"><span data-stu-id="c10ad-128">The following tabs are displayed when you view a virtual application in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="c10ad-129">**Свойства**— отображает сведения о выбранном виртуальном приложении.</span><span class="sxs-lookup"><span data-stu-id="c10ad-129">**Properties**—Displays information about the selected virtual application.</span></span> <span data-ttu-id="c10ad-130">Вы можете изменить **имя пакета** и **Комментарии** , связанные с виртуальным приложением.</span><span class="sxs-lookup"><span data-stu-id="c10ad-130">You can update the **Package Name** and **Comments** associated with the virtual application.</span></span>

-   <span data-ttu-id="c10ad-131">**Развертывание**— отображает сведения о том, как целевые компьютеры будут получать доступ к виртуальному приложению.</span><span class="sxs-lookup"><span data-stu-id="c10ad-131">**Deployment**—Displays information about how the virtual application will be accessed by target computers.</span></span> <span data-ttu-id="c10ad-132">Вы можете настроить метод доставки виртуальных приложений, и вы можете настроить, какие операционные системы должны выполняться на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="c10ad-132">You can configure the virtual application delivery method, and you can configure which operating systems must be running on the target computer.</span></span> <span data-ttu-id="c10ad-133">Вы также можете настроить соответствующие параметры вывода.</span><span class="sxs-lookup"><span data-stu-id="c10ad-133">You can also configure the associated output options.</span></span> <span data-ttu-id="c10ad-134">Если вы планируете клиентам получать доступ к виртуальному приложению из файла, используйте следующий формат при указании пути: **File://Server/Share/Path/.SFT**.</span><span class="sxs-lookup"><span data-stu-id="c10ad-134">If you plan to have clients access a virtual application from a file, use the following format when specifying the path: **File://server/share/path/.sft**.</span></span> <span data-ttu-id="c10ad-135">Установите флажок **применять дескрипторы безопасности** , чтобы сохранить безопасность, связанную с пакетом, во время обновления, или разрешения будут сброшены во время обновления.</span><span class="sxs-lookup"><span data-stu-id="c10ad-135">Select **Enforce Security Descriptors** to preserve security associated with the package during an upgrade, or the permissions will be reset during the upgrade.</span></span>

-   <span data-ttu-id="c10ad-136">**Журнал изменений**— отображает сведения об обновлениях, внесенных в виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="c10ad-136">**Change History**—Displays information about updates that have been made to the virtual application.</span></span>

-   <span data-ttu-id="c10ad-137">**Файлы**— отображает файлы, связанные с выбранным виртуальным приложением.</span><span class="sxs-lookup"><span data-stu-id="c10ad-137">**Files**—Displays the files associated with the selected virtual application.</span></span> <span data-ttu-id="c10ad-138">Вы можете вносить небольшие изменения в связанные свойства файла с помощью соответствующих полей.</span><span class="sxs-lookup"><span data-stu-id="c10ad-138">You can make minor revisions to the associated file properties by using the appropriate fields.</span></span>

-   <span data-ttu-id="c10ad-139">**Виртуальный реестр**— отображает виртуальный реестр, связанный с выбранным виртуальным приложением.</span><span class="sxs-lookup"><span data-stu-id="c10ad-139">**Virtual Registry**—Displays the virtual registry associated with the selected virtual application.</span></span> <span data-ttu-id="c10ad-140">Вы можете добавить или удалить разделы реестра, щелкнув соответствующую запись правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="c10ad-140">You can add or delete registry keys by right-clicking the appropriate entry.</span></span>

-   <span data-ttu-id="c10ad-141">**Виртуальная файловая система**— отображает виртуальные файловые системы, связанные с выбранным виртуальным приложением.</span><span class="sxs-lookup"><span data-stu-id="c10ad-141">**Virtual File System**—Displays the virtual file systems associated with the selected virtual application.</span></span> <span data-ttu-id="c10ad-142">Вы можете добавить, удалить или изменить элементы файловой системы на этой вкладке, щелкнув соответствующую запись правой кнопкой мыши и выбрав нужный параметр.</span><span class="sxs-lookup"><span data-stu-id="c10ad-142">You can add, delete, or edit file system entries on this tab by right-clicking the appropriate entry and selecting the option.</span></span>

-   <span data-ttu-id="c10ad-143">**Виртуальные службы**— отображает службы, связанные с выбранным виртуальным приложением.</span><span class="sxs-lookup"><span data-stu-id="c10ad-143">**Virtual Services**—Displays the services associated with the selected virtual application.</span></span>

-   <span data-ttu-id="c10ad-144">**OSD**— отображает сведения об открытом дескрипторе программного обеспечения (OSD), связанном с виртуальным приложением.</span><span class="sxs-lookup"><span data-stu-id="c10ad-144">**OSD**—Displays information about the Open Software Descriptor (OSD) associated with the virtual application.</span></span> <span data-ttu-id="c10ad-145">Вы можете обновить файлы, связанные с OSD-файлом, щелкнув соответствующую запись правой кнопкой мыши и выбрав нужное действие.</span><span class="sxs-lookup"><span data-stu-id="c10ad-145">You can update the files associated with the OSD file by right-clicking the appropriate entry and selecting the action that you want.</span></span>

## <span data-ttu-id="c10ad-146">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c10ad-146">Related topics</span></span>


[<span data-ttu-id="c10ad-147">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="c10ad-147">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





