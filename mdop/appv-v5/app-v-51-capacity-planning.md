---
title: Планирование мощности App-V 5.1
description: Планирование мощности App-V 5.1
author: dansimp
ms.assetid: 7a98062f-5a60-49d6-ab40-dc6057e1dd5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b152536b3c61e47f3fda84489b1e102c285e01c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814784"
---
# <span data-ttu-id="3620d-103">Планирование мощности App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="3620d-103">App-V 5.1 Capacity Planning</span></span>


<span data-ttu-id="3620d-104">Перечисленные ниже рекомендации можно использовать в качестве базового плана, чтобы определить сведения о планировании мощности, соответствующие инфраструктуре App-V 5,1 в Организации.</span><span class="sxs-lookup"><span data-stu-id="3620d-104">The following recommendations can be used as a baseline to help determine capacity planning information that is appropriate to your organization’s App-V 5.1 infrastructure.</span></span>

<span data-ttu-id="3620d-105">**Важно!**  Данные в этом разделе используются только в качестве общего руководства по планированию развертывания приложения-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3620d-105">**Important** Use the information in this section only as a general guide for planning your App-V 5.1 deployment.</span></span> <span data-ttu-id="3620d-106">Требования к системной мощности будут зависеть от конкретных сведений о вашем оборудовании и среде приложений.</span><span class="sxs-lookup"><span data-stu-id="3620d-106">Your system capacity requirements will depend on the specific details of your hardware and application environment.</span></span> <span data-ttu-id="3620d-107">Кроме того, в этом документе отображаются номера производительности, которые можно увидеть, и результаты могут отличаться.</span><span class="sxs-lookup"><span data-stu-id="3620d-107">Additionally, the performance numbers displayed in this document are examples and your results may vary.</span></span>

 

## <span data-ttu-id="3620d-108">Определение области охвата проекта</span><span class="sxs-lookup"><span data-stu-id="3620d-108">Determine the Project Scope</span></span>


<span data-ttu-id="3620d-109">Прежде чем приступить к разработке инфраструктуры App-V 5,1, необходимо определить область проекта.</span><span class="sxs-lookup"><span data-stu-id="3620d-109">Before you design the App-V 5.1 infrastructure, you must determine the project’s scope.</span></span> <span data-ttu-id="3620d-110">Область действия состоит из определения того, какие приложения будут доступны для выполнения практически и для определения конечных пользователей, и их расположения.</span><span class="sxs-lookup"><span data-stu-id="3620d-110">The scope consists of determining which applications will be available virtually and to also identify the target users, and their locations.</span></span> <span data-ttu-id="3620d-111">Эта информация поможет вам определить, какой тип инфраструктуры App-V 5,1 следует реализовать.</span><span class="sxs-lookup"><span data-stu-id="3620d-111">This information will help determine what type of App-V 5.1 infrastructure should be implemented.</span></span> <span data-ttu-id="3620d-112">Решения, касающиеся области охвата проекта, должны основываться на конкретных требованиях вашей организации.</span><span class="sxs-lookup"><span data-stu-id="3620d-112">Decisions about the scope of the project must be based on the specific needs of your organization.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3620d-113">Задача</span><span class="sxs-lookup"><span data-stu-id="3620d-113">Task</span></span></th>
<th align="left"><span data-ttu-id="3620d-114">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3620d-114">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-115">Определение области применения приложения</span><span class="sxs-lookup"><span data-stu-id="3620d-115">Determine Application Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="3620d-116">В зависимости от виртуализированных приложений инфраструктура App-V 5,1 может быть настроена различными способами.</span><span class="sxs-lookup"><span data-stu-id="3620d-116">Depending on the applications to be virtualized, the App-V 5.1 infrastructure can be set up in different ways.</span></span> <span data-ttu-id="3620d-117">Первая задача — определить приложения, которые нужно виртуализировать.</span><span class="sxs-lookup"><span data-stu-id="3620d-117">The first task is to define what applications you want to virtualize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3620d-118">Определение области расположения</span><span class="sxs-lookup"><span data-stu-id="3620d-118">Determine Location Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="3620d-119">Область расположения — это физическое расположение (например, в масштабах всей организации или в определенном географическом расположении), в котором планируется запускать виртуализированные приложения.</span><span class="sxs-lookup"><span data-stu-id="3620d-119">Location scope refers to the physical locations (for example, enterprise-wide or a specific geographic location) where you plan to run the virtualized applications.</span></span> <span data-ttu-id="3620d-120">Она также может ссылаться на заполнение пользователей (например, один отдел), который будет запускать виртуальные приложения.</span><span class="sxs-lookup"><span data-stu-id="3620d-120">It can also refer to the user population (for example, a single department) who will run the virtual applications.</span></span> <span data-ttu-id="3620d-121">Вы должны получить карту сети, которая содержит пути подключения, а также пропускную способность для каждого места и количество пользователей, использующих виртуализированные приложения и скорость связи WAN.</span><span class="sxs-lookup"><span data-stu-id="3620d-121">You should obtain a network map that includes the connection paths as well as available bandwidth to each location and the number of users using virtualized applications and the WAN link speed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3620d-122">Определение необходимости инфраструктуры App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="3620d-122">Determine Which App-V 5.1 Infrastructure is Required</span></span>


<span data-ttu-id="3620d-123">**Важно!**  Для обеих следующих моделей на компьютере, на котором планируется запускать виртуальные приложения, должен быть установлен клиент App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3620d-123">**Important** Both of the following models require the App-V 5.1 client to be installed on the computer where you plan to run virtual applications.</span></span>

