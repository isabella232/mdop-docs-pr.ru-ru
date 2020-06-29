---
title: Планирование развертывания сервера App-V 5.0
description: Планирование развертывания сервера App-V 5.0
author: dansimp
ms.assetid: fd89b324-3961-471a-ad90-c8f9ae7a8155
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06c7c17fd081b89337bbecd31f20f6796338f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813456"
---
# <span data-ttu-id="a484a-103">Планирование развертывания сервера App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a484a-103">Planning for the App-V 5.0 Server Deployment</span></span>


<span data-ttu-id="a484a-104">Серверная инфраструктура Microsoft Application Virtualization (App-V) 5,0 состоит из набора специализированных функций, которые можно установить на одном или нескольких серверных компьютерах в зависимости от требований предприятия.</span><span class="sxs-lookup"><span data-stu-id="a484a-104">The Microsoft Application Virtualization (App-V) 5.0 server infrastructure consists of a set of specialized features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span>

## <span data-ttu-id="a484a-105">Планирование развертывания сервера App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a484a-105">Planning for App-V 5.0 Server Deployment</span></span>


<span data-ttu-id="a484a-106">Сервер App-V 5,0 состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="a484a-106">The App-V 5.0 server consists of the following features:</span></span>

-   <span data-ttu-id="a484a-107">Сервер управления — предоставляет общую функциональность управления для инфраструктуры App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a484a-107">Management Server – provides overall management functionality for the App-V 5.0 infrastructure.</span></span>

-   <span data-ttu-id="a484a-108">База данных управления — упрощает предварительное развертывание баз данных для управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a484a-108">Management Database – facilitates database predeployments for App-V 5.0 management.</span></span>

-   <span data-ttu-id="a484a-109">Сервер публикации — предоставляет функции размещения и потоковой передачи для виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="a484a-109">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="a484a-110">Сервер отчетов — предоставляет службы отчетов App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a484a-110">Reporting Server – provides App-V 5.0 reporting services.</span></span>

-   <span data-ttu-id="a484a-111">База данных отчетов — упрощает предварительное развертывание баз данных для отчетов App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a484a-111">Reporting Database – facilitates database predeployments for App-V 5.0 reporting.</span></span>

<span data-ttu-id="a484a-112">В списке ниже приведены рекомендуемые методы для установки инфраструктуры сервера App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a484a-112">The following list displays the recommended methods for installing the App-V 5.0 server infrastructure:</span></span>

-   <span data-ttu-id="a484a-113">Установите сервер App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a484a-113">Install the App-V 5.0 server.</span></span> <span data-ttu-id="a484a-114">Дополнительные сведения можно найти в разделе [развертывание сервера App-V 5,0](how-to-deploy-the-app-v-50-server-50sp3.md).</span><span class="sxs-lookup"><span data-stu-id="a484a-114">For more information, see [How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md).</span></span>

-   <span data-ttu-id="a484a-115">Установите на отдельных компьютерах базу данных, отчеты и функции управления.</span><span class="sxs-lookup"><span data-stu-id="a484a-115">Install the database, reporting, and management features on separate computers.</span></span> <span data-ttu-id="a484a-116">Дополнительные сведения можно найти в разделе [Установка баз данных управления и отчетов на разных компьютерах из служб управления и отчетов](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md).</span><span class="sxs-lookup"><span data-stu-id="a484a-116">For more information, see [How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md).</span></span>

-   <span data-ttu-id="a484a-117">Используй электронную рассылку программного обеспечения (ESD).</span><span class="sxs-lookup"><span data-stu-id="a484a-117">Use Electronic Software Distribution (ESD).</span></span> <span data-ttu-id="a484a-118">Дополнительные сведения [можно найти в разделе Развертывание пакетов приложения App-V 5,0 с помощью электронного распространения программного обеспечения](how-to-deploy-app-v-50-packages-using-electronic-software-distribution.md).</span><span class="sxs-lookup"><span data-stu-id="a484a-118">For more information, see [How to deploy App-V 5.0 Packages Using Electronic Software Distribution](how-to-deploy-app-v-50-packages-using-electronic-software-distribution.md).</span></span>

-   <span data-ttu-id="a484a-119">Установите все компоненты сервера на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a484a-119">Install all server features on a single computer.</span></span>

## <a href="" id="---------app-v-5-0-server-interaction"></a> <span data-ttu-id="a484a-120">Взаимодействие с сервером App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a484a-120">App-V 5.0 Server Interaction</span></span>


<span data-ttu-id="a484a-121">В этом разделе содержатся сведения о том, как взаимодействуют различные роли сервера App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a484a-121">This section contains information about how the various App-V 5.0 server roles interact with each other.</span></span>

