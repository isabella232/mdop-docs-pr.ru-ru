---
title: 'Панель "Результаты: политики поставщика"'
description: 'Панель "Результаты: политики поставщика"'
author: dansimp
ms.assetid: 17ea0836-bfb5-4966-8778-155444d81e64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97e7497617d19c09291104fce237b030a149e743
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815822"
---
# <span data-ttu-id="39ecc-103">Панель "Результаты: политики поставщика"</span><span class="sxs-lookup"><span data-stu-id="39ecc-103">Provider Policies Results Pane</span></span>


<span data-ttu-id="39ecc-104">На панели **результатов политик провайдеров** в консоли управления сервером виртуализации приложений отображается список доступных политик поставщиков.</span><span class="sxs-lookup"><span data-stu-id="39ecc-104">The **Provider Policies Results** pane in the Application Virtualization Server Management Console displays a list of the available provider policies.</span></span>

<span data-ttu-id="39ecc-105">Щелкните правой кнопкой мыши политику поставщика для отображения указанных ниже элементов.</span><span class="sxs-lookup"><span data-stu-id="39ecc-105">Right-click any provider policy to display the following elements.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="39ecc-106">Delete</span><span class="sxs-lookup"><span data-stu-id="39ecc-106">Delete</span></span>**  
<span data-ttu-id="39ecc-107">Этот элемент меню позволяет удалить политику поставщика из области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="39ecc-107">This menu item enables you to delete a provider policy from the **Results** pane.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="39ecc-108">Rename</span><span class="sxs-lookup"><span data-stu-id="39ecc-108">Rename</span></span>**  
<span data-ttu-id="39ecc-109">Этот элемент меню позволяет изменить имя политики поставщика в области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="39ecc-109">This menu item enables you to change the name of a provider policy in the **Results** pane.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="39ecc-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="39ecc-110">Properties</span></span>**  
<span data-ttu-id="39ecc-111">Этот элемент меню отображает диалоговое окно " **Свойства** " для выбранной политики поставщика.</span><span class="sxs-lookup"><span data-stu-id="39ecc-111">This menu item displays the **Properties** dialog box for the selected provider policy.</span></span> <span data-ttu-id="39ecc-112">В диалоговом окне **Свойства** указаны следующие вкладки:</span><span class="sxs-lookup"><span data-stu-id="39ecc-112">The **Properties** dialog box has the following tabs:</span></span>

-   <span data-ttu-id="39ecc-113">**General (общие**) — позволяет выбрать элемент **Управление рабочим столом на клиентском компьютере с помощью** **консоли управления** , если вы хотите централизованно управлять ярлыками на клиентских компьютерах в консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="39ecc-113">**General**—Enables you to select the **Manage client desktop using the** **Management Console** check box if you want to centrally manage shortcuts on the client desktops from the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="39ecc-114">Если вы решили управлять сочетаниями клавиш на консоли, вы можете установить флажки для обновления рабочего стола при каждом входе пользователя в систему и при указанном интервале времени.</span><span class="sxs-lookup"><span data-stu-id="39ecc-114">If you choose to manage shortcuts from the console, you can select check boxes to refresh the desktop every time a user logs in and at intervals you specify.</span></span>

-   <span data-ttu-id="39ecc-115">**Групповое назначение**— позволяет добавлять и удалять группы пользователей, назначенные политике поставщика.</span><span class="sxs-lookup"><span data-stu-id="39ecc-115">**Group Assignment**—Enables you to add and remove user groups assigned to the provider policy.</span></span>

-   <span data-ttu-id="39ecc-116">**Конвейер поставщика**— позволяет указать необходимый способ проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="39ecc-116">**Provider Pipeline**—Enables you to specify the authentication required.</span></span>

    -   <span data-ttu-id="39ecc-117">Установите нужные флажки, чтобы **задать параметры разрешений на доступ**, **сведения об использовании**и **Лицензирование**.</span><span class="sxs-lookup"><span data-stu-id="39ecc-117">Select the desired check boxes for **Enforce Access Permission Settings**, **Log Usage Information**, and **Licensing**.</span></span> <span data-ttu-id="39ecc-118">Если вы установите флажок **Лицензирование** , в раскрывающемся списке выберите пункт **Аудит использования лицензий** или **принудительные политики лицензий** .</span><span class="sxs-lookup"><span data-stu-id="39ecc-118">If you select the **Licensing** check box, select **Audit License Usage Only** or **Enforce License Policies** from the drop-down list.</span></span> <span data-ttu-id="39ecc-119">Первый вариант отслеживает использование лицензий, а второй параметр — исключительно принудительное применение политики лицензирования.</span><span class="sxs-lookup"><span data-stu-id="39ecc-119">The first option monitors license usage, while the second option strictly enforces your licensing policy.</span></span> <span data-ttu-id="39ecc-120">Нажмите кнопку **Готово**, а затем прочтите запрос и нажмите кнопку **ОК** , чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="39ecc-120">Click **Finish**, and then read the prompt and click **OK** to continue.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="39ecc-121">Help</span><span class="sxs-lookup"><span data-stu-id="39ecc-121">Help</span></span>**  
<span data-ttu-id="39ecc-122">Вывод справочной системы для консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="39ecc-122">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="39ecc-123">Щелкните правой кнопкой мыши в любом месте области **результатов** , кроме политики поставщика, чтобы отобразить всплывающее меню, содержащее следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="39ecc-123">Right-click anywhere in the **Results** pane, except on a provider policy, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="39ecc-124">Обновить</span><span class="sxs-lookup"><span data-stu-id="39ecc-124">Refresh</span></span>**  
<span data-ttu-id="39ecc-125">Выберите этот пункт меню, чтобы обновить представление политик поставщика.</span><span class="sxs-lookup"><span data-stu-id="39ecc-125">Select this menu item to refresh the view of the provider policies.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="39ecc-126">Экспорт списка</span><span class="sxs-lookup"><span data-stu-id="39ecc-126">Export List</span></span>**  
<span data-ttu-id="39ecc-127">С помощью этого элемента меню можно создать текстовый файл с разделителями-знаками табуляции, который будет содержать содержимое области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="39ecc-127">With this menu item, you can create a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="39ecc-128">Этот элемент отображает диалоговое окно " **Сохранение файла** ", в котором указывается расположение для текстового файла, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="39ecc-128">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="39ecc-129">Просмотр</span><span class="sxs-lookup"><span data-stu-id="39ecc-129">View</span></span>**  
<span data-ttu-id="39ecc-130">Этот элемент меню позволяет изменить внешний вид и содержимое области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="39ecc-130">This menu item lets you change the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="39ecc-131">Значки "упорядочить/выровнять вверх"</span><span class="sxs-lookup"><span data-stu-id="39ecc-131">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="39ecc-132">Эти элементы меню можно использовать для изменения способа отображения значков в области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="39ecc-132">These menu items can be used to change how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="39ecc-133">Help</span><span class="sxs-lookup"><span data-stu-id="39ecc-133">Help</span></span>**  
<span data-ttu-id="39ecc-134">Вывод справочной системы консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="39ecc-134">Displays the help system of the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="39ecc-135">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="39ecc-135">Related topics</span></span>


[<span data-ttu-id="39ecc-136">Консоль управления серверами: узел политик поставщика</span><span class="sxs-lookup"><span data-stu-id="39ecc-136">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





