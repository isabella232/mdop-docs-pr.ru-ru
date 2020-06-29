---
title: Загрузка виртуальных приложений из области уведомлений рабочего стола
description: Загрузка виртуальных приложений из области уведомлений рабочего стола
author: dansimp
ms.assetid: f52758eb-8b81-4b3c-9bc3-adcf7c00c238
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7004f9e0031dfeeedc8b6a916e2f3488f1d31e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817219"
---
# <span data-ttu-id="5955b-103">Загрузка виртуальных приложений из области уведомлений рабочего стола</span><span class="sxs-lookup"><span data-stu-id="5955b-103">How to Load Virtual Applications from the Desktop Notification Area</span></span>


<span data-ttu-id="5955b-104">Если вы являетесь мобильным пользователем, вам может потребоваться полностью загрузить в кэш приложения, чтобы использовать их во время отключенной операции или автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="5955b-104">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="5955b-105">Для потоковой передачи приложений из сервера Application Virtualization (App-V) или серверного потока Application Virtualization (App-V) необходимо подключение к серверу для загрузки приложений.</span><span class="sxs-lookup"><span data-stu-id="5955b-105">To stream applications from the Application Virtualization (App-V) Server or the Application Virtualization (App-V) Streaming Server, you must be connected to a server to load applications.</span></span> <span data-ttu-id="5955b-106">Если вы не подключены к серверу при попытке загрузить приложение, система создаст соответствующее сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5955b-106">If you are not connected to the server when you attempt to load applications, your system will generate an appropriate error message.</span></span> <span data-ttu-id="5955b-107">Кроме того, вы можете выполнять потоковую передачу приложений клиенту из файла или с диска.</span><span class="sxs-lookup"><span data-stu-id="5955b-107">You can also stream applications to the client from a file or disk.</span></span>

<span data-ttu-id="5955b-108">Приложения загружаются по одному приложению за один раз.</span><span class="sxs-lookup"><span data-stu-id="5955b-108">The applications are loaded one application at a time.</span></span> <span data-ttu-id="5955b-109">Индикатор выполнения показывает имя приложения, процент загруженного приложения, а также количество заявлений, которые уже обрабатывались по сравнению с общим количеством приложений, поставленных в очередь.</span><span class="sxs-lookup"><span data-stu-id="5955b-109">The progress bar shows you the application name, the percentage of application loaded, and the number of applications already processed compared to the total number of the applications queued.</span></span> <span data-ttu-id="5955b-110">Вы можете пропустить все выполняемые приложения до загрузки 100%.</span><span class="sxs-lookup"><span data-stu-id="5955b-110">You can skip any application in progress before it is 100% loaded.</span></span> <span data-ttu-id="5955b-111">Вы также можете пропустить загрузку всех остальных приложений.</span><span class="sxs-lookup"><span data-stu-id="5955b-111">You can skip the loading of all remaining applications as well.</span></span>

<span data-ttu-id="5955b-112">**Примечание**  Если при загрузке приложения система обнаружила ошибку, она сообщит об этом.</span><span class="sxs-lookup"><span data-stu-id="5955b-112">**Note** If your system encounters an error while loading an application, it reports the error to you.</span></span> <span data-ttu-id="5955b-113">Вы должны закрыть диалоговое окно ошибки, прежде чем загружать следующее приложение.</span><span class="sxs-lookup"><span data-stu-id="5955b-113">You must dismiss the error dialog before it will load the next application.</span></span>

 

**<span data-ttu-id="5955b-114">Загрузка всех приложений</span><span class="sxs-lookup"><span data-stu-id="5955b-114">To load all applications</span></span>**

1.  <span data-ttu-id="5955b-115">Щелкните правой кнопкой мыши значок системы Application Virtualization в области уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5955b-115">Right-click the Application Virtualization System icon in the notification area.</span></span>

2.  <span data-ttu-id="5955b-116">В раскрывающемся меню выберите пункт **загрузить приложения** .</span><span class="sxs-lookup"><span data-stu-id="5955b-116">Select **Load Applications** from the pop-up menu.</span></span>

**<span data-ttu-id="5955b-117">Пропуск приложений</span><span class="sxs-lookup"><span data-stu-id="5955b-117">To skip applications</span></span>**

1.  <span data-ttu-id="5955b-118">Щелкните индикатор выполнения, чтобы открыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5955b-118">Click the progress bar to display the dialog box.</span></span>

2.  <span data-ttu-id="5955b-119">Чтобы получить нужные результаты, нажмите одну из указанных ниже кнопок.</span><span class="sxs-lookup"><span data-stu-id="5955b-119">Select one of the following buttons to achieve the desired results:</span></span>

    1.  <span data-ttu-id="5955b-120">**Пропустить**— пропустить текущее загруженное приложение.</span><span class="sxs-lookup"><span data-stu-id="5955b-120">**Skip**—To skip the currently loading application.</span></span>

    2.  <span data-ttu-id="5955b-121">**Пропустить все**— пропустить все оставшиеся приложения.</span><span class="sxs-lookup"><span data-stu-id="5955b-121">**Skip All**—To skip all remaining applications.</span></span>

    3.  <span data-ttu-id="5955b-122">**Продолжайте**, чтобы закрыть диалоговое окно и продолжить загрузку приложений.</span><span class="sxs-lookup"><span data-stu-id="5955b-122">**Continue**—To cancel the dialog box and continue loading applications.</span></span>

## <span data-ttu-id="5955b-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5955b-123">Related topics</span></span>


[<span data-ttu-id="5955b-124">Использование области уведомлений рабочего стола для управления клиента Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="5955b-124">How to Use the Desktop Notification Area for Application Virtualization Client Management</span></span>](how-to-use-the-desktop-notification-area-for-application-virtualization-client-management.md)

 

 





