---
title: Изменение файла OSD
description: Изменение файла OSD
author: dansimp
ms.assetid: 0d126ba7-72fb-42ce-982e-90ed01a852c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4a0ff4a8efe1fa177f6847c344add94bca3648cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817439"
---
# <span data-ttu-id="a393e-103">Изменение файла OSD</span><span class="sxs-lookup"><span data-stu-id="a393e-103">How to Edit an OSD File</span></span>


<span data-ttu-id="a393e-104">Чтобы изменить файл дескриптора программного обеспечения (OSD) пакета приложения с помощью добавления или удаления элемента или атрибута, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a393e-104">Use the following procedures to modify a sequenced application package's Open Software Descriptor (OSD) file by adding or deleting an element or an attribute.</span></span>

<span data-ttu-id="a393e-105">**Примечание**  У некоторых элементов нет атрибута, поэтому добавить атрибут к каждому элементу невозможно.</span><span class="sxs-lookup"><span data-stu-id="a393e-105">**Note** Some elements do not have an attribute, so it is not possible to add an attribute to every element.</span></span>

 

<span data-ttu-id="a393e-106">**Важно!**  Если вы используете редактор OSD для изменения имени SFT – файла, атрибута HREF элемента CODEBASE в OSD, необходимо использовать команду **Сохранить как** , чтобы сохранить изменения в файлах проекта.</span><span class="sxs-lookup"><span data-stu-id="a393e-106">**Important** If you use the OSD editor to change the .sft file name, the HREF attribute of the CODEBASE element in the OSD file, you must use the **Save As** command to save the change to the project files.</span></span>

 

**<span data-ttu-id="a393e-107">Добавление элемента</span><span class="sxs-lookup"><span data-stu-id="a393e-107">To add an element</span></span>**

1.  <span data-ttu-id="a393e-108">Откройте вкладку **OSD файл** .</span><span class="sxs-lookup"><span data-stu-id="a393e-108">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="a393e-109">В области навигации выберите OSD-файл пакета приложения, который вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="a393e-109">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="a393e-110">В области навигации щелкните правой кнопкой мыши элемент, который вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="a393e-110">In the navigation pane, right-click the element that you want to modify.</span></span> <span data-ttu-id="a393e-111">В меню выберите **элемент** и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="a393e-111">On the menu, select **Element** and select **Add**.</span></span>

4.  <span data-ttu-id="a393e-112">В меню выберите элемент, который вы хотите добавить, например **CodeBase**.</span><span class="sxs-lookup"><span data-stu-id="a393e-112">From the menu, select the element you want to add—for example, **Codebase**.</span></span>

5.  <span data-ttu-id="a393e-113">В меню **файл** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a393e-113">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="a393e-114">Удаление элемента</span><span class="sxs-lookup"><span data-stu-id="a393e-114">To delete an element</span></span>**

1.  <span data-ttu-id="a393e-115">Откройте вкладку **OSD файл** .</span><span class="sxs-lookup"><span data-stu-id="a393e-115">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="a393e-116">В области навигации выберите OSD-файл пакета приложения, который вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="a393e-116">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="a393e-117">В области навигации щелкните правой кнопкой мыши элемент, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="a393e-117">In the navigation pane, right-click the element that you want to delete.</span></span> <span data-ttu-id="a393e-118">В меню выберите **элемент** и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="a393e-118">On the menu, select **Element** and select **Delete**.</span></span>

4.  <span data-ttu-id="a393e-119">В меню **файл** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a393e-119">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="a393e-120">Добавление атрибута</span><span class="sxs-lookup"><span data-stu-id="a393e-120">To add an attribute</span></span>**

1.  <span data-ttu-id="a393e-121">Откройте вкладку **OSD файл** .</span><span class="sxs-lookup"><span data-stu-id="a393e-121">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="a393e-122">В области навигации выберите OSD-файл пакета приложения, который вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="a393e-122">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="a393e-123">В левой области щелкните правой кнопкой мыши элемент, к которому вы хотите добавить атрибут.</span><span class="sxs-lookup"><span data-stu-id="a393e-123">In the left pane, right-click the element to which you want to add an attribute.</span></span> <span data-ttu-id="a393e-124">В меню выберите **атрибут** и нажмите кнопку **Добавить**, выбрав из списка Доступные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="a393e-124">On the menu, select **Attribute** and select **Add**, choosing from the listed available attributes.</span></span>

4.  <span data-ttu-id="a393e-125">В меню **файл** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a393e-125">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="a393e-126">Удаление атрибута</span><span class="sxs-lookup"><span data-stu-id="a393e-126">To delete an attribute</span></span>**

1.  <span data-ttu-id="a393e-127">Откройте вкладку **OSD файл** .</span><span class="sxs-lookup"><span data-stu-id="a393e-127">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="a393e-128">В области навигации выберите OSD-файл пакета приложения, который вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="a393e-128">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="a393e-129">В области навигации щелкните правой кнопкой мыши элемент, из которого вы хотите удалить атрибут.</span><span class="sxs-lookup"><span data-stu-id="a393e-129">In the navigation pane, right-click the element from which you want to delete an attribute.</span></span> <span data-ttu-id="a393e-130">В меню выберите **атрибут** и нажмите кнопку **Удалить**, выбрав атрибут, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="a393e-130">On the menu, select **Attribute** and then select **Delete**, choosing the attribute you wish to delete.</span></span>

4.  <span data-ttu-id="a393e-131">В меню **файл** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a393e-131">From the **File** menu, select **Save**.</span></span>

## <span data-ttu-id="a393e-132">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a393e-132">Related topics</span></span>


[<span data-ttu-id="a393e-133">Вкладка "Сведения об OSD"</span><span class="sxs-lookup"><span data-stu-id="a393e-133">About the OSD Tab</span></span>](about-the-osd-tab.md)

[<span data-ttu-id="a393e-134">Изменение файла OSD с помощью текстового редактора</span><span class="sxs-lookup"><span data-stu-id="a393e-134">How to Edit an OSD File Using a Text Editor</span></span>](how-to-edit-an-osd-file-using-a-text-editor.md)

[<span data-ttu-id="a393e-135">Элементы файлов OSD</span><span class="sxs-lookup"><span data-stu-id="a393e-135">OSD File Elements</span></span>](osd-file-elements.md)

[<span data-ttu-id="a393e-136">Консоль Sequencer</span><span class="sxs-lookup"><span data-stu-id="a393e-136">Sequencer Console</span></span>](sequencer-console.md)

 

 





