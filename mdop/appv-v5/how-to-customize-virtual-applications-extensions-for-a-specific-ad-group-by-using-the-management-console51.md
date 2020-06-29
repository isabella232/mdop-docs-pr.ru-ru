---
title: Настройка расширений виртуальных приложений для определенной группы AD с помощью консоли управления
description: Настройка расширений виртуальных приложений для определенной группы AD с помощью консоли управления
author: dansimp
ms.assetid: dd71df05-512f-4eb4-a55f-e5b93601323d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bf086da3fbb6938a4fc602af5ab63adb1621532
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814256"
---
# <span data-ttu-id="40185-103">Настройка расширений виртуальных приложений для определенной группы AD с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="40185-103">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>


<span data-ttu-id="40185-104">Чтобы настроить расширения виртуальных приложений для группы Active Directory (AD), выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="40185-104">Use the following procedure to customize the virtual application extensions for an Active Directory (AD) group.</span></span>

**<span data-ttu-id="40185-105">Настройка расширений виртуальных приложений для группы AD</span><span class="sxs-lookup"><span data-stu-id="40185-105">To customize virtual applications extensions for an AD group</span></span>**

1.  <span data-ttu-id="40185-106">Чтобы просмотреть пакет, который вы хотите настроить, откройте консоль управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="40185-106">To view the package that you want to configure, open the App-V 5.1 Management Console.</span></span> <span data-ttu-id="40185-107">Чтобы просмотреть конфигурацию, назначенную данной группе пользователей, выберите пакет и щелкните правой кнопкой мыши имя пакета и выберите пункт **изменить доступ к Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="40185-107">To view the configuration that is assigned to a given user group, select the package, and right-click the package name and select **Edit active directory access**.</span></span> <span data-ttu-id="40185-108">Кроме того, можно выбрать пакет и нажать кнопку **изменить** на панели **AD Access** .</span><span class="sxs-lookup"><span data-stu-id="40185-108">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="40185-109">Чтобы настроить группу БАННЕРов, вы можете найти ее в списке **сущностей рекламных объявлений с Access**.</span><span class="sxs-lookup"><span data-stu-id="40185-109">To customize an AD group, you can find the group from the list of **AD Entities with Access**.</span></span> <span data-ttu-id="40185-110">Затем с помощью раскрывающегося списка в области **назначенная конфигурация** выберите пункт **Настраиваемая**и нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="40185-110">Then, using the drop-down box in the **Assigned Configuration** pane, select **Custom**, and then click **EDIT**.</span></span>

3.  <span data-ttu-id="40185-111">Чтобы отключить все расширения для данного приложения, снимите флажок **включить**.</span><span class="sxs-lookup"><span data-stu-id="40185-111">To disable all extensions for a given application, clear **ENABLE**.</span></span>

    <span data-ttu-id="40185-112">Чтобы добавить новое сочетание клавиш для выбранного приложения, щелкните его правой кнопкой мыши в области **ярлыков** и выберите команду **Добавить новый ярлык**.</span><span class="sxs-lookup"><span data-stu-id="40185-112">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane, and select **Add new shortcut**.</span></span> <span data-ttu-id="40185-113">Чтобы удалить ярлык, щелкните его правой кнопкой мыши в области **ярлыков** и выберите команду **удалить ярлык**.</span><span class="sxs-lookup"><span data-stu-id="40185-113">To remove a shortcut, right-click the application in the **SHORTCUTS** pane, and select **Remove Shortcut**.</span></span> <span data-ttu-id="40185-114">Чтобы изменить существующий ярлык, щелкните приложение правой кнопкой мыши и выберите команду **изменить ярлык**.</span><span class="sxs-lookup"><span data-stu-id="40185-114">To edit an existing shortcut, right-click the application, and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="40185-115">Чтобы просмотреть другие расширения приложения, нажмите кнопку **Дополнительно**и выберите пункт **Экспорт конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="40185-115">To view any other application extensions, click **Advanced**, and click **Export Configuration**.</span></span> <span data-ttu-id="40185-116">Введите имя файла и нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="40185-116">Type in a filename and click **Save**.</span></span> <span data-ttu-id="40185-117">С помощью файла конфигурации можно просмотреть все расширения приложений, связанные с пакетом.</span><span class="sxs-lookup"><span data-stu-id="40185-117">You can view all application extensions that are associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="40185-118">Чтобы изменить дополнительные расширения приложения, измените файл конфигурации и нажмите кнопку **Импорт и перезапись конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="40185-118">To edit additional application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="40185-119">Выберите измененный файл и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="40185-119">Select the modified file and click **Open**.</span></span> <span data-ttu-id="40185-120">В диалоговом окне нажмите кнопку **Перезаписать** , чтобы завершить процесс.</span><span class="sxs-lookup"><span data-stu-id="40185-120">In the dialog, click **Overwrite** to complete the process.</span></span>

    <span data-ttu-id="40185-121">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="40185-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="40185-122">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="40185-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="40185-123">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="40185-123">Got an App-V issue?</span></span>** <span data-ttu-id="40185-124">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="40185-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="40185-125">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="40185-125">Related topics</span></span>


[<span data-ttu-id="40185-126">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="40185-126">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





