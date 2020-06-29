---
title: Планирование решения для потоковой передачи при внедрении с помощью электронного распространения программного обеспечения
description: Планирование решения для потоковой передачи при внедрении с помощью электронного распространения программного обеспечения
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815859"
---
# <span data-ttu-id="ceca6-103">Планирование решения для потоковой передачи при внедрении с помощью электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="ceca6-103">Planning Your Streaming Solution in an Electronic Software Distribution Implementation</span></span>


<span data-ttu-id="ceca6-104">Если вы решили использовать потоковые серверы в сочетании с системой ESD, чтобы сделать содержимое приложения доступным для компьютеров конечных пользователей, вы можете выбрать один из нескольких вариантов и воспользоваться преимуществами какой бы то или другой инфраструктуры уже на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="ceca6-104">If you decide to use streaming servers in conjunction with your ESD system to make application content available to your end user computers, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="ceca6-105">Например, если в системе ESD есть общий доступ к программному обеспечению на серверах в офисах филиалов, вы можете поместить \\CONTENT Application Virtualization на эти серверы и настроить клиенты таким образом, чтобы они использовали этот контент в качестве источника контента приложения.</span><span class="sxs-lookup"><span data-stu-id="ceca6-105">For example, if your ESD system has software distribution shares on servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="ceca6-106">Поддерживаемые параметры включают использование файлового сервера или сервера IIS.</span><span class="sxs-lookup"><span data-stu-id="ceca6-106">The supported options include using a file server or an IIS server.</span></span> <span data-ttu-id="ceca6-107">Вы также можете установить потоковый сервер Application Virtualization на существующем файловом сервере или сервере IIS.</span><span class="sxs-lookup"><span data-stu-id="ceca6-107">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span>

<span data-ttu-id="ceca6-108">Потоковый сервер Application Virtualization обеспечивает поддержку функции активного обновления в Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="ceca6-108">The Application Virtualization Streaming Server provides support for the active upgrade feature in Application Virtualization.</span></span> <span data-ttu-id="ceca6-109">Функция активного обновления позволяет добавить новую версию приложения на сервер управления App-V или потоковый сервер, не затрагивая пользователей, которые в данный момент запускают приложение.</span><span class="sxs-lookup"><span data-stu-id="ceca6-109">The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="ceca6-110">Клиенты App-V будут автоматически получать последнюю версию приложения с сервера управления App-V или потокового сервера, когда пользователь в следующий раз запускает приложение.</span><span class="sxs-lookup"><span data-stu-id="ceca6-110">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="ceca6-111">Для этой функции требуется использовать протокол RTSP (S).</span><span class="sxs-lookup"><span data-stu-id="ceca6-111">Use of the RTSP(S) protocol is required for this feature.</span></span> <span data-ttu-id="ceca6-112">Если вы решили не использовать потоковый сервер Application Virtualization, вам потребуется явно управлять обновлением пакета приложения с помощью системы ESD.</span><span class="sxs-lookup"><span data-stu-id="ceca6-112">If you choose not to use the Application Virtualization Streaming Server, you will need to explicitly manage application package upgrades by using the ESD system.</span></span>

<span data-ttu-id="ceca6-113">**Примечание**  Управление доступом к приложениям осуществляется с помощью групп безопасности доменных служб Active Directory, поэтому вам потребуется планировать процесс настройки группы безопасности для каждого виртуального приложения и для управления добавлением пользователей в каждую группу.</span><span class="sxs-lookup"><span data-stu-id="ceca6-113">**Note** Access to the applications is controlled by means of Security Groups in Active Directory Domain Services, so you will need to plan a process for setting up a security group for each virtual application and for managing which users are added to each group.</span></span> <span data-ttu-id="ceca6-114">Системный администратор Application Virtualization настраивает каждый потоковый сервер для использования этих групп Active Directory, применяя списки ACL к каталогам приложений в рамках общего доступа к СОДЕРЖИМому, которое управляет доступом к пакетам на основе членства в группе Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ceca6-114">The Application Virtualization system administrator configures each streaming server to use these Active Directory groups by applying ACLs to the application directories under the CONTENT share, which controls access to the packages based on Active Directory group membership.</span></span>

 

