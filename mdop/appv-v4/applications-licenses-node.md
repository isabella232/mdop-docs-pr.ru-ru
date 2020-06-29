---
title: Узел лицензий приложений
description: Узел лицензий приложений
author: dansimp
ms.assetid: 2b8752ff-aa56-483e-b844-966941af2d94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 720de1860e72ae2c71298f93e9b346afd66da569
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819512"
---
# <span data-ttu-id="07cba-103">Узел лицензий приложений</span><span class="sxs-lookup"><span data-stu-id="07cba-103">Applications Licenses Node</span></span>


<span data-ttu-id="07cba-104">Узел **лицензии** на приложение находится на одном уровне под узлом системы Application Virtualization в области **область** консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="07cba-104">The **Applications Licenses** node is one level below the Application Virtualization System node in the **Scope** pane in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="07cba-105">При выборе этого узла в области **результатов** отображается список лицензий и групп лицензий.</span><span class="sxs-lookup"><span data-stu-id="07cba-105">When you select this node, the **Results** pane displays a list of licenses and license groups.</span></span> <span data-ttu-id="07cba-106">Доступны следующие типы лицензий:</span><span class="sxs-lookup"><span data-stu-id="07cba-106">The following license types are available:</span></span>

-   <span data-ttu-id="07cba-107">**Неограниченная лицензия**— предоставляет доступ к любому количеству одновременных пользователей.</span><span class="sxs-lookup"><span data-stu-id="07cba-107">**Unlimited License**—Provides access for any number of simultaneous users.</span></span> <span data-ttu-id="07cba-108">Этот метод лицензирования подходит, если вы хотите связать лицензию на уровне Организации с приложением.</span><span class="sxs-lookup"><span data-stu-id="07cba-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="07cba-109">**Одновременная лицензия**— позволяет определить максимальное количество пользователей, которые могут использовать приложение.</span><span class="sxs-lookup"><span data-stu-id="07cba-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="07cba-110">" **Лицензия с именем**" — позволяет назначать лицензию отдельному пользователю.</span><span class="sxs-lookup"><span data-stu-id="07cba-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="07cba-111">Именованную лицензию можно использовать, чтобы гарантировать, что определенный пользователь всегда сможет запускать приложение.</span><span class="sxs-lookup"><span data-stu-id="07cba-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="07cba-112">**Примечание**  Вы можете сочетать одновременные и именованные лицензии для одного и того же приложения.</span><span class="sxs-lookup"><span data-stu-id="07cba-112">**Note** You can combine concurrent and named licenses for the same application.</span></span>

 

<span data-ttu-id="07cba-113">Щелкните правой кнопкой мыши узел **лицензии на приложения** , чтобы открыть всплывающее меню, содержащее следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="07cba-113">Right-click the **Applications Licenses** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-unlimited-license"></a>**<span data-ttu-id="07cba-114">Новая неограниченная лицензия</span><span class="sxs-lookup"><span data-stu-id="07cba-114">New Unlimited License</span></span>**  
<span data-ttu-id="07cba-115">Отображение нового мастера неограниченных лицензий.</span><span class="sxs-lookup"><span data-stu-id="07cba-115">Displays the New Unlimited License Wizard.</span></span> <span data-ttu-id="07cba-116">Этот мастер состоит из следующих страниц:</span><span class="sxs-lookup"><span data-stu-id="07cba-116">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="07cba-117">Введите имя лицензионной группы в поле **имя группы лицензирования приложений** и введите значение (в минутах) в поле **предупреждение об истечении срока действия лицензии** .</span><span class="sxs-lookup"><span data-stu-id="07cba-117">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="07cba-118">(Вы можете ввести любое значение от 0 до 100.) Вы также можете выбрать нужное количество минут с помощью стрелок вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="07cba-118">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="07cba-119">Введите краткий описательный текст в поле **описания лицензии** и установите флажок **включено** , чтобы включить лицензию.</span><span class="sxs-lookup"><span data-stu-id="07cba-119">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="07cba-120">Кроме того, можно использовать поле **Дата окончания** срока действия, чтобы задать дату окончания срока действия лицензии.</span><span class="sxs-lookup"><span data-stu-id="07cba-120">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="07cba-121">Вы можете установить флажок, чтобы использовать отображаемую дату окончания срока действия, или воспользоваться служебной программой "Календарь", чтобы перейти к нужной дате.</span><span class="sxs-lookup"><span data-stu-id="07cba-121">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="07cba-122">Нажмите кнопку **Готово** , чтобы добавить новую лицензию.</span><span class="sxs-lookup"><span data-stu-id="07cba-122">Click **Finish** to add the new license.</span></span>

