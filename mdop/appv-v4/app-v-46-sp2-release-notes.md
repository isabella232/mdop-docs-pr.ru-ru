---
title: Заметки о выпуске App-V 4.6 с пакетом обновления 2 (SP2)
description: Заметки о выпуске App-V 4.6 с пакетом обновления 2 (SP2)
author: dansimp
ms.assetid: abb536f0-e187-4c5b-952a-f837abd10ad2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cf36a6361e6f49c2b868c6752e1b2eb379cc9a31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822342"
---
# <span data-ttu-id="7655e-103">Заметки о выпуске App-V 4.6 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="7655e-103">App-V 4.6 SP2 Release Notes</span></span>


**<span data-ttu-id="7655e-104">Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="7655e-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="7655e-105">Внимательно прочтите эти заметки о выпуске, прежде чем устанавливать Microsoft Application Virtualization (App-V) 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="7655e-105">Read these release notes thoroughly before you install Microsoft Application Virtualization (App-V)4.6 SP2.</span></span>

<span data-ttu-id="7655e-106">Эти заметки о выпуске содержат сведения, необходимые для успешной установки Application Virtualization 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="7655e-106">These release notes contain information that is required to successfully install Application Virtualization 4.6 SP2.</span></span> <span data-ttu-id="7655e-107">Заметки о выпуске также содержат сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="7655e-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="7655e-108">Если существует разница между этими заметками о выпуске и другой документацией по App-V 4.6 SP2, Последнее изменение должно считаться полномочным.</span><span class="sxs-lookup"><span data-stu-id="7655e-108">If there is a difference between these release notes and other App-V4.6SP2 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="7655e-109">Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.</span><span class="sxs-lookup"><span data-stu-id="7655e-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="7655e-110">Сведения о документации по продукту</span><span class="sxs-lookup"><span data-stu-id="7655e-110">About the Product Documentation</span></span>


