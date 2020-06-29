---
title: Обзор сценария на основе использования сервера Application Virtualization Server
description: Обзор сценария на основе использования сервера Application Virtualization Server
author: dansimp
ms.assetid: 2d91392b-5085-4a5d-94f2-15eed1ed2928
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b3ac3f10a5b7c7705e6d72c122d52be801a6d50
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822092"
---
# <span data-ttu-id="6a8eb-103">Обзор сценария на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="6a8eb-103">Application Virtualization Server-Based Scenario Overview</span></span>


<span data-ttu-id="6a8eb-104">Если вы планируете использовать серверный сценарий развертывания для вашей среды виртуализации приложений (Майкрософт), важно понимать различия между *сервером управления виртуализацией приложений* и потоком данных сервера в *потоке Application Virtualization*.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the differences between the *Application Virtualization Management Server* and the *Application Virtualization Streaming Server*.</span></span> <span data-ttu-id="6a8eb-105">В этой статье описаны эти различия, а также сведения о методах доставки пакетов, протоколах передачи и внешних компонентах, которые необходимо учитывать при переходе к развертыванию.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-105">This topic describes those differences and also provides information about package delivery methods, transmission protocols, and external components that you will need to consider as you proceed with your deployment.</span></span>

## <span data-ttu-id="6a8eb-106">Сервер управления виртуализацией приложений</span><span class="sxs-lookup"><span data-stu-id="6a8eb-106">Application Virtualization Management Server</span></span>


<span data-ttu-id="6a8eb-107">Сервер управления виртуализацией приложений выполняет и функцию публикации, и потоковую функцию.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-107">The Application Virtualization Management Server performs both the publishing function and the streaming function.</span></span> <span data-ttu-id="6a8eb-108">Сервер публикует значки, ярлыки и сопоставления типов файлов для клиентов App-V для авторизованных пользователей.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-108">The server publishes application icons, shortcuts, and file type associations to the App-V clients for authorized users.</span></span> <span data-ttu-id="6a8eb-109">Когда пользователь запрашивает приложения, получаются потоки сервера, которые проявляются данными по требованию авторизованных пользователей, использующих протоколы RTSP или RTSP.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-109">When user requests for applications are received the server streams that data on-demand to authorized users using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="6a8eb-110">В большинстве конфигураций с помощью этого сервера один или несколько серверов управления используют общее хранилище данных для конфигурации и сведений о пакете.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-110">In most configurations using this server, one or more Management Servers share a common data store for configuration and package information.</span></span>

