---
title: Сценарии использования серверов с выходом в Интернет в сети периметра
description: Сценарии использования серверов с выходом в Интернет в сети периметра
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fcb04e651341fa107c358eaabbd7992d7ea155ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816282"
---
# <span data-ttu-id="15895-103">Сценарии использования серверов с выходом в Интернет в сети периметра</span><span class="sxs-lookup"><span data-stu-id="15895-103">Internet-Facing Server Scenarios for Perimeter Networks</span></span>


<span data-ttu-id="15895-104">Приложение App-V 4.5 поддерживает сценарии сервера в Интернете, в которых пользователи, не подключенные к корпоративной сети или отключенные от сети, по-прежнему могут использовать App-V.</span><span class="sxs-lookup"><span data-stu-id="15895-104">App-V4.5 supports Internet-facing server scenarios, in which users who are not connected to the corporate network or who disconnect from the network can still use App-V.</span></span> <span data-ttu-id="15895-105">Как показано на приведенном ниже рисунке, поддерживаются только безопасные протоколы в Интернете (RTSP и HTTPS).</span><span class="sxs-lookup"><span data-stu-id="15895-105">As shown in the following illustration, only the use of secure protocols on the Internet (RTSPS and HTTPS) is supported.</span></span>

![Схема расположения брандмауэра App-v](images/appvfirewalls.gif)

<span data-ttu-id="15895-107">Вы можете настроить Интернет-решение с помощью сервера ISA Server, где инфраструктура App-V находится во внутренней сети следующими способами:</span><span class="sxs-lookup"><span data-stu-id="15895-107">You can set up an Internet-facing solution, using an ISA Server, where the App-V infrastructure is on the internal network in the following ways:</span></span>

-   <span data-ttu-id="15895-108">Создайте правило веб-публикации для сервера IIS, на котором размещаются файлы ICO и OSD, и (необязательно) пакеты для потоковой передачи данных, расположенные во внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="15895-108">Create a Web Publishing rule for the IIS server that is hosting the ICO and OSD files—and optionally, the packages for streaming—located on the internal network.</span></span> <span data-ttu-id="15895-109">Подробное руководство представлено ниже <https://go.microsoft.com/fwlink/?LinkId=151982> .</span><span class="sxs-lookup"><span data-stu-id="15895-109">Detailed steps are provided at <https://go.microsoft.com/fwlink/?LinkId=151982>.</span></span>