<a href="" id="new-concurrent-license"></a>**<span data-ttu-id="07cba-123">Новая лицензия для параллельных лицензий</span><span class="sxs-lookup"><span data-stu-id="07cba-123">New Concurrent License</span></span>**  
<span data-ttu-id="07cba-124">Отображение мастера создания лицензий с параллельной лицензией.</span><span class="sxs-lookup"><span data-stu-id="07cba-124">Displays the New Concurrent License Wizard.</span></span> <span data-ttu-id="07cba-125">Этот мастер состоит из трех следующих страниц и почти одинаково для нового мастера неограниченных лицензий.</span><span class="sxs-lookup"><span data-stu-id="07cba-125">This wizard consists of the following three pages and is almost identical to the New Unlimited License Wizard:</span></span>

1.  <span data-ttu-id="07cba-126">Введите имя лицензионной группы в поле **имя группы лицензирования приложений** и введите значение (в минутах) в поле **предупреждение об истечении срока действия лицензии** .</span><span class="sxs-lookup"><span data-stu-id="07cba-126">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="07cba-127">(Вы можете ввести любое значение от 0 до 100.) Вы также можете выбрать нужное количество минут с помощью стрелок вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="07cba-127">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="07cba-128">Введите краткий описательный текст в поле **Описание лицензии** и введите значение в поле « **количество одновременных лицензий** ».</span><span class="sxs-lookup"><span data-stu-id="07cba-128">Enter brief descriptive text in the **License Description** field, and enter a value in the **Concurrent License Quantity** field.</span></span>

    <span data-ttu-id="07cba-129">Вы также можете использовать стрелки вверх и вниз, чтобы указать количество одновременных лицензий.</span><span class="sxs-lookup"><span data-stu-id="07cba-129">You can also use the up and down arrows to specify the number of concurrent licenses.</span></span> <span data-ttu-id="07cba-130">Установите флажок **включено** , чтобы включить лицензию.</span><span class="sxs-lookup"><span data-stu-id="07cba-130">Select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="07cba-131">Кроме того, можно использовать поле **Дата окончания** срока действия, чтобы задать дату окончания срока действия лицензии.</span><span class="sxs-lookup"><span data-stu-id="07cba-131">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="07cba-132">Вы можете установить флажок, чтобы использовать отображаемую дату окончания срока действия, или воспользоваться служебной программой "Календарь", чтобы перейти к нужной дате.</span><span class="sxs-lookup"><span data-stu-id="07cba-132">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="07cba-133">Нажмите кнопку **Готово** , чтобы добавить новые лицензии.</span><span class="sxs-lookup"><span data-stu-id="07cba-133">Click **Finish** to add the new licenses.</span></span>

<a href="" id="new-named-license"></a>**<span data-ttu-id="07cba-134">Новая именованная лицензия</span><span class="sxs-lookup"><span data-stu-id="07cba-134">New Named License</span></span>**  
<span data-ttu-id="07cba-135">Отображает мастер создания лицензии.</span><span class="sxs-lookup"><span data-stu-id="07cba-135">Displays the New Named License Wizard.</span></span> <span data-ttu-id="07cba-136">Этот мастер состоит из следующих четырех страниц:</span><span class="sxs-lookup"><span data-stu-id="07cba-136">This wizard consists of the following four pages:</span></span>

1.  <span data-ttu-id="07cba-137">Введите имя лицензионной группы в поле **имя группы лицензирования приложений** и введите значение (в минутах) в поле **предупреждение об истечении срока действия лицензии** .</span><span class="sxs-lookup"><span data-stu-id="07cba-137">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="07cba-138">(Вы можете ввести любое значение от 0 до 100).</span><span class="sxs-lookup"><span data-stu-id="07cba-138">(You can enter any value from 0 through 100).</span></span> <span data-ttu-id="07cba-139">Вы также можете выбрать нужное количество минут с помощью стрелок вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="07cba-139">You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="07cba-140">Введите краткий описательный текст в поле **описания лицензии** и установите флажок **включено** , чтобы включить лицензию.</span><span class="sxs-lookup"><span data-stu-id="07cba-140">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="07cba-141">Кроме того, можно использовать поле **Дата окончания** срока действия, чтобы задать дату окончания срока действия лицензии.</span><span class="sxs-lookup"><span data-stu-id="07cba-141">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="07cba-142">Вы можете установить флажок, чтобы использовать отображаемую дату окончания срока действия, или воспользоваться служебной программой "Календарь", чтобы перейти к нужной дате.</span><span class="sxs-lookup"><span data-stu-id="07cba-142">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="07cba-143">Нажмите кнопку **Добавить**, **изменить**или **Удалить** именованных пользователей.</span><span class="sxs-lookup"><span data-stu-id="07cba-143">Click **Add**, **Edit**, or **Remove** named users.</span></span>

