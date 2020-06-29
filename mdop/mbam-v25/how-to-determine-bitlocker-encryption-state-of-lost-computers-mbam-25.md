---
title: Определение состояния шифрования BitLocker утерянных компьютеров
description: Определение состояния шифрования BitLocker утерянных компьютеров
author: dansimp
ms.assetid: 4f4bec1b-df3e-40ee-b431-291440268d64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95fb843b230804417e375946814a585d1d681634
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824472"
---
# <span data-ttu-id="741d9-103">Определение состояния шифрования BitLocker утерянных компьютеров</span><span class="sxs-lookup"><span data-stu-id="741d9-103">How to Determine BitLocker Encryption State of Lost Computers</span></span>


<span data-ttu-id="741d9-104">Используйте эту процедуру с веб-сайтом администрирования и мониторинга для определения указанных ниже параметров.</span><span class="sxs-lookup"><span data-stu-id="741d9-104">Use this procedure with the Administration and Monitoring Website to determine the following:</span></span>

-   <span data-ttu-id="741d9-105">Последнее известное состояние шифрования BitLocker для потерянных или украденных компьютеров</span><span class="sxs-lookup"><span data-stu-id="741d9-105">The last known BitLocker encryption status of lost or stolen computers</span></span>

-   <span data-ttu-id="741d9-106">Зашифрованы ли тома потерянного или украденного компьютера</span><span class="sxs-lookup"><span data-stu-id="741d9-106">Whether the volumes on a lost or stolen computer were encrypted</span></span>

<span data-ttu-id="741d9-107">Для выполнения этой задачи вам понадобится доступ к области " **отчеты** " на веб-сайте администрирования и наблюдения.</span><span class="sxs-lookup"><span data-stu-id="741d9-107">To complete this task, you need access to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="741d9-108">Чтобы получить доступ к этой области, необходимо назначить роль пользователей отчетов MBAM.</span><span class="sxs-lookup"><span data-stu-id="741d9-108">To get access to this area, you must be assigned the MBAM Report Users role.</span></span> <span data-ttu-id="741d9-109">Возможно, вы предоставили эти роли имена при их создании.</span><span class="sxs-lookup"><span data-stu-id="741d9-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="741d9-110">Дополнительные сведения можно найти в разделе [планирование для групп MBAM 2,5 и учетных записей](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="741d9-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="741d9-111">**Примечание**  Соответствие устройства определяется политиками BitLocker, развернутыми в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="741d9-111">**Note** Device compliance is determined by the BitLocker policies that your enterprise has deployed.</span></span> <span data-ttu-id="741d9-112">Возможно, потребуется проверить развернутые политики, прежде чем пытаться определить состояние шифрования BitLocker для устройства.</span><span class="sxs-lookup"><span data-stu-id="741d9-112">You may want to verify your deployed policies before you try to determine the BitLocker encryption state of a device.</span></span>

 

**<span data-ttu-id="741d9-113">Определение последнего известного состояния шифрования BitLocker для потерянных компьютеров</span><span class="sxs-lookup"><span data-stu-id="741d9-113">To determine the last known BitLocker encryption state of lost computers</span></span>**

1.  <span data-ttu-id="741d9-114">Откройте веб-браузер и перейдите на **веб-сайт администрирования и мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="741d9-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="741d9-115">На левой панели выберите **отчеты** , чтобы открыть страницу отчеты.</span><span class="sxs-lookup"><span data-stu-id="741d9-115">In the left pane, select **Reports** to open the Reports page.</span></span>

3.  <span data-ttu-id="741d9-116">Выберите **отчет о соответствии компьютера**.</span><span class="sxs-lookup"><span data-stu-id="741d9-116">Select the **Computer Compliance Report**.</span></span>

4.  <span data-ttu-id="741d9-117">С помощью полей фильтра на правой панели Ограничьте результаты поиска и нажмите кнопку **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="741d9-117">Use the filter fields in the right pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="741d9-118">Результаты отображаются под вашим поисковым запросом.</span><span class="sxs-lookup"><span data-stu-id="741d9-118">Results are shown under your search query.</span></span>

5.  <span data-ttu-id="741d9-119">Выполните необходимые действия в соответствии с определением политики для потерянных устройств.</span><span class="sxs-lookup"><span data-stu-id="741d9-119">Take the appropriate action, as determined by your policy for lost devices.</span></span>



## <span data-ttu-id="741d9-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="741d9-120">Related topics</span></span>


[<span data-ttu-id="741d9-121">Управление BitLocker с помощью MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="741d9-121">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="741d9-122">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="741d9-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="741d9-123">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="741d9-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="741d9-124">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="741d9-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





