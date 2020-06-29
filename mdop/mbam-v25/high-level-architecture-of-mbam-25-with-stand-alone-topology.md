---
title: Высокоуровневая архитектура MBAM 2.5 с изолированной топологией
description: Высокоуровневая архитектура MBAM 2.5 с изолированной топологией
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 75e878e24b4675f2f2f574791d0f06ecadd0196d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826559"
---
# <span data-ttu-id="2d127-103">Высокоуровневая архитектура MBAM 2.5 с изолированной топологией</span><span class="sxs-lookup"><span data-stu-id="2d127-103">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>


<span data-ttu-id="2d127-104">В этом разделе описана Рекомендуемая архитектура развертывания администрирования и мониторинга Microsoft BitLocker (MBAM) с изолированной топологией Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2d127-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Stand-alone topology.</span></span> <span data-ttu-id="2d127-105">В этой топологии MBAM разворачивается как отдельный продукт.</span><span class="sxs-lookup"><span data-stu-id="2d127-105">In this topology, MBAM is deployed as a stand-alone product.</span></span> <span data-ttu-id="2d127-106">Вы также можете развернуть MBAM с топологией интеграции Configuration Manager, которая интегрирует MBAM с помощью Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2d127-106">You can alternatively deploy MBAM with the Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span> <span data-ttu-id="2d127-107">Дополнительные сведения можно найти в разделе [архитектура высокого уровня MBAM 2,5 с топологией интеграции Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="2d127-107">For more information, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="2d127-108">Список поддерживаемых версий программного обеспечения, описанных в этом разделе, можно найти в разделе [Поддерживаемые конфигурации MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="2d127-108">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="2d127-109">**Примечание**  Мы рекомендуем использовать архитектуру единого сервера в тестовых средах.</span><span class="sxs-lookup"><span data-stu-id="2d127-109">**Note** We recommend you use a single-server architecture in test environments only.</span></span>

 

## <span data-ttu-id="2d127-110">Рекомендуемое количество серверов и поддерживаемое количество клиентов</span><span class="sxs-lookup"><span data-stu-id="2d127-110">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="2d127-111">В рабочей среде рекомендовано следующее количество серверов и поддерживаемое число клиентов:</span><span class="sxs-lookup"><span data-stu-id="2d127-111">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2d127-112">Рекомендуемая архитектура в рабочей среде</span><span class="sxs-lookup"><span data-stu-id="2d127-112">Recommended architecture in a production environment</span></span></th>
<th align="left"><span data-ttu-id="2d127-113">Сведения</span><span class="sxs-lookup"><span data-stu-id="2d127-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2d127-114">Количество серверов и других компьютеров</span><span class="sxs-lookup"><span data-stu-id="2d127-114">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d127-115">Два сервера</span><span class="sxs-lookup"><span data-stu-id="2d127-115">Two servers</span></span></p>
<p><span data-ttu-id="2d127-116">Одна рабочая станция</span><span class="sxs-lookup"><span data-stu-id="2d127-116">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2d127-117">Количество поддерживаемых клиентских компьютеров</span><span class="sxs-lookup"><span data-stu-id="2d127-117">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d127-118">500000</span><span class="sxs-lookup"><span data-stu-id="2d127-118">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2d127-119">Рекомендуемая архитектура MBAM высокого уровня с изолированной топологией</span><span class="sxs-lookup"><span data-stu-id="2d127-119">Recommended MBAM high-level architecture with the Stand-alone topology</span></span>


<span data-ttu-id="2d127-120">На приведенной ниже схеме и таблице описана Рекомендуемая архитектура высокого уровня с двумя серверами для MBAM с помощью изолированной топологии.</span><span class="sxs-lookup"><span data-stu-id="2d127-120">The following diagram and table describe the recommended high-level, two-server architecture for MBAM with the Stand-alone topology.</span></span> <span data-ttu-id="2d127-121">Для развертываний с несколькими лесами MBAM требуется одностороннее или двухстороннее доверие.</span><span class="sxs-lookup"><span data-stu-id="2d127-121">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="2d127-122">Односторонние доверительные отношения требуют, чтобы домен сервера доверял домену клиента.</span><span class="sxs-lookup"><span data-stu-id="2d127-122">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2](images/mbam2-5-2servers.png)

