---
title: Сведения о пакетах Application Virtualization
description: Сведения о пакетах Application Virtualization
author: dansimp
ms.assetid: 69bd35c1-7af3-43db-931b-3074780aa926
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfe6df90881ea4179fa8cd224609ca6d28ff5f61
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820082"
---
# <span data-ttu-id="9f033-103">Сведения о пакетах Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="9f033-103">About Application Virtualization Packages</span></span>


<span data-ttu-id="9f033-104">В Application Virtualization *Package* — это результат процесса упорядочения.</span><span class="sxs-lookup"><span data-stu-id="9f033-104">In Application Virtualization, a *package* is the output of the sequencing process.</span></span> <span data-ttu-id="9f033-105">Пакеты используются при первом развертывании приложений на серверах и при обновлении приложений с помощью новой версии.</span><span class="sxs-lookup"><span data-stu-id="9f033-105">You use packages when you first deploy applications on your servers and when you upgrade applications with a new version.</span></span> <span data-ttu-id="9f033-106">Пакеты позволяют управлять версиями виртуальных приложений на серверах управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="9f033-106">Packages enable you to control virtual application versions on your Application Virtualization Management Servers.</span></span> <span data-ttu-id="9f033-107">Один пакет может содержать одно или несколько приложений.</span><span class="sxs-lookup"><span data-stu-id="9f033-107">A single package can contain one or more applications.</span></span> <span data-ttu-id="9f033-108">Каждый пакет приложения содержит набор файлов как самостоятельный блок.</span><span class="sxs-lookup"><span data-stu-id="9f033-108">Each application package contains a set of files as a self-contained unit.</span></span>

## <span data-ttu-id="9f033-109">Управление пакетами</span><span class="sxs-lookup"><span data-stu-id="9f033-109">Managing Packages</span></span>


<span data-ttu-id="9f033-110">После того как секвенсор создаст пакет из одного или нескольких приложений как часть его процесса, вы можете скопировать созданные программой Sequencer файлы на сервер управления виртуализацией приложений и сделать их доступными для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="9f033-110">After the Sequencer creates a package of one or more applications as part of its process, you can copy the Sequencer-generated files to a Application Virtualization Management Server and make them available for streaming.</span></span>

<span data-ttu-id="9f033-111">Доступные пакеты отображаются в контейнере **пакеты** в левой области консоли управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="9f033-111">Available packages appear under the **Packages** container in the left pane of the Application Virtualization Management Console.</span></span> <span data-ttu-id="9f033-112">При импорте приложения с помощью файла проекта секвенсора (SPRJ) или открытого файла программного дескриптора (OSD) соответствующая запись появится в контейнере **Packages (пакеты** ).</span><span class="sxs-lookup"><span data-stu-id="9f033-112">When you import an application with a Sequencer Project (SPRJ) file or an Open Software Descriptor (OSD) file, a related entry appears in the **Packages** container.</span></span> <span data-ttu-id="9f033-113">С помощью консоли управления сервером виртуализации приложений вы можете развертывать, обновлять и удалять пакеты и их версии.</span><span class="sxs-lookup"><span data-stu-id="9f033-113">From the Application Virtualization Server Management Console, you can then deploy, upgrade, or delete packages and versions of them.</span></span>

<span data-ttu-id="9f033-114">У каждого виртуального приложения есть связанный пакет.</span><span class="sxs-lookup"><span data-stu-id="9f033-114">Each virtual application has an associated package.</span></span> <span data-ttu-id="9f033-115">Этот пакет содержит следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="9f033-115">This package includes the following files:</span></span>

-   <span data-ttu-id="9f033-116">SFT — файл, который пересылает приложение клиентам.</span><span class="sxs-lookup"><span data-stu-id="9f033-116">SFT—The file that streams the application to clients.</span></span>

-   <span data-ttu-id="9f033-117">OSD — открытый файл дескриптора программного обеспечения содержат сведения, необходимые для поиска и запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="9f033-117">OSD—The Open Software Descriptor file contains the information needed to find and launch the application.</span></span>

-   <span data-ttu-id="9f033-118">ICO — файл значка, который визуально представляет приложение в пользовательском интерфейсе и сочетаниях клавиш.</span><span class="sxs-lookup"><span data-stu-id="9f033-118">ICO—The icon file that visually represents the application in user interfaces and shortcuts.</span></span>

-   <span data-ttu-id="9f033-119">SPRJ — файл проекта секвенсора.</span><span class="sxs-lookup"><span data-stu-id="9f033-119">SPRJ—The Sequencer Project file.</span></span>

