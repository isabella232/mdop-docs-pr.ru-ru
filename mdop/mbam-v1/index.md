---
title: Руководство администратора для администрирования Microsoft BitLocker и мониторинга 1
description: Руководство администратора для администрирования Microsoft BitLocker и мониторинга 1
author: dansimp
ms.assetid: 4086e721-db24-4439-bdcd-ac5ef901811f
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 5336108e12738a21441df8062fbcd8bd98933945
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795922"
---
# <span data-ttu-id="c51ec-103">Руководство администратора для администрирования Microsoft BitLocker и мониторинга 1</span><span class="sxs-lookup"><span data-stu-id="c51ec-103">Microsoft BitLocker Administration and Monitoring 1 Administrator's Guide</span></span>

<span data-ttu-id="c51ec-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) — это упрощенный интерфейс администрирования, который можно использовать для управления шифрованием диска BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51ec-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides a simplified administrative interface that you can use to manage BitLocker drive encryption.</span></span> <span data-ttu-id="c51ec-105">С помощью MBAM вы можете выбрать параметры политики шифрования BitLocker, соответствующие вашей организации, а затем использовать их для отслеживания соответствия требованиям клиентов этим политикам.</span><span class="sxs-lookup"><span data-stu-id="c51ec-105">With MBAM, you can select BitLocker encryption policy options that are appropriate to your enterprise and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="c51ec-106">Вы также можете сообщить о состоянии шифрования отдельного компьютера и всего предприятия.</span><span class="sxs-lookup"><span data-stu-id="c51ec-106">You can also report on the encryption status of an individual computer and on the entire enterprise.</span></span> <span data-ttu-id="c51ec-107">Кроме того, вы можете получить доступ к сведениям о ключе восстановления, когда пользователь забыл свой PIN-код или пароль, а также при изменении BIOS или загрузочной записи.</span><span class="sxs-lookup"><span data-stu-id="c51ec-107">In addition, you can access recovery key information when users forget their PIN or password, or when their BIOS or boot record changes.</span></span>

- [<span data-ttu-id="c51ec-108">Начало работы с MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-108">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)  
  - [<span data-ttu-id="c51ec-109">Сведения о MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-109">About MBAM 1.0</span></span>](about-mbam-10.md)
  - [<span data-ttu-id="c51ec-110">Заметки о выпуске для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-110">Release Notes for MBAM 1.0</span></span>](release-notes-for-mbam-10.md)
  - [<span data-ttu-id="c51ec-111">Оценка MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-111">Evaluating MBAM 1.0</span></span>](evaluating-mbam-10.md)
  - [<span data-ttu-id="c51ec-112">Высокоуровневая архитектура для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-112">High Level Architecture for MBAM 1.0</span></span>](high-level-architecture-for-mbam-10.md)
  - [<span data-ttu-id="c51ec-113">Специальные возможности для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-113">Accessibility for MBAM 1.0</span></span>](accessibility-for-mbam-10.md)
  - [<span data-ttu-id="c51ec-114">Заявление о конфиденциальности для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-114">Privacy Statement for MBAM 1.0</span></span>](privacy-statement-for-mbam-10.md)
- [<span data-ttu-id="c51ec-115">Планирование для MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-115">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)  
  - [<span data-ttu-id="c51ec-116">Подготовка среды для развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-116">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)
  - [<span data-ttu-id="c51ec-117">Необходимые компоненты развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-117">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)
  - [<span data-ttu-id="c51ec-118">Планирование развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-118">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)
  - [<span data-ttu-id="c51ec-119">Поддерживаемые конфигурации MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-119">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)
  - [<span data-ttu-id="c51ec-120">Контрольный список планирования MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-120">MBAM 1.0 Planning Checklist</span></span>](mbam-10-planning-checklist.md)
- [<span data-ttu-id="c51ec-121">Развертывание MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-121">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)  
  - [<span data-ttu-id="c51ec-122">Развертывание инфраструктуры сервера MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-122">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)
  - [<span data-ttu-id="c51ec-123">Развертывание объектов групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-123">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)
  - [<span data-ttu-id="c51ec-124">Развертывание клиента MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-124">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)
  - [<span data-ttu-id="c51ec-125">Развертывание обновления языковой версии MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-125">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)
  - [<span data-ttu-id="c51ec-126">Контрольный список необходимых компонентов развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-126">MBAM 1.0 Deployment Checklist</span></span>](mbam-10-deployment-checklist.md)
- [<span data-ttu-id="c51ec-127">Операции MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-127">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)  
  - [<span data-ttu-id="c51ec-128">Администрирование компонентов MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-128">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)
  - [<span data-ttu-id="c51ec-129">Мониторинг и создание отчетов по соответствию BitLocker с помощью MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-129">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)
  - [<span data-ttu-id="c51ec-130">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="c51ec-130">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)
  - [<span data-ttu-id="c51ec-131">Администрирование MBAM 1.0 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="c51ec-131">Administering MBAM 1.0 by Using PowerShell</span></span>](administering-mbam-10-by-using-powershell.md)
- [<span data-ttu-id="c51ec-132">Устранение неполадок MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c51ec-132">Troubleshooting MBAM 1.0</span></span>](troubleshooting-mbam-10.md)  

## <span data-ttu-id="c51ec-133">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="c51ec-133">More Information</span></span>
- [<span data-ttu-id="c51ec-134">Информационные функции для MDOP</span><span class="sxs-lookup"><span data-stu-id="c51ec-134">MDOP Information Experience</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=236032)  
  <span data-ttu-id="c51ec-135">Ознакомьтесь с документацией, видеороликами и прочими материалами, посвященными технологиям MDOP.</span><span class="sxs-lookup"><span data-stu-id="c51ec-135">Find documentation, videos, and other resources for MDOP technologies.</span></span>
