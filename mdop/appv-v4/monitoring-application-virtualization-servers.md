---
title: Мониторинг серверов Application Virtualization Server
description: Мониторинг серверов Application Virtualization Server
author: dansimp
ms.assetid: d84355ae-4fe4-41d9-ac3a-3eaa32d9a61f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a53c0c37ca609c701727a7f4e18019a9f20110ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816142"
---
# <span data-ttu-id="3ed72-103">Мониторинг серверов Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="3ed72-103">Monitoring Application Virtualization Servers</span></span>


<span data-ttu-id="3ed72-104">Для упрощения управления сервером Application Virtualization (App-V) можно использовать System Center Operations Management Pack Manager2007.</span><span class="sxs-lookup"><span data-stu-id="3ed72-104">To simplify Application Virtualization (App-V) Server management, you can use the System Center Operations Manager2007 Management Pack.</span></span> <span data-ttu-id="3ed72-105">Этот пакет управления поддерживает только серверы Application Virtualization (App-V) 4,5; предыдущие версии сервера не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="3ed72-105">This Management Pack supports only Application Virtualization (App-V) 4.5 servers; it does not support previous server versions.</span></span> <span data-ttu-id="3ed72-106">Пакет управления повышает доступность сервера App-V для обработки запросов клиентов App-V.</span><span class="sxs-lookup"><span data-stu-id="3ed72-106">The Management Pack maximizes App-V Server availability for handling App-V Client requests.</span></span>

## <span data-ttu-id="3ed72-107">Индикаторы состояния</span><span class="sxs-lookup"><span data-stu-id="3ed72-107">Status Indicators</span></span>


<span data-ttu-id="3ed72-108">Индикаторы состояния работоспособности сервера App-V запрограммированы цветом.</span><span class="sxs-lookup"><span data-stu-id="3ed72-108">The App-V Server health status indicators are color-coded.</span></span> <span data-ttu-id="3ed72-109">Цвета представляют следующие значения состояния:</span><span class="sxs-lookup"><span data-stu-id="3ed72-109">The colors represent the following status values:</span></span>

-   <span data-ttu-id="3ed72-110">Нет цвета указывает на то, что сервер запущен без ошибок, которые не могут быть восстановлены.</span><span class="sxs-lookup"><span data-stu-id="3ed72-110">No color indicates that the server is running without non-recoverable errors.</span></span>

-   <span data-ttu-id="3ed72-111">Желтый цвет указывает на то, что один из компонентов не работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="3ed72-111">Yellow indicates that one of the components is not functioning correctly.</span></span> <span data-ttu-id="3ed72-112">Общая функциональность сервера снижена, но сервер по-прежнему доступен.</span><span class="sxs-lookup"><span data-stu-id="3ed72-112">The overall functionality of the server is degraded, but the server is still available.</span></span>

-   <span data-ttu-id="3ed72-113">Красный указывает на то, что сервер недоступен и не может предоставлять ключевые службы или взаимодействовать с внешними зависимостями служб.</span><span class="sxs-lookup"><span data-stu-id="3ed72-113">Red indicates that the server is not available and that it cannot provide key services or communicate with external service dependencies.</span></span>

## <span data-ttu-id="3ed72-114">Условия наблюдения</span><span class="sxs-lookup"><span data-stu-id="3ed72-114">Monitoring Criteria</span></span>


<span data-ttu-id="3ed72-115">Пакет управления наблюдает за следующими аспектами работоспособности сервера:</span><span class="sxs-lookup"><span data-stu-id="3ed72-115">The Management Pack monitors the following aspects of server health:</span></span>

-   <span data-ttu-id="3ed72-116">Состояние сервера — наблюдает за событиями сервера, чтобы убедиться в том, что сервер предоставляет ожидаемые службы.</span><span class="sxs-lookup"><span data-stu-id="3ed72-116">Server Status—monitors server events to validate that the server is providing its expected services.</span></span>

-   <span data-ttu-id="3ed72-117">Доступ к хранилищу данных — отслеживает возможность одного или нескольких серверов управления App-V для доступа к хранилищу данных App-V и взаимодействия с ним.</span><span class="sxs-lookup"><span data-stu-id="3ed72-117">Data Store Access—tracks the ability of one or more of the App-V Management Servers to access and communicate with the App-V data store.</span></span>

