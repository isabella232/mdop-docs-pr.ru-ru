---
title: 'Панель "Результаты: лицензии приложений"'
description: 'Панель "Результаты: лицензии приложений"'
author: dansimp
ms.assetid: 8b519715-b2fe-451e-ad9b-e9b73f454961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5a86c22e67e061ec873317c455958536fae75b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819509"
---
# <span data-ttu-id="07e66-103">Панель "Результаты: лицензии приложений"</span><span class="sxs-lookup"><span data-stu-id="07e66-103">Applications Licenses Results Pane</span></span>


<span data-ttu-id="07e66-104">На панели **результатов "лицензии приложений** " в консоли управления сервером виртуализации приложений отображается список доступных групп лицензий приложений и лицензий приложений.</span><span class="sxs-lookup"><span data-stu-id="07e66-104">The **Applications Licenses Results** pane in the Application Virtualization Server Management Console displays a list of the available application license groups and application licenses.</span></span>

<span data-ttu-id="07e66-105">Щелкните правой кнопкой мыши любую группу лицензий приложения, чтобы отобразить всплывающее меню, содержащее указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="07e66-105">Right-click any application license group to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-unlimited-license"></a>**<span data-ttu-id="07e66-106">Новая неограниченная лицензия</span><span class="sxs-lookup"><span data-stu-id="07e66-106">New Unlimited License</span></span>**  
<span data-ttu-id="07e66-107">Отображение нового мастера неограниченных лицензий.</span><span class="sxs-lookup"><span data-stu-id="07e66-107">Displays the New Unlimited License Wizard.</span></span> <span data-ttu-id="07e66-108">Этот параметр доступен только в том случае, если лицензионная группа не имеет лицензий.</span><span class="sxs-lookup"><span data-stu-id="07e66-108">This option is available only when the license group has no licenses.</span></span> <span data-ttu-id="07e66-109">Этот мастер состоит из трех страниц:</span><span class="sxs-lookup"><span data-stu-id="07e66-109">This wizard consists of three pages:</span></span>

1.  <span data-ttu-id="07e66-110">Введите имя группы в поле **имя группы лицензий приложений** и значение (в минутах) в поле **предупреждения об истечении срока действия лицензии** .</span><span class="sxs-lookup"><span data-stu-id="07e66-110">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="07e66-111">(Вы можете ввести любое значение от 0 до 100.) Вы также можете выбрать нужное количество минут с помощью стрелок вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="07e66-111">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="07e66-112">Введите краткий описательный текст в поле **Описание лицензии** и установите флажок **включено** .</span><span class="sxs-lookup"><span data-stu-id="07e66-112">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box.</span></span> <span data-ttu-id="07e66-113">Кроме того, можно использовать поле **Дата окончания** срока действия, чтобы задать дату окончания срока действия лицензии.</span><span class="sxs-lookup"><span data-stu-id="07e66-113">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="07e66-114">Вы можете установить флажок по умолчанию или воспользоваться служебной программой "Календарь", чтобы перейти к нужной дате окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="07e66-114">You can select the default check box or use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="07e66-115">Нажмите кнопку **Готово** , чтобы добавить новую лицензию.</span><span class="sxs-lookup"><span data-stu-id="07e66-115">Click **Finish** to add the new license.</span></span>

<a href="" id="new-concurrent-license"></a>**<span data-ttu-id="07e66-116">Новая лицензия для параллельных лицензий</span><span class="sxs-lookup"><span data-stu-id="07e66-116">New Concurrent License</span></span>**  
<span data-ttu-id="07e66-117">Отображение мастера создания лицензий с параллельной лицензией.</span><span class="sxs-lookup"><span data-stu-id="07e66-117">Displays the New Concurrent License Wizard.</span></span> <span data-ttu-id="07e66-118">Этот параметр доступен только в том случае, если лицензионная группа не имеет неограниченных лицензий.</span><span class="sxs-lookup"><span data-stu-id="07e66-118">This option is available only when the license group has no unlimited licenses.</span></span> <span data-ttu-id="07e66-119">Этот мастер состоит из следующих страниц и почти идентичен мастеру создания неограниченных лицензий.</span><span class="sxs-lookup"><span data-stu-id="07e66-119">This wizard consists of the following pages and is almost identical to the New Unlimited License Wizard:</span></span>

