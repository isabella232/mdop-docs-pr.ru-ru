---
title: Локализация текста уведомления портала самообслуживания
description: Локализация текста уведомления портала самообслуживания
author: dansimp
ms.assetid: a4c878b7-e5c8-45af-a537-761bb2991659
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a2385f6b00713e7373bd1707b02324b80f300c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826712"
---
# <span data-ttu-id="063ff-103">Локализация текста уведомления портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="063ff-103">How to Localize the Self-Service Portal Notice Text</span></span>


<span data-ttu-id="063ff-104">Вы можете настроить локализованный текст уведомлений, который будет отображаться для конечных пользователей по умолчанию на портале самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="063ff-104">You can configure localized notice text to display to end users by default in the Self-Service Portal.</span></span> <span data-ttu-id="063ff-105">Файл Notice.txt, в котором отображается текст уведомления, находится в следующем корневом каталоге:</span><span class="sxs-lookup"><span data-stu-id="063ff-105">The Notice.txt file that displays the notice text is in the following root directory:</span></span>

<span data-ttu-id="063ff-106">&lt;Каталог установки самообслуживания *MBAM* &gt; Служба \\Self Website</span><span class="sxs-lookup"><span data-stu-id="063ff-106">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="063ff-107">Чтобы отобразить локализованный текст уведомления, создайте локализованный Notice.txt файл, а затем сохраните его в папке для определенного языка в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="063ff-107">To display localized notice text, you create a localized Notice.txt file, and then save it under a specific language folder in the following example directory:</span></span>

<span data-ttu-id="063ff-108">&lt;Каталог установки самообслуживания *MBAM* &gt; Служба \\Self Website</span><span class="sxs-lookup"><span data-stu-id="063ff-108">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="063ff-109">**Примечание**  Вы можете настроить путь с помощью элемента **NoticeTextPath** в **параметрах приложения**.</span><span class="sxs-lookup"><span data-stu-id="063ff-109">**Note** You can configure the path by using the **NoticeTextPath** item in **Application Settings**.</span></span>

 

<span data-ttu-id="063ff-110">MBAM отображает текст уведомления, основываясь на указанных ниже правилах.</span><span class="sxs-lookup"><span data-stu-id="063ff-110">MBAM displays the notice text, based on the following rules:</span></span>

-   <span data-ttu-id="063ff-111">Если вы создаете локализованный файл **Notice.txt** в соответствующей папке языка, MBAM отображает локализованный текст, если файл **Notice.txt** по умолчанию существует.</span><span class="sxs-lookup"><span data-stu-id="063ff-111">If you create a localized **Notice.txt** file in the appropriate language folder, MBAM displays the localized notice text if the default **Notice.txt** file exists.</span></span> <span data-ttu-id="063ff-112">Если файл **Notice.txt** по умолчанию отсутствует, появится сообщение о том, что файл по умолчанию отсутствует.</span><span class="sxs-lookup"><span data-stu-id="063ff-112">If the default **Notice.txt** file is missing, a message displays indicating that the default file is missing.</span></span>

-   <span data-ttu-id="063ff-113">Если MBAM не удается найти локализованную версию файла Notice.txt, она отобразится в файле Notice.txt по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="063ff-113">If MBAM does not find a localized version of the Notice.txt file, it displays the text in the default Notice.txt file.</span></span>

-   <span data-ttu-id="063ff-114">Если MBAM не удается найти файл Notice.txt по умолчанию, он отображает текст по умолчанию на портале самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="063ff-114">If MBAM does not find a default Notice.txt file, it displays the default text in the Self-Service Portal.</span></span>

<span data-ttu-id="063ff-115">**Примечание**  Если для браузера конечного пользователя выбран язык, для которого не указана соответствующая языковая вложенная папка или Notice.txt, отобразится текст Notice.txt файла в следующем корневом каталоге:</span><span class="sxs-lookup"><span data-stu-id="063ff-115">**Note** If an end user’s browser is set to a language that does not have a corresponding language subfolder or Notice.txt, the text in the Notice.txt file in the following root directory is displayed:</span></span>