4.  <span data-ttu-id="07cba-144">Нажмите кнопку **Готово** , чтобы добавить новую лицензию.</span><span class="sxs-lookup"><span data-stu-id="07cba-144">Click **Finish** to add the new license.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="07cba-145">Просмотр</span><span class="sxs-lookup"><span data-stu-id="07cba-145">View</span></span>**  
<span data-ttu-id="07cba-146">Изменение внешнего вида и содержимого области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="07cba-146">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="07cba-147">Новое окно</span><span class="sxs-lookup"><span data-stu-id="07cba-147">New Window from Here</span></span>**  
<span data-ttu-id="07cba-148">Открытие новой консоли управления с выбранным узлом в качестве корневого узла.</span><span class="sxs-lookup"><span data-stu-id="07cba-148">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="07cba-149">Обновить</span><span class="sxs-lookup"><span data-stu-id="07cba-149">Refresh</span></span>**  
<span data-ttu-id="07cba-150">Обновляет представление сервера.</span><span class="sxs-lookup"><span data-stu-id="07cba-150">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="07cba-151">Экспорт списка</span><span class="sxs-lookup"><span data-stu-id="07cba-151">Export List</span></span>**  
<span data-ttu-id="07cba-152">Создает текстовый файл с разделителями-знаками табуляции, который включает содержимое области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="07cba-152">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="07cba-153">Этот элемент отображает диалоговое окно " **Сохранение файла** ", в котором указывается расположение для текстового файла, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="07cba-153">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="07cba-154">Help</span><span class="sxs-lookup"><span data-stu-id="07cba-154">Help</span></span>**  
<span data-ttu-id="07cba-155">Вывод справочной системы для консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="07cba-155">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="07cba-156">Если вы щелкните лицензионную группу или лицензию, которая отображается в разделе " **лицензии приложений** " в области " **область** ", доступны следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="07cba-156">If you click a license group or license that appears under the **Application Licenses** node in the **Scope** pane, the following elements are available.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="07cba-157">Просмотр</span><span class="sxs-lookup"><span data-stu-id="07cba-157">View</span></span>**  
<span data-ttu-id="07cba-158">Изменение внешнего вида и содержимого области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="07cba-158">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="07cba-159">Новое окно</span><span class="sxs-lookup"><span data-stu-id="07cba-159">New Window from Here</span></span>**  
<span data-ttu-id="07cba-160">Открытие новой консоли управления с выбранным узлом в качестве корневого узла.</span><span class="sxs-lookup"><span data-stu-id="07cba-160">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="07cba-161">Delete</span><span class="sxs-lookup"><span data-stu-id="07cba-161">Delete</span></span>**  
<span data-ttu-id="07cba-162">Удаляет пакет из области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="07cba-162">Deletes a package from the **Results** pane.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="07cba-163">Rename</span><span class="sxs-lookup"><span data-stu-id="07cba-163">Rename</span></span>**  
<span data-ttu-id="07cba-164">Изменяет имя пакета в области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="07cba-164">Changes the name of a package in the **Results** pane.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="07cba-165">Экспорт списка</span><span class="sxs-lookup"><span data-stu-id="07cba-165">Export List</span></span>**  
<span data-ttu-id="07cba-166">Создает текстовый файл с разделителями-знаками табуляции, который включает содержимое области **результатов** .</span><span class="sxs-lookup"><span data-stu-id="07cba-166">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="07cba-167">Этот элемент отображает диалоговое окно " **Сохранение файла** ", в котором указывается расположение для текстового файла, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="07cba-167">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="07cba-168">Свойства</span><span class="sxs-lookup"><span data-stu-id="07cba-168">Properties</span></span>**  
<span data-ttu-id="07cba-169">Вывод диалогового окна " **Свойства** " для выбранной лицензионной группы.</span><span class="sxs-lookup"><span data-stu-id="07cba-169">Displays the **Properties** dialog box for the selected license group.</span></span> <span data-ttu-id="07cba-170">На вкладке " **Общие** " в диалоговом окне " **свойства** " отображаются сведения о лицензионной группе и можно изменить значение времени в поле " **предупреждение об истечении срока действия лицензии** ".</span><span class="sxs-lookup"><span data-stu-id="07cba-170">The **General** tab of the **Properties** dialog box displays information about the license group and lets you change the time value in the **License Expiration Warning** field.</span></span> <span data-ttu-id="07cba-171">На вкладке **приложения** отображается список приложений, связанных с лицензионной группой.</span><span class="sxs-lookup"><span data-stu-id="07cba-171">The **Applications** tab displays the list of applications associated with the license group.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="07cba-172">Help</span><span class="sxs-lookup"><span data-stu-id="07cba-172">Help</span></span>**  
<span data-ttu-id="07cba-173">Вывод справочной системы для консоли управления сервером виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="07cba-173">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="07cba-174">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="07cba-174">Related topics</span></span>


[<span data-ttu-id="07cba-175">Сведения о лицензировании приложений</span><span class="sxs-lookup"><span data-stu-id="07cba-175">About Application Licensing</span></span>](about-application-licensing.md)

[<span data-ttu-id="07cba-176">Управление лицензиями приложений на консоли управления серверами</span><span class="sxs-lookup"><span data-stu-id="07cba-176">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="07cba-177">Консоль управления серверами: узел лицензий приложений</span><span class="sxs-lookup"><span data-stu-id="07cba-177">Server Management Console: Application Licenses Node</span></span>](server-management-console-application-licenses-node.md)

 

 