1.  <span data-ttu-id="07e66-120">Введите имя группы в поле **имя группы лицензий приложений** и значение (в минутах) в поле **предупреждения об истечении срока действия лицензии** .</span><span class="sxs-lookup"><span data-stu-id="07e66-120">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="07e66-121">(Вы можете ввести любое значение от 0 до 100.) Вы также можете выбрать нужное количество минут с помощью стрелок вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="07e66-121">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="07e66-122">Введите краткий описательный текст в поле **Описание лицензии** и введите значение в поле « **количество одновременных лицензий** ».</span><span class="sxs-lookup"><span data-stu-id="07e66-122">Enter brief descriptive text in the **License Description** field, and enter a value in the **Concurrent License Quantity** field.</span></span> <span data-ttu-id="07e66-123">Вы также можете использовать стрелки вверх и вниз, чтобы указать количество одновременных лицензий.</span><span class="sxs-lookup"><span data-stu-id="07e66-123">You can also use the up and down arrows to specify the number of concurrent licenses.</span></span> <span data-ttu-id="07e66-124">Установите флажок **включено** , чтобы включить лицензию.</span><span class="sxs-lookup"><span data-stu-id="07e66-124">Select the **Enabled** check box to enable the license.</span></span> <span data-ttu-id="07e66-125">Кроме того, вы можете использовать поле **Дата окончания срока** действия, чтобы выбрать дату окончания срока действия лицензии.</span><span class="sxs-lookup"><span data-stu-id="07e66-125">Optionally, you can use the **Expiration Date** field to select an expiration date for the license.</span></span> <span data-ttu-id="07e66-126">Вы можете установить флажок, чтобы использовать отображаемую дату окончания срока действия, или воспользоваться служебной программой "Календарь", чтобы перейти к нужной дате.</span><span class="sxs-lookup"><span data-stu-id="07e66-126">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="07e66-127">Нажмите кнопку **Готово** , чтобы добавить новые лицензии.</span><span class="sxs-lookup"><span data-stu-id="07e66-127">Click **Finish** to add the new licenses.</span></span>

<a href="" id="new-named-license"></a>**<span data-ttu-id="07e66-128">Новая именованная лицензия</span><span class="sxs-lookup"><span data-stu-id="07e66-128">New Named License</span></span>**  
<span data-ttu-id="07e66-129">Отображает мастер создания лицензии.</span><span class="sxs-lookup"><span data-stu-id="07e66-129">Displays the New Named License Wizard.</span></span> <span data-ttu-id="07e66-130">Этот параметр доступен только в том случае, если лицензионная группа не имеет неограниченных лицензий.</span><span class="sxs-lookup"><span data-stu-id="07e66-130">This option is available only when the license group has no unlimited licenses.</span></span> <span data-ttu-id="07e66-131">Этот мастер состоит из следующих страниц:</span><span class="sxs-lookup"><span data-stu-id="07e66-131">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="07e66-132">Введите имя группы в поле **имя группы лицензий приложений** и значение (в минутах) в поле **предупреждения об истечении срока действия лицензии** .</span><span class="sxs-lookup"><span data-stu-id="07e66-132">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="07e66-133">(Вы можете ввести любое значение от 0 до 100.) Вы также можете выбрать нужное количество минут с помощью стрелок вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="07e66-133">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="07e66-134">Введите краткий описательный текст в **описании лицензии**и установите флажок **Enabled (включено** ).</span><span class="sxs-lookup"><span data-stu-id="07e66-134">Enter brief descriptive text in the **License Description**, and select the **Enabled** check box.</span></span> <span data-ttu-id="07e66-135">Кроме того, можно использовать поле **Дата окончания** срока действия, чтобы задать дату окончания срока действия лицензии.</span><span class="sxs-lookup"><span data-stu-id="07e66-135">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="07e66-136">Вы можете установить флажок, чтобы использовать отображаемую дату окончания срока действия, или воспользоваться служебной программой "Календарь", чтобы перейти к нужной дате.</span><span class="sxs-lookup"><span data-stu-id="07e66-136">You can select the check box to use the displayed expiration date, or use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="07e66-137">Нажмите кнопку **Добавить**, **изменить**или **Удалить** именованных пользователей.</span><span class="sxs-lookup"><span data-stu-id="07e66-137">Click **Add**, **Edit**, or **Remove** named users.</span></span>

