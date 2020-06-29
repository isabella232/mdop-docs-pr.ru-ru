---
title: Публикация пакета с помощью консоли управления
description: Публикация пакета с помощью консоли управления
author: dansimp
ms.assetid: 7c6930fc-5c89-4519-a901-512dae155fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 832dd95edbb0f4cd6b6ae242a81859141ebcb279
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813784"
---
# <span data-ttu-id="0189a-103">Публикация пакета с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="0189a-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="0189a-104">Чтобы опубликовать пакет App-V 5,0, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="0189a-104">Use the following procedure to publish an App-V 5.0 package.</span></span> <span data-ttu-id="0189a-105">После публикации пакета компьютеры, на которых работает клиент App-V 5,0, смогут получать доступ к приложениям в этом пакете и запускать их.</span><span class="sxs-lookup"><span data-stu-id="0189a-105">Once you publish a package, computers that are running the App-V 5.0 client can access and run the applications in that package.</span></span>

<span data-ttu-id="0189a-106">**Примечание**  Возможность разрешения только администраторам публиковать и отменять публикацию пакетов (описанных ниже) поддерживается начиная с версии App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="0189a-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="0189a-107">Публикация пакета App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0189a-107">To publish an App-V 5.0 package</span></span>**

1.  <span data-ttu-id="0189a-108">В консоли управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0189a-108">In the App-V 5.0 Management console.</span></span> <span data-ttu-id="0189a-109">Щелкните правой кнопкой мыши имя пакета, который нужно опубликовать, и выберите команду **опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="0189a-109">right-click the name of the package to be published, and select **Publish**.</span></span>

2.  <span data-ttu-id="0189a-110">Просмотрите столбец **состояние** , чтобы убедиться, что пакет опубликован и теперь доступен.</span><span class="sxs-lookup"><span data-stu-id="0189a-110">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="0189a-111">Если пакет доступен, отображается состояние **опубликован** .</span><span class="sxs-lookup"><span data-stu-id="0189a-111">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="0189a-112">Если пакет не был успешно опубликован, отображается состояние **unpublisheded** (вместе с текстом ошибки, объясняющее причину недоступности пакета).</span><span class="sxs-lookup"><span data-stu-id="0189a-112">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="0189a-113">Разрешение администраторам публиковать и отменять публикацию пакетов</span><span class="sxs-lookup"><span data-stu-id="0189a-113">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="0189a-114">Перейдите к следующему узлу объекта групповой политики:</span><span class="sxs-lookup"><span data-stu-id="0189a-114">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="0189a-115">**Конфигурация &gt; компьютера Политики. &gt; административные &gt; шаблоны &gt; &gt; Публикация системы App-V**.</span><span class="sxs-lookup"><span data-stu-id="0189a-115">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="0189a-116">Включите параметр **требуется опубликовать как** групповую политику администратора.</span><span class="sxs-lookup"><span data-stu-id="0189a-116">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="0189a-117">Кроме того, чтобы настроить этот элемент с помощью PowerShell, Узнайте, [как управлять пакетами App-V 5,0, запущенными на отдельном компьютере, с помощью PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="0189a-117">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="0189a-118">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="0189a-118">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="0189a-119">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="0189a-119">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="0189a-120">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="0189a-120">Got an App-V issue?</span></span>** <span data-ttu-id="0189a-121">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="0189a-121">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="0189a-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0189a-122">Related topics</span></span>


[<span data-ttu-id="0189a-123">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="0189a-123">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="0189a-124">Настройка доступа к пакетам с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="0189a-124">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

 

 





