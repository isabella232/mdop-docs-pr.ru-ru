---
title: Создание шаблона проекта App-V (App-V 4.6 с пакетом обновления 1 (SP1))
description: Создание шаблона проекта App-V (App-V 4.6 с пакетом обновления 1 (SP1))
author: dansimp
ms.assetid: 7e87fba2-b72a-4bc9-92b8-220e25aae99a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e264d5c41b663bc9c450dc642e2b26297ee7ea1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817649"
---
# <span data-ttu-id="82f19-103">Создание шаблона проекта App-V (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="82f19-103">How to Create an App-V Project Template (App-V 4.6 SP1)</span></span>


<span data-ttu-id="82f19-104">Вы можете использовать шаблон проекта App-V, чтобы сохранить часто используемые параметры, связанные с существующим пакетом виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="82f19-104">You can use an App-V project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="82f19-105">Эти параметры затем можно применять при создании новых виртуальных пакетов приложений в среде, которые помогут вам оптимизировать процесс создания пакетов виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="82f19-105">These settings can then be applied when you create new virtual application packages in your environment which can help streamline the process of creating virtual application packages.</span></span>

<span data-ttu-id="82f19-106">**Примечание**  Шаблон проекта App-V можно применять только в том случае, если вы создаете новый виртуальный пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="82f19-106">**Note** You can only apply an App-V project template when you are creating a new virtual application package.</span></span> <span data-ttu-id="82f19-107">Применение шаблонов проектов к существующим виртуальным пакетам приложений не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="82f19-107">Applying project templates to existing virtual application packages is not supported.</span></span>

 

