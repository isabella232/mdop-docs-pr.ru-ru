---
title: Справочник по командам SFTMIME
description: Справочник по командам SFTMIME
author: dansimp
ms.assetid: a4a69228-9dd3-4623-b773-899d03c0cf10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 47aac9110febaf3f349461d74fef840326b1c6e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815349"
---
# <span data-ttu-id="3abce-103">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="3abce-103">SFTMIME Command Reference</span></span>


<span data-ttu-id="3abce-104">SFTMIME — это интерфейс командной строки, который используется Application Virtualization (App-V), позволяющим управлять многими сведениями о конфигурации клиента.</span><span class="sxs-lookup"><span data-stu-id="3abce-104">SFTMIME is a command-line interface used by Application Virtualization (App-V) that enables you to manage many client configuration details.</span></span> <span data-ttu-id="3abce-105">Этот раздел включает все команды и их параметры с кратким описанием каждого из них.</span><span class="sxs-lookup"><span data-stu-id="3abce-105">This section contains all the commands and their parameters, with a brief description of each.</span></span>

**<span data-ttu-id="3abce-106">Важно.</span><span class="sxs-lookup"><span data-stu-id="3abce-106">Important</span></span>**  
-   <span data-ttu-id="3abce-107">Все символы обратной косой черты должны быть преобразованы в escape-последовательность с помощью предшествующей обратной косой черты или путь будет проанализирован неправильно.</span><span class="sxs-lookup"><span data-stu-id="3abce-107">All backslash characters must be escaped using a preceding backslash, or the path will not be parsed correctly.</span></span>

-   <span data-ttu-id="3abce-108">Если вы используете вызывающую программу для вызова SFTMIME с помощью **CreateProcess**, необходимо убедиться, что первый параметр — путь к sftmime.exe.</span><span class="sxs-lookup"><span data-stu-id="3abce-108">If you are using a calling program to invoke SFTMIME with **CreateProcess**, you must ensure that the first parameter is the path to sftmime.exe.</span></span>

-   <span data-ttu-id="3abce-109">Вывод команды "SFTMIME **Query** " не может быть передан команде **findstr** для поиска строки.</span><span class="sxs-lookup"><span data-stu-id="3abce-109">The output of the SFTMIME **QUERY OBJ** command cannot be piped to the **findstr** command to search for a string.</span></span>

-   <span data-ttu-id="3abce-110">Для использования **глобального** коммутатора требуются права локального администратора.</span><span class="sxs-lookup"><span data-stu-id="3abce-110">Use of the **GLOBAL** switch requires local administrator rights.</span></span>

-   <span data-ttu-id="3abce-111">Использование коротких путей и относительных путей может привести к неожиданным результатам и следует избегать.</span><span class="sxs-lookup"><span data-stu-id="3abce-111">Use of short paths and relative paths can lead to unexpected results and should be avoided.</span></span> <span data-ttu-id="3abce-112">Всегда используйте полные пути.</span><span class="sxs-lookup"><span data-stu-id="3abce-112">Always use full paths.</span></span>

 

## <span data-ttu-id="3abce-113">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="3abce-113">In This Section</span></span>


