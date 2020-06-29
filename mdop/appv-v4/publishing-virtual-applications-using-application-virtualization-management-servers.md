---
title: Публикация виртуальных приложений с помощью серверов Application Virtualization Management Server
description: Публикация виртуальных приложений с помощью серверов Application Virtualization Management Server
author: dansimp
ms.assetid: f3d79284-3f82-4ca3-b741-1a80b61490da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01b85d73ed0a6a8bf723be381e947fbbc003bf6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815769"
---
# <span data-ttu-id="5a075-103">Публикация виртуальных приложений с помощью серверов Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="5a075-103">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>


<span data-ttu-id="5a075-104">В развертывании на базе сервера Application Virtualization пакеты виртуальных приложений, которые были последовательно, проверены и обнаружены, будут скопированы в основную доступную для использования сервер управления Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="5a075-104">In an Application Virtualization Server-based deployment, virtual application packages that have been sequenced, tested, and found deployable are copied to the main CONTENT share to be used by the Application Virtualization Management Server.</span></span> <span data-ttu-id="5a075-105">После импорта пакетов на сервер управления Application Virtualization они могут быть опубликованы для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="5a075-105">After the packages are imported on the Application Virtualization Management Server, they can be published to the end users.</span></span>

<span data-ttu-id="5a075-106">**Примечание**  Общий доступ к КОНТЕНТу должен находиться на дисках, подключенных к серверу.</span><span class="sxs-lookup"><span data-stu-id="5a075-106">**Note** The CONTENT share should be located on the server’s attached disk storage.</span></span> <span data-ttu-id="5a075-107">Использование сетевого запоминающего устройства, такого как сеть хранения данных или общий доступ к распределенной файловой сети DFS, должно быть тщательно рассмотрено из-за воздействия на сеть.</span><span class="sxs-lookup"><span data-stu-id="5a075-107">Using a network storage device such as a SAN or a DFS share should be considered carefully because of the network impact.</span></span>

 

<span data-ttu-id="5a075-108">Приложения загружаются в группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5a075-108">Applications are provisioned to Active Directory groups.</span></span> <span data-ttu-id="5a075-109">Обычно администратор Application Virtualization создает группы Active Directory для каждого виртуального приложения, которые нужно опубликовать, а затем добавляет в них соответствующих пользователей.</span><span class="sxs-lookup"><span data-stu-id="5a075-109">Typically, the Application Virtualization administrator will create Active Directory groups for each virtual application to be published and then add the appropriate users to those groups.</span></span> <span data-ttu-id="5a075-110">Когда пользователи выполняют вход на рабочие станции, клиент Application Virtualization по умолчанию выполняет обновление публикации с использованием учетных данных пользователя, выполнившего вход.</span><span class="sxs-lookup"><span data-stu-id="5a075-110">When the users log on to their workstations, the Application Virtualization Client, by default, performs a publishing refresh using the credentials of the logged on user.</span></span> <span data-ttu-id="5a075-111">После этого пользователь сможет запускать приложения из любой точки, куда вы находились сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="5a075-111">The user can then start applications from wherever the shortcuts have been placed.</span></span> <span data-ttu-id="5a075-112">Администратор Application Virtualization определяет, где и сколько сочетаний клавиш находится на клиентском компьютере во время последовательного выполнения приложения.</span><span class="sxs-lookup"><span data-stu-id="5a075-112">The Application Virtualization administrator determines where and how many shortcuts are located on the client system during the sequencing of the application.</span></span>

<span data-ttu-id="5a075-113">**Примечание**  *Обновление публикации* — это звонок на сервер Application Virtualization, который определен в клиенте Application Virtualization, чтобы определить, какие из виртуальных приложений отправляются клиенту для использования конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="5a075-113">**Note** A *publishing refresh* is a call to the Application Virtualization Server that is defined on the Application Virtualization Client, to determine which virtual application shortcuts are sent to the client for use by the end user.</span></span>

 

## <span data-ttu-id="5a075-114">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5a075-114">Related topics</span></span>


[<span data-ttu-id="5a075-115">Сценарий на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="5a075-115">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="5a075-116">Публикация виртуального приложения на клиенте</span><span class="sxs-lookup"><span data-stu-id="5a075-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="5a075-117">Обзор компонентов системы Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="5a075-117">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="5a075-118">Планирование решения для потоковой передачи при внедрении на основе сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="5a075-118">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

 

 





