---
title: Настройка файлового сервера
description: Настройка файлового сервера
author: dansimp
ms.assetid: 0977554c-1741-411b-85e7-7e1cd017542f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a8971ad5c9f83dec4d0c77a16f1093ef7026b5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817782"
---
# <span data-ttu-id="4957e-103">Настройка файлового сервера</span><span class="sxs-lookup"><span data-stu-id="4957e-103">How to Configure the File Server</span></span>


<span data-ttu-id="4957e-104">Вы можете использовать описанную ниже процедуру для настройки локального компьютера, который используется в качестве общего файлового файла и для потоковой обработки приложений в классическом клиенте Application Virtualization и клиенте для служб удаленных рабочих столов (ранее служб терминалов).</span><span class="sxs-lookup"><span data-stu-id="4957e-104">You can use the following procedure to configure a local computer that is used as a file share and streams applications to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="4957e-105">Этот сценарий используется в том случае, если вы не хотите добавлять дополнительную серверную инфраструктуру в существующую аппаратную среду.</span><span class="sxs-lookup"><span data-stu-id="4957e-105">This scenario is used when you do not want to add an additional server infrastructure to your existing hardware environment.</span></span>

<span data-ttu-id="4957e-106">Если вы используете сервер управления виртуализацией приложений в качестве точки распространения для общей папки, установленной в локальных офисах, необходимо настроить этот сервер, прежде чем виртуальные приложения смогут передаваться на компьютеры, которые используются в качестве файловых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4957e-106">If you are using an Application Virtualization Management Server as a distribution point to the file share installed in local offices, you must configure this server before virtual applications can be streamed to the computers that are used as file shares.</span></span> <span data-ttu-id="4957e-107">При настройке серверов и общих файловых ресурсов настраивается каталог содержимого, в котором загружаются и сохраняются файлы SFT.</span><span class="sxs-lookup"><span data-stu-id="4957e-107">When you configure the servers and the file shares, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="4957e-108">SFT-файлы содержат виртуальное приложение (или приложения).</span><span class="sxs-lookup"><span data-stu-id="4957e-108">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="4957e-109">**Важно!**  Чтобы приложения правильно переносились в классическое приложение Application Virtualization и клиент для служб удаленных рабочих столов, вы создаете потоки файлов SFT из каталога содержимого на сервере, где вы хотите сохранить виртуальное приложение. файл ICO (значок) и файл OSD (открыть программный дескриптор) можно настроить для потоковой передачи с другого сервера.</span><span class="sxs-lookup"><span data-stu-id="4957e-109">**Important** For applications to stream properly to the Application Virtualization Desktop Client and the Client for Remote Desktop Services, the SFT file streams from the content directory on the server where you store the virtual application; the ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different server.</span></span>

 

**<span data-ttu-id="4957e-110">Настройка файлового сервера виртуализации приложений</span><span class="sxs-lookup"><span data-stu-id="4957e-110">To configure the Application Virtualization file server</span></span>**

1.  <span data-ttu-id="4957e-111">Выполните описанную ниже процедуру установки, чтобы настроить сервер, который используется в качестве точки распространения.</span><span class="sxs-lookup"><span data-stu-id="4957e-111">Complete the following installation procedure to configure the server that is used as the distribution point:</span></span>

    [<span data-ttu-id="4957e-112">Установка сервера Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="4957e-112">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="4957e-113">**Примечание**  Во время процедуры установки вы указываете расположение каталога \\Content на экране " **путь к содержимому** ".</span><span class="sxs-lookup"><span data-stu-id="4957e-113">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="4957e-114">Создайте каталог \\Content, соответствующий каталогу, который вы указали при установке сервера, на каждом компьютере, который используется в качестве общего файла.</span><span class="sxs-lookup"><span data-stu-id="4957e-114">Create a \\Content directory, which corresponds to the directory you specified when you installed the server, on each computer that you are using as a file share.</span></span>

    <span data-ttu-id="4957e-115">**Важно!**  Настройте клиентские компьютеры Application Virtualization для потоковой передачи приложений с компьютера, который используется в качестве общего файлового файла, а не с сервера Application Virtualization или IIS Server.</span><span class="sxs-lookup"><span data-stu-id="4957e-115">**Important** Configure the Application Virtualization Desktop Clients to stream applications from the computer you are using as a file share rather than from an Application Virtualization Server or IIS server.</span></span>

     

3.  <span data-ttu-id="4957e-116">После создания каталога \\Content настройте этот каталог как стандартный файловый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="4957e-116">When the \\Content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="4957e-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4957e-117">Related topics</span></span>


[<span data-ttu-id="4957e-118">Сценарий на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="4957e-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="4957e-119">Сценарий на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="4957e-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="4957e-120">Настройка серверов Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="4957e-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="4957e-121">Настройка серверов Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="4957e-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="4957e-122">Настройка сервера для служб IIS</span><span class="sxs-lookup"><span data-stu-id="4957e-122">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





