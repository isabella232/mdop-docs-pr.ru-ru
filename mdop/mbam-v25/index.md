---
title: Microsoft BitLocker Administration and Monitoring 2.5
description: Microsoft BitLocker Administration and Monitoring 2.5
author: dansimp
ms.assetid: fd81d7de-b166-47e8-b6c7-d984830762b6
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 2e5243131853207f0ed3cbb6d0cd8fb8e3d56108
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795890"
---
# <span data-ttu-id="d8507-103">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-103">Microsoft BitLocker Administration and Monitoring 2.5</span></span>

<span data-ttu-id="d8507-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) 2,5 предоставляет упрощенный интерфейс администрирования, который можно использовать для управления шифрованием диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d8507-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 provides a simplified administrative interface that you can use to manage BitLocker Drive Encryption.</span></span> <span data-ttu-id="d8507-105">Вы настраиваете шаблоны групповой политики MBAM, которые позволяют настраивать параметры политики шифрования диска BitLocker, подходящие для вашего предприятия, а затем используйте их для отслеживания соответствия требованиям клиентов этим политикам.</span><span class="sxs-lookup"><span data-stu-id="d8507-105">You configure MBAM Group Policy Templates that enable you to set BitLocker Drive Encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="d8507-106">Вы также можете сообщить о состоянии шифрования отдельного компьютера и всего предприятия.</span><span class="sxs-lookup"><span data-stu-id="d8507-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="d8507-107">Кроме того, вы можете получить доступ к сведениям о ключе восстановления, когда пользователь забыл свой PIN-код или пароль, а также при изменении BIOS или загрузочной записи.</span><span class="sxs-lookup"><span data-stu-id="d8507-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span> <span data-ttu-id="d8507-108">Более подробное описание MBAM можно найти в разделе [о MBAM 2,5](about-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="d8507-108">For a more detailed description of MBAM, see [About MBAM 2.5](about-mbam-25.md).</span></span>

<span data-ttu-id="d8507-109">Чтобы получить MBAM, ознакомьтесь со [статьей получение MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop).</span><span class="sxs-lookup"><span data-stu-id="d8507-109">To obtain MBAM, see [How Do I Get MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop).</span></span>

## <span data-ttu-id="d8507-110">Структуры</span><span class="sxs-lookup"><span data-stu-id="d8507-110">Outline</span></span>