[<span data-ttu-id="3abce-114">ADD APP (ДОБАВИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="3abce-114">ADD APP</span></span>](add-app.md)

[<span data-ttu-id="3abce-115">ADD PACKAGE (ДОБАВИТЬ ПАКЕТ)</span><span class="sxs-lookup"><span data-stu-id="3abce-115">ADD PACKAGE</span></span>](add-package.md)

[<span data-ttu-id="3abce-116">ADD SERVER (ДОБАВИТЬ СЕРВЕР)</span><span class="sxs-lookup"><span data-stu-id="3abce-116">ADD SERVER</span></span>](add-server.md)

[<span data-ttu-id="3abce-117">ADD TYPE (ДОБАВИТЬ ТИП)</span><span class="sxs-lookup"><span data-stu-id="3abce-117">ADD TYPE</span></span>](add-type.md)

[<span data-ttu-id="3abce-118">CLEAR APP (ОЧИСТИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="3abce-118">CLEAR APP</span></span>](clear-app.md)

[<span data-ttu-id="3abce-119">CLEAR OBJ (ОЧИСТИТЬ ОБЪЕКТ)</span><span class="sxs-lookup"><span data-stu-id="3abce-119">CLEAR OBJ</span></span>](clear-obj.md)

[<span data-ttu-id="3abce-120">CONFIGURE APP (НАСТРОИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="3abce-120">CONFIGURE APP</span></span>](configure-app.md)

[<span data-ttu-id="3abce-121">CONFIGURE PACKAGE (НАСТРОИТЬ ПАКЕТ)</span><span class="sxs-lookup"><span data-stu-id="3abce-121">CONFIGURE PACKAGE</span></span>](configure-package.md)

[<span data-ttu-id="3abce-122">CONFIGURE SERVER (НАСТРОИТЬ СЕРВЕР)</span><span class="sxs-lookup"><span data-stu-id="3abce-122">CONFIGURE SERVER</span></span>](configure-server.md)

[<span data-ttu-id="3abce-123">CONFIGURE TYPE (НАСТРОИТЬ ТИП)</span><span class="sxs-lookup"><span data-stu-id="3abce-123">CONFIGURE TYPE</span></span>](configure-type.md)

[<span data-ttu-id="3abce-124">DELETE APP (УДАЛИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="3abce-124">DELETE APP</span></span>](delete-app.md)

[<span data-ttu-id="3abce-125">DELETE OBJ (УДАЛИТЬ ОБЪЕКТ)</span><span class="sxs-lookup"><span data-stu-id="3abce-125">DELETE OBJ</span></span>](delete-obj.md)

[<span data-ttu-id="3abce-126">DELETE PACKAGE (УДАЛИТЬ ПАКЕТ)</span><span class="sxs-lookup"><span data-stu-id="3abce-126">DELETE PACKAGE</span></span>](delete-package.md)

[<span data-ttu-id="3abce-127">DELETE SERVER (УДАЛИТЬ СЕРВЕР)</span><span class="sxs-lookup"><span data-stu-id="3abce-127">DELETE SERVER</span></span>](delete-server.md)

[<span data-ttu-id="3abce-128">DELETE TYPE (УДАЛИТЬ ТИП)</span><span class="sxs-lookup"><span data-stu-id="3abce-128">DELETE TYPE</span></span>](delete-type.md)

[<span data-ttu-id="3abce-129">HELP (СПРАВКА)</span><span class="sxs-lookup"><span data-stu-id="3abce-129">HELP</span></span>](help.md)

[<span data-ttu-id="3abce-130">LOAD APP (ЗАГРУЗИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="3abce-130">LOAD APP</span></span>](load-app.md)

[<span data-ttu-id="3abce-131">LOAD PACKAGE (ЗАГРУЗИТЬ ПАКЕТ)</span><span class="sxs-lookup"><span data-stu-id="3abce-131">LOAD PACKAGE</span></span>](load-package.md)

[<span data-ttu-id="3abce-132">LOCK APP (ЗАБЛОКИРОВАТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="3abce-132">LOCK APP</span></span>](lock-app.md)

[<span data-ttu-id="3abce-133">PUBLISH APP (ОПУБЛИКОВАТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="3abce-133">PUBLISH APP</span></span>](publish-app.md)

[<span data-ttu-id="3abce-134">PUBLISH PACKAGE (ОПУБЛИКОВАТЬ ПАКЕТ)</span><span class="sxs-lookup"><span data-stu-id="3abce-134">PUBLISH PACKAGE</span></span>](publish-package.md)

[<span data-ttu-id="3abce-135">QUERY OBJ (ЗАПРОСИТЬ ОБЪЕКТ)</span><span class="sxs-lookup"><span data-stu-id="3abce-135">QUERY OBJ</span></span>](query-obj.md)

[<span data-ttu-id="3abce-136">REFRESH SERVER (ОБНОВИТЬ СЕРВЕР)</span><span class="sxs-lookup"><span data-stu-id="3abce-136">REFRESH SERVER</span></span>](refresh-server.md)

[<span data-ttu-id="3abce-137">REPAIR APP (ВОССТАНОВИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="3abce-137">REPAIR APP</span></span>](repair-app.md)

[<span data-ttu-id="3abce-138">UNLOAD APP (ВЫГРУЗИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="3abce-138">UNLOAD APP</span></span>](unload-app.md)

[<span data-ttu-id="3abce-139">UNLOAD PACKAGE (ВЫГРУЗИТЬ ПАКЕТ)</span><span class="sxs-lookup"><span data-stu-id="3abce-139">UNLOAD PACKAGE</span></span>](unload-package.md)

[<span data-ttu-id="3abce-140">UNLOCK APP (РАЗБЛОКИРОВАТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="3abce-140">UNLOCK APP</span></span>](unlock-app.md)

[<span data-ttu-id="3abce-141">UNPUBLISH PACKAGE (ОТМЕНИТЬ ПУБЛИКАЦИЮ ПАКЕТА)</span><span class="sxs-lookup"><span data-stu-id="3abce-141">UNPUBLISH PACKAGE</span></span>](unpublish-package.md)

 

 





