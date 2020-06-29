---
title: Сведения о приложениях Application Virtualization
description: Сведения о приложениях Application Virtualization
author: dansimp
ms.assetid: 3bf833b7-d172-4eef-a9e8-4b4f0c7eb15b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4eeea7a0ec4454aefcdde5196ae15ed029da45b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820089"
---
# <span data-ttu-id="9d772-103">Сведения о приложениях Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="9d772-103">About Application Virtualization Applications</span></span>


<span data-ttu-id="9d772-104">В Application Virtualization *приложение* — это исполняемая программа, например Microsoft Visio, которая передается на клиентское приложение Application Virtualization или клиент для служб удаленных рабочих столов (прежнее название — службы терминалов) с сервера управления виртуализацией приложений.</span><span class="sxs-lookup"><span data-stu-id="9d772-104">In Application Virtualization, an *application* is an executable program, such as Microsoft Visio, that is streamed to the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) from an Application Virtualization Management Server.</span></span> <span data-ttu-id="9d772-105">Перед тем, как приложение будет передаваться клиенту, оно должно быть подготовлено для потоковой передачи, обрабатывая его с помощью Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="9d772-105">Before an application can be streamed to a client, the application must be prepared for streaming by processing it with the Application Virtualization Sequencer.</span></span>

## <span data-ttu-id="9d772-106">Управление приложениями</span><span class="sxs-lookup"><span data-stu-id="9d772-106">Managing Applications</span></span>


<span data-ttu-id="9d772-107">Прежде чем вы сможете сделать приложения доступными для пользователей, вы должны добавить в систему приложения.</span><span class="sxs-lookup"><span data-stu-id="9d772-107">You must add applications to the system before you can make the applications available to users.</span></span> <span data-ttu-id="9d772-108">Наиболее распространенный способ добавления приложений в систему — это импорт.</span><span class="sxs-lookup"><span data-stu-id="9d772-108">The most common method for adding applications to the system is to import them.</span></span> <span data-ttu-id="9d772-109">Чтобы получить доступ к этой функции, щелкните правой кнопкой мыши узел **приложения** в консоли управления сервером виртуализации приложений и выберите команду **Импорт приложений**.</span><span class="sxs-lookup"><span data-stu-id="9d772-109">To access this feature, right-click the **Applications** node in the Application Virtualization Server Management Console and choose **Import Applications**.</span></span>

<span data-ttu-id="9d772-110">Вы можете импортировать более одного файла программного дескриптора (OSD) одновременно или импортировать файл проекта секвенсора (SPRJ), который может содержать несколько файлов OSD.</span><span class="sxs-lookup"><span data-stu-id="9d772-110">You can import more than one Open Software Descriptor (OSD) file at the same time, or you can import a Sequencer Project file (SPRJ) that can contain multiple OSD files.</span></span> <span data-ttu-id="9d772-111">Эта функция позволяет настраивать связанные приложения аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="9d772-111">This functionality enables you to configure related applications similarly.</span></span>

<span data-ttu-id="9d772-112">Вы также можете использовать следующие функции для управления приложениями:</span><span class="sxs-lookup"><span data-stu-id="9d772-112">You can also use the following features to help you manage your applications:</span></span>

-   <span data-ttu-id="9d772-113">**Группы приложений**— позволяет создавать логические группы приложений для упрощения управления.</span><span class="sxs-lookup"><span data-stu-id="9d772-113">**Application Groups**—Enables you to create logical groups of applications for simplified management.</span></span> <span data-ttu-id="9d772-114">При внесении изменений в группу (например, разрешения на доступ) изменения применяются ко всем приложениям в группе.</span><span class="sxs-lookup"><span data-stu-id="9d772-114">When changes are made to a group (for example, access permissions), the changes are applied to all applications in the group.</span></span> <span data-ttu-id="9d772-115">Приложения в группе могут поступать из разных пакетов.</span><span class="sxs-lookup"><span data-stu-id="9d772-115">Applications in a group can come from different packages.</span></span>

-   <span data-ttu-id="9d772-116">**Множественный выбор**— позволяет выбрать сразу несколько приложений, удерживая нажатой клавишу CTRL при щелчке приложения, чтобы изменить свойства приложения.</span><span class="sxs-lookup"><span data-stu-id="9d772-116">**Multi Select**—Enables you to select multiple applications at once by holding the CTRL key when you click an application to modify the application properties.</span></span> <span data-ttu-id="9d772-117">Тем не менее, если вы хотите обеспечить связь между приложениями, нужно создать группу приложения для хранения приложений.</span><span class="sxs-lookup"><span data-stu-id="9d772-117">However, if you want to maintain a relationship between the applications, you should create an application group to hold the applications.</span></span>

-   <span data-ttu-id="9d772-118">**Перекрестное копирование системы**— позволяет копировать приложения из одной среды в другую для одной и той же версии App-V за один шаг.</span><span class="sxs-lookup"><span data-stu-id="9d772-118">**Cross System Copy**—Enables you to copy applications from one environment to another environment that is running the same version of App-V in one step.</span></span> <span data-ttu-id="9d772-119">Например, у вас может быть пользовательская среда тестирования приема, в которой первоначально развертываются и настраиваются приложения.</span><span class="sxs-lookup"><span data-stu-id="9d772-119">For example, you might have a user acceptance test environment where you initially deploy and configure applications.</span></span> <span data-ttu-id="9d772-120">После того как вы завершите этап тестирования, возможно, потребуется реплицировать тот же набор приложений (включая разрешения) в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="9d772-120">After you finish your testing phase, you might want to replicate the same set of applications (including permissions) to the production environment.</span></span>

## <span data-ttu-id="9d772-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9d772-121">Related topics</span></span>


[<span data-ttu-id="9d772-122">Сведения о пакетах Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="9d772-122">About Application Virtualization Packages</span></span>](about-application-virtualization-packages.md)

[<span data-ttu-id="9d772-123">Сведения о консоли управления серверами Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="9d772-123">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="9d772-124">Управление группами приложений на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="9d772-124">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="9d772-125">Управление приложениями на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="9d772-125">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





