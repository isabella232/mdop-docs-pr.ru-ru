---
title: Работа в автономном или интерактивном режиме с помощью системы Application Virtualization
description: Работа в автономном или интерактивном режиме с помощью системы Application Virtualization
author: dansimp
ms.assetid: aa532b37-8a00-4db4-9b51-e1e8354b2495
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0dfdd315fe607156135247c4a34d0248ef8fbdd9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816379"
---
# <span data-ttu-id="c5128-103">Работа в автономном или интерактивном режиме с помощью системы Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="c5128-103">How to Work Offline or Online with Application Virtualization</span></span>


<span data-ttu-id="c5128-104">Если вы планируете отключиться от сети в течение длительного периода времени, вы можете работать в автономном режиме, чтобы устранить возможные задержки при попытке клиента Application Virtualization взаимодействовать с сервером.</span><span class="sxs-lookup"><span data-stu-id="c5128-104">If you plan to be disconnected from the network for an extended period of time, you can work in offline mode to eliminate possible delays when the Application Virtualization client attempts to communicate with the server.</span></span> <span data-ttu-id="c5128-105">В автономном режиме клиент Application Virtualization не будет пытаться взаимодействовать с сервером публикаций, поэтому приложения должны быть полностью кэшированы перед включением автономного режима.</span><span class="sxs-lookup"><span data-stu-id="c5128-105">In offline mode, the Application Virtualization client will not attempt to communicate with the publishing server, so applications must be fully cached before enabling offline mode.</span></span> <span data-ttu-id="c5128-106">Приложения не будут извлекаться из общего доступа к контенту, даже если они находятся на локальном диске компьютера.</span><span class="sxs-lookup"><span data-stu-id="c5128-106">Applications will not be retrieved from the content share even if they are on the local disk on the computer.</span></span> <span data-ttu-id="c5128-107">Вы можете использовать следующую процедуру клиента Application Virtualization для переключения между автономным и интерактивным режимом работы.</span><span class="sxs-lookup"><span data-stu-id="c5128-107">You can use the following Application Virtualization Client procedure to toggle between working offline and online.</span></span>

<span data-ttu-id="c5128-108">**Примечание**  По умолчанию **Автономная работа** отключена для клиента служб удаленных рабочих столов (ранее служб терминалов).</span><span class="sxs-lookup"><span data-stu-id="c5128-108">**Note** By default, **Work Offline** is disabled for the Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="c5128-109">Системный администратор должен изменить разрешения пользователя, чтобы разрешить использование этого параметра на клиенте для служб удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c5128-109">Your system administrator must change your user permissions to allow you to use this setting on a Client for Remote Desktop Services.</span></span>

 

**<span data-ttu-id="c5128-110">Работа в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="c5128-110">To work offline</span></span>**

-   <span data-ttu-id="c5128-111">Щелкните правой кнопкой мыши значок системы Application Virtualization в области уведомлений и выберите в контекстном меню команду **Автономная работа** .</span><span class="sxs-lookup"><span data-stu-id="c5128-111">Right-click the Application Virtualization System icon in the notification area, and select **Work Offline** from the pop-up menu.</span></span>

**<span data-ttu-id="c5128-112">Работа в сети</span><span class="sxs-lookup"><span data-stu-id="c5128-112">To work online</span></span>**

-   <span data-ttu-id="c5128-113">Щелкните правой кнопкой мыши значок системы Application Virtualization в области уведомлений и выберите в контекстном меню пункт **работать в сети** .</span><span class="sxs-lookup"><span data-stu-id="c5128-113">Right-click the Application Virtualization System icon in the notification area, and select **Work Online** from the pop-up menu.</span></span>

## <span data-ttu-id="c5128-114">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c5128-114">Related topics</span></span>


[<span data-ttu-id="c5128-115">Использование области уведомлений рабочего стола для управления клиента Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="c5128-115">How to Use the Desktop Notification Area for Application Virtualization Client Management</span></span>](how-to-use-the-desktop-notification-area-for-application-virtualization-client-management.md)

 

 





