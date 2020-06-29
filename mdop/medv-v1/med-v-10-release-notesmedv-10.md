---
title: Заметки о выпуске MED-V 1.0
description: Заметки о выпуске MED-V 1.0
author: dansimp
ms.assetid: 006a3537-5c5b-43b5-8df8-4bf6ddd3cd2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 683056f768a3d547828996a9b191d58337c21ad6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826592"
---
# <span data-ttu-id="47745-103">Заметки о выпуске MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="47745-103">MED-V 1.0 Release Notes</span></span>


## <span data-ttu-id="47745-104">Известные проблемы с MED-V</span><span class="sxs-lookup"><span data-stu-id="47745-104">Known Issues with MED-V</span></span>


<span data-ttu-id="47745-105">Этот раздел содержит наиболее актуальные сведения об общих проблемах с платформой Microsoft Enterprise Virtualization (MED-V).</span><span class="sxs-lookup"><span data-stu-id="47745-105">This section provides the most up-to-date information about general issues with the Microsoft Enterprise Desktop Virtualization (MED-V) platform.</span></span> <span data-ttu-id="47745-106">Эти проблемы не отображаются в документации на продукт, и в некоторых случаях может привести к противоречию с существующим документом о продукте.</span><span class="sxs-lookup"><span data-stu-id="47745-106">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="47745-107">Если это возможно, эти проблемы будут рассмотрены в более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="47745-107">Whenever possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="47745-108">Загрузка файлов не отслеживается в правилах перенаправления веб-сайта</span><span class="sxs-lookup"><span data-stu-id="47745-108">File downloads do not follow Web redirection rules</span></span>

<span data-ttu-id="47745-109">Загрузка файлов не отслеживает правила перенаправления веб-сайта, заданные в политике рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="47745-109">File downloads do not follow Web redirection rules set in a MED-V workspace policy.</span></span>

### <span data-ttu-id="47745-110">При развертывании окна опубликованного приложения на весь экран он исчезает</span><span class="sxs-lookup"><span data-stu-id="47745-110">When expanding a console-published application window to full screen, it disappears</span></span>

<span data-ttu-id="47745-111">Если развернуть опубликованное консольное приложение (например, cmd.exe) на весь экран в рабочей области MED-V, настроенной в режиме прямой интеграции, окно приложения может исчезнуть или не ответить.</span><span class="sxs-lookup"><span data-stu-id="47745-111">If you expand a console-published application (such as cmd.exe) window to full screen inside a MED-V workspace configured in seamless integration mode, the application window might disappear or not respond.</span></span>

### <span data-ttu-id="47745-112">При работе в режиме полного рабочего стола не сохраняются расположения значков на рабочем столе</span><span class="sxs-lookup"><span data-stu-id="47745-112">When working in full desktop mode, icon locations on the desktop are not saved</span></span>

<span data-ttu-id="47745-113">При работе в режиме полного рабочего стола изменения расположения значков на рабочем столе, заданных вручную, не сохраняются между сеансами рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="47745-113">When working in full desktop mode, manual location changes of icons on the desktop are not saved between MED-V workspace sessions.</span></span>

### <span data-ttu-id="47745-114">Локальное изображение и тестовое изображение с таким же именем не могут существовать в том же домене</span><span class="sxs-lookup"><span data-stu-id="47745-114">A local image and a test image with the same name cannot exist in the same domain</span></span>

<span data-ttu-id="47745-115">Если локальный образ присоединен к домену, а администратор создает новую версию того же образа с тем же именем компьютера, что и у тестового образа, при присоединении тестового образа к домену происходит сбой действия "присоединиться к домену", в результате чего удалено локальное изображение из домена.</span><span class="sxs-lookup"><span data-stu-id="47745-115">If a local image is joined to the domain and the administrator creates a new version of the same image with the same computer name as a test image, when the test image joins the domain, either the join domain action fails or it succeeds and the local image is removed from the domain.</span></span>

### <span data-ttu-id="47745-116">MED-V не поддерживает функции Windows Aero</span><span class="sxs-lookup"><span data-stu-id="47745-116">MED-V does not support Windows Aero features</span></span>

<span data-ttu-id="47745-117">MED-V не поддерживает функции Windows Aero (такие как Aero-эргономичное пролистывание).</span><span class="sxs-lookup"><span data-stu-id="47745-117">MED-V does not support Windows Aero features (such as Aero Flip 3D).</span></span>

### <span data-ttu-id="47745-118">Консоль управления может использоваться только одним пользователем Windows на компьютере.</span><span class="sxs-lookup"><span data-stu-id="47745-118">The management console can be used by only one Windows user per computer</span></span>

<span data-ttu-id="47745-119">Консоль управления MED-V может использоваться только администраторами и пользователем Windows, который установил приложение управления.</span><span class="sxs-lookup"><span data-stu-id="47745-119">The MED-V management console can be used only by administrators and the Windows user who installed the management application.</span></span>

### <span data-ttu-id="47745-120">Служебная программа настройки сервера MED-V проверяет подключение Microsoft SQL Server в контексте пользователя, а не в контекстной службе сервера MED-V</span><span class="sxs-lookup"><span data-stu-id="47745-120">The MED-V Server configuration utility tests Microsoft SQL Server connectivity under user context rather than under MED-V Server service context</span></span>

<span data-ttu-id="47745-121">MED-V использует контекст службы сервера MED-V для сбора отчетов из базы данных отчетов Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="47745-121">MED-V uses MED-V Server service context to collect reports from the Microsoft SQL Server reports database.</span></span> <span data-ttu-id="47745-122">Служебная программа настройки сервера MED-V проверяет базу данных и проверяет строку подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="47745-122">The MED-V Server configuration utility verifies the database and tests the database connection string.</span></span> <span data-ttu-id="47745-123">Она не проверяет доступ к базе данных для службы MED-V Server.</span><span class="sxs-lookup"><span data-stu-id="47745-123">It does not validate the access of MED-V Server service to the database.</span></span>

 

 