<span data-ttu-id="9f033-120">При импорте файла SPRJ все последовательные приложения доступны для развертывания по умолчанию, но приложения не включены для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="9f033-120">When you import the SPRJ file, all sequenced applications are available for deployment, by default, but the applications are not enabled for streaming.</span></span> <span data-ttu-id="9f033-121">Вы можете выбрать потоковую передачу всех или некоторых приложений в пакете.</span><span class="sxs-lookup"><span data-stu-id="9f033-121">You can choose to stream all or some of the applications in the package.</span></span> <span data-ttu-id="9f033-122">Например, если вы попланируете и импортировали Microsoft Office, вы можете отказаться от развертывания некоторых приложений, например мастера сохранения личных настроек.</span><span class="sxs-lookup"><span data-stu-id="9f033-122">For example, if you sequenced and imported Microsoft Office, you can choose not to deploy some applications, such as the Save My Settings Wizard.</span></span> <span data-ttu-id="9f033-123">В этом случае щелкните правой кнопкой мыши каждое приложение, которое вы хотите развернуть, выберите пункт **Свойства**и убедитесь, что флажок **включено** (пусто).</span><span class="sxs-lookup"><span data-stu-id="9f033-123">In this case, right-click each application you want to deploy, choose **Properties**, and make sure that the **Enabled** box is cleared (blank).</span></span> <span data-ttu-id="9f033-124">На клиентские компьютеры будут переделены только приложения с установленным флажком " **включено** ".</span><span class="sxs-lookup"><span data-stu-id="9f033-124">Only the applications with the **Enabled** box selected will stream to client computers.</span></span>

<span data-ttu-id="9f033-125">После переупорядочения пакета и создания нового SFT-файла для потоковой передачи данных вы можете быстро и легко обновить старый пакет с помощью консоли управления сервером Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="9f033-125">After you resequence a package and produce a new SFT file for streaming, you can upgrade the old package quickly and easily through the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="9f033-126">Единственный рабочий сценарий, в котором вам нужно использовать узел **packages** , — это указать новую версию (файл SFT) для пакета.</span><span class="sxs-lookup"><span data-stu-id="9f033-126">The only operational scenario that requires you to use the **Packages** node is when you introduce a new version (SFT file) for the package.</span></span> <span data-ttu-id="9f033-127">Каждый раз, когда вы импортируете приложения, назначаете доступ к приложениям, а также другие лицензии, система Application Virtualization отслеживает эти данные на уровне пакета.</span><span class="sxs-lookup"><span data-stu-id="9f033-127">Whenever you import applications, assign access and licenses to applications, and so on, the Application Virtualization System tracks this information at the package level.</span></span> <span data-ttu-id="9f033-128">Это означает, что если вы решите пользователю использовать приложение, вы предоставляете пользователю разрешение на запуск приложения в том же пакете.</span><span class="sxs-lookup"><span data-stu-id="9f033-128">This means that when you authorize a user to use an application, you are giving the user permission to run any application in the same package.</span></span>

### <span data-ttu-id="9f033-129">Версия пакета</span><span class="sxs-lookup"><span data-stu-id="9f033-129">Package Version</span></span>

<span data-ttu-id="9f033-130">Версия пакета представлена определенным SFT-файлом.</span><span class="sxs-lookup"><span data-stu-id="9f033-130">A package version is represented by a specific SFT file.</span></span> <span data-ttu-id="9f033-131">При обновлении пакета (применение обновления к приложению или добавлении приложения в пакет) создается новый SFT-файл.</span><span class="sxs-lookup"><span data-stu-id="9f033-131">When you upgrade a package (apply an update to an application or add an application to a package), you generate a new SFT file.</span></span> <span data-ttu-id="9f033-132">Каждый раз, когда вы создаете новый файл SFT, вы создаете новую версию пакета.</span><span class="sxs-lookup"><span data-stu-id="9f033-132">Each time you create a new SFT file, you are creating a new package version.</span></span>

<span data-ttu-id="9f033-133">При импорте приложений с помощью консоли управления сервером Application Virtualization программа автоматически создает пакет и версию пакета, если они еще не установлены.</span><span class="sxs-lookup"><span data-stu-id="9f033-133">When you import applications through the Application Virtualization Server Management Console, the software automatically creates a package and a package version if they do not already exist.</span></span>

## <span data-ttu-id="9f033-134">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9f033-134">Related topics</span></span>


[<span data-ttu-id="9f033-135">Сведения о приложениях Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="9f033-135">About Application Virtualization Applications</span></span>](about-application-virtualization-applications.md)

[<span data-ttu-id="9f033-136">Сведения о консоли управления серверами Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="9f033-136">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="9f033-137">Управление пакетами на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="9f033-137">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





