---
title: Планирование развертывания сервера App-V 5.1
description: Планирование развертывания сервера App-V 5.1
author: dansimp
ms.assetid: eedd97c9-bee0-4749-9d1e-ab9528fba398
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31e3a116eb511356b061e6ccb18c7e25c060a66e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813437"
---
# <span data-ttu-id="2b5e5-103">Планирование развертывания сервера App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2b5e5-103">Planning for the App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="2b5e5-104">Серверная инфраструктура Microsoft Application Virtualization (App-V) 5,1 состоит из набора специализированных функций, которые можно установить на одном или нескольких серверных компьютерах в зависимости от требований предприятия.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-104">The Microsoft Application Virtualization (App-V) 5.1 server infrastructure consists of a set of specialized features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span>

## <span data-ttu-id="2b5e5-105">Планирование развертывания сервера App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="2b5e5-105">Planning for App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="2b5e5-106">Сервер App-V 5,1 состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="2b5e5-106">The App-V 5.1 server consists of the following features:</span></span>

-   <span data-ttu-id="2b5e5-107">Сервер управления — предоставляет общую функциональность управления для инфраструктуры App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-107">Management Server – provides overall management functionality for the App-V 5.1 infrastructure.</span></span>

-   <span data-ttu-id="2b5e5-108">База данных управления — упрощает предварительное развертывание баз данных для управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-108">Management Database – facilitates database predeployments for App-V 5.1 management.</span></span>

-   <span data-ttu-id="2b5e5-109">Сервер публикации — предоставляет функции размещения и потоковой передачи для виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-109">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="2b5e5-110">Сервер отчетов — предоставляет службы отчетов App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-110">Reporting Server – provides App-V 5.1 reporting services.</span></span>

-   <span data-ttu-id="2b5e5-111">База данных отчетов — упрощает предварительное развертывание баз данных для отчетов App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-111">Reporting Database – facilitates database predeployments for App-V 5.1 reporting.</span></span>

<span data-ttu-id="2b5e5-112">В списке ниже приведены рекомендуемые методы для установки инфраструктуры сервера App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-112">The following list displays the recommended methods for installing the App-V 5.1 server infrastructure:</span></span>

-   <span data-ttu-id="2b5e5-113">Установите сервер App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-113">Install the App-V 5.1 server.</span></span> <span data-ttu-id="2b5e5-114">Дополнительные сведения можно найти в разделе [развертывание сервера App-V 5,1](how-to-deploy-the-app-v-51-server.md).</span><span class="sxs-lookup"><span data-stu-id="2b5e5-114">For more information, see [How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md).</span></span>

-   <span data-ttu-id="2b5e5-115">Установите на отдельных компьютерах базу данных, отчеты и функции управления.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-115">Install the database, reporting, and management features on separate computers.</span></span> <span data-ttu-id="2b5e5-116">Дополнительные сведения можно найти в разделе [Установка баз данных управления и отчетов на разных компьютерах из служб управления и отчетов](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md).</span><span class="sxs-lookup"><span data-stu-id="2b5e5-116">For more information, see [How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md).</span></span>

