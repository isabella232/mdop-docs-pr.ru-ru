---
title: Высокоуровневая архитектура
description: Высокоуровневая архитектура
author: dansimp
ms.assetid: a00edb9f-207b-4f32-9e8f-522ea2739d2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a5db4a56b2abfb0df19b0d6d86f4bf88380c2bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827292"
---
# <span data-ttu-id="7bbd2-103">Высокоуровневая архитектура</span><span class="sxs-lookup"><span data-stu-id="7bbd2-103">High-Level Architecture</span></span>


<span data-ttu-id="7bbd2-104">В этом разделе описывается архитектура системы высокого уровня и проектирование компонентов Microsoft Enterprise Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-104">This section describes the high-level system architecture and component design of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="7bbd2-105">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="7bbd2-105">System Architecture</span></span>


<span data-ttu-id="7bbd2-106">MED-V расширяет возможности Virtual PC для Windows, чтобы работать с двумя операционными системами на одном устройстве, добавлять виртуальные образы, подготавливать их и централизованно управлять.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-106">MED-V enhances Windows Virtual PC to run two operating systems on one device, adding virtual image delivery, Group Policy-based provisioning, and centralized management.</span></span> <span data-ttu-id="7bbd2-107">С помощью MED-V вы можете легко настраивать, развертывать и управлять корпоративными изображениями виртуальных ПК под управлением Windows на компьютерах под управлением Windows 7 Профессиональная, Enterprise и Windows 7 Ultimate.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-107">By using MED-V, you can easily configure, deploy, and manage corporate Windows Virtual PC images on any Windows-based desktop running Windows 7 Professional, Enterprise, or Windows 7 Ultimate.</span></span> <span data-ttu-id="7bbd2-108">Решение для MED-V включает следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="7bbd2-108">The MED-V solution includes the following components:</span></span>

<a href="" id="---------------med-v-host"></a> **<span data-ttu-id="7bbd2-109">Узел MED-V</span><span class="sxs-lookup"><span data-stu-id="7bbd2-109">MED-V Host</span></span>**  
<span data-ttu-id="7bbd2-110">Среда Windows 7, включающая в себя агент узла MED-V, электронную рассылку программного обеспечения (ESD), систему управления реестром и гостя MED-V.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-110">A Windows 7 environment that includes a MED-V Host Agent, an electronic software distribution (ESD) system, a registry management system, and a MED-V guest.</span></span> <span data-ttu-id="7bbd2-111">Узел MED-V взаимодействует с гостевой системой MED-V, чтобы можно было обрабатывать определенные функции настройки и сведения о системе.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-111">The MED-V host interacts with the MED-V guest so that certain setup functions and system information can be processed.</span></span>

<a href="" id="-------------------med-v-host-agent"></a> **<span data-ttu-id="7bbd2-112">Агент узла MED-V</span><span class="sxs-lookup"><span data-stu-id="7bbd2-112">MED-V Host Agent</span></span>**  
<span data-ttu-id="7bbd2-113">Программное обеспечение MED-V, содержащееся на узле MED-V, которое предоставляет канал для связи с гостевой системой MED-V.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-113">The MED-V software contained in the MED-V host that provides a channel to communicate with the MED-V guest.</span></span> <span data-ttu-id="7bbd2-114">Она также предоставляет такие функциональные возможности, как установка первого раза и публикация приложений.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-114">It also provides functionality such as first time setup and application publishing.</span></span>

<span data-ttu-id="7bbd2-115">**Примечание**  После установки MED-V и обязательных компонентов необходимо настроить MED-V.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-115">**Note** After MED-V and its required components are installed MED-V must be configured.</span></span> <span data-ttu-id="7bbd2-116">Настройка MED-V называется при первом запуске программы.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-116">The configuration of MED-V is referred to as first time setup.</span></span>

 

<a href="" id="esd-system"></a>**<span data-ttu-id="7bbd2-117">Система ESD</span><span class="sxs-lookup"><span data-stu-id="7bbd2-117">ESD System</span></span>**  
<span data-ttu-id="7bbd2-118">Существующий метод распространения программного обеспечения, который позволяет развертывать и устанавливать файлы пакета для рабочей области MED-V, создаваемые MED-V.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-118">Your existing software distribution method that lets you deploy and install the MED-V workspace package files that MED-V creates.</span></span>