<span data-ttu-id="a484a-122">Сервер управления App-V 5,0 включает в себя репозиторий пакетов и их назначенные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a484a-122">The App-V 5.0 Management Server contains the repository of packages and their assigned configurations.</span></span> <span data-ttu-id="a484a-123">Для серверов публикаций, которые зарегистрированы на сервере управления, связанные метаданные предоставляются на серверы публикаций, которые будут использоваться при получении запросов на обновление публикации с компьютеров, на которых запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a484a-123">For Publishing Servers that are registered with the Management Server, the associated metadata is provided to the Publishing servers for use when publishing refresh requests are received from computers running the App-V 5.0 Client.</span></span> <span data-ttu-id="a484a-124">Серверы публикации App-V 5,0, управляемые с помощью одного сервера управления, могут поддерживать различные клиенты и могут иметь разные имена веб-сайтов и привязки портов.</span><span class="sxs-lookup"><span data-stu-id="a484a-124">App-V 5.0 publishing servers managed by a single management server can be serving different clients and can have different website names and port bindings.</span></span> <span data-ttu-id="a484a-125">Кроме того, все серверы публикаций, управляемые одним сервером управления, являются репликами друг друга.</span><span class="sxs-lookup"><span data-stu-id="a484a-125">Additionally, all Publishing Servers managed by the same Management Server are replicas of each other.</span></span>

<span data-ttu-id="a484a-126">**Примечание**  Сервер управления не выполняет балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a484a-126">**Note** The Management Server does not perform any load balancing.</span></span> <span data-ttu-id="a484a-127">Связанные метаданные просто передаются на сервер публикаций для использования при обработке запросов клиентов.</span><span class="sxs-lookup"><span data-stu-id="a484a-127">The associated metadata is simply passed to the publishing server for use when processing client requests.</span></span>

 

## <span data-ttu-id="a484a-128">Протоколы, связанные с сервером, и внешние возможности</span><span class="sxs-lookup"><span data-stu-id="a484a-128">Server-Related Protocols and External Features</span></span>


<span data-ttu-id="a484a-129">Ниже отображаются сведения о серверных протоколах, используемых серверами App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a484a-129">The following displays information about server-related protocols used by the App-V 5.0 servers.</span></span> <span data-ttu-id="a484a-130">В таблице также есть механизм составления отчетов для каждого типа сервера.</span><span class="sxs-lookup"><span data-stu-id="a484a-130">The table also includes the reporting mechanism for each server type.</span></span>

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
<th align="left"><span data-ttu-id="a484a-131">Тип сервера</span><span class="sxs-lookup"><span data-stu-id="a484a-131">Server Type</span></span></th>
<th align="left"><span data-ttu-id="a484a-132">Протоколы</span><span class="sxs-lookup"><span data-stu-id="a484a-132">Protocols</span></span></th>
<th align="left"><span data-ttu-id="a484a-133">Необходимые внешние функции</span><span class="sxs-lookup"><span data-stu-id="a484a-133">External Features Needed</span></span></th>
<th align="left"><span data-ttu-id="a484a-134">Отчеты</span><span class="sxs-lookup"><span data-stu-id="a484a-134">Reporting</span></span></th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a484a-135">Сервер IIS</span><span class="sxs-lookup"><span data-stu-id="a484a-135">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="a484a-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="a484a-136">HTTP</span></span></p>
<p><span data-ttu-id="a484a-137">HTTPS</span><span class="sxs-lookup"><span data-stu-id="a484a-137">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="a484a-138">Для этой комбинации протоколов сервера требуется механизм синхронизации содержимого между сервером управления и потоковым сервером.</span><span class="sxs-lookup"><span data-stu-id="a484a-138">This server-protocol combination requires a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="a484a-139">При использовании HTTP или HTTPS используйте сервер IIS и брандмауэр, чтобы защитить сервер от доступа к Интернету.</span><span class="sxs-lookup"><span data-stu-id="a484a-139">When using HTTP or HTTPS, use an IIS server and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a484a-140">внутренний</span><span class="sxs-lookup"><span data-stu-id="a484a-140">Internal</span></span></p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a484a-141">Файл</span><span class="sxs-lookup"><span data-stu-id="a484a-141">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="a484a-142">SMB</span><span class="sxs-lookup"><span data-stu-id="a484a-142">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a484a-143">Эта комбинация протоколов сервера должна поддерживать синхронизацию содержимого между сервером управления и потоковым сервером.</span><span class="sxs-lookup"><span data-stu-id="a484a-143">This server-protocol combination requires support to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="a484a-144">Используйте клиентский компьютер с функцией обмена файлами или потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="a484a-144">Use a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a484a-145">внутренний</span><span class="sxs-lookup"><span data-stu-id="a484a-145">Internal</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="a484a-146">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a484a-146">Related topics</span></span>


[<span data-ttu-id="a484a-147">Планирование развертывания App-V</span><span class="sxs-lookup"><span data-stu-id="a484a-147">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="a484a-148">Развертывание сервера App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a484a-148">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

 

 





