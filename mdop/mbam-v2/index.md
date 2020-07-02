---
title: Руководство администратора для администрирования Microsoft BitLocker и мониторинга 2
description: Руководство администратора для администрирования Microsoft BitLocker и мониторинга 2
author: dansimp
ms.assetid: fdb43f62-960a-4811-8802-50efdf04b4af
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: dd6deb6fb91c64ac8609b54114e0dd417497034a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795918"
---
# <span data-ttu-id="f2a61-103">Руководство администратора для администрирования Microsoft BitLocker и мониторинга 2</span><span class="sxs-lookup"><span data-stu-id="f2a61-103">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>

<span data-ttu-id="f2a61-104">Microsoft BitLockerAdministration и мониторинг (MBAM) 2.0 — это упрощенный интерфейс администрирования, который можно использовать для управления шифрованием диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f2a61-104">Microsoft BitLockerAdministration and Monitoring(MBAM)2.0 provides a simplified administrative interface that you can use to manage BitLocker drive encryption.</span></span> <span data-ttu-id="f2a61-105">В BitLockerAdministration и мониторинге 2.0 вы можете выбрать параметры политики шифрования диска BitLocker, подходящие для вашего предприятия, а затем использовать их для отслеживания соответствия требованиям клиентов этим политикам.</span><span class="sxs-lookup"><span data-stu-id="f2a61-105">In BitLockerAdministration and Monitoring2.0, you can select BitLocker drive encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="f2a61-106">Вы также можете сообщить о состоянии шифрования отдельного компьютера и всего предприятия.</span><span class="sxs-lookup"><span data-stu-id="f2a61-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="f2a61-107">Кроме того, вы можете получить доступ к сведениям о ключе восстановления, когда пользователь забыл свой PIN-код или пароль, а также при изменении BIOS или загрузочной записи.</span><span class="sxs-lookup"><span data-stu-id="f2a61-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span>

## <span data-ttu-id="f2a61-108">Структуры</span><span class="sxs-lookup"><span data-stu-id="f2a61-108">Outline</span></span>

- [<span data-ttu-id="f2a61-109">Начало работы с MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-109">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="f2a61-110">Сведения о MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-110">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)
  - [<span data-ttu-id="f2a61-111">Заметки о выпуске для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-111">Release Notes for MBAM 2.0</span></span>](release-notes-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="f2a61-112">Сведения о MBAM 2.0 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="f2a61-112">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)
  - [<span data-ttu-id="f2a61-113">Заметки о выпуске для MBAM 2.0 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="f2a61-113">Release Notes for MBAM 2.0 SP1</span></span>](release-notes-for-mbam-20-sp1.md)
  - [<span data-ttu-id="f2a61-114">Оценка MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-114">Evaluating MBAM 2.0</span></span>](evaluating-mbam-20-mbam-2.md)
  - [<span data-ttu-id="f2a61-115">Высокоуровневая архитектура для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-115">High-Level Architecture for MBAM 2.0</span></span>](high-level-architecture-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="f2a61-116">Специальные возможности для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-116">Accessibility for MBAM 2.0</span></span>](accessibility-for-mbam-20-mbam-2.md)
- [<span data-ttu-id="f2a61-117">Планирование для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-117">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="f2a61-118">Подготовка среды для развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-118">Preparing your Environment for MBAM 2.0</span></span>](preparing-your-environment-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="f2a61-119">Необходимые условия для развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-119">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)
  - [<span data-ttu-id="f2a61-120">Планирование развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-120">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)
  - [<span data-ttu-id="f2a61-121">Поддерживаемые конфигурации MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-121">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)
  - [<span data-ttu-id="f2a61-122">Контрольный список планирования MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-122">MBAM 2.0 Planning Checklist</span></span>](mbam-20-planning-checklist-mbam-2.md)
- [<span data-ttu-id="f2a61-123">Развертывание MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-123">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)
  - [<span data-ttu-id="f2a61-124">Развертывание инфраструктуры сервера MBAM 2.0 Server</span><span class="sxs-lookup"><span data-stu-id="f2a61-124">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)
  - [<span data-ttu-id="f2a61-125">Развертывание объектов групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-125">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)
  - [<span data-ttu-id="f2a61-126">Развертывание клиента MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-126">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)
  - [<span data-ttu-id="f2a61-127">Контрольный список необходимых компонентов развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-127">MBAM 2.0 Deployment Checklist</span></span>](mbam-20-deployment-checklist-mbam-2.md)
  - [<span data-ttu-id="f2a61-128">Обновление с предыдущих версий MBAM</span><span class="sxs-lookup"><span data-stu-id="f2a61-128">Upgrading from Previous Versions of MBAM</span></span>](upgrading-from-previous-versions-of-mbam.md)
- [<span data-ttu-id="f2a61-129">Операции MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-129">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="f2a61-130">Использование MBAM с диспетчером конфигураций</span><span class="sxs-lookup"><span data-stu-id="f2a61-130">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)
  - [<span data-ttu-id="f2a61-131">Администрирование компонентов MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-131">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)
  - [<span data-ttu-id="f2a61-132">Мониторинг и создание отчетов по соответствию BitLocker с помощью MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-132">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="f2a61-133">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="f2a61-133">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)
  - [<span data-ttu-id="f2a61-134">Обслуживание MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-134">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)
  - [<span data-ttu-id="f2a61-135">Безопасность и конфиденциальность для MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-135">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="f2a61-136">Администрирование MBAM 2.0 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="f2a61-136">Administering MBAM 2.0 Using PowerShell</span></span>](administering-mbam-20-using-powershell-mbam-2.md)
- [<span data-ttu-id="f2a61-137">Устранение неполадок MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f2a61-137">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

## <span data-ttu-id="f2a61-138">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="f2a61-138">More Information</span></span>

- [<span data-ttu-id="f2a61-139">Информационные функции для MDOP</span><span class="sxs-lookup"><span data-stu-id="f2a61-139">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="f2a61-140">Ознакомьтесь с документацией, видеороликами и прочими материалами, посвященными технологиям MDOP.</span><span class="sxs-lookup"><span data-stu-id="f2a61-140">Find documentation, videos, and other resources for MDOP technologies.</span></span>

 

 