<span data-ttu-id="063ff-116">&lt;Каталог установки самообслуживания *MBAM* &gt; Служба \\Self Website</span><span class="sxs-lookup"><span data-stu-id="063ff-116">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

 

**<span data-ttu-id="063ff-117">Создание локализованного Notice.txt файла</span><span class="sxs-lookup"><span data-stu-id="063ff-117">To create a localized Notice.txt file</span></span>**

1.  <span data-ttu-id="063ff-118">На сервере, на котором настроен портал самообслуживания, создайте папку на &lt; *языке* &gt; в следующем примере, где &lt; *язык* &gt; — это название локализованного языка:</span><span class="sxs-lookup"><span data-stu-id="063ff-118">On the server where you configured the Self-Service Portal, create a &lt;*Language*&gt; folder in the following example directory, where &lt;*Language*&gt; represents the name of the localized language:</span></span>

    <span data-ttu-id="063ff-119">&lt;Каталог установки самообслуживания *MBAM* &gt; Служба \\Self Website</span><span class="sxs-lookup"><span data-stu-id="063ff-119">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

    <span data-ttu-id="063ff-120">**Примечание**  Некоторые языковые папки уже существуют, поэтому вам может понадобиться создать папку.</span><span class="sxs-lookup"><span data-stu-id="063ff-120">**Note** Some language folders already exist, so you might not have to create a folder.</span></span> <span data-ttu-id="063ff-121">Если вам нужно создать папку для языка, ознакомьтесь со справочными материалами о [поддержке языковых версий (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947) и просмотрите список допустимых имен, которые можно использовать для &lt; *Language* &gt; папки языка.</span><span class="sxs-lookup"><span data-stu-id="063ff-121">If you do have to create a language folder, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) for a list of the valid names that you can use for the &lt;*Language*&gt; folder.</span></span>

     

2.  <span data-ttu-id="063ff-122">Создайте Notice.txt файл, содержащий локализованный текст уведомления.</span><span class="sxs-lookup"><span data-stu-id="063ff-122">Create a Notice.txt file that contains the localized notice text.</span></span>

3.  <span data-ttu-id="063ff-123">Сохраните файл Notice.txt в &lt; *Language* &gt; папке Language.</span><span class="sxs-lookup"><span data-stu-id="063ff-123">Save the Notice.txt file in the &lt;*Language*&gt; folder.</span></span> <span data-ttu-id="063ff-124">Например, чтобы создать локализованный файл Notice.txt на испанском языке, сохраните локализованный файл Notice.txt в следующем примере каталога:</span><span class="sxs-lookup"><span data-stu-id="063ff-124">For example, to create a localized Notice.txt file in Spanish, save the localized Notice.txt file in the following example directory:</span></span>

    <span data-ttu-id="063ff-125">&lt;Каталог установки самообслуживания *MBAM* &gt; Служба \\Self Website\\Es-es</span><span class="sxs-lookup"><span data-stu-id="063ff-125">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\Es-es</span></span>

    <span data-ttu-id="063ff-126">Имя языковой папки также может представлять собой нейтральное имя языка, **а не** **es-ES**.</span><span class="sxs-lookup"><span data-stu-id="063ff-126">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="063ff-127">Если для браузера конечного пользователя задано значение **es-ES** , а эта папка не существует, родительский языковой стандарт (определенный в .NET) рекурсивно извлекается и проверяется, разрешаются в &lt; Каталог\\SelfServiceWebsite\\es\\Notice.txt самообслуживания MBAM &gt; перед тем, как стать файлом по умолчанию Notice.txt.</span><span class="sxs-lookup"><span data-stu-id="063ff-127">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="063ff-128">Этот рекурсивный резервный вариант имитирует правила загрузки ресурсов .NET.</span><span class="sxs-lookup"><span data-stu-id="063ff-128">This recursive fallback mimics the .NET resource loading rules.</span></span>



## <span data-ttu-id="063ff-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="063ff-129">Related topics</span></span>


[<span data-ttu-id="063ff-130">Настройка портала самообслуживания для организации</span><span class="sxs-lookup"><span data-stu-id="063ff-130">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

## <span data-ttu-id="063ff-131">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="063ff-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="063ff-132">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="063ff-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="063ff-133">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="063ff-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





