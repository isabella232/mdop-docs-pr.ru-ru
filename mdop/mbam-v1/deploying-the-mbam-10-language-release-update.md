---
title: Развертывание обновления языковой версии MBAM 1.0
description: Развертывание обновления языковой версии MBAM 1.0
author: dansimp
ms.assetid: 9dbd85c3-e470-4752-a90f-25754dd46dab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a819be81594efd9349e3f6c0f6559c2b810bdc9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812824"
---
# <span data-ttu-id="5a74d-103">Развертывание обновления языковой версии MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5a74d-103">Deploying the MBAM 1.0 Language Release Update</span></span>


<span data-ttu-id="5a74d-104">Языковой выпуск Microsoft BitLocker (Администрирование и мониторинг) (MBAM) 1.0 является обновлением для MBAM и включает поддержку новых языков.</span><span class="sxs-lookup"><span data-stu-id="5a74d-104">Microsoft BitLocker Administration and Monitoring (MBAM)1.0 Language Release is an update to MBAM and includes the support of new languages.</span></span> <span data-ttu-id="5a74d-105">Новые языки:</span><span class="sxs-lookup"><span data-stu-id="5a74d-105">The new languages are:</span></span>

-   <span data-ttu-id="5a74d-106">Английский (EN-US)</span><span class="sxs-lookup"><span data-stu-id="5a74d-106">English (en-us)</span></span>

-   <span data-ttu-id="5a74d-107">Французский (fr)</span><span class="sxs-lookup"><span data-stu-id="5a74d-107">French (fr)</span></span>

-   <span data-ttu-id="5a74d-108">Итальянский (IT)</span><span class="sxs-lookup"><span data-stu-id="5a74d-108">Italian (it)</span></span>

-   <span data-ttu-id="5a74d-109">Немецкий (ru)</span><span class="sxs-lookup"><span data-stu-id="5a74d-109">German (de)</span></span>

-   <span data-ttu-id="5a74d-110">Испанский (ES)</span><span class="sxs-lookup"><span data-stu-id="5a74d-110">Spanish (es)</span></span>

-   <span data-ttu-id="5a74d-111">Корейский (Ko)</span><span class="sxs-lookup"><span data-stu-id="5a74d-111">Korean (ko)</span></span>

-   <span data-ttu-id="5a74d-112">Японский (JA)</span><span class="sxs-lookup"><span data-stu-id="5a74d-112">Japanese (ja)</span></span>

-   <span data-ttu-id="5a74d-113">Португальский (Бразилия) (тчк – BR)</span><span class="sxs-lookup"><span data-stu-id="5a74d-113">Brazilian Portuguese (pt-br)</span></span>

-   <span data-ttu-id="5a74d-114">Русский (ru)</span><span class="sxs-lookup"><span data-stu-id="5a74d-114">Russian (ru)</span></span>

-   <span data-ttu-id="5a74d-115">Китайская традиционная (zh-TW)</span><span class="sxs-lookup"><span data-stu-id="5a74d-115">Chinese Traditional (zh-tw)</span></span>

-   <span data-ttu-id="5a74d-116">Китайская упрощенная (zh-CN)</span><span class="sxs-lookup"><span data-stu-id="5a74d-116">Chinese Simplified (zh-cn)</span></span>

<span data-ttu-id="5a74d-117">Обновление на языке MBAM 1.0 изменит номер версии с MBAM 1.0.1237.1 на MBAM 1.0.2001.</span><span class="sxs-lookup"><span data-stu-id="5a74d-117">The MBAM1.0 language update will change the version number from MBAM 1.0.1237.1 to MBAM 1.0.2001.</span></span>

<span data-ttu-id="5a74d-118">Вам не нужно переустанавливать все функции MBAM, чтобы добавить эти дополнительные языки.</span><span class="sxs-lookup"><span data-stu-id="5a74d-118">You do not need to reinstall all of the MBAM features in order to add these additional languages.</span></span> <span data-ttu-id="5a74d-119">В этой статье описаны действия, которые необходимо выполнить, чтобы добавить новые поддерживаемые языки.</span><span class="sxs-lookup"><span data-stu-id="5a74d-119">This topic defines the steps required to add the newly supported languages.</span></span>

## <span data-ttu-id="5a74d-120">Развертывание MBAM международные выпуски для MBAM функций сервера</span><span class="sxs-lookup"><span data-stu-id="5a74d-120">Deploy the MBAM international release to MBAM Server features</span></span>


<span data-ttu-id="5a74d-121">Для начала необходимо обновить следующие возможности сервера MBAM:</span><span class="sxs-lookup"><span data-stu-id="5a74d-121">To begin, you must update the following MBAM server features:</span></span>

-   <span data-ttu-id="5a74d-122">Отчет о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="5a74d-122">Compliance and Audit Report</span></span>

-   <span data-ttu-id="5a74d-123">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="5a74d-123">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="5a74d-124">Шаблоны политик</span><span class="sxs-lookup"><span data-stu-id="5a74d-124">Policy Templates</span></span>

<span data-ttu-id="5a74d-125">Затем необходимо выполнить **MbamSetup.exe** для обновления функций MBAM, которые выполняются на одном и том же сервере.</span><span class="sxs-lookup"><span data-stu-id="5a74d-125">Then, you must run **MbamSetup.exe** to upgrade the MBAM features that run on the same server at the same time.</span></span>

