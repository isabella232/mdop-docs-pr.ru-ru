---
title: Обзор сценария на основе электронного распространения программного обеспечения
description: Обзор сценария на основе электронного распространения программного обеспечения
author: dansimp
ms.assetid: e9e94b8a-6cba-4de8-9b57-73897796b6a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cfbdf40f5ac0f61721c05d0da5cd49e910b16154
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821599"
---
# <span data-ttu-id="a181f-103">Обзор сценария на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="a181f-103">Electronic Software Distribution-Based Scenario Overview</span></span>


<span data-ttu-id="a181f-104">Если вы планируете использовать электронное распространение программного обеспечения (ESD) для развертывания виртуальных приложений, важно понимать факторы, в которых они распространяются, и которые затрагиваются этим решением.</span><span class="sxs-lookup"><span data-stu-id="a181f-104">If you plan to use an electronic software distribution (ESD) solution to deploy virtual applications, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="a181f-105">В этой статье описаны преимущества использования сценария на основе ESD и содержатся сведения о методах публикации и потоковой передачи, которые необходимо принять во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="a181f-105">This topic describes the benefits of using an ESD-based scenario and provides information about the publishing and package streaming methods that you will need to consider as you proceed with your deployment.</span></span>

<span data-ttu-id="a181f-106">**Важно!**  Если вы используете какое бы то или недействительное решение, вам необходимо ознакомиться с требованиями, предъявляемыми конкретным решением.</span><span class="sxs-lookup"><span data-stu-id="a181f-106">**Important** Whichever ESD solution you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="a181f-107">Если вы используете Диспетчер конфигураций конечных точек Microsoft, ознакомьтесь с документацией по Configuration Manager по адресу <https://go.microsoft.com/fwlink/?LinkId=66999> .</span><span class="sxs-lookup"><span data-stu-id="a181f-107">If you are using Microsoft Endpoint Configuration Manager, see the Configuration Manager documentation at <https://go.microsoft.com/fwlink/?LinkId=66999>.</span></span>

 

<span data-ttu-id="a181f-108">Использование существующей системы ESD обеспечивает следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="a181f-108">Using an existing ESD system provides you with the following benefits:</span></span>

-   <span data-ttu-id="a181f-109">Исключает инфраструктуры двух систем управления</span><span class="sxs-lookup"><span data-stu-id="a181f-109">Eliminates dual management infrastructures</span></span>

-   <span data-ttu-id="a181f-110">Сокращает стоимость дополнительного оборудования</span><span class="sxs-lookup"><span data-stu-id="a181f-110">Reduces the cost of additional hardware</span></span>

-   <span data-ttu-id="a181f-111">Сокращает стоимость дополнительных лицензий на операционную систему и базу данных.</span><span class="sxs-lookup"><span data-stu-id="a181f-111">Reduces the cost of additional operating system and database licenses</span></span>

## <span data-ttu-id="a181f-112">Методы публикации</span><span class="sxs-lookup"><span data-stu-id="a181f-112">Publishing Methods</span></span>


<span data-ttu-id="a181f-113">При использовании сценария на основе ESD вы можете опубликовать приложение для клиентов.</span><span class="sxs-lookup"><span data-stu-id="a181f-113">When using an ESD-based scenario, you have the following choices for publishing the application to the clients:</span></span>

-   **<span data-ttu-id="a181f-114">Самостоятельный установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="a181f-114">Stand-alone Windows Installer.</span></span>** <span data-ttu-id="a181f-115">Файл установщика Windows включает манифест и OSD-и ICO-файлы, используемые клиентами для настройки пакета.</span><span class="sxs-lookup"><span data-stu-id="a181f-115">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="a181f-116">Файл установщика Windows также копирует SFT-файл в клиент, так как этот сценарий не использует сервер.</span><span class="sxs-lookup"><span data-stu-id="a181f-116">The Windows Installer file also copies the SFT file to the client because this scenario does not use a server.</span></span>

