---
title: Планирование развертывания DaRT 7.0
description: Планирование развертывания DaRT 7.0
author: dansimp
ms.assetid: 05e97cdb-a8c2-46e4-9c75-a7d12fe26fe8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09725e994a95f4f93ae655402e7577e137e33f18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821319"
---
# <span data-ttu-id="7ec29-103">Планирование развертывания DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7ec29-103">Planning to Deploy DaRT 7.0</span></span>


<span data-ttu-id="7ec29-104">Существует несколько различных конфигураций и предварительных требований, которые необходимо принять перед созданием плана развертывания.</span><span class="sxs-lookup"><span data-stu-id="7ec29-104">There are a number of different deployment configurations and prerequisites that you must consider before you create your deployment plan.</span></span> <span data-ttu-id="7ec29-105">В этом разделе содержатся сведения о том, как собрать сведения, необходимые для формулировки плана развертывания, который наилучшим образом соответствует вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="7ec29-105">This section includes information that can help you gather the information that you must have to formulate a deployment plan that best meets your business requirements.</span></span>

<span data-ttu-id="7ec29-106">Если вы планируете установку средств диагностики и восстановления Microsoft (DaRT) 7, учитывайте следующее:</span><span class="sxs-lookup"><span data-stu-id="7ec29-106">Consider the following when you plan your Microsoft Diagnostics and Recovery Toolset (DaRT)7 installation:</span></span>

-   <span data-ttu-id="7ec29-107">При установке DaRT вы можете установить все функции, связанные с выполнением DaRT, на компьютере администратора, на котором вы будете выполнять все задачи.</span><span class="sxs-lookup"><span data-stu-id="7ec29-107">When you install DaRT, you can either install all functionality on an IT administrator computer where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="7ec29-108">Кроме того, вы можете установить только функцию DaRT, которая создает образ восстановления на компьютере администратора.</span><span class="sxs-lookup"><span data-stu-id="7ec29-108">Or you can install only the DaRT functionality that creates the recovery image on the IT administrator computer.</span></span> <span data-ttu-id="7ec29-109">Затем установите функцию, используемую для запуска DaRT (например, **средство просмотра удаленных подключений DART** и **анализатор аварийных сбоев**) на компьютере агента службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="7ec29-109">Then, install the functionality used to run DaRT, such as the **DaRT Remote Connection Viewer** and **Crash Analyzer**, on a helpdesk agent computer.</span></span>

-   <span data-ttu-id="7ec29-110">Чтобы можно было удаленно запускать DaRT, убедитесь в том, что компьютер агента службы поддержки и все компьютеры, на которых может быть выполнена удаленная диагностика, находятся в одной сети.</span><span class="sxs-lookup"><span data-stu-id="7ec29-110">To be able to run DaRT remotely, make sure that the helpdesk agent computer and all computers that you might be troubleshooting remotely are on the same network.</span></span>

-   <span data-ttu-id="7ec29-111">Перед тем как приступить к развертыванию DaRT, вы можете сначала построить лабораторную среду для тестирования.</span><span class="sxs-lookup"><span data-stu-id="7ec29-111">Before you roll out DaRT into production, you can first build a lab environment for testing.</span></span> <span data-ttu-id="7ec29-112">Тестовая лаборатория должна включать в себя не менее двух компьютеров, один из которых будет выступать в качестве компьютера агента ИТ-администратора/поддержки и один для работы в качестве компьютера конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="7ec29-112">A test lab should include a minimum of two computers, one to act as the IT administrator/helpdesk agent computer and one to act as an end-user computer.</span></span> <span data-ttu-id="7ec29-113">Кроме того, вы можете использовать три компьютера в лаборатории, если вы хотите отделять обязанности администратора от агента службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="7ec29-113">Or, you can use three computers in your lab if you want to separate the IT administrator responsibilities from those of the helpdesk agent.</span></span>

## <span data-ttu-id="7ec29-114">Проверка поддерживаемых конфигураций</span><span class="sxs-lookup"><span data-stu-id="7ec29-114">Review the supported configurations</span></span>


