---
title: Необходимые условия для компонента интеграции диспетчера конфигураций
description: Необходимые условия для компонента интеграции диспетчера конфигураций
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825012"
---
# <span data-ttu-id="4b2bf-103">Необходимые условия для компонента интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="4b2bf-103">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="4b2bf-104">Если вы разворачиваете MBAM с помощью топологии интеграции System Center Configuration Manager, мы рекомендуем использовать архитектуру с тремя серверами, как описано в [высоком уровне архитектуры MBAM 2,5 с топологией интеграции Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="4b2bf-104">If you deploy MBAM with the System Center Configuration Manager Integration topology, we recommend a three-server architecture, as described in [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span> <span data-ttu-id="4b2bf-105">Эта архитектура может поддерживать клиентские компьютеры 500 000.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-105">This architecture can support 500,000 client computers.</span></span>

**<span data-ttu-id="4b2bf-106">Важно.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-106">Important</span></span>**  
<span data-ttu-id="4b2bf-107">Windows To Go не поддерживается при установке топологии интеграции Configuration Manager при использовании Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-107">Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>



## <span data-ttu-id="4b2bf-108">Общие требования для компонента интеграции Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4b2bf-108">General prerequisites for the Configuration Manager Integration feature</span></span>


<span data-ttu-id="4b2bf-109">При установке MBAM с помощью Configuration Manager необходимо добавить в дополнение к предварительным требованиям для изолированной топологии следующие дополнительные требования.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-109">When you install MBAM with Configuration Manager, the following additional prerequisites are required in addition to the prerequisites for the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4b2bf-110">Предварительные</span><span class="sxs-lookup"><span data-stu-id="4b2bf-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="4b2bf-111">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="4b2bf-111">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b2bf-112">Сервер Configuration Manager — это основной сайт в системе Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-112">The Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b2bf-113">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4b2bf-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b2bf-114">Агент клиента инвентаризации оборудования находится на сервере Configuration Manager Server.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-114">The Hardware Inventory Client Agent is on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b2bf-115">Инструкции для System Center 2012 Configuration Manager можно найти <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> в разделе Настройка инвентаризации оборудования в Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="4b2bf-115">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="4b2bf-116">В Configuration Manager 2007 вы можете узнать, <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> как настроить инвентаризацию оборудования для сайта </a> .</span><span class="sxs-lookup"><span data-stu-id="4b2bf-116">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b2bf-117">В зависимости от используемой версии Configuration Manager включена одна из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="4b2bf-117">One of the following is enabled, depending on the version of Configuration Manager that you are using:</span></span></p>
<ul>
<li><p><span data-ttu-id="4b2bf-118">Параметры соответствия требованиям — (System Center 2012 Configuration Manager)</span><span class="sxs-lookup"><span data-stu-id="4b2bf-118">Compliance Settings - (System Center 2012 Configuration Manager)</span></span></p></li>
<li><p><span data-ttu-id="4b2bf-119">Агент клиента управления требуемой конфигурацией (DCM) — (Configuration Manager 2007)</span><span class="sxs-lookup"><span data-stu-id="4b2bf-119">Desired Configuration Management (DCM) Client Agent – (Configuration Manager 2007)</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="4b2bf-120">Сведения о System Center 2012 Configuration Manager можно найти <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> в разделе Настройка параметров соответствия в Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="4b2bf-120">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="4b2bf-121">Сведения о Configuration Manager 2007 можно найти в разделе <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> Свойства агента клиента управления требуемой конфигурацией </a> .</span><span class="sxs-lookup"><span data-stu-id="4b2bf-121">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b2bf-122">Точка служб Reporting Services определена в Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-122">A reporting services point is defined in Configuration Manager.</span></span> <span data-ttu-id="4b2bf-123">Требуется для служб SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="4b2bf-123">Required for SQL Server Reporting Services (SSRS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b2bf-124">Для System Center 2012 Configuration Manager ознакомьтесь с разделами <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> Предварительные требования для создания отчетов в Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="4b2bf-124">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="4b2bf-125">В Configuration Manager 2007 вы узнаете, <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> как создать точку служб Reporting Services для служб отчетов SQL </a> .</span><span class="sxs-lookup"><span data-stu-id="4b2bf-125">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b2bf-126">Для Configuration Manager 2007 требуется Microsoft .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="4b2bf-126">Configuration Manager 2007 requires Microsoft .NET Framework 2.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b2bf-127">Для агента клиента управления требуемой конфигурацией (DCM) в Configuration Manager 2007 требуется платформа .NET Framework 2,0 для создания отчета о соответствии.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-127">The Desired Configuration Management (DCM) Client Agent in Configuration Manager 2007 requires .NET Framework 2.0 to report compliance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4b2bf-128">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-128">Note</span></span></strong><br/><p><span data-ttu-id="4b2bf-129">Установка .NET Framework 3,5 автоматически устанавливает .NET Framework 2,0.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-129">Installing .NET Framework 3.5 automatically installs .NET Framework 2.0.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="4b2bf-130">Необходимые разрешения для установки MBAM с помощью Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4b2bf-130">Required permissions to install MBAM with Configuration Manager</span></span>


<span data-ttu-id="4b2bf-131">Чтобы установить MBAM с помощью Configuration Manager, необходимо обладать правами администратора в Configuration Manager, у которого есть роль безопасности с минимальными разрешениями, указанными в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-131">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="4b2bf-132">Кроме того, для установки сервера MBAM в таблице также выводятся права, выходящие за основные права администратора компьютера.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-132">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

**<span data-ttu-id="4b2bf-133">Разрешения, указанные в приведенной ниже таблице, применимы к обеим версиям Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-133">The permissions in the following table apply to both versions of Configuration Manager.</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4b2bf-134">Разрешения</span><span class="sxs-lookup"><span data-stu-id="4b2bf-134">Permissions</span></span></th>
<th align="left"><span data-ttu-id="4b2bf-135">Компонент сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="4b2bf-135">MBAM Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b2bf-136">Роли сервера входа для экземпляра SQL Server:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="4b2bf-136">SQL Server instance login server roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="4b2bf-137">База данных для восстановления — база данных аудита</span><span class="sxs-lookup"><span data-stu-id="4b2bf-137">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b2bf-138">Права экземпляра служб SSRS:-создание папок — публикация отчетов</span><span class="sxs-lookup"><span data-stu-id="4b2bf-138">SSRS instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="4b2bf-139">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4b2bf-139">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="4b2bf-140">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4b2bf-140">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4b2bf-141">Разрешения</span><span class="sxs-lookup"><span data-stu-id="4b2bf-141">Permissions</span></span></th>
<th align="left"><span data-ttu-id="4b2bf-142">Компонент сервера Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4b2bf-142">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b2bf-143">Права доступа к сайту Configuration Manager:-Read</span><span class="sxs-lookup"><span data-stu-id="4b2bf-143">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b2bf-144">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4b2bf-144">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b2bf-145">Права на сбор Configuration Manager:-создание элементов конфигурации и развертывание</span><span class="sxs-lookup"><span data-stu-id="4b2bf-145">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b2bf-146">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4b2bf-146">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b2bf-147">Разрешения элемента конфигурации Configuration Manager:-Create-Delete-Read</span><span class="sxs-lookup"><span data-stu-id="4b2bf-147">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b2bf-148">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4b2bf-148">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="4b2bf-149">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="4b2bf-149">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4b2bf-150">Разрешения</span><span class="sxs-lookup"><span data-stu-id="4b2bf-150">Permissions</span></span></th>
<th align="left"><span data-ttu-id="4b2bf-151">Компонент сервера Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4b2bf-151">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b2bf-152">Права доступа к сайту Configuration Manager:-Read</span><span class="sxs-lookup"><span data-stu-id="4b2bf-152">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b2bf-153">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4b2bf-153">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b2bf-154">Права на сбор Configuration Manager:-Create-Delete-Read-ReadResource</span><span class="sxs-lookup"><span data-stu-id="4b2bf-154">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b2bf-155">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4b2bf-155">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b2bf-156">Права конфигурации Configuration Manager:-создание-удаление-чтение и распространение</span><span class="sxs-lookup"><span data-stu-id="4b2bf-156">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b2bf-157">Интеграция System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4b2bf-157">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="4b2bf-158">Изменения, необходимые для файлов. mof</span><span class="sxs-lookup"><span data-stu-id="4b2bf-158">Required changes for the .mof files</span></span>


<span data-ttu-id="4b2bf-159">Чтобы клиентские компьютеры могли сообщать о соответствии требованиям BitLocker в отчетах Configuration Manager MBAM, необходимо изменить файл Configuration. mof и SMS \ _def. mof для System Center 2012 Configuration Manager и Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="4b2bf-159">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file and Sms\_def.mof file for System Center 2012 Configuration Manager and Microsoft System Center Configuration Manager 2007.</span></span> <span data-ttu-id="4b2bf-160">Инструкции можно найти [в разделе MBAM 2,5 Server требования, применимые только к топологии интеграции Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="4b2bf-160">For instructions, see [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="4b2bf-161">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4b2bf-161">Related topics</span></span>


[<span data-ttu-id="4b2bf-162">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="4b2bf-162">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[<span data-ttu-id="4b2bf-163">Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="4b2bf-163">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## <span data-ttu-id="4b2bf-164">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="4b2bf-164">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4b2bf-165">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="4b2bf-165">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="4b2bf-166">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4b2bf-166">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





