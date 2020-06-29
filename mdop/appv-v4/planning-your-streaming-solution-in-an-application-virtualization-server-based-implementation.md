---
title: Планирование решения для потоковой передачи при внедрении на основе сервера Application Virtualization Server
description: Планирование решения для потоковой передачи при внедрении на основе сервера Application Virtualization Server
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815869"
---
# <span data-ttu-id="28a15-103">Планирование решения для потоковой передачи при внедрении на основе сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="28a15-103">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>


<span data-ttu-id="28a15-104">Если вы хотите использовать потоки управления виртуализацией приложений в сочетании с серверной реализацией Application Virtualization, вы можете выбрать один из нескольких альтернативных вариантов и воспользоваться преимуществами какой-либо инфраструктуры уже на месте.</span><span class="sxs-lookup"><span data-stu-id="28a15-104">If you want to use Application Virtualization Streaming Servers in conjunction with your Application Virtualization Management Server-based implementation, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="28a15-105">Например, если у вас уже есть серверы в офисах филиалов, вы можете поместить на них \\CONTENT виртуализации приложений, а затем настроить клиенты таким образом, чтобы они использовали этот контент в качестве источника контента приложения.</span><span class="sxs-lookup"><span data-stu-id="28a15-105">For example, if you already have servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="28a15-106">Если вы выбрали только серверы управления виртуализацией приложений (например, если у вас есть только один набор Office), клиенты смогут передавать содержимое из этого сервера.</span><span class="sxs-lookup"><span data-stu-id="28a15-106">If you choose to use only Application Virtualization Management Servers—for example, because you have only a single office—the clients can stream content from that server.</span></span>

<span data-ttu-id="28a15-107">Поддерживаемые параметры включают использование файлового сервера, сервера IIS или потокового сервера Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="28a15-107">The supported options include using a file server, an IIS server, or an Application Virtualization Streaming Server.</span></span> <span data-ttu-id="28a15-108">Вы также можете установить потоковый сервер Application Virtualization на существующем файловом сервере или сервере IIS.</span><span class="sxs-lookup"><span data-stu-id="28a15-108">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span> <span data-ttu-id="28a15-109">Характеристики этих параметров описаны в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="28a15-109">The characteristics of these different options are summarized in the following table.</span></span>

