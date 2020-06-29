---
title: Высокоуровневая архитектура MBAM 2.5 с топологией интеграции диспетчера конфигураций
description: Высокоуровневая архитектура MBAM 2.5 с топологией интеграции диспетчера конфигураций
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: 75af2e22981d76568916c36acadbbb25648b1f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825762"
---
# <span data-ttu-id="d8b2a-103">Архитектура высокого уровня MBAM 2,5 с топологией интеграции Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d8b2a-103">High-level architecture of MBAM 2.5 with Configuration Manager Integration topology</span></span>

<span data-ttu-id="d8b2a-104">В этом разделе описана Рекомендуемая архитектура развертывания администрирования и мониторинга Microsoft BitLocker (MBAM) с топологией интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="d8b2a-105">Эта топология интегрирует MBAM с помощью System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-105">This topology integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="d8b2a-106">Чтобы развернуть MBAM с помощью изолированной топологии, ознакомьтесь с [высокоуровневой архитектурой MBAM 2,5 с изолированной топологией](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span><span class="sxs-lookup"><span data-stu-id="d8b2a-106">To deploy MBAM with the Stand-alone topology, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

<span data-ttu-id="d8b2a-107">Список поддерживаемых версий программного обеспечения, описанных в этом разделе, можно найти в разделе [Поддерживаемые конфигурации MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="d8b2a-107">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="d8b2a-108">**Важно!**  Windows To Go не поддерживается при установке топологии интеграции Configuration Manager при использовании Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-108">**Important** Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="d8b2a-109">Рекомендуемое количество серверов и поддерживаемое количество клиентов</span><span class="sxs-lookup"><span data-stu-id="d8b2a-109">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="d8b2a-110">В рабочей среде рекомендовано следующее количество серверов и поддерживаемое число клиентов:</span><span class="sxs-lookup"><span data-stu-id="d8b2a-110">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d8b2a-111">Рекомендуемая архитектура</span><span class="sxs-lookup"><span data-stu-id="d8b2a-111">Recommended architecture</span></span></th>
<th align="left"><span data-ttu-id="d8b2a-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="d8b2a-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2a-113">Количество серверов и других компьютеров</span><span class="sxs-lookup"><span data-stu-id="d8b2a-113">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2a-114">Три сервера</span><span class="sxs-lookup"><span data-stu-id="d8b2a-114">Three servers</span></span></p>
<p><span data-ttu-id="d8b2a-115">Одна рабочая станция</span><span class="sxs-lookup"><span data-stu-id="d8b2a-115">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d8b2a-116">Количество поддерживаемых клиентских компьютеров</span><span class="sxs-lookup"><span data-stu-id="d8b2a-116">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2a-117">500000</span><span class="sxs-lookup"><span data-stu-id="d8b2a-117">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d8b2a-118">Различия между интеграцией Configuration Manager и изолированными топологиями</span><span class="sxs-lookup"><span data-stu-id="d8b2a-118">Differences between Configuration Manager Integration and stand-alone topologies</span></span>


<span data-ttu-id="d8b2a-119">Основные различия между топологиями:</span><span class="sxs-lookup"><span data-stu-id="d8b2a-119">The main differences between the topologies are:</span></span>

-   <span data-ttu-id="d8b2a-120">Функции соответствия и отчетов удаляются из MBAM и доступны из Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-120">The compliance and reporting features are removed from MBAM and are accessed from Configuration Manager.</span></span>

-   <span data-ttu-id="d8b2a-121">Отчеты просматриваются из консоли управления Configuration Manager, за исключением отчета аудита восстановления, который вы продолжаете просматривать на веб-сайте администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-121">Reports are viewed from the Configuration Manager Management Console, with the exception of the Recovery Audit Report, which you continue to view from the MBAM Administration and Monitoring Website.</span></span>

## <span data-ttu-id="d8b2a-122">Рекомендуемая архитектура MBAM высокого уровня с топологией интеграции Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d8b2a-122">Recommended MBAM high-level architecture with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="d8b2a-123">На приведенной ниже схеме и таблице описана Рекомендуемая архитектура высокого уровня для MBAM с топологией интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-123">The following diagram and table describe the recommended high-level architecture for MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="d8b2a-124">Для развертываний с несколькими лесами MBAM требуется одностороннее или двухстороннее доверие.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-124">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="d8b2a-125">Односторонние доверительные отношения требуют, чтобы домен сервера доверял домену клиента.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-125">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2\-5](images/mbam2-5-cmserver.png)

### <span data-ttu-id="d8b2a-127">Сервер базы данных</span><span class="sxs-lookup"><span data-stu-id="d8b2a-127">Database server</span></span>

#### <span data-ttu-id="d8b2a-128">База данных восстановления</span><span class="sxs-lookup"><span data-stu-id="d8b2a-128">Recovery database</span></span>

<span data-ttu-id="d8b2a-129">Эта функция настраивается на компьютере с операционной системой Windows Server и поддерживаемым экземпляром SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-129">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="d8b2a-130">В **базе данных восстановления** хранятся данные для восстановления, собранные из клиентских компьютеров MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-130">The **Recovery Database** stores recovery data that is collected from MBAM Client computers.</span></span>

#### <span data-ttu-id="d8b2a-131">База данных аудита</span><span class="sxs-lookup"><span data-stu-id="d8b2a-131">Audit database</span></span>

<span data-ttu-id="d8b2a-132">Эта функция настраивается на компьютере с операционной системой Windows Server и поддерживаемым экземпляром SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-132">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="d8b2a-133">**База данных аудита** хранит данные об активности аудита, полученные с клиентских компьютеров, которые получили доступ к данным для восстановления.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-133">The **Audit Database** stores audit activity data that is collected from client computers that have accessed recovery data.</span></span>

#### <span data-ttu-id="d8b2a-134">Отчеты</span><span class="sxs-lookup"><span data-stu-id="d8b2a-134">Reports</span></span>

<span data-ttu-id="d8b2a-135">Эта функция настраивается на компьютере с операционной системой Windows Server и поддерживаемым экземпляром SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-135">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="d8b2a-136">**Отчеты** предоставляют данные аудита восстановления для клиентских компьютеров предприятия.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-136">The **Reports** provide recovery audit data for the client computers in your enterprise.</span></span> <span data-ttu-id="d8b2a-137">Вы можете просматривать отчеты на консоли Configuration Manager или прямо из служб SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-137">You can view reports from the Configuration Manager console or directly from SQL Server Reporting Services.</span></span>

### <span data-ttu-id="d8b2a-138">Сервер основного сайта Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d8b2a-138">Configuration Manager primary site server</span></span>

<span data-ttu-id="d8b2a-139">Компонент интеграции System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d8b2a-139">System Center Configuration Manager Integration feature</span></span>

-   <span data-ttu-id="d8b2a-140">Эта функция настраивается на сервере основного сайта Configuration Manager, который является сервером верхнего уровня в инфраструктуре Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-140">This feature is configured on the Configuration Manager Primary Site Server, which is the top-tier server in your Configuration Manager infrastructure.</span></span>

-   <span data-ttu-id="d8b2a-141">**Сервер Configuration Manager** собирает данные инвентаризации оборудования с клиентских компьютеров и использует ее для создания отчета о соответствии требованиям BitLocker для клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-141">The **Configuration Manager Server** collects the hardware inventory information from client computers and is used to report BitLocker compliance of client computers.</span></span>

-   <span data-ttu-id="d8b2a-142">При запуске мастера настройки администрирования и мониторинга Microsoft BitLocker для установки серверного программного обеспечения, семейство MBAM поддерживаемых компьютеров, шаблон базовой конфигурации и отчеты настраиваются на сервере основного сайта Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-142">When you run the Microsoft BitLocker Administration and Monitoring Setup wizard to install the server software, the MBAM Supported Computers collection, configuration baseline, and reports are configured on the Configuration Manager Primary Site Server.</span></span>

-   <span data-ttu-id="d8b2a-143">**Консоль Configuration Manager** должна быть установлена на том же компьютере, на котором вы установили программное обеспечение сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-143">The **Configuration Manager console** must be installed on the same computer on which you install the MBAM Server software.</span></span>

### <span data-ttu-id="d8b2a-144">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="d8b2a-144">Administration and monitoring server</span></span>

#### <span data-ttu-id="d8b2a-145">Веб-сайт администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="d8b2a-145">Administration and monitoring website</span></span>

<span data-ttu-id="d8b2a-146">Эта функция настраивается на компьютере под управлением Windows Server.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-146">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="d8b2a-147">**Веб-сайт администрирования и мониторинга** используется для того, чтобы:</span><span class="sxs-lookup"><span data-stu-id="d8b2a-147">The **Administration and monitoring website** is used to:</span></span>

-   <span data-ttu-id="d8b2a-148">Помогите конечным пользователям восстановить доступ к своим компьютерам, когда они заблокированы. (Эта область веб-сайта обычно называется службой поддержки).</span><span class="sxs-lookup"><span data-stu-id="d8b2a-148">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="d8b2a-149">Просмотр отчета аудита восстановления, который показывает активность восстановления для клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-149">View the Recovery Audit Report, which shows recovery activity for client computers.</span></span> <span data-ttu-id="d8b2a-150">Другие отчеты можно просмотреть на консоли Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-150">Other reports are viewed from the Configuration Manager console.</span></span>

#### <span data-ttu-id="d8b2a-151">Портал самообслуживания</span><span class="sxs-lookup"><span data-stu-id="d8b2a-151">Self-service portal</span></span>

<span data-ttu-id="d8b2a-152">Эта функция настраивается на компьютере под управлением Windows Server.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-152">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="d8b2a-153">**Портал самообслуживания** — это веб-сайт, который позволяет конечным пользователям на клиентских компьютерах независимо входить на веб-сайт, чтобы получить ключ восстановления, если он теряет или забывает пароль BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-153">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

#### <span data-ttu-id="d8b2a-154">Наблюдение за веб-службами для этого веб-сайта</span><span class="sxs-lookup"><span data-stu-id="d8b2a-154">Monitoring web services for this website</span></span>

<span data-ttu-id="d8b2a-155">Этот компонент установлен на компьютере под управлением Windows Server.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-155">This feature is installed on a computer running Windows Server.</span></span>

<span data-ttu-id="d8b2a-156">**Веб-службы мониторинга** используются клиентом MBAM и веб-сайтами для связи с базой данных.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-156">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

**<span data-ttu-id="d8b2a-157">Важно.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-157">Important</span></span>**<br><span data-ttu-id="d8b2a-158">Веб-служба мониторинга больше не доступна в администрировании и мониторинге Microsoft BitLocker (MBAM) 2,5 с пакетом обновления 1 (SP1), поскольку веб-сайты MBAM взаимодействуют непосредственно с базой данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-158">The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span> 

 

### <span data-ttu-id="d8b2a-159">Рабочая станция для управления</span><span class="sxs-lookup"><span data-stu-id="d8b2a-159">Management workstation</span></span>

#### <span data-ttu-id="d8b2a-160">Шаблоны групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="d8b2a-160">MBAM group policy templates</span></span>

-   <span data-ttu-id="d8b2a-161">**Шаблоны групповой политики MBAM** — это параметры, определяющие параметры реализации MBAM, позволяющие управлять шифрованием диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-161">The **MBAM Group Policy Templates** are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker drive encryption.</span></span>

-   <span data-ttu-id="d8b2a-162">Перед запуском MBAM необходимо скачать шаблоны групповой политики, [чтобы получить шаблоны групповой политики MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393941) и скопировать их на сервер или рабочую станцию, на которой работает поддерживаемая операционная система Windows Server или Windows.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-162">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

    **<span data-ttu-id="d8b2a-163">ПРИМЕЧАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8b2a-163">NOTE</span></span>**<br><span data-ttu-id="d8b2a-164">Рабочая станция не должна быть выделенным компьютером.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-164">The workstation does not have to be a dedicated computer.</span></span>

     

### <span data-ttu-id="d8b2a-165">Клиентский компьютер MBAM и клиент Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d8b2a-165">MBAM Client and Configuration Manager Client computer</span></span>

#### <span data-ttu-id="d8b2a-166">Клиентское программное обеспечение MBAM</span><span class="sxs-lookup"><span data-stu-id="d8b2a-166">MBAM Client software</span></span>

<span data-ttu-id="d8b2a-167">**Клиент MBAM**:</span><span class="sxs-lookup"><span data-stu-id="d8b2a-167">The **MBAM Client**:</span></span>

-   <span data-ttu-id="d8b2a-168">Использование объектов групповой политики для применения шифрования диска BitLocker на клиентских компьютерах в предприятии.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-168">Uses Group Policy Objects to enforce BitLocker drive encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="d8b2a-169">Собирает ключ восстановления BitLocker для трех типов дисков данных: диски операционной системы, несъемные диски с данными и съемные носители данных (USB).</span><span class="sxs-lookup"><span data-stu-id="d8b2a-169">Collects the BitLocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="d8b2a-170">Собирает сведения о восстановлении и сведения о компьютере для клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-170">Collects recovery information and computer information about the client computers.</span></span>

#### <span data-ttu-id="d8b2a-171">Клиент Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d8b2a-171">Configuration Manager Client</span></span>

<span data-ttu-id="d8b2a-172">**Клиент Configuration Manager** позволяет Configuration Manager собирать данные о совместимости оборудования с клиентскими компьютерами и сообщать о соответствии требованиям.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-172">The **Configuration Manager Client** enables Configuration Manager to collect hardware compatibility data about the client computers and report compliance information.</span></span>

 

## <span data-ttu-id="d8b2a-173">Отличия в развертывании MBAM для поддерживаемых версий Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d8b2a-173">Differences in MBAM deployment for supported Configuration Manager versions</span></span>


<span data-ttu-id="d8b2a-174">При развертывании MBAM с топологией интеграции Configuration Manager вы можете установить MBAM на основном сервере сайта.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-174">When you deploy MBAM with the Configuration Manager Integration topology, you can install MBAM on a primary site server.</span></span> <span data-ttu-id="d8b2a-175">Тем не менее, установка MBAM работает не так, как в диспетчере конфигураций системы Center2012 Configuration Manager и Configuration Manager2007.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-175">However, the MBAM installation works differently for System Center2012 Configuration Manager and Configuration Manager2007.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d8b2a-176">Версия Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d8b2a-176">Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="d8b2a-177">Описание</span><span class="sxs-lookup"><span data-stu-id="d8b2a-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2a-178">Configuration Manager System Center2012 R2</span><span class="sxs-lookup"><span data-stu-id="d8b2a-178">System Center2012 R2 Configuration Manager</span></span></p>
<p><span data-ttu-id="d8b2a-179">Системный Center2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d8b2a-179">System Center2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2a-180">Если вы установили MBAM на основном сервере сайта или на сервере центра администрирования, MBAM выполняет все действия по установке на сервере сайта.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-180">If you install MBAM on a primary site server or on a central administration server, MBAM performs all of the installation actions on that site server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d8b2a-181">Configuration Manager2007 R2</span><span class="sxs-lookup"><span data-stu-id="d8b2a-181">Configuration Manager2007 R2</span></span></p>
<p><span data-ttu-id="d8b2a-182">Manager2007 конфигурации</span><span class="sxs-lookup"><span data-stu-id="d8b2a-182">Configuration Manager2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2a-183">Если вы установили MBAM на сервере первичного сайта, который является частью более крупной иерархии Configuration Manager с родительским сервером центрального сайта, MBAM определяет родительский сервер центрального сайта и выполняет все действия по установке на этом родительском сервере.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-183">If you install MBAM on a primary site server that is part of a larger Configuration Manager hierarchy with a central site parent server, MBAM identifies the central site parent server and performs all of the installation actions on that parent server.</span></span> <span data-ttu-id="d8b2a-184">Установка включает проверку предварительных требований и установку объектов и отчетов Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-184">The installation includes checking prerequisites and installing the Configuration Manager objects and reports.</span></span></p>
<p><span data-ttu-id="d8b2a-185">Например, если вы установили MBAM на основном сервере сайта, который является дочерним для основного сервера сайта, MBAM устанавливает все объекты и отчеты Configuration Manager на родительский сервер.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-185">For example, if you install MBAM on a primary site server that is a child of a central site parent server, MBAM installs all of the Configuration Manager objects and reports on the parent server.</span></span> <span data-ttu-id="d8b2a-186">Если вы установили MBAM на родительский сервер, MBAM выполняет все действия по установке на этом родительском сервере.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-186">If you install MBAM on the parent server, MBAM performs all of the installation actions on that parent server.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d8b2a-187">Как MBAM работает в Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d8b2a-187">How MBAM works with Configuration Manager</span></span>


<span data-ttu-id="d8b2a-188">Интеграция MBAM с Configuration Manager основывается на пакете конфигурации, который устанавливает элементы, описанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-188">The integration of MBAM with Configuration Manager is based on a configuration pack that installs the items described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d8b2a-189">Элементы, установленные в Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d8b2a-189">Items installed into Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="d8b2a-190">Описание</span><span class="sxs-lookup"><span data-stu-id="d8b2a-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2a-191">Данные конфигурации</span><span class="sxs-lookup"><span data-stu-id="d8b2a-191">Configuration data</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2a-192">Данные конфигурации устанавливают шаблон базовой конфигурации с именем "Защита BitLocker", который содержит два элемента конфигурации:</span><span class="sxs-lookup"><span data-stu-id="d8b2a-192">The configuration data installs a configuration baseline, called “BitLocker Protection,” which contains two configuration items:</span></span></p>
<ul>
<li><p><span data-ttu-id="d8b2a-193">Защита диска операционной системы BitLocker</span><span class="sxs-lookup"><span data-stu-id="d8b2a-193">BitLocker Operating System Drive Protection</span></span></p></li>
<li><p><span data-ttu-id="d8b2a-194">Защита фиксированных дисков с данными BitLocker</span><span class="sxs-lookup"><span data-stu-id="d8b2a-194">BitLocker Fixed Data Drives Protection</span></span></p></li>
</ul>
<p><span data-ttu-id="d8b2a-195">Шаблон базовой конфигурации развертывается в семействе компьютеров, поддерживаемых MBAM, который также создается при установке MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-195">The configuration baseline is deployed to the MBAM Supported Computers collection, which is also created when MBAM is installed.</span></span></p>
<p><span data-ttu-id="d8b2a-196">Два элемента конфигурации предоставляют основу для оценки состояния соответствия требованиям клиентских компьютеров.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-196">The two configuration items provide the basis for evaluating the compliance status of the client computers.</span></span> <span data-ttu-id="d8b2a-197">Эти данные записываются, сохраняются и оцениваются в Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-197">This information is captured, stored, and evaluated in Configuration Manager.</span></span></p>
<p><span data-ttu-id="d8b2a-198">Элементы конфигурации основываются на требованиях к соответствию для дисков операционной системы и несъемных дисков с данными.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-198">The configuration items are based on the compliance requirements for operating system drives and fixed data drives.</span></span> <span data-ttu-id="d8b2a-199">Данные, необходимые для развернутых компьютеров, собираются таким образом, чтобы можно было оценивать соответствие для этих типов устройств.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-199">The required details for the deployed computers are collected so that the compliance for those drive types can be evaluated.</span></span></p>
<p><span data-ttu-id="d8b2a-200">По умолчанию шаблон базовой конфигурации оценивает состояние соответствия требованиям every12 часов и отправляет данные о соответствии в Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-200">By default, the configuration baseline evaluates the compliance status every12 hours and sends the compliance data to Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d8b2a-201">Семейство поддерживаемых компьютеров MBAM</span><span class="sxs-lookup"><span data-stu-id="d8b2a-201">MBAM Supported Computers collection</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2a-202">MBAM создает коллекцию, которая называется MBAM поддерживаемые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-202">MBAM creates a collection that is called MBAM Supported Computers.</span></span> <span data-ttu-id="d8b2a-203">Шаблон базовой конфигурации предназначен для клиентских компьютеров, которые находятся в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-203">The configuration baseline is targeted to client computers that are in this collection.</span></span></p>
<p><span data-ttu-id="d8b2a-204">Это динамическая коллекция.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-204">This is a dynamic collection.</span></span> <span data-ttu-id="d8b2a-205">По умолчанию он запускает every12ные часы и оценивает членство, основываясь на трех критериях:</span><span class="sxs-lookup"><span data-stu-id="d8b2a-205">By default, it runs every12 hours and evaluates membership, based on three criteria:</span></span></p>
<ul>
<li><p><span data-ttu-id="d8b2a-206">Компьютер является поддерживаемой версией операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-206">The computer is a supported version of the Windows operating system.</span></span></p></li>
<li><p><span data-ttu-id="d8b2a-207">Компьютер является физическим компьютером.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-207">The computer is a physical computer.</span></span> <span data-ttu-id="d8b2a-208">Виртуальные машины не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-208">Virtual machines are not supported.</span></span></p></li>
<li><p><span data-ttu-id="d8b2a-209">На компьютере установлен доверенный платформенный модуль (TPM).</span><span class="sxs-lookup"><span data-stu-id="d8b2a-209">The computer has a Trusted Platform Module (TPM) that is available.</span></span> <span data-ttu-id="d8b2a-210">Для Windows7 требуется совместимая версия доверенного платформенного модуля (TPM 1.2 или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="d8b2a-210">A compatible version of TPM1.2 or later is required for Windows7.</span></span> <span data-ttu-id="d8b2a-211">В Windows10, Windows 8.1, Windows8 и Windows To Go не требуется доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-211">Windows10, Windows8.1, Windows8, and Windows To Go do not require a TPM.</span></span></p></li>
</ul>
<p><span data-ttu-id="d8b2a-212">Коллекция оценивается на всех компьютерах, и создается подмножество совместимых компьютеров, что обеспечивает основу для оценки соответствия требованиям и создания отчетов для интеграции MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-212">The collection is evaluated against all computers and a subset of compatible computers is created, which provides the basis for compliance evaluation and reporting for the MBAM integration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2a-213">Отчеты</span><span class="sxs-lookup"><span data-stu-id="d8b2a-213">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2a-214">Когда вы настраиваете MBAM с помощью топологии интеграции Configuration Manager, вы сможете просматривать отчеты в Configuration Manager, кроме отчета аудита восстановления, последнюю из которых вы продолжаете просматривать на веб-сайте администрирования MBAM и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-214">When you configure MBAM with the Configuration Manager Integration topology, you view all reports in Configuration Manager, except the Recovery Audit Report, the latter of which you continue to view in the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="d8b2a-215">Ниже указаны отчеты, доступные в диспетчере конфигураций.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-215">The reports available in Configuration Manager are:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d8b2a-216">Отчет</span><span class="sxs-lookup"><span data-stu-id="d8b2a-216">Report</span></span></th>
<th align="left"><span data-ttu-id="d8b2a-217">Описание</span><span class="sxs-lookup"><span data-stu-id="d8b2a-217">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2a-218">Панель мониторинга соответствия требованиям для предприятия BitLocker</span><span class="sxs-lookup"><span data-stu-id="d8b2a-218">BitLocker Enterprise Compliance Dashboard</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2a-219">Предоставляет ИТ-администраторам три вида данных в одном отчете: распространение состояния соответствия требованиям, несоответствующие требованиям, распространение ошибок и распространение состояния соответствия по типу диска.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-219">Gives IT administrators three views of information in a single report: Compliance Status Distribution, Non Compliant – Errors Distribution, and Compliance Status Distribution By Drive Type.</span></span> <span data-ttu-id="d8b2a-220">Параметры детализации в отчете позволяют ИТ-администраторам щелкать данные и просматривать список компьютеров, которые соответствуют выбранному состоянию.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-220">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d8b2a-221">Сведения о соответствии требованиям BitLocker для предприятий</span><span class="sxs-lookup"><span data-stu-id="d8b2a-221">BitLocker Enterprise Compliance Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2a-222">Позволяет администраторам ИТ просматривать сведения о состоянии соответствия требованиям шифрования BitLocker для предприятия и включают состояние соответствия для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-222">Lets IT administrators view information about the BitLocker encryption compliance status of the enterprise and includes the compliance status for each computer.</span></span> <span data-ttu-id="d8b2a-223">Параметры детализации в отчете позволяют ИТ-администраторам щелкать данные и просматривать список компьютеров, которые соответствуют выбранному состоянию.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-223">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d8b2a-224">Соответствие требованиям компьютера BitLocker</span><span class="sxs-lookup"><span data-stu-id="d8b2a-224">BitLocker Computer Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2a-225">Позволяет ИТ-администраторам просматривать отдельный компьютер и определять причины, по которым он был признан совместимым или несовместимым.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-225">Lets IT administrators view an individual computer and determine why it was reported with a status of compliant or not compliant.</span></span> <span data-ttu-id="d8b2a-226">В отчете также отображается состояние шифрования дисков операционной системы и несъемных дисков с данными.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-226">The report also displays the encryption state of the operating system drives and fixed data drives.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d8b2a-227">Сводка по соответствию требованиям для предприятий BitLocker</span><span class="sxs-lookup"><span data-stu-id="d8b2a-227">BitLocker Enterprise Compliance Summary</span></span></p></td>
<td align="left"><p><span data-ttu-id="d8b2a-228">Позволяет администраторам ИТ просматривать состояние соответствия политике MBAM в предприятии.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-228">Lets IT administrators view the status of MBAM policy compliance in the enterprise.</span></span> <span data-ttu-id="d8b2a-229">Оценивается состояние каждого компьютера, и в отчете показана сводка соответствия требованиям для всех компьютеров в Организации.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-229">Each computer’s state is evaluated, and the report shows a summary of the compliance of all computers in the enterprise against the policy.</span></span> <span data-ttu-id="d8b2a-230">Параметры детализации в отчете позволяют ИТ-администраторам щелкать данные и просматривать список компьютеров, которые соответствуют выбранному состоянию.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-230">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="d8b2a-231">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d8b2a-231">Related topics</span></span>


[<span data-ttu-id="d8b2a-232">Начало работы с MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8b2a-232">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="d8b2a-233">Высокоуровневая архитектура MBAM 2.5 с изолированной топологией</span><span class="sxs-lookup"><span data-stu-id="d8b2a-233">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[<span data-ttu-id="d8b2a-234">Иллюстрированные функции развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8b2a-234">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## <span data-ttu-id="d8b2a-235">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="d8b2a-235">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d8b2a-236">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="d8b2a-236">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="d8b2a-237">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="d8b2a-237">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