<span data-ttu-id="7655e-111">Дополнительные сведения о документации для App-V можно найти на странице [Application Virtualization](https://go.microsoft.com/fwlink/?LinkID=232982) в Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="7655e-111">For more information about documentation for App-V, see the [Application Virtualization](https://go.microsoft.com/fwlink/?LinkID=232982) page on Microsoft TechNet.</span></span>

## <span data-ttu-id="7655e-112">Предоставление отзыва</span><span class="sxs-lookup"><span data-stu-id="7655e-112">Providing feedback</span></span>


<span data-ttu-id="7655e-113">Мы заинтересованы в ваших отзывах о приложении App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="7655e-113">We are interested in your feedback on App-V4.6SP2.</span></span> <span data-ttu-id="7655e-114">Вы можете отправить свой отзыв <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="7655e-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="7655e-115">**Примечание**  Этот адрес электронной почты не является каналом поддержки, но ваш отзыв поможет нам спланировать будущие изменения документации и выпусков продуктов.</span><span class="sxs-lookup"><span data-stu-id="7655e-115">**Note** This email address is not a support channel, but your feedback will help us to plan future changes for our documentation and product releases.</span></span>

 

<span data-ttu-id="7655e-116">Последние сведения о MDOP и дополнительных учебных материалах можно найти на странице [сведения о MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="7655e-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="7655e-117">Дополнительные сведения о новых обновлениях и отзыве можно получить, выполнив следующие действия в [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) или [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="7655e-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <a href="" id="known-issues-with-app-v-4-6-sp2-"></a><span data-ttu-id="7655e-118">Известные проблемы с приложением-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="7655e-118">Known Issues with App-V4.6SP2</span></span>


### <span data-ttu-id="7655e-119">Поддержка коротких имен файлов отключена на физических дисках, не являющихся системными, при последовательном выборе</span><span class="sxs-lookup"><span data-stu-id="7655e-119">Short file name support is disabled for non-system physical drives when you sequence</span></span>

<span data-ttu-id="7655e-120">При использовании последовательности в Windows 8 или Windows Server 2012 поддержка коротких имен файлов (8,3) по умолчанию отключена для физических дисков без системы.</span><span class="sxs-lookup"><span data-stu-id="7655e-120">When you sequence on Windows 8 or Windows Server 2012, support for short file names (8.3) is disabled by default for non-system physical drives.</span></span>

<span data-ttu-id="7655e-121">Основной физический диск, связанный с основным каталогом виртуальных приложений (например, "Q:\\appname") на станции виртуализации, должен предоставлять поддержку короткого имени файла (8,3), чтобы при создании пакетов виртуальных приложений для App-V 4.6 SP2 создавались короткие имена файлов.</span><span class="sxs-lookup"><span data-stu-id="7655e-121">The underlying physical drive associated with the primary virtual application directory (for example, “Q:\\appname”) on the sequencing station must provide short file name (8.3) support in order for the App-V4.6SP2 Sequencer to generate short file names when creating virtual application packages.</span></span> <span data-ttu-id="7655e-122">В Windows 8 и Windows Server 2012 поддержка коротких имен файлов (8,3) отключена по умолчанию для несистемных физических дисков.</span><span class="sxs-lookup"><span data-stu-id="7655e-122">Short file name (8.3) support is disabled by default for non-system physical drives on Windows 8 or Windows Server 2012.</span></span>

<span data-ttu-id="7655e-123">**Временное решение:** Включите поддержку коротких имен файлов (8,3) на физических дисках, не являющихся системами.</span><span class="sxs-lookup"><span data-stu-id="7655e-123">**Workaround:** Enable short file name (8.3) support on non-system physical drives.</span></span> <span data-ttu-id="7655e-124">Вы можете использовать указанную ниже команду, чтобы включить поддержку коротких имен файлов в Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="7655e-124">You can use the following command to enable short file name support on Windows 8 or Windows Server 2012.</span></span>

``` syntax
fsutil 8dot3name set <virtual drive letter>:
```

<span data-ttu-id="7655e-125">Например, чтобы указать букву диска "Q:", выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7655e-125">For example, use the following command if the drive letter is “Q:”:</span></span>

``` syntax
fsutil 8dot3name set Q: 0
```

<span data-ttu-id="7655e-126">**Примечание**  Вам не нужно изменять этот параметр в клиенте App-V, так как в файловой системе App-V для Windows 8 или Windows Server 2012 правильно обрабатываются короткие пути.</span><span class="sxs-lookup"><span data-stu-id="7655e-126">**Note** You do not need to change this setting on the App-V client because the App-V file system properly handles short paths on Windows 8 or Windows Server 2012.</span></span>

 

### <a href="" id="-------------app-v-does-not-override-the-default-handler-for-file-type-or-protocol-associations-on-windows-8"></a> <span data-ttu-id="7655e-127">Приложение App-V не переопределяет обработчик по умолчанию для связей с типами файлов и протоколов в Windows 8</span><span class="sxs-lookup"><span data-stu-id="7655e-127">App-V does not override the default handler for file type or protocol associations on Windows 8</span></span>

<span data-ttu-id="7655e-128">Если выбрать приложение по умолчанию с помощью **программ по умолчанию** на **панели управления** в Windows 8, приложение App-V не будет переопределять сопоставлений типов файлов для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="7655e-128">If you select a default application by using **Default Programs** in **Control Panel** on Windows 8, App-V will not override the associated file type associations for that application.</span></span>

<span data-ttu-id="7655e-129">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="7655e-129">**Workaround:** None.</span></span>

### <span data-ttu-id="7655e-130">Виртуализированные Outlook 2010 не предлагаются в качестве параметра для ссылок, которые можно щелкать по адресу mailto в Windows 8</span><span class="sxs-lookup"><span data-stu-id="7655e-130">Virtualized Outlook 2010 is not offered as an option for mailto clickable links on Windows 8</span></span>

<span data-ttu-id="7655e-131">Расширение оболочки mailto не поддерживает виртуализированное приложение Outlook 2010 в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7655e-131">The mailto shell extension does not offer virtualized Outlook 2010 on Windows 8.</span></span> <span data-ttu-id="7655e-132">Например, если вы щелкните ссылку mailto: из виртуализированного Outlook 2010, работающего в Windows 8, не будет создано новое окно электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7655e-132">For example, if you click a mailto: link from virtualized Outlook 2010 that is running on Windows 8, a new email window is not created.</span></span> <span data-ttu-id="7655e-133">Этот параметр работает правильно в Windows 7 и более ранних версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="7655e-133">This option works correctly on Windows 7 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="7655e-134">**Временное решение:** Ничего.</span><span class="sxs-lookup"><span data-stu-id="7655e-134">**Workaround:** None.</span></span>

### <a href="" id="-------------application-virtualization-4-6-sp2-update-is-not-offered-on-all-locales-that-use-microsoft-update"></a> <span data-ttu-id="7655e-135">Обновление Application Virtualization 4,6 с пакетом обновления 2 (SP2) не предлагается на всех языках, использующих Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="7655e-135">Application Virtualization 4.6 SP2 update is not offered on all locales that use Microsoft Update</span></span>

<span data-ttu-id="7655e-136">При использовании центра обновления Майкрософт Обновление для App-V 4.6 SP2 недоступно для языковых стандартов, указанных ниже.</span><span class="sxs-lookup"><span data-stu-id="7655e-136">When you use Microsoft Update, the update for App-V4.6SP2 is not available for the following language locales:</span></span>

-   <span data-ttu-id="7655e-137">Казахский</span><span class="sxs-lookup"><span data-stu-id="7655e-137">Kazakh</span></span>

-   <span data-ttu-id="7655e-138">Хинди</span><span class="sxs-lookup"><span data-stu-id="7655e-138">Hindi</span></span>

-   <span data-ttu-id="7655e-139">Сербский (кириллица)</span><span class="sxs-lookup"><span data-stu-id="7655e-139">Serbian-Cyrillic</span></span>

<span data-ttu-id="7655e-140">**Временное решение:** Если вы используете Microsoft Windows Server Update Services (WSUS), используйте английскую версию обновления или загрузите обновление из каталога Центра обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7655e-140">**Workaround:** If you are using Microsoft Windows Server Update Services (WSUS), use the English version of the update or download the update from the Microsoft Update Catalog.</span></span>

## <span data-ttu-id="7655e-141">Сведения о заметках об авторском праве</span><span class="sxs-lookup"><span data-stu-id="7655e-141">Release Notes Copyright Information</span></span>


<span data-ttu-id="7655e-142">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune и WindowsPowerShell являются товарными знаками группы компании Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7655e-142">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="7655e-143">Все прочие товарные знаки являются собственностью соответствующих владельцев.</span><span class="sxs-lookup"><span data-stu-id="7655e-143">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="7655e-144">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7655e-144">Related topics</span></span>


[<span data-ttu-id="7655e-145">Сведения о системе Microsoft Application Virtualization 4.6 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="7655e-145">About Microsoft Application Virtualization 4.6 SP2</span></span>](about-microsoft-application-virtualization-46-sp2.md)

 

 





