---
title: Обновление выпуска обновления для MBAM 2,5 до MBAM 2,5 SP1
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812768"
---
# <span data-ttu-id="4e6e7-102">Переход с MBAM 2,5 на MBAM 2,5 SP1 обслуживание выпуск обновление</span><span class="sxs-lookup"><span data-stu-id="4e6e7-102">Upgrade from MBAM 2.5 to MBAM 2.5 SP1 Servicing Release Update</span></span>

<span data-ttu-id="4e6e7-103">В этой статье приведены пошаговые инструкции по обновлению администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5 для MBAM 2,5 с пакетом обновления 1 (SP1), а также [пакетом Microsoft Desktop Optimization (MDOP) может 2019 обновление обслуживания](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) в автономной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-103">This article provides step-by-step instructions to upgrade Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 to MBAM 2.5 Service Pack 1 (SP1) together with the [Microsoft Desktop Optimization Pack (MDOP) May 2019 servicing update](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) in a standalone configuration.</span></span>

<span data-ttu-id="4e6e7-104">В этом руководстве мы будем использовать конфигурацию с двумя серверами.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-104">In this guide, we will use a two-server configuration.</span></span> <span data-ttu-id="4e6e7-105">Один сервер является сервером баз данных, на котором работает Microsoft SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-105">One server will be a database server that's running Microsoft SQL Server 2016.</span></span> <span data-ttu-id="4e6e7-106">На этом сервере будут размещены базы данных и отчеты MBAM.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-106">This server will host the MBAM databases and reports.</span></span> <span data-ttu-id="4e6e7-107">Другой сервер будет веб-сервером Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-107">The other server will be a Windows Server 2012 R2 web server.</span></span> <span data-ttu-id="4e6e7-108">Этот сервер будет размещать "Администрирование и мониторинг" и "Портал самообслуживания".</span><span class="sxs-lookup"><span data-stu-id="4e6e7-108">This server will host "Administration and Monitoring" and "Self-Service Portal."</span></span>

## <span data-ttu-id="4e6e7-109">Подготовка к обновлению MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="4e6e7-109">Prepare to upgrade MBAM 2.5 SP1</span></span>

### <span data-ttu-id="4e6e7-110">Знакомство с серверами MBAM в вашей среде</span><span class="sxs-lookup"><span data-stu-id="4e6e7-110">Know the MBAM servers in your environment</span></span>

1. <span data-ttu-id="4e6e7-111">Ядро СУБД SQL Server: сервер, на котором размещены базы данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-111">SQL Server Database Engine: Server that hosts the MBAM databases.</span></span>
2. <span data-ttu-id="4e6e7-112">Службы SQL Server Reporting Services: сервер, на котором размещаются отчеты MBAM.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-112">SQL Server Reporting Services: Server that hosts the MBAM reports.</span></span>
3. <span data-ttu-id="4e6e7-113">Веб-серверы служб IIS: сервер, на котором размещены веб-приложения MBAM и службы MBAM.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-113">Internet Information Services (IIS) web servers: Server that hosts MBAM Web Applications and MBAM services.</span></span>
4. <span data-ttu-id="4e6e7-114">Необязательно Сервер основного сайта Microsoft System Center Configuration Manager: приложение конфигурации MBAM запущено на этом сервере для интеграции MBAM отчетов с Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-114">(Optional) Microsoft System Center Configuration Manager primary site server: The MBAM configuration application is run on this server to integrate MBAM reports with Configuration Manager.</span></span> <span data-ttu-id="4e6e7-115">Эти отчеты затем объединяются с существующими отчетами Configuration Manager в экземпляре служб SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="4e6e7-115">These reports are then merged with existing Configuration Manager reports on the Configuration Manager SQL Server Reporting Services (SSRS) instance.</span></span>

### <span data-ttu-id="4e6e7-116">Определение учетных записей служб, групп, имени сервера и URL-адреса отчетов</span><span class="sxs-lookup"><span data-stu-id="4e6e7-116">Identify service accounts, groups, server name, and reports URL</span></span>

