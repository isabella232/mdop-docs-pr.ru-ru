---
title: Новые возможности в App-V 5.0 с пакетом обновления 1 (SP1)
description: Новые возможности в App-V 5.0 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: e97c2dbb-7b40-46a0-8137-9ee4fc2bd071
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2542d0cc5a544d26b3279b24063cf3ef428b9f39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813216"
---
# <span data-ttu-id="6c9ab-103">Новые возможности в App-V 5.0 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="6c9ab-103">What's new in App-V 5.0 SP1</span></span>


<span data-ttu-id="6c9ab-104">Этот раздел предназначен для пользователей, которые уже знакомы с приложением-V и хотят узнать, какие изменения были внесены в App-V 5,0 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6c9ab-104">This section is for users who are already familiar with App-V and want to know what has changed in App-V 5.0 SP1.</span></span> <span data-ttu-id="6c9ab-105">Если вы еще не знакомы с приложением-V, вы должны ознакомиться с [планированием для App-v 5,0](planning-for-app-v-50-rc.md).</span><span class="sxs-lookup"><span data-stu-id="6c9ab-105">If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.0](planning-for-app-v-50-rc.md).</span></span>

## <span data-ttu-id="6c9ab-106">Изменения в стандартных функциях</span><span class="sxs-lookup"><span data-stu-id="6c9ab-106">Changes in Standard Functionality</span></span>


<span data-ttu-id="6c9ab-107">В следующих разделах содержатся сведения об изменениях в стандартных функциях для App-V 5,0 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6c9ab-107">The following sections contain information about the changes in standard functionality for App-V 5.0 SP1.</span></span>

### <span data-ttu-id="6c9ab-108">Изменения на поддерживаемых языках</span><span class="sxs-lookup"><span data-stu-id="6c9ab-108">Changes to Supported Languages</span></span>

<span data-ttu-id="6c9ab-109">Дополнительные сведения можно найти в разделе [о приложении App-V 5,0 с пакетом обновления 1 (SP1)](about-app-v-50-sp1.md).</span><span class="sxs-lookup"><span data-stu-id="6c9ab-109">For more information, see [About App-V 5.0 SP1](about-app-v-50-sp1.md).</span></span>

<span data-ttu-id="6c9ab-110">В следующем списке приведены дополнительные сведения о новых языковых пакетах:</span><span class="sxs-lookup"><span data-stu-id="6c9ab-110">The following list contains more information about the new Language Packs:</span></span>

-   <span data-ttu-id="6c9ab-111">Языковые пакеты App-V 5.0 SP1 объединены в установщик **appv\_xxx\_setup.exe** для всех компонентов App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="6c9ab-111">The App-V 5.0SP1 language packs are bundled into the **appv\_xxx\_setup.exe** installer for all the App-V 5.0 Components.</span></span>

-   <span data-ttu-id="6c9ab-112">При запуске установщика будет автоматически устанавливаться подходящий языковой пакет, зависящий от языкового стандарта связанной операционной системы, установленной на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="6c9ab-112">When you run the installer it will automatically install the most appropriate language pack based on the locale of the associated operating system running on the target computer.</span></span>

-   <span data-ttu-id="6c9ab-113">Если требуются дополнительные языковые пакеты, необходимо извлечь из установщика эти языковые пакеты, выполнив следующую команду: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”` .</span><span class="sxs-lookup"><span data-stu-id="6c9ab-113">If additional language packs are required, you must extract these language packs from the installer by running the following command: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”`.</span></span> <span data-ttu-id="6c9ab-114">После этого содержимое установщика извлекается в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="6c9ab-114">After this has been run, the contents of the installer are extracted to the specified location.</span></span>

-   <span data-ttu-id="6c9ab-115">Чтобы установить нужный языковой пакет, примените файл установки Windows для соответствующего языкового пакета.</span><span class="sxs-lookup"><span data-stu-id="6c9ab-115">You must install the desired language pack by applying the appropriate Language pack Windows Installation file.</span></span> <span data-ttu-id="6c9ab-116">Например, **appv\_hib\_LP\_jmmb\_x86.msi** или **appv\_hib\_LP\_jmmb\_x64.msi**, где **Hib** ссылается на компонент, а **jmmb** — на языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="6c9ab-116">For example, **appv\_hib\_LP\_jmmb\_x86.msi** or **appv\_hib\_LP\_jmmb\_x64.msi**, where **hib** refers to the component and **jmmb** refers to the locale.</span></span>

## <span data-ttu-id="6c9ab-117">Улучшенная поддержка для Microsoft Office2010</span><span class="sxs-lookup"><span data-stu-id="6c9ab-117">Enhanced Support for Microsoft Office2010</span></span>


<span data-ttu-id="6c9ab-118">**Комплект виртуализации Microsoft Office 2010 для Application Virtualization (5,0** ) помогает обеспечить единую работу пользователей с помощью виртуализированной версии Microsoft Office2010.</span><span class="sxs-lookup"><span data-stu-id="6c9ab-118">**Microsoft Office 2010 Sequencing Kit for Application Virtualization 5.0** – helps provide users with a consistent experience using a virtualized version of Microsoft Office2010.</span></span> <span data-ttu-id="6c9ab-119">Комплект виртуализации **Microsoft office 2010 для Application 5,0 virtualizations** используется в сочетании с **комплектом средств для развертывания Microsoft Office 2010 для App-V** , а также предоставляет необходимую службу лицензирования Microsoft Office2010.</span><span class="sxs-lookup"><span data-stu-id="6c9ab-119">The **Microsoft Office 2010 Sequencing Kit for Application Virtualization 5.0** is used in conjunction with the **Microsoft Office 2010 Deployment Kit for App-V** and also provides the required Microsoft Office2010 licensing service.</span></span>






## <span data-ttu-id="6c9ab-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="6c9ab-120">Related topics</span></span>


[<span data-ttu-id="6c9ab-121">Сведения о App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="6c9ab-121">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





