---
title: Определение состояния шифрования BitLocker утерянных компьютеров
description: Определение состояния шифрования BitLocker утерянных компьютеров
author: dansimp
ms.assetid: dbd23b64-dff3-4913-9acd-affe67b9462e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9ea4afd6dd08f2040b9e2bd1e1a8998181d1e60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824612"
---
# <span data-ttu-id="9ab11-103">Определение состояния шифрования BitLocker утерянных компьютеров</span><span class="sxs-lookup"><span data-stu-id="9ab11-103">How to Determine BitLocker Encryption State of Lost Computers</span></span>


<span data-ttu-id="9ab11-104">Вы можете использовать администрирование и мониторинг Microsoft BitLocker (MBAM), чтобы определить Последнее известное состояние шифрования BitLocker для компьютеров, которые были утрачены или украдены.</span><span class="sxs-lookup"><span data-stu-id="9ab11-104">You can use Microsoft BitLocker Administration and Monitoring (MBAM) to determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span> <span data-ttu-id="9ab11-105">Ниже описана процедура проверки того, зашифрованы ли тома на компьютере при потере или краже.</span><span class="sxs-lookup"><span data-stu-id="9ab11-105">The following procedure explains how to determine whether the volumes on a computer are encrypted if there is a loss or theft.</span></span>

**<span data-ttu-id="9ab11-106">Определение последнего известного состояния шифрования BitLocker для потерянных компьютеров</span><span class="sxs-lookup"><span data-stu-id="9ab11-106">To determine the last known BitLocker encryption state of lost computers</span></span>**

1.  <span data-ttu-id="9ab11-107">Откройте веб-браузер и перейдите на веб-сайт администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="9ab11-107">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

    <span data-ttu-id="9ab11-108">**Примечание**  Примечание: адрес по умолчанию для веб-сайта администрирования и мониторинга — http://\* &lt; ComputerName &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="9ab11-108">**Note** Note: The default address for the Administration and Monitoring website is http://*&lt;computername&gt;*.</span></span> <span data-ttu-id="9ab11-109">Использование полного имени сервера позволяет быстрее просматривать результаты.</span><span class="sxs-lookup"><span data-stu-id="9ab11-109">Using the fully qualified server name will yield faster browsing results.</span></span>

     

2.  <span data-ttu-id="9ab11-110">Выбор узла **отчета** в области навигации и выбор **отчета о соответствии компьютера**.</span><span class="sxs-lookup"><span data-stu-id="9ab11-110">Selects the **Report** node from the navigation pane, and select the **Computer Compliance Report**.</span></span>

3.  <span data-ttu-id="9ab11-111">С помощью полей фильтра на правой панели Ограничьте результаты поиска и нажмите кнопку **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="9ab11-111">Use the filter fields in the right pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="9ab11-112">Результаты поиска выводятся под поисковым запросом.</span><span class="sxs-lookup"><span data-stu-id="9ab11-112">Results are shown below your search query.</span></span>

4.  <span data-ttu-id="9ab11-113">Выполните необходимые действия в соответствии с определением политики для потерянных устройств.</span><span class="sxs-lookup"><span data-stu-id="9ab11-113">Take the appropriate action, as determined by your policy for lost devices.</span></span>

    <span data-ttu-id="9ab11-114">**Примечание**  Соответствие устройства определяется политиками BitLocker, развернутыми в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="9ab11-114">**Note** Device compliance is determined by the BitLocker policies that your enterprise has deployed.</span></span> <span data-ttu-id="9ab11-115">Возможно, потребуется проверить развернутые политики, прежде чем пытаться определить состояние шифрования BitLocker для устройства.</span><span class="sxs-lookup"><span data-stu-id="9ab11-115">You may want to verify your deployed policies before you try to determine the BitLocker encryption state of a device.</span></span>

     

## <span data-ttu-id="9ab11-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9ab11-116">Related topics</span></span>


[<span data-ttu-id="9ab11-117">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="9ab11-117">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