<span data-ttu-id="2d127-124">Возможности сервера для настройки на этом сервере сервер базы данных описаний</span><span class="sxs-lookup"><span data-stu-id="2d127-124">Server Features to configure on this server Description Database server</span></span>

<span data-ttu-id="2d127-125">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="2d127-125">Compliance and Audit Database</span></span>

<span data-ttu-id="2d127-126">Эта функция настраивается на сервере под управлением Windows Server и поддерживаемом экземпляре SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2d127-126">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="2d127-127">**База данных соответствия и аудита** хранит данные о соответствии требованиям, которые используются преимущественно для отчетов, которые размещаются в службах SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="2d127-127">The **Compliance and Audit Database** stores compliance data, which is used primarily for reports that SQL Server Reporting Services hosts.</span></span>

<span data-ttu-id="2d127-128">База данных восстановления</span><span class="sxs-lookup"><span data-stu-id="2d127-128">Recovery Database</span></span>

<span data-ttu-id="2d127-129">Эта функция настраивается на сервере под управлением Windows Server и поддерживаемом экземпляре SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2d127-129">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="2d127-130">В **базе данных восстановления** хранятся данные для восстановления, собранные из клиентских компьютеров MBAM.</span><span class="sxs-lookup"><span data-stu-id="2d127-130">The **Recovery Database** stores recovery data that is collected from MBAM client computers.</span></span>

<span data-ttu-id="2d127-131">Отчеты</span><span class="sxs-lookup"><span data-stu-id="2d127-131">Reports</span></span>

<span data-ttu-id="2d127-132">Эта функция настраивается на сервере под управлением Windows Server и поддерживаемом экземпляре SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2d127-132">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="2d127-133">**Отчеты** содержат сведения о аудите восстановления и состоянии соответствия требованиям для клиентских компьютеров в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="2d127-133">The **Reports** provide recovery audit and compliance status data about the client computers in your enterprise.</span></span> <span data-ttu-id="2d127-134">Вы можете получить доступ к отчетам на веб-сайте администрирования и мониторинга либо прямо из служб SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="2d127-134">You can access the reports from the Administration and Monitoring Website or directly from SQL Server Reporting Services.</span></span>

<span data-ttu-id="2d127-135">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="2d127-135">Administration and Monitoring Server</span></span>

<span data-ttu-id="2d127-136">Веб-сайт администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="2d127-136">Administration and Monitoring Website</span></span>

<span data-ttu-id="2d127-137">Эта функция настраивается на компьютере под управлением Windows Server.</span><span class="sxs-lookup"><span data-stu-id="2d127-137">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="2d127-138">**Веб-сайт администрирования и мониторинга** используется для того, чтобы:</span><span class="sxs-lookup"><span data-stu-id="2d127-138">The **Administration and Monitoring Website** is used to:</span></span>

-   <span data-ttu-id="2d127-139">Помогите конечным пользователям восстановить доступ к своим компьютерам, когда они заблокированы. (Эта область веб-сайта обычно называется службой поддержки).</span><span class="sxs-lookup"><span data-stu-id="2d127-139">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="2d127-140">Просмотр отчетов, в которых отображаются состояние соответствия требованиям и восстановление для клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="2d127-140">View reports that show compliance status and recovery activity for client computers.</span></span>

<span data-ttu-id="2d127-141">Портал самообслуживания</span><span class="sxs-lookup"><span data-stu-id="2d127-141">Self-Service Portal</span></span>

<span data-ttu-id="2d127-142">Эта функция настраивается на компьютере под управлением Windows Server.</span><span class="sxs-lookup"><span data-stu-id="2d127-142">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="2d127-143">**Портал самообслуживания** — это веб-сайт, который позволяет конечным пользователям на клиентских компьютерах независимо входить на веб-сайт, чтобы получить ключ восстановления, если он теряет или забывает пароль BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2d127-143">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