<span data-ttu-id="7ec29-115">Чтобы убедиться в том, что компьютеры, выбранные для установки клиента или компонента, соответствуют минимальным требованиям к оборудованию и операционной системе, ознакомьтесь со сведениями о поддерживаемых конфигурациях средств диагностики и восстановления Microsoft (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="7ec29-115">You should review the Microsoft Diagnostics and Recovery Toolset (DaRT)7 Supported Configurations information to confirm that the computers you have selected for client or feature installation meet the minimum hardware and operating system requirements.</span></span>

[<span data-ttu-id="7ec29-116">Поддерживаемые конфигурации в DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7ec29-116">DaRT 7.0 Supported Configurations</span></span>](dart-70-supported-configurations-dart-7.md)

## <span data-ttu-id="7ec29-117">Планирование создания изображения для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="7ec29-117">Plan for creating the DaRT recovery image</span></span>


<span data-ttu-id="7ec29-118">При создании изображения для восстановления DaRT необходимо решить, какие инструменты следует включить в изображение.</span><span class="sxs-lookup"><span data-stu-id="7ec29-118">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="7ec29-119">Когда вы принимаете это решение, помните, что конечные пользователи могут иногда получить доступ к различным средствам DaRT.</span><span class="sxs-lookup"><span data-stu-id="7ec29-119">When you make that decision, remember that end users might have access occasionally to the various DaRT tools.</span></span> <span data-ttu-id="7ec29-120">При создании образа восстановления вы также можете указать, нужно ли включать дополнительные драйверы или файлы.</span><span class="sxs-lookup"><span data-stu-id="7ec29-120">When you create the recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="7ec29-121">Определите расположение дополнительных драйверов или файлов, которые вы хотите включить в изображение для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="7ec29-121">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="7ec29-122">Необходимо учитывать требования и другие дополнительные рекомендации по планированию создания изображения для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="7ec29-122">You should be aware of the prerequisites and other additional planning recommendations for creating the DaRT recovery image.</span></span>

[<span data-ttu-id="7ec29-123">Планирование создания образа для восстановления DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7ec29-123">Planning to Create the DaRT 7.0 Recovery Image</span></span>](planning-to-create-the-dart-70-recovery-image.md)

## <span data-ttu-id="7ec29-124">Планирование сохранения и развертывания изображения для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="7ec29-124">Plan for saving and deploying the DaRT recovery image</span></span>


<span data-ttu-id="7ec29-125">Для сохранения и развертывания изображения восстановления DaRT можно использовать несколько методов.</span><span class="sxs-lookup"><span data-stu-id="7ec29-125">Several methods can be used to save and deploy the DaRT recovery image.</span></span> <span data-ttu-id="7ec29-126">Определив метод, который будет использоваться, продумайте преимущества и недостатки каждого из них.</span><span class="sxs-lookup"><span data-stu-id="7ec29-126">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="7ec29-127">Кроме того, вы можете использовать DaRT в Организации.</span><span class="sxs-lookup"><span data-stu-id="7ec29-127">Also, consider how you want to use DaRT in your enterprise.</span></span>

<span data-ttu-id="7ec29-128">**Примечание**  Возможно, вы захотите использовать в Организации более одного способа.</span><span class="sxs-lookup"><span data-stu-id="7ec29-128">**Note** You might want to use more than one method in your organization.</span></span> <span data-ttu-id="7ec29-129">Например, вы можете загрузить DaRT из удаленной секции для большинства ситуаций и получить доступ к флэш-накопителю USB на случай, если компьютер пользователя не может подключиться к сети.</span><span class="sxs-lookup"><span data-stu-id="7ec29-129">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

[<span data-ttu-id="7ec29-130">Планирование способов сохранения и развертывания образа для восстановления DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7ec29-130">Planning How to Save and Deploy the DaRT 7.0 Recovery Image</span></span>](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)

## <span data-ttu-id="7ec29-131">Другие ресурсы по планированию развертывания DaRT</span><span class="sxs-lookup"><span data-stu-id="7ec29-131">Other resources for Planning to Deploy DaRT</span></span>


[<span data-ttu-id="7ec29-132">Планирование для DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7ec29-132">Planning for DaRT 7.0</span></span>](planning-for-dart-70-new-ia.md)

 

 





