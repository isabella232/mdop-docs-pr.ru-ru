---
title: Публикация ярлыков приложений
description: Публикация ярлыков приложений
author: dansimp
ms.assetid: fc5efe86-1bbe-438b-b7d8-4f9b815cc58e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eafdb85414a1a6cf3e1072fdc5532bcd04699653
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816842"
---
# <span data-ttu-id="0eef7-103">Публикация ярлыков приложений</span><span class="sxs-lookup"><span data-stu-id="0eef7-103">How to Publish Application Shortcuts</span></span>


<span data-ttu-id="0eef7-104">С помощью описанной ниже процедуры можно публиковать ярлыки приложений прямо из области **результатов** узла **приложения** на консоли управления клиентом Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="0eef7-104">You can use the following procedure to publish shortcuts to an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="0eef7-105">Публикация сочетаний клавиш для приложений</span><span class="sxs-lookup"><span data-stu-id="0eef7-105">To publish application shortcuts</span></span>**

1.  <span data-ttu-id="0eef7-106">Переместите курсор в область **результатов** , щелкните нужное приложение правой кнопкой мыши и выберите в контекстном меню команду **создать** ярлык, чтобы открыть мастер создания ярлыков.</span><span class="sxs-lookup"><span data-stu-id="0eef7-106">Move the cursor to the **Results** pane, right-click the desired application, and select **New Shortcut** from the pop-up menu to display the New Shortcut Wizard.</span></span>

2.  <span data-ttu-id="0eef7-107">На первой странице мастера создания ярлыков выберите значок и укажите имя для ярлыка.</span><span class="sxs-lookup"><span data-stu-id="0eef7-107">On the first page of the New Shortcut Wizard, select an icon and specify a name for the shortcut.</span></span>

    1.  <span data-ttu-id="0eef7-108">**Значок "изменить**" — отображает стандартный браузер значков Windows.</span><span class="sxs-lookup"><span data-stu-id="0eef7-108">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="0eef7-109">Перейдите к нужному значку и выберите его.</span><span class="sxs-lookup"><span data-stu-id="0eef7-109">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="0eef7-110">**Название ярлыка**: введите имя, которое вы хотите назначить сочетанию клавиш.</span><span class="sxs-lookup"><span data-stu-id="0eef7-110">**Shortcut Title**—Enter the name you want to give the shortcut.</span></span> <span data-ttu-id="0eef7-111">Это поле по умолчанию является существующим именем и версией приложения.</span><span class="sxs-lookup"><span data-stu-id="0eef7-111">This field defaults to the existing name and version of the application.</span></span>

3.  <span data-ttu-id="0eef7-112">На второй странице мастера определите расположение опубликованного ярлыка.</span><span class="sxs-lookup"><span data-stu-id="0eef7-112">On the second page of the wizard, determine the location of the published shortcut.</span></span>

    1.  <span data-ttu-id="0eef7-113">**Рабочий стол**— установите этот флажок, чтобы опубликовать ярлык на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="0eef7-113">**The Desktop**—Select this check box to publish the shortcut to the desktop.</span></span>

    2.  <span data-ttu-id="0eef7-114">**Панель быстрого запуска**— установите этот флажок, чтобы опубликовать ярлык на панели быстрого запуска.</span><span class="sxs-lookup"><span data-stu-id="0eef7-114">**The Quick Launch Toolbar**—Select this check box to publish the shortcut to the Quick Launch toolbar.</span></span>

    3.  <span data-ttu-id="0eef7-115">В **меню "Отправить**" — выберите этот флажок, чтобы опубликовать ярлык в меню " **Отправить** ".</span><span class="sxs-lookup"><span data-stu-id="0eef7-115">**The Send To Menu**—Select this check box to publish the shortcut to the **Send To** menu.</span></span>

    4.  <span data-ttu-id="0eef7-116">**Программы в меню "Пуск**" — это поле становится активным, если установлен флажок **меню "Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="0eef7-116">**Programs in the Start Menu**—When you select the **Start Menu** check box, this field becomes active.</span></span> <span data-ttu-id="0eef7-117">Оставьте это поле пустым, чтобы опубликовать ярлык прямо в корневом каталоге папки программы или введите имя папки или иерархии, например "My \ _Computer \\Officeные приложения".</span><span class="sxs-lookup"><span data-stu-id="0eef7-117">Leave this field blank to publish the shortcut directly to the root of the Programs folder, or enter a folder name or hierarchy—for example, "My\_Computer\\Office Applications."</span></span> <span data-ttu-id="0eef7-118">Сочетания клавиш, созданные таким образом, доступны только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="0eef7-118">Shortcuts created this way are available only for the current user.</span></span>

    5.  <span data-ttu-id="0eef7-119">**Другое расположение** и кнопка **обзора** — при установке **другого местоположения** это поле становится активным.</span><span class="sxs-lookup"><span data-stu-id="0eef7-119">**Another location** and **Browse** button—When you select the **Another location** check box, this field becomes active.</span></span> <span data-ttu-id="0eef7-120">Введите любое допустимое расположение на компьютере или любой доступный UNC-путь (общий файл или каталог в сети).</span><span class="sxs-lookup"><span data-stu-id="0eef7-120">Enter any valid location on the computer or any available UNC path (shared file or directory on a network).</span></span> <span data-ttu-id="0eef7-121">Кнопка " **Обзор** " отображает стандартное диалоговое окно **открытия файла** Windows.</span><span class="sxs-lookup"><span data-stu-id="0eef7-121">The **Browse** button displays a standard Windows **File Open** dialog box.</span></span>

4.  <span data-ttu-id="0eef7-122">На третьей странице мастера введите нужные параметры командной строки.</span><span class="sxs-lookup"><span data-stu-id="0eef7-122">On the third page of the wizard, enter desired command-line parameters.</span></span>

5.  <span data-ttu-id="0eef7-123">Нажмите кнопку **Готово** , чтобы опубликовать ярлыки и выйти в область **результатов** .</span><span class="sxs-lookup"><span data-stu-id="0eef7-123">Click **Finish** to publish the shortcuts and exit to the **Results** pane.</span></span>

## <span data-ttu-id="0eef7-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0eef7-124">Related topics</span></span>


[<span data-ttu-id="0eef7-125">Добавление сопоставления типов файлов</span><span class="sxs-lookup"><span data-stu-id="0eef7-125">How to Add a File Type Association</span></span>](how-to-add-a-file-type-association.md)

[<span data-ttu-id="0eef7-126">Добавление приложения</span><span class="sxs-lookup"><span data-stu-id="0eef7-126">How to Add an Application</span></span>](how-to-add-an-application.md)

[<span data-ttu-id="0eef7-127">Удаление сопоставления типов файлов</span><span class="sxs-lookup"><span data-stu-id="0eef7-127">How to Delete a File Type Association</span></span>](how-to-delete-a-file-type-association.md)

 

 





