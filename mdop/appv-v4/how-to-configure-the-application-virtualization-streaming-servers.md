---
title: Настройка серверов Application Virtualization Streaming Server
description: Настройка серверов Application Virtualization Streaming Server
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817822"
---
# <span data-ttu-id="e9c3e-103">Настройка серверов Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="e9c3e-103">How to Configure the Application Virtualization Streaming Servers</span></span>


<span data-ttu-id="e9c3e-104">Прежде чем виртуальные приложения можно будет передаваться в клиентское приложение Application Virtualization или клиент для служб удаленных рабочих столов (ранее — службы терминалов), необходимо настроить серверы потоковой виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="e9c3e-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Streaming Servers must be configured.</span></span> <span data-ttu-id="e9c3e-105">При настройке серверов вы настраиваете *каталог содержимого* , в котором загружаются и сохраняются файлы SFT.</span><span class="sxs-lookup"><span data-stu-id="e9c3e-105">When you configure the servers, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="e9c3e-106">SFT-файлы содержат виртуальное приложение (или приложения).</span><span class="sxs-lookup"><span data-stu-id="e9c3e-106">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="e9c3e-107">**Важно!**  Серверы Application Virtualization поменяют SFT на Настольный клиент и клиент для служб удаленных рабочих столов, используя только протоколы RTSP или RTSP.</span><span class="sxs-lookup"><span data-stu-id="e9c3e-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="e9c3e-108">Файл ICO (значок) и файл OSD (открыть программный дескриптор) можно настроить для потоковой передачи с другого файла или HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="e9c3e-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="e9c3e-109">Настройка серверов потоковой передачи Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="e9c3e-109">To configure the Application Virtualization Streaming Servers</span></span>**

1.  <span data-ttu-id="e9c3e-110">Выполните процедуру установки для сервера потоковой передачи Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="e9c3e-110">Complete the installation procedure for the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="e9c3e-111">Во время процедуры установки вы указываете расположение каталога \\Content на экране " **путь к содержимому** ".</span><span class="sxs-lookup"><span data-stu-id="e9c3e-111">During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

2.  <span data-ttu-id="e9c3e-112">Перейдите в расположение, указанное для каталога \\Content, и при необходимости создайте каталог.</span><span class="sxs-lookup"><span data-stu-id="e9c3e-112">Navigate to the location that you specified for the \\Content directory, and if you have to, create the directory.</span></span>

3.  <span data-ttu-id="e9c3e-113">Когда создается каталог содержимого, настройте этот каталог как стандартный файловый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="e9c3e-113">When the Content directory is created, configure this directory as a standard file share.</span></span>

4.  <span data-ttu-id="e9c3e-114">Настройте разрешения файловой системы NTFS для каталога содержимого и папок пакета в каталоге содержимого.</span><span class="sxs-lookup"><span data-stu-id="e9c3e-114">Configure the NTFS file system permissions to the Content directory and the package folders under the Content directory.</span></span> <span data-ttu-id="e9c3e-115">В доменных службах Active Directory следует использовать группы безопасности, определяющие, какие пользователи могут получать доступ к каждому приложению.</span><span class="sxs-lookup"><span data-stu-id="e9c3e-115">You should use Security Groups in Active Directory Domain Services that define which users can access each application.</span></span>

## <span data-ttu-id="e9c3e-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e9c3e-116">Related topics</span></span>


[<span data-ttu-id="e9c3e-117">Сценарий на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="e9c3e-117">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="e9c3e-118">Сценарий на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="e9c3e-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="e9c3e-119">Настройка серверов Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="e9c3e-119">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="e9c3e-120">Настройка файлового сервера</span><span class="sxs-lookup"><span data-stu-id="e9c3e-120">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

[<span data-ttu-id="e9c3e-121">Настройка сервера для служб IIS</span><span class="sxs-lookup"><span data-stu-id="e9c3e-121">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





