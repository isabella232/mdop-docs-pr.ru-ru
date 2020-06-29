---
title: Разветвление пакета
description: Разветвление пакета
author: dansimp
ms.assetid: bfe46a8a-f0ee-4a71-9e9c-64ac08aac9c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2de36fae1a09aeae4d1b7b21ebe00f683e3b3693
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818129"
---
# <span data-ttu-id="dc863-103">Разветвление пакета</span><span class="sxs-lookup"><span data-stu-id="dc863-103">How to Branch a Package</span></span>


<span data-ttu-id="dc863-104">Используйте эту процедуру, чтобы изменить существующий пакет приложения в последовательности, чтобы можно было выполнить его параллельно с исходным пакетом приложения.</span><span class="sxs-lookup"><span data-stu-id="dc863-104">Use this procedure to modify an existing sequenced application package so you can run it side-by-side with the original sequenced application package.</span></span> <span data-ttu-id="dc863-105">Этот процесс называется ветвлением.</span><span class="sxs-lookup"><span data-stu-id="dc863-105">This process is called branching.</span></span> <span data-ttu-id="dc863-106">При ветвлении пакета виртуальных приложений вы можете запускать две версии одного пакета.</span><span class="sxs-lookup"><span data-stu-id="dc863-106">When you branch a virtual application package you are able to run two versions of the same package.</span></span> <span data-ttu-id="dc863-107">Например, вы можете применить пакет обновления к существующему пакету и выполнить его параллельно с исходным пакетом виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="dc863-107">For example, you can apply a service pack to an existing package, and run it side-by-side with the original sequenced virtual application package.</span></span>

<span data-ttu-id="dc863-108">Используйте описанную ниже процедуру для ветвления упорядоченного виртуального пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="dc863-108">Use the following procedure to branch a sequenced virtual application package.</span></span>

**<span data-ttu-id="dc863-109">Переход к последовательности виртуальных пакетов приложений</span><span class="sxs-lookup"><span data-stu-id="dc863-109">To branch a sequenced virtual application package</span></span>**

1.  <span data-ttu-id="dc863-110">Откройте секвенсор Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="dc863-110">Open the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="dc863-111">Чтобы указать каталог назначения, содержащий пакет (. SPRJ), выберите пункт **файл**, **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="dc863-111">To specify the destination directory that contains the package (.sprj) you want to branch select **File**, **Open**.</span></span>

2.  <span data-ttu-id="dc863-112">Перейдите в каталог, содержащий виртуализированное приложение, которое вы собираетесь создать, и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="dc863-112">Navigate to the directory that contains the sequenced application you plan to branch and click **Open**.</span></span>

3.  <span data-ttu-id="dc863-113">Чтобы сохранить копию пакета, в секвенсоре App-V выберите **файл**, **Сохранить как**.</span><span class="sxs-lookup"><span data-stu-id="dc863-113">To save a copy of the package, in the App-V Sequencer, select **File**, **Save As**.</span></span> <span data-ttu-id="dc863-114">Укажите новое уникальное имя и укажите новый уникальный корневой каталог пакета для копии пакета.</span><span class="sxs-lookup"><span data-stu-id="dc863-114">Specify a new, unique name, and specify a new unique package root directory for the copy of the package.</span></span> <span data-ttu-id="dc863-115">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="dc863-115">Click **Save**.</span></span>

    **<span data-ttu-id="dc863-116">Важно.</span><span class="sxs-lookup"><span data-stu-id="dc863-116">Important</span></span>**  
    <span data-ttu-id="dc863-117">Необходимо указать новое имя пакета или перезаписать существующую версию пакета.</span><span class="sxs-lookup"><span data-stu-id="dc863-117">You must specify a new package name or you will overwrite the existing version of the package.</span></span>



~~~
The sequencer will automatically generate new GUID files for the new package. The version number associated with the package will also be automatically appended to the OSD file name.
~~~

4. <span data-ttu-id="dc863-118">После сохранения новой версии вы можете применить необходимые изменения конфигурации и сохранить соответствующие файлы ICO, OSD, SFT и SPRJ в правильном расположении на сервере Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="dc863-118">After you save the new version you can apply the required configuration changes and save the associated ICO, OSD, SFT, and SPRJ files to correct location on the Application Virtualization (App-V) server.</span></span>

## <span data-ttu-id="dc863-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="dc863-119">Related topics</span></span>


[<span data-ttu-id="dc863-120">Задачи Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="dc863-120">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)









