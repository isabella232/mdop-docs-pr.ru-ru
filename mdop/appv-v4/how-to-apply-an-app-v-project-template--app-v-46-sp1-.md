---
title: Применение шаблона проекта App-V (App-V 4.6 с пакетом обновления 1 (SP1))
description: Применение шаблона проекта App-V (App-V 4.6 с пакетом обновления 1 (SP1))
author: dansimp
ms.assetid: 8ef120ab-8cfb-438c-8136-671167b7bd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b5f04f3f31838bfb13c19eee5f2314c3a3d291f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821372"
---
# <span data-ttu-id="221ec-103">Применение шаблона проекта App-V (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="221ec-103">How to Apply an App-V Project Template (App-V 4.6 SP1)</span></span>


<span data-ttu-id="221ec-104">Вы можете использовать шаблон проекта App-V для применения общих параметров, связанных с существующим виртуальным пакетом приложения, с новым виртуальным пакетом приложения.</span><span class="sxs-lookup"><span data-stu-id="221ec-104">You can use an App-V project template to apply common settings associated with an existing virtual application package to a new virtual application package.</span></span> <span data-ttu-id="221ec-105">С помощью шаблонов проектов App-V можно оптимизировать процесс создания виртуальных пакетов приложений, настроив общие параметры перед началом виртуализации приложения.</span><span class="sxs-lookup"><span data-stu-id="221ec-105">Using App-V project templates can help streamline the process of creating virtual application packages by configuring common settings before you begin sequencing an application.</span></span>

<span data-ttu-id="221ec-106">**Примечание**  Шаблон проекта App-V можно применять только в том случае, если вы создаете новый виртуальный пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="221ec-106">**Note** You can only apply an App-V project template when you are creating a new virtual application package.</span></span> <span data-ttu-id="221ec-107">Применение шаблонов проектов к существующим виртуальным пакетам приложений не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="221ec-107">Applying project templates to existing virtual application packages is not supported.</span></span> <span data-ttu-id="221ec-108">Кроме того, шаблон проекта нельзя использовать в сочетании с ускорителем пакетов.</span><span class="sxs-lookup"><span data-stu-id="221ec-108">Additionally, you cannot use a project template in conjunction with a Package Accelerator.</span></span>

 

<span data-ttu-id="221ec-109">Дополнительные сведения о создании шаблонов проектов App-V можно найти [в разделе Создание шаблона проекта App-v (App-v 4,6 SP1)](how-to-create-an-app-v-project-template--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="221ec-109">For more information about creating App-V project templates, see [How to Create an App-V Project Template (App-V 4.6 SP1)](how-to-create-an-app-v-project-template--app-v-46-sp1-.md).</span></span>

**<span data-ttu-id="221ec-110">Применение шаблона проекта App-V</span><span class="sxs-lookup"><span data-stu-id="221ec-110">To apply an App-V project template</span></span>**

1.  <span data-ttu-id="221ec-111">Чтобы запустить программу Microsoft Application Virtualization Sequencer на компьютере, на котором установлен секвенсор App-V, нажмите кнопку **запустить**  /  **All Programs**  /  **Microsoft Application**Virtualization  /  **Sequencer Microsoft**Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="221ec-111">To start the Microsoft Application Virtualization Sequencer, on the computer on which App-V Sequencer is installed, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="221ec-112">Чтобы создать новый виртуальный пакет приложения с помощью шаблона проекта App-V, нажмите **файл**  /  **создать из шаблона**.</span><span class="sxs-lookup"><span data-stu-id="221ec-112">To create a new virtual application package by using an App-V project template, click **File** / **New From Template**.</span></span>

3.  <span data-ttu-id="221ec-113">Чтобы выбрать шаблон проекта, который вы хотите использовать, перейдите в каталог, в котором хранится шаблон проекта, выберите шаблон проекта, а затем нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="221ec-113">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

4.  <span data-ttu-id="221ec-114">Создайте новый виртуальный пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="221ec-114">Create the new virtual application package.</span></span> <span data-ttu-id="221ec-115">Параметры, сохраненные с указанным шаблоном, будут применены к новому пакету виртуального приложения, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="221ec-115">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span> <span data-ttu-id="221ec-116">Дополнительные сведения о создании нового пакета виртуальных приложений можно найти в разделе [Определение типа приложения для последовательного выполнения (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)и выберите соответствующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="221ec-116">For more information about creating a new virtual application package, see [How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md), and select the appropriate procedure.</span></span>

## <span data-ttu-id="221ec-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="221ec-117">Related topics</span></span>


[<span data-ttu-id="221ec-118">Задачи для Application Virtualization Sequencer (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="221ec-118">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="221ec-119">Создание шаблона проекта App-V (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="221ec-119">How to Create an App-V Project Template (App-V 4.6 SP1)</span></span>](how-to-create-an-app-v-project-template--app-v-46-sp1-.md)

 

 