-   <span data-ttu-id="3ed72-118">Доступ к данным содержимого — отслеживает доступ к каталогу \\Content, который может представлять собой локальный каталог или сетевую папку, а также возможность чтения запрашиваемых файлов.</span><span class="sxs-lookup"><span data-stu-id="3ed72-118">Content Data Access—monitors access to the \\Content directory, which might be a local directory or a network share, and the ability to read the requested files.</span></span>

-   <span data-ttu-id="3ed72-119">Security (безопасность) — сообщает об ошибках с сертификатом сервера App-V и безопасной связью.</span><span class="sxs-lookup"><span data-stu-id="3ed72-119">Security—reports errors with the App-V Server’s certificate and secure communications.</span></span>

-   <span data-ttu-id="3ed72-120">Обработка запросов клиентов — отслеживает способность одного или нескольких серверов App-V обрабатывать и правильно отвечать на запросы клиентов.</span><span class="sxs-lookup"><span data-stu-id="3ed72-120">Client Request Handling—monitors the ability of one or more of the App-V Servers to handle and correctly respond to client requests.</span></span> <span data-ttu-id="3ed72-121">Эти запросы включают публикацию таких элементов, как запросы на настройку, запросы на загрузку пакетов и запросы на непоследовательность.</span><span class="sxs-lookup"><span data-stu-id="3ed72-121">These requests include publishing such items as configuration requests, package load requests, and out of sequence requests.</span></span>

-   <span data-ttu-id="3ed72-122">Конфигурация сервера — проверяет параметры конфигурации сервера App-V.</span><span class="sxs-lookup"><span data-stu-id="3ed72-122">Server Configuration—checks the configuration settings of the App-V Server.</span></span> <span data-ttu-id="3ed72-123">Эти параметры конфигурации включают параметры в реестре и в хранилище данных App-V.</span><span class="sxs-lookup"><span data-stu-id="3ed72-123">These configuration settings include the settings in the registry and in the App-V data store.</span></span>

## <span data-ttu-id="3ed72-124">Различия на сервере</span><span class="sxs-lookup"><span data-stu-id="3ed72-124">Server Differences</span></span>


<span data-ttu-id="3ed72-125">Ниже приведены основные различия между сервером управления App-V и потоком потокового сервера App-V.</span><span class="sxs-lookup"><span data-stu-id="3ed72-125">The main differences between the App-V Management Server and the App-V Streaming Server are as follows:</span></span>

-   <span data-ttu-id="3ed72-126">Серверы управления App-V могут поддерживать публикацию, потоковую передачу, управление и службы отчетов.</span><span class="sxs-lookup"><span data-stu-id="3ed72-126">App-V Management Servers can provide publishing, streaming, management, and reporting services.</span></span> <span data-ttu-id="3ed72-127">Таким образом, пакет управления может управлять дополнительными аспектами сервера управления App-V, чем он может управлять на потоковый сервер App-V, который предоставляет только потоковую передачу пакетов.</span><span class="sxs-lookup"><span data-stu-id="3ed72-127">Therefore, the Management Pack can manage more aspects of the App-V Management Server than it can manage on the App-V Streaming Server, which provides only package streaming.</span></span>

-   <span data-ttu-id="3ed72-128">Потоковый сервер App-V не имеет хранилища данных App-V, поэтому доступ к хранилищу данных не отслеживается.</span><span class="sxs-lookup"><span data-stu-id="3ed72-128">The App-V Streaming Server does not have an App-V data store, so data store access is not monitored.</span></span> <span data-ttu-id="3ed72-129">Сведения о конфигурации для потокового сервера App-V управляются в реестре.</span><span class="sxs-lookup"><span data-stu-id="3ed72-129">The configuration information for the App-V Streaming Server is managed in the registry.</span></span>

-   <span data-ttu-id="3ed72-130">Потоковый сервер App-V не использует интерфейс консоли управления App-V Server; Используйте другие инструменты для управления конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="3ed72-130">The App-V Streaming Server does not use the App-V Server Management Console interface; use other tools to manage the configuration.</span></span>

## <span data-ttu-id="3ed72-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3ed72-131">Related topics</span></span>


[<span data-ttu-id="3ed72-132">Сервер Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="3ed72-132">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