-   **<span data-ttu-id="a181f-117">Установщик Windows с манифестом пакета.</span><span class="sxs-lookup"><span data-stu-id="a181f-117">Windows Installer with the package manifest.</span></span>** <span data-ttu-id="a181f-118">Файл установщика Windows включает манифест и OSD-и ICO-файлы, используемые клиентами для настройки пакета.</span><span class="sxs-lookup"><span data-stu-id="a181f-118">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="a181f-119">SFT-файл хранится на сервере.</span><span class="sxs-lookup"><span data-stu-id="a181f-119">The SFT file is stored on a server.</span></span> <span data-ttu-id="a181f-120">Параметр командной строки направляет клиенту расположение SFT-файла.</span><span class="sxs-lookup"><span data-stu-id="a181f-120">A command-line parameter directs the client to the location of the SFT file.</span></span>

-   **<span data-ttu-id="a181f-121">Команды SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="a181f-121">SFTMIME commands.</span></span>** <span data-ttu-id="a181f-122">Команды SFTMIME используются для файлов манифеста, OSD, ICO и SFT для добавления пакетов в клиент.</span><span class="sxs-lookup"><span data-stu-id="a181f-122">SFTMIME commands are used with the manifest, OSD, ICO, and SFT files to add packages to the client.</span></span> <span data-ttu-id="a181f-123">Файл манифеста должен быть на клиентском компьютере, или он должен быть доступен через путь UNC.</span><span class="sxs-lookup"><span data-stu-id="a181f-123">The manifest file must be on the client computer, or it must be accessible through a UNC path.</span></span> <span data-ttu-id="a181f-124">В зависимости от конфигурации клиента и параметров командной строки, файлы OSD, ICO и SFT могут находиться на клиентском компьютере или на сервере.</span><span class="sxs-lookup"><span data-stu-id="a181f-124">Depending on the client configuration and the command-line options, the OSD, ICO, and SFT files can be on the client computer or on a server.</span></span>

<span data-ttu-id="a181f-125">Более подробные сведения об описанных выше методах публикации можно найти в разделе [Определение способа публикации](determine-your-publishing-method.md).</span><span class="sxs-lookup"><span data-stu-id="a181f-125">For more detailed information about the preceding publishing methods, see [Determine Your Publishing Method](determine-your-publishing-method.md).</span></span>

## <span data-ttu-id="a181f-126">Методы потоковой передачи пакетов</span><span class="sxs-lookup"><span data-stu-id="a181f-126">Package Streaming Methods</span></span>


<span data-ttu-id="a181f-127">Вам потребуется определить метод, который будет использоваться системой виртуализации приложений для потоковой передачи виртуальных пакетов приложений или SFT файлов с сервера на клиентские компьютеры.</span><span class="sxs-lookup"><span data-stu-id="a181f-127">You will need to determine the method your Application Virtualization System will use to stream the virtual application packages, or SFT files, from the server to the clients.</span></span> <span data-ttu-id="a181f-128">Доступны следующие параметры потоковой передачи:</span><span class="sxs-lookup"><span data-stu-id="a181f-128">The following streaming options are available:</span></span>

-   **<span data-ttu-id="a181f-129">Потоковый сервер Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="a181f-129">Application Virtualization Streaming Server.</span></span>** <span data-ttu-id="a181f-130">Если в конфигурации используется потоковый сервер Application Virtualization, SFT файлы будут переносятся на клиентские компьютеры с сервера, использующего протоколы RTSP или RTSP.</span><span class="sxs-lookup"><span data-stu-id="a181f-130">If you use an Application Virtualization Streaming Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="a181f-131">Вы должны установить программное обеспечение сервера на компьютере, и вы должны настроить его в реестре, но эта конфигурация не зависит от таких служб, как SQL или доменные службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a181f-131">You must install the server software on a computer and you must configure it through the registry, but this configuration does not depend on services such as SQL or Active Directory Domain Services.</span></span> <span data-ttu-id="a181f-132">SFT-файлы хранятся на сервере в расположении, доступном для клиентов.</span><span class="sxs-lookup"><span data-stu-id="a181f-132">The SFT files are stored on the server at a location accessible by the clients.</span></span> <span data-ttu-id="a181f-133">Сведения о публикации могут распространяться между клиентами с помощью любого механизма распространения.</span><span class="sxs-lookup"><span data-stu-id="a181f-133">Publishing information can be distributed to the clients through any distribution mechanism.</span></span> <span data-ttu-id="a181f-134">Однако при настройке клиент получает обновления пакетов автоматически и поддерживается активное обновление.</span><span class="sxs-lookup"><span data-stu-id="a181f-134">However, when configured, the client receives package upgrades automatically and active upgrade is supported.</span></span>