<span data-ttu-id="28a15-110">**Примечание**  Функция активного обновления позволяет добавить новую версию приложения на сервер управления App-V или потоковый сервер, не затрагивая пользователей, которые в данный момент запускают приложение.</span><span class="sxs-lookup"><span data-stu-id="28a15-110">**Note** The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="28a15-111">Клиенты App-V будут автоматически получать последнюю версию приложения с сервера управления App-V или потокового сервера, когда пользователь в следующий раз запускает приложение.</span><span class="sxs-lookup"><span data-stu-id="28a15-111">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="28a15-112">Для этой функции требуется использовать протокол RTSP (S).</span><span class="sxs-lookup"><span data-stu-id="28a15-112">Use of the RTSP(S) protocol is required for this feature.</span></span>

 

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
<th align="left"><span data-ttu-id="28a15-113">Тип сервера</span><span class="sxs-lookup"><span data-stu-id="28a15-113">Server Type</span></span></th>
<th align="left"><span data-ttu-id="28a15-114">Используемый протокол</span><span class="sxs-lookup"><span data-stu-id="28a15-114">Protocol</span></span></th>
<th align="left"><span data-ttu-id="28a15-115">Преимущества</span><span class="sxs-lookup"><span data-stu-id="28a15-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="28a15-116">Недостатки</span><span class="sxs-lookup"><span data-stu-id="28a15-116">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="28a15-117">Ссылки</span><span class="sxs-lookup"><span data-stu-id="28a15-117">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="28a15-118">Файловый сервер</span><span class="sxs-lookup"><span data-stu-id="28a15-118">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="28a15-119">SMB</span><span class="sxs-lookup"><span data-stu-id="28a15-119">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="28a15-120">Простое решение недорогих ресурсов для настройки существующего файлового сервера с \CONTENT</span><span class="sxs-lookup"><span data-stu-id="28a15-120">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="28a15-121">Нет активного обновления</span><span class="sxs-lookup"><span data-stu-id="28a15-121">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="28a15-122">Настройка файлового сервера</span><span class="sxs-lookup"><span data-stu-id="28a15-122">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="28a15-123">Сервер IIS</span><span class="sxs-lookup"><span data-stu-id="28a15-123">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="28a15-124">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="28a15-124">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="28a15-125">Поддерживает улучшенную безопасность по протоколу HTTPS</span><span class="sxs-lookup"><span data-stu-id="28a15-125">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="28a15-126">Поддерживает потоковую передачу на удаленные компьютеры через Интернет</span><span class="sxs-lookup"><span data-stu-id="28a15-126">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="28a15-127">Только один порт в брандмауэре, чтобы открыть</span><span class="sxs-lookup"><span data-stu-id="28a15-127">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="28a15-128">Возможностью</span><span class="sxs-lookup"><span data-stu-id="28a15-128">Scalable</span></span></p></li>
<li><p><span data-ttu-id="28a15-129">Знакомый протокол</span><span class="sxs-lookup"><span data-stu-id="28a15-129">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="28a15-130">Требуется управление IIS</span><span class="sxs-lookup"><span data-stu-id="28a15-130">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="28a15-131">Нет активного обновления</span><span class="sxs-lookup"><span data-stu-id="28a15-131">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="28a15-132">Настройка сервера для служб IIS</span><span class="sxs-lookup"><span data-stu-id="28a15-132">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="28a15-133">Потоковый сервер Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="28a15-133">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="28a15-134">RTSP/RTSP</span><span class="sxs-lookup"><span data-stu-id="28a15-134">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="28a15-135">Активное обновление</span><span class="sxs-lookup"><span data-stu-id="28a15-135">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="28a15-136">Поддержка расширенной защиты с помощью протокола RTSP</span><span class="sxs-lookup"><span data-stu-id="28a15-136">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="28a15-137">Только один порт в брандмауэре, чтобы открыть</span><span class="sxs-lookup"><span data-stu-id="28a15-137">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="28a15-138">Двойная инфраструктура</span><span class="sxs-lookup"><span data-stu-id="28a15-138">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="28a15-139">Требование для администрирования сервера</span><span class="sxs-lookup"><span data-stu-id="28a15-139">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)"><span data-ttu-id="28a15-140">Настройка серверов Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="28a15-140">How to Configure the Application Virtualization Streaming Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="28a15-141">Сервер управления виртуализацией приложений</span><span class="sxs-lookup"><span data-stu-id="28a15-141">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="28a15-142">RTSP/RTSP</span><span class="sxs-lookup"><span data-stu-id="28a15-142">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="28a15-143">Активное обновление</span><span class="sxs-lookup"><span data-stu-id="28a15-143">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="28a15-144">Поддержка расширенной защиты с помощью протокола RTSP</span><span class="sxs-lookup"><span data-stu-id="28a15-144">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="28a15-145">Только один порт в брандмауэре, чтобы открыть</span><span class="sxs-lookup"><span data-stu-id="28a15-145">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="28a15-146">Двойная инфраструктура</span><span class="sxs-lookup"><span data-stu-id="28a15-146">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="28a15-147">Требование для администрирования сервера</span><span class="sxs-lookup"><span data-stu-id="28a15-147">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="28a15-148">Настройка серверов Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="28a15-148">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="28a15-149">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="28a15-149">Related topics</span></span>


[<span data-ttu-id="28a15-150">Сценарий на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="28a15-150">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="28a15-151">Обзор компонентов системы Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="28a15-151">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="28a15-152">Публикация виртуальных приложений с помощью серверов Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="28a15-152">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





