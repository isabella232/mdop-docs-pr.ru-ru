---
title: Настройка серверов Application Virtualization Management Server
description: Настройка серверов Application Virtualization Management Server
author: dansimp
ms.assetid: a9f96148-bf2d-486f-98c2-23409bfb0935
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6d54dd213efb8d5cbff5d0e730e6dc08c8d19b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817842"
---
# <span data-ttu-id="8328d-103">Настройка серверов Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="8328d-103">How to Configure the Application Virtualization Management Servers</span></span>


<span data-ttu-id="8328d-104">Перед тем, как виртуализированные приложения будут передаваться в клиентское приложение Application Virtualization или клиент для служб удаленных рабочих столов (ранее — службы терминалов), необходимо настроить сервер управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="8328d-104">Before virtualized applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Management Server must be configured.</span></span> <span data-ttu-id="8328d-105">При настройке сервера вы настраиваете *каталог содержимого* , в котором загружаются и сохраняются файлы SFT.</span><span class="sxs-lookup"><span data-stu-id="8328d-105">When you configure the server, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="8328d-106">SFT-файлы содержат виртуализированное приложение (или приложения).</span><span class="sxs-lookup"><span data-stu-id="8328d-106">The SFT files contain the virtualized application (or applications).</span></span>

<span data-ttu-id="8328d-107">**Важно!**  Серверы Application Virtualization поменяют SFT на Настольный клиент и клиент для служб удаленных рабочих столов, используя только протоколы RTSP или RTSP.</span><span class="sxs-lookup"><span data-stu-id="8328d-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="8328d-108">Файл ICO (значок) и файл OSD (открыть программный дескриптор) можно настроить для потоковой передачи с другого файла или HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="8328d-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="8328d-109">Настройка сервера управления виртуализацией приложений</span><span class="sxs-lookup"><span data-stu-id="8328d-109">To configure the Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="8328d-110">Выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8328d-110">Complete the following procedure:</span></span>

    [<span data-ttu-id="8328d-111">Установка сервера Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="8328d-111">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="8328d-112">**Примечание**  Во время процедуры установки вы указываете расположение каталога \\Content на экране " **путь к содержимому** ".</span><span class="sxs-lookup"><span data-stu-id="8328d-112">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="8328d-113">Перейдите в расположение, указанное для каталога \\Content, и при необходимости создайте каталог.</span><span class="sxs-lookup"><span data-stu-id="8328d-113">Navigate to the location that you specified for the \\Content directory, and if necessary, create the directory.</span></span>

3.  <span data-ttu-id="8328d-114">Когда создается каталог содержимого, настройте этот каталог как стандартный файловый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="8328d-114">When the content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="8328d-115">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8328d-115">Related topics</span></span>


[<span data-ttu-id="8328d-116">Сценарий на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="8328d-116">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="8328d-117">Требования к системе при работе с Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8328d-117">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="8328d-118">Сценарий на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="8328d-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="8328d-119">Настройка серверов для развертывания на основе сервера</span><span class="sxs-lookup"><span data-stu-id="8328d-119">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 





