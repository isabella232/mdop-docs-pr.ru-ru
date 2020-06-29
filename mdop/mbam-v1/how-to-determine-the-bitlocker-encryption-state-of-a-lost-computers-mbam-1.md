---
title: Определение состояния шифрования BitLocker утерянных компьютеров
description: Определение состояния шифрования BitLocker утерянных компьютеров
author: dansimp
ms.assetid: 9440890a-9c63-463b-9113-f46071446388
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9b977b20ecf219830609c3b1f646a29e6678448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824292"
---
# <span data-ttu-id="0037d-103">Определение состояния шифрования BitLocker утерянных компьютеров</span><span class="sxs-lookup"><span data-stu-id="0037d-103">How to Determine the BitLocker Encryption State of a Lost Computers</span></span>


<span data-ttu-id="0037d-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) позволяет определить Последнее известное состояние шифрования BitLocker для потерянных или украденных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="0037d-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to determine the last known BitLocker encryption status of computers that are lost or stolen.</span></span> <span data-ttu-id="0037d-105">Выполните описанные ниже действия, чтобы определить, зашифрованы ли тома на компьютерах, которые больше не находятся в Вашем пользовании.</span><span class="sxs-lookup"><span data-stu-id="0037d-105">Use the following procedure to determine whether the volumes have been encrypted on computers that are no longer in your possession.</span></span>

**<span data-ttu-id="0037d-106">Определение последнего известного состояния шифрования BitLocker для компьютера</span><span class="sxs-lookup"><span data-stu-id="0037d-106">Determine a Computer's Last Known BitLocker Encryption state</span></span>**

1.  <span data-ttu-id="0037d-107">Откройте веб-сайт MBAM.</span><span class="sxs-lookup"><span data-stu-id="0037d-107">Open the MBAM website.</span></span>

    <span data-ttu-id="0037d-108">**Примечание**  Адресом по умолчанию для веб-сайта MBAM является http://\* &lt; имя_компьютера &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="0037d-108">**Note** The default address for the MBAM website is http://*&lt;computername&gt;*.</span></span> <span data-ttu-id="0037d-109">Используйте полное имя сервера для более быстрых результатов просмотра.</span><span class="sxs-lookup"><span data-stu-id="0037d-109">Use the fully qualified server name for faster browsing results.</span></span>

     

2.  <span data-ttu-id="0037d-110">Выберите узел **отчета** в области навигации, а затем выберите **отчет о соответствии компьютера**.</span><span class="sxs-lookup"><span data-stu-id="0037d-110">Select the **Report** node from the navigation pane, and then select the **Computer Compliance Report**.</span></span>

3.  <span data-ttu-id="0037d-111">С помощью полей фильтра на правой панели Ограничьте результаты поиска и нажмите кнопку **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="0037d-111">Use the filter fields in the right-side pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="0037d-112">Результаты поиска будут показаны под поисковым запросом.</span><span class="sxs-lookup"><span data-stu-id="0037d-112">Results will be shown below your search query.</span></span>

4.  <span data-ttu-id="0037d-113">Выполните необходимые действия, которые определяются политикой для потерянных устройств.</span><span class="sxs-lookup"><span data-stu-id="0037d-113">Take the appropriate action as determined by your policy for lost devices.</span></span>

    <span data-ttu-id="0037d-114">**Примечание**  Соответствие устройства определяется развернутыми политиками BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0037d-114">**Note** Device compliance is determined by the deployed BitLocker policies.</span></span> <span data-ttu-id="0037d-115">Эти развернутые политики следует проверять при попытке определить состояние шифрования BitLocker для устройства.</span><span class="sxs-lookup"><span data-stu-id="0037d-115">You should verify these deployed policies when you are trying to determine the BitLocker encryption state of a device.</span></span>

     

## <span data-ttu-id="0037d-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0037d-116">Related topics</span></span>


[<span data-ttu-id="0037d-117">Управление BitLocker с помощью MBAM</span><span class="sxs-lookup"><span data-stu-id="0037d-117">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