-   **<span data-ttu-id="a181f-135">Сервер управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="a181f-135">Application Virtualization Management Server.</span></span>** <span data-ttu-id="a181f-136">Если вы используете сервер управления виртуализацией приложений в конфигурации, SFT файлы будут переносятся на клиентские компьютеры с сервера, использующего протоколы RTSP или RTSP.</span><span class="sxs-lookup"><span data-stu-id="a181f-136">If you use an Application Virtualization Management Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="a181f-137">Управление сервером осуществляется с помощью консоли управления Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="a181f-137">You manage this server through the Application Virtualization Management Console.</span></span> <span data-ttu-id="a181f-138">В этой конфигурации используются база данных SQL и службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a181f-138">This configuration uses a SQL database and Active Directory services.</span></span> <span data-ttu-id="a181f-139">Сервер может распространять сведения о публикации клиентам, поэтому дополнительные механизмы публикации не требуются.</span><span class="sxs-lookup"><span data-stu-id="a181f-139">The server can distribute publishing information to the clients, so additional publishing mechanisms are not needed.</span></span>

-   **<span data-ttu-id="a181f-140">Файлового сервера.</span><span class="sxs-lookup"><span data-stu-id="a181f-140">File server.</span></span>** <span data-ttu-id="a181f-141">Если вы используете файловый сервер в конфигурации, SFT-файлы переносятся на другие клиентские компьютеры с помощью протоколов SMB.</span><span class="sxs-lookup"><span data-stu-id="a181f-141">If you use a file server in your configuration, the SFT files are streamed to the other client computers by using SMB protocols.</span></span> <span data-ttu-id="a181f-142">Файловые серверы, используемые в этой конфигурации, управляются путем создания списков управления доступом (ACL) для файлов общих папок и SFT-файлов.</span><span class="sxs-lookup"><span data-stu-id="a181f-142">File servers used in this configuration are managed by creating access control lists (ACLs) on the file shares and SFT files.</span></span> <span data-ttu-id="a181f-143">Будьте внимательны, чтобы направить клиентам необходимые файлы на файловом сервере.</span><span class="sxs-lookup"><span data-stu-id="a181f-143">Care must be taken to direct the clients to the correct files on the file server.</span></span>

-   **<span data-ttu-id="a181f-144">Сервер IIS.</span><span class="sxs-lookup"><span data-stu-id="a181f-144">IIS server.</span></span>** <span data-ttu-id="a181f-145">Если вы используете сервер IIS в конфигурации, SFT-файлы передаются клиентам с этого сервера через протоколы HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a181f-145">If you use an IIS server in your configuration, the SFT files are streamed to the clients from that server using HTTP or HTTPS protocols.</span></span> <span data-ttu-id="a181f-146">Сервер IIS легко настраивать и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="a181f-146">The IIS server is easy to configure and manage.</span></span> <span data-ttu-id="a181f-147">Будьте внимательны, чтобы направить клиентов на нужные файлы на сервере IIS.</span><span class="sxs-lookup"><span data-stu-id="a181f-147">Care must be taken to direct the clients to the correct files on the IIS server.</span></span>

<span data-ttu-id="a181f-148">Более подробные сведения об описанных выше потоковых методах можно найти в разделе [Определение потокового метода](determine-your-streaming-method.md).</span><span class="sxs-lookup"><span data-stu-id="a181f-148">For more detailed information about the preceding streaming methods, see [Determine Your Streaming Method](determine-your-streaming-method.md).</span></span>

## <span data-ttu-id="a181f-149">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a181f-149">Related topics</span></span>


[<span data-ttu-id="a181f-150">Параметры командной строки установщика клиента Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="a181f-150">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="a181f-151">Сценарий на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="a181f-151">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="a181f-152">Определение способа публикации</span><span class="sxs-lookup"><span data-stu-id="a181f-152">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="a181f-153">Определение способа потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="a181f-153">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="a181f-154">Сценарий на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="a181f-154">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="a181f-155">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="a181f-155">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