4.  <span data-ttu-id="07e66-138">Нажмите кнопку **Готово** , чтобы добавить новую лицензию.</span><span class="sxs-lookup"><span data-stu-id="07e66-138">Click **Finish** to add the new license.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="07e66-139">Новое окно</span><span class="sxs-lookup"><span data-stu-id="07e66-139">New Window from Here</span></span>**  
<span data-ttu-id="07e66-140">Открытие новой консоли управления с выбранным узлом в качестве корневого узла.</span><span class="sxs-lookup"><span data-stu-id="07e66-140">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="07e66-141">Delete</span><span class="sxs-lookup"><span data-stu-id="07e66-141">Delete</span></span>**  
<span data-ttu-id="07e66-142">Удаляет лицензионную группу из списка.</span><span class="sxs-lookup"><span data-stu-id="07e66-142">Deletes the license group from the list.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="07e66-143">Rename</span><span class="sxs-lookup"><span data-stu-id="07e66-143">Rename</span></span>**  
<span data-ttu-id="07e66-144">Изменение имени группы лицензирования приложений.</span><span class="sxs-lookup"><span data-stu-id="07e66-144">Changes the name of the applications license group.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="07e66-145">Свойства</span><span class="sxs-lookup"><span data-stu-id="07e66-145">Properties</span></span>**  
<span data-ttu-id="07e66-146">Отображает диалоговое окно " **Свойства** " для выбранных групп лицензирования приложений.</span><span class="sxs-lookup"><span data-stu-id="07e66-146">Displays the **Properties** dialog box for the selected application license groups.</span></span> <span data-ttu-id="07e66-147">Это диалоговое окно содержит следующие вкладки:</span><span class="sxs-lookup"><span data-stu-id="07e66-147">This dialog box has the following tabs:</span></span>

-   <span data-ttu-id="07e66-148">Вкладка " **Общие** " — отображает общие сведения о лицензионной группе.</span><span class="sxs-lookup"><span data-stu-id="07e66-148">**General** tab—Displays general information about the license group.</span></span> <span data-ttu-id="07e66-149">На этой вкладке можно изменить значение времени (в минутах) в поле **предупреждение об окончании срока действия лицензии** .</span><span class="sxs-lookup"><span data-stu-id="07e66-149">From this tab, you can change the time value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="07e66-150">Вы можете ввести любое значение от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="07e66-150">You can enter any value from 0–100.</span></span>

-   <span data-ttu-id="07e66-151">Вкладка " **приложения** " — отображает список приложений, связанных с лицензионной группой.</span><span class="sxs-lookup"><span data-stu-id="07e66-151">**Applications** tab—Displays the list of applications associated with the license group.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="07e66-152">Help</span><span class="sxs-lookup"><span data-stu-id="07e66-152">Help</span></span>**  
<span data-ttu-id="07e66-153">Вывод справочной системы консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="07e66-153">Displays the Application Virtualization Server Management Console help system.</span></span>

<span data-ttu-id="07e66-154">Когда в области **результатов** отображаются группы лицензий приложений, щелкните правой кнопкой мыши в любом месте области **результатов** , кроме лицензионной группы, чтобы отобразить всплывающее меню, содержащее указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="07e66-154">When the **Results** pane displays application license groups, right-click anywhere in the **Results** pane, except on a license group, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="07e66-155">Обновить</span><span class="sxs-lookup"><span data-stu-id="07e66-155">Refresh</span></span>**  
<span data-ttu-id="07e66-156">Обновляет представление сервера.</span><span class="sxs-lookup"><span data-stu-id="07e66-156">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="07e66-157">Экспорт списка</span><span class="sxs-lookup"><span data-stu-id="07e66-157">Export List</span></span>**  
<span data-ttu-id="07e66-158">Создает текстовый файл с разделителями-знаками табуляции, который включает содержимое области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="07e66-158">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="07e66-159">Этот элемент отображает диалоговое окно " **Сохранение файла** ", в котором указывается расположение для текстового файла, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="07e66-159">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="07e66-160">Просмотр</span><span class="sxs-lookup"><span data-stu-id="07e66-160">View</span></span>**  
<span data-ttu-id="07e66-161">Изменение внешнего вида и содержимого области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="07e66-161">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="07e66-162">Значки "упорядочить/выровнять вверх"</span><span class="sxs-lookup"><span data-stu-id="07e66-162">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="07e66-163">Изменение способа отображения значков в области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="07e66-163">Changes how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="07e66-164">Help</span><span class="sxs-lookup"><span data-stu-id="07e66-164">Help</span></span>**  
<span data-ttu-id="07e66-165">Вывод справочной системы для консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="07e66-165">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="07e66-166">Когда в области **результатов** отображаются лицензии, щелкните правой кнопкой мыши любую лицензию на приложение, чтобы отобразить всплывающее меню, содержащее указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="07e66-166">When the **Results** pane displays licenses, right-click any application license to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="07e66-167">Delete</span><span class="sxs-lookup"><span data-stu-id="07e66-167">Delete</span></span>**  
<span data-ttu-id="07e66-168">Удаление лицензии из списка.</span><span class="sxs-lookup"><span data-stu-id="07e66-168">Deletes the license from the list.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="07e66-169">Rename</span><span class="sxs-lookup"><span data-stu-id="07e66-169">Rename</span></span>**  
<span data-ttu-id="07e66-170">Изменение имени лицензии.</span><span class="sxs-lookup"><span data-stu-id="07e66-170">Changes the name of the license.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="07e66-171">Свойства</span><span class="sxs-lookup"><span data-stu-id="07e66-171">Properties</span></span>**  
<span data-ttu-id="07e66-172">Вывод диалогового окна " **Свойства** " для выбранной лицензии на приложение.</span><span class="sxs-lookup"><span data-stu-id="07e66-172">Displays the **Properties** dialog box for the selected application license.</span></span>

