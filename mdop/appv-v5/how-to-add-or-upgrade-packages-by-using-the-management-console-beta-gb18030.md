---
title: Добавление или обновление пакетов с помощью консоли управления
description: Добавление или обновление пакетов с помощью консоли управления
author: dansimp
ms.assetid: 4e389d7e-f402-44a7-bc4c-42c2a8440573
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 583ac07168c44c7d0a605b81512ae01a6d979db2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814469"
---
# <span data-ttu-id="cb969-103">Добавление или обновление пакетов с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="cb969-103">How to Add or Upgrade Packages by Using the Management Console</span></span>


<span data-ttu-id="cb969-104">Чтобы добавить или обновить пакет на консоли управления App-V 5,0, можно выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cb969-104">You can the following procedure to add or upgrade a package to the App-V 5.0 Management Console.</span></span> <span data-ttu-id="cb969-105">Чтобы обновить пакет, уже существующий на консоли управления, выполните указанные ниже действия и Импортируйте обновленный пакет, используя то же **имя**пакета.</span><span class="sxs-lookup"><span data-stu-id="cb969-105">To upgrade a package that already exists in the Management Console, use the following steps and import the upgraded package using the same package **Name**.</span></span>

**<span data-ttu-id="cb969-106">Добавление пакета на консоль управления</span><span class="sxs-lookup"><span data-stu-id="cb969-106">To add a package to the Management Console</span></span>**

1.  <span data-ttu-id="cb969-107">Откройте вкладку **пакеты** в области навигации экрана консоли управления.</span><span class="sxs-lookup"><span data-stu-id="cb969-107">Click the **Packages** tab in the navigation pane of the Management Console display.</span></span>

    <span data-ttu-id="cb969-108">На консоли отображается список пакетов, добавленных на сервер, а также сведения о состоянии каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="cb969-108">The console displays the list of packages that have been added to the server along with status information about each package.</span></span> <span data-ttu-id="cb969-109">При выборе пакета подробные сведения о нем выводятся на панели **пакеты** .</span><span class="sxs-lookup"><span data-stu-id="cb969-109">When a package is selected, detailed information about the package is displayed in the **PACKAGES** pane.</span></span>

    <span data-ttu-id="cb969-110">Щелкните раскрывающийся список **разгруппировка** и укажите, как пакеты должны отображаться на консоли.</span><span class="sxs-lookup"><span data-stu-id="cb969-110">Click the **Ungrouped** drop-down list box and specify how the packages are to be displayed in the console.</span></span> <span data-ttu-id="cb969-111">Вы также можете щелкнуть заголовок соответствующего столбца, чтобы отсортировать пакеты.</span><span class="sxs-lookup"><span data-stu-id="cb969-111">You can also click the associated column header to sort the packages.</span></span>

2.  <span data-ttu-id="cb969-112">Чтобы указать пакет, который нужно добавить, нажмите кнопку **Добавить или обновить пакеты**.</span><span class="sxs-lookup"><span data-stu-id="cb969-112">To specify the package you want to add, click **Add or Upgrade Packages**.</span></span>

3.  <span data-ttu-id="cb969-113">Введите полный путь к пакету, который вы хотите добавить.</span><span class="sxs-lookup"><span data-stu-id="cb969-113">Type the full path to the package that you want to add.</span></span> <span data-ttu-id="cb969-114">Используйте формат пути UNC или HTTP (например, **\\\\servername\\sharename\\foldername\\packagename.AppV** ) или **http://server.1234/file.appv** , а затем нажмите кнопку **добавить**.</span><span class="sxs-lookup"><span data-stu-id="cb969-114">Use the UNC or HTTP path format, for example **\\\\servername\\sharename\\foldername\\packagename.appv** or **http://server.1234/file.appv**, and then click **Add**.</span></span>

    <span data-ttu-id="cb969-115">**Важно!**  Необходимо выбрать пакет с расширением имени файла **. AppV** .</span><span class="sxs-lookup"><span data-stu-id="cb969-115">**Important** You must select a package with the **.appv** file name extension.</span></span>

     

4.  <span data-ttu-id="cb969-116">На странице отобразится сообщение о состоянии, \*\*добавляющее &lt; PackageName &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="cb969-116">The page displays the status message **Adding &lt;Packagename&gt;**.</span></span> <span data-ttu-id="cb969-117">Нажмите кнопку **ИМПОРТИРОВАТЬ состояние** , чтобы проверить состояние импортированного пакета.</span><span class="sxs-lookup"><span data-stu-id="cb969-117">Click **IMPORT STATUS** to check the status of a package that you have imported.</span></span>

    <span data-ttu-id="cb969-118">Нажмите кнопку **ОК** , чтобы добавить пакет и закрыть страницу **Добавить пакет** .</span><span class="sxs-lookup"><span data-stu-id="cb969-118">Click **OK** to add the package and close the **Add Package** page.</span></span> <span data-ttu-id="cb969-119">Если во время импорта возникла ошибка, нажмите **Подробности** на странице **Импорт пакета** для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="cb969-119">If there was an error during the import, click **Detail** on the **Package Import** page for more information.</span></span> <span data-ttu-id="cb969-120">Недавно добавленный пакет теперь доступен на панели **пакеты** .</span><span class="sxs-lookup"><span data-stu-id="cb969-120">The newly added package is now available in the **PACKAGES** pane.</span></span>

5.  <span data-ttu-id="cb969-121">Нажмите кнопку **Закрыть** , чтобы закрыть страницу **Добавить или обновить пакеты** .</span><span class="sxs-lookup"><span data-stu-id="cb969-121">Click **Close** to close the **Add or Upgrade Packages** page.</span></span>

    <span data-ttu-id="cb969-122">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="cb969-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="cb969-123">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="cb969-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="cb969-124">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="cb969-124">Got an App-V issue?</span></span>** <span data-ttu-id="cb969-125">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="cb969-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="cb969-126">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="cb969-126">Related topics</span></span>


[<span data-ttu-id="cb969-127">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="cb969-127">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 




