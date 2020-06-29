---
title: Публикация пакета с помощью консоли управления
description: Публикация пакета с помощью консоли управления
author: dansimp
ms.assetid: e34d2bcf-15ac-4a75-9dc8-79380b36a25f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b0783a05f658da5e93603e26dc7e9581d26b81f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813768"
---
# <span data-ttu-id="3fd4a-103">Публикация пакета с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="3fd4a-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="3fd4a-104">Чтобы опубликовать пакет App-V 5,1, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3fd4a-104">Use the following procedure to publish an App-V 5.1 package.</span></span> <span data-ttu-id="3fd4a-105">После публикации пакета компьютеры, на которых работает клиент App-V 5,1, смогут получать доступ к приложениям в этом пакете и запускать их.</span><span class="sxs-lookup"><span data-stu-id="3fd4a-105">Once you publish a package, computers that are running the App-V 5.1 client can access and run the applications in that package.</span></span>

<span data-ttu-id="3fd4a-106">**Примечание**  Возможность разрешения только администраторам публиковать и отменять публикацию пакетов (описанных ниже) поддерживается начиная с версии App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3fd4a-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="3fd4a-107">Публикация пакета App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="3fd4a-107">To publish an App-V 5.1 package</span></span>**

1.  <span data-ttu-id="3fd4a-108">В консоли управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3fd4a-108">In the App-V 5.1 Management console.</span></span> <span data-ttu-id="3fd4a-109">Щелкните или щелкните правой кнопкой мыши имя пакета, который нужно опубликовать.</span><span class="sxs-lookup"><span data-stu-id="3fd4a-109">Click or right-click the name of the package to be published.</span></span> <span data-ttu-id="3fd4a-110">Нажмите кнопку **опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="3fd4a-110">Select **Publish**.</span></span>

2.  <span data-ttu-id="3fd4a-111">Просмотрите столбец **состояние** , чтобы убедиться, что пакет опубликован и теперь доступен.</span><span class="sxs-lookup"><span data-stu-id="3fd4a-111">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="3fd4a-112">Если пакет доступен, отображается состояние **опубликован** .</span><span class="sxs-lookup"><span data-stu-id="3fd4a-112">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="3fd4a-113">Если пакет не был успешно опубликован, отображается состояние **unpublisheded** (вместе с текстом ошибки, объясняющее причину недоступности пакета).</span><span class="sxs-lookup"><span data-stu-id="3fd4a-113">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="3fd4a-114">Разрешение администраторам публиковать и отменять публикацию пакетов</span><span class="sxs-lookup"><span data-stu-id="3fd4a-114">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="3fd4a-115">Перейдите к следующему узлу объекта групповой политики:</span><span class="sxs-lookup"><span data-stu-id="3fd4a-115">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="3fd4a-116">**Конфигурация &gt; компьютера Политики. &gt; административные &gt; шаблоны &gt; &gt; Публикация системы App-V**.</span><span class="sxs-lookup"><span data-stu-id="3fd4a-116">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="3fd4a-117">Включите параметр **требуется опубликовать как** групповую политику администратора.</span><span class="sxs-lookup"><span data-stu-id="3fd4a-117">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="3fd4a-118">Кроме того, чтобы настроить этот элемент с помощью PowerShell, Узнайте, [как управлять пакетами App-V 5,1, запущенными на отдельном компьютере, с помощью PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="3fd4a-118">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="3fd4a-119">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="3fd4a-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="3fd4a-120">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="3fd4a-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="3fd4a-121">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="3fd4a-121">Got an App-V issue?</span></span>** <span data-ttu-id="3fd4a-122">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="3fd4a-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="3fd4a-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3fd4a-123">Related topics</span></span>


[<span data-ttu-id="3fd4a-124">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="3fd4a-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="3fd4a-125">Настройка доступа к пакетам с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="3fd4a-125">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

 

 





