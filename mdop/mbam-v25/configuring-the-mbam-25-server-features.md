---
title: Настройка компонентов сервера MBAM 2.5 Server
description: Настройка компонентов сервера MBAM 2.5 Server
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823059"
---
# <span data-ttu-id="33b8c-103">Настройка компонентов сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="33b8c-103">Configuring the MBAM 2.5 Server Features</span></span>


<span data-ttu-id="33b8c-104">Используйте эти сведения в качестве начального места для настройки функций администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5 после [установки серверного программного обеспечения MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="33b8c-104">Use this information as a starting place for configuring Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server features after [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span> <span data-ttu-id="33b8c-105">Для настройки MBAM можно использовать два способа:</span><span class="sxs-lookup"><span data-stu-id="33b8c-105">There are two methods you can use to configure MBAM:</span></span>

-   <span data-ttu-id="33b8c-106">Мастер настройки сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="33b8c-106">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="33b8c-107">Командлеты Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="33b8c-107">Windows PowerShell cmdlets</span></span>

## <span data-ttu-id="33b8c-108">Прежде чем приступить к настройке функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="33b8c-108">Before you start configuring MBAM Server features</span></span>


<span data-ttu-id="33b8c-109">Прежде чем приступить к настройке функций сервера MBAM, ознакомьтесь с приведенными ниже инструкциями и выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="33b8c-109">Review and complete the following steps before you start configuring the MBAM Server features:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="33b8c-110">Шаг</span><span class="sxs-lookup"><span data-stu-id="33b8c-110">Step</span></span></th>
<th align="left"><span data-ttu-id="33b8c-111">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="33b8c-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33b8c-112">Изучите рекомендованную архитектуру для MBAM.</span><span class="sxs-lookup"><span data-stu-id="33b8c-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="33b8c-113">Высокоуровневая архитектура для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="33b8c-113">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="33b8c-114">Проверка поддерживаемых конфигураций для MBAM.</span><span class="sxs-lookup"><span data-stu-id="33b8c-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="33b8c-115">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="33b8c-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33b8c-116">Заполните необходимые условия на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="33b8c-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="33b8c-117">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="33b8c-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="33b8c-118">Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="33b8c-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="33b8c-119">Установка программного обеспечения сервера MBAM на каждый сервер, на котором будет настроена функция сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="33b8c-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="33b8c-120">Установка программного обеспечения MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="33b8c-120">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33b8c-121">Ознакомьтесь с требованиями для настройки функций сервера MBAM с помощью Windows PowerShell (если вы используете этот метод для настройки MBAM функций сервера).</span><span class="sxs-lookup"><span data-stu-id="33b8c-121">Review the prerequisites for using Windows PowerShell to configure MBAM Server features (if you are using this method to configure MBAM Server features).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="33b8c-122">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="33b8c-122">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="33b8c-123">Инструкции по настройке функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="33b8c-123">Steps for configuring MBAM Server features</span></span>


<span data-ttu-id="33b8c-124">В каждой строке в следующей таблице описаны возможности, которые будут настраиваться на отдельном сервере в соответствии с рекомендованной [высокоуровневой архитектурой для MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="33b8c-124">Each row in the following table describes the features that you will configure on a separate server, according to the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="33b8c-125">Устанавливаемые компоненты</span><span class="sxs-lookup"><span data-stu-id="33b8c-125">Features to install</span></span></th>
<th align="left"><span data-ttu-id="33b8c-126">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="33b8c-126">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33b8c-127">Настройте базы данных.</span><span class="sxs-lookup"><span data-stu-id="33b8c-127">Configure the databases.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="33b8c-128">Настройка баз данных MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="33b8c-128">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="33b8c-129">Настройте отчеты.</span><span class="sxs-lookup"><span data-stu-id="33b8c-129">Configure the reports.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="33b8c-130">Настройка отчетов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="33b8c-130">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33b8c-131">Настройте веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="33b8c-131">Configure the web applications.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="33b8c-132">Настройка веб-приложений MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="33b8c-132">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="33b8c-133">Настройка интеграции System Center Configuration Manager (если применимо).</span><span class="sxs-lookup"><span data-stu-id="33b8c-133">Configure the System Center Configuration Manager Integration (if applicable).</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="33b8c-134">Настройка интеграции System Center Configuration Manager с MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="33b8c-134">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="33b8c-135">Список событий, посвященных настройке компонентов сервера MBAM, можно найти в разделе [журналы событий сервера](server-event-logs.md).</span><span class="sxs-lookup"><span data-stu-id="33b8c-135">For a list of events about MBAM Server feature configuration, see [Server Event Logs](server-event-logs.md).</span></span>



## <span data-ttu-id="33b8c-136">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="33b8c-136">Related topics</span></span>


<span data-ttu-id="33b8c-137">Настройка компонентов сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="33b8c-137">Configuring the MBAM 2.5 Server Features</span></span>
 

 
## <span data-ttu-id="33b8c-138">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="33b8c-138">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="33b8c-139">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="33b8c-139">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="33b8c-140">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="33b8c-140">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