-   <span data-ttu-id="2b5e5-117">Используй электронную рассылку программного обеспечения (ESD).</span><span class="sxs-lookup"><span data-stu-id="2b5e5-117">Use Electronic Software Distribution (ESD).</span></span> <span data-ttu-id="2b5e5-118">Дополнительные сведения [можно найти в разделе Развертывание пакетов приложения App-V 5,1 с помощью электронного распространения программного обеспечения](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span><span class="sxs-lookup"><span data-stu-id="2b5e5-118">For more information, see [How to deploy App-V 5.1 Packages Using Electronic Software Distribution](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span></span>

-   <span data-ttu-id="2b5e5-119">Установите все компоненты сервера на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-119">Install all server features on a single computer.</span></span>

## <a href="" id="---------app-v-5-1-server-interaction"></a> <span data-ttu-id="2b5e5-120">Взаимодействие с сервером App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="2b5e5-120">App-V 5.1 Server Interaction</span></span>


<span data-ttu-id="2b5e5-121">В этом разделе содержатся сведения о том, как взаимодействуют различные роли сервера App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-121">This section contains information about how the various App-V 5.1 server roles interact with each other.</span></span>

<span data-ttu-id="2b5e5-122">Сервер управления App-V 5,1 включает в себя репозиторий пакетов и их назначенные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-122">The App-V 5.1 Management Server contains the repository of packages and their assigned configurations.</span></span> <span data-ttu-id="2b5e5-123">Для серверов публикаций, которые зарегистрированы на сервере управления, связанные метаданные предоставляются на серверы публикаций, которые будут использоваться при получении запросов на обновление публикации с компьютеров, на которых запущен клиент App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-123">For Publishing Servers that are registered with the Management Server, the associated metadata is provided to the Publishing servers for use when publishing refresh requests are received from computers running the App-V 5.1 Client.</span></span> <span data-ttu-id="2b5e5-124">Серверы публикации App-V 5,1, управляемые с помощью одного сервера управления, могут поддерживать различные клиенты и могут иметь разные имена веб-сайтов и привязки портов.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-124">App-V 5.1 publishing servers managed by a single management server can be serving different clients and can have different website names and port bindings.</span></span> <span data-ttu-id="2b5e5-125">Кроме того, все серверы публикаций, управляемые одним сервером управления, являются репликами друг друга.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-125">Additionally, all Publishing Servers managed by the same Management Server are replicas of each other.</span></span>

<span data-ttu-id="2b5e5-126">**Примечание**  Сервер управления не выполняет балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-126">**Note** The Management Server does not perform any load balancing.</span></span> <span data-ttu-id="2b5e5-127">Связанные метаданные просто передаются на сервер публикаций для использования при обработке запросов клиентов.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-127">The associated metadata is simply passed to the publishing server for use when processing client requests.</span></span>

 

## <span data-ttu-id="2b5e5-128">Протоколы, связанные с сервером, и внешние возможности</span><span class="sxs-lookup"><span data-stu-id="2b5e5-128">Server-Related Protocols and External Features</span></span>


<span data-ttu-id="2b5e5-129">Ниже отображаются сведения о серверных протоколах, используемых серверами App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-129">The following displays information about server-related protocols used by the App-V 5.1 servers.</span></span> <span data-ttu-id="2b5e5-130">В таблице также есть механизм составления отчетов для каждого типа сервера.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-130">The table also includes the reporting mechanism for each server type.</span></span>

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
<th align="left"><span data-ttu-id="2b5e5-131">Тип сервера</span><span class="sxs-lookup"><span data-stu-id="2b5e5-131">Server Type</span></span></th>
<th align="left"><span data-ttu-id="2b5e5-132">Протоколы</span><span class="sxs-lookup"><span data-stu-id="2b5e5-132">Protocols</span></span></th>
<th align="left"><span data-ttu-id="2b5e5-133">Необходимые внешние функции</span><span class="sxs-lookup"><span data-stu-id="2b5e5-133">External Features Needed</span></span></th>
<th align="left"><span data-ttu-id="2b5e5-134">Отчеты</span><span class="sxs-lookup"><span data-stu-id="2b5e5-134">Reporting</span></span></th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2b5e5-135">Сервер IIS</span><span class="sxs-lookup"><span data-stu-id="2b5e5-135">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="2b5e5-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="2b5e5-136">HTTP</span></span></p>
<p><span data-ttu-id="2b5e5-137">HTTPS</span><span class="sxs-lookup"><span data-stu-id="2b5e5-137">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="2b5e5-138">Для этой комбинации протоколов сервера требуется механизм синхронизации содержимого между сервером управления и потоковым сервером.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-138">This server-protocol combination requires a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="2b5e5-139">При использовании HTTP или HTTPS используйте сервер IIS и брандмауэр, чтобы защитить сервер от доступа к Интернету.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-139">When using HTTP or HTTPS, use an IIS server and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2b5e5-140">внутренний</span><span class="sxs-lookup"><span data-stu-id="2b5e5-140">Internal</span></span></p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2b5e5-141">Файл</span><span class="sxs-lookup"><span data-stu-id="2b5e5-141">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="2b5e5-142">SMB</span><span class="sxs-lookup"><span data-stu-id="2b5e5-142">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2b5e5-143">Эта комбинация протоколов сервера должна поддерживать синхронизацию содержимого между сервером управления и потоковым сервером.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-143">This server-protocol combination requires support to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="2b5e5-144">Используйте клиентский компьютер с функцией обмена файлами или потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="2b5e5-144">Use a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2b5e5-145">внутренний</span><span class="sxs-lookup"><span data-stu-id="2b5e5-145">Internal</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="2b5e5-146">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2b5e5-146">Related topics</span></span>


[<span data-ttu-id="2b5e5-147">Планирование развертывания App-V</span><span class="sxs-lookup"><span data-stu-id="2b5e5-147">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="2b5e5-148">Развертывание сервера App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2b5e5-148">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

 

 





