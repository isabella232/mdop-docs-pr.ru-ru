---
title: Настройка публикации пакетов с помощью ESD только для администраторов
description: Настройка публикации пакетов с помощью ESD только для администраторов
author: dansimp
ms.assetid: 03367b26-83d5-4299-ad52-b9177b9cf9a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 341e86ca806c5acc736c78cf8072aab6fb4286df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814109"
---
# <span data-ttu-id="6ddf8-103">Настройка публикации пакетов с помощью ESD только для администраторов</span><span class="sxs-lookup"><span data-stu-id="6ddf8-103">How to Enable Only Administrators to Publish Packages by Using an ESD</span></span>


<span data-ttu-id="6ddf8-104">Начиная с версии App-V 5,0 SP3, вы можете настроить клиент App-V таким образом, чтобы только администраторы (не конечные пользователи) могли публиковать и отменять публикацию пакетов.</span><span class="sxs-lookup"><span data-stu-id="6ddf8-104">Starting in App-V 5.0 SP3, you can configure the App-V client so that only administrators (not end users) can publish or unpublish packages.</span></span> <span data-ttu-id="6ddf8-105">В более ранних версиях приложения App-V вы не смогли предотвратить выполнение этих задач конечными пользователями.</span><span class="sxs-lookup"><span data-stu-id="6ddf8-105">In earlier versions of App-V, you could not prevent end users from performing these tasks.</span></span>

**<span data-ttu-id="6ddf8-106">Разрешение администраторам публиковать и отменять публикацию пакетов</span><span class="sxs-lookup"><span data-stu-id="6ddf8-106">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="6ddf8-107">Перейдите к следующему узлу объекта групповой политики:</span><span class="sxs-lookup"><span data-stu-id="6ddf8-107">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="6ddf8-108">**Конфигурация &gt; компьютера Политики. &gt; административные &gt; шаблоны &gt; &gt; Публикация системы App-V**.</span><span class="sxs-lookup"><span data-stu-id="6ddf8-108">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="6ddf8-109">Включите параметр **требуется опубликовать как** групповую политику администратора.</span><span class="sxs-lookup"><span data-stu-id="6ddf8-109">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="6ddf8-110">Кроме того, чтобы настроить этот элемент с помощью PowerShell, Узнайте, [как управлять пакетами App-V 5,0, запущенными на отдельном компьютере, с помощью PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="6ddf8-110">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="6ddf8-111">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="6ddf8-111">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="6ddf8-112">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="6ddf8-112">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="6ddf8-113">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="6ddf8-113">Got an App-V issue?</span></span>** <span data-ttu-id="6ddf8-114">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="6ddf8-114">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

 

 




