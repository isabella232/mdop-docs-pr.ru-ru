---
title: Управление лицензиями приложений на консоли управления серверами
description: Управление лицензиями приложений на консоли управления серверами
author: dansimp
ms.assetid: 48503b04-0de7-48de-98ee-4623a712a341
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ca9ab54c8b4cee06e0b17d8b5dee3d3ca7ce69c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817222"
---
# <span data-ttu-id="b08a1-103">Управление лицензиями приложений на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="b08a1-103">How to Manage Application Licenses in the Server Management Console</span></span>


<span data-ttu-id="b08a1-104">Консоль управления сервером виртуализации приложений — это интерфейс, с помощью которого можно управлять платформой Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="b08a1-104">The Application Virtualization Server Management Console is the interface you use to manage the Application Virtualization platform.</span></span> <span data-ttu-id="b08a1-105">Из него можно добавлять, удалять, настраивать группы лицензий приложений и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="b08a1-105">From it, you can add, remove, configure, and control application license groups.</span></span>

<span data-ttu-id="b08a1-106">**Важно!**  Если параметр "источник (ASR)" клиентского приложения App-V настроен на использование любого типа потоковой передачи, отличного от сервера управления (например, потокового сервера, сервера IIS или файлового сервера), то сервер управления не может применить политику лицензирования.</span><span class="sxs-lookup"><span data-stu-id="b08a1-106">**Important** If the App-V client Application Source Root (ASR) setting is configured to use any type of streaming source other than the Management Server, for example a Streaming Server, an IIS server, or a File server, then the Management Server is unable to enforce its licensing policy.</span></span>

 

## <span data-ttu-id="b08a1-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="b08a1-107">In This Section</span></span>


<a href="" id="how-to-create-an-application-license-group"></a>[<span data-ttu-id="b08a1-108">Создание группы лицензий приложений</span><span class="sxs-lookup"><span data-stu-id="b08a1-108">How to Create an Application License Group</span></span>](how-to-create-an-application-license-group.md)  
<span data-ttu-id="b08a1-109">В этой процедуре описывается создание нового приложения в лицензионной группе.</span><span class="sxs-lookup"><span data-stu-id="b08a1-109">Provides a procedure for creating a new application in a license group.</span></span>

<a href="" id="how-to-associate-an-application-with-a-license-group"></a>[<span data-ttu-id="b08a1-110">Связывание приложения с группой лицензий</span><span class="sxs-lookup"><span data-stu-id="b08a1-110">How to Associate an Application with a License Group</span></span>](how-to-associate-an-application-with-a-license-group.md)  
<span data-ttu-id="b08a1-111">Приводятся инструкции по добавлению приложения в лицензионную группу.</span><span class="sxs-lookup"><span data-stu-id="b08a1-111">Provides a procedure for adding an application to a license group.</span></span>

<a href="" id="how-to-remove-an-application-from-a-license-group"></a>[<span data-ttu-id="b08a1-112">Удаление приложения из группы лицензий</span><span class="sxs-lookup"><span data-stu-id="b08a1-112">How to Remove an Application from a License Group</span></span>](how-to-remove-an-application-from-a-license-group.md)  
<span data-ttu-id="b08a1-113">Описание процедуры удаления приложения из лицензионной группы.</span><span class="sxs-lookup"><span data-stu-id="b08a1-113">Provides a procedure for removing an application from a license group.</span></span>

<a href="" id="how-to-remove-an-application-license-group"></a>[<span data-ttu-id="b08a1-114">Удаление группы лицензий приложений</span><span class="sxs-lookup"><span data-stu-id="b08a1-114">How to Remove an Application License Group</span></span>](how-to-remove-an-application-license-group.md)  
<span data-ttu-id="b08a1-115">Этот раздел содержит инструкции, необходимые для удаления группы лицензий приложения.</span><span class="sxs-lookup"><span data-stu-id="b08a1-115">This section includes the steps necessary to delete an application license group.</span></span>

<a href="" id="how-to-set-up-an-unlimited-license-group"></a>[<span data-ttu-id="b08a1-116">Установка группы неограниченных лицензий</span><span class="sxs-lookup"><span data-stu-id="b08a1-116">How to Set Up an Unlimited License Group</span></span>](how-to-set-up-an-unlimited-license-group.md)  
<span data-ttu-id="b08a1-117">В этой процедуре описана процедура создания новой неограниченной лицензионной группы, позволяющая неограниченному количеству пользователей получить доступ к приложениям в группе.</span><span class="sxs-lookup"><span data-stu-id="b08a1-117">Provides a procedure for creating a new unlimited license group, allowing an unlimited number of users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-concurrent-license-group"></a>[<span data-ttu-id="b08a1-118">Установка группы параллельных лицензий</span><span class="sxs-lookup"><span data-stu-id="b08a1-118">How to Set Up a Concurrent License Group</span></span>](how-to-set-up-a-concurrent-license-group.md)  
<span data-ttu-id="b08a1-119">В этой процедуре описана процедура создания новой параллельной группы лицензий, позволяющая определенному числу параллельных пользователей получать доступ к приложениям в группе.</span><span class="sxs-lookup"><span data-stu-id="b08a1-119">Provides a procedure for creating a new concurrent license group, allowing a specific number of concurrent users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-named-license-group"></a>[<span data-ttu-id="b08a1-120">Установка группы именованных лицензий</span><span class="sxs-lookup"><span data-stu-id="b08a1-120">How to Set Up a Named License Group</span></span>](how-to-set-up-a-named-license-group.md)  
<span data-ttu-id="b08a1-121">Инструкции по созданию новой неограниченной лицензионной группы, позволяющей определенным пользователям получать доступ к приложениям в группе.</span><span class="sxs-lookup"><span data-stu-id="b08a1-121">Provides a procedure for creating a new unlimited license group, allowing specific users to access the applications in the group.</span></span>

## <span data-ttu-id="b08a1-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b08a1-122">Related topics</span></span>


[<span data-ttu-id="b08a1-123">Выполнение задач администрирования на консоли управления серверами Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="b08a1-123">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





