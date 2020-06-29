---
title: Просмотр и настройка приложений и расширений виртуальных приложений по умолчанию с помощью консоли управления
description: Просмотр и настройка приложений и расширений виртуальных приложений по умолчанию с помощью консоли управления
author: dansimp
ms.assetid: c77e6662-7a18-4da1-8da8-b58068b65fa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c5a8cd5c914d1ddd720ebfef318e3a094cdc6f0b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813621"
---
# <span data-ttu-id="71910-103">Просмотр и настройка приложений и расширений виртуальных приложений по умолчанию с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="71910-103">How to View and Configure Applications and Default Virtual Application Extensions by Using the Management Console</span></span>


<span data-ttu-id="71910-104">Чтобы просмотреть и настроить расширения пакетов по умолчанию, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="71910-104">Use the following procedure to view and configure default package extensions.</span></span>

**<span data-ttu-id="71910-105">Просмотр и настройка расширений виртуальных приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="71910-105">To view and configure default virtual application extensions</span></span>**

1.  <span data-ttu-id="71910-106">Чтобы просмотреть пакет, который вы хотите настроить, откройте консоль управления App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="71910-106">To view the package that you want to configure, open the App-V 5.0 Management Console.</span></span> <span data-ttu-id="71910-107">Выберите пакет, который вы хотите настроить, щелкните правой кнопкой мыши имя пакета и выберите пункт **изменить конфигурацию по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="71910-107">Select the package that you want to configure, right-click the package name and select **edit default configuration**.</span></span>

2.  <span data-ttu-id="71910-108">Чтобы просмотреть приложения, содержащиеся в указанном пакете, в области **Конфигурация по умолчанию** выберите пункт **приложения**.</span><span class="sxs-lookup"><span data-stu-id="71910-108">To view the applications contained in the specified package, in the **Default Configuration** pane, click **Applications**.</span></span> <span data-ttu-id="71910-109">Для просмотра сочетаний клавиш для этого пакета нажмите кнопку **сочетания клавиш**.</span><span class="sxs-lookup"><span data-stu-id="71910-109">To view the shortcuts for that package, click **Shortcuts**.</span></span> <span data-ttu-id="71910-110">Чтобы просмотреть сопоставления типов файлов для этого пакета, выберите **типы файлов**.</span><span class="sxs-lookup"><span data-stu-id="71910-110">To view the file type associations for that package, click **File Types**.</span></span>

3.  <span data-ttu-id="71910-111">Чтобы включить расширения приложения, нажмите кнопку **включить**.</span><span class="sxs-lookup"><span data-stu-id="71910-111">To enable the application extensions, select **ENABLE**.</span></span>

    <span data-ttu-id="71910-112">Чтобы включить сочетания клавиш, выберите **включить СОЧЕТАНИЯ клавиш**.</span><span class="sxs-lookup"><span data-stu-id="71910-112">To enable shortcuts, select **ENABLE SHORTCUTS**.</span></span> <span data-ttu-id="71910-113">Чтобы добавить новый ярлык для выбранного приложения, щелкните его правой кнопкой мыши в области **ярлыков** и выберите команду **Добавить новый ярлык**.</span><span class="sxs-lookup"><span data-stu-id="71910-113">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane and select **Add new shortcut**.</span></span> <span data-ttu-id="71910-114">Чтобы удалить ярлык, щелкните его правой кнопкой мыши в области **ярлыков** и выберите команду **удалить ярлык**.</span><span class="sxs-lookup"><span data-stu-id="71910-114">To remove a shortcut, right-click the application in the **SHORTCUTS** pane and select **Remove Shortcut**.</span></span> <span data-ttu-id="71910-115">Чтобы изменить существующий ярлык, щелкните его правой кнопкой мыши и выберите команду **изменить ярлык**.</span><span class="sxs-lookup"><span data-stu-id="71910-115">To edit an existing shortcut, right-click the application and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="71910-116">Чтобы просмотреть другие расширения приложения, нажмите кнопку **Дополнительно** и выберите пункт **Экспорт конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="71910-116">To view any other application extensions, click **Advanced** and click **Export Configuration**.</span></span> <span data-ttu-id="71910-117">Введите имя файла и нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="71910-117">Type in a filename and click **Save**.</span></span> <span data-ttu-id="71910-118">С помощью файла конфигурации можно просмотреть все расширения приложений, связанные с пакетом.</span><span class="sxs-lookup"><span data-stu-id="71910-118">You can view all application extensions associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="71910-119">Чтобы изменить другие расширения приложения, измените файл конфигурации и нажмите кнопку **Импорт и перезапись конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="71910-119">To edit other application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="71910-120">Выберите измененный файл и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="71910-120">Select the modified file and click **Open**.</span></span> <span data-ttu-id="71910-121">В диалоговом окне нажмите кнопку **Перезаписать** , чтобы завершить процесс.</span><span class="sxs-lookup"><span data-stu-id="71910-121">In the dialog box, click **Overwrite** to complete the process.</span></span>

    <span data-ttu-id="71910-122">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="71910-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="71910-123">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="71910-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="71910-124">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="71910-124">Got an App-V issue?</span></span>** <span data-ttu-id="71910-125">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="71910-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="71910-126">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="71910-126">Related topics</span></span>


[<span data-ttu-id="71910-127">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="71910-127">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





