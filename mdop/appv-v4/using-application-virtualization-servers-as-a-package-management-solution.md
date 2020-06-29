---
title: Использование серверов Application Virtualization Server в качестве решения по управлению пакетами
description: Использование серверов Application Virtualization Server в качестве решения по управлению пакетами
author: dansimp
ms.assetid: 41597355-e7bb-45e2-b300-7b1724419975
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2b81ed3ab6fa3a70fe4780904059091f22579d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815122"
---
# <span data-ttu-id="dad21-103">Использование серверов Application Virtualization Server в качестве решения по управлению пакетами</span><span class="sxs-lookup"><span data-stu-id="dad21-103">Using Application Virtualization Servers as a Package Management Solution</span></span>


<span data-ttu-id="dad21-104">Если у вас нет существующей системы ESD для развертывания решения Application Virtualization или вы не хотите использовать его, вам потребуется установить один или несколько серверов управления виртуализацией приложений в качестве ядра архитектуры системы.</span><span class="sxs-lookup"><span data-stu-id="dad21-104">If you do not have an existing ESD system to deploy your Application Virtualization solution or do not wish to use one, you will need to install one or more Application Virtualization Management Servers as the core of your system architecture.</span></span> <span data-ttu-id="dad21-105">Для сервера управления Application Virtualization требуется выделенный серверный компьютер и нужна база данных Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dad21-105">The Application Virtualization Management Server requires a dedicated server computer and needs a Microsoft SQL Server database.</span></span> <span data-ttu-id="dad21-106">База данных может находиться на том же сервере или быть настроена на корпоративном сервере базы данных, доступном для сервера управления виртуализацией приложений по высокоскоростному подключению к локальной сети.</span><span class="sxs-lookup"><span data-stu-id="dad21-106">The database can be on the same server, or it can be configured on a corporate database server that is accessible to the Application Virtualization Management Server over a high-speed LAN connection.</span></span> <span data-ttu-id="dad21-107">Кроме того, вам потребуется установить консоль управления виртуализации приложений (Майкрософт) либо на сервере управления виртуализацией приложений, либо на назначенной рабочей станции управления, и вам потребуется установить веб-службу Microsoft Application Virtualization, которая также может быть установлена на сервере управления виртуализацией приложений или на отдельном сервере IIS.</span><span class="sxs-lookup"><span data-stu-id="dad21-107">In addition, you will need to install the Microsoft Application Virtualization Management Console, on either the Application Virtualization Management Server or on a designated management workstation, and you will need to install the Microsoft Application Virtualization Management Web Service, which can also be installed on the Application Virtualization Management Server or on a separate IIS server.</span></span> <span data-ttu-id="dad21-108">Консоль управления виртуализацией приложений используется для подключения к веб-службе управления виртуализацией приложений, что позволяет системному администратору взаимодействовать с сервером управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="dad21-108">The Application Virtualization Management Console is used to connect to the Application Virtualization Management Web Service, enabling the system administrator to interact with the Application Virtualization Management Server.</span></span>

<span data-ttu-id="dad21-109">**Примечание**  Управление доступом к приложениям осуществляется с помощью групп безопасности доменных служб Active Directory, поэтому вам потребуется планировать процесс настройки группы безопасности для каждого виртуализированного приложения и для управления добавлением пользователей в каждую группу.</span><span class="sxs-lookup"><span data-stu-id="dad21-109">**Note** Access to the applications is controlled by means of Security Groups in Active Directory Domain Services, so you will need to plan a process to set up a security group for each virtualized application and for managing which users are added to each group.</span></span> <span data-ttu-id="dad21-110">Администратор сервера управления виртуализацией приложений настраивает сервер для использования этих групп Active Directory, а затем сервер автоматически контролирует доступ к пакетам на основе членства в группе Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dad21-110">The Application Virtualization Management Server administrator configures the server to use these Active Directory groups, and the server then automatically controls access to the packages based on Active Directory group membership.</span></span>

 

## <span data-ttu-id="dad21-111">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="dad21-111">In This Section</span></span>


<a href="" id="overview-of-the-application-virtualization-system-components"></a>[<span data-ttu-id="dad21-112">Обзор компонентов системы Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="dad21-112">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)  
<span data-ttu-id="dad21-113">Список и описание основных компонентов системы управления виртуализацией приложений Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dad21-113">Lists and describes the primary components of the Microsoft Application Virtualization Management System.</span></span>

<a href="" id="publishing-virtual-applications-using-application-virtualization-management-servers"></a>[<span data-ttu-id="dad21-114">Публикация виртуальных приложений с помощью серверов Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="dad21-114">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)  
<span data-ttu-id="dad21-115">В этом кратком обзоре описаны способы публикации виртуальных приложений в сценарии развертывания на основе сервера Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="dad21-115">Provides a brief overview of how virtual applications are published in an Application Virtualization Server-based deployment scenario.</span></span>

<a href="" id="planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation"></a>[<span data-ttu-id="dad21-116">Планирование решения для потоковой передачи при внедрении на основе сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="dad21-116">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)  
<span data-ttu-id="dad21-117">В этой статье описаны доступные параметры для использования серверных потоков виртуализации приложений вместе с реализацией на основе сервера управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="dad21-117">Describes available options for using Application Virtualization Streaming Servers in conjunction with your Application Virtualization Management Server-based implementation.</span></span>

## <span data-ttu-id="dad21-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="dad21-118">Related topics</span></span>


[<span data-ttu-id="dad21-119">Сценарий на основе использования сервера Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="dad21-119">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="dad21-120">Планирование развертывания системы виртуализации приложений</span><span class="sxs-lookup"><span data-stu-id="dad21-120">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





