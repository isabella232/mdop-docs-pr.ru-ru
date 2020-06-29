---
title: Планирование загрузки App-V 5.0
description: Планирование загрузки App-V 5.0
author: dansimp
ms.assetid: 56f48b00-cd91-4280-9481-5372a0e2e792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e828457a286f6f686c227a935828679514d87ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814853"
---
# <span data-ttu-id="72fb3-103">Планирование загрузки App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="72fb3-103">App-V 5.0 Capacity Planning</span></span>


<span data-ttu-id="72fb3-104">Перечисленные ниже рекомендации можно использовать в качестве базового плана, чтобы определить сведения о планировании мощности, соответствующие инфраструктуре App-V 5,0 в Организации.</span><span class="sxs-lookup"><span data-stu-id="72fb3-104">The following recommendations can be used as a baseline to help determine capacity planning information that is appropriate to your organization’s App-V 5.0 infrastructure.</span></span>

<span data-ttu-id="72fb3-105">**Важно!**  Данные в этом разделе используются только в качестве общего руководства по планированию развертывания приложения-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="72fb3-105">**Important** Use the information in this section only as a general guide for planning your App-V 5.0 deployment.</span></span> <span data-ttu-id="72fb3-106">Требования к системной мощности будут зависеть от конкретных сведений о вашем оборудовании и среде приложений.</span><span class="sxs-lookup"><span data-stu-id="72fb3-106">Your system capacity requirements will depend on the specific details of your hardware and application environment.</span></span> <span data-ttu-id="72fb3-107">Кроме того, в этом документе отображаются номера производительности, которые можно увидеть, и результаты могут отличаться.</span><span class="sxs-lookup"><span data-stu-id="72fb3-107">Additionally, the performance numbers displayed in this document are examples and your results may vary.</span></span>

 

## <span data-ttu-id="72fb3-108">Определение области охвата проекта</span><span class="sxs-lookup"><span data-stu-id="72fb3-108">Determine the Project Scope</span></span>


<span data-ttu-id="72fb3-109">Прежде чем приступить к разработке инфраструктуры App-V 5,0, необходимо определить область проекта.</span><span class="sxs-lookup"><span data-stu-id="72fb3-109">Before you design the App-V 5.0 infrastructure, you must determine the project’s scope.</span></span> <span data-ttu-id="72fb3-110">Область действия состоит из определения того, какие приложения будут доступны для выполнения практически и для определения конечных пользователей, и их расположения.</span><span class="sxs-lookup"><span data-stu-id="72fb3-110">The scope consists of determining which applications will be available virtually and to also identify the target users, and their locations.</span></span> <span data-ttu-id="72fb3-111">Эта информация поможет вам определить, какой тип инфраструктуры App-V 5,0 следует реализовать.</span><span class="sxs-lookup"><span data-stu-id="72fb3-111">This information will help determine what type of App-V 5.0 infrastructure should be implemented.</span></span> <span data-ttu-id="72fb3-112">Решения, касающиеся области охвата проекта, должны основываться на конкретных требованиях вашей организации.</span><span class="sxs-lookup"><span data-stu-id="72fb3-112">Decisions about the scope of the project must be based on the specific needs of your organization.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72fb3-113">Задача</span><span class="sxs-lookup"><span data-stu-id="72fb3-113">Task</span></span></th>
<th align="left"><span data-ttu-id="72fb3-114">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="72fb3-114">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-115">Определение области применения приложения</span><span class="sxs-lookup"><span data-stu-id="72fb3-115">Determine Application Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="72fb3-116">В зависимости от виртуализированных приложений инфраструктура App-V 5,0 может быть настроена различными способами.</span><span class="sxs-lookup"><span data-stu-id="72fb3-116">Depending on the applications to be virtualized, the App-V 5.0 infrastructure can be set up in different ways.</span></span> <span data-ttu-id="72fb3-117">Первая задача — определить приложения, которые нужно виртуализировать.</span><span class="sxs-lookup"><span data-stu-id="72fb3-117">The first task is to define what applications you want to virtualize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72fb3-118">Определение области расположения</span><span class="sxs-lookup"><span data-stu-id="72fb3-118">Determine Location Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="72fb3-119">Область расположения — это физическое расположение (например, в масштабах всей организации или в определенном географическом расположении), в котором планируется запускать виртуализированные приложения.</span><span class="sxs-lookup"><span data-stu-id="72fb3-119">Location scope refers to the physical locations (for example, enterprise-wide or a specific geographic location) where you plan to run the virtualized applications.</span></span> <span data-ttu-id="72fb3-120">Она также может ссылаться на заполнение пользователей (например, один отдел), который будет запускать виртуальные приложения.</span><span class="sxs-lookup"><span data-stu-id="72fb3-120">It can also refer to the user population (for example, a single department) who will run the virtual applications.</span></span> <span data-ttu-id="72fb3-121">Вы должны получить карту сети, которая содержит пути подключения, а также пропускную способность для каждого места и количество пользователей, использующих виртуализированные приложения и скорость связи WAN.</span><span class="sxs-lookup"><span data-stu-id="72fb3-121">You should obtain a network map that includes the connection paths as well as available bandwidth to each location and the number of users using virtualized applications and the WAN link speed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="72fb3-122">Определение необходимости инфраструктуры App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="72fb3-122">Determine Which App-V 5.0 Infrastructure is Required</span></span>


<span data-ttu-id="72fb3-123">**Важно!**  Для обеих следующих моделей на компьютере, на котором планируется запускать виртуальные приложения, должен быть установлен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="72fb3-123">**Important** Both of the following models require the App-V 5.0 client to be installed on the computer where you plan to run virtual applications.</span></span>

<span data-ttu-id="72fb3-124">Вы также можете управлять средой App-V 5,0 с помощью электронного решения для рассылки программного обеспечения (ESD), такого как Microsoft Systems Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="72fb3-124">You can also manage your App-V 5.0 environment using an Electronic Software Distribution (ESD) solution such as Microsoft Systems Center Configuration Manager.</span></span> <span data-ttu-id="72fb3-125">Дополнительные сведения можно найти в разделе [Развертывание пакетов приложений для App-V 5,0 с помощью электронного распространения программного обеспечения (ESD)](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md).</span><span class="sxs-lookup"><span data-stu-id="72fb3-125">For more information see [Deploying App-V 5.0 Packages by Using Electronic Software Distribution (ESD)](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md).</span></span>

 