<a href="" id="registry-management-system"></a>**<span data-ttu-id="7bbd2-119">Система управления реестром</span><span class="sxs-lookup"><span data-stu-id="7bbd2-119">Registry Management System</span></span>**  
<span data-ttu-id="7bbd2-120">Существующий способ управления параметрами и настройками групповой политики.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-120">Your existing method of managing Group Policy settings and preferences.</span></span>

<a href="" id="windows-virtual-pc-image"></a>**<span data-ttu-id="7bbd2-121">Образ виртуальных компьютеров Windows</span><span class="sxs-lookup"><span data-stu-id="7bbd2-121">Windows Virtual PC Image</span></span>**  
<span data-ttu-id="7bbd2-122">Виртуальная машина, определенная администратором и содержащая следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="7bbd2-122">An administrator-defined virtual machine that contains the following components:</span></span>

<a href="" id="corporate-operating-system"></a>**<span data-ttu-id="7bbd2-123">Корпоративная операционная система</span><span class="sxs-lookup"><span data-stu-id="7bbd2-123">Corporate Operating System</span></span>**  
<span data-ttu-id="7bbd2-124">Ваша Стандартная корпоративная операционная система.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-124">Your standard corporate operating system.</span></span>

<a href="" id="management-and-security-tools"></a>**<span data-ttu-id="7bbd2-125">Средства управления и безопасности</span><span class="sxs-lookup"><span data-stu-id="7bbd2-125">Management and Security Tools</span></span>**  
<span data-ttu-id="7bbd2-126">Ваши стандартные средства управления и безопасности, например защита от вирусов.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-126">Your standard management and security tools, such as virus protection.</span></span>

<a href="" id="-----------------------med-v-guest"></a> **<span data-ttu-id="7bbd2-127">Гость для MED-V</span><span class="sxs-lookup"><span data-stu-id="7bbd2-127">MED-V Guest</span></span>**  
<span data-ttu-id="7bbd2-128">Среда Windows XP с пакетом обновления 3 (SP3), как часть виртуального ПК под управлением Windows 7, которая включает следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="7bbd2-128">A Windows XP SP3 environment, as part of a Windows Virtual PC running on Windows 7 that contains the following components:</span></span>

<a href="" id="---------------------------med-v-guest-agent"></a> **<span data-ttu-id="7bbd2-129">Гостевой агент MED-V</span><span class="sxs-lookup"><span data-stu-id="7bbd2-129">MED-V Guest Agent</span></span>**  
<span data-ttu-id="7bbd2-130">Программное обеспечение MED-V, содержащееся в гостевой системе MED-V и предоставляющее канал для связи с узлом MED-V.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-130">The MED-V software contained in the MED-V guest that provides a channel to communicate with the MED-V host.</span></span> <span data-ttu-id="7bbd2-131">Кроме того, он поддерживает агент узла MED-V с такими функциями, как выполнение первой настройки.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-131">It also supports the MED-V Host Agent with functions like performing first time setup.</span></span>

<span data-ttu-id="7bbd2-132">**Примечание**  Гостевой агент MED-V устанавливается автоматически при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-132">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<a href="" id="esd-client"></a>**<span data-ttu-id="7bbd2-133">Клиент ESD</span><span class="sxs-lookup"><span data-stu-id="7bbd2-133">ESD Client</span></span>**  
<span data-ttu-id="7bbd2-134">Необязательная часть системы ESD, которая устанавливает пакеты программного обеспечения и сообщает о состоянии в системе ESD.</span><span class="sxs-lookup"><span data-stu-id="7bbd2-134">An optional part of your ESD system that installs software packages and reports status to the ESD system.</span></span>

## <span data-ttu-id="7bbd2-135">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7bbd2-135">Related topics</span></span>


[<span data-ttu-id="7bbd2-136">Планирование совместимости приложений и операционной системы</span><span class="sxs-lookup"><span data-stu-id="7bbd2-136">Planning for Application Operating System Compatibility</span></span>](planning-for-application-operating-system-compatibility.md)

[<span data-ttu-id="7bbd2-137">Подготовка среды развертывания для MED-V</span><span class="sxs-lookup"><span data-stu-id="7bbd2-137">Prepare the Deployment Environment for MED-V</span></span>](prepare-the-deployment-environment-for-med-v.md)

 

 