[<span data-ttu-id="5a74d-126">Установка языкового обновления MBAM на отдельном сервере</span><span class="sxs-lookup"><span data-stu-id="5a74d-126">How to Install the MBAM Language Update on a Single Server</span></span>](how-to-install-the-mbam-language-update-on-a-single-server-mbam-1.md)

[<span data-ttu-id="5a74d-127">Установка обновлений языкового пакета MBAM на распределенных серверах</span><span class="sxs-lookup"><span data-stu-id="5a74d-127">How to Install the MBAM Language Update on Distributed Servers</span></span>](how-to-install-the-mbam-language-update-on-distributed-servers-mbam-1.md)

## <span data-ttu-id="5a74d-128">Установка языкового обновления для групповых политик MBAM</span><span class="sxs-lookup"><span data-stu-id="5a74d-128">Install the MBAM language update for Group Policies</span></span>


<span data-ttu-id="5a74d-129">Шаблоны групповой политики MBAM можно установить на каждую рабочую станцию для управления или скопировать в центральное хранилище групповой политики, чтобы сделать шаблоны доступными для всех администраторов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="5a74d-129">The MBAM Group Policy templates can be installed on each management workstation or they can be copied to the Group Policy central store, in order to make the templates available to all Group Policy administrators.</span></span> <span data-ttu-id="5a74d-130">Шаблоны политик невозможно установить непосредственно на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="5a74d-130">The policy templates cannot be directly installed on a domain controller.</span></span> <span data-ttu-id="5a74d-131">Если вы не используете центральное хранилище групповой политики, необходимо вручную скопировать политики на каждый контроллер домена, управляющий групповой политикой MBAM.</span><span class="sxs-lookup"><span data-stu-id="5a74d-131">If you do not use a Group Policy central store, then you must copy the policies manually to each domain controller that manages MBAM Group Policy.</span></span>

<span data-ttu-id="5a74d-132">Чтобы добавить шаблоны языковых политик MBAM, скопируйте языковые файлы групповой политики из%SystemRoot%\\PolicyDefinitions на компьютере, на котором роль "шаблоны политик" была установлена в одно и то же место на компьютере рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="5a74d-132">To add the MBAM language policies templates, copy the Group Policy language files from %SystemRoot%\\PolicyDefinitions on the computer where the “Policy Templates” role was installed to the same location on the workstation computer.</span></span> <span data-ttu-id="5a74d-133">Ниже приведены некоторые примеры файлов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="5a74d-133">Here are some examples of Group Policy files:</span></span>

-   <span data-ttu-id="5a74d-134">BitLockerManagement. ADMX</span><span class="sxs-lookup"><span data-stu-id="5a74d-134">BitLockerManagement.admx</span></span>

-   <span data-ttu-id="5a74d-135">BitLockerUserManagement. ADMX</span><span class="sxs-lookup"><span data-stu-id="5a74d-135">BitLockerUserManagement.admx</span></span>

-   <span data-ttu-id="5a74d-136">en-us\\BitLockerManagement.adml</span><span class="sxs-lookup"><span data-stu-id="5a74d-136">en-us\\BitLockerManagement.adml</span></span>

-   <span data-ttu-id="5a74d-137">en-us\\BitLockerUserManagement.adml</span><span class="sxs-lookup"><span data-stu-id="5a74d-137">en-us\\BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="5a74d-138">FR-fr\\ BitLockerManagement. ADML</span><span class="sxs-lookup"><span data-stu-id="5a74d-138">fr-fr\\ BitLockerManagement.adml</span></span>

-   <span data-ttu-id="5a74d-139">FR-fr\\ BitLockerUserManagement. ADML</span><span class="sxs-lookup"><span data-stu-id="5a74d-139">fr-fr\\ BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="5a74d-140">(и аналогично для каждого поддерживаемого языка)</span><span class="sxs-lookup"><span data-stu-id="5a74d-140">(and similarly for each supported language)</span></span>

## <span data-ttu-id="5a74d-141">Известные проблемы в MBAM международной выпуске</span><span class="sxs-lookup"><span data-stu-id="5a74d-141">Known issues in the MBAM international release</span></span>


<span data-ttu-id="5a74d-142">В этой статье описаны известные проблемы, связанные с администрированием Microsoft BitLocker и международным выпуском для мониторинга.</span><span class="sxs-lookup"><span data-stu-id="5a74d-142">This topic contains known issues for Microsoft BitLocker Administration and Monitoring International Release.</span></span>

[<span data-ttu-id="5a74d-143">Известные проблемы, связанные с международным выпуском MBAM</span><span class="sxs-lookup"><span data-stu-id="5a74d-143">Known Issues in the MBAM International Release</span></span>](known-issues-in-the-mbam-international-release-mbam-1.md)

## <span data-ttu-id="5a74d-144">Другие ресурсы по развертыванию языкового обновления для MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="5a74d-144">Other resources for deploying the MBAM 1.0 Language Update</span></span>


[<span data-ttu-id="5a74d-145">Развертывание MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5a74d-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





