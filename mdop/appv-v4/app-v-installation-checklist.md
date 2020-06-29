---
title: Контрольный список установки App-V
description: Контрольный список установки App-V
author: dansimp
ms.assetid: b17efaab-cd6d-4c30-beb7-c6e7c9c87657
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d6d83ac465a7e48dd35bd2fe966c3c51be24c96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819812"
---
# <span data-ttu-id="840ec-103">Контрольный список установки App-V</span><span class="sxs-lookup"><span data-stu-id="840ec-103">App-V Installation Checklist</span></span>


<span data-ttu-id="840ec-104">Приведенный ниже контрольный список предназначен для создания высокоуровневого списка элементов, которые необходимо учитывать, и подробно описанных действий, которые необходимо предпринять, чтобы установить серверы Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="840ec-104">The following checklist is intended to provide a high-level list of items to consider and outlines the steps you should take to install the Microsoft Application Virtualization (App-V) servers.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="840ec-105">Шаг</span><span class="sxs-lookup"><span data-stu-id="840ec-105">Step</span></span></th>
<th align="left"><span data-ttu-id="840ec-106">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="840ec-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="840ec-107">Установите сервер управления App-V.</span><span class="sxs-lookup"><span data-stu-id="840ec-107">Install the App-V Management Server.</span></span> <span data-ttu-id="840ec-108">Если вы устанавливаете веб-службу управления, консоль управления или хранилище данных на разных серверах, вы можете воспользоваться параметром выборочной установки.</span><span class="sxs-lookup"><span data-stu-id="840ec-108">If you are installing the Management Web Service, Management Console, or the Data Store on different servers, you can use the custom installation option.</span></span></p></td>
<td align="left"><p><a href="how-to-install-application-virtualization-management-server.md" data-raw-source="[How to Install Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)"><span data-ttu-id="840ec-109">Установка сервера Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="840ec-109">How to Install Application Virtualization Management Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="840ec-110">Установите веб-службу управления App-V.</span><span class="sxs-lookup"><span data-stu-id="840ec-110">Install the App-V Management Web Service.</span></span> <span data-ttu-id="840ec-111">(Опционально ¹)</span><span class="sxs-lookup"><span data-stu-id="840ec-111">(Optional ¹)</span></span></p></td>
<td align="left"><p><a href="how-to-install-the-management-web-service.md" data-raw-source="[How to Install the Management Web Service](how-to-install-the-management-web-service.md)"><span data-ttu-id="840ec-112">Установка веб-службы управления</span><span class="sxs-lookup"><span data-stu-id="840ec-112">How to Install the Management Web Service</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="840ec-113">Установите консоль управления App-V.</span><span class="sxs-lookup"><span data-stu-id="840ec-113">Install the App-V Management Console.</span></span> <span data-ttu-id="840ec-114">(Опционально ¹)</span><span class="sxs-lookup"><span data-stu-id="840ec-114">(Optional ¹)</span></span></p></td>
<td align="left"><p><a href="how-to-install-the-management-console.md" data-raw-source="[How to Install the Management Console](how-to-install-the-management-console.md)"><span data-ttu-id="840ec-115">Установка консоли управления</span><span class="sxs-lookup"><span data-stu-id="840ec-115">How to Install the Management Console</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="840ec-116">Установите хранилище данных App-V.</span><span class="sxs-lookup"><span data-stu-id="840ec-116">Install the App-V Data Store.</span></span> <span data-ttu-id="840ec-117">(Опционально ¹)</span><span class="sxs-lookup"><span data-stu-id="840ec-117">(Optional ¹)</span></span></p></td>
<td align="left"><p><a href="how-to-install-a-database.md" data-raw-source="[How to Install a Database](how-to-install-a-database.md)"><span data-ttu-id="840ec-118">Установка базы данных</span><span class="sxs-lookup"><span data-stu-id="840ec-118">How to Install a Database</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="840ec-119">Установите клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="840ec-119">Install the App-V client.</span></span></p></td>
<td align="left"><p><a href="how-to-manually-install-the-application-virtualization-client.md" data-raw-source="[How to Manually Install the Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)"><span data-ttu-id="840ec-120">Установка клиента Application Virtualization Client вручную</span><span class="sxs-lookup"><span data-stu-id="840ec-120">How to Manually Install the Application Virtualization Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="840ec-121">Установка секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="840ec-121">Install the App-V Sequencer.</span></span></p></td>
<td align="left"><p><a href="how-to-install-the-application-virtualization-sequencer.md" data-raw-source="[How to Install the Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md)"><span data-ttu-id="840ec-122">Установка программы Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="840ec-122">How to Install the Application Virtualization Sequencer</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="840ec-123">Установите потоковый сервер App-V.</span><span class="sxs-lookup"><span data-stu-id="840ec-123">Install the App-V Streaming Server.</span></span> <span data-ttu-id="840ec-124">(Это необязательно и требуется только при установке потокового сервера).</span><span class="sxs-lookup"><span data-stu-id="840ec-124">(This is optional and required only if you are installing the Streaming Server).</span></span></p></td>
<td align="left"><p><a href="how-to-install-the-application-virtualization-streaming-server.md" data-raw-source="[How to Install the Application Virtualization Streaming Server](how-to-install-the-application-virtualization-streaming-server.md)"><span data-ttu-id="840ec-125">Установка сервера потоковой передачи Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="840ec-125">How to Install the Application Virtualization Streaming Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="840ec-126">Создавайте каталоги содержимого на серверах, которые будут использоваться для потоковой передачи приложений на компьютеры пользователей.</span><span class="sxs-lookup"><span data-stu-id="840ec-126">Create Content directories on the servers that will be used for streaming applications to users’ computers.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="840ec-127">Настройка серверов Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="840ec-127">How to Configure the Application Virtualization Management Servers</span></span></a></p>
<p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)"><span data-ttu-id="840ec-128">Настройка серверов Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="840ec-128">How to Configure the Application Virtualization Streaming Servers</span></span></a></p>
<p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="840ec-129">Настройка сервера для служб IIS</span><span class="sxs-lookup"><span data-stu-id="840ec-129">How to Configure the Server for IIS</span></span></a></p>
<p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="840ec-130">Настройка файлового сервера</span><span class="sxs-lookup"><span data-stu-id="840ec-130">How to Configure the File Server</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="840ec-131">¹ этот параметр требуется только в том случае, если вы устанавливаете веб-службу управления App-V, консоль управления или хранилище данных на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="840ec-131">¹ This is required only if you are installing the App-V Management Web Service, Management Console, or the Data Store on a different computer.</span></span>

## <span data-ttu-id="840ec-132">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="840ec-132">Related topics</span></span>


[<span data-ttu-id="840ec-133">Контрольные списки развертывания и обновления Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="840ec-133">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

[<span data-ttu-id="840ec-134">Контрольный список пост-установки App-V</span><span class="sxs-lookup"><span data-stu-id="840ec-134">App-V Postinstallation Checklist</span></span>](app-v-postinstallation-checklist.md)

 

 





