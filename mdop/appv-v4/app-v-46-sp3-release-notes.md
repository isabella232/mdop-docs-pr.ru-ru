---
title: Заметки о выпуске App-V 4.6 с пакетом обновления 3 (SP3)
description: Заметки о выпуске App-V 4.6 с пакетом обновления 3 (SP3)
author: dansimp
ms.assetid: 206fadeb-59cc-47b4-836f-191ab1c27ff8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: dd0b82c5e12cbe161066a7f4a4e0932cb92cca42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819792"
---
# <span data-ttu-id="f9266-103">Заметки о выпуске App-V 4.6 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="f9266-103">App-V 4.6 SP3 Release Notes</span></span>


<span data-ttu-id="f9266-104">Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="f9266-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="f9266-105">Внимательно прочтите эти заметки о выпуске, прежде чем устанавливать систему управления Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="f9266-105">Read these Release Notes thoroughly before you install the Microsoft Application Virtualization (App-V) Management System.</span></span> <span data-ttu-id="f9266-106">Эти заметки о выпуске содержат сведения, которые помогут вам успешно установить Application Virtualization (App-V) 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="f9266-106">These Release Notes contain information that helps you successfully install Application Virtualization (App-V)4.6 SP3.</span></span> <span data-ttu-id="f9266-107">Этот документ содержит сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="f9266-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="f9266-108">Если между этими заметками о выпуске и другой документацией приложения App-V есть разница, Последнее изменение должно считаться полномочным.</span><span class="sxs-lookup"><span data-stu-id="f9266-108">If there is a difference between these Release Notes and other App-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="f9266-109">Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.</span><span class="sxs-lookup"><span data-stu-id="f9266-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="f9266-110">Защита от уязвимостей и вирусов в системе безопасности</span><span class="sxs-lookup"><span data-stu-id="f9266-110">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="f9266-111">Для защиты от уязвимостей и вирусов в системе безопасности важно установить последние обновления безопасности для любого нового программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="f9266-111">To help protect against security vulnerabilities and viruses, it is important to install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="f9266-112">Дополнительные сведения можно найти на [веб-сайте Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="f9266-112">For more information, see the [Microsoft Security website](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="f9266-113">Известные проблемы с виртуализацией приложений 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="f9266-113">Known Issues with Application Virtualization4.6 SP3</span></span>


<span data-ttu-id="f9266-114">Этот раздел содержит наиболее актуальные сведения о проблемах, связанных с Microsoft Application Virtualization (App-V) 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="f9266-114">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.6SP3.</span></span> <span data-ttu-id="f9266-115">Эти проблемы не отображаются в документации на продукт, и в некоторых случаях может привести к противоречию с существующим документом о продукте.</span><span class="sxs-lookup"><span data-stu-id="f9266-115">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="f9266-116">По возможности эти проблемы будут рассмотрены в более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="f9266-116">When it is possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="f9266-117">Не удается открыть гиперссылки с помощью Internet Explorer11 в Microsoft Windows 8,1 в виртуальной среде</span><span class="sxs-lookup"><span data-stu-id="f9266-117">Unable to open hyperlinks using Internet Explorer11 on Microsoft Windows 8.1 within the Virtual Environment</span></span>

<span data-ttu-id="f9266-118">При попытке открыть гиперссылки из виртуальной среды в Windows 8,1 с помощью Internet Explorer 11 происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="f9266-118">Attempting to open hyperlinks from within a virtual environment will fail on Windows 8.1 using Internet Explorer 11.</span></span> <span data-ttu-id="f9266-119">Это связано с тем, что в Internet Explorer 11 теперь есть возможность включения режима повышенной защиты (EPM) по умолчанию, и это приводит к тому, что приложению-V не удается получить доступ к нужным разделам реестра, файлам и объектам коммуникационного порта.</span><span class="sxs-lookup"><span data-stu-id="f9266-119">This is because Internet Explorer 11 now ships with the Enhanced Protection Mode (EPM) enabled by default and this causes App-V to be unable to access required registry keys, files and communication port objects.</span></span>

<span data-ttu-id="f9266-120">ВРЕМЕННОе решение: отключите функцию EPM в Internet Explorer11, прежде чем открывать пакет App-V.</span><span class="sxs-lookup"><span data-stu-id="f9266-120">WORKAROUND: Disable EPM in Internet Explorer11 before opening an App-V package.</span></span> <span data-ttu-id="f9266-121">Это позволит вам открыть Internet Explorer в виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="f9266-121">This will allow you to open Internet Explorer from within the virtual environment.</span></span>

## <span data-ttu-id="f9266-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f9266-122">Related topics</span></span>


[<span data-ttu-id="f9266-123">Сведения о системе Microsoft Application Virtualization 4.6 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="f9266-123">About Microsoft Application Virtualization 4.6 SP3</span></span>](about-microsoft-application-virtualization-46-sp3.md)

 

 