1. <span data-ttu-id="4e6e7-117">Укажите учетную запись службы пула приложений MBAM, которая используется веб-серверами IIS для чтения и записи данных в MBAM базах данных.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-117">Identify the MBAM application pool service account that's used by IIS web servers to read and write data to MBAM databases.</span></span>
2. <span data-ttu-id="4e6e7-118">Определите группы, которые используются при настройке веб-компонентов MBAM и URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-118">Identify the groups that are used during the MBAM web features configuration and the reports web service URL.</span></span>
3. <span data-ttu-id="4e6e7-119">Определение имени сервера SQL Server и имени экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-119">Identify the SQL Server name and instance name.</span></span> <span data-ttu-id="4e6e7-120">Просмотрите это видео, чтобы узнать больше.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-120">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. <span data-ttu-id="4e6e7-121">Укажите учетную запись служб SQL Server Reporting Services, которая используется для чтения данных соответствия в базе данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-121">Identify the SQL Server Reporting Services Account that's used for reading compliance data from the Compliance and Audit database.</span></span> <span data-ttu-id="4e6e7-122">Просмотрите это видео, чтобы узнать больше.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-122">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## <span data-ttu-id="4e6e7-123">Обновление инфраструктуры MBAM до последней доступной версии</span><span class="sxs-lookup"><span data-stu-id="4e6e7-123">Upgrade the MBAM infrastructure to the latest version available</span></span>

<span data-ttu-id="4e6e7-124">Установка или обновление инфраструктуры сервера MBAM всегда выполняется в указанном ниже порядке:</span><span class="sxs-lookup"><span data-stu-id="4e6e7-124">MBAM Server infrastructure installation or upgrade is always performed in the order listed below:</span></span>

- <span data-ttu-id="4e6e7-125">Ядро СУБД SQL Server: базы данных</span><span class="sxs-lookup"><span data-stu-id="4e6e7-125">SQL Server Database Engine: Databases</span></span>
- <span data-ttu-id="4e6e7-126">Службы SQL Server Reporting Services: отчеты</span><span class="sxs-lookup"><span data-stu-id="4e6e7-126">SQL Server Reporting Services: Reports</span></span>
- <span data-ttu-id="4e6e7-127">Веб-сервер: веб-приложения</span><span class="sxs-lookup"><span data-stu-id="4e6e7-127">Web Server: Web Applications</span></span>
- <span data-ttu-id="4e6e7-128">Сервер SCCM: интегрированные отчеты SCCM (если применимо)</span><span class="sxs-lookup"><span data-stu-id="4e6e7-128">SCCM Server: SCCM Integrated Reports if applicable</span></span>
- <span data-ttu-id="4e6e7-129">Клиенты: агент MBAM или клиентское обновление</span><span class="sxs-lookup"><span data-stu-id="4e6e7-129">Clients: MBAM Agent or Client Update</span></span>
- <span data-ttu-id="4e6e7-130">Шаблоны групповой политики: обновление существующей групповой политики с помощью новых шаблонов и включение новых параметров для существующей групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="4e6e7-130">Group Policy Templates: Update the existing Group Policy with new templates and enable new settings on existing MBAM Group Policy</span></span>

> [!NOTE]
> <span data-ttu-id="4e6e7-131">Перед запуском обновлений рекомендуется создать полную резервную копию базы данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="4e6e7-131">We recommend that you create a full database backup of the MBAM databases before you run the upgrades.</span></span>

### <span data-ttu-id="4e6e7-132">Обновление сервера SQL Server MBAM</span><span class="sxs-lookup"><span data-stu-id="4e6e7-132">Upgrade the MBAM SQL Server</span></span>

<span data-ttu-id="4e6e7-133">Просмотрите этот видеоролик, чтобы получить сведения о том, как обновить SQL Server MBAM:</span><span class="sxs-lookup"><span data-stu-id="4e6e7-133">Watch this video to learn how to upgrade the MBAM SQL Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### <span data-ttu-id="4e6e7-134">Обновление веб-сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="4e6e7-134">Upgrade the MBAM Web Server</span></span>

<span data-ttu-id="4e6e7-135">Просмотрите этот видеоролик, чтобы получить сведения о том, как обновить веб-сервер MBAM:</span><span class="sxs-lookup"><span data-stu-id="4e6e7-135">Watch this video to learn how to upgrade the MBAM Web Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## <span data-ttu-id="4e6e7-136">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="4e6e7-136">More information</span></span>

<span data-ttu-id="4e6e7-137">Дополнительные сведения об известных проблемах в MBAM 2,5 с пакетом обновления 1 (SP1) можно найти в разделе [заметки о выпуске для MBAM 2,5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).</span><span class="sxs-lookup"><span data-stu-id="4e6e7-137">For more information about known issues in MBAM 2.5 SP1, see [Release Notes for MBAM 2.5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).</span></span>
