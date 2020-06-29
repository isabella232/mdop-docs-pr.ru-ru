---
title: Узел сопоставления типов файлов
description: Узел сопоставления типов файлов
author: dansimp
ms.assetid: 48e4d9eb-00bd-4231-a68a-f8597ab683ff
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d94621a1d418f0af29ef9e73b8d430c81a7181c8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821532"
---
# <span data-ttu-id="2ba0a-103">Узел сопоставления типов файлов</span><span class="sxs-lookup"><span data-stu-id="2ba0a-103">File Type Associations Node</span></span>


<span data-ttu-id="2ba0a-104">Узел " **сопоставления типов файлов** " находится на одном уровне под узлом **Application Virtualization** в области **область** консоли управления клиентом Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-104">The **File Type Associations** node is one level below the **Application Virtualization** node in the **Scope** pane of the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="2ba0a-105">При выборе этого узла в области **результатов** отображается список сопоставлений типов файлов.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-105">When you select this node, the **Results** pane displays a list of file type associations.</span></span>

<span data-ttu-id="2ba0a-106">Щелкните правой кнопкой мыши узел **сопоставления типов файлов** , чтобы открыть всплывающее меню, содержащее указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-106">Right-click the **File Type Associations** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-association"></a>**<span data-ttu-id="2ba0a-107">Новая ассоциация</span><span class="sxs-lookup"><span data-stu-id="2ba0a-107">New Association</span></span>**  
<span data-ttu-id="2ba0a-108">Этот элемент меню отображает мастер создания ассоциаций.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-108">This menu item displays the New Association Wizard.</span></span> <span data-ttu-id="2ba0a-109">Этот мастер состоит из двух страниц:</span><span class="sxs-lookup"><span data-stu-id="2ba0a-109">This wizard consists of two pages:</span></span>

1.  <span data-ttu-id="2ba0a-110">Введите новое или существующее расширение имени файла и свяжите расширение с типом файла:</span><span class="sxs-lookup"><span data-stu-id="2ba0a-110">Enter a new or existing file name extension, and associate the extension with a file type:</span></span>

    -   <span data-ttu-id="2ba0a-111">**Расширение**: введите новое или существующее расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-111">**Extension**—Enter a new or existing file name extension.</span></span> <span data-ttu-id="2ba0a-112">По умолчанию это поле оставлено пустым.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-112">This field is blank by default.</span></span>

    -   <span data-ttu-id="2ba0a-113">**Создайте новый тип файлов с помощью этого описания**: Выберите этот переключатель, чтобы ввести новое описание типа файла в поле активно.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-113">**Create a new file type with this description**—Select this radio button to enter a new file type description in the active field.</span></span> <span data-ttu-id="2ba0a-114">Эта кнопка выбрана по умолчанию, а активное поле пусто.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-114">This button is selected by default, and the active field is blank.</span></span>

    -   <span data-ttu-id="2ba0a-115">**Применить этот тип файла ко всем пользователям**— установите этот флажок, если вы хотите, чтобы эта ассоциация была глобальной для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-115">**Apply this file type to all users**—Select this check box when you want this association to be global for all users.</span></span> <span data-ttu-id="2ba0a-116">По умолчанию этот флажок не установлен.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-116">By default, this box is not selected.</span></span>

    -   <span data-ttu-id="2ba0a-117">**Свяжите это расширение с существующим типом файлов**— выберите этот переключатель, чтобы связать расширение с существующим типом файла.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-117">**Link this extension with an existing file type**—Select this radio button to associate the extension with an existing file type.</span></span> <span data-ttu-id="2ba0a-118">Выберите тип файла из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-118">Choose a file type from the drop-down list.</span></span> <span data-ttu-id="2ba0a-119">Если выбрать этот параметр, команда **Далее** изменится на **"Готово"**.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-119">When you choose this option, **Next** is changed to **Finish**.</span></span>