-   <span data-ttu-id="15895-110">Создайте правило публикации сервера для веб-сервера App-V (RTSP).</span><span class="sxs-lookup"><span data-stu-id="15895-110">Create a Server Publishing rule for the App-V Web Management Server (RTSPS).</span></span> <span data-ttu-id="15895-111">Подробное руководство представлено ниже [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .</span><span class="sxs-lookup"><span data-stu-id="15895-111">Detailed steps are provided at [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983).</span></span>

<span data-ttu-id="15895-112">Как показано на приведенном ниже рисунке, если инфраструктура реализовала другие брандмауэры между клиентом и сервером ISA, а также между сервером ISA и внутренней сетью, для поддержки потока трафика должны быть созданы правила брандмауэра для протоколов RTSP (TCP 322) и HTTPS (TCP 443).</span><span class="sxs-lookup"><span data-stu-id="15895-112">As shown in the following illustration, if the infrastructure has implemented other firewalls between the client and the ISA Server or between the ISA Server and the internal network, both RTSPS (TCP 322) and HTTPS (TCP 443) firewall rules must be created to support the flow of traffic.</span></span> <span data-ttu-id="15895-113">Кроме того, если вы реализовали брандмауэры между сервером ISA и внутренней сетью, для участников домена необходимо разрешить туннелирование через брандмауэр (DNS, LDAP, Kerberos, SMB/CIFS).</span><span class="sxs-lookup"><span data-stu-id="15895-113">Also, if firewalls have been implemented between the ISA Server and the internal network, the default traffic required for domain members must be permitted to tunnel through the firewall (DNS, LDAP, Kerberos, SMB/CIFS).</span></span>

![Схема брандмауэра пограничной сети для App-v](images/appvperimeternetworkfirewall.gif)

<span data-ttu-id="15895-115">Так как решения брандмауэра отличаются от среды к среде, в руководстве, описанном в этом разделе, описывается трафик, который требуется для настройки среды App-V в сети периметра.</span><span class="sxs-lookup"><span data-stu-id="15895-115">Because the firewall solutions vary from environment to environment, the guidance provided in this topic describes the traffic that would be required to configure an Internet-facing App-V environment in the perimeter network.</span></span> <span data-ttu-id="15895-116">Эти сведения также относятся к рекомендуемым серверам внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="15895-116">This information also includes the recommended internal network servers.</span></span>

<span data-ttu-id="15895-117">Поместите в демилитаризованную сеть следующие серверы:</span><span class="sxs-lookup"><span data-stu-id="15895-117">Place the following servers in the perimeter network:</span></span>

-   <span data-ttu-id="15895-118">Сервер управления App-V</span><span class="sxs-lookup"><span data-stu-id="15895-118">App-V Management Server</span></span>

-   <span data-ttu-id="15895-119">Сервер IIS для публикации и потоковая передача</span><span class="sxs-lookup"><span data-stu-id="15895-119">IIS server for publishing and streaming</span></span>

<span data-ttu-id="15895-120">**Примечание**  Рекомендуется размещать сервер управления и сервер IIS на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="15895-120">**Note** It is a best practice to place the Management Server and IIS server on separate computers.</span></span>

 

<span data-ttu-id="15895-121">Поместите в внутреннюю сеть следующие серверы:</span><span class="sxs-lookup"><span data-stu-id="15895-121">Place the following servers in the internal network:</span></span>

-   <span data-ttu-id="15895-122">Сервер содержимого</span><span class="sxs-lookup"><span data-stu-id="15895-122">Content server</span></span>

-   <span data-ttu-id="15895-123">Хранилище данных (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="15895-123">Data store (SQL Server)</span></span>

-   <span data-ttu-id="15895-124">Контроллер домена Active Directory</span><span class="sxs-lookup"><span data-stu-id="15895-124">Active Directory Domain Controller</span></span>

## <span data-ttu-id="15895-125">Требования к трафику</span><span class="sxs-lookup"><span data-stu-id="15895-125">Traffic Requirements</span></span>


<span data-ttu-id="15895-126">В приведенных ниже таблицах перечислены требования к трафику для обмена данными через Интернет и демилитаризованную сеть и от демилитаризованной зоны к внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="15895-126">The following tables list the traffic requirements for communication from the Internet and the perimeter network and from the perimeter network to the internal network.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15895-127">Требования к трафику из Интернета в демилитаризованную сеть</span><span class="sxs-lookup"><span data-stu-id="15895-127">Traffic Requirements from Internet to Perimeter Network</span></span></th>
<th align="left"><span data-ttu-id="15895-128">Сведения</span><span class="sxs-lookup"><span data-stu-id="15895-128">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15895-129">RTSP (обновление публикации и потоковые пакеты)</span><span class="sxs-lookup"><span data-stu-id="15895-129">RTSPS (publishing refresh and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="15895-130">TCP 322 по умолчанию; Это можно изменить на сервере управления App-V.</span><span class="sxs-lookup"><span data-stu-id="15895-130">TCP 322 by default; this can be changed in App-V Management Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15895-131">HTTPS (файлы ICO и OSD и потоковые пакеты)</span><span class="sxs-lookup"><span data-stu-id="15895-131">HTTPS (publishing ICO and OSD files and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="15895-132">TCP 443 по умолчанию; Это можно изменить в конфигурации IIS.</span><span class="sxs-lookup"><span data-stu-id="15895-132">TCP 443 by default; this can be changed in the IIS configuration.</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15895-133">Требования к трафику из периметра внутренней сети</span><span class="sxs-lookup"><span data-stu-id="15895-133">Traffic Requirements from Perimeter Network to Internal Network</span></span></th>
<th align="left"><span data-ttu-id="15895-134">Сведения</span><span class="sxs-lookup"><span data-stu-id="15895-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15895-135">SQL Server</span><span class="sxs-lookup"><span data-stu-id="15895-135">SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="15895-136">TCP 1433 является значением по умолчанию, но может быть настроено в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="15895-136">TCP 1433 is the default but can be configured in SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15895-137">SMB/CIFS</span><span class="sxs-lookup"><span data-stu-id="15895-137">SMB/CIFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="15895-138">Если каталог содержимого удален с серверов управления (-ов) или сервера IIS (рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="15895-138">If the content directory is located remotely from the Management Server(s) or IIS server (recommended).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15895-139">Kerberos</span><span class="sxs-lookup"><span data-stu-id="15895-139">Kerberos</span></span></p></td>
<td align="left"><p><span data-ttu-id="15895-140">TCP и UDP 88</span><span class="sxs-lookup"><span data-stu-id="15895-140">TCP and UDP 88</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15895-141">LDAP</span><span class="sxs-lookup"><span data-stu-id="15895-141">LDAP</span></span></p></td>
<td align="left"><p><span data-ttu-id="15895-142">TCP и UDP 389</span><span class="sxs-lookup"><span data-stu-id="15895-142">TCP and UDP 389</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15895-143">DNS</span><span class="sxs-lookup"><span data-stu-id="15895-143">DNS</span></span></p></td>
<td align="left"><p><span data-ttu-id="15895-144">Разрешение имен внутренних ресурсов (может быть удалено с использованием файла узла на серверах сети периметра)</span><span class="sxs-lookup"><span data-stu-id="15895-144">For name resolution of internal resources (can be eliminated with the use of host’s file on perimeter network servers)</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