<span data-ttu-id="82f19-108">Дополнительные сведения о применении шаблона проекта App-V можно найти в разделе [Применение шаблона проекта App-v (App-v 4,6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="82f19-108">For more information about applying an App-V project template, see [How to Apply an App-V Project Template (App-V 4.6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="82f19-109">Шаблоны проектов App-V отличаются от ускорителей приложений App-V, так как акселераторы приложений App-v являются специфическими для приложения, а шаблоны проектов App-V можно применять к нескольким приложениям.</span><span class="sxs-lookup"><span data-stu-id="82f19-109">App-V project templates differ from App-V Application Accelerators because App-V Application Accelerators are application-specific, and App-V project templates can be applied to multiple applications.</span></span> <span data-ttu-id="82f19-110">Кроме того, шаблон проекта нельзя использовать для создания виртуального пакета приложения, если вы используете ускоритель пакетов.</span><span class="sxs-lookup"><span data-stu-id="82f19-110">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span>

<span data-ttu-id="82f19-111">Следующие общие параметры сохраняются в шаблоне проекта App-V.</span><span class="sxs-lookup"><span data-stu-id="82f19-111">The following general settings are saved with an App-V project template:</span></span>

-   <span data-ttu-id="82f19-112">**Дополнительные параметры наблюдения**.</span><span class="sxs-lookup"><span data-stu-id="82f19-112">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="82f19-113">Включение функции центра обновления Майкрософт при наблюдении, rebase **. dll**.</span><span class="sxs-lookup"><span data-stu-id="82f19-113">Enables Microsoft Update to run during monitoring, Rebase **.dll’s**.</span></span>

-   <span data-ttu-id="82f19-114">**Параметры развертывания пакета**.</span><span class="sxs-lookup"><span data-stu-id="82f19-114">**Package Deployment Settings**.</span></span> <span data-ttu-id="82f19-115">Включает **протокол**, **имя узла**, **порт**, **путь**, **операционные системы**, **Использование дескрипторов безопасности**, **Создание MSI**-файла, **Сжатие пакета**.</span><span class="sxs-lookup"><span data-stu-id="82f19-115">Contains **Protocol**, **Host Name**, **Port**, **Path**, **Operating Systems**, **Enforce Security Descriptors**, **Create MSI**, **Compress Package**.</span></span>

-   <span data-ttu-id="82f19-116">**Общие параметры**.</span><span class="sxs-lookup"><span data-stu-id="82f19-116">**General Options**.</span></span> <span data-ttu-id="82f19-117">Позволяет создавать пакеты **установщика Microsoft Windows (MSI)** , **разрешать виртуализацию событий**, **разрешать виртуализацию служб**, **добавлять версию пакета в имя файла**.</span><span class="sxs-lookup"><span data-stu-id="82f19-117">Allows you to **Generate Microsoft Windows Installer (MSI)** package, **Allow Virtualization of Events**, **Allow Virtualization of Services**, **Append Package Version to Filename**.</span></span>

-   <span data-ttu-id="82f19-118">**Исключаемые элементы**.</span><span class="sxs-lookup"><span data-stu-id="82f19-118">**Exclusion Items**.</span></span> <span data-ttu-id="82f19-119">Содержащий список шаблонов исключений.</span><span class="sxs-lookup"><span data-stu-id="82f19-119">Contains the Exclusion pattern list.</span></span>

**<span data-ttu-id="82f19-120">Создание шаблона проекта</span><span class="sxs-lookup"><span data-stu-id="82f19-120">To create a project template</span></span>**

1.  <span data-ttu-id="82f19-121">Чтобы запустить секвенсор App-v на компьютере, на котором работает секвенсор App-v, нажмите кнопку **запустить**  /  **все программы**  /  **Microsoft**Application Virtualization  /  **Sequencer Microsoft**Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="82f19-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="82f19-122">Если в данный момент виртуальный пакет приложения открыт в секвенсоре App-V, перейдите к шагу 3 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="82f19-122">If the virtual application package is currently open in the App-V Sequencer, skip to step 3 of this procedure.</span></span> <span data-ttu-id="82f19-123">Чтобы открыть существующий пакет виртуального приложения, содержащий параметры, которые вы хотите сохранить с помощью шаблона проекта App-V, нажмите кнопку **File**  /  **Открыть** файл и выберите команду **изменить** **пакет**.</span><span class="sxs-lookup"><span data-stu-id="82f19-123">To open the existing virtual application package that contains the settings you want to save with the App-V project template, click **File** / **Open** and click **Edit** **Package**.</span></span> <span data-ttu-id="82f19-124">На странице **Выбор пакета** нажмите кнопку **Обзор** и найдите пакет виртуального приложения, который вы хотите открыть.</span><span class="sxs-lookup"><span data-stu-id="82f19-124">On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open.</span></span> <span data-ttu-id="82f19-125">Нажмите кнопку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="82f19-125">Click **Edit**.</span></span>

3.  <span data-ttu-id="82f19-126">На консоли секвенсора App-V щелкните **файл**  /  **Сохранить как шаблон**.</span><span class="sxs-lookup"><span data-stu-id="82f19-126">In the App-V Sequencer console, click **File** / **Save As Template**.</span></span> <span data-ttu-id="82f19-127">После рассмотрения параметров, которые будут сохранены вместе с новым шаблоном, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="82f19-127">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="82f19-128">Укажите имя, которое будет связано с новым шаблоном проекта App-V.</span><span class="sxs-lookup"><span data-stu-id="82f19-128">Specify a name that will be associated with the new App-V project template.</span></span> <span data-ttu-id="82f19-129">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="82f19-129">Click **Save**.</span></span>

    <span data-ttu-id="82f19-130">Новый шаблон проекта App-V сохраняется в каталоге, указанном на этапе 3 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="82f19-130">The new App-V project template is saved in the directory specified in step 3 of this procedure.</span></span>

## <span data-ttu-id="82f19-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="82f19-131">Related topics</span></span>


[<span data-ttu-id="82f19-132">Задачи для Application Virtualization Sequencer (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="82f19-132">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="82f19-133">Применение шаблона проекта App-V (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="82f19-133">How to Apply an App-V Project Template (App-V 4.6 SP1)</span></span>](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)

 

 