<span data-ttu-id="6a8eb-111">Серверы управления виртуализацией приложений используют группы Active Directory для управления авторизацией пользователей.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-111">The Application Virtualization Management Servers use Active Directory groups to manage user authorization.</span></span> <span data-ttu-id="6a8eb-112">Помимо доменных служб Active Directory для управления базой данных и хранилищем данных на этих серверах установлены SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-112">In addition to Active Directory Domain Services, these servers have SQL Server installed to manage the database and data store.</span></span> <span data-ttu-id="6a8eb-113">Управление сервером управления осуществляется с помощью консоли управления виртуализацией приложений, оснастке на консоль управления (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="6a8eb-113">The Management Server is controlled through the Application Virtualization Management Console, a snap-in to the Microsoft Management Console.</span></span>

<span data-ttu-id="6a8eb-114">Так как серверы управления виртуализацией приложений являются потоками приложений для конечных пользователей по запросу, эти серверы лучше всего подходят для конфигураций системы, которые обладают надежными и высокоскоростными сетями с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-114">Because the Application Virtualization Management Servers stream applications to end-users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span>

## <span data-ttu-id="6a8eb-115">Потоковый сервер Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6a8eb-115">Application Virtualization Streaming Server</span></span>


<span data-ttu-id="6a8eb-116">Потоковый сервер Application Virtualization обеспечивает такие же возможности по обновлению потоков и пакетов, предоставляемые сервером управления, но без требования к службе каталогов Active Directory или SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-116">The Application Virtualization Streaming Server delivers the same streaming and package upgrade capabilities provided by the Management Server, but without its Active Directory or SQL Server requirements.</span></span> <span data-ttu-id="6a8eb-117">Однако потоковый сервер не имеет службы публикации и не имеет возможностей лицензирования или измерения.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-117">However, the Streaming Server does not have a publishing service, nor does it have licensing or metering capabilities.</span></span> <span data-ttu-id="6a8eb-118">Служба публикации отдельного сервера управления App-V используется совместно с потоковым сервером App-V.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-118">The publishing service of a separate App-V Management Server is used in conjunction with the App-V Streaming Server.</span></span> <span data-ttu-id="6a8eb-119">Потоковый сервер App-V предназначен для бизнеса, которым требуется Виртуализация приложений в нескольких расположениях с помощью потоковых возможностей классической конфигурации сервера, но может не иметь инфраструктуры, поддерживающей серверы управления App-V в любом месте.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-119">The App-V Streaming Server addresses the needs of businesses that want to use Application Virtualization in multiple locations with the streaming capabilities of the classic server configuration but might not have the infrastructure to support App-V Management Servers in every location.</span></span>

<span data-ttu-id="6a8eb-120">Потоковый сервер Application Virtualization также может использоваться в средах с существующей электронной системой распространения программного обеспечения (ESD).</span><span class="sxs-lookup"><span data-stu-id="6a8eb-120">The Application Virtualization Streaming Server can also be used in environments with an existing electronic software distribution system (ESD).</span></span> <span data-ttu-id="6a8eb-121">С помощью ESD вы можете управлять потоковыми приложениями.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-121">You use the ESD to manage streaming applications.</span></span> <span data-ttu-id="6a8eb-122">В отличие от сервера управления виртуализацией приложений, потоковый сервер не использует SQL или консоль управления.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-122">Unlike the Application Virtualization Management Server, the Streaming Server does not use SQL or a management console.</span></span> <span data-ttu-id="6a8eb-123">Эти серверы используют списки управления доступом (ACL) для предоставления авторизации пользователей.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-123">These servers use access control lists (ACLs) to grant user authorization.</span></span>

## <span data-ttu-id="6a8eb-124">Способы доставки пакетов</span><span class="sxs-lookup"><span data-stu-id="6a8eb-124">Package Delivery Methods</span></span>


<span data-ttu-id="6a8eb-125">Если вы планируете использовать сервер Application Virtualization Server в качестве метода доставке публикации, необходимо определить, какой из указанных ниже методов доставки пакетов использует ваш сценарий.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-125">If you plan to use an Application Virtualization Server as the publishing delivery method, you need to determine which of the following package delivery methods your scenario employs:</span></span>

-   *<span data-ttu-id="6a8eb-126">Динамическое предоставление пакетов</span><span class="sxs-lookup"><span data-stu-id="6a8eb-126">Dynamic package delivery</span></span>*

-   *<span data-ttu-id="6a8eb-127">Загрузка из файлового пакета доставки</span><span class="sxs-lookup"><span data-stu-id="6a8eb-127">Load from file package delivery</span></span>*

### <span data-ttu-id="6a8eb-128">Динамическое предоставление пакетов</span><span class="sxs-lookup"><span data-stu-id="6a8eb-128">Dynamic Package Delivery</span></span>

<span data-ttu-id="6a8eb-129">При динамическом доставке пакета сервер (сервер управления виртуализацией приложений, сервер потоков виртуализации приложений или сервер IIS) предоставляет виртуализованные приложения конечным пользователям, используя развертывание по запросу.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-129">During dynamic package delivery, the server (Application Virtualization Management Server, Application Virtualization Streaming Server, or IIS server) delivers the virtualized applications to the end users through on-demand deployment.</span></span> <span data-ttu-id="6a8eb-130">Сервер доставляет виртуализированные приложения и пакеты на клиентский компьютер только в том случае, если пользователь впервые пытается запустить приложение (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="6a8eb-130">The server delivers the virtualized applications and packages to a client computer only when a user first attempts to launch an application (on demand).</span></span> <span data-ttu-id="6a8eb-131">Сервер пересылает только блоки, необходимые для запуска приложения (основной блок функций).</span><span class="sxs-lookup"><span data-stu-id="6a8eb-131">The server streams only the blocks needed to start the application (primary feature block).</span></span> <span data-ttu-id="6a8eb-132">После того как основной блок функций доставляется клиенту, приложение запускается; Клиент не получает полное приложение (добавочное развертывание), если только клиенту не требуется доступ к части приложения, которая не включена в основной блок функций.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-132">After the primary feature block is delivered to the client, the application runs; the client does not receive the complete application (incremental deployment) unless the client needs access to a part of the application that is not included in the primary feature block.</span></span> <span data-ttu-id="6a8eb-133">Когда это происходит, клиент выполняет неупорядоченный запрос, а дополнительный блок функций передается клиенту в потоке.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-133">When this occurs, the client performs an out-of-sequence request and the secondary feature block is streamed to the client.</span></span> <span data-ttu-id="6a8eb-134">Динамическое предоставление пакетов позволяет быстро запускать приложение.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-134">Dynamic package delivery allows for rapid application launch.</span></span>

### <span data-ttu-id="6a8eb-135">Загрузка из файлового пакета доставки</span><span class="sxs-lookup"><span data-stu-id="6a8eb-135">Load from File Package Delivery</span></span>

<span data-ttu-id="6a8eb-136">Для загрузки из файлового пакета сервер доставляет весь пакет виртуализированного приложения на клиентский компьютер, прежде чем пользователь запустит приложение.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-136">For load from file package delivery, the server delivers the entire virtualized application package to a client computer before the user launches the application.</span></span> <span data-ttu-id="6a8eb-137">В этом сценарии виртуализированные приложения доставляются в виде полного пакета, а не через динамический, добавочный метод, который используется моделью динамической доставки.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-137">In this scenario, virtualized applications are delivered as a full package, rather than through the dynamic, incremental method used by the dynamic delivery model.</span></span>

<span data-ttu-id="6a8eb-138">**Примечание**  Для каждого метода доставки первоначальный виртуальный процесс доставки приложения и процесс обновления виртуального приложения одинаковы. обновленный виртуальный пакет приложений заменяет исходный пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-138">**Note** For each delivery method, the initial virtual application delivery process and the virtual application update process are the same; the updated virtual application package replaces the original application package.</span></span>

 

<span data-ttu-id="6a8eb-139">В таблице ниже сравниваются преимущества и недостатки каждого метода доставки пакетов.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-139">The following table compares the advantages and disadvantages of each package delivery method.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a8eb-140">Метод</span><span class="sxs-lookup"><span data-stu-id="6a8eb-140">Method</span></span></th>
<th align="left"><span data-ttu-id="6a8eb-141">Преимущества</span><span class="sxs-lookup"><span data-stu-id="6a8eb-141">Advantages</span></span></th>
<th align="left"><span data-ttu-id="6a8eb-142">Недостатки</span><span class="sxs-lookup"><span data-stu-id="6a8eb-142">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="6a8eb-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a8eb-143">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a8eb-144">Динамическое предоставление пакетов</span><span class="sxs-lookup"><span data-stu-id="6a8eb-144">Dynamic package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-145">Приложения доставляются и обновляются по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-145">Applications are delivered and updated on demand.</span></span></p>
<p><span data-ttu-id="6a8eb-146">Приложения доставляются и обновляются постепенно, чтобы оптимизировать время запуска.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-146">Applications are delivered and updated incrementally to optimize launch time.</span></span></p>
<p><span data-ttu-id="6a8eb-147">Обновления будут автоматически доставлены на Рабочий стол клиента.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-147">Updates are delivered automatically to the client desktop.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-148">Более крупный объем в корпоративной топологии из-за требований к серверу.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-148">Larger footprint in enterprise topology because of server requirements.</span></span></p>
<p><span data-ttu-id="6a8eb-149">Потоки приложения должны быть в локальной сети. сценарии развертывания в глобальной сети или использование ненадежных или периодических соединений между сервером и клиентом могут быть непригодными для использования.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-149">Application streaming should be over a LAN; deployment scenarios over a WAN or that use an unreliable or intermittent connection between the server and client might be unusable.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-150">Требуется инфраструктура потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-150">Requires a streaming infrastructure.</span></span></p>
<p><span data-ttu-id="6a8eb-151">Установщик Windows, который используется для развертывания клиентского программного обеспечения для настольных систем виртуализации приложений на компьютеры конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-151">Windows Installer used to deploy Application Virtualization Desktop Client software to end-user computers.</span></span></p>
<p><span data-ttu-id="6a8eb-152">Крупные предприятия должны использовать серверы потоков виртуализации приложений в качестве точек распространения.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-152">Large enterprises should use Application Virtualization Streaming Servers as distribution points.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a8eb-153">Загрузка из файлового пакета доставки</span><span class="sxs-lookup"><span data-stu-id="6a8eb-153">Load from file package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-154">В соответствии с типичными методиками управления предприятием.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-154">Consistent with typical enterprise management practices.</span></span></p>
<p><span data-ttu-id="6a8eb-155">Поддержка изолированного сценария конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-155">Supports stand-alone configuration scenario.</span></span></p>
<p><span data-ttu-id="6a8eb-156">Предоставляет решение для Micro-проблемы с офисом филиала.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-156">Provides solution to micro–branch office problem.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-157">Доставка и обновление приложения по запросу невозможны.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-157">Application delivery and update is not possible on-demand.</span></span></p>
<p><span data-ttu-id="6a8eb-158">Доставка и обновление приложения не являются инкрементными. Это увеличивает потребление ресурсов относительно динамической доставки.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-158">Application delivery and update is not incremental; it increases resource consumption relative to dynamic delivery.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-159">ИТ – организация часто отвечает за управление лицензиями приложений, авторизацией пользователей и проверкой подлинности.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-159">The IT organization is often responsible for managing application licenses, user authorization, and authentication.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6a8eb-160">Протоколы, связанные с сервером, и внешние компоненты</span><span class="sxs-lookup"><span data-stu-id="6a8eb-160">Server-Related Protocols and External Components</span></span>


<span data-ttu-id="6a8eb-161">В приведенной ниже таблице перечислены типы серверов, которые можно использовать в серверных сценариях виртуализации приложений, а также их соответствующие протоколы передачи и внешние компоненты, необходимые для поддержки конкретной конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-161">The following table lists the server types that can be used in an Application Virtualization Server-based scenarios, along with their corresponding transmission protocols and the external components needed to support the specific server configuration.</span></span> <span data-ttu-id="6a8eb-162">В таблице также есть механизм отчетов и активный механизм обновления для каждого типа сервера.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-162">The table also includes the reporting mechanism and the active upgrade mechanism for each server type.</span></span> <span data-ttu-id="6a8eb-163">Так как в этих сценариях используется сервер управления виртуализацией приложений, вы можете использовать встроенные в систему функции отчетов.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-163">Because these scenarios all use the Application Virtualization Management Server, you can use the internal reporting functionality that is built into the system.</span></span> <span data-ttu-id="6a8eb-164">Если вы используете управление виртуализацией приложений или потоковый сервер Application Virtualization для доставки пакетов клиенту, пакеты на сервере автоматически обновляются, когда пользователь входит в систему клиента; Если вы используете серверы IIS или файл для доставки пакетов клиенту, пакеты на клиенте необходимо обновить вручную.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-164">If you use an Application Virtualization Management or an Application Virtualization Streaming Server to deliver packages to the client, packages on the server are automatically upgraded when a user logs into the client; if you use IIS servers or a file to deliver the packages to the client, the packages on the client must be upgraded manually.</span></span>

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
<th align="left"><span data-ttu-id="6a8eb-165">Тип сервера</span><span class="sxs-lookup"><span data-stu-id="6a8eb-165">Server Type</span></span></th>
<th align="left"><span data-ttu-id="6a8eb-166">Протоколы</span><span class="sxs-lookup"><span data-stu-id="6a8eb-166">Protocols</span></span></th>
<th align="left"><span data-ttu-id="6a8eb-167">Нужны внешние компоненты</span><span class="sxs-lookup"><span data-stu-id="6a8eb-167">External Components Needed</span></span></th>
<th align="left"><span data-ttu-id="6a8eb-168">Отчеты</span><span class="sxs-lookup"><span data-stu-id="6a8eb-168">Reporting</span></span></th>
<th align="left"><span data-ttu-id="6a8eb-169">Активное обновление</span><span class="sxs-lookup"><span data-stu-id="6a8eb-169">Active Upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a8eb-170">Сервер управления виртуализацией приложений</span><span class="sxs-lookup"><span data-stu-id="6a8eb-170">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-171">Протокол</span><span class="sxs-lookup"><span data-stu-id="6a8eb-171">RTSP</span></span></p>
<p><span data-ttu-id="6a8eb-172">RTSP</span><span class="sxs-lookup"><span data-stu-id="6a8eb-172">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-173">При использовании HTTPS-сервера используйте сервер IIS для загрузки файлов ICO и OSD и брандмауэра, чтобы защитить сервер от доступа к Интернету.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-173">When using HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-174">внутренний</span><span class="sxs-lookup"><span data-stu-id="6a8eb-174">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-175">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="6a8eb-175">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a8eb-176">Потоковый сервер Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6a8eb-176">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-177">Протокол</span><span class="sxs-lookup"><span data-stu-id="6a8eb-177">RTSP</span></span></p>
<p><span data-ttu-id="6a8eb-178">RTSP</span><span class="sxs-lookup"><span data-stu-id="6a8eb-178">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-179">Используйте механизм для синхронизации содержимого между сервером управления и потоковым сервером.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-179">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="6a8eb-180">При использовании HTTPS используйте сервер IIS для загрузки файлов ICO и OSD и используйте брандмауэр, чтобы защитить сервер от доступа к Интернету.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-180">When using HTTPS, use an IIS server to download ICO and OSD files and use a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-181">внутренний</span><span class="sxs-lookup"><span data-stu-id="6a8eb-181">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-182">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="6a8eb-182">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a8eb-183">Сервер IIS</span><span class="sxs-lookup"><span data-stu-id="6a8eb-183">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-184">HTTP</span><span class="sxs-lookup"><span data-stu-id="6a8eb-184">HTTP</span></span></p>
<p><span data-ttu-id="6a8eb-185">HTTPS</span><span class="sxs-lookup"><span data-stu-id="6a8eb-185">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-186">Используйте механизм для синхронизации содержимого между сервером управления и потоковым сервером.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-186">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="6a8eb-187">При использовании HTTP или HTTPS используйте сервер IIS для загрузки файлов ICO и OSD и брандмауэра, чтобы защитить сервер от доступа к Интернету.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-187">When using HTTP or HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-188">внутренний</span><span class="sxs-lookup"><span data-stu-id="6a8eb-188">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-189">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6a8eb-189">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a8eb-190">Файл</span><span class="sxs-lookup"><span data-stu-id="6a8eb-190">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-191">SMB</span><span class="sxs-lookup"><span data-stu-id="6a8eb-191">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-192">Вам необходим способ синхронизации содержимого между сервером управления и потоковым сервером.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-192">You need a way to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="6a8eb-193">Вам нужен клиентский компьютер с функцией обмена файлами или потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="6a8eb-193">You need a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-194">внутренний</span><span class="sxs-lookup"><span data-stu-id="6a8eb-194">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a8eb-195">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6a8eb-195">Not Supported</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6a8eb-196">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="6a8eb-196">Related topics</span></span>


[<span data-ttu-id="6a8eb-197">Сценарий на основе электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="6a8eb-197">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="6a8eb-198">Настройка серверов для развертывания на основе сервера</span><span class="sxs-lookup"><span data-stu-id="6a8eb-198">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="6a8eb-199">Установка серверов и компонентов системы</span><span class="sxs-lookup"><span data-stu-id="6a8eb-199">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





