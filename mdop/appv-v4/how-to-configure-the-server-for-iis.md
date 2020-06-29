---
title: Настройка сервера для служб IIS
description: Настройка сервера для служб IIS
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817742"
---
# <span data-ttu-id="c41ec-103">Настройка сервера для служб IIS</span><span class="sxs-lookup"><span data-stu-id="c41ec-103">How to Configure the Server for IIS</span></span>


<span data-ttu-id="c41ec-104">Прежде чем виртуальные приложения будут передаваться в клиентское приложение Application Virtualization и клиент для служб удаленных рабочих столов (ранее — службы терминалов), необходимо настроить серверы IIS.</span><span class="sxs-lookup"><span data-stu-id="c41ec-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services), the IIS servers must be configured.</span></span> <span data-ttu-id="c41ec-105">При настройке серверов вы настраиваете каталог содержимого, в котором загружаются и сохраняются файлы SFT.</span><span class="sxs-lookup"><span data-stu-id="c41ec-105">When you configure the servers, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="c41ec-106">SFT-файлы содержат виртуальное приложение (или приложения).</span><span class="sxs-lookup"><span data-stu-id="c41ec-106">The SFT files contain the virtual application (or applications).</span></span>

**<span data-ttu-id="c41ec-107">Настройка каталога содержимого на сервере IIS</span><span class="sxs-lookup"><span data-stu-id="c41ec-107">To configure the content directory on the IIS server</span></span>**

1.  <span data-ttu-id="c41ec-108">На сервере, на котором запущены службы IIS, найдите каталог, который вы хотите использовать в качестве каталога содержимого, или создайте каталог, если он не существует.</span><span class="sxs-lookup"><span data-stu-id="c41ec-108">On the server that is running IIS, locate the directory that you want to use as the content directory, or create the directory if it does not exist.</span></span> <span data-ttu-id="c41ec-109">Настройте этот каталог как стандартный файловый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="c41ec-109">Configure this directory as a standard file share.</span></span>

2.  <span data-ttu-id="c41ec-110">На сервере, на котором запущены службы IIS, откройте **Диспетчер IIS**и на веб-сайте по умолчанию создайте виртуальный каталог, соответствующий каталогу содержимого, созданному на сервере.</span><span class="sxs-lookup"><span data-stu-id="c41ec-110">On the server that is running IIS, open **IIS Manager**, and under the default website, create a virtual directory that corresponds to the content directory that you created on the server.</span></span> <span data-ttu-id="c41ec-111">Убедитесь, что флажок **Read (чтение** ) установлен.</span><span class="sxs-lookup"><span data-stu-id="c41ec-111">Make sure that **Read** is checked.</span></span>

3.  <span data-ttu-id="c41ec-112">Присвойте созданному виртуальному каталогу **содержимое**псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="c41ec-112">Give the newly created virtual directory the alias **Content**.</span></span>

4.  <span data-ttu-id="c41ec-113">Подтвердите все другие параметры по умолчанию для этого виртуального каталога.</span><span class="sxs-lookup"><span data-stu-id="c41ec-113">Accept all other default settings for this virtual directory.</span></span>

5.  <span data-ttu-id="c41ec-114">Настройте разрешения файловой системы NTFS для каталога содержимого и папок пакета в каталоге содержимого с помощью групп безопасности в доменных службах Active Directory, определенных ранее.</span><span class="sxs-lookup"><span data-stu-id="c41ec-114">Configure the NTFS file system permissions to the content directory and the package folders under the content directory by using the Security Groups in Active Directory Domain Services that you defined earlier.</span></span>

<span data-ttu-id="c41ec-115">**Примечание**  Если для публикации ICO-и OSD-файлов используется IIS, необходимо настроить тип MIME для OSD = TXT; в противном случае службы IIS не будут обрабатывать файлы ICO и OSD для клиентов.</span><span class="sxs-lookup"><span data-stu-id="c41ec-115">**Note** If you are using IIS to publish the ICO and OSD files, you must configure a MIME type for OSD=TXT; otherwise, IIS will not serve the ICO and OSD files to clients.</span></span> <span data-ttu-id="c41ec-116">Если вы используете IIS для публикации пакетов (SFT-файлов), необходимо настроить тип MIME для SFT = binary. в противном случае службы IIS не будут обрабатывать файлы SFT для клиентов.</span><span class="sxs-lookup"><span data-stu-id="c41ec-116">If you are using IIS to publish packages (SFT files), you must configure a MIME type for SFT=Binary; otherwise, IIS will not serve the SFT files to clients.</span></span>

 

## <span data-ttu-id="c41ec-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c41ec-117">Related topics</span></span>


[<span data-ttu-id="c41ec-118">Сценарий на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="c41ec-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="c41ec-119">Сценарий на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="c41ec-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="c41ec-120">Настройка серверов Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="c41ec-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="c41ec-121">Настройка серверов Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="c41ec-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="c41ec-122">Настройка файлового сервера</span><span class="sxs-lookup"><span data-stu-id="c41ec-122">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

 

 





