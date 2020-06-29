---
title: Настройка портала самообслуживания при отсутствии у клиентских компьютеров доступа к сети доставки содержимого корпорации Майкрософт
description: Настройка портала самообслуживания при отсутствии у клиентских компьютеров доступа к сети доставки содержимого корпорации Майкрософт
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824492"
---
# <span data-ttu-id="1ce5b-103">Настройка портала самообслуживания при отсутствии у клиентских компьютеров доступа к сети доставки содержимого корпорации Майкрософт</span><span class="sxs-lookup"><span data-stu-id="1ce5b-103">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>


<span data-ttu-id="1ce5b-104">Следуйте этим инструкциям, если клиентские компьютеры в вашей организации не имеют доступа к сети доставки содержимого (CDN) Microsoft AJAX.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-104">Follow these instructions if the client computers in your organization do not have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

**<span data-ttu-id="1ce5b-105">Зачем нужно настраивать это:</span><span class="sxs-lookup"><span data-stu-id="1ce5b-105">Why you need to configure this:</span></span>**

<span data-ttu-id="1ce5b-106">Клиентские компьютеры нуждаются в доступе к сети CDN, который предоставляет порталу самообслуживания необходимый доступ к определенным файлам JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-106">Your client computers need access to the CDN, which gives the Self-Service Portal the required access to certain JavaScript files.</span></span> <span data-ttu-id="1ce5b-107">Если вы не настраиваете портал самообслуживания, когда клиентские компьютеры не могут получить доступ к сети CDN, будет отображаться только название компании и учетная запись, под которой входит конечный пользователь.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-107">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which the end user logs in will be displayed.</span></span> <span data-ttu-id="1ce5b-108">Сообщение об ошибке не выводится.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-108">No error message will be shown.</span></span>

<span data-ttu-id="1ce5b-109">**Примечание**  В MBAM 2,5 с пакетом обновления 1 (SP1) файлы JavaScript включены в продукт, и вам не нужно выполнять инструкции, описанные в этом разделе, для настройки поставщика общих служб на поддержку клиентов, которые не могут получить доступ к Интернету.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-109">**Note** In MBAM 2.5 SP1, the JavaScript files are included in the product, and you do not need to follow the instructions in this section to configure the SSP to support clients that cannot access the internet.</span></span>

 

**<span data-ttu-id="1ce5b-110">Настройка портала самообслуживания, когда клиентские компьютеры не могут получить доступ к сети CDN</span><span class="sxs-lookup"><span data-stu-id="1ce5b-110">How to configure the Self-Service Portal when client computers cannot access the CDN</span></span>**

1. <span data-ttu-id="1ce5b-111">Скачайте следующие файлы JavaScript из сети CDN:</span><span class="sxs-lookup"><span data-stu-id="1ce5b-111">Download the following JavaScript files from the CDN:</span></span>

   -   [<span data-ttu-id="1ce5b-112">jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="1ce5b-112">jQuery-1.10.2.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [<span data-ttu-id="1ce5b-113">jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="1ce5b-113">jQuery.validate.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [<span data-ttu-id="1ce5b-114">jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="1ce5b-114">jQuery.validate.unobtrusive.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390517)

2. <span data-ttu-id="1ce5b-115">Скопируйте файлы JavaScript в каталог **Scripts** на портале самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-115">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="1ce5b-116">Этот каталог находится в службе самообслуживания <em> &lt; MBAM в каталогах самостоятельной установки &gt; \\ </em> Website\\Scripts.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-116">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

3. <span data-ttu-id="1ce5b-117">Откройте диспетчер информационных служб Интернета (IIS).</span><span class="sxs-lookup"><span data-stu-id="1ce5b-117">Open Internet Information Services (IIS) Manager.</span></span>

4. <span data-ttu-id="1ce5b-118">Разверните **сайты** &gt; **Администрирование и мониторинг Microsoft BitLocker**и выберите **Selfservice**.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-118">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="1ce5b-119">Примечание.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-119">Note</span></span>**  
   <span data-ttu-id="1ce5b-120">*Selfservice* — имя виртуального каталога по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-120">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="1ce5b-121">Если во время настройки вы выбрали другое имя для этого каталога, не забудьте заменить *Selfservice* в этих инструкциях на выбранное вами имя.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-121">If you chose a different name for this directory during the configuration, remember to replace *SelfService* in these instructions with the name you chose.</span></span>

     

5. <span data-ttu-id="1ce5b-122">В средней области дважды щелкните **Параметры приложения**.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-122">In the middle pane, double-click **Application Settings**.</span></span>

6. <span data-ttu-id="1ce5b-123">Для каждого элемента в списке ниже измените параметры приложения, чтобы они ссылались на новое расположение, заменив/ &lt; *виртуальные каталоги* &gt; /с/Selfservice/(или любым именем, которое вы выбрали при настройке).</span><span class="sxs-lookup"><span data-stu-id="1ce5b-123">For each item in the following list, edit the application settings to reference the new location by replacing /&lt;*virtual directory*&gt;/ with /SelfService/ (or whatever name you chose during configuration).</span></span> <span data-ttu-id="1ce5b-124">Например, путь к виртуальному каталогу будет похож на/selfservice/Scripts/jQuery-1.10.2.min.js.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-124">For example, the virtual directory path will be similar to /selfservice/Scripts/ jQuery-1.10.2.min.js.</span></span>

   -   <span data-ttu-id="1ce5b-125">jQueryPath:/ &lt; *virtual directory* &gt; /Scripts/jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="1ce5b-125">jQueryPath: /&lt;*virtual directory*&gt;/Scripts/jQuery-1.10.2.min.js</span></span>

   -   <span data-ttu-id="1ce5b-126">jQueryValidatePath:/ &lt; *virtual directory* &gt; /Scripts/jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="1ce5b-126">jQueryValidatePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.min.js</span></span>

   -   <span data-ttu-id="1ce5b-127">jQueryValidateUnobtrusivePath:/ &lt; *virtual directory* &gt; /Scripts/jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="1ce5b-127">jQueryValidateUnobtrusivePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.unobtrusive.min.js</span></span>



## <span data-ttu-id="1ce5b-128">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1ce5b-128">Related topics</span></span>


[<span data-ttu-id="1ce5b-129">Настройка веб-приложений MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1ce5b-129">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

 

## <span data-ttu-id="1ce5b-130">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="1ce5b-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="1ce5b-131">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="1ce5b-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="1ce5b-132">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="1ce5b-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