<span data-ttu-id="07e66-173">На вкладке " **Общие** " в диалоговом окне " **свойства** " отображаются сведения о лицензии и вы можете изменить состояние включения, дату окончания срока действия лицензии и данные ключа лицензии.</span><span class="sxs-lookup"><span data-stu-id="07e66-173">The **General** tab of the **Properties** dialog box displays information about the license and lets you change the enabled status, license expiration date, and license key information.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="07e66-174">Help</span><span class="sxs-lookup"><span data-stu-id="07e66-174">Help</span></span>**  
<span data-ttu-id="07e66-175">Вывод справочной системы консоли управления сервером.</span><span class="sxs-lookup"><span data-stu-id="07e66-175">Displays the server management console help system.</span></span>

<span data-ttu-id="07e66-176">Когда в области **результатов** отображаются лицензии, щелкните правой кнопкой мыши в области **результатов** (за исключением лицензии), чтобы отобразить всплывающее меню, содержащее указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="07e66-176">When the **Results** pane displays licenses, right-click anywhere in the **Results** pane, except on a license, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="07e66-177">Экспорт списка</span><span class="sxs-lookup"><span data-stu-id="07e66-177">Export List</span></span>**  
<span data-ttu-id="07e66-178">Создает текстовый файл с разделителями-знаками табуляции, который включает содержимое области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="07e66-178">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="07e66-179">Этот элемент отображает диалоговое окно " **Сохранение файла** ", в котором указывается расположение для текстового файла, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="07e66-179">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="07e66-180">Просмотр</span><span class="sxs-lookup"><span data-stu-id="07e66-180">View</span></span>**  
<span data-ttu-id="07e66-181">Изменение внешнего вида и содержимого области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="07e66-181">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="07e66-182">Значки "упорядочить/выровнять вверх"</span><span class="sxs-lookup"><span data-stu-id="07e66-182">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="07e66-183">Изменение способа отображения значков в области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="07e66-183">Changes how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="07e66-184">Свойства</span><span class="sxs-lookup"><span data-stu-id="07e66-184">Properties</span></span>**  
<span data-ttu-id="07e66-185">Вывод диалогового окна " **Свойства** " для выбранной лицензии.</span><span class="sxs-lookup"><span data-stu-id="07e66-185">Displays the **Properties** dialog box for the selected license.</span></span>

<span data-ttu-id="07e66-186">На вкладке " **Общие** " в диалоговом окне " **свойства** " отображаются сведения о лицензии и вы можете изменить состояние включения, дату окончания срока действия лицензии и данные ключа лицензии.</span><span class="sxs-lookup"><span data-stu-id="07e66-186">The **General** tab of the **Properties** dialog box displays information about the license and lets you change the enabled status, license expiration date, and license key information.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="07e66-187">Help</span><span class="sxs-lookup"><span data-stu-id="07e66-187">Help</span></span>**  
<span data-ttu-id="07e66-188">Вывод справочной системы для консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="07e66-188">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="07e66-189">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="07e66-189">Related topics</span></span>


[<span data-ttu-id="07e66-190">Сведения о лицензировании приложений</span><span class="sxs-lookup"><span data-stu-id="07e66-190">About Application Licensing</span></span>](about-application-licensing.md)

[<span data-ttu-id="07e66-191">Управление лицензиями приложений на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="07e66-191">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="07e66-192">Консоль управления серверами: узел лицензий приложений</span><span class="sxs-lookup"><span data-stu-id="07e66-192">Server Management Console: Application Licenses Node</span></span>](server-management-console-application-licenses-node.md)

 

 





