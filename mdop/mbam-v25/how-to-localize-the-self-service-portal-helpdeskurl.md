---
title: Локализация параметра "HelpdeskURL" портала самообслуживания
description: Локализация параметра "HelpdeskURL" портала самообслуживания
author: dansimp
ms.assetid: 86798460-077b-459b-8d54-4b605e07d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0d7ec4ce87bbe5aab56e9fa877ced5f51625a5dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826709"
---
# <span data-ttu-id="8a750-103">Локализация параметра "HelpdeskURL" портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="8a750-103">How to Localize the Self-Service Portal “HelpdeskURL”</span></span>


<span data-ttu-id="8a750-104">Вы можете настроить локализованную версию URL-адреса портала самообслуживания, которая будет отображаться для конечных пользователей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8a750-104">You can configure a localized version of the Self-Service Portal URL to display to end users by default.</span></span> <span data-ttu-id="8a750-105">URL-адрес портала самообслуживания представлен параметром **HelpdeskURL**.</span><span class="sxs-lookup"><span data-stu-id="8a750-105">The Self-Service Portal URL is represented by the parameter **HelpdeskURL**.</span></span>

<span data-ttu-id="8a750-106">Если вы создали локализованную версию, как описано в приведенных ниже инструкциях, Администрирование и мониторинг Microsoft BitLocker (MBAM) находит и отображает локализованную версию.</span><span class="sxs-lookup"><span data-stu-id="8a750-106">If you create a localized version, as described in the following instructions, Microsoft BitLocker Administration and Monitoring (MBAM) finds and displays the localized version.</span></span> <span data-ttu-id="8a750-107">Если MBAM не удается найти локализованную версию, выводится URL-адрес, настроенный для параметра **HelpDeskURL**.</span><span class="sxs-lookup"><span data-stu-id="8a750-107">If MBAM does not find a localized version, it displays the URL that is configured for the parameter **HelpDeskURL**.</span></span>

<span data-ttu-id="8a750-108">**Примечание**  В приведенных ниже инструкциях *Selfservice* является именем виртуального каталога по умолчанию для портала самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="8a750-108">**Note** In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="8a750-109">Возможно, вы использовали другое имя, когда вы настроили портал самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="8a750-109">You might have used a different name when you configured the Self-Service Portal.</span></span>

 

**<span data-ttu-id="8a750-110">Локализация URL-адреса портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="8a750-110">To localize the Self-Service Portal URL</span></span>**

1.  <span data-ttu-id="8a750-111">На сервере, на котором настроен портал самообслуживания, перейдите к **сайтам** &gt; **Администрирование Microsoft BitLocker и отслеживайте** &gt; **SelfService** &gt; **Параметры Selfservice приложения**.</span><span class="sxs-lookup"><span data-stu-id="8a750-111">On the server where you configured the Self-Service Portal, browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

2.  <span data-ttu-id="8a750-112">В области **действия** нажмите кнопку **Добавить** , чтобы открыть диалоговое окно **Добавление параметра приложения** .</span><span class="sxs-lookup"><span data-stu-id="8a750-112">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="8a750-113">В поле **Name (имя** ) введите **HelpdeskURL**\ _ &lt; *Language* &gt; (язык), где &lt; *Language* &gt; — код, соответствующий URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="8a750-113">In the **Name** field, type **HelpdeskURL**\_&lt;*Language*&gt;, where &lt;*Language*&gt; is the appropriate language code for the URL.</span></span>

    <span data-ttu-id="8a750-114">Например, чтобы создать локализованную версию `HelpdeskURL` значения на испанском языке, назовите параметр **HelpdeskURL \ _es-ES**.</span><span class="sxs-lookup"><span data-stu-id="8a750-114">For example, to create a localized version of the `HelpdeskURL` value in Spanish, name the parameter **HelpdeskURL\_es-es**.</span></span>

    <span data-ttu-id="8a750-115">Имя языковой папки также может представлять собой нейтральное имя языка, **а не** **es-ES**.</span><span class="sxs-lookup"><span data-stu-id="8a750-115">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="8a750-116">Если для браузера конечного пользователя задано значение **es-ES** , а эта папка не существует, родительский языковой стандарт (определенный в .NET) рекурсивно извлекается и проверяется, разрешаются в &lt; Каталог\\SelfServiceWebsite\\es\\Notice.txt самообслуживания MBAM &gt; перед тем, как стать файлом по умолчанию Notice.txt.</span><span class="sxs-lookup"><span data-stu-id="8a750-116">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="8a750-117">Этот рекурсивный резервный вариант имитирует правила загрузки ресурсов .NET.</span><span class="sxs-lookup"><span data-stu-id="8a750-117">This recursive fallback mimics the .NET resource loading rules.</span></span>

    <span data-ttu-id="8a750-118">Список допустимых кодов языков, которые можно использовать, приведен в разделе [Справочник по API на языке поддержки языков (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="8a750-118">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="8a750-119">В поле **value (значение** ) введите локализованную версию `HelpdeskURL` значения, которое будет отображаться для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="8a750-119">In the **Value** field, type the localized version of the `HelpdeskURL` value that you want to display to end users.</span></span>



## <span data-ttu-id="8a750-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8a750-120">Related topics</span></span>


[<span data-ttu-id="8a750-121">Настройка портала самообслуживания для организации</span><span class="sxs-lookup"><span data-stu-id="8a750-121">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

 
## <span data-ttu-id="8a750-122">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="8a750-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8a750-123">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8a750-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8a750-124">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8a750-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




