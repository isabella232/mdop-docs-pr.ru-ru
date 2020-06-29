---
title: Создание и использование шаблона проекта
description: Создание и использование шаблона проекта
author: dansimp
ms.assetid: e5ac1dc8-a88f-4b16-8e3c-df07ef5e4c3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de3471eca39d3804e8c5f070c5ec37560fae5dc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814248"
---
# <span data-ttu-id="b774b-103">Создание и использование шаблона проекта</span><span class="sxs-lookup"><span data-stu-id="b774b-103">How to Create and Use a Project Template</span></span>


<span data-ttu-id="b774b-104">Вы можете использовать шаблон проекта App-V 5,1, чтобы сохранить часто используемые параметры, связанные с существующим пакетом виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="b774b-104">You can use an App-V 5.1 project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="b774b-105">Эти параметры затем можно применять при создании новых виртуальных пакетов приложений в среде.</span><span class="sxs-lookup"><span data-stu-id="b774b-105">These settings can then be applied when you create new virtual application packages in your environment.</span></span> <span data-ttu-id="b774b-106">С помощью шаблона проекта можно упростить процесс создания виртуальных пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="b774b-106">Using a project template can streamline the process of creating virtual application packages.</span></span>

**<span data-ttu-id="b774b-107">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b774b-107">Note</span></span>**  
<span data-ttu-id="b774b-108">Вы можете часто применять шаблон проекта App-V 5,1 во время обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="b774b-108">You can, and often should apply an App-V 5.1 project template during a package upgrade.</span></span> <span data-ttu-id="b774b-109">Например, если вы помещаете приложение с помощью настраиваемого списка исключений, рекомендуется создать и сохранить связанный шаблон для дальнейшего использования во время обновления упорядоченного приложения.</span><span class="sxs-lookup"><span data-stu-id="b774b-109">For example, if you sequenced an application with a custom exclusion list, it is recommended that an associated template is created and saved for later use while upgrading the sequenced application.</span></span>



<span data-ttu-id="b774b-110">Шаблоны проектов App-V 5,1 отличаются от ускорителей приложений App-V 5,1, так как для App-V 5,1 акселераторы приложений и шаблоны проектов App-V 5,1 можно применять к нескольким приложениям.</span><span class="sxs-lookup"><span data-stu-id="b774b-110">App-V 5.1 project templates differ from App-V 5.1 Application Accelerators because App-V 5.1 Application Accelerators are application-specific, and App-V 5.1 project templates can be applied to multiple applications.</span></span>

<span data-ttu-id="b774b-111">Для создания и применения нового шаблона выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b774b-111">Use the following procedures to create and apply a new template.</span></span>

**<span data-ttu-id="b774b-112">Создание шаблона проекта</span><span class="sxs-lookup"><span data-stu-id="b774b-112">To create a project template</span></span>**

1.  <span data-ttu-id="b774b-113">Чтобы запустить секвенсор App-V 5,1, на компьютере, на котором работает секвенсор, нажмите кнопку **запустить**  /  **все программы**  /  **Microsoft**Application Virtualization  /  **Sequencer Microsoft**Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="b774b-113">To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  **<span data-ttu-id="b774b-114">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b774b-114">Note</span></span>**  
    <span data-ttu-id="b774b-115">Если в данный момент виртуальный пакет приложения открыт в консоли секвенсор App-V 5,1, перейдите к шагу 3 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="b774b-115">If the virtual application package is currently open in the App-V 5.1 Sequencer console, skip to step 3 of this procedure.</span></span>



~~~
To open the existing virtual application package that contains the settings you want to save with the App-V 5.1 project template, click **File** / **Open**, and then click **Edit Package**. On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open. Click **Edit**.
~~~

3. <span data-ttu-id="b774b-116">На консоли App-V 5,1, чтобы сохранить файл шаблона, щелкните **файл**  /  **Сохранить как шаблон**.</span><span class="sxs-lookup"><span data-stu-id="b774b-116">In the App-V 5.1 Sequencer console, to save the template file, click **File** / **Save As Template**.</span></span> <span data-ttu-id="b774b-117">После рассмотрения параметров, которые будут сохранены вместе с новым шаблоном, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b774b-117">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="b774b-118">Укажите имя, которое будет связано с новым шаблоном проекта App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b774b-118">Specify a name that will be associated with the new App-V 5.1 project template.</span></span> <span data-ttu-id="b774b-119">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="b774b-119">Click Save.</span></span>

   <span data-ttu-id="b774b-120">Новый шаблон проекта App-V 5,1 сохраняется в каталоге, указанном на этапе 3 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="b774b-120">The new App-V 5.1 project template is saved in the directory specified in step 3 of this procedure.</span></span>

**<span data-ttu-id="b774b-121">Применение шаблона проекта</span><span class="sxs-lookup"><span data-stu-id="b774b-121">To apply a project template</span></span>**

1.  **<span data-ttu-id="b774b-122">Важно.</span><span class="sxs-lookup"><span data-stu-id="b774b-122">Important</span></span>**  
    <span data-ttu-id="b774b-123">Создание виртуального пакета приложений с помощью шаблона проекта в сочетании с ускорителем пакетов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b774b-123">Creating a virtual application package using a project template in conjunction with a Package Accelerator is not supported.</span></span>



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="b774b-124">Чтобы создать или обновить новый виртуальный пакет приложения с помощью шаблона проекта App-V 5,1, выберите **файл**  /  **создать из шаблона**.</span><span class="sxs-lookup"><span data-stu-id="b774b-124">To create or upgrade a new virtual application package by using an App-V 5.1 project template, click **File** / **New From Template**.</span></span>

3. <span data-ttu-id="b774b-125">Чтобы выбрать шаблон проекта, который вы хотите использовать, перейдите в каталог, в котором хранится шаблон проекта, выберите шаблон проекта, а затем нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="b774b-125">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

   <span data-ttu-id="b774b-126">Создайте новый виртуальный пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="b774b-126">Create the new virtual application package.</span></span> <span data-ttu-id="b774b-127">Параметры, сохраненные с указанным шаблоном, будут применены к новому пакету виртуального приложения, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="b774b-127">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span>

   <span data-ttu-id="b774b-128">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="b774b-128">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="b774b-129">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="b774b-129">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="b774b-130">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="b774b-130">Got an App-V issue?</span></span>** <span data-ttu-id="b774b-131">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="b774b-131">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="b774b-132">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b774b-132">Related topics</span></span>


[<span data-ttu-id="b774b-133">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="b774b-133">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