<span data-ttu-id="3620d-124">Вы также можете управлять средой App-V 5,1 с помощью электронного решения для рассылки программного обеспечения (ESD), такого как Microsoft Systems Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="3620d-124">You can also manage your App-V 5.1 environment using an Electronic Software Distribution (ESD) solution such as Microsoft Systems Center Configuration Manager.</span></span> <span data-ttu-id="3620d-125">Дополнительные сведения о [том, как развертывать пакеты App-V 5,1 с помощью электронного распространения программного обеспечения](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span><span class="sxs-lookup"><span data-stu-id="3620d-125">For more information see [How to deploy App-V 5.1 Packages Using Electronic Software Distribution](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span></span>

 

-   <span data-ttu-id="3620d-126">**Отдельная модель** : Автономная модель позволяет использовать для распространения виртуальные приложения, поддерживающие установщик Windows, без потоковой передачи данных.</span><span class="sxs-lookup"><span data-stu-id="3620d-126">**Standalone Model** - The standalone model allows virtual applications to be Windows Installer-enabled for distribution without streaming.</span></span> <span data-ttu-id="3620d-127">App-V 5,1 в автономном режиме состоит из секвенсора и клиента; Дополнительные компоненты не требуются.</span><span class="sxs-lookup"><span data-stu-id="3620d-127">App-V 5.1 in Standalone Mode consists of the sequencer and the client; no additional components are required.</span></span> <span data-ttu-id="3620d-128">Приложения подготавливаются для виртуализации с помощью процессов, которые называются виртуализацией.</span><span class="sxs-lookup"><span data-stu-id="3620d-128">Applications are prepared for virtualization using a process called sequencing.</span></span> <span data-ttu-id="3620d-129">Дополнительные сведения можно найти [в разделе Планирование приложения Sequencer-V 5,1 и развертывание клиента](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="3620d-129">For more information see, [Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span></span> <span data-ttu-id="3620d-130">Изолированная модель рекомендуется для следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="3620d-130">The stand-alone model is recommended for the following scenarios:</span></span>

    -   <span data-ttu-id="3620d-131">С отключенными удаленными пользователями, которые не могут подключиться к инфраструктуре App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3620d-131">With disconnected remote users who cannot connect to the App-V 5.1 infrastructure.</span></span>

    -   <span data-ttu-id="3620d-132">При запуске системы управления программным обеспечением, например Configuration Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="3620d-132">When you are running a software management system, such as Configuration Manager 2012.</span></span>

    -   <span data-ttu-id="3620d-133">Если ограничения пропускной способности сети задерживает электронное распространение программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="3620d-133">When network bandwidth limitations inhibit electronic software distribution.</span></span>

-   <span data-ttu-id="3620d-134">**Полная модель инфраструктуры** — полная модель инфраструктуры предоставляет возможности распространения программного обеспечения, управления и создания отчетов; Она также включает потоковую передачу приложений по сети.</span><span class="sxs-lookup"><span data-stu-id="3620d-134">**Full Infrastructure Model** - The full infrastructure model provides for software distribution, management, and reporting capabilities; it also includes the streaming of applications across the network.</span></span> <span data-ttu-id="3620d-135">Модель полной инфраструктуры App-V 5,1 состоит из одного или нескольких серверов управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3620d-135">The App-V 5.1 Full Infrastructure Model consists of one or more App-V 5.1 management servers.</span></span> <span data-ttu-id="3620d-136">Сервер управления можно использовать для публикации приложений на всех клиентах.</span><span class="sxs-lookup"><span data-stu-id="3620d-136">The Management Server can be used to publish applications to all clients.</span></span> <span data-ttu-id="3620d-137">Процесс публикации поместит значки виртуальных приложений и ярлыки на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="3620d-137">The publishing process places the virtual application icons and shortcuts on the target computer.</span></span> <span data-ttu-id="3620d-138">Кроме того, он может выполнять потоковую передачу приложений для локальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="3620d-138">It can also stream applications to local users.</span></span> <span data-ttu-id="3620d-139">Дополнительные сведения об установке сервера управления можно найти в разделе [Планирование развертывания сервера App-V 5,1](planning-for-the-app-v-51-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="3620d-139">For more information about installing the management server see, [Planning for the App-V 5.1 Server Deployment](planning-for-the-app-v-51-server-deployment.md).</span></span> <span data-ttu-id="3620d-140">Полная модель инфраструктуры рекомендуется для следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="3620d-140">The full infrastructure model is recommended for the following scenarios:</span></span>

    <span data-ttu-id="3620d-141">**Важно!**  Для модели App-V 5,1 в полной инфраструктуре инфраструктуры требуется Microsoft SQL Server для хранения данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3620d-141">**Important** The App-V 5.1 full infrastructure model requires Microsoft SQL Server to store configuration data.</span></span> <span data-ttu-id="3620d-142">Дополнительные сведения см. в разделе [Поддерживаемые конфигурации App-V 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="3620d-142">For more information see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

     

    -   <span data-ttu-id="3620d-143">Если вы хотите опубликовать приложение на целевом компьютере с помощью сервера управления.</span><span class="sxs-lookup"><span data-stu-id="3620d-143">When you want to use the Management Server to publish the application to target computers.</span></span>

    -   <span data-ttu-id="3620d-144">Для быстрой подготовки приложений к целевым компьютерам.</span><span class="sxs-lookup"><span data-stu-id="3620d-144">For rapid provisioning of applications to target computers.</span></span>

    -   <span data-ttu-id="3620d-145">Если вы хотите использовать отчеты App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3620d-145">When you want to use App-V 5.1 reporting.</span></span>

## <span data-ttu-id="3620d-146">Рекомендации по выбору размера для сквозного сервера</span><span class="sxs-lookup"><span data-stu-id="3620d-146">End-to-end Server Sizing Guidance</span></span>


<span data-ttu-id="3620d-147">В следующем разделе содержатся сведения о сквозном изменении размера и планировании приложения App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3620d-147">The following section provides information about end-to-end App-V 5.1 sizing and planning.</span></span> <span data-ttu-id="3620d-148">Более подробную информацию можно найти в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="3620d-148">For more specific information, refer to the subsequent sections.</span></span>

<span data-ttu-id="3620d-149">**Примечание**  Время ответа на клиенте в цикле обработки — это время, затраченное на работу компьютера, на котором запущен клиент App-V 5,1, чтобы получить успешное уведомление от сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="3620d-149">**Note** Round trip response time on the client is the time taken by the computer running the App-V 5.1 client to receive a successful notification from the publishing server.</span></span> <span data-ttu-id="3620d-150">Время ответа цикла обработки на сервере публикаций — это время, потребовавшееся на компьютере, на котором запущен сервер публикаций, для получения успешно обновленных метаданных пакета с сервера управления.</span><span class="sxs-lookup"><span data-stu-id="3620d-150">Round trip response time on the publishing server is the time taken by the computer running the publishing server to receive a successful package metadata update from the management server.</span></span>

 

-   <span data-ttu-id="3620d-151">Клиенты 20 000 могут ориентироваться на один сервер публикаций для получения пакета в приемлемое время кругового приема.</span><span class="sxs-lookup"><span data-stu-id="3620d-151">20,000 clients can target a single publishing server to obtain the package refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="3620d-152">( &lt; 3 секунды)</span><span class="sxs-lookup"><span data-stu-id="3620d-152">(&lt;3 seconds)</span></span>

-   <span data-ttu-id="3620d-153">Один сервер управления может поддерживать до 50 серверов публикации для метаданных пакета в течение приемлемого времени приема-передачи.</span><span class="sxs-lookup"><span data-stu-id="3620d-153">A single management server can support up to 50 publishing servers for package metadata refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="3620d-154">( &lt; 5 секунд)</span><span class="sxs-lookup"><span data-stu-id="3620d-154">(&lt;5 seconds)</span></span>

## <a href="" id="---------app-v-5-1-management-server-capacity-planning-recommendations"></a> <span data-ttu-id="3620d-155">Рекомендации по планированию производительности сервера управления для App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="3620d-155">App-V 5.1 Management Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="3620d-156">Для серверов публикаций App-V 5,1 требуется сервер управления для запросов на обновление пакетов и ответов на обновление пакетов.</span><span class="sxs-lookup"><span data-stu-id="3620d-156">The App-V 5.1 publishing servers require the management server for package refresh requests and package refresh responses.</span></span> <span data-ttu-id="3620d-157">Затем сервер управления отправляет сведения в базу данных управления для получения информации.</span><span class="sxs-lookup"><span data-stu-id="3620d-157">The management server then sends the information to the management database to retrieve information.</span></span> <span data-ttu-id="3620d-158">Дополнительные сведения о конфигурациях, поддерживаемых сервером управления App-V 5,1, приведены в разделе [Поддерживаемые конфигурации App-v 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="3620d-158">For more information about App-V 5.1 management server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="3620d-159">**Примечание**  Время обновления по умолчанию на сервере публикаций App-V 5,1 составляет десять минут.</span><span class="sxs-lookup"><span data-stu-id="3620d-159">**Note** The default refresh time on the App-V 5.1 publishing server is ten minutes.</span></span>

 

<span data-ttu-id="3620d-160">При обращении нескольких одновременных серверов публикаций к единому серверу управления для обновления метаданных пакета на сервере публикаций влияют следующие три фактора.</span><span class="sxs-lookup"><span data-stu-id="3620d-160">When multiple simultaneous publishing servers contact a single management server for package metadata refreshes, the following three factors influence the round trip response time on the publishing server:</span></span>

1.  <span data-ttu-id="3620d-161">Количество серверов публикаций, выполняющих одновременные запросы.</span><span class="sxs-lookup"><span data-stu-id="3620d-161">Number of publishing servers making simultaneous requests.</span></span>

2.  <span data-ttu-id="3620d-162">Количество групп подключений, настроенных на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="3620d-162">Number of connection groups configured on the management server.</span></span>

3.  <span data-ttu-id="3620d-163">Количество групп доступа, настроенных на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="3620d-163">Number of access groups configured on the management server.</span></span>

<span data-ttu-id="3620d-164">В следующей таблице приведены дополнительные сведения о каждом факторе, влияющем на время приема круга.</span><span class="sxs-lookup"><span data-stu-id="3620d-164">The following table displays more information about each factor that impacts round trip time.</span></span>

<span data-ttu-id="3620d-165">**Примечание**  Время ответа цикла обработки — это время, потребовавшееся на компьютере, на котором работает сервер публикаций App-V 5,1, чтобы получить успешное обновление метаданных пакета от сервера управления.</span><span class="sxs-lookup"><span data-stu-id="3620d-165">**Note** Round trip response time is the time taken by the computer running the App-V 5.1 publishing server to receive a successful package metadata update from the management server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3620d-166">Факторы, влияющие на время ответа кругового цикла</span><span class="sxs-lookup"><span data-stu-id="3620d-166">Factors impacting round trip response time</span></span></th>
<th align="left"><span data-ttu-id="3620d-167">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3620d-167">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-168">Количество серверов публикаций, запрашивающих обновление метаданных пакета одновременно.</span><span class="sxs-lookup"><span data-stu-id="3620d-168">The number of publishing servers simultaneously requesting package metadata refreshes.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-169">Один сервер управления может отвечать на запросы до 320 серверов публикаций, запрашивающих публикацию метаданных одновременно.</span><span class="sxs-lookup"><span data-stu-id="3620d-169">A single management server can respond to up to 320 publishing servers requesting publishing metadata simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="3620d-170">Время ответа на запрос в формате кругового приема для 320 Pub Server составляет ~ 40 секунд.</span><span class="sxs-lookup"><span data-stu-id="3620d-170">Round trip response time for 320 pub servers is ~40 seconds.</span></span></p></li>
<li><p><span data-ttu-id="3620d-171">Для &lt; серверов публикаций 50 с запросом метаданных одновременно время ответа цикла обработки составляет &lt; 5 секунд.</span><span class="sxs-lookup"><span data-stu-id="3620d-171">For &lt;50 publishing servers requesting metadata simultaneously, the round trip response time is &lt;5 seconds.</span></span></p></li>
<li><p><span data-ttu-id="3620d-172">Время отклика от 50 до 320 сервера публикаций повышается линейно (примерно 2x).</span><span class="sxs-lookup"><span data-stu-id="3620d-172">From 50 to 320 publishing servers, the response time increases linearly (approximately 2x).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3620d-173">Количество групп подключений, настроенных на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="3620d-173">The number of connection groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-174">Для групп соединений до 100 не существует значительных изменений в времени ответа на цикл обработки на сервере публикации.</span><span class="sxs-lookup"><span data-stu-id="3620d-174">For up to 100 connection groups, there is no significant change in the round trip response time on the publishing server.</span></span></p></li>
<li><p><span data-ttu-id="3620d-175">Для групп соединений 100-400 существует незначительное линейное приращение времени ответа цикла обработки.</span><span class="sxs-lookup"><span data-stu-id="3620d-175">For 100 - 400 connection groups, there is a minor linear increase in the round trip response time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-176">Количество групп доступа, настроенных на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="3620d-176">The number of access groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-177">Для групп доступа до 40 имеется линейное (примерно 3x) приращение времени ответа на время приема-передачи на сервере публикации.</span><span class="sxs-lookup"><span data-stu-id="3620d-177">For up to 40 access groups, there is a linear (approximately 3x) increase in the round trip response time on the publishing server.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3620d-178">В следующей таблице показаны примеры значений для каждого из предыдущих факторов.</span><span class="sxs-lookup"><span data-stu-id="3620d-178">The following table displays sample values for each of the previous factors.</span></span> <span data-ttu-id="3620d-179">В каждом варианте пакеты 120 обновляются на сервере управления App-V 5.1.</span><span class="sxs-lookup"><span data-stu-id="3620d-179">In each variation, 120 packages are refreshed from the App-V 5.1management server.</span></span>

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
<th align="left"><span data-ttu-id="3620d-180">Сценарий</span><span class="sxs-lookup"><span data-stu-id="3620d-180">Scenario</span></span></th>
<th align="left"><span data-ttu-id="3620d-181">Вариант</span><span class="sxs-lookup"><span data-stu-id="3620d-181">Variation</span></span></th>
<th align="left"><span data-ttu-id="3620d-182">Количество групп соединения</span><span class="sxs-lookup"><span data-stu-id="3620d-182">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="3620d-183">Количество групп доступа</span><span class="sxs-lookup"><span data-stu-id="3620d-183">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="3620d-184">Количество серверов публикаций</span><span class="sxs-lookup"><span data-stu-id="3620d-184">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="3620d-185">Сервер или сервер управления публикации типа сетевого подключения</span><span class="sxs-lookup"><span data-stu-id="3620d-185">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="3620d-186">Время ответа цикла обработки на сервере публикаций (в секундах)</span><span class="sxs-lookup"><span data-stu-id="3620d-186">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="3620d-187">Использование ЦП на сервере управления</span><span class="sxs-lookup"><span data-stu-id="3620d-187">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-188">Серверы публикации одновременные связи с сервером управления для публикации метаданных.</span><span class="sxs-lookup"><span data-stu-id="3620d-188">Publishing servers simultaneously contacting management server for publishing metadata.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3620d-189">Количество серверов публикаций</span><span class="sxs-lookup"><span data-stu-id="3620d-189">Number of publishing servers</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-190">до</span><span class="sxs-lookup"><span data-stu-id="3620d-190">0</span></span></p></li>
<li><p><span data-ttu-id="3620d-191">до</span><span class="sxs-lookup"><span data-stu-id="3620d-191">0</span></span></p></li>
<li><p><span data-ttu-id="3620d-192">до</span><span class="sxs-lookup"><span data-stu-id="3620d-192">0</span></span></p></li>
<li><p><span data-ttu-id="3620d-193">до</span><span class="sxs-lookup"><span data-stu-id="3620d-193">0</span></span></p></li>
<li><p><span data-ttu-id="3620d-194">до</span><span class="sxs-lookup"><span data-stu-id="3620d-194">0</span></span></p></li>
<li><p><span data-ttu-id="3620d-195">до</span><span class="sxs-lookup"><span data-stu-id="3620d-195">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-196">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-196">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-197">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-197">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-198">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-198">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-199">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-199">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-200">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-200">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-201">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-201">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-202">50</span><span class="sxs-lookup"><span data-stu-id="3620d-202">50</span></span></p></li>
<li><p><span data-ttu-id="3620d-203">100</span><span class="sxs-lookup"><span data-stu-id="3620d-203">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-204">200</span><span class="sxs-lookup"><span data-stu-id="3620d-204">200</span></span></p></li>
<li><p><span data-ttu-id="3620d-205">300</span><span class="sxs-lookup"><span data-stu-id="3620d-205">300</span></span></p></li>
<li><p><span data-ttu-id="3620d-206">315</span><span class="sxs-lookup"><span data-stu-id="3620d-206">315</span></span></p></li>
<li><p><span data-ttu-id="3620d-207">320</span><span class="sxs-lookup"><span data-stu-id="3620d-207">320</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-208">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-208">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-209">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-209">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-210">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-210">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-211">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-211">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-212">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-212">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-213">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-213">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-214">5</span><span class="sxs-lookup"><span data-stu-id="3620d-214">5</span></span></p></li>
<li><p><span data-ttu-id="3620d-215">5-10</span><span class="sxs-lookup"><span data-stu-id="3620d-215">10</span></span></p></li>
<li><p><span data-ttu-id="3620d-216">19</span><span class="sxs-lookup"><span data-stu-id="3620d-216">19</span></span></p></li>
<li><p><span data-ttu-id="3620d-217">32</span><span class="sxs-lookup"><span data-stu-id="3620d-217">32</span></span></p></li>
<li><p><span data-ttu-id="3620d-218">30</span><span class="sxs-lookup"><span data-stu-id="3620d-218">30</span></span></p></li>
<li><p><span data-ttu-id="3620d-219">37</span><span class="sxs-lookup"><span data-stu-id="3620d-219">37</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-220">18</span><span class="sxs-lookup"><span data-stu-id="3620d-220">17</span></span></p></li>
<li><p><span data-ttu-id="3620d-221">18</span><span class="sxs-lookup"><span data-stu-id="3620d-221">17</span></span></p></li>
<li><p><span data-ttu-id="3620d-222">18</span><span class="sxs-lookup"><span data-stu-id="3620d-222">17</span></span></p></li>
<li><p><span data-ttu-id="3620d-223">10-15</span><span class="sxs-lookup"><span data-stu-id="3620d-223">15</span></span></p></li>
<li><p><span data-ttu-id="3620d-224">18</span><span class="sxs-lookup"><span data-stu-id="3620d-224">17</span></span></p></li>
<li><p><span data-ttu-id="3620d-225">10-15</span><span class="sxs-lookup"><span data-stu-id="3620d-225">15</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3620d-226">Метаданные публикации содержат группы подключений</span><span class="sxs-lookup"><span data-stu-id="3620d-226">Publishing metadata contains connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="3620d-227">Количество групп соединения</span><span class="sxs-lookup"><span data-stu-id="3620d-227">Number of connection groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-228">5-10</span><span class="sxs-lookup"><span data-stu-id="3620d-228">10</span></span></p></li>
<li><p><span data-ttu-id="3620d-229">50</span><span class="sxs-lookup"><span data-stu-id="3620d-229">50</span></span></p></li>
<li><p><span data-ttu-id="3620d-230">100</span><span class="sxs-lookup"><span data-stu-id="3620d-230">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-231">150</span><span class="sxs-lookup"><span data-stu-id="3620d-231">150</span></span></p></li>
<li><p><span data-ttu-id="3620d-232">300</span><span class="sxs-lookup"><span data-stu-id="3620d-232">300</span></span></p></li>
<li><p><span data-ttu-id="3620d-233">400</span><span class="sxs-lookup"><span data-stu-id="3620d-233">400</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-234">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-234">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-235">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-235">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-236">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-236">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-237">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-237">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-238">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-238">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-239">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-239">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-240">100</span><span class="sxs-lookup"><span data-stu-id="3620d-240">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-241">100</span><span class="sxs-lookup"><span data-stu-id="3620d-241">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-242">100</span><span class="sxs-lookup"><span data-stu-id="3620d-242">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-243">100</span><span class="sxs-lookup"><span data-stu-id="3620d-243">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-244">100</span><span class="sxs-lookup"><span data-stu-id="3620d-244">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-245">100</span><span class="sxs-lookup"><span data-stu-id="3620d-245">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-246">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-246">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-247">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-247">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-248">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-248">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-249">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-249">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-250">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-250">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-251">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-251">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-252">5-10</span><span class="sxs-lookup"><span data-stu-id="3620d-252">10</span></span></p></li>
<li><p><span data-ttu-id="3620d-253">11</span><span class="sxs-lookup"><span data-stu-id="3620d-253">11</span></span></p></li>
<li><p><span data-ttu-id="3620d-254">11</span><span class="sxs-lookup"><span data-stu-id="3620d-254">11</span></span></p></li>
<li><p><span data-ttu-id="3620d-255">шестнадцат</span><span class="sxs-lookup"><span data-stu-id="3620d-255">16</span></span></p></li>
<li><p><span data-ttu-id="3620d-256">максималь</span><span class="sxs-lookup"><span data-stu-id="3620d-256">22</span></span></p></li>
<li><p><span data-ttu-id="3620d-257">24</span><span class="sxs-lookup"><span data-stu-id="3620d-257">25</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-258">18</span><span class="sxs-lookup"><span data-stu-id="3620d-258">17</span></span></p></li>
<li><p><span data-ttu-id="3620d-259">19</span><span class="sxs-lookup"><span data-stu-id="3620d-259">19</span></span></p></li>
<li><p><span data-ttu-id="3620d-260">максималь</span><span class="sxs-lookup"><span data-stu-id="3620d-260">22</span></span></p></li>
<li><p><span data-ttu-id="3620d-261">19</span><span class="sxs-lookup"><span data-stu-id="3620d-261">19</span></span></p></li>
<li><p><span data-ttu-id="3620d-262">средняя</span><span class="sxs-lookup"><span data-stu-id="3620d-262">20</span></span></p></li>
<li><p><span data-ttu-id="3620d-263">средняя</span><span class="sxs-lookup"><span data-stu-id="3620d-263">20</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-264">Метаданные публикации содержат группы доступа</span><span class="sxs-lookup"><span data-stu-id="3620d-264">Publishing metadata contains access groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="3620d-265">Количество групп доступа</span><span class="sxs-lookup"><span data-stu-id="3620d-265">Number of access groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-266">до</span><span class="sxs-lookup"><span data-stu-id="3620d-266">0</span></span></p></li>
<li><p><span data-ttu-id="3620d-267">до</span><span class="sxs-lookup"><span data-stu-id="3620d-267">0</span></span></p></li>
<li><p><span data-ttu-id="3620d-268">до</span><span class="sxs-lookup"><span data-stu-id="3620d-268">0</span></span></p></li>
<li><p><span data-ttu-id="3620d-269">до</span><span class="sxs-lookup"><span data-stu-id="3620d-269">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-270">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-270">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-271">5-10</span><span class="sxs-lookup"><span data-stu-id="3620d-271">10</span></span></p></li>
<li><p><span data-ttu-id="3620d-272">средняя</span><span class="sxs-lookup"><span data-stu-id="3620d-272">20</span></span></p></li>
<li><p><span data-ttu-id="3620d-273">40</span><span class="sxs-lookup"><span data-stu-id="3620d-273">40</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-274">100</span><span class="sxs-lookup"><span data-stu-id="3620d-274">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-275">100</span><span class="sxs-lookup"><span data-stu-id="3620d-275">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-276">100</span><span class="sxs-lookup"><span data-stu-id="3620d-276">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-277">100</span><span class="sxs-lookup"><span data-stu-id="3620d-277">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-278">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-278">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-279">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-279">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-280">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-280">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-281">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-281">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-282">5-10</span><span class="sxs-lookup"><span data-stu-id="3620d-282">10</span></span></p></li>
<li><p><span data-ttu-id="3620d-283">43</span><span class="sxs-lookup"><span data-stu-id="3620d-283">43</span></span></p></li>
<li><p><span data-ttu-id="3620d-284">153</span><span class="sxs-lookup"><span data-stu-id="3620d-284">153</span></span></p></li>
<li><p><span data-ttu-id="3620d-285">535</span><span class="sxs-lookup"><span data-stu-id="3620d-285">535</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-286">18</span><span class="sxs-lookup"><span data-stu-id="3620d-286">17</span></span></p></li>
<li><p><span data-ttu-id="3620d-287">26</span><span class="sxs-lookup"><span data-stu-id="3620d-287">26</span></span></p></li>
<li><p><span data-ttu-id="3620d-288">24</span><span class="sxs-lookup"><span data-stu-id="3620d-288">24</span></span></p></li>
<li><p><span data-ttu-id="3620d-289">24</span><span class="sxs-lookup"><span data-stu-id="3620d-289">24</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3620d-290">Загрузка ЦП на компьютере, на котором работает сервер управления, составляет около 25%, независимо от количества серверов публикации, на которых она нацелена.</span><span class="sxs-lookup"><span data-stu-id="3620d-290">The CPU utilization of the computer running the management server is around 25% irrespective of the number of publishing servers targeting it.</span></span> <span data-ttu-id="3620d-291">Количество транзакций в базе данных Microsoft SQL Server (в секунду) запросы пакетов в секунду и соединения пользователя идентичны, независимо от количества серверов публикации.</span><span class="sxs-lookup"><span data-stu-id="3620d-291">The Microsoft SQL Server database transactions/sec, batch requests/sec and user connections are identical irrespective of the number of publishing servers.</span></span> <span data-ttu-id="3620d-292">Например: Transactions/sec составляет ~ 30, пакетные запросы ~ 200, а пользователь соединяет ~ 6.</span><span class="sxs-lookup"><span data-stu-id="3620d-292">For example: Transactions/sec is ~30, batch requests ~200, and user connects ~6.</span></span>

<span data-ttu-id="3620d-293">Если вы используете географически распределенное развертывание, где сервер управления & серверы публикации используют сеть медленного канала связи между ними, время кругового приема на серверах публикации выходит за допустимые пределы ( &lt; 5 секунд), даже для 100 одновременных запросов на одном сервере управления.</span><span class="sxs-lookup"><span data-stu-id="3620d-293">Using a geographically distributed deployment, where the management server & publishing servers utilize a slow link network between them, the round trip response time on the publishing servers is within acceptable time limits (&lt;5 seconds), even for 100 simultaneous requests on a single management server.</span></span>

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
<th align="left"><span data-ttu-id="3620d-294">Сценарий</span><span class="sxs-lookup"><span data-stu-id="3620d-294">Scenario</span></span></th>
<th align="left"><span data-ttu-id="3620d-295">Вариант</span><span class="sxs-lookup"><span data-stu-id="3620d-295">Variation</span></span></th>
<th align="left"><span data-ttu-id="3620d-296">Количество групп соединения</span><span class="sxs-lookup"><span data-stu-id="3620d-296">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="3620d-297">Количество групп доступа</span><span class="sxs-lookup"><span data-stu-id="3620d-297">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="3620d-298">Количество серверов публикаций</span><span class="sxs-lookup"><span data-stu-id="3620d-298">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="3620d-299">Сервер или сервер управления публикации типа сетевого подключения</span><span class="sxs-lookup"><span data-stu-id="3620d-299">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="3620d-300">Время ответа цикла обработки на сервере публикаций (в секундах)</span><span class="sxs-lookup"><span data-stu-id="3620d-300">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="3620d-301">Использование ЦП на сервере управления</span><span class="sxs-lookup"><span data-stu-id="3620d-301">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-302">Сетевое соединение между сервером публикации и сервером управления</span><span class="sxs-lookup"><span data-stu-id="3620d-302">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="3620d-303">Сеть 1,5 Мбит/с медленной связью</span><span class="sxs-lookup"><span data-stu-id="3620d-303">1.5 Mbps Slow link Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-304">до</span><span class="sxs-lookup"><span data-stu-id="3620d-304">0</span></span></p></li>
<li><p><span data-ttu-id="3620d-305">до</span><span class="sxs-lookup"><span data-stu-id="3620d-305">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-306">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-306">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-307">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-307">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-308">50</span><span class="sxs-lookup"><span data-stu-id="3620d-308">50</span></span></p></li>
<li><p><span data-ttu-id="3620d-309">100</span><span class="sxs-lookup"><span data-stu-id="3620d-309">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-310">1,5 Мбит/с, кабель DSL</span><span class="sxs-lookup"><span data-stu-id="3620d-310">1.5Mbps Cable DSL</span></span></p></li>
<li><p><span data-ttu-id="3620d-311">1,5 Мбит/с, кабель DSL</span><span class="sxs-lookup"><span data-stu-id="3620d-311">1.5Mbps Cable DSL</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-312">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="3620d-312">4</span></span></p></li>
<li><p><span data-ttu-id="3620d-313">5</span><span class="sxs-lookup"><span data-stu-id="3620d-313">5</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-314">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-314">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-315">2</span><span class="sxs-lookup"><span data-stu-id="3620d-315">2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3620d-316">Сетевое соединение между сервером публикации и сервером управления</span><span class="sxs-lookup"><span data-stu-id="3620d-316">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="3620d-317">Сеть ЛС/WIFI</span><span class="sxs-lookup"><span data-stu-id="3620d-317">LAN / WIFI Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-318">до</span><span class="sxs-lookup"><span data-stu-id="3620d-318">0</span></span></p></li>
<li><p><span data-ttu-id="3620d-319">до</span><span class="sxs-lookup"><span data-stu-id="3620d-319">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-320">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-320">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-321">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-321">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-322">100</span><span class="sxs-lookup"><span data-stu-id="3620d-322">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-323">200</span><span class="sxs-lookup"><span data-stu-id="3620d-323">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-324">Wifi</span><span class="sxs-lookup"><span data-stu-id="3620d-324">Wifi</span></span></p></li>
<li><p><span data-ttu-id="3620d-325">Wifi</span><span class="sxs-lookup"><span data-stu-id="3620d-325">Wifi</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-326">11</span><span class="sxs-lookup"><span data-stu-id="3620d-326">11</span></span></p></li>
<li><p><span data-ttu-id="3620d-327">средняя</span><span class="sxs-lookup"><span data-stu-id="3620d-327">20</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-328">10-15</span><span class="sxs-lookup"><span data-stu-id="3620d-328">15</span></span></p></li>
<li><p><span data-ttu-id="3620d-329">18</span><span class="sxs-lookup"><span data-stu-id="3620d-329">17</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3620d-330">Подключены ли сервер управления и серверы публикаций по медленному каналу связи или высокоскоростной сети, сервер управления может обрабатывать около 15 000 запросов на обновление пакетов в течение 30 минут.</span><span class="sxs-lookup"><span data-stu-id="3620d-330">Whether the management server and publishing servers are connected over a slow link network, or a high speed network, the management server can handle approximately 15,000 package refresh requests in 30 minutes.</span></span>

## <a href="" id="---------app-v-5-1-reporting-server-capacity-planning-recommendations"></a> <span data-ttu-id="3620d-331">Рекомендации по планированию мощности сервера для App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="3620d-331">App-V 5.1 Reporting Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="3620d-332">Клиенты App-V 5,1 отправляют данные отчета на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="3620d-332">App-V 5.1 clients send reporting data to the reporting server.</span></span> <span data-ttu-id="3620d-333">Затем сервер отчетов записывает данные в базу данных Microsoft SQL Server и возвращает успешное уведомление на компьютер, на котором запущен клиент App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3620d-333">The reporting server then records the information in the Microsoft SQL Server database and returns a successful notification back to the computer running App-V 5.1 client.</span></span> <span data-ttu-id="3620d-334">Дополнительные сведения о конфигурациях поддерживаемые сервером отчетов App-V 5,1 можно найти в статьях [Поддерживаемые конфигурации App-v 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="3620d-334">For more information about App-V 5.1 Reporting Server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="3620d-335">**Примечание**  Время ответа цикла обработки — это время, затраченное на компьютере, на котором запущен клиент App-V 5,1 для отправки данных отчетов на сервер отчетов и получения уведомления об успешном уведомлении от сервера отчетов.</span><span class="sxs-lookup"><span data-stu-id="3620d-335">**Note** Round trip response time is the time taken by the computer running the App-V 5.1 client to send the reporting information to the reporting server and receive a successful notification from the reporting server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3620d-336">Сценарий</span><span class="sxs-lookup"><span data-stu-id="3620d-336">Scenario</span></span></th>
<th align="left"><span data-ttu-id="3620d-337">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3620d-337">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-338">Несколько клиентов App-V 5,1 отправляют данные отчетов на сервер отчетов одновременно.</span><span class="sxs-lookup"><span data-stu-id="3620d-338">Multiple App-V 5.1 clients send reporting information to the reporting server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-339">Время ответа от сервера отчетов составляет 2,6 секунд для клиентов 500.</span><span class="sxs-lookup"><span data-stu-id="3620d-339">Round trip response time from the reporting server is 2.6 seconds for 500 clients.</span></span></p></li>
<li><p><span data-ttu-id="3620d-340">Время ответа от сервера отчетов составляет 5,65 секунд для клиентов 1000.</span><span class="sxs-lookup"><span data-stu-id="3620d-340">Round trip response time from the reporting server is 5.65 seconds for 1000 clients.</span></span></p></li>
<li><p><span data-ttu-id="3620d-341">Время реагирования на круговую передачу в зависимости от количества клиентов возрастает в линейном режиме.</span><span class="sxs-lookup"><span data-stu-id="3620d-341">Round trip response time increases linearly depending on number of clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3620d-342">Количество запросов в секунду, обработанных сервером отчетов.</span><span class="sxs-lookup"><span data-stu-id="3620d-342">Requests per second processed by the reporting server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-343">Один сервер отчетов и единая база данных могут обрабатывать не более 139 запросов в секунду.</span><span class="sxs-lookup"><span data-stu-id="3620d-343">A single reporting server and a single database, can process a maximum of 139 requests per second.</span></span> <span data-ttu-id="3620d-344">Среднее значение составляет 121 запросов в секунду.</span><span class="sxs-lookup"><span data-stu-id="3620d-344">The average is 121 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="3620d-345">Используя два сервера отчетов для одной базы данных Microsoft SQL Server, средние запросы на секунду похожи на один сервер отчетов = ~ 127, с максимальным количеством запросов 278 в секунду.</span><span class="sxs-lookup"><span data-stu-id="3620d-345">Using two reporting servers reporting to the same Microsoft SQL Server database, the average requests/second is similar to a single reporting server = ~127, with a max of 278 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="3620d-346">Один сервер отчетов может обрабатывать одновременные и активные соединения 500.</span><span class="sxs-lookup"><span data-stu-id="3620d-346">A single reporting server can process 500 concurrent/active connections.</span></span></p></li>
<li><p><span data-ttu-id="3620d-347">Один сервер отчетов может обрабатывать максимум 1500 одновременных подключений.</span><span class="sxs-lookup"><span data-stu-id="3620d-347">A single reporting server can process a maximum 1500 concurrent connections.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-348">База данных отчетов.</span><span class="sxs-lookup"><span data-stu-id="3620d-348">Reporting Database.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-349">Конфликт блокировки на компьютере с Microsoft SQL Server — это ограничивающий коэффициент запросов в секунду.</span><span class="sxs-lookup"><span data-stu-id="3620d-349">Lock contention on the computer running Microsoft SQL Server is the limiting factor for requests/second.</span></span></p></li>
<li><p><span data-ttu-id="3620d-350">Пропускная способность и время отклика не зависят от размера базы данных.</span><span class="sxs-lookup"><span data-stu-id="3620d-350">Throughput and response time are independent of database size.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3620d-351">**Расчет случайной задержки**:</span><span class="sxs-lookup"><span data-stu-id="3620d-351">**Calculating random delay**:</span></span>

<span data-ttu-id="3620d-352">Случайная задержка определяет максимальную задержку (в минутах) для данных, отправляемых на сервер отчетов.</span><span class="sxs-lookup"><span data-stu-id="3620d-352">The random delay specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="3620d-353">При запуске запланированной задачи клиент создает произвольную задержку от **0** до **ReportingRandomDelay** и ждет указанное время перед отправкой данных.</span><span class="sxs-lookup"><span data-stu-id="3620d-353">When the scheduled task is started, the client generates a random delay between **0** and **ReportingRandomDelay** and will wait the specified duration before sending data.</span></span>

<span data-ttu-id="3620d-354">Произвольная задержка = 4 \ \* количество клиентов/среднее число запросов в секунду.</span><span class="sxs-lookup"><span data-stu-id="3620d-354">Random delay = 4 \* number of clients / average requests per second.</span></span>

<span data-ttu-id="3620d-355">Пример: для клиентов 500 с количеством запросов 120 в секунду случайная задержка — 4 \ \* 500/120 = ~ 17 минут.</span><span class="sxs-lookup"><span data-stu-id="3620d-355">Example: For 500 clients, with 120 requests per second, the Random delay is, 4 \* 500 / 120 = ~17 minutes.</span></span>

## <a href="" id="---------app-v-5-1-publishing-server-capacity-planning-recommendations"></a> <span data-ttu-id="3620d-356">Рекомендации по планированию производительности сервера App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="3620d-356">App-V 5.1 Publishing Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="3620d-357">Компьютеры, на которых работает клиент App-V 5,1, подключаются к серверу публикации App-v 5,1 для отправки запроса на обновление публикации и получения ответа.</span><span class="sxs-lookup"><span data-stu-id="3620d-357">Computers running the App-V 5.1 client connect to the App-V 5.1 publishing server to send a publishing refresh request and to receive a response.</span></span> <span data-ttu-id="3620d-358">Время отклика на круговую передачу измеряется на компьютере, на котором запущен клиент App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3620d-358">Round trip response time is measured on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="3620d-359">Время процессора измеряется на сервере публикаций.</span><span class="sxs-lookup"><span data-stu-id="3620d-359">Processor time is measured on the publishing server.</span></span> <span data-ttu-id="3620d-360">Дополнительные сведения о конфигурациях, поддерживаемых сервером публикаций App-V 5,1, приведены в разделе [Поддерживаемые конфигурации App-v 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="3620d-360">For more information about App-V 5.1 Publishing Server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="3620d-361">**Важно!**  В списке ниже приведены основные факторы, которые необходимо учитывать при настройке сервера публикаций App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3620d-361">**Important** The following list displays the main factors to consider when setting up the App-V 5.1 publishing server:</span></span>

-   <span data-ttu-id="3620d-362">Количество клиентов, которые одновременно подключаются к одному серверу публикаций.</span><span class="sxs-lookup"><span data-stu-id="3620d-362">The number of clients connecting simultaneously to a single publishing server.</span></span>

-   <span data-ttu-id="3620d-363">Количество пакетов в каждом обновлении.</span><span class="sxs-lookup"><span data-stu-id="3620d-363">The number of packages in each refresh.</span></span>

-   <span data-ttu-id="3620d-364">Доступная пропускная способность сети между клиентом и сервером публикаций App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3620d-364">The available network bandwidth in your environment between the client and the App-V 5.1 publishing server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3620d-365">Сценарий</span><span class="sxs-lookup"><span data-stu-id="3620d-365">Scenario</span></span></th>
<th align="left"><span data-ttu-id="3620d-366">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3620d-366">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-367">Несколько клиентов App-V 5,1 подключаются к одному серверу публикаций одновременно.</span><span class="sxs-lookup"><span data-stu-id="3620d-367">Multiple App-V 5.1 clients connect to a single publishing server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-368">Сервер публикаций, использующий два ядра процессора, может отвечать не более чем на 5000 клиентов, которые запрашивают обновление одновременно.</span><span class="sxs-lookup"><span data-stu-id="3620d-368">A publishing server running dual core processors can respond to at most 5000 clients requesting a refresh simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="3620d-369">Для клиентов 5000-10000 для сервера публикаций требуется не менее четырех ядер.</span><span class="sxs-lookup"><span data-stu-id="3620d-369">For 5000-10000 clients, the publishing server requires a minimum quad core.</span></span></p></li>
<li><p><span data-ttu-id="3620d-370">Для клиентов 10000-20000 сервер публикаций должен иметь два четырехъядерных ядра для более эффективного отклика.</span><span class="sxs-lookup"><span data-stu-id="3620d-370">For 10000-20000 clients, the publishing server should have dual quad cores for more efficient response times.</span></span></p></li>
<li><p><span data-ttu-id="3620d-371">Сервер публикаций с четырехъядерным процессором может обновлять до 10000 пакетов в течение 3 секунд.</span><span class="sxs-lookup"><span data-stu-id="3620d-371">A publishing server with a quad core can refresh up to 10000 packages within 3 seconds.</span></span> <span data-ttu-id="3620d-372">(Поддержка одновременных клиентов 10000)</span><span class="sxs-lookup"><span data-stu-id="3620d-372">(Supporting 10000 simultaneous clients)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3620d-373">Количество пакетов в каждом обновлении.</span><span class="sxs-lookup"><span data-stu-id="3620d-373">Number of packages in each refresh.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-374">Увеличение количества пакетов увеличит время отклика на ~ 40% (до 1000 пакетов).</span><span class="sxs-lookup"><span data-stu-id="3620d-374">Increasing number of packages will increase response time by ~40% (up to 1000 packages).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-375">Сеть между клиентом App-V 5,1 и сервером публикации.</span><span class="sxs-lookup"><span data-stu-id="3620d-375">Network between the App-V 5.1 client and the publishing server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-376">В течение медленной сети (1,5 Мбит/с) время ответа увеличивается на 97% (до 1000 пользователей).</span><span class="sxs-lookup"><span data-stu-id="3620d-376">Across a slow network (1.5 Mbps bandwidth), there is a 97% increase in response time compared to LAN (up to 1000 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3620d-377">**Примечание**  Использование ЦП сервера публикаций всегда велико в течение интервала времени, когда он должен обрабатывать одновременные запросы ( &gt; 90% в большинстве случаев).</span><span class="sxs-lookup"><span data-stu-id="3620d-377">**Note** The publishing server CPU usage is always high during the time interval when it has to process simultaneous requests (&gt;90% in most cases).</span></span> <span data-ttu-id="3620d-378">Сервер публикаций может обрабатывать запросы ~ 1500 клиента через 1 секунду.</span><span class="sxs-lookup"><span data-stu-id="3620d-378">The publishing server can handle ~1500 client requests in 1 second.</span></span>

 

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
<th align="left"><span data-ttu-id="3620d-379">Сценарий</span><span class="sxs-lookup"><span data-stu-id="3620d-379">Scenario</span></span></th>
<th align="left"><span data-ttu-id="3620d-380">Вариант</span><span class="sxs-lookup"><span data-stu-id="3620d-380">Variation</span></span></th>
<th align="left"><span data-ttu-id="3620d-381">Число клиентов App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="3620d-381">Number of App-V 5.1 clients</span></span></th>
<th align="left"><span data-ttu-id="3620d-382">Количество пакетов</span><span class="sxs-lookup"><span data-stu-id="3620d-382">Number of packages</span></span></th>
<th align="left"><span data-ttu-id="3620d-383">Конфигурация процессора на сервере публикаций</span><span class="sxs-lookup"><span data-stu-id="3620d-383">Processor configuration on the publishing server</span></span></th>
<th align="left"><span data-ttu-id="3620d-384">Сервер публикации или приложение App-5,1 V типа "Сетевое подключение"</span><span class="sxs-lookup"><span data-stu-id="3620d-384">Network connection type publishing server / App-V 5.1 client</span></span></th>
<th align="left"><span data-ttu-id="3620d-385">Время кругового обращения в клиенте App-V 5,1 (в секундах)</span><span class="sxs-lookup"><span data-stu-id="3620d-385">Round trip time on the App-V 5.1 client (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="3620d-386">Загрузка ЦП на сервере публикаций (в%)</span><span class="sxs-lookup"><span data-stu-id="3620d-386">CPU utilization on publishing server (in %)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-387">Клиент App-V 5,1 отправляет запрос на обновление публикации &amp; , каждый запрос содержит пакеты 120.</span><span class="sxs-lookup"><span data-stu-id="3620d-387">App-V 5.1 client sends publishing refresh request &amp; receives response, each request containing 120 packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="3620d-388">Количество клиентов</span><span class="sxs-lookup"><span data-stu-id="3620d-388">Number of clients</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-389">100</span><span class="sxs-lookup"><span data-stu-id="3620d-389">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-390">1000</span><span class="sxs-lookup"><span data-stu-id="3620d-390">1000</span></span></p></li>
<li><p><span data-ttu-id="3620d-391">5000</span><span class="sxs-lookup"><span data-stu-id="3620d-391">5000</span></span></p></li>
<li><p><span data-ttu-id="3620d-392">10000</span><span class="sxs-lookup"><span data-stu-id="3620d-392">10000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-393">120</span><span class="sxs-lookup"><span data-stu-id="3620d-393">120</span></span></p></li>
<li><p><span data-ttu-id="3620d-394">120</span><span class="sxs-lookup"><span data-stu-id="3620d-394">120</span></span></p></li>
<li><p><span data-ttu-id="3620d-395">120</span><span class="sxs-lookup"><span data-stu-id="3620d-395">120</span></span></p></li>
<li><p><span data-ttu-id="3620d-396">120</span><span class="sxs-lookup"><span data-stu-id="3620d-396">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-397">Двухъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="3620d-397">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="3620d-398">Двухъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="3620d-398">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="3620d-399">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="3620d-399">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="3620d-400">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="3620d-400">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-401">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-401">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-402">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-402">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-403">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-403">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-404">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-404">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-405">1,1</span><span class="sxs-lookup"><span data-stu-id="3620d-405">1</span></span></p></li>
<li><p><span data-ttu-id="3620d-406">2</span><span class="sxs-lookup"><span data-stu-id="3620d-406">2</span></span></p></li>
<li><p><span data-ttu-id="3620d-407">2</span><span class="sxs-lookup"><span data-stu-id="3620d-407">2</span></span></p></li>
<li><p><span data-ttu-id="3620d-408">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="3620d-408">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-409">100</span><span class="sxs-lookup"><span data-stu-id="3620d-409">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-410">99</span><span class="sxs-lookup"><span data-stu-id="3620d-410">99</span></span></p></li>
<li><p><span data-ttu-id="3620d-411">89</span><span class="sxs-lookup"><span data-stu-id="3620d-411">89</span></span></p></li>
<li><p><span data-ttu-id="3620d-412">77</span><span class="sxs-lookup"><span data-stu-id="3620d-412">77</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3620d-413">Несколько пакетов в каждом обновлении</span><span class="sxs-lookup"><span data-stu-id="3620d-413">Multiple packages in each refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="3620d-414">Количество пакетов</span><span class="sxs-lookup"><span data-stu-id="3620d-414">Number of packages</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-415">1000</span><span class="sxs-lookup"><span data-stu-id="3620d-415">1000</span></span></p></li>
<li><p><span data-ttu-id="3620d-416">1000</span><span class="sxs-lookup"><span data-stu-id="3620d-416">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-417">500</span><span class="sxs-lookup"><span data-stu-id="3620d-417">500</span></span></p></li>
<li><p><span data-ttu-id="3620d-418">1000</span><span class="sxs-lookup"><span data-stu-id="3620d-418">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-419">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="3620d-419">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="3620d-420">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="3620d-420">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-421">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-421">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-422">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-422">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-423">2</span><span class="sxs-lookup"><span data-stu-id="3620d-423">2</span></span></p></li>
<li><p><span data-ttu-id="3620d-424">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="3620d-424">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-425">92</span><span class="sxs-lookup"><span data-stu-id="3620d-425">92</span></span></p></li>
<li><p><span data-ttu-id="3620d-426">91</span><span class="sxs-lookup"><span data-stu-id="3620d-426">91</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-427">Сеть между клиентом и сервером публикаций</span><span class="sxs-lookup"><span data-stu-id="3620d-427">Network between client and publishing server</span></span></p></td>
<td align="left"><p><span data-ttu-id="3620d-428">сеть 1,5 Мбит/с медленной связью</span><span class="sxs-lookup"><span data-stu-id="3620d-428">1.5 Mbps Slow link network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-429">100</span><span class="sxs-lookup"><span data-stu-id="3620d-429">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-430">500</span><span class="sxs-lookup"><span data-stu-id="3620d-430">500</span></span></p></li>
<li><p><span data-ttu-id="3620d-431">1000</span><span class="sxs-lookup"><span data-stu-id="3620d-431">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-432">120</span><span class="sxs-lookup"><span data-stu-id="3620d-432">120</span></span></p></li>
<li><p><span data-ttu-id="3620d-433">120</span><span class="sxs-lookup"><span data-stu-id="3620d-433">120</span></span></p></li>
<li><p><span data-ttu-id="3620d-434">120</span><span class="sxs-lookup"><span data-stu-id="3620d-434">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-435">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="3620d-435">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="3620d-436">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="3620d-436">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="3620d-437">Четырехъядерный процессор</span><span class="sxs-lookup"><span data-stu-id="3620d-437">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-438">1,5 Мбит/с в пределах континентальные сети</span><span class="sxs-lookup"><span data-stu-id="3620d-438">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-439">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="3620d-439">3</span></span></p></li>
<li><p><span data-ttu-id="3620d-440">10 (с количеством сбоев 0,2%)</span><span class="sxs-lookup"><span data-stu-id="3620d-440">10 (with 0.2% failure rate)</span></span></p></li>
<li><p><span data-ttu-id="3620d-441">17 (с количеством сбоев 1%)</span><span class="sxs-lookup"><span data-stu-id="3620d-441">17 (with 1% failure rate)</span></span></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-1-streaming-capacity-planning-recommendations"></a> <span data-ttu-id="3620d-442">Рекомендации по планированию мощности потоков App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="3620d-442">App-V 5.1 Streaming Capacity Planning Recommendations</span></span>


<span data-ttu-id="3620d-443">Компьютеры, на которых выполняется поток клиента App-V 5,1, виртуальный пакет приложения от сервера потоков.</span><span class="sxs-lookup"><span data-stu-id="3620d-443">Computers running the App-V 5.1 client stream the virtual application package from the streaming server.</span></span> <span data-ttu-id="3620d-444">Время отклика на круговую передачу измеряется на компьютере, на котором запущен клиент App-V 5,1, а также время, затраченное на потоковую передачу всего пакета.</span><span class="sxs-lookup"><span data-stu-id="3620d-444">Round trip response time is measured on the computer running the App-V 5.1 client, and is the time taken to stream the entire package.</span></span>

<span data-ttu-id="3620d-445">**Важно!**  В следующем списке приведены основные факторы, которые необходимо учитывать при настройке потокового сервера App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="3620d-445">**Important** The following list identifies the main factors to consider when setting up the App-V 5.1 streaming server:</span></span>

-   <span data-ttu-id="3620d-446">Количество клиентов, одновременно выполняющих потоковую передачу пакетов приложения с одного сервера потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="3620d-446">The number of clients streaming application packages simultaneously from a single streaming server.</span></span>

-   <span data-ttu-id="3620d-447">Размер пакета, который передается в потоке.</span><span class="sxs-lookup"><span data-stu-id="3620d-447">The size of the package being streamed.</span></span>

-   <span data-ttu-id="3620d-448">Доступная пропускная способность сети между клиентом и сервером потоковой передачи данных.</span><span class="sxs-lookup"><span data-stu-id="3620d-448">The available network bandwidth in your environment between the client and the streaming server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3620d-449">Сценарий</span><span class="sxs-lookup"><span data-stu-id="3620d-449">Scenario</span></span></th>
<th align="left"><span data-ttu-id="3620d-450">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3620d-450">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-451">Несколько клиентов App-V 5,1 одновременные потоковые приложения на одном поток-сервере.</span><span class="sxs-lookup"><span data-stu-id="3620d-451">Multiple App-V 5.1 clients stream applications from a single streaming server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-452">Если количество клиентов, одновременно выполняющих потоковую передачу на одном и том же сервере, будет увеличиваться, существует линейная связь с пакетом для загрузки/потокового времени.</span><span class="sxs-lookup"><span data-stu-id="3620d-452">If the number of clients simultaneously streaming from the same server increases, there is a linear relationship with the package download/streaming time.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3620d-453">Размер пакета, который передается в потоке.</span><span class="sxs-lookup"><span data-stu-id="3620d-453">Size of the package being streamed.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-454">Размер пакета имеет значительное влияние на потоковую передачу и время загрузки только для больших пакетов размером ~ 1 ГБ.</span><span class="sxs-lookup"><span data-stu-id="3620d-454">The package size has a significant impact on the streaming/download time only for larger packages with a size ~ 1GB.</span></span> <span data-ttu-id="3620d-455">Для размеров пакета от 3 до 100 МБ количество потоков в диапазоне от 20 до 100 секунд с 100 одновременных клиентов.</span><span class="sxs-lookup"><span data-stu-id="3620d-455">For package sizes ranging from 3 MB to 100 MB, the streaming time ranges from 20 seconds to 100 seconds, with 100 simultaneous clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-456">Сеть между клиентом App-V 5,1 и потоковым сервером.</span><span class="sxs-lookup"><span data-stu-id="3620d-456">Network between the App-V 5.1 client and the streaming server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-457">В течение медленной сети (1,5 Мбит/с) время ответа увеличивается на 70-80% (до 100 пользователей).</span><span class="sxs-lookup"><span data-stu-id="3620d-457">Across a slow network (1.5 Mbps bandwidth), there is a 70-80% increase in response time compared to LAN (up to 100 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3620d-458">В следующей таблице показаны примеры значений для каждого из факторов, описанных в предыдущем списке.</span><span class="sxs-lookup"><span data-stu-id="3620d-458">The following table displays sample values for each of the factors in the previous list:</span></span>

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
<th align="left"><span data-ttu-id="3620d-459">Сценарий</span><span class="sxs-lookup"><span data-stu-id="3620d-459">Scenario</span></span></th>
<th align="left"><span data-ttu-id="3620d-460">Вариант</span><span class="sxs-lookup"><span data-stu-id="3620d-460">Variation</span></span></th>
<th align="left"><span data-ttu-id="3620d-461">Число клиентов App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="3620d-461">Number of App-V 5.1 clients</span></span></th>
<th align="left"><span data-ttu-id="3620d-462">Размер каждого пакета</span><span class="sxs-lookup"><span data-stu-id="3620d-462">Size of each package</span></span></th>
<th align="left"><span data-ttu-id="3620d-463">Сервер потоков данных сетевого подключения (App-V), клиент 5,1</span><span class="sxs-lookup"><span data-stu-id="3620d-463">Network connection type streaming server / App-V 5.1 client</span></span></th>
<th align="left"><span data-ttu-id="3620d-464">Время кругового обращения в клиенте App-V 5,1 (в секундах)</span><span class="sxs-lookup"><span data-stu-id="3620d-464">Round trip time on the App-V 5.1 client (in seconds)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-465">Несколько клиентов App-V 5,1 попотоковые пакеты виртуальных приложений с потокового сервера.</span><span class="sxs-lookup"><span data-stu-id="3620d-465">Multiple App-V 5.1 clients streaming virtual application packages from a streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3620d-466">Количество клиентов.</span><span class="sxs-lookup"><span data-stu-id="3620d-466">Number of clients.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-467">100</span><span class="sxs-lookup"><span data-stu-id="3620d-467">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-468">200</span><span class="sxs-lookup"><span data-stu-id="3620d-468">200</span></span></p></li>
<li><p><span data-ttu-id="3620d-469">1000</span><span class="sxs-lookup"><span data-stu-id="3620d-469">1000</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="3620d-470">100</span><span class="sxs-lookup"><span data-stu-id="3620d-470">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-471">200</span><span class="sxs-lookup"><span data-stu-id="3620d-471">200</span></span></p></li>
<li><p><span data-ttu-id="3620d-472">1000</span><span class="sxs-lookup"><span data-stu-id="3620d-472">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-473">3,5 MБ</span><span class="sxs-lookup"><span data-stu-id="3620d-473">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="3620d-474">3,5 MБ</span><span class="sxs-lookup"><span data-stu-id="3620d-474">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="3620d-475">3,5 MБ</span><span class="sxs-lookup"><span data-stu-id="3620d-475">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="3620d-476">5 МБ</span><span class="sxs-lookup"><span data-stu-id="3620d-476">5 MB</span></span></p></li>
<li><p><span data-ttu-id="3620d-477">5 МБ</span><span class="sxs-lookup"><span data-stu-id="3620d-477">5 MB</span></span></p></li>
<li><p><span data-ttu-id="3620d-478">5 МБ</span><span class="sxs-lookup"><span data-stu-id="3620d-478">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-479">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-479">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-480">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-480">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-481">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-481">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="3620d-482">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-482">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-483">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-483">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-484">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-484">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-485">составляет</span><span class="sxs-lookup"><span data-stu-id="3620d-485">29</span></span></p></li>
<li><p><span data-ttu-id="3620d-486">39</span><span class="sxs-lookup"><span data-stu-id="3620d-486">39</span></span></p></li>
<li><p><span data-ttu-id="3620d-487">391</span><span class="sxs-lookup"><span data-stu-id="3620d-487">391</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="3620d-488">35</span><span class="sxs-lookup"><span data-stu-id="3620d-488">35</span></span></p></li>
<li><p><span data-ttu-id="3620d-489">68</span><span class="sxs-lookup"><span data-stu-id="3620d-489">68</span></span></p></li>
<li><p><span data-ttu-id="3620d-490">461</span><span class="sxs-lookup"><span data-stu-id="3620d-490">461</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3620d-491">Размер каждого пакета, который передается в потоке.</span><span class="sxs-lookup"><span data-stu-id="3620d-491">Size of each package being streamed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3620d-492">Размер каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="3620d-492">Size of each package.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-493">100</span><span class="sxs-lookup"><span data-stu-id="3620d-493">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-494">200</span><span class="sxs-lookup"><span data-stu-id="3620d-494">200</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="3620d-495">100</span><span class="sxs-lookup"><span data-stu-id="3620d-495">100</span></span></p></li>
<li><p><span data-ttu-id="3620d-496">200</span><span class="sxs-lookup"><span data-stu-id="3620d-496">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-497">21 МБАЙТ</span><span class="sxs-lookup"><span data-stu-id="3620d-497">21 MB</span></span></p></li>
<li><p><span data-ttu-id="3620d-498">21 МБАЙТ</span><span class="sxs-lookup"><span data-stu-id="3620d-498">21 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="3620d-499">109</span><span class="sxs-lookup"><span data-stu-id="3620d-499">109</span></span></p></li>
<li><p><span data-ttu-id="3620d-500">109</span><span class="sxs-lookup"><span data-stu-id="3620d-500">109</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-501">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-501">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-502">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-502">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="3620d-503">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-503">LAN</span></span></p></li>
<li><p><span data-ttu-id="3620d-504">Локальная сеть</span><span class="sxs-lookup"><span data-stu-id="3620d-504">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="3620d-505">33</span><span class="sxs-lookup"><span data-stu-id="3620d-505">33</span></span></p>
<p><span data-ttu-id="3620d-506">83</span><span class="sxs-lookup"><span data-stu-id="3620d-506">83</span></span></p>
<p></p>
<p><span data-ttu-id="3620d-507">100</span><span class="sxs-lookup"><span data-stu-id="3620d-507">100</span></span></p>
<p><span data-ttu-id="3620d-508">160</span><span class="sxs-lookup"><span data-stu-id="3620d-508">160</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3620d-509">Сетевое соединение между клиентом и приложением-V 5,1 Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="3620d-509">Network connection between client and App-V 5.1 streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3620d-510">1,5 Мбит/с медленной связью сети.</span><span class="sxs-lookup"><span data-stu-id="3620d-510">1.5 Mbps Slow link network.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-511">100</span><span class="sxs-lookup"><span data-stu-id="3620d-511">100</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="3620d-512">100</span><span class="sxs-lookup"><span data-stu-id="3620d-512">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-513">3,5 MБ</span><span class="sxs-lookup"><span data-stu-id="3620d-513">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="3620d-514">5 МБ</span><span class="sxs-lookup"><span data-stu-id="3620d-514">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="3620d-515">1,5 Мбит/с в пределах континентальные сети</span><span class="sxs-lookup"><span data-stu-id="3620d-515">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="3620d-516">102</span><span class="sxs-lookup"><span data-stu-id="3620d-516">102</span></span></p>
<p></p>
<p><span data-ttu-id="3620d-517">121</span><span class="sxs-lookup"><span data-stu-id="3620d-517">121</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3620d-518">Каждый потоковый сервер App-V 5,1 должен обрабатывать 200 минимум одновременных потоков приложений, поддерживающих виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="3620d-518">Each App-V 5.1 streaming server should be able to handle a minimum of 200 clients concurrently streaming virtualized applications.</span></span>

<span data-ttu-id="3620d-519">**Примечание**  Фактическое время на этот поток будет определяться в первую очередь количеством потоков на клиентах, число пакетов, размер пакета, сетевая активность сервера и условия сети.</span><span class="sxs-lookup"><span data-stu-id="3620d-519">**Note** The actual time to it will take to stream is determined primarily by the number of clients streaming simultaneously, number of packages, package size, the server’s network activity, and network conditions.</span></span>

 

<span data-ttu-id="3620d-520">Например, пользователь может перечислить пакет 100 МБ менее чем на 2 минуты, когда 100 одновременных клиентов переносят потоковую передачу на сервер.</span><span class="sxs-lookup"><span data-stu-id="3620d-520">For example, an average user can stream a 100 MB package in less than 2 minutes, when 100 simultaneous clients are streaming from the server.</span></span> <span data-ttu-id="3620d-521">Однако пакет размером 1 ГБ может занять до 30 минут.</span><span class="sxs-lookup"><span data-stu-id="3620d-521">However, a package of size 1 GB could take up to 30 minutes.</span></span> <span data-ttu-id="3620d-522">В большинстве реальных сред потребность в потоковых данных не распределена равномерно, вам необходимо понять приблизительные пиковые требования к потоковой передаче в среде для правильного изменения числа требуемых потоков серверов.</span><span class="sxs-lookup"><span data-stu-id="3620d-522">In most real world environments streaming demand is not uniformly distributed, you will need to understand the approximate peak streaming requirements present in your environment in order to properly size the number of required streaming servers.</span></span>

<span data-ttu-id="3620d-523">Количество клиентов, которые может поддерживать потоковый сервер, может быть значительно увеличено, а пиковые требования к потоковой передаче уменьшились при предварительном кэшировании приложений.</span><span class="sxs-lookup"><span data-stu-id="3620d-523">The number of clients a streaming server can support can be significantly increased and the peak streaming requirements reduced if you pre-cache your applications.</span></span> <span data-ttu-id="3620d-524">Вы также можете увеличивать количество клиентов, которые может поддерживать потоковый сервер, с помощью доставки потоковой передачи по требованию и оптимизированных потоков.</span><span class="sxs-lookup"><span data-stu-id="3620d-524">You can also increase the number of clients a streaming server can support by using on-demand streaming delivery and stream optimized packages.</span></span>

## <span data-ttu-id="3620d-525">Объединение ролей сервера App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="3620d-525">Combining App-V 5.1 Server Roles</span></span>


<span data-ttu-id="3620d-526">Скидка на масштабирование и отказоустойчивость, минимальное количество серверов, необходимое для расположения с подключением к службе каталогов Active Directory, — это один из них.</span><span class="sxs-lookup"><span data-stu-id="3620d-526">Discounting scaling and fault-tolerance requirements, the minimum number of servers needed for a location with connectivity to Active Directory is one.</span></span> <span data-ttu-id="3620d-527">На этом сервере будут размещены сервер управления, служба сервера управления и роли Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3620d-527">This server will host the management server, management server service, and Microsoft SQL Server roles.</span></span> <span data-ttu-id="3620d-528">Таким образом, роли сервера можно упорядочить по любой нужной комбинации, так как они не конфликтуют друг с другом.</span><span class="sxs-lookup"><span data-stu-id="3620d-528">Server roles, therefore, can be arranged in any desired combination since they do not conflict with one another.</span></span>

<span data-ttu-id="3620d-529">Игнорируя требования масштабирования, минимальное количество серверов, необходимых для обеспечения отказоустойчивой реализации, — четыре.</span><span class="sxs-lookup"><span data-stu-id="3620d-529">Ignoring scaling requirements, the minimum number of servers necessary to provide a fault-tolerant implementation is four.</span></span> <span data-ttu-id="3620d-530">Сервер управления и поддержка ролей Microsoft SQL Server размещаются в отказоустойчивых конфигурациях.</span><span class="sxs-lookup"><span data-stu-id="3620d-530">The management server, and Microsoft SQL Server roles support being placed in fault-tolerant configurations.</span></span> <span data-ttu-id="3620d-531">Службу сервера управления можно объединить с любой из ролей, но при этом останется единственная точка сбоя.</span><span class="sxs-lookup"><span data-stu-id="3620d-531">The management server service can be combined with any of the roles, but remains a single point of failure.</span></span>

<span data-ttu-id="3620d-532">Несмотря на то, что существует ряд стратегий и технологий отказоустойчивости, не все применимы к данной службе.</span><span class="sxs-lookup"><span data-stu-id="3620d-532">Although there are a number of fault-tolerance strategies and technologies available, not all are applicable to a given service.</span></span> <span data-ttu-id="3620d-533">Кроме того, если роли App-V 5,1 объединены, некоторые параметры отказоустойчивости могут больше не применяться из-за несовместимости.</span><span class="sxs-lookup"><span data-stu-id="3620d-533">Additionally, if App-V 5.1 roles are combined, certain fault-tolerance options may no longer apply due to incompatibilities.</span></span>






## <span data-ttu-id="3620d-534">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3620d-534">Related topics</span></span>


[<span data-ttu-id="3620d-535">Поддерживаемые конфигурации в App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="3620d-535">App-V 5.1 Supported Configurations</span></span>](app-v-51-supported-configurations.md)

[<span data-ttu-id="3620d-536">Планирование высокого уровня доступности в App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="3620d-536">Planning for High Availability with App-V 5.1</span></span>](planning-for-high-availability-with-app-v-51.md)

[<span data-ttu-id="3620d-537">Планирование развертывания App-V</span><span class="sxs-lookup"><span data-stu-id="3620d-537">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