- <a href="" id="getting-started-with-mbam-2-5"></a>[<span data-ttu-id="d8507-111">Начало работы с MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-111">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)
  - [<span data-ttu-id="d8507-112">О программе MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-112">About MBAM 2.5</span></span>](about-mbam-25.md)
  - [<span data-ttu-id="d8507-113">Заметки о выпуске для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-113">Release Notes for MBAM 2.5</span></span>](release-notes-for-mbam-25.md)
  - [<span data-ttu-id="d8507-114">Сведения о программе MBAM 2.5 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="d8507-114">About MBAM 2.5 SP1</span></span>](about-mbam-25-sp1.md)
  - [<span data-ttu-id="d8507-115">Заметки о выпуске MBAM 2.5 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="d8507-115">Release Notes for MBAM 2.5 SP1</span></span>](release-notes-for-mbam-25-sp1.md)
  - [<span data-ttu-id="d8507-116">Оценка MBAM 2.5 в тестовой среде</span><span class="sxs-lookup"><span data-stu-id="d8507-116">Evaluating MBAM 2.5 in a Test Environment</span></span>](evaluating-mbam-25-in-a-test-environment.md)
  - [<span data-ttu-id="d8507-117">Высокоуровневая архитектура для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-117">High-Level Architecture for MBAM 2.5</span></span>](high-level-architecture-for-mbam-25.md)
  - [<span data-ttu-id="d8507-118">Специальные возможности для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-118">Accessibility for MBAM 2.5</span></span>](accessibility-for-mbam-25.md)
- <a href="" id="planning-for-mbam-2-5"></a>[<span data-ttu-id="d8507-119">Планирование для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-119">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)
  - [<span data-ttu-id="d8507-120">Подготовка среды для развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-120">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)
  - [<span data-ttu-id="d8507-121">Необходимые условия для развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-121">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)
  - [<span data-ttu-id="d8507-122">Планирование требований групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-122">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)
  - [<span data-ttu-id="d8507-123">Планирование групп и учетных записей MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-123">Planning for MBAM 2.5 Groups and Accounts</span></span>](planning-for-mbam-25-groups-and-accounts.md)
  - [<span data-ttu-id="d8507-124">Планирование защиты веб-сайтов MBAM</span><span class="sxs-lookup"><span data-stu-id="d8507-124">Planning How to Secure the MBAM Websites</span></span>](planning-how-to-secure-the-mbam-websites.md)
  - [<span data-ttu-id="d8507-125">Планирование развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-125">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)
  - [<span data-ttu-id="d8507-126">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-126">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)
  - [<span data-ttu-id="d8507-127">Планирование высокой доступности MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-127">Planning for MBAM 2.5 High Availability</span></span>](planning-for-mbam-25-high-availability.md)
  - [<span data-ttu-id="d8507-128">Процедуры безопасности MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-128">MBAM 2.5 Security Considerations</span></span>](mbam-25-security-considerations.md)
  - [<span data-ttu-id="d8507-129">Контрольный список планирования MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-129">MBAM 2.5 Planning Checklist</span></span>](mbam-25-planning-checklist.md)
- <a href="" id="deploying-mbam-2-5"></a>[<span data-ttu-id="d8507-130">Развертывание MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-130">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)
  - [<span data-ttu-id="d8507-131">Развертывание инфраструктуры сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="d8507-131">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)
  - [<span data-ttu-id="d8507-132">Развертывание объектов групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)
  - [<span data-ttu-id="d8507-133">Развертывание клиента MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-133">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)
  - [<span data-ttu-id="d8507-134">Контрольный список необходимых компонентов развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-134">MBAM 2.5 Deployment Checklist</span></span>](mbam-25-deployment-checklist.md)
  - [<span data-ttu-id="d8507-135">Обновление с предыдущих версий до MBAM 2.5 или MBAM 2.5 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="d8507-135">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)
  - [<span data-ttu-id="d8507-136">Удаление компонентов или программного обеспечения MBAM Server</span><span class="sxs-lookup"><span data-stu-id="d8507-136">Removing MBAM Server Features or Software</span></span>](removing-mbam-server-features-or-software.md)
- <a href="" id="operations-for-mbam-2-5"></a>[<span data-ttu-id="d8507-137">Операции MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-137">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)
  - [<span data-ttu-id="d8507-138">Администрирование компонентов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-138">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)
  - [<span data-ttu-id="d8507-139">Мониторинг и создание отчетов по соответствию BitLocker с помощью MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-139">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)
  - [<span data-ttu-id="d8507-140">Управление BitLocker с помощью MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-140">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)
  - [<span data-ttu-id="d8507-141">Обслуживание MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)
  - [<span data-ttu-id="d8507-142">Использование Windows PowerShell для администрирования MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-142">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)
- <a href="" id="troubleshooting-mbam-2-5"></a>[<span data-ttu-id="d8507-143">Устранение неполадок MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-143">Troubleshooting MBAM 2.5</span></span>](troubleshooting-mbam-25.md)
- <a href="" id="technical-reference-for-mbam-2-5"></a>[<span data-ttu-id="d8507-144">Технический справочник по MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d8507-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)
  - [<span data-ttu-id="d8507-145">Журналы событий клиента</span><span class="sxs-lookup"><span data-stu-id="d8507-145">Client Event Logs</span></span>](client-event-logs.md)
  - [<span data-ttu-id="d8507-146">Журналы событий сервера</span><span class="sxs-lookup"><span data-stu-id="d8507-146">Server Event Logs</span></span>](server-event-logs.md)

## <span data-ttu-id="d8507-147">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="d8507-147">More Information</span></span>

- [<span data-ttu-id="d8507-148">Информационные функции для MDOP</span><span class="sxs-lookup"><span data-stu-id="d8507-148">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="d8507-149">Ознакомьтесь с документацией, видеороликами и прочими материалами, посвященными технологиям MDOP.</span><span class="sxs-lookup"><span data-stu-id="d8507-149">Find documentation, videos, and other resources for MDOP technologies.</span></span>

- [<span data-ttu-id="d8507-150">Руководство по развертыванию MBAM</span><span class="sxs-lookup"><span data-stu-id="d8507-150">MBAM Deployment Guide</span></span>](https://www.microsoft.com/download/details.aspx?id=38398)

  <span data-ttu-id="d8507-151">Получите помощь в выборе метода развертывания для MBAM, в том числе пошаговых инструкций для каждого из этих методов.</span><span class="sxs-lookup"><span data-stu-id="d8507-151">Get help in choosing a deployment method for MBAM, including step-by-step instructions for each method.</span></span>
    
- [<span data-ttu-id="d8507-152">Установка исправлений на сервере MBAM 2,5 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="d8507-152">Apply Hotfixes on MBAM 2.5 SP1 Server</span></span>](apply-hotfix-for-mbam-25-sp1.md)

  <span data-ttu-id="d8507-153">Руководство по применению исправлений сервера MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="d8507-153">Guide of how to apply MBAM 2.5 SP1 Server hotfixes</span></span>
