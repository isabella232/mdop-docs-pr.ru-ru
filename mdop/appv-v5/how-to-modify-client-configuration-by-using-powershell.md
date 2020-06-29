---
title: Изменение конфигурации клиента с помощью PowerShell
description: Изменение конфигурации клиента с помощью PowerShell
author: dansimp
ms.assetid: 53ccb2cf-ef81-4310-a853-efcb395f006e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d3173944abfe2c2b3d30aa9654dae81f204a32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813829"
---
# <span data-ttu-id="5c89d-103">Изменение конфигурации клиента с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="5c89d-103">How to Modify Client Configuration by Using PowerShell</span></span>


<span data-ttu-id="5c89d-104">Чтобы настроить конфигурацию клиента App-V 5,0, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5c89d-104">Use the following procedure to configure the App-V 5.0 client configuration.</span></span>

**<span data-ttu-id="5c89d-105">Изменение конфигурации клиента App-V 5,0 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="5c89d-105">To modify App-V 5.0 client configuration using PowerShell</span></span>**

1.  <span data-ttu-id="5c89d-106">Чтобы настроить параметры клиента с помощью PowerShell, используйте командлет **Set-AppvClientConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="5c89d-106">To configure the client settings using PowerShell, use the **Set-AppvClientConfiguration** cmdlet.</span></span>

2.  <span data-ttu-id="5c89d-107">Чтобы изменить конфигурацию клиента, откройте командную строка PowerShell и запустите следующий командлет **Set-AppvClientConfiguration** с необходимыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="5c89d-107">To modify the client configuration, open a PowerShell Command prompt and run the following cmdlet **Set-AppvClientConfiguration** with any required parameters.</span></span> <span data-ttu-id="5c89d-108">Пример</span><span class="sxs-lookup"><span data-stu-id="5c89d-108">For example:</span></span>

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    <span data-ttu-id="5c89d-109">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="5c89d-109">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="5c89d-110">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="5c89d-110">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="5c89d-111">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="5c89d-111">Got an App-V issue?</span></span>** <span data-ttu-id="5c89d-112">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="5c89d-112">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="5c89d-113">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5c89d-113">Related topics</span></span>


[<span data-ttu-id="5c89d-114">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="5c89d-114">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





