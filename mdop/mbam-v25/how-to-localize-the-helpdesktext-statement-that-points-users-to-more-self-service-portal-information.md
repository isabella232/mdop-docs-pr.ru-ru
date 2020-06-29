---
title: Локализация оператора "HelpdeskText", указывающего на дополнительные сведения портала самообслуживания пользователям
description: Локализация оператора "HelpdeskText", указывающего на дополнительные сведения портала самообслуживания пользователям
author: dansimp
ms.assetid: 09ba2a07-3186-45d9-adef-4034c70ae7cf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2367424185da813a46fa52f3614c03083864f75f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823422"
---
# <span data-ttu-id="9d7cc-103">Локализация оператора "HelpdeskText", указывающего на дополнительные сведения портала самообслуживания пользователям</span><span class="sxs-lookup"><span data-stu-id="9d7cc-103">How to Localize the “HelpdeskText” Statement that Points Users to More Self-Service Portal Information</span></span>


<span data-ttu-id="9d7cc-104">Вы можете настроить локализованную версию оператора самообслуживания портала "HelpdeskText", который информирует пользователей о том, как получить дополнительные сведения о том, как пользоваться порталом самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="9d7cc-104">You can configure a localized version of the Self-Service Portal "HelpdeskText" statement, which informs end users about how to get additional help when they are using the Self-Service Portal.</span></span> <span data-ttu-id="9d7cc-105">Если вы настроили локализованный текст для инструкции, как описано в приведенных ниже инструкциях, MBAM отображает локализованную версию.</span><span class="sxs-lookup"><span data-stu-id="9d7cc-105">If you configure localized text for the statement, as described in the following instructions, MBAM displays the localized version.</span></span> <span data-ttu-id="9d7cc-106">Если MBAM не удается найти локализованную версию, отобразится значение, заданное в параметре **HelpdeskText** .</span><span class="sxs-lookup"><span data-stu-id="9d7cc-106">If MBAM does not find the localized version, it displays the value that is in the **HelpdeskText** parameter.</span></span>

<span data-ttu-id="9d7cc-107">**Примечание**  В приведенных ниже инструкциях *Selfservice* является именем виртуального каталога по умолчанию для портала самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="9d7cc-107">**Note** In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="9d7cc-108">Возможно, вы использовали другое имя, когда вы настроили портал самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="9d7cc-108">You might have used a different name when you configured the Self-Service Portal.</span></span>

 

**<span data-ttu-id="9d7cc-109">Отображение локализованной версии инструкции HelpdeskText</span><span class="sxs-lookup"><span data-stu-id="9d7cc-109">To display a localized version of the HelpdeskText statement</span></span>**

1.  <span data-ttu-id="9d7cc-110">На сервере, на котором настроен портал самообслуживания, перейдите к **сайтам** &gt; **Администрирование Microsoft BitLocker и отслеживайте** &gt; **SelfService** &gt; **Параметры Selfservice приложения**.</span><span class="sxs-lookup"><span data-stu-id="9d7cc-110">On the server where you configured the Self-Service Portal, browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

2.  <span data-ttu-id="9d7cc-111">В области **действия** нажмите кнопку **Добавить** , чтобы открыть диалоговое окно **Добавление параметра приложения** .</span><span class="sxs-lookup"><span data-stu-id="9d7cc-111">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="9d7cc-112">В поле **Name (имя** ) введите **HelpdeskText**\ _ &lt; *Language* &gt; , где &lt; *Language* &gt; — код соответствующего языка для текста.</span><span class="sxs-lookup"><span data-stu-id="9d7cc-112">In the **Name** field, type **HelpdeskText**\_&lt;*Language*&gt;, where &lt;*Language*&gt; is the appropriate language code for the text.</span></span>

    <span data-ttu-id="9d7cc-113">Например, чтобы создать локализованную инструкцию HelpdeskText на испанском языке, назовите параметр **HelpdeskText \ _es-ES**.</span><span class="sxs-lookup"><span data-stu-id="9d7cc-113">For example, to create a localized HelpdeskText statement in Spanish, name the parameter **HelpdeskText\_es-es**.</span></span>

    <span data-ttu-id="9d7cc-114">Имя языковой папки также может представлять собой нейтральное имя языка, **а не** **es-ES**.</span><span class="sxs-lookup"><span data-stu-id="9d7cc-114">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="9d7cc-115">Если для браузера конечного пользователя задано значение **es-ES** , а эта папка не существует, родительский языковой стандарт (определенный в .NET) рекурсивно извлекается и проверяется, разрешаются в &lt; Каталог\\SelfServiceWebsite\\es\\Notice.txt самообслуживания MBAM &gt; перед тем, как стать файлом по умолчанию Notice.txt.</span><span class="sxs-lookup"><span data-stu-id="9d7cc-115">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="9d7cc-116">Этот рекурсивный резервный вариант имитирует правила загрузки ресурсов .NET.</span><span class="sxs-lookup"><span data-stu-id="9d7cc-116">This recursive fallback mimics the .NET resource loading rules.</span></span>

    <span data-ttu-id="9d7cc-117">Список допустимых кодов языков, которые можно использовать, приведен в разделе [Справочник по API на языке поддержки языков (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="9d7cc-117">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="9d7cc-118">В поле **value (значение** ) введите локализованный текст, который будет отображаться для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="9d7cc-118">In the **Value** field, type the localized text that you want to display to end users.</span></span>



## <span data-ttu-id="9d7cc-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9d7cc-119">Related topics</span></span>


[<span data-ttu-id="9d7cc-120">Настройка портала самообслуживания для организации</span><span class="sxs-lookup"><span data-stu-id="9d7cc-120">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

 

## <span data-ttu-id="9d7cc-121">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="9d7cc-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="9d7cc-122">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="9d7cc-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="9d7cc-123">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="9d7cc-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



