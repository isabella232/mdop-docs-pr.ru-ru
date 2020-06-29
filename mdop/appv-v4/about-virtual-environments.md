---
title: Сведения о виртуальных средах
description: Сведения о виртуальных средах
author: dansimp
ms.assetid: e03a8c72-56c1-4ae9-aa45-0283c50a154c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15f3ae29ae8d5586f83baa98ea6821e09ae5c305
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822392"
---
# <span data-ttu-id="8272b-103">Сведения о виртуальных средах</span><span class="sxs-lookup"><span data-stu-id="8272b-103">About Virtual Environments</span></span>


<span data-ttu-id="8272b-104">Виртуальные приложения выполняются в виртуальных средах.</span><span class="sxs-lookup"><span data-stu-id="8272b-104">Virtual applications run in virtual environments.</span></span> <span data-ttu-id="8272b-105">Виртуальные среды позволяют каждому приложению выполняться на настольном компьютере, ноутбуке или хост-сервере сеансов удаленных рабочих столов (RDSession) без установки и изменения операционной системы узла.</span><span class="sxs-lookup"><span data-stu-id="8272b-105">Virtual environments enable each application to run on a desktop, laptop, or Remote Desktop Session Host (RDSession Host) server without installation and alteration of the host operating system.</span></span> <span data-ttu-id="8272b-106">Каждое приложение несет собственные сведения о конфигурации в виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="8272b-106">Each application carries its own configuration information in the virtual environment.</span></span> <span data-ttu-id="8272b-107">В результате многие приложения работают параллельно с другими приложениями на одном компьютере без конфликтов.</span><span class="sxs-lookup"><span data-stu-id="8272b-107">As a result, many applications run side by side with other applications on the same computer without any conflicts.</span></span>

<span data-ttu-id="8272b-108">Виртуальные приложения выполняются локально, поэтому они работают с полной производительностью, функциональностью и доступом к локальным службам, которые вы ожидаете из любого приложения, установленного локально.</span><span class="sxs-lookup"><span data-stu-id="8272b-108">Virtual applications run locally, so they run with the full performance, functionality, and access to local services that you would expect from any application installed locally.</span></span>

<span data-ttu-id="8272b-109">Поскольку каждое приложение запускается в виртуальной среде, уменьшается ряд описанных ниже проблем.</span><span class="sxs-lookup"><span data-stu-id="8272b-109">Because each application runs in a virtual environment, the following problems are reduced:</span></span>

-   <span data-ttu-id="8272b-110">Конфликты приложений — в средах, в которых не используется виртуализация приложений, необходимо тщательно протестировать каждое приложение, чтобы убедиться, что он не мешает другим установленным приложениям.</span><span class="sxs-lookup"><span data-stu-id="8272b-110">Application conflicts—In environments that do not use Application Virtualization, you must thoroughly test every application to ensure that it does not interfere with other installed applications.</span></span>

-   <span data-ttu-id="8272b-111">Тестирование регрессии — так как приложение не изменяет операционную систему, а не подлежащий тестированию регрессия, она исключается.</span><span class="sxs-lookup"><span data-stu-id="8272b-111">Regression testing—Because the application does not change the underlying operating system, lengthy regression testing is eliminated.</span></span>

-   <span data-ttu-id="8272b-112">Несовместимость версий — разные версии одного и того же приложения могут одновременно выполняться на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="8272b-112">Version incompatibilities—Different versions of the same application can run simultaneously on the same computer.</span></span>

-   <span data-ttu-id="8272b-113">Многопользовательский доступ — приложения, которые не работают в многопользовательской среде и, следовательно, не могут работать на узле RDSession, теперь могут выполнять и работать надлежащим образом для нескольких пользователей на одном узле RDSession.</span><span class="sxs-lookup"><span data-stu-id="8272b-113">Multiuser access—Applications that do not run in multiuser mode, and therefore cannot run within an RDSession Host, can now do so and function correctly for multiple users on a single RDSession Host.</span></span>

-   <span data-ttu-id="8272b-114">Проблемы с несколькими тарифами — два экземпляра одного и того же приложения, использующих различные конфигурации, могут работать на одном компьютере в одно и то же время.</span><span class="sxs-lookup"><span data-stu-id="8272b-114">Multitenancy issues—Two instances of the same application that use different configurations can run on the same computer at the same time.</span></span>

-   <span data-ttu-id="8272b-115">Серверная независимая — необходимость в нескольких отдельных фермах серверов исключается.</span><span class="sxs-lookup"><span data-stu-id="8272b-115">Server siloing—The need for many separate server farms is eliminated.</span></span>

<span data-ttu-id="8272b-116">Виртуальные среды включают виртуальный реестр для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="8272b-116">Virtual environments include a virtual registry for each application.</span></span> <span data-ttu-id="8272b-117">Параметры реестра, созданные одним приложением, не отображаются другими приложениями или служебными программами, такими как regedit.</span><span class="sxs-lookup"><span data-stu-id="8272b-117">Registry settings created by one application cannot be seen by other applications or utilities such as Regedit.</span></span> <span data-ttu-id="8272b-118">Вместо того чтобы копировать реестр целиком, виртуальный реестр использует метод *Overlay* .</span><span class="sxs-lookup"><span data-stu-id="8272b-118">Rather than copying the entire registry, the virtual registry uses an *overlay* method.</span></span> <span data-ttu-id="8272b-119">Элементы в реестре клиента могут быть прочитаны приложением, если виртуальная копия этого элемента реестра не включена в виртуальный реестр.</span><span class="sxs-lookup"><span data-stu-id="8272b-119">Items in the client registry can be read by the application as long as a virtual copy of that registry item is not included in the virtual registry.</span></span> <span data-ttu-id="8272b-120">Все записи приложений, записанные в реестр, содержатся в виртуальном реестре.</span><span class="sxs-lookup"><span data-stu-id="8272b-120">All application writes to the registry are contained in the virtual registry.</span></span>

<span data-ttu-id="8272b-121">Виртуальные среды также включают виртуальную файловую систему и другие виртуальные компоненты, в том числе виртуальные и виртуальные COM.</span><span class="sxs-lookup"><span data-stu-id="8272b-121">Virtual environments also include a virtual file system and other virtual components, including virtual services and virtual COM.</span></span>

## <span data-ttu-id="8272b-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8272b-122">Related topics</span></span>


[<span data-ttu-id="8272b-123">Обзор консоли управления клиентом Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8272b-123">Application Virtualization Client Management Console Overview</span></span>](application-virtualization-client-management-console-overview.md)

 

 





