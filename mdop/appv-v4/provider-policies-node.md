---
title: Узел политик поставщика
description: Узел политик поставщика
author: dansimp
ms.assetid: 89b47076-7732-4128-93cc-8e6d5b671c8e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221171b22471a4a8614b13023b24dd21fd571dd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815832"
---
# <span data-ttu-id="964ec-103">Узел политик поставщика</span><span class="sxs-lookup"><span data-stu-id="964ec-103">Provider Policies Node</span></span>


<span data-ttu-id="964ec-104">Узел **политики поставщика** — это один из уровней ниже узла системы Application Virtualization в области **область** консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="964ec-104">The **Provider Policies** node is one level below the Application Virtualization System node in the **Scope** pane in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="964ec-105">При выборе этого узла в области **результатов** отображается список политик поставщика.</span><span class="sxs-lookup"><span data-stu-id="964ec-105">When you select this node, the **Results** pane displays a list of provider policies.</span></span> <span data-ttu-id="964ec-106">Щелкните правой кнопкой мыши узел **политики поставщика** , чтобы открыть всплывающее меню, содержащее указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="964ec-106">Right-click the **Provider Policies** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-provider-policy"></a>**<span data-ttu-id="964ec-107">Новая политика поставщика</span><span class="sxs-lookup"><span data-stu-id="964ec-107">New Provider Policy</span></span>**  
<span data-ttu-id="964ec-108">Отображение мастера создания политики поставщика.</span><span class="sxs-lookup"><span data-stu-id="964ec-108">Displays the New Provider Policy Wizard.</span></span> <span data-ttu-id="964ec-109">Этот мастер состоит из следующих страниц:</span><span class="sxs-lookup"><span data-stu-id="964ec-109">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="964ec-110">Введите имя в поле **имя политики поставщика** .</span><span class="sxs-lookup"><span data-stu-id="964ec-110">Enter a name in the **Provider Policy Name** field.</span></span> <span data-ttu-id="964ec-111">Выберите " **Управление рабочим столом на клиентском компьютере" с помощью консоли управления** , если эта возможность нужна.</span><span class="sxs-lookup"><span data-stu-id="964ec-111">Select the **Manage client desktop using the Management Console** check box if you want that capability.</span></span> <span data-ttu-id="964ec-112">Установите один или оба указанных ниже флажка, если вы хотите применить соответствующие функции.</span><span class="sxs-lookup"><span data-stu-id="964ec-112">Select one or both of the following check boxes if you want the associated functionality:</span></span>

    -   **<span data-ttu-id="964ec-113">Обновление конфигурации публикации при входе пользователя</span><span class="sxs-lookup"><span data-stu-id="964ec-113">Refresh publishing configuration when a user logs in</span></span>**

    -   <span data-ttu-id="964ec-114">**Обновлять конфигурацию каждые**.</span><span class="sxs-lookup"><span data-stu-id="964ec-114">**Refresh configuration every**.</span></span> <span data-ttu-id="964ec-115">После выбора этого параметра введите номер и выберите единицу в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="964ec-115">After selecting this option, enter a number and select the unit from the drop-down menu.</span></span> <span data-ttu-id="964ec-116">Диапазон допустимых записей не должен превышать **30 минут** в течение не менее **999 дней**.</span><span class="sxs-lookup"><span data-stu-id="964ec-116">Valid entries range from a minimum of **30 minutes** to a maximum of **999 days**.</span></span>

2.  <span data-ttu-id="964ec-117">Нажмите кнопку **Добавить** или **Удалить** , чтобы добавить или удалить назначение группы.</span><span class="sxs-lookup"><span data-stu-id="964ec-117">Click **Add** or **Remove** to add or remove a group assignment.</span></span> <span data-ttu-id="964ec-118">Используйте стандартное диалоговое окно " **Обзор** " для поиска группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="964ec-118">Use the standard **Windows Browse** dialog box to find a user group.</span></span>

3.  <span data-ttu-id="964ec-119">Установите один из указанных ниже флажков в диалоговом окне **Настройка конвейера поставщика** , чтобы включить соответствующую функцию.</span><span class="sxs-lookup"><span data-stu-id="964ec-119">Select one of the following check boxes on the **Provider Pipeline Configuration** dialog box to enable the associated feature:</span></span>

    -   <span data-ttu-id="964ec-120">**Проверка подлинности**— выберите тип проверки подлинности из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="964ec-120">**Authentication**—Select the type of authentication from the drop-down list.</span></span>

    -   **<span data-ttu-id="964ec-121">Принудительная установка разрешений на доступ</span><span class="sxs-lookup"><span data-stu-id="964ec-121">Enforce Access Permission Settings</span></span>**

    -   **<span data-ttu-id="964ec-122">Ведение журнала сведений об использовании</span><span class="sxs-lookup"><span data-stu-id="964ec-122">Log Usage Information</span></span>**

    -   <span data-ttu-id="964ec-123">**Лицензирование**: выберите схему принудительного применения из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="964ec-123">**Licensing**—Select an enforcement scheme from the drop-down list.</span></span>

4.  <span data-ttu-id="964ec-124">Нажмите кнопку **Готово** , чтобы добавить новую политику поставщика.</span><span class="sxs-lookup"><span data-stu-id="964ec-124">Click **Finish** to add the new provider policy.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="964ec-125">Просмотр</span><span class="sxs-lookup"><span data-stu-id="964ec-125">View</span></span>**  
<span data-ttu-id="964ec-126">Изменение внешнего вида и содержимого области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="964ec-126">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="964ec-127">Новое окно</span><span class="sxs-lookup"><span data-stu-id="964ec-127">New Window from Here</span></span>**  
<span data-ttu-id="964ec-128">Открытие новой консоли управления с выбранным узлом в качестве корневого узла.</span><span class="sxs-lookup"><span data-stu-id="964ec-128">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="964ec-129">Обновить</span><span class="sxs-lookup"><span data-stu-id="964ec-129">Refresh</span></span>**  
<span data-ttu-id="964ec-130">Обновляет представление сервера.</span><span class="sxs-lookup"><span data-stu-id="964ec-130">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="964ec-131">Экспорт списка</span><span class="sxs-lookup"><span data-stu-id="964ec-131">Export List</span></span>**  
<span data-ttu-id="964ec-132">Создает текстовый файл с разделителями-знаками табуляции, который включает содержимое области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="964ec-132">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="964ec-133">Этот элемент отображает диалоговое окно " **Сохранение файла** ", в котором указывается расположение для текстового файла, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="964ec-133">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="964ec-134">Help</span><span class="sxs-lookup"><span data-stu-id="964ec-134">Help</span></span>**  
<span data-ttu-id="964ec-135">Вывод справочной системы для консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="964ec-135">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="964ec-136">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="964ec-136">Related topics</span></span>


[<span data-ttu-id="964ec-137">Консоль управления серверами: узел политик поставщика</span><span class="sxs-lookup"><span data-stu-id="964ec-137">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





