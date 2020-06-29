---
title: Узел "Серверы публикации"
description: Узел "Серверы публикации"
author: dansimp
ms.assetid: b5823c6c-15bc-4e8d-aeeb-acc366ffedd1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c001e246c63919773d29a2317d5a43937c0813f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815799"
---
# <span data-ttu-id="29bdd-103">Узел "Серверы публикации"</span><span class="sxs-lookup"><span data-stu-id="29bdd-103">Publishing Servers Node</span></span>


<span data-ttu-id="29bdd-104">Узел **Серверы публикаций** находится на одном уровне под узлом **Application Virtualization** в области **область** консоли управления клиентом Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="29bdd-104">The **Publishing Servers** node is one level below the **Application Virtualization** node in the **Scope** pane of the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="29bdd-105">При выборе этого узла в области **результатов** отображается список серверов публикации.</span><span class="sxs-lookup"><span data-stu-id="29bdd-105">When you select this node, the **Results** pane displays a list of publishing servers.</span></span>

<span data-ttu-id="29bdd-106">Щелкните правой кнопкой мыши узел **Серверы публикации** , чтобы открыть всплывающее меню, содержащее следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="29bdd-106">Right-click the **Publishing Servers** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-server"></a>**<span data-ttu-id="29bdd-107">Новый сервер</span><span class="sxs-lookup"><span data-stu-id="29bdd-107">New Server</span></span>**  
<span data-ttu-id="29bdd-108">В этом элементе меню отображается мастер создания сервера.</span><span class="sxs-lookup"><span data-stu-id="29bdd-108">This menu item displays the New Server Wizard.</span></span> <span data-ttu-id="29bdd-109">Этот мастер состоит из двух страниц:</span><span class="sxs-lookup"><span data-stu-id="29bdd-109">This wizard consists of two pages:</span></span>

1.  <span data-ttu-id="29bdd-110">Введите отображаемое имя сервера и тип сервера:</span><span class="sxs-lookup"><span data-stu-id="29bdd-110">Enter a server display name and server type:</span></span>

    -   <span data-ttu-id="29bdd-111">**Отображаемое имя**— введите имя, которое будет отображаться для сервера.</span><span class="sxs-lookup"><span data-stu-id="29bdd-111">**Display Name**—Enter a name that you want displayed for the server.</span></span> <span data-ttu-id="29bdd-112">По умолчанию это поле оставлено пустым.</span><span class="sxs-lookup"><span data-stu-id="29bdd-112">This field is blank by default.</span></span>

    -   <span data-ttu-id="29bdd-113">**Тип**: выберите тип сервера в раскрывающемся списке типы серверов.</span><span class="sxs-lookup"><span data-stu-id="29bdd-113">**Type**—Choose the server type from the drop-down list of server types.</span></span>

2.  <span data-ttu-id="29bdd-114">Укажите параметры подключения для сервера.</span><span class="sxs-lookup"><span data-stu-id="29bdd-114">Specify the connection settings for the server:</span></span>

    -   <span data-ttu-id="29bdd-115">**Host Name (имя узла**) — введите имя или IP-адрес сервера.</span><span class="sxs-lookup"><span data-stu-id="29bdd-115">**Host Name**—Enter the name or IP address for the server.</span></span>

    -   <span data-ttu-id="29bdd-116">**Port (порт**) — введите числовое значение, соответствующее номеру порта.</span><span class="sxs-lookup"><span data-stu-id="29bdd-116">**Port**—Enter a numeric value that corresponds to the port number.</span></span> <span data-ttu-id="29bdd-117">Значением по умолчанию является 554, если тип сервера — "сервер Application Virtualization", а 80 — тип сервера "Стандартный HTTP-сервер".</span><span class="sxs-lookup"><span data-stu-id="29bdd-117">The default value is 554 if the server type is "Application Virtualization Server" and 80 if the server type is "Standard HTTP Server."</span></span>

    -   <span data-ttu-id="29bdd-118">**Path (путь**) — это поле по умолчанию имеет значение "/" и доступно только для чтения, если тип сервера — "сервер виртуализации приложений" или "сервер виртуализации приложений для повышенной безопасности".</span><span class="sxs-lookup"><span data-stu-id="29bdd-118">**Path**—This field defaults to "/" and is read-only when the server type is "Application Virtualization Server" or “Enhanced Security Application Virtualization Server”.</span></span> <span data-ttu-id="29bdd-119">Если тип сервера — "Стандартный HTTP-сервер" или "Улучшенный HTTP-сервер", поле " **путь** " также можно редактировать.</span><span class="sxs-lookup"><span data-stu-id="29bdd-119">When the server type is “Standard HTTP Server” or “Enhanced Security HTTP Server”, the **Path** field is also editable.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="29bdd-120">Новое окно</span><span class="sxs-lookup"><span data-stu-id="29bdd-120">New Window from Here</span></span>**  
<span data-ttu-id="29bdd-121">Выберите этот пункт меню, чтобы открыть новую консоль управления с выбранным узлом в качестве корневого узла.</span><span class="sxs-lookup"><span data-stu-id="29bdd-121">Select this menu item to open a new management console with the selected node as the root node.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="29bdd-122">Экспорт списка</span><span class="sxs-lookup"><span data-stu-id="29bdd-122">Export List</span></span>**  
<span data-ttu-id="29bdd-123">С помощью этого элемента меню можно создать текстовый файл с разделителями-знаками табуляции, содержащий содержимое области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="29bdd-123">You can use this menu item to create a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="29bdd-124">Этот элемент отображает диалоговое окно " **Сохранение файла** ", в котором указывается расположение для текстового файла, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="29bdd-124">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="29bdd-125">Просмотр</span><span class="sxs-lookup"><span data-stu-id="29bdd-125">View</span></span>**  
<span data-ttu-id="29bdd-126">Этот всплывающий список элементов меню позволяет изменять внешний вид и содержимое области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="29bdd-126">This pop-up list of menu items enables you to change the appearance and content of the **Results** pane.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="29bdd-127">Обновить</span><span class="sxs-lookup"><span data-stu-id="29bdd-127">Refresh</span></span>**  
<span data-ttu-id="29bdd-128">Выберите этот элемент, чтобы обновить консоль управления.</span><span class="sxs-lookup"><span data-stu-id="29bdd-128">Select this item to refresh the management console.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="29bdd-129">Help</span><span class="sxs-lookup"><span data-stu-id="29bdd-129">Help</span></span>**  
<span data-ttu-id="29bdd-130">Этот элемент отображает справочную систему для консоли управления.</span><span class="sxs-lookup"><span data-stu-id="29bdd-130">This item displays the help system for the management console.</span></span>

## <span data-ttu-id="29bdd-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="29bdd-131">Related topics</span></span>


[<span data-ttu-id="29bdd-132">Область "Результаты: серверы публикации"</span><span class="sxs-lookup"><span data-stu-id="29bdd-132">Publishing Servers Results Pane</span></span>](publishing-servers-results-pane.md)

[<span data-ttu-id="29bdd-133">Столбцы панели "Результаты: серверы публикации"</span><span class="sxs-lookup"><span data-stu-id="29bdd-133">Publishing Servers Results Pane Columns</span></span>](publishing-servers-results-pane-columns.md)

 

 