<span data-ttu-id="2d127-144">Наблюдение за веб-службами для этого веб-сайта</span><span class="sxs-lookup"><span data-stu-id="2d127-144">Monitoring web services for this website</span></span>

<span data-ttu-id="2d127-145">Эта функция настраивается на компьютере под управлением Windows Server.</span><span class="sxs-lookup"><span data-stu-id="2d127-145">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="2d127-146">**Веб-службы мониторинга** используются клиентом MBAM и веб-сайтами для связи с базой данных.</span><span class="sxs-lookup"><span data-stu-id="2d127-146">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

<span data-ttu-id="2d127-147">**Важно!**  Веб-служба мониторинга больше не доступна в администрировании и мониторинге Microsoft BitLocker (MBAM) 2,5 с пакетом обновления 1 (SP1), поскольку веб-сайты MBAM взаимодействуют непосредственно с базой данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="2d127-147">**Important** The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span>

 

<span data-ttu-id="2d127-148">Рабочая станция для управления</span><span class="sxs-lookup"><span data-stu-id="2d127-148">Management workstation</span></span>

<span data-ttu-id="2d127-149">Шаблоны групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="2d127-149">MBAM Group Policy Templates</span></span>

-   <span data-ttu-id="2d127-150">Шаблоны групповой политики MBAM — это параметры, определяющие параметры реализации MBAM, позволяющие управлять шифрованием диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2d127-150">The MBAM Group Policy Templates are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker Drive Encryption.</span></span>

-   <span data-ttu-id="2d127-151">Перед запуском MBAM необходимо скачать шаблоны групповой политики, [чтобы получить шаблоны групповой политики MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393941) и скопировать их на сервер или рабочую станцию, на которой работает поддерживаемая операционная система Windows Server или Windows.</span><span class="sxs-lookup"><span data-stu-id="2d127-151">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

-   <span data-ttu-id="2d127-152">Рабочая станция не должна быть выделенным компьютером.</span><span class="sxs-lookup"><span data-stu-id="2d127-152">The workstation does not have to be a dedicated computer.</span></span>

<span data-ttu-id="2d127-153">Клиентский компьютер MBAM и клиент Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2d127-153">MBAM Client and Configuration Manager client computer</span></span>

<span data-ttu-id="2d127-154">Клиентское программное обеспечение MBAM</span><span class="sxs-lookup"><span data-stu-id="2d127-154">MBAM Client software</span></span>

<span data-ttu-id="2d127-155">Клиент MBAM:</span><span class="sxs-lookup"><span data-stu-id="2d127-155">The MBAM Client:</span></span>

-   <span data-ttu-id="2d127-156">Использование объектов групповой политики для применения шифрования диска BitLocker на клиентских компьютерах в предприятии.</span><span class="sxs-lookup"><span data-stu-id="2d127-156">Uses Group Policy Objects to enforce BitLocker Drive Encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="2d127-157">Собирает ключ восстановления BitLocker для трех типов дисков данных: диски операционной системы, несъемные диски с данными и съемные носители данных (USB).</span><span class="sxs-lookup"><span data-stu-id="2d127-157">Collects the Bitlocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="2d127-158">Собирает сведения о восстановлении и сведения о компьютере для клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="2d127-158">Collects recovery information and computer information about the client computers.</span></span>



## <span data-ttu-id="2d127-159">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2d127-159">Related topics</span></span>


[<span data-ttu-id="2d127-160">Начало работы с MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2d127-160">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="2d127-161">Высокоуровневая архитектура MBAM 2.5 с топологией интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="2d127-161">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span>](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[<span data-ttu-id="2d127-162">Иллюстрированные функции развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2d127-162">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

## <span data-ttu-id="2d127-163">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="2d127-163">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="2d127-164">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="2d127-164">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="2d127-165">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="2d127-165">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