<span data-ttu-id="ceca6-115">Характеристики доступных потоковых параметров описаны в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="ceca6-115">The characteristics of the available streaming options are summarized in the following table.</span></span>

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
<th align="left"><span data-ttu-id="ceca6-116">Тип сервера</span><span class="sxs-lookup"><span data-stu-id="ceca6-116">Server Type</span></span></th>
<th align="left"><span data-ttu-id="ceca6-117">Используемый протокол</span><span class="sxs-lookup"><span data-stu-id="ceca6-117">Protocol</span></span></th>
<th align="left"><span data-ttu-id="ceca6-118">Преимущества</span><span class="sxs-lookup"><span data-stu-id="ceca6-118">Advantages</span></span></th>
<th align="left"><span data-ttu-id="ceca6-119">Недостатки</span><span class="sxs-lookup"><span data-stu-id="ceca6-119">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="ceca6-120">Ссылки</span><span class="sxs-lookup"><span data-stu-id="ceca6-120">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ceca6-121">Файловый сервер</span><span class="sxs-lookup"><span data-stu-id="ceca6-121">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ceca6-122">SMB</span><span class="sxs-lookup"><span data-stu-id="ceca6-122">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ceca6-123">Простое решение недорогих ресурсов для настройки существующего файлового сервера с \CONTENT</span><span class="sxs-lookup"><span data-stu-id="ceca6-123">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ceca6-124">Нет активного обновления</span><span class="sxs-lookup"><span data-stu-id="ceca6-124">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="ceca6-125">Настройка файлового сервера</span><span class="sxs-lookup"><span data-stu-id="ceca6-125">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ceca6-126">Сервер IIS</span><span class="sxs-lookup"><span data-stu-id="ceca6-126">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ceca6-127">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="ceca6-127">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ceca6-128">Поддерживает улучшенную безопасность по протоколу HTTPS</span><span class="sxs-lookup"><span data-stu-id="ceca6-128">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="ceca6-129">Поддерживает потоковую передачу на удаленные компьютеры через Интернет</span><span class="sxs-lookup"><span data-stu-id="ceca6-129">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="ceca6-130">Только один порт в брандмауэре, чтобы открыть</span><span class="sxs-lookup"><span data-stu-id="ceca6-130">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="ceca6-131">Возможностью</span><span class="sxs-lookup"><span data-stu-id="ceca6-131">Scalable</span></span></p></li>
<li><p><span data-ttu-id="ceca6-132">Знакомый протокол</span><span class="sxs-lookup"><span data-stu-id="ceca6-132">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ceca6-133">Требуется управление IIS</span><span class="sxs-lookup"><span data-stu-id="ceca6-133">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="ceca6-134">Нет активного обновления</span><span class="sxs-lookup"><span data-stu-id="ceca6-134">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="ceca6-135">Настройка сервера для служб IIS</span><span class="sxs-lookup"><span data-stu-id="ceca6-135">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ceca6-136">Потоковый сервер Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="ceca6-136">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ceca6-137">RTSP/RTSP</span><span class="sxs-lookup"><span data-stu-id="ceca6-137">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ceca6-138">Активное обновление</span><span class="sxs-lookup"><span data-stu-id="ceca6-138">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="ceca6-139">Поддержка расширенной защиты с помощью протокола RTSP</span><span class="sxs-lookup"><span data-stu-id="ceca6-139">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="ceca6-140">Только один порт в брандмауэре, чтобы открыть</span><span class="sxs-lookup"><span data-stu-id="ceca6-140">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ceca6-141">Двойная инфраструктура</span><span class="sxs-lookup"><span data-stu-id="ceca6-141">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="ceca6-142">Требование для администрирования сервера</span><span class="sxs-lookup"><span data-stu-id="ceca6-142">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="ceca6-143">Настройка серверов Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="ceca6-143">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ceca6-144">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ceca6-144">Related topics</span></span>


[<span data-ttu-id="ceca6-145">Настройка серверов для развертывания на основе ESD</span><span class="sxs-lookup"><span data-stu-id="ceca6-145">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)

[<span data-ttu-id="ceca6-146">Обзор защиты и безопасности</span><span class="sxs-lookup"><span data-stu-id="ceca6-146">Security and Protection Overview</span></span>](security-and-protection-overview.md)

[<span data-ttu-id="ceca6-147">Публикация виртуальных приложений с помощью электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="ceca6-147">Publishing Virtual Applications Using Electronic Software Distribution</span></span>](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





