---
title: Определение способа потоковой передачи
description: Определение способа потоковой передачи
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821669"
---
# <span data-ttu-id="e4254-103">Определение способа потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="e4254-103">Determine Your Streaming Method</span></span>


<span data-ttu-id="e4254-104">При первом нажатии пользователем значка, который был размещен на компьютере с помощью процесса публикации, клиент Application Virtualization получит содержимое пакета виртуального приложения из расположения для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="e4254-104">The first time that a user double-clicks the icon that has been placed on a computer through the publishing process, the Application Virtualization client will obtain the virtual application package content from a streaming source location.</span></span>

<span data-ttu-id="e4254-105">**Примечание** 
 *Потоковая передача* — это термин, используемый для описания процесса получения содержимого из упорядоченного пакета приложения, начиная с основного блока функций и получая дополнительные блоки по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="e4254-105">**Note**
*Streaming* is the term used to describe the process of obtaining content from a sequenced application package, starting with the primary feature block and then obtaining additional blocks as needed.</span></span>

 

<span data-ttu-id="e4254-106">Расположение исходного потока обычно является сервером, доступным для компьютера пользователя; Однако некоторые электронные системы рассылки, такие как диспетчер конфигурации конечной точки Майкрософт, могут распространять SFT-файл на компьютер пользователя, а затем передавать виртуальный пакет виртуального приложения локально из кэша этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="e4254-106">The streaming source location is usually a server that is accessible by the user’s computer; however, some electronic distribution systems, such as Microsoft Endpoint Configuration Manager, can distribute the SFT file to the user’s computer and then stream the virtual application package locally from that computer’s cache.</span></span>

<span data-ttu-id="e4254-107">**Примечание**  Расположение источника потока для виртуальных пакетов можно настроить на компьютере, который не является сервером.</span><span class="sxs-lookup"><span data-stu-id="e4254-107">**Note** A streaming source location for virtual packages can be set up on a computer that is not a server.</span></span> <span data-ttu-id="e4254-108">Это особенно удобно в небольших офисах филиалов без сервера.</span><span class="sxs-lookup"><span data-stu-id="e4254-108">This is especially useful in a small branch office that has no server.</span></span>

 

<span data-ttu-id="e4254-109">В следующей таблице описаны источники потоков, которые можно использовать для хранения упорядоченных приложений.</span><span class="sxs-lookup"><span data-stu-id="e4254-109">The streaming sources that can be used to store sequenced applications are described in the following table.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e4254-110">Тип сервера</span><span class="sxs-lookup"><span data-stu-id="e4254-110">Server Type</span></span></th>
<th align="left"><span data-ttu-id="e4254-111">Используемый протокол</span><span class="sxs-lookup"><span data-stu-id="e4254-111">Protocol</span></span></th>
<th align="left"><span data-ttu-id="e4254-112">Преимущества</span><span class="sxs-lookup"><span data-stu-id="e4254-112">Advantages</span></span></th>
<th align="left"><span data-ttu-id="e4254-113">Недостатки</span><span class="sxs-lookup"><span data-stu-id="e4254-113">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="e4254-114">Ссылки</span><span class="sxs-lookup"><span data-stu-id="e4254-114">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4254-115">Файловый сервер</span><span class="sxs-lookup"><span data-stu-id="e4254-115">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4254-116">Файл</span><span class="sxs-lookup"><span data-stu-id="e4254-116">File</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e4254-117">Простое решение недорогих ресурсов для настройки существующего файлового сервера с \CONTENT</span><span class="sxs-lookup"><span data-stu-id="e4254-117">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e4254-118">Нет активного обновления</span><span class="sxs-lookup"><span data-stu-id="e4254-118">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="e4254-119">Настройка файлового сервера</span><span class="sxs-lookup"><span data-stu-id="e4254-119">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4254-120">Сервер IIS</span><span class="sxs-lookup"><span data-stu-id="e4254-120">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4254-121">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="e4254-121">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e4254-122">Поддерживает улучшенную безопасность по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e4254-122">Supports enhanced security using HTTPS protocol.</span></span></p></li>
<li><p><span data-ttu-id="e4254-123">Поддерживает потоковую передачу на удаленные компьютеры через Интернет</span><span class="sxs-lookup"><span data-stu-id="e4254-123">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="e4254-124">Только один порт в брандмауэре, чтобы открыть</span><span class="sxs-lookup"><span data-stu-id="e4254-124">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="e4254-125">Высоко масштабируемый</span><span class="sxs-lookup"><span data-stu-id="e4254-125">Highly scalable</span></span></p></li>
<li><p><span data-ttu-id="e4254-126">Знакомый протокол</span><span class="sxs-lookup"><span data-stu-id="e4254-126">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e4254-127">Требуется управление IIS</span><span class="sxs-lookup"><span data-stu-id="e4254-127">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="e4254-128">Нет активного обновления</span><span class="sxs-lookup"><span data-stu-id="e4254-128">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="e4254-129">Настройка сервера для служб IIS</span><span class="sxs-lookup"><span data-stu-id="e4254-129">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4254-130">Потоковый сервер Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="e4254-130">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4254-131">RTSP/RTSP</span><span class="sxs-lookup"><span data-stu-id="e4254-131">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e4254-132">Активное обновление</span><span class="sxs-lookup"><span data-stu-id="e4254-132">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="e4254-133">Поддержка расширенной защиты с помощью протокола RTSP</span><span class="sxs-lookup"><span data-stu-id="e4254-133">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="e4254-134">Только один порт в брандмауэре для открытия (только для RTSP)</span><span class="sxs-lookup"><span data-stu-id="e4254-134">Only one port in firewall to open (RTSPS only)</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e4254-135">Двойная инфраструктура</span><span class="sxs-lookup"><span data-stu-id="e4254-135">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="e4254-136">Требование для администрирования сервера</span><span class="sxs-lookup"><span data-stu-id="e4254-136">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="e4254-137">Настройка серверов Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="e4254-137">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e4254-138">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e4254-138">Related topics</span></span>


[<span data-ttu-id="e4254-139">Сценарий на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="e4254-139">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="e4254-140">Обзор сценария на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="e4254-140">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="e4254-141">Определение способа публикации</span><span class="sxs-lookup"><span data-stu-id="e4254-141">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

 

 





