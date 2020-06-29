---
title: Создание и использование шаблона проекта
description: Создание и использование шаблона проекта
author: dansimp
ms.assetid: 2063f0b3-47a1-4090-bf99-0f26b107331c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e7640b9dc1e7baec194315400ee5672dfa83f394
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814261"
---
# <span data-ttu-id="f8424-103">Создание и использование шаблона проекта</span><span class="sxs-lookup"><span data-stu-id="f8424-103">How to Create and Use a Project Template</span></span>


<span data-ttu-id="f8424-104">Вы можете использовать шаблон проекта App-V 5,0, чтобы сохранить часто используемые параметры, связанные с существующим пакетом виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="f8424-104">You can use an App-V 5.0 project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="f8424-105">Эти параметры затем можно применять при создании новых виртуальных пакетов приложений в среде.</span><span class="sxs-lookup"><span data-stu-id="f8424-105">These settings can then be applied when you create new virtual application packages in your environment.</span></span> <span data-ttu-id="f8424-106">С помощью шаблона проекта можно упростить процесс создания виртуальных пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="f8424-106">Using a project template can streamline the process of creating virtual application packages.</span></span>

<span data-ttu-id="f8424-107">**Примечание**  Вы можете часто применять шаблон проекта App-V 5,0 во время обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="f8424-107">**Note** You can, and often should apply an App-V 5.0 project template during a package upgrade.</span></span> <span data-ttu-id="f8424-108">Например, если вы помещаете приложение с помощью настраиваемого списка исключений, рекомендуется создать и сохранить связанный шаблон для дальнейшего использования во время обновления упорядоченного приложения.</span><span class="sxs-lookup"><span data-stu-id="f8424-108">For example, if you sequenced an application with a custom exclusion list, it is recommended that an associated template is created and saved for later use while upgrading the sequenced application.</span></span>

<span data-ttu-id="f8424-109">Шаблоны проектов App-V 5,0 отличаются от ускорителей приложений App-V 5,0, так как для App-V 5,0 акселераторы приложений и шаблоны проектов App-V 5,0 можно применять к нескольким приложениям.</span><span class="sxs-lookup"><span data-stu-id="f8424-109">App-V 5.0 project templates differ from App-V 5.0 Application Accelerators because App-V 5.0 Application Accelerators are application-specific, and App-V 5.0 project templates can be applied to multiple applications.</span></span>

<span data-ttu-id="f8424-110">Для создания и применения нового шаблона выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f8424-110">Use the following procedures to create and apply a new template.</span></span>

**<span data-ttu-id="f8424-111">Создание шаблона проекта</span><span class="sxs-lookup"><span data-stu-id="f8424-111">To create a project template</span></span>**

1.  <span data-ttu-id="f8424-112">Чтобы запустить секвенсор App-V 5,0, на компьютере, на котором работает секвенсор, нажмите кнопку **запустить**  /  **все программы**  /  **Microsoft**Application Virtualization  /  **Sequencer Microsoft**Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f8424-112">To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

<span data-ttu-id="f8424-113">**Примечание**  Если в данный момент виртуальный пакет приложения открыт в консоли секвенсор App-V 5,0, перейдите к шагу 3 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="f8424-113">**Note** If the virtual application package is currently open in the App-V 5.0 Sequencer console, skip to step 3 of this procedure.</span></span>

2. <span data-ttu-id="f8424-114">Чтобы открыть существующий пакет виртуального приложения, содержащий параметры, которые вы хотите сохранить с помощью шаблона проекта App-V 5,0, нажмите кнопку **File**  /  **Открыть**файл, а затем выберите команду **изменить пакет**.</span><span class="sxs-lookup"><span data-stu-id="f8424-114">To open the existing virtual application package that contains the settings you want to save with the App-V 5.0 project template, click **File** / **Open**, and then click **Edit Package**.</span></span> <span data-ttu-id="f8424-115">На странице **Выбор пакета** нажмите кнопку **Обзор** и найдите пакет виртуального приложения, который вы хотите открыть.</span><span class="sxs-lookup"><span data-stu-id="f8424-115">On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open.</span></span> <span data-ttu-id="f8424-116">Нажмите кнопку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="f8424-116">Click **Edit**.</span></span>

3. <span data-ttu-id="f8424-117">На консоли App-V 5,0, чтобы сохранить файл шаблона, щелкните **файл**  /  **Сохранить как шаблон**.</span><span class="sxs-lookup"><span data-stu-id="f8424-117">In the App-V 5.0 Sequencer console, to save the template file, click **File** / **Save As Template**.</span></span> <span data-ttu-id="f8424-118">После рассмотрения параметров, которые будут сохранены вместе с новым шаблоном, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f8424-118">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="f8424-119">Укажите имя, которое будет связано с новым шаблоном проекта App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f8424-119">Specify a name that will be associated with the new App-V 5.0 project template.</span></span> <span data-ttu-id="f8424-120">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="f8424-120">Click Save.</span></span>
   <span data-ttu-id="f8424-121">Новый шаблон проекта App-V 5,0 сохраняется в каталоге, указанном на этапе 3 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="f8424-121">The new App-V 5.0 project template is saved in the directory specified in step 3 of this procedure.</span></span>

**<span data-ttu-id="f8424-122">Применение шаблона проекта</span><span class="sxs-lookup"><span data-stu-id="f8424-122">To apply a project template</span></span>**

<span data-ttu-id="f8424-123">**Важно!**  Создание виртуального пакета приложений с помощью шаблона проекта в сочетании с ускорителем пакетов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f8424-123">**Important** Creating a virtual application package using a project template in conjunction with a Package Accelerator is not supported.</span></span>

1.  <span data-ttu-id="f8424-124">Чтобы запустить секвенсор App-V 5,0, на компьютере, на котором работает секвенсор, нажмите кнопку **запустить**  /  **все программы**  /  **Microsoft**Application Virtualization  /  **Sequencer Microsoft**Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f8424-124">To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="f8424-125">Чтобы создать или обновить новый виртуальный пакет приложения с помощью шаблона проекта App-V 5,0, выберите **файл**  /  **создать из шаблона**.</span><span class="sxs-lookup"><span data-stu-id="f8424-125">To create or upgrade a new virtual application package by using an App-V 5.0 project template, click **File** / **New From Template**.</span></span>

3.  <span data-ttu-id="f8424-126">Чтобы выбрать шаблон проекта, который вы хотите использовать, перейдите в каталог, в котором хранится шаблон проекта, выберите шаблон проекта, а затем нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="f8424-126">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

    <span data-ttu-id="f8424-127">Создайте новый виртуальный пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="f8424-127">Create the new virtual application package.</span></span> <span data-ttu-id="f8424-128">Параметры, сохраненные с указанным шаблоном, будут применены к новому пакету виртуального приложения, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="f8424-128">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span>

    <span data-ttu-id="f8424-129">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="f8424-129">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f8424-130">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="f8424-130">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f8424-131">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="f8424-131">Got an App-V issue?</span></span>** <span data-ttu-id="f8424-132">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f8424-132">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f8424-133">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f8424-133">Related topics</span></span>


[<span data-ttu-id="f8424-134">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f8424-134">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