-   <span data-ttu-id="72fb3-126">**Отдельная модель** : Автономная модель позволяет использовать для распространения виртуальные приложения, поддерживающие установщик Windows, без потоковой передачи данных.</span><span class="sxs-lookup"><span data-stu-id="72fb3-126">**Standalone Model** - The standalone model allows virtual applications to be Windows Installer-enabled for distribution without streaming.</span></span> <span data-ttu-id="72fb3-127">App-V 5,0 в автономном режиме состоит из секвенсора и клиента; Дополнительные компоненты не требуются.</span><span class="sxs-lookup"><span data-stu-id="72fb3-127">App-V 5.0 in Standalone Mode consists of the sequencer and the client; no additional components are required.</span></span> <span data-ttu-id="72fb3-128">Приложения подготавливаются для виртуализации с помощью процессов, которые называются виртуализацией.</span><span class="sxs-lookup"><span data-stu-id="72fb3-128">Applications are prepared for virtualization using a process called sequencing.</span></span> <span data-ttu-id="72fb3-129">Дополнительные сведения можно найти [в разделе Планирование приложения Sequencer-V 5,0 и развертывание клиента](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="72fb3-129">For more information see, [Planning for the App-V 5.0 Sequencer and Client Deployment](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span></span> <span data-ttu-id="72fb3-130">Изолированная модель рекомендуется для следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="72fb3-130">The stand-alone model is recommended for the following scenarios:</span></span>

    -   <span data-ttu-id="72fb3-131">С отключенными удаленными пользователями, которые не могут подключиться к инфраструктуре App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="72fb3-131">With disconnected remote users who cannot connect to the App-V 5.0 infrastructure.</span></span>

    -   <span data-ttu-id="72fb3-132">При запуске системы управления программным обеспечением, например Configuration Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="72fb3-132">When you are running a software management system, such as Configuration Manager 2012.</span></span>

    -   <span data-ttu-id="72fb3-133">Если ограничения пропускной способности сети задерживает электронное распространение программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="72fb3-133">When network bandwidth limitations inhibit electronic software distribution.</span></span>

-   <span data-ttu-id="72fb3-134">**Полная модель инфраструктуры** — полная модель инфраструктуры предоставляет возможности распространения программного обеспечения, управления и создания отчетов; Она также включает потоковую передачу приложений по сети.</span><span class="sxs-lookup"><span data-stu-id="72fb3-134">**Full Infrastructure Model** - The full infrastructure model provides for software distribution, management, and reporting capabilities; it also includes the streaming of applications across the network.</span></span> <span data-ttu-id="72fb3-135">Модель полной инфраструктуры App-V 5,0 состоит из одного или нескольких серверов управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="72fb3-135">The App-V 5.0 Full Infrastructure Model consists of one or more App-V 5.0 management servers.</span></span> <span data-ttu-id="72fb3-136">Сервер управления можно использовать для публикации приложений на всех клиентах.</span><span class="sxs-lookup"><span data-stu-id="72fb3-136">The Management Server can be used to publish applications to all clients.</span></span> <span data-ttu-id="72fb3-137">Процесс публикации поместит значки виртуальных приложений и ярлыки на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="72fb3-137">The publishing process places the virtual application icons and shortcuts on the target computer.</span></span> <span data-ttu-id="72fb3-138">Кроме того, он может выполнять потоковую передачу приложений для локальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="72fb3-138">It can also stream applications to local users.</span></span> <span data-ttu-id="72fb3-139">Дополнительные сведения об установке сервера управления можно найти в разделе [Планирование развертывания сервера App-V 5,0](planning-for-the-app-v-50-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="72fb3-139">For more information about installing the management server see, [Planning for the App-V 5.0 Server Deployment](planning-for-the-app-v-50-server-deployment.md).</span></span> <span data-ttu-id="72fb3-140">Полная модель инфраструктуры рекомендуется для следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="72fb3-140">The full infrastructure model is recommended for the following scenarios:</span></span>

    <span data-ttu-id="72fb3-141">**Важно!**  Для модели App-V 5,0 в полной инфраструктуре инфраструктуры требуется Microsoft SQL Server для хранения данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="72fb3-141">**Important** The App-V 5.0 full infrastructure model requires Microsoft SQL Server to store configuration data.</span></span> <span data-ttu-id="72fb3-142">Дополнительные сведения см. в разделе [Поддерживаемые конфигурации App-V 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="72fb3-142">For more information see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

     

    -   <span data-ttu-id="72fb3-143">Если вы хотите опубликовать приложение на целевом компьютере с помощью сервера управления.</span><span class="sxs-lookup"><span data-stu-id="72fb3-143">When you want to use the Management Server to publish the application to target computers.</span></span>

    -   <span data-ttu-id="72fb3-144">Для быстрой подготовки приложений к целевым компьютерам.</span><span class="sxs-lookup"><span data-stu-id="72fb3-144">For rapid provisioning of applications to target computers.</span></span>

    -   <span data-ttu-id="72fb3-145">Если вы хотите использовать отчеты App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="72fb3-145">When you want to use App-V 5.0 reporting.</span></span>

## <span data-ttu-id="72fb3-146">Рекомендации по выбору размера для сквозного сервера</span><span class="sxs-lookup"><span data-stu-id="72fb3-146">End-to-end Server Sizing Guidance</span></span>


<span data-ttu-id="72fb3-147">В следующем разделе содержатся сведения о сквозном изменении размера и планировании приложения App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="72fb3-147">The following section provides information about end-to-end App-V 5.0 sizing and planning.</span></span> <span data-ttu-id="72fb3-148">Более подробную информацию можно найти в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="72fb3-148">For more specific information, refer to the subsequent sections.</span></span>

<span data-ttu-id="72fb3-149">**Примечание**  Время ответа на клиенте в цикле обработки — это время, затраченное на работу компьютера, на котором запущен клиент App-V 5,0, чтобы получить успешное уведомление от сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="72fb3-149">**Note** Round trip response time on the client is the time taken by the computer running the App-V 5.0 client to receive a successful notification from the publishing server.</span></span> <span data-ttu-id="72fb3-150">Время ответа цикла обработки на сервере публикаций — это время, потребовавшееся на компьютере, на котором запущен сервер публикаций, для получения успешно обновленных метаданных пакета с сервера управления.</span><span class="sxs-lookup"><span data-stu-id="72fb3-150">Round trip response time on the publishing server is the time taken by the computer running the publishing server to receive a successful package metadata update from the management server.</span></span>

 

-   <span data-ttu-id="72fb3-151">Клиенты 20 000 могут ориентироваться на один сервер публикаций для получения пакета в приемлемое время кругового приема.</span><span class="sxs-lookup"><span data-stu-id="72fb3-151">20,000 clients can target a single publishing server to obtain the package refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="72fb3-152">( &lt; 3 секунды)</span><span class="sxs-lookup"><span data-stu-id="72fb3-152">(&lt;3 seconds)</span></span>

-   <span data-ttu-id="72fb3-153">Один сервер управления может поддерживать до 50 серверов публикации для метаданных пакета в течение приемлемого времени приема-передачи.</span><span class="sxs-lookup"><span data-stu-id="72fb3-153">A single management server can support up to 50 publishing servers for package metadata refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="72fb3-154">( &lt; 5 секунд)</span><span class="sxs-lookup"><span data-stu-id="72fb3-154">(&lt;5 seconds)</span></span>

## <a href="" id="---------app-v-5-0-management-server-capacity-planning-recommendations"></a> <span data-ttu-id="72fb3-155">Рекомендации по планированию производительности сервера управления для App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="72fb3-155">App-V 5.0 Management Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="72fb3-156">Для серверов публикаций App-V 5,0 требуется сервер управления для запросов на обновление пакетов и ответов на обновление пакетов.</span><span class="sxs-lookup"><span data-stu-id="72fb3-156">The App-V 5.0 publishing servers require the management server for package refresh requests and package refresh responses.</span></span> <span data-ttu-id="72fb3-157">Затем сервер управления отправляет сведения в базу данных управления для получения информации.</span><span class="sxs-lookup"><span data-stu-id="72fb3-157">The management server then sends the information to the management database to retrieve information.</span></span> <span data-ttu-id="72fb3-158">Дополнительные сведения о конфигурациях, поддерживаемых сервером управления App-V 5,0, приведены в разделе [Поддерживаемые конфигурации App-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="72fb3-158">For more information about App-V 5.0 management server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="72fb3-159">**Примечание**  Время обновления по умолчанию на сервере публикаций App-V 5,0 составляет десять минут.</span><span class="sxs-lookup"><span data-stu-id="72fb3-159">**Note** The default refresh time on the App-V 5.0 publishing server is ten minutes.</span></span>

 

<span data-ttu-id="72fb3-160">При обращении нескольких одновременных серверов публикаций к единому серверу управления для обновления метаданных пакета на сервере публикаций влияют следующие три фактора.</span><span class="sxs-lookup"><span data-stu-id="72fb3-160">When multiple simultaneous publishing servers contact a single management server for package metadata refreshes, the following three factors influence the round trip response time on the publishing server:</span></span>

1.  <span data-ttu-id="72fb3-161">Количество серверов публикаций, выполняющих одновременные запросы.</span><span class="sxs-lookup"><span data-stu-id="72fb3-161">Number of publishing servers making simultaneous requests.</span></span>

2.  <span data-ttu-id="72fb3-162">Количество групп подключений, настроенных на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="72fb3-162">Number of connection groups configured on the management server.</span></span>

3.  <span data-ttu-id="72fb3-163">Количество групп доступа, настроенных на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="72fb3-163">Number of access groups configured on the management server.</span></span>

<span data-ttu-id="72fb3-164">В следующей таблице приведены дополнительные сведения о каждом факторе, влияющем на время приема круга.</span><span class="sxs-lookup"><span data-stu-id="72fb3-164">The following table displays more information about each factor that impacts round trip time.</span></span>

<span data-ttu-id="72fb3-165">**Примечание**  Время ответа цикла обработки — это время, потребовавшееся на компьютере, на котором работает сервер публикаций App-V 5,0, чтобы получить успешное обновление метаданных пакета от сервера управления.</span><span class="sxs-lookup"><span data-stu-id="72fb3-165">**Note** Round trip response time is the time taken by the computer running the App-V 5.0 publishing server to receive a successful package metadata update from the management server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72fb3-166">Факторы, влияющие на время ответа кругового цикла</span><span class="sxs-lookup"><span data-stu-id="72fb3-166">Factors impacting round trip response time</span></span></th>
<th align="left"><span data-ttu-id="72fb3-167">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="72fb3-167">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-168">Количество серверов публикаций, запрашивающих обновление метаданных пакета одновременно.</span><span class="sxs-lookup"><span data-stu-id="72fb3-168">The number of publishing servers simultaneously requesting package metadata refreshes.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-169">Один сервер управления может отвечать на запросы до 320 серверов публикаций, запрашивающих публикацию метаданных одновременно.</span><span class="sxs-lookup"><span data-stu-id="72fb3-169">A single management server can respond to up to 320 publishing servers requesting publishing metadata simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="72fb3-170">Время ответа на запрос в формате кругового приема для 320 Pub Server составляет ~ 40 секунд.</span><span class="sxs-lookup"><span data-stu-id="72fb3-170">Round trip response time for 320 pub servers is ~40 seconds.</span></span></p></li>
<li><p><span data-ttu-id="72fb3-171">Для &lt; серверов публикаций 50 с запросом метаданных одновременно время ответа цикла обработки составляет &lt; 5 секунд.</span><span class="sxs-lookup"><span data-stu-id="72fb3-171">For &lt;50 publishing servers requesting metadata simultaneously, the round trip response time is &lt;5 seconds.</span></span></p></li>
<li><p><span data-ttu-id="72fb3-172">Время отклика от 50 до 320 сервера публикаций повышается линейно (примерно 2x).</span><span class="sxs-lookup"><span data-stu-id="72fb3-172">From 50 to 320 publishing servers, the response time increases linearly (approximately 2x).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72fb3-173">Количество групп подключений, настроенных на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="72fb3-173">The number of connection groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-174">Для групп соединений до 100 не существует значительных изменений в времени ответа на цикл обработки на сервере публикации.</span><span class="sxs-lookup"><span data-stu-id="72fb3-174">For up to 100 connection groups, there is no significant change in the round trip response time on the publishing server.</span></span></p></li>
<li><p><span data-ttu-id="72fb3-175">Для групп соединений 100-400 существует незначительное линейное приращение времени ответа цикла обработки.</span><span class="sxs-lookup"><span data-stu-id="72fb3-175">For 100 - 400 connection groups, there is a minor linear increase in the round trip response time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-176">Количество групп доступа, настроенных на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="72fb3-176">The number of access groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-177">Для групп доступа до 40 имеется линейное (примерно 3x) приращение времени ответа на время приема-передачи на сервере публикации.</span><span class="sxs-lookup"><span data-stu-id="72fb3-177">For up to 40 access groups, there is a linear (approximately 3x) increase in the round trip response time on the publishing server.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="72fb3-178">В следующей таблице показаны примеры значений для каждого из предыдущих факторов.</span><span class="sxs-lookup"><span data-stu-id="72fb3-178">The following table displays sample values for each of the previous factors.</span></span> <span data-ttu-id="72fb3-179">В каждом варианте пакеты 120 обновляются с сервера управления App-V 5.0.</span><span class="sxs-lookup"><span data-stu-id="72fb3-179">In each variation, 120 packages are refreshed from the App-V 5.0management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72fb3-180">Сценарий</span><span class="sxs-lookup"><span data-stu-id="72fb3-180">Scenario</span></span></th>
<th align="left"><span data-ttu-id="72fb3-181">Вариант</span><span class="sxs-lookup"><span data-stu-id="72fb3-181">Variation</span></span></th>
<th align="left"><span data-ttu-id="72fb3-182">Количество групп соединения</span><span class="sxs-lookup"><span data-stu-id="72fb3-182">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="72fb3-183">Количество групп доступа</span><span class="sxs-lookup"><span data-stu-id="72fb3-183">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="72fb3-184">Количество серверов публикаций</span><span class="sxs-lookup"><span data-stu-id="72fb3-184">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="72fb3-185">Сервер или сервер управления публикации типа сетевого подключения</span><span class="sxs-lookup"><span data-stu-id="72fb3-185">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="72fb3-186">Время ответа цикла обработки на сервере публикаций (в секундах)</span><span class="sxs-lookup"><span data-stu-id="72fb3-186">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="72fb3-187">Использование ЦП на сервере управления</span><span class="sxs-lookup"><span data-stu-id="72fb3-187">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-188">Серверы публикации одновременные связи с сервером управления для публикации метаданных.</span><span class="sxs-lookup"><span data-stu-id="72fb3-188">Publishing servers simultaneously contacting management server for publishing metadata.</span></span></p></td>
<td align="left"><p><span data-ttu-id="72fb3-189">Количество серверов публикаций</span><span class="sxs-lookup"><span data-stu-id="72fb3-189">Number of publishing servers</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-190">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-190">0</span></span></p></li>
<li><p><span data-ttu-id="72fb3-191">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-191">0</span></span></p></li>
<li><p><span data-ttu-id="72fb3-192">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-192">0</span></span></p></li>
<li><p><span data-ttu-id="72fb3-193">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-193">0</span></span></p></li>
<li><p><span data-ttu-id="72fb3-194">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-194">0</span></span></p></li>
<li><p><span data-ttu-id="72fb3-195">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-195">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-196">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-196">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-197">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-197">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-198">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-198">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-199">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-199">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-200">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-200">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-201">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-201">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-202">50</span><span class="sxs-lookup"><span data-stu-id="72fb3-202">50</span></span></p></li>
<li><p><span data-ttu-id="72fb3-203">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-203">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-204">200</span><span class="sxs-lookup"><span data-stu-id="72fb3-204">200</span></span></p></li>
<li><p><span data-ttu-id="72fb3-205">300</span><span class="sxs-lookup"><span data-stu-id="72fb3-205">300</span></span></p></li>
<li><p><span data-ttu-id="72fb3-206">315</span><span class="sxs-lookup"><span data-stu-id="72fb3-206">315</span></span></p></li>
<li><p><span data-ttu-id="72fb3-207">320</span><span class="sxs-lookup"><span data-stu-id="72fb3-207">320</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-208">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-208">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-209">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-209">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-210">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-210">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-211">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-211">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-212">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-212">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-213">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-213">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-214">5</span><span class="sxs-lookup"><span data-stu-id="72fb3-214">5</span></span></p></li>
<li><p><span data-ttu-id="72fb3-215">5-10</span><span class="sxs-lookup"><span data-stu-id="72fb3-215">10</span></span></p></li>
<li><p><span data-ttu-id="72fb3-216">19</span><span class="sxs-lookup"><span data-stu-id="72fb3-216">19</span></span></p></li>
<li><p><span data-ttu-id="72fb3-217">32</span><span class="sxs-lookup"><span data-stu-id="72fb3-217">32</span></span></p></li>
<li><p><span data-ttu-id="72fb3-218">30</span><span class="sxs-lookup"><span data-stu-id="72fb3-218">30</span></span></p></li>
<li><p><span data-ttu-id="72fb3-219">37</span><span class="sxs-lookup"><span data-stu-id="72fb3-219">37</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-220">18</span><span class="sxs-lookup"><span data-stu-id="72fb3-220">17</span></span></p></li>
<li><p><span data-ttu-id="72fb3-221">18</span><span class="sxs-lookup"><span data-stu-id="72fb3-221">17</span></span></p></li>
<li><p><span data-ttu-id="72fb3-222">18</span><span class="sxs-lookup"><span data-stu-id="72fb3-222">17</span></span></p></li>
<li><p><span data-ttu-id="72fb3-223">10-15</span><span class="sxs-lookup"><span data-stu-id="72fb3-223">15</span></span></p></li>
<li><p><span data-ttu-id="72fb3-224">18</span><span class="sxs-lookup"><span data-stu-id="72fb3-224">17</span></span></p></li>
<li><p><span data-ttu-id="72fb3-225">10-15</span><span class="sxs-lookup"><span data-stu-id="72fb3-225">15</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72fb3-226">Метаданные публикации содержат группы подключений</span><span class="sxs-lookup"><span data-stu-id="72fb3-226">Publishing metadata contains connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="72fb3-227">Количество групп соединения</span><span class="sxs-lookup"><span data-stu-id="72fb3-227">Number of connection groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-228">5-10</span><span class="sxs-lookup"><span data-stu-id="72fb3-228">10</span></span></p></li>
<li><p><span data-ttu-id="72fb3-229">50</span><span class="sxs-lookup"><span data-stu-id="72fb3-229">50</span></span></p></li>
<li><p><span data-ttu-id="72fb3-230">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-230">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-231">150</span><span class="sxs-lookup"><span data-stu-id="72fb3-231">150</span></span></p></li>
<li><p><span data-ttu-id="72fb3-232">300</span><span class="sxs-lookup"><span data-stu-id="72fb3-232">300</span></span></p></li>
<li><p><span data-ttu-id="72fb3-233">400</span><span class="sxs-lookup"><span data-stu-id="72fb3-233">400</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-234">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-234">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-235">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-235">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-236">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-236">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-237">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-237">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-238">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-238">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-239">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-239">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-240">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-240">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-241">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-241">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-242">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-242">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-243">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-243">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-244">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-244">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-245">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-245">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-246">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-246">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-247">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-247">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-248">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-248">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-249">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-249">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-250">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-250">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-251">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-251">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-252">5-10</span><span class="sxs-lookup"><span data-stu-id="72fb3-252">10</span></span></p></li>
<li><p><span data-ttu-id="72fb3-253">11</span><span class="sxs-lookup"><span data-stu-id="72fb3-253">11</span></span></p></li>
<li><p><span data-ttu-id="72fb3-254">11</span><span class="sxs-lookup"><span data-stu-id="72fb3-254">11</span></span></p></li>
<li><p><span data-ttu-id="72fb3-255">шестнадцат</span><span class="sxs-lookup"><span data-stu-id="72fb3-255">16</span></span></p></li>
<li><p><span data-ttu-id="72fb3-256">максималь</span><span class="sxs-lookup"><span data-stu-id="72fb3-256">22</span></span></p></li>
<li><p><span data-ttu-id="72fb3-257">24</span><span class="sxs-lookup"><span data-stu-id="72fb3-257">25</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-258">18</span><span class="sxs-lookup"><span data-stu-id="72fb3-258">17</span></span></p></li>
<li><p><span data-ttu-id="72fb3-259">19</span><span class="sxs-lookup"><span data-stu-id="72fb3-259">19</span></span></p></li>
<li><p><span data-ttu-id="72fb3-260">максималь</span><span class="sxs-lookup"><span data-stu-id="72fb3-260">22</span></span></p></li>
<li><p><span data-ttu-id="72fb3-261">19</span><span class="sxs-lookup"><span data-stu-id="72fb3-261">19</span></span></p></li>
<li><p><span data-ttu-id="72fb3-262">средняя</span><span class="sxs-lookup"><span data-stu-id="72fb3-262">20</span></span></p></li>
<li><p><span data-ttu-id="72fb3-263">средняя</span><span class="sxs-lookup"><span data-stu-id="72fb3-263">20</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-264">Метаданные публикации содержат группы доступа</span><span class="sxs-lookup"><span data-stu-id="72fb3-264">Publishing metadata contains access groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="72fb3-265">Количество групп доступа</span><span class="sxs-lookup"><span data-stu-id="72fb3-265">Number of access groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-266">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-266">0</span></span></p></li>
<li><p><span data-ttu-id="72fb3-267">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-267">0</span></span></p></li>
<li><p><span data-ttu-id="72fb3-268">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-268">0</span></span></p></li>
<li><p><span data-ttu-id="72fb3-269">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-269">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-270">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-270">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-271">5-10</span><span class="sxs-lookup"><span data-stu-id="72fb3-271">10</span></span></p></li>
<li><p><span data-ttu-id="72fb3-272">средняя</span><span class="sxs-lookup"><span data-stu-id="72fb3-272">20</span></span></p></li>
<li><p><span data-ttu-id="72fb3-273">40</span><span class="sxs-lookup"><span data-stu-id="72fb3-273">40</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-274">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-274">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-275">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-275">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-276">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-276">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-277">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-277">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-278">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-278">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-279">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-279">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-280">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-280">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-281">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-281">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-282">5-10</span><span class="sxs-lookup"><span data-stu-id="72fb3-282">10</span></span></p></li>
<li><p><span data-ttu-id="72fb3-283">43</span><span class="sxs-lookup"><span data-stu-id="72fb3-283">43</span></span></p></li>
<li><p><span data-ttu-id="72fb3-284">153</span><span class="sxs-lookup"><span data-stu-id="72fb3-284">153</span></span></p></li>
<li><p><span data-ttu-id="72fb3-285">535</span><span class="sxs-lookup"><span data-stu-id="72fb3-285">535</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-286">18</span><span class="sxs-lookup"><span data-stu-id="72fb3-286">17</span></span></p></li>
<li><p><span data-ttu-id="72fb3-287">26</span><span class="sxs-lookup"><span data-stu-id="72fb3-287">26</span></span></p></li>
<li><p><span data-ttu-id="72fb3-288">24</span><span class="sxs-lookup"><span data-stu-id="72fb3-288">24</span></span></p></li>
<li><p><span data-ttu-id="72fb3-289">24</span><span class="sxs-lookup"><span data-stu-id="72fb3-289">24</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="72fb3-290">Загрузка ЦП на компьютере, на котором работает сервер управления, составляет около 25%, независимо от количества серверов публикации, на которых она нацелена.</span><span class="sxs-lookup"><span data-stu-id="72fb3-290">The CPU utilization of the computer running the management server is around 25% irrespective of the number of publishing servers targeting it.</span></span> <span data-ttu-id="72fb3-291">Количество транзакций в базе данных Microsoft SQL Server (в секунду) запросы пакетов в секунду и соединения пользователя идентичны, независимо от количества серверов публикации.</span><span class="sxs-lookup"><span data-stu-id="72fb3-291">The Microsoft SQL Server database transactions/sec, batch requests/sec and user connections are identical irrespective of the number of publishing servers.</span></span> <span data-ttu-id="72fb3-292">Например: Transactions/sec составляет ~ 30, пакетные запросы ~ 200, а пользователь соединяет ~ 6.</span><span class="sxs-lookup"><span data-stu-id="72fb3-292">For example: Transactions/sec is ~30, batch requests ~200, and user connects ~6.</span></span>

<span data-ttu-id="72fb3-293">Если вы используете географически распределенное развертывание, где сервер управления & серверы публикации используют сеть медленного канала связи между ними, время кругового приема на серверах публикации выходит за допустимые пределы ( &lt; 5 секунд), даже для 100 одновременных запросов на одном сервере управления.</span><span class="sxs-lookup"><span data-stu-id="72fb3-293">Using a geographically distributed deployment, where the management server & publishing servers utilize a slow link network between them, the round trip response time on the publishing servers is within acceptable time limits (&lt;5 seconds), even for 100 simultaneous requests on a single management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72fb3-294">Сценарий</span><span class="sxs-lookup"><span data-stu-id="72fb3-294">Scenario</span></span></th>
<th align="left"><span data-ttu-id="72fb3-295">Вариант</span><span class="sxs-lookup"><span data-stu-id="72fb3-295">Variation</span></span></th>
<th align="left"><span data-ttu-id="72fb3-296">Количество групп соединения</span><span class="sxs-lookup"><span data-stu-id="72fb3-296">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="72fb3-297">Количество групп доступа</span><span class="sxs-lookup"><span data-stu-id="72fb3-297">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="72fb3-298">Количество серверов публикаций</span><span class="sxs-lookup"><span data-stu-id="72fb3-298">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="72fb3-299">Сервер или сервер управления публикации типа сетевого подключения</span><span class="sxs-lookup"><span data-stu-id="72fb3-299">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="72fb3-300">Время ответа цикла обработки на сервере публикаций (в секундах)</span><span class="sxs-lookup"><span data-stu-id="72fb3-300">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="72fb3-301">Использование ЦП на сервере управления</span><span class="sxs-lookup"><span data-stu-id="72fb3-301">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-302">Сетевое соединение между сервером публикации и сервером управления</span><span class="sxs-lookup"><span data-stu-id="72fb3-302">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="72fb3-303">Сеть 1,5 Мбит/с медленной связью</span><span class="sxs-lookup"><span data-stu-id="72fb3-303">1.5 Mbps Slow link Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-304">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-304">0</span></span></p></li>
<li><p><span data-ttu-id="72fb3-305">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-305">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-306">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-306">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-307">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-307">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-308">50</span><span class="sxs-lookup"><span data-stu-id="72fb3-308">50</span></span></p></li>
<li><p><span data-ttu-id="72fb3-309">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-309">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-310">1,5 Мбит/с, кабель DSL</span><span class="sxs-lookup"><span data-stu-id="72fb3-310">1.5Mbps Cable DSL</span></span></p></li>
<li><p><span data-ttu-id="72fb3-311">1,5 Мбит/с, кабель DSL</span><span class="sxs-lookup"><span data-stu-id="72fb3-311">1.5Mbps Cable DSL</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-312">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="72fb3-312">4</span></span></p></li>
<li><p><span data-ttu-id="72fb3-313">5</span><span class="sxs-lookup"><span data-stu-id="72fb3-313">5</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-314">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-314">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-315">2</span><span class="sxs-lookup"><span data-stu-id="72fb3-315">2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72fb3-316">Сетевое соединение между сервером публикации и сервером управления</span><span class="sxs-lookup"><span data-stu-id="72fb3-316">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="72fb3-317">Сеть ЛС/WIFI</span><span class="sxs-lookup"><span data-stu-id="72fb3-317">LAN / WIFI Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-318">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-318">0</span></span></p></li>
<li><p><span data-ttu-id="72fb3-319">до</span><span class="sxs-lookup"><span data-stu-id="72fb3-319">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-320">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-320">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-321">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-321">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-322">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-322">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-323">200</span><span class="sxs-lookup"><span data-stu-id="72fb3-323">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-324">Wifi</span><span class="sxs-lookup"><span data-stu-id="72fb3-324">Wifi</span></span></p></li>
<li><p><span data-ttu-id="72fb3-325">Wifi</span><span class="sxs-lookup"><span data-stu-id="72fb3-325">Wifi</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-326">11</span><span class="sxs-lookup"><span data-stu-id="72fb3-326">11</span></span></p></li>
<li><p><span data-ttu-id="72fb3-327">средняя</span><span class="sxs-lookup"><span data-stu-id="72fb3-327">20</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-328">10-15</span><span class="sxs-lookup"><span data-stu-id="72fb3-328">15</span></span></p></li>
<li><p><span data-ttu-id="72fb3-329">18</span><span class="sxs-lookup"><span data-stu-id="72fb3-329">17</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="72fb3-330">Подключены ли сервер управления и серверы публикаций по медленному каналу связи или высокоскоростной сети, сервер управления может обрабатывать около 15 000 запросов на обновление пакетов в течение 30 минут.</span><span class="sxs-lookup"><span data-stu-id="72fb3-330">Whether the management server and publishing servers are connected over a slow link network, or a high speed network, the management server can handle approximately 15,000 package refresh requests in 30 minutes.</span></span>

## <a href="" id="---------app-v-5-0-reporting-server-capacity-planning-recommendations"></a> <span data-ttu-id="72fb3-331">Рекомендации по планированию мощности сервера для App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="72fb3-331">App-V 5.0 Reporting Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="72fb3-332">Клиенты App-V 5,0 отправляют данные отчета на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="72fb3-332">App-V 5.0 clients send reporting data to the reporting server.</span></span> <span data-ttu-id="72fb3-333">Затем сервер отчетов записывает данные в базу данных Microsoft SQL Server и возвращает успешное уведомление на компьютер, на котором запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="72fb3-333">The reporting server then records the information in the Microsoft SQL Server database and returns a successful notification back to the computer running App-V 5.0 client.</span></span> <span data-ttu-id="72fb3-334">Дополнительные сведения о конфигурациях поддерживаемые сервером отчетов App-V 5,0 можно найти в статьях [Поддерживаемые конфигурации App-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="72fb3-334">For more information about App-V 5.0 Reporting Server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="72fb3-335">**Примечание**  Время ответа цикла обработки — это время, затраченное на компьютере, на котором запущен клиент App-V 5,0 для отправки данных отчетов на сервер отчетов и получения уведомления об успешном уведомлении от сервера отчетов.</span><span class="sxs-lookup"><span data-stu-id="72fb3-335">**Note** Round trip response time is the time taken by the computer running the App-V 5.0 client to send the reporting information to the reporting server and receive a successful notification from the reporting server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72fb3-336">Сценарий</span><span class="sxs-lookup"><span data-stu-id="72fb3-336">Scenario</span></span></th>
<th align="left"><span data-ttu-id="72fb3-337">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="72fb3-337">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-338">Несколько клиентов App-V 5,0 отправляют данные отчетов на сервер отчетов одновременно.</span><span class="sxs-lookup"><span data-stu-id="72fb3-338">Multiple App-V 5.0 clients send reporting information to the reporting server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-339">Время ответа от сервера отчетов составляет 2,6 секунд для клиентов 500.</span><span class="sxs-lookup"><span data-stu-id="72fb3-339">Round trip response time from the reporting server is 2.6 seconds for 500 clients.</span></span></p></li>
<li><p><span data-ttu-id="72fb3-340">Время ответа от сервера отчетов составляет 5,65 секунд для клиентов 1000.</span><span class="sxs-lookup"><span data-stu-id="72fb3-340">Round trip response time from the reporting server is 5.65 seconds for 1000 clients.</span></span></p></li>
<li><p><span data-ttu-id="72fb3-341">Время реагирования на круговую передачу в зависимости от количества клиентов возрастает в линейном режиме.</span><span class="sxs-lookup"><span data-stu-id="72fb3-341">Round trip response time increases linearly depending on number of clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72fb3-342">Количество запросов в секунду, обработанных сервером отчетов.</span><span class="sxs-lookup"><span data-stu-id="72fb3-342">Requests per second processed by the reporting server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-343">Один сервер отчетов и единая база данных могут обрабатывать не более 139 запросов в секунду.</span><span class="sxs-lookup"><span data-stu-id="72fb3-343">A single reporting server and a single database, can process a maximum of 139 requests per second.</span></span> <span data-ttu-id="72fb3-344">Среднее значение составляет 121 запросов в секунду.</span><span class="sxs-lookup"><span data-stu-id="72fb3-344">The average is 121 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="72fb3-345">Используя два сервера отчетов для одной базы данных Microsoft SQL Server, средние запросы на секунду похожи на один сервер отчетов = ~ 127, с максимальным количеством запросов 278 в секунду.</span><span class="sxs-lookup"><span data-stu-id="72fb3-345">Using two reporting servers reporting to the same Microsoft SQL Server database, the average requests/second is similar to a single reporting server = ~127, with a max of 278 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="72fb3-346">Один сервер отчетов может обрабатывать одновременные и активные соединения 500.</span><span class="sxs-lookup"><span data-stu-id="72fb3-346">A single reporting server can process 500 concurrent/active connections.</span></span></p></li>
<li><p><span data-ttu-id="72fb3-347">Один сервер отчетов может обрабатывать максимум 1500 одновременных подключений.</span><span class="sxs-lookup"><span data-stu-id="72fb3-347">A single reporting server can process a maximum 1500 concurrent connections.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-348">База данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="72fb3-348">Reporting Database.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-349">Конфликт блокировки на компьютере с Microsoft SQL Server — это ограничивающий коэффициент запросов в секунду.</span><span class="sxs-lookup"><span data-stu-id="72fb3-349">Lock contention on the computer running Microsoft SQL Server is the limiting factor for requests/second.</span></span></p></li>
<li><p><span data-ttu-id="72fb3-350">Пропускная способность и время отклика не зависят от размера базы данных.</span><span class="sxs-lookup"><span data-stu-id="72fb3-350">Throughput and response time are independent of database size.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="72fb3-351">**Расчет случайной задержки**:</span><span class="sxs-lookup"><span data-stu-id="72fb3-351">**Calculating random delay**:</span></span>

<span data-ttu-id="72fb3-352">Случайная задержка определяет максимальную задержку (в минутах) для данных, отправляемых на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="72fb3-352">The random delay specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="72fb3-353">При запуске запланированной задачи клиент создает произвольную задержку от **0** до **ReportingRandomDelay** и ждет указанное время перед отправкой данных.</span><span class="sxs-lookup"><span data-stu-id="72fb3-353">When the scheduled task is started, the client generates a random delay between **0** and **ReportingRandomDelay** and will wait the specified duration before sending data.</span></span>

<span data-ttu-id="72fb3-354">Произвольная задержка = 4 \ \* количество клиентов/среднее число запросов в секунду.</span><span class="sxs-lookup"><span data-stu-id="72fb3-354">Random delay = 4 \* number of clients / average requests per second.</span></span>

<span data-ttu-id="72fb3-355">Пример: для клиентов 500 с количеством запросов 120 в секунду случайная задержка — 4 \ \* 500/120 = ~ 17 минут.</span><span class="sxs-lookup"><span data-stu-id="72fb3-355">Example: For 500 clients, with 120 requests per second, the Random delay is, 4 \* 500 / 120 = ~17 minutes.</span></span>

## <a href="" id="---------app-v-5-0-publishing-server-capacity-planning-recommendations"></a> <span data-ttu-id="72fb3-356">Рекомендации по планированию производительности сервера App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="72fb3-356">App-V 5.0 Publishing Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="72fb3-357">Компьютеры, на которых работает клиент App-V 5,0, подключаются к серверу публикации App-v 5,0 для отправки запроса на обновление публикации и получения ответа.</span><span class="sxs-lookup"><span data-stu-id="72fb3-357">Computers running the App-V 5.0 client connect to the App-V 5.0 publishing server to send a publishing refresh request and to receive a response.</span></span> <span data-ttu-id="72fb3-358">Время отклика на круговую передачу измеряется на компьютере, на котором запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="72fb3-358">Round trip response time is measured on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="72fb3-359">Время процессора измеряется на сервере публикаций.</span><span class="sxs-lookup"><span data-stu-id="72fb3-359">Processor time is measured on the publishing server.</span></span> <span data-ttu-id="72fb3-360">Дополнительные сведения о конфигурациях, поддерживаемых сервером публикаций App-V 5,0, приведены в разделе [Поддерживаемые конфигурации App-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="72fb3-360">For more information about App-V 5.0 Publishing Server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="72fb3-361">**Важно!**  В списке ниже приведены основные факторы, которые необходимо учитывать при настройке сервера публикаций App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="72fb3-361">**Important** The following list displays the main factors to consider when setting up the App-V 5.0 publishing server:</span></span>

-   <span data-ttu-id="72fb3-362">Количество клиентов, которые одновременно подключаются к одному серверу публикаций.</span><span class="sxs-lookup"><span data-stu-id="72fb3-362">The number of clients connecting simultaneously to a single publishing server.</span></span>

-   <span data-ttu-id="72fb3-363">Количество пакетов в каждом обновлении.</span><span class="sxs-lookup"><span data-stu-id="72fb3-363">The number of packages in each refresh.</span></span>

-   <span data-ttu-id="72fb3-364">Доступная пропускная способность сети между клиентом и сервером публикаций App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="72fb3-364">The available network bandwidth in your environment between the client and the App-V 5.0 publishing server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72fb3-365">Сценарий</span><span class="sxs-lookup"><span data-stu-id="72fb3-365">Scenario</span></span></th>
<th align="left"><span data-ttu-id="72fb3-366">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="72fb3-366">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-367">Несколько клиентов App-V 5,0 подключаются к одному серверу публикаций одновременно.</span><span class="sxs-lookup"><span data-stu-id="72fb3-367">Multiple App-V 5.0 clients connect to a single publishing server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-368">Сервер публикаций, использующий два ядра процессора, может отвечать не более чем на 5000 клиентов, которые запрашивают обновление одновременно.</span><span class="sxs-lookup"><span data-stu-id="72fb3-368">A publishing server running dual core processors can respond to at most 5000 clients requesting a refresh simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="72fb3-369">Для клиентов 5000-10000 для сервера публикаций требуется не менее четырех ядер.</span><span class="sxs-lookup"><span data-stu-id="72fb3-369">For 5000-10000 clients, the publishing server requires a minimum quad core.</span></span></p></li>
<li><p><span data-ttu-id="72fb3-370">Для клиентов 10000-20000 сервер публикаций должен иметь два четырехъядерных ядра для более эффективного отклика.</span><span class="sxs-lookup"><span data-stu-id="72fb3-370">For 10000-20000 clients, the publishing server should have dual quad cores for more efficient response times.</span></span></p></li>
<li><p><span data-ttu-id="72fb3-371">Сервер публикаций с четырехъядерным процессором может обновлять до 10000 пакетов в течение 3 секунд.</span><span class="sxs-lookup"><span data-stu-id="72fb3-371">A publishing server with a quad core can refresh up to 10000 packages within 3 seconds.</span></span> <span data-ttu-id="72fb3-372">(Поддержка одновременных клиентов 10000)</span><span class="sxs-lookup"><span data-stu-id="72fb3-372">(Supporting 10000 simultaneous clients)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72fb3-373">Количество пакетов в каждом обновлении.</span><span class="sxs-lookup"><span data-stu-id="72fb3-373">Number of packages in each refresh.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-374">Увеличение количества пакетов увеличит время отклика на ~ 40% (до 1000 пакетов).</span><span class="sxs-lookup"><span data-stu-id="72fb3-374">Increasing number of packages will increase response time by ~40% (up to 1000 packages).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-375">Сеть между клиентом App-V 5,0 и сервером публикации.</span><span class="sxs-lookup"><span data-stu-id="72fb3-375">Network between the App-V 5.0 client and the publishing server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-376">В течение медленной сети (1,5 Мбит/с) время ответа увеличивается на 97% (до 1000 пользователей).</span><span class="sxs-lookup"><span data-stu-id="72fb3-376">Across a slow network (1.5 Mbps bandwidth), there is a 97% increase in response time compared to LAN (up to 1000 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="72fb3-377">**Примечание**  Использование ЦП сервера публикаций всегда велико в течение интервала времени, когда он должен обрабатывать одновременные запросы ( &gt; 90% в большинстве случаев).</span><span class="sxs-lookup"><span data-stu-id="72fb3-377">**Note** The publishing server CPU usage is always high during the time interval when it has to process simultaneous requests (&gt;90% in most cases).</span></span> <span data-ttu-id="72fb3-378">Сервер публикаций может обрабатывать запросы ~ 1500 клиента через 1 секунду.</span><span class="sxs-lookup"><span data-stu-id="72fb3-378">The publishing server can handle ~1500 client requests in 1 second.</span></span>

 

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72fb3-379">Сценарий</span><span class="sxs-lookup"><span data-stu-id="72fb3-379">Scenario</span></span></th>
<th align="left"><span data-ttu-id="72fb3-380">Вариант</span><span class="sxs-lookup"><span data-stu-id="72fb3-380">Variation</span></span></th>
<th align="left"><span data-ttu-id="72fb3-381">Число клиентов App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="72fb3-381">Number of App-V 5.0 clients</span></span></th>
<th align="left"><span data-ttu-id="72fb3-382">Количество пакетов</span><span class="sxs-lookup"><span data-stu-id="72fb3-382">Number of packages</span></span></th>
<th align="left"><span data-ttu-id="72fb3-383">Конфигурация процессора на сервере публикаций</span><span class="sxs-lookup"><span data-stu-id="72fb3-383">Processor configuration on the publishing server</span></span></th>
<th align="left"><span data-ttu-id="72fb3-384">Сервер публикации или приложение App-5,0 V типа "Сетевое подключение"</span><span class="sxs-lookup"><span data-stu-id="72fb3-384">Network connection type publishing server / App-V 5.0 client</span></span></th>
<th align="left"><span data-ttu-id="72fb3-385">Время кругового обращения в клиенте App-V 5,0 (в секундах)</span><span class="sxs-lookup"><span data-stu-id="72fb3-385">Round trip time on the App-V 5.0 client (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="72fb3-386">Загрузка ЦП на сервере публикаций (в%)</span><span class="sxs-lookup"><span data-stu-id="72fb3-386">CPU utilization on publishing server (in %)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-387">Клиент App-V 5,0 отправляет запрос на обновление публикации &amp; , каждый запрос содержит пакеты 120.</span><span class="sxs-lookup"><span data-stu-id="72fb3-387">App-V 5.0 client sends publishing refresh request &amp; receives response, each request containing 120 packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="72fb3-388">Количество клиентов</span><span class="sxs-lookup"><span data-stu-id="72fb3-388">Number of clients</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-389">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-389">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-390">1000</span><span class="sxs-lookup"><span data-stu-id="72fb3-390">1000</span></span></p></li>
<li><p><span data-ttu-id="72fb3-391">5000</span><span class="sxs-lookup"><span data-stu-id="72fb3-391">5000</span></span></p></li>
<li><p><span data-ttu-id="72fb3-392">10000</span><span class="sxs-lookup"><span data-stu-id="72fb3-392">10000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-393">120</span><span class="sxs-lookup"><span data-stu-id="72fb3-393">120</span></span></p></li>
<li><p><span data-ttu-id="72fb3-394">120</span><span class="sxs-lookup"><span data-stu-id="72fb3-394">120</span></span></p></li>
<li><p><span data-ttu-id="72fb3-395">120</span><span class="sxs-lookup"><span data-stu-id="72fb3-395">120</span></span></p></li>
<li><p><span data-ttu-id="72fb3-396">120</span><span class="sxs-lookup"><span data-stu-id="72fb3-396">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-397">Двухъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="72fb3-397">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="72fb3-398">Двухъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="72fb3-398">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="72fb3-399">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="72fb3-399">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="72fb3-400">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="72fb3-400">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-401">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-401">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-402">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-402">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-403">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-403">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-404">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-404">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-405">1,1</span><span class="sxs-lookup"><span data-stu-id="72fb3-405">1</span></span></p></li>
<li><p><span data-ttu-id="72fb3-406">2</span><span class="sxs-lookup"><span data-stu-id="72fb3-406">2</span></span></p></li>
<li><p><span data-ttu-id="72fb3-407">2</span><span class="sxs-lookup"><span data-stu-id="72fb3-407">2</span></span></p></li>
<li><p><span data-ttu-id="72fb3-408">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="72fb3-408">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-409">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-409">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-410">99</span><span class="sxs-lookup"><span data-stu-id="72fb3-410">99</span></span></p></li>
<li><p><span data-ttu-id="72fb3-411">89</span><span class="sxs-lookup"><span data-stu-id="72fb3-411">89</span></span></p></li>
<li><p><span data-ttu-id="72fb3-412">77</span><span class="sxs-lookup"><span data-stu-id="72fb3-412">77</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72fb3-413">Несколько пакетов в каждом обновлении</span><span class="sxs-lookup"><span data-stu-id="72fb3-413">Multiple packages in each refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="72fb3-414">Количество пакетов</span><span class="sxs-lookup"><span data-stu-id="72fb3-414">Number of packages</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-415">1000</span><span class="sxs-lookup"><span data-stu-id="72fb3-415">1000</span></span></p></li>
<li><p><span data-ttu-id="72fb3-416">1000</span><span class="sxs-lookup"><span data-stu-id="72fb3-416">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-417">500</span><span class="sxs-lookup"><span data-stu-id="72fb3-417">500</span></span></p></li>
<li><p><span data-ttu-id="72fb3-418">1000</span><span class="sxs-lookup"><span data-stu-id="72fb3-418">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-419">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="72fb3-419">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="72fb3-420">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="72fb3-420">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-421">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-421">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-422">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-422">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-423">2</span><span class="sxs-lookup"><span data-stu-id="72fb3-423">2</span></span></p></li>
<li><p><span data-ttu-id="72fb3-424">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="72fb3-424">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-425">92</span><span class="sxs-lookup"><span data-stu-id="72fb3-425">92</span></span></p></li>
<li><p><span data-ttu-id="72fb3-426">91</span><span class="sxs-lookup"><span data-stu-id="72fb3-426">91</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-427">Сеть между клиентом и сервером публикаций</span><span class="sxs-lookup"><span data-stu-id="72fb3-427">Network between client and publishing server</span></span></p></td>
<td align="left"><p><span data-ttu-id="72fb3-428">сеть 1,5 Мбит/с медленной связью</span><span class="sxs-lookup"><span data-stu-id="72fb3-428">1.5 Mbps Slow link network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-429">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-429">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-430">500</span><span class="sxs-lookup"><span data-stu-id="72fb3-430">500</span></span></p></li>
<li><p><span data-ttu-id="72fb3-431">1000</span><span class="sxs-lookup"><span data-stu-id="72fb3-431">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-432">120</span><span class="sxs-lookup"><span data-stu-id="72fb3-432">120</span></span></p></li>
<li><p><span data-ttu-id="72fb3-433">120</span><span class="sxs-lookup"><span data-stu-id="72fb3-433">120</span></span></p></li>
<li><p><span data-ttu-id="72fb3-434">120</span><span class="sxs-lookup"><span data-stu-id="72fb3-434">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-435">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="72fb3-435">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="72fb3-436">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="72fb3-436">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="72fb3-437">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="72fb3-437">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-438">1,5 Мбит/с в пределах континентальные сети</span><span class="sxs-lookup"><span data-stu-id="72fb3-438">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-439">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="72fb3-439">3</span></span></p></li>
<li><p><span data-ttu-id="72fb3-440">10 (с количеством сбоев 0,2%)</span><span class="sxs-lookup"><span data-stu-id="72fb3-440">10 (with 0.2% failure rate)</span></span></p></li>
<li><p><span data-ttu-id="72fb3-441">17 (с количеством сбоев 1%)</span><span class="sxs-lookup"><span data-stu-id="72fb3-441">17 (with 1% failure rate)</span></span></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-0-streaming-capacity-planning-recommendations"></a> <span data-ttu-id="72fb3-442">Рекомендации по планированию мощности потоков App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="72fb3-442">App-V 5.0 Streaming Capacity Planning Recommendations</span></span>


<span data-ttu-id="72fb3-443">Компьютеры, на которых выполняется поток клиента App-V 5,0, виртуальный пакет приложения от сервера потоков.</span><span class="sxs-lookup"><span data-stu-id="72fb3-443">Computers running the App-V 5.0 client stream the virtual application package from the streaming server.</span></span> <span data-ttu-id="72fb3-444">Время отклика на круговую передачу измеряется на компьютере, на котором запущен клиент App-V 5,0, а также время, затраченное на потоковую передачу всего пакета.</span><span class="sxs-lookup"><span data-stu-id="72fb3-444">Round trip response time is measured on the computer running the App-V 5.0 client, and is the time taken to stream the entire package.</span></span>

<span data-ttu-id="72fb3-445">**Важно!**  В следующем списке приведены основные факторы, которые необходимо учитывать при настройке потокового сервера App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="72fb3-445">**Important** The following list identifies the main factors to consider when setting up the App-V 5.0 streaming server:</span></span>

-   <span data-ttu-id="72fb3-446">Количество клиентов, одновременно выполняющих потоковую передачу пакетов приложения с одного сервера потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="72fb3-446">The number of clients streaming application packages simultaneously from a single streaming server.</span></span>

-   <span data-ttu-id="72fb3-447">Размер пакета, который передается в потоке.</span><span class="sxs-lookup"><span data-stu-id="72fb3-447">The size of the package being streamed.</span></span>

-   <span data-ttu-id="72fb3-448">Доступная пропускная способность сети между клиентом и сервером потоковой передачи данных.</span><span class="sxs-lookup"><span data-stu-id="72fb3-448">The available network bandwidth in your environment between the client and the streaming server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72fb3-449">Сценарий</span><span class="sxs-lookup"><span data-stu-id="72fb3-449">Scenario</span></span></th>
<th align="left"><span data-ttu-id="72fb3-450">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="72fb3-450">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-451">Несколько клиентов App-V 5,0 одновременные потоковые приложения на одном поток-сервере.</span><span class="sxs-lookup"><span data-stu-id="72fb3-451">Multiple App-V 5.0 clients stream applications from a single streaming server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-452">Если количество клиентов, одновременно выполняющих потоковую передачу на одном и том же сервере, будет увеличиваться, существует линейная связь с пакетом для загрузки/потокового времени.</span><span class="sxs-lookup"><span data-stu-id="72fb3-452">If the number of clients simultaneously streaming from the same server increases, there is a linear relationship with the package download/streaming time.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72fb3-453">Размер пакета, который передается в потоке.</span><span class="sxs-lookup"><span data-stu-id="72fb3-453">Size of the package being streamed.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-454">Размер пакета имеет значительное влияние на потоковую передачу и время загрузки только для больших пакетов размером ~ 1 ГБ.</span><span class="sxs-lookup"><span data-stu-id="72fb3-454">The package size has a significant impact on the streaming/download time only for larger packages with a size ~ 1GB.</span></span> <span data-ttu-id="72fb3-455">Для размеров пакета от 3 до 100 МБ количество потоков в диапазоне от 20 до 100 секунд с 100 одновременных клиентов.</span><span class="sxs-lookup"><span data-stu-id="72fb3-455">For package sizes ranging from 3 MB to 100 MB, the streaming time ranges from 20 seconds to 100 seconds, with 100 simultaneous clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-456">Сеть между клиентом App-V 5,0 и потоковым сервером.</span><span class="sxs-lookup"><span data-stu-id="72fb3-456">Network between the App-V 5.0 client and the streaming server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-457">В течение медленной сети (1,5 Мбит/с) время ответа увеличивается на 70-80% (до 100 пользователей).</span><span class="sxs-lookup"><span data-stu-id="72fb3-457">Across a slow network (1.5 Mbps bandwidth), there is a 70-80% increase in response time compared to LAN (up to 100 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="72fb3-458">В следующей таблице показаны примеры значений для каждого из факторов, описанных в предыдущем списке.</span><span class="sxs-lookup"><span data-stu-id="72fb3-458">The following table displays sample values for each of the factors in the previous list:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72fb3-459">Сценарий</span><span class="sxs-lookup"><span data-stu-id="72fb3-459">Scenario</span></span></th>
<th align="left"><span data-ttu-id="72fb3-460">Вариант</span><span class="sxs-lookup"><span data-stu-id="72fb3-460">Variation</span></span></th>
<th align="left"><span data-ttu-id="72fb3-461">Число клиентов App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="72fb3-461">Number of App-V 5.0 clients</span></span></th>
<th align="left"><span data-ttu-id="72fb3-462">Размер каждого пакета</span><span class="sxs-lookup"><span data-stu-id="72fb3-462">Size of each package</span></span></th>
<th align="left"><span data-ttu-id="72fb3-463">Сервер потоков данных сетевого подключения (App-V), клиент 5,0</span><span class="sxs-lookup"><span data-stu-id="72fb3-463">Network connection type streaming server / App-V 5.0 client</span></span></th>
<th align="left"><span data-ttu-id="72fb3-464">Время кругового обращения в клиенте App-V 5,0 (в секундах)</span><span class="sxs-lookup"><span data-stu-id="72fb3-464">Round trip time on the App-V 5.0 client (in seconds)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-465">Несколько клиентов App-V 5,0 попотоковые пакеты виртуальных приложений с потокового сервера.</span><span class="sxs-lookup"><span data-stu-id="72fb3-465">Multiple App-V 5.0 clients streaming virtual application packages from a streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="72fb3-466">Количество клиентов.</span><span class="sxs-lookup"><span data-stu-id="72fb3-466">Number of clients.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-467">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-467">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-468">200</span><span class="sxs-lookup"><span data-stu-id="72fb3-468">200</span></span></p></li>
<li><p><span data-ttu-id="72fb3-469">1000</span><span class="sxs-lookup"><span data-stu-id="72fb3-469">1000</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="72fb3-470">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-470">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-471">200</span><span class="sxs-lookup"><span data-stu-id="72fb3-471">200</span></span></p></li>
<li><p><span data-ttu-id="72fb3-472">1000</span><span class="sxs-lookup"><span data-stu-id="72fb3-472">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-473">3,5 MБ</span><span class="sxs-lookup"><span data-stu-id="72fb3-473">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="72fb3-474">3,5 MБ</span><span class="sxs-lookup"><span data-stu-id="72fb3-474">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="72fb3-475">3,5 MБ</span><span class="sxs-lookup"><span data-stu-id="72fb3-475">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="72fb3-476">5 МБ</span><span class="sxs-lookup"><span data-stu-id="72fb3-476">5 MB</span></span></p></li>
<li><p><span data-ttu-id="72fb3-477">5 МБ</span><span class="sxs-lookup"><span data-stu-id="72fb3-477">5 MB</span></span></p></li>
<li><p><span data-ttu-id="72fb3-478">5 МБ</span><span class="sxs-lookup"><span data-stu-id="72fb3-478">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-479">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-479">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-480">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-480">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-481">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-481">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="72fb3-482">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-482">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-483">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-483">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-484">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-484">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-485">составляет</span><span class="sxs-lookup"><span data-stu-id="72fb3-485">29</span></span></p></li>
<li><p><span data-ttu-id="72fb3-486">39</span><span class="sxs-lookup"><span data-stu-id="72fb3-486">39</span></span></p></li>
<li><p><span data-ttu-id="72fb3-487">391</span><span class="sxs-lookup"><span data-stu-id="72fb3-487">391</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="72fb3-488">35</span><span class="sxs-lookup"><span data-stu-id="72fb3-488">35</span></span></p></li>
<li><p><span data-ttu-id="72fb3-489">68</span><span class="sxs-lookup"><span data-stu-id="72fb3-489">68</span></span></p></li>
<li><p><span data-ttu-id="72fb3-490">461</span><span class="sxs-lookup"><span data-stu-id="72fb3-490">461</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72fb3-491">Размер каждого пакета, который передается в потоке.</span><span class="sxs-lookup"><span data-stu-id="72fb3-491">Size of each package being streamed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="72fb3-492">Размер каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="72fb3-492">Size of each package.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-493">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-493">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-494">200</span><span class="sxs-lookup"><span data-stu-id="72fb3-494">200</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="72fb3-495">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-495">100</span></span></p></li>
<li><p><span data-ttu-id="72fb3-496">200</span><span class="sxs-lookup"><span data-stu-id="72fb3-496">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-497">21 МБАЙТ</span><span class="sxs-lookup"><span data-stu-id="72fb3-497">21 MB</span></span></p></li>
<li><p><span data-ttu-id="72fb3-498">21 МБАЙТ</span><span class="sxs-lookup"><span data-stu-id="72fb3-498">21 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="72fb3-499">109</span><span class="sxs-lookup"><span data-stu-id="72fb3-499">109</span></span></p></li>
<li><p><span data-ttu-id="72fb3-500">109</span><span class="sxs-lookup"><span data-stu-id="72fb3-500">109</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-501">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-501">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-502">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-502">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="72fb3-503">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-503">LAN</span></span></p></li>
<li><p><span data-ttu-id="72fb3-504">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="72fb3-504">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="72fb3-505">33</span><span class="sxs-lookup"><span data-stu-id="72fb3-505">33</span></span></p>
<p><span data-ttu-id="72fb3-506">83</span><span class="sxs-lookup"><span data-stu-id="72fb3-506">83</span></span></p>
<p></p>
<p><span data-ttu-id="72fb3-507">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-507">100</span></span></p>
<p><span data-ttu-id="72fb3-508">160</span><span class="sxs-lookup"><span data-stu-id="72fb3-508">160</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72fb3-509">Сетевое соединение между клиентом и приложением-V 5,0 Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="72fb3-509">Network connection between client and App-V 5.0 streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="72fb3-510">1,5 Мбит/с медленной связью сети.</span><span class="sxs-lookup"><span data-stu-id="72fb3-510">1.5 Mbps Slow link network.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-511">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-511">100</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="72fb3-512">100</span><span class="sxs-lookup"><span data-stu-id="72fb3-512">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-513">3,5 MБ</span><span class="sxs-lookup"><span data-stu-id="72fb3-513">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="72fb3-514">5 МБ</span><span class="sxs-lookup"><span data-stu-id="72fb3-514">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="72fb3-515">1,5 Мбит/с в пределах континентальные сети</span><span class="sxs-lookup"><span data-stu-id="72fb3-515">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="72fb3-516">102</span><span class="sxs-lookup"><span data-stu-id="72fb3-516">102</span></span></p>
<p></p>
<p><span data-ttu-id="72fb3-517">121</span><span class="sxs-lookup"><span data-stu-id="72fb3-517">121</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="72fb3-518">Каждый потоковый сервер App-V 5,0 должен обрабатывать 200 минимум одновременных потоков приложений, поддерживающих виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="72fb3-518">Each App-V 5.0 streaming server should be able to handle a minimum of 200 clients concurrently streaming virtualized applications.</span></span>

<span data-ttu-id="72fb3-519">**Примечание**  Фактическое время на этот поток будет определяться в первую очередь количеством потоков на клиентах, число пакетов, размер пакета, сетевая активность сервера и условия сети.</span><span class="sxs-lookup"><span data-stu-id="72fb3-519">**Note** The actual time to it will take to stream is determined primarily by the number of clients streaming simultaneously, number of packages, package size, the server’s network activity, and network conditions.</span></span>

 

<span data-ttu-id="72fb3-520">Например, пользователь может перечислить пакет 100 МБ менее чем на 2 минуты, когда 100 одновременных клиентов переносят потоковую передачу на сервер.</span><span class="sxs-lookup"><span data-stu-id="72fb3-520">For example, an average user can stream a 100 MB package in less than 2 minutes, when 100 simultaneous clients are streaming from the server.</span></span> <span data-ttu-id="72fb3-521">Однако пакет размером 1 ГБ может занять до 30 минут.</span><span class="sxs-lookup"><span data-stu-id="72fb3-521">However, a package of size 1 GB could take up to 30 minutes.</span></span> <span data-ttu-id="72fb3-522">В большинстве реальных сред потребность в потоковых данных не распределена равномерно, вам необходимо понять приблизительные пиковые требования к потоковой передаче в среде для правильного изменения числа требуемых потоков серверов.</span><span class="sxs-lookup"><span data-stu-id="72fb3-522">In most real world environments streaming demand is not uniformly distributed, you will need to understand the approximate peak streaming requirements present in your environment in order to properly size the number of required streaming servers.</span></span>

<span data-ttu-id="72fb3-523">Количество клиентов, которые может поддерживать потоковый сервер, может быть значительно увеличено, а пиковые требования к потоковой передаче уменьшились при предварительном кэшировании приложений.</span><span class="sxs-lookup"><span data-stu-id="72fb3-523">The number of clients a streaming server can support can be significantly increased and the peak streaming requirements reduced if you pre-cache your applications.</span></span> <span data-ttu-id="72fb3-524">Вы также можете увеличивать количество клиентов, которые может поддерживать потоковый сервер, с помощью доставки потоковой передачи по требованию и оптимизированных потоков.</span><span class="sxs-lookup"><span data-stu-id="72fb3-524">You can also increase the number of clients a streaming server can support by using on-demand streaming delivery and stream optimized packages.</span></span>

## <span data-ttu-id="72fb3-525">Объединение ролей сервера App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="72fb3-525">Combining App-V 5.0 Server Roles</span></span>


<span data-ttu-id="72fb3-526">Скидка на масштабирование и отказоустойчивость, минимальное количество серверов, необходимое для расположения с подключением к службе каталогов Active Directory, — это один из них.</span><span class="sxs-lookup"><span data-stu-id="72fb3-526">Discounting scaling and fault-tolerance requirements, the minimum number of servers needed for a location with connectivity to Active Directory is one.</span></span> <span data-ttu-id="72fb3-527">На этом сервере будут размещены сервер управления, служба сервера управления и роли Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="72fb3-527">This server will host the management server, management server service, and Microsoft SQL Server roles.</span></span> <span data-ttu-id="72fb3-528">Таким образом, роли сервера можно упорядочить по любой нужной комбинации, так как они не конфликтуют друг с другом.</span><span class="sxs-lookup"><span data-stu-id="72fb3-528">Server roles, therefore, can be arranged in any desired combination since they do not conflict with one another.</span></span>

<span data-ttu-id="72fb3-529">Игнорируя требования масштабирования, минимальное количество серверов, необходимых для обеспечения отказоустойчивой реализации, — четыре.</span><span class="sxs-lookup"><span data-stu-id="72fb3-529">Ignoring scaling requirements, the minimum number of servers necessary to provide a fault-tolerant implementation is four.</span></span> <span data-ttu-id="72fb3-530">Сервер управления и поддержка ролей Microsoft SQL Server размещаются в отказоустойчивых конфигурациях.</span><span class="sxs-lookup"><span data-stu-id="72fb3-530">The management server, and Microsoft SQL Server roles support being placed in fault-tolerant configurations.</span></span> <span data-ttu-id="72fb3-531">Службу сервера управления можно объединить с любой из ролей, но при этом останется единственная точка сбоя.</span><span class="sxs-lookup"><span data-stu-id="72fb3-531">The management server service can be combined with any of the roles, but remains a single point of failure.</span></span>

<span data-ttu-id="72fb3-532">Несмотря на то, что существует ряд стратегий и технологий отказоустойчивости, не все применимы к данной службе.</span><span class="sxs-lookup"><span data-stu-id="72fb3-532">Although there are a number of fault-tolerance strategies and technologies available, not all are applicable to a given service.</span></span> <span data-ttu-id="72fb3-533">Кроме того, если роли App-V 5,0 объединены, некоторые параметры отказоустойчивости могут больше не применяться из-за несовместимости.</span><span class="sxs-lookup"><span data-stu-id="72fb3-533">Additionally, if App-V 5.0 roles are combined, certain fault-tolerance options may no longer apply due to incompatibilities.</span></span>






## <span data-ttu-id="72fb3-534">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="72fb3-534">Related topics</span></span>


[<span data-ttu-id="72fb3-535">Поддерживаемые конфигурации в App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="72fb3-535">App-V 5.0 Supported Configurations</span></span>](app-v-50-supported-configurations.md)

[<span data-ttu-id="72fb3-536">Планирование для обеспечения высокой доступности при использовании App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="72fb3-536">Planning for High Availability with App-V 5.0</span></span>](planning-for-high-availability-with-app-v-50.md)

[<span data-ttu-id="72fb3-537">Планирование развертывания App-V</span><span class="sxs-lookup"><span data-stu-id="72fb3-537">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