2.  <span data-ttu-id="2ba0a-120">Выберите приложение, которое будет открывать файлы с указанным расширением:</span><span class="sxs-lookup"><span data-stu-id="2ba0a-120">Select the application that will open files with the specified extension:</span></span>

    -   <span data-ttu-id="2ba0a-121">**Открытие файлов с помощью выбранного приложения**— выберите этот переключатель, чтобы открыть файл в существующем приложении.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-121">**Open files with the selected application**—Select this radio button to open the file with an existing application.</span></span> <span data-ttu-id="2ba0a-122">Выберите приложение из раскрывающегося списка доступных приложений.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-122">Choose an application from the drop-down list of available applications.</span></span>

    -   <span data-ttu-id="2ba0a-123">**Открытие файлов с помощью приложения, описанного в этом OSD-файле**. Выберите этот переключатель, чтобы задать файл дескриптора программного обеспечения (OSD), определяющий приложение, которое использовалось для открытия файла.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-123">**Open files with the application described in this OSD file**—Select this radio button to specify an Open Software Descriptor (OSD) file that determines the application used to open the file.</span></span> <span data-ttu-id="2ba0a-124">Выберите существующее расположение или введите в это поле путь или URL-адрес в формате HTTP.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-124">Browse to select an existing location, or enter a path or HTTP-formatted URL in this field.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="2ba0a-125">Новое окно</span><span class="sxs-lookup"><span data-stu-id="2ba0a-125">New Window from Here</span></span>**  
<span data-ttu-id="2ba0a-126">Выберите этот пункт меню, чтобы открыть новую консоль управления с выбранным узлом в качестве корневого узла.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-126">Select this menu item to open a new management console with the selected node as the root node.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="2ba0a-127">Экспорт списка</span><span class="sxs-lookup"><span data-stu-id="2ba0a-127">Export List</span></span>**  
<span data-ttu-id="2ba0a-128">С помощью этого элемента меню можно создать текстовый файл с разделителями-знаками табуляции, содержащий содержимое области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="2ba0a-128">You can use this menu item to create a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="2ba0a-129">Этот элемент отображает диалоговое окно " **Сохранение файла** ", в котором указывается расположение для текстового файла, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-129">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="2ba0a-130">Просмотр</span><span class="sxs-lookup"><span data-stu-id="2ba0a-130">View</span></span>**  
<span data-ttu-id="2ba0a-131">Этот всплывающий список элементов меню позволяет изменять внешний вид и содержимое области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="2ba0a-131">This pop-up list of menu items enables you to change the appearance and content of the **Results** pane.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="2ba0a-132">Обновить</span><span class="sxs-lookup"><span data-stu-id="2ba0a-132">Refresh</span></span>**  
<span data-ttu-id="2ba0a-133">Выберите этот элемент, чтобы обновить консоль управления.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-133">Select this item to refresh the management console.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="2ba0a-134">Help</span><span class="sxs-lookup"><span data-stu-id="2ba0a-134">Help</span></span>**  
<span data-ttu-id="2ba0a-135">С помощью этого элемента меню можно отобразить справочную систему для консоли управления.</span><span class="sxs-lookup"><span data-stu-id="2ba0a-135">With this menu item, you can display the help system for the management console.</span></span>

## <span data-ttu-id="2ba0a-136">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2ba0a-136">Related topics</span></span>


[<span data-ttu-id="2ba0a-137">Панель "Результаты: сопоставления типов файлов"</span><span class="sxs-lookup"><span data-stu-id="2ba0a-137">File Type Association Results Pane</span></span>](file-type-association-results-pane.md)

[<span data-ttu-id="2ba0a-138">Столбцы панели "Результаты: сопоставления типов файлов"</span><span class="sxs-lookup"><span data-stu-id="2ba0a-138">File Type Association Results Pane Columns</span></span>](file-type-association-results-pane-columns.md)

 

 





