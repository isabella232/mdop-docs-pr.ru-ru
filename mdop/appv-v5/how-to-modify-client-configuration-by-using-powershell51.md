---
title: Изменение конфигурации клиента с помощью PowerShell
description: Изменение конфигурации клиента с помощью PowerShell
author: dansimp
ms.assetid: c3a59592-bb0d-43b6-8f4e-44f3a2d5b7ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 368a0d12c12e10a623afad3f9040ae01cee6cb38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813813"
---
# <span data-ttu-id="a6f26-103">Изменение конфигурации клиента с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6f26-103">How to Modify Client Configuration by Using PowerShell</span></span>


<span data-ttu-id="a6f26-104">Чтобы настроить конфигурацию клиента App-V 5,1, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a6f26-104">Use the following procedure to configure the App-V 5.1 client configuration.</span></span>

**<span data-ttu-id="a6f26-105">Изменение конфигурации клиента App-V 5,1 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6f26-105">To modify App-V 5.1 client configuration using PowerShell</span></span>**

1.  <span data-ttu-id="a6f26-106">Чтобы настроить параметры клиента с помощью PowerShell, используйте командлет **Set-AppvClientConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="a6f26-106">To configure the client settings using PowerShell, use the **Set-AppvClientConfiguration** cmdlet.</span></span> <span data-ttu-id="a6f26-107">Дополнительные сведения об установке PowerShell и список командлетов можно найти в разделе [как загрузить командлеты PowerShell и получить справку по командлету](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).</span><span class="sxs-lookup"><span data-stu-id="a6f26-107">For more information about installing PowerShell, and a list of cmdlets see, [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).</span></span>

2.  <span data-ttu-id="a6f26-108">Чтобы изменить конфигурацию клиента, откройте командную строка PowerShell и запустите следующий командлет **Set-AppvClientConfiguration** с необходимыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="a6f26-108">To modify the client configuration, open a PowerShell Command prompt and run the following cmdlet **Set-AppvClientConfiguration** with any required parameters.</span></span> <span data-ttu-id="a6f26-109">Пример</span><span class="sxs-lookup"><span data-stu-id="a6f26-109">For example:</span></span>

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    <span data-ttu-id="a6f26-110">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="a6f26-110">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a6f26-111">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="a6f26-111">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a6f26-112">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="a6f26-112">Got an App-V issue?</span></span>** <span data-ttu-id="a6f26-113">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a6f26-113">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a6f26-114">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a6f26-114">Related topics</span></span>


[<span data-ttu-id="a6f26-115">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a6f26-115">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





