---
title: Настройка опубликованных приложений
description: Настройка опубликованных приложений
author: dansimp
ms.assetid: 43a59ff7-5d4e-49dc-84e5-1082bc4dd8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cb5736382f03e818ef10aa814a8e61044ca2b73a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824312"
---
# <span data-ttu-id="2d2f4-103">Настройка опубликованных приложений</span><span class="sxs-lookup"><span data-stu-id="2d2f4-103">How to Configure Published Applications</span></span>


<span data-ttu-id="2d2f4-104">Приложения, несовместимые с операционной системой узла, можно запускать в рабочей области MED-V и инициировать из рабочей области MED-V таким же образом, как и на рабочем столе — в меню "Пуск" или с помощью ярлыка на локальном узле.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-104">Applications that are not compatible with the host operating system can be run within the MED-V workspace and initiated from within the MED-V workspace the same way they are initiated from the desktop—from the Start menu or from a local host shortcut.</span></span> <span data-ttu-id="2d2f4-105">Выделены и определены приложения, которые называются опубликованными приложениями.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-105">Applications selected and defined are called published applications.</span></span> <span data-ttu-id="2d2f4-106">Процедуры, описанные в этом разделе, описывают, как добавлять и удалять опубликованные приложения.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-106">The procedures in this section describe how to add and remove published applications.</span></span>

<span data-ttu-id="2d2f4-107">Приложение может быть опубликовано одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-107">An application can be published in one of the following ways:</span></span>

-   <span data-ttu-id="2d2f4-108">Как приложение — выберите определенное приложение, введя его в командную строку приложения.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-108">As an application—Select a specific application by typing in the command line for the application.</span></span> <span data-ttu-id="2d2f4-109">Опубликовано только выбранное приложение.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-109">Only the application selected is published.</span></span>

-   <span data-ttu-id="2d2f4-110">Меню — выберите папку, которая включает несколько приложений.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-110">As a menu—Select a folder that contains multiple applications.</span></span> <span data-ttu-id="2d2f4-111">Все приложения в папке публикуются и отображаются в виде меню.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-111">All applications within the folder are published and displayed as a menu.</span></span>

## <a href="" id="bkmk-addingapublishedapplication"></a><span data-ttu-id="2d2f4-112">Добавление опубликованного приложения в рабочую область MED-V</span><span class="sxs-lookup"><span data-stu-id="2d2f4-112">How to Add a Published Application to a MED-V Workspace</span></span>


**<span data-ttu-id="2d2f4-113">Добавление приложения в рабочую область MED-V</span><span class="sxs-lookup"><span data-stu-id="2d2f4-113">To add an application to the MED-V workspace</span></span>**

1.  <span data-ttu-id="2d2f4-114">Щелкните рабочую область MED-V, которую нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-114">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="2d2f4-115">В области **приложения** в разделе **опубликованные приложения** нажмите кнопку **добавить** , чтобы добавить новое приложение.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-115">In the **Applications** pane, in the **Published Applications** section, click **Add** to add a new application.</span></span>

3.  <span data-ttu-id="2d2f4-116">Настройте свойства приложения, как описано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-116">Configure the application properties as described in the following table.</span></span>

4.  <span data-ttu-id="2d2f4-117">В меню **Политика** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-117">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="2d2f4-118">Примечание.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-118">Note</span></span>**  
    <span data-ttu-id="2d2f4-119">Если вы настраиваете Internet Explorer как опубликованное приложение, чтобы обеспечить правильную работу перенаправления веб-браузера, убедитесь в том, что параметры не заключены в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-119">If you are setting Internet Explorer as a published application to ensure that Web redirection works properly, make certain that any parameters are not in parentheses.</span></span>



**<span data-ttu-id="2d2f4-120">Свойства опубликованного приложения</span><span class="sxs-lookup"><span data-stu-id="2d2f4-120">Published Application Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2d2f4-121">Свойство</span><span class="sxs-lookup"><span data-stu-id="2d2f4-121">Property</span></span></th>
<th align="left"><span data-ttu-id="2d2f4-122">Описание</span><span class="sxs-lookup"><span data-stu-id="2d2f4-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2d2f4-123">Включено</span><span class="sxs-lookup"><span data-stu-id="2d2f4-123">Enabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d2f4-124">Установите этот флажок, чтобы включить опубликованное приложение.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-124">Select this check box to enable the published application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2d2f4-125">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2d2f4-125">Display name</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d2f4-126">Название ярлыка в меню "Пуск" в Windows&#39;s.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-126">The name of the shortcut in the user&#39;s Windows Start menu.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="2d2f4-127">Примечание.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-127">Note</span></span></strong><br/><p><span data-ttu-id="2d2f4-128">Отображаемое имя <strong> не </strong> учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-128">The display name is <strong>not</strong> case sensitive.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2d2f4-129">Описание</span><span class="sxs-lookup"><span data-stu-id="2d2f4-129">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d2f4-130">Описание опубликованного приложения, которое отображается как всплывающая подсказка, когда пользователь&#39;наводит указатель мыши на этот ярлык.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-130">A description of the published application, which appears as a tooltip when the user&#39;s mouse hovers over the shortcut.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2d2f4-131">Командная строка</span><span class="sxs-lookup"><span data-stu-id="2d2f4-131">Command line</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d2f4-132">Команда, используемая для запуска приложения в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-132">The command used to run the application from within the MED-V workspace.</span></span> <span data-ttu-id="2d2f4-133">Требуется указывать полный путь, и параметры можно передать в приложение так же, как и в любой другой команде Windows.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-133">The full path is required, and the parameters can be passed to the application in a similar fashion as in any other Windows command.</span></span></p>
<p><span data-ttu-id="2d2f4-134">В рабочей области revertible MED-V вы можете сопоставить сетевой диск с синтаксисом MapNetworkDrive: &quot; <em> MapNetworkDrive &lt; путь к диску, &gt; &lt; &gt; </em> &quot; например &quot; <em> MapNetworkDrive t: \tux\date </em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="2d2f4-134">In a revertible MED-V workspace, you can map a network drive with MapNetworkDrive syntax: &quot;<em>MapNetworkDrive &lt;drive&gt; &lt;path&gt;</em>&quot;—for example, &quot;<em>MapNetworkDrive t: \tux\date</em>&quot;.</span></span></p>
<p><span data-ttu-id="2d2f4-135">Например, чтобы опубликовать проводник Windows, используйте следующий синтаксис: &quot; <em> c: &lt; /EM &gt; &quot; или &quot; <em> c:\Windows </em> .&quot;</span><span class="sxs-lookup"><span data-stu-id="2d2f4-135">For example, to publish Windows Explorer, use the following syntax: &quot;<em>c:&lt;/em&gt;&quot; or &quot;<em>c:\windows</em>.&quot;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="2d2f4-136">Примечание.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-136">Note</span></span></strong><br/><p><span data-ttu-id="2d2f4-137">Чтобы использовать разрешение имен, необходимо выполнить одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="2d2f4-137">To have a name resolution, you need to perform one of the following:</span></span></p>
</div>
<div>

</div>
<ul>
<li><p><span data-ttu-id="2d2f4-138">Настройте DNS в основном образе рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-138">Configure the DNS in the base MED-V workspace image.</span></span></p></li>
<li><p><span data-ttu-id="2d2f4-139">Убедитесь, что разрешение DNS определено на узле, и настройте его на использование DNS узла.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-139">Verify the DNS resolution is defined in the host, and configure it to use the host DNS.</span></span></p></li>
<li><p><span data-ttu-id="2d2f4-140">Используйте IP-адрес для определения сетевого диска.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-140">Use the IP for defining the network drive.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="2d2f4-141">Примечание.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-141">Note</span></span></strong><br/><p><span data-ttu-id="2d2f4-142">Если путь содержит пробелы, весь путь должен быть заключен в кавычки.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-142">If the path includes spaces, the entire path must be inside quotation marks.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="2d2f4-143">Примечание.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-143">Note</span></span></strong><br/><p><span data-ttu-id="2d2f4-144">Путь не должен заканчиваться обратной косой чертой ().</span><span class="sxs-lookup"><span data-stu-id="2d2f4-144">The path should not end with a backslash ().</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2d2f4-145">Меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="2d2f4-145">Start menu</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d2f4-146">Установите этот флажок, чтобы создать ярлык для приложения в меню "Пуск" в Windows "пользователь&#39;s".</span><span class="sxs-lookup"><span data-stu-id="2d2f4-146">Select this check box to create a shortcut for the application in the user&#39;s Windows Start menu.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="2d2f4-147">Все опубликованные приложения отображаются в меню " **Пуск** " в Windows с помощью сочетаний клавиш (**запускать &gt; все программы для &gt; MED-V приложений**).</span><span class="sxs-lookup"><span data-stu-id="2d2f4-147">All published applications appear as shortcuts in the Windows **Start** menu (**Start &gt;All Programs&gt; MED-V Applications**).</span></span>

## <span data-ttu-id="2d2f4-148">Удаление опубликованного приложения из рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="2d2f4-148">How to Remove a Published Application from a MED-V Workspace</span></span>


**<span data-ttu-id="2d2f4-149">Удаление приложения из рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="2d2f4-149">To remove an application from the MED-V workspace</span></span>**

1.  <span data-ttu-id="2d2f4-150">Щелкните рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-150">Click a MED-V workspace.</span></span>

2.  <span data-ttu-id="2d2f4-151">В области **приложения** в разделе **опубликованные приложения** выберите приложение, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-151">In the **Applications** pane, in the **Published Applications** section, select an application to remove.</span></span>

3.  <span data-ttu-id="2d2f4-152">Нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-152">Click **Remove**.</span></span>

    <span data-ttu-id="2d2f4-153">Приложение удаляется из списка опубликованных приложений.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-153">The application is removed from the list of published applications.</span></span>

4.  <span data-ttu-id="2d2f4-154">В меню **Политика** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-154">On the **Policy** menu, select **Commit**.</span></span>

## <span data-ttu-id="2d2f4-155">Добавление опубликованного меню в рабочую область MED-V</span><span class="sxs-lookup"><span data-stu-id="2d2f4-155">How to Add a Published Menu to a MED-V Workspace</span></span>


**<span data-ttu-id="2d2f4-156">Добавление опубликованного меню в рабочую область для MED-V</span><span class="sxs-lookup"><span data-stu-id="2d2f4-156">To add a published menu to the MED-V workspace</span></span>**

1.  <span data-ttu-id="2d2f4-157">Щелкните рабочую область MED-V, которую нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-157">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="2d2f4-158">На панели **приложения** в разделе **опубликованные меню** нажмите кнопку **добавить** , чтобы добавить новое меню.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-158">In the **Applications** pane, in the **Published Menus** section, click **Add** to add a new menu.</span></span>

3.  <span data-ttu-id="2d2f4-159">Настройте свойства меню, как описано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-159">Configure the menu properties as described in the following table.</span></span>

4.  <span data-ttu-id="2d2f4-160">В меню **Политика** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-160">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="2d2f4-161">Свойства меню «опубликованные»</span><span class="sxs-lookup"><span data-stu-id="2d2f4-161">Published Menu Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2d2f4-162">Свойство</span><span class="sxs-lookup"><span data-stu-id="2d2f4-162">Property</span></span></th>
<th align="left"><span data-ttu-id="2d2f4-163">Описание</span><span class="sxs-lookup"><span data-stu-id="2d2f4-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2d2f4-164">Включено</span><span class="sxs-lookup"><span data-stu-id="2d2f4-164">Enabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d2f4-165">Установите этот флажок, чтобы включить меню "опубликован".</span><span class="sxs-lookup"><span data-stu-id="2d2f4-165">Select this check box to enable the published menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2d2f4-166">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2d2f4-166">Display name</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d2f4-167">Название ярлыка в меню "Пуск" в Windows&#39;s.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-167">The name of the shortcut in the user&#39;s Windows Start menu.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2d2f4-168">Описание</span><span class="sxs-lookup"><span data-stu-id="2d2f4-168">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d2f4-169">Описание, которое отображается как всплывающая подсказка, когда пользователь&#39;наводит указатель мыши на этот ярлык.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-169">The description, which appears as a tooltip when the user&#39;s mouse hovers over the shortcut.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2d2f4-170">Папка в рабочей области</span><span class="sxs-lookup"><span data-stu-id="2d2f4-170">Folder in workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d2f4-171">Выберите папку для публикации в виде меню, содержащего все приложения в папке.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-171">Select the folder to publish as a menu containing all the applications within the folder.</span></span></p>
<p><span data-ttu-id="2d2f4-172">Отображаемый текст — это относительный путь из папки программы.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-172">The text displayed is a relative path from the Programs folder.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="2d2f4-173">Примечание.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-173">Note</span></span></strong><br/><p><span data-ttu-id="2d2f4-174">Если оставить поле пустым, все программы на узле будут опубликованы как меню.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-174">If left blank, all programs on the host will be published as a menu.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="2d2f4-175">Все опубликованные меню выводятся в меню " **Пуск** " в Windows (**запускать &gt; все программы на &gt; основе приложений MED-V**).</span><span class="sxs-lookup"><span data-stu-id="2d2f4-175">All published menus appear as shortcuts in the Windows **Start** menu (**Start &gt;All Programs&gt; MED-V Applications**).</span></span> <span data-ttu-id="2d2f4-176">Вы можете изменить имя ярлыка в поле " **Папка для ярлыков** " в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="2d2f4-176">You can change the name of the shortcut in the **Start-menu shortcuts folder** field.</span></span>

**<span data-ttu-id="2d2f4-177">Примечание.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-177">Note</span></span>**  
<span data-ttu-id="2d2f4-178">При настройке двух рабочих областей MED-V рекомендуется настроить другое имя для папки "ярлыки" в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="2d2f4-178">When configuring two MED-V workspaces, it is recommended to configure a different name for the Start menu shortcuts folder.</span></span>



## <span data-ttu-id="2d2f4-179">Удаление опубликованного меню из рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="2d2f4-179">How to Remove a Published Menu from a MED-V Workspace</span></span>


**<span data-ttu-id="2d2f4-180">Удаление опубликованного меню из рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="2d2f4-180">To remove a published menu from a MED-V workspace</span></span>**

1.  <span data-ttu-id="2d2f4-181">Щелкните рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-181">Click a MED-V workspace.</span></span>

2.  <span data-ttu-id="2d2f4-182">На панели **приложения** в разделе **опубликованные меню** выберите меню, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-182">In the **Applications** pane, in the **Published Menus** section, select a menu to remove.</span></span>

3.  <span data-ttu-id="2d2f4-183">Нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-183">Click **Remove**.</span></span>

    <span data-ttu-id="2d2f4-184">Меню удаляется из списка опубликованных меню.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-184">The menu is removed from the list of published menus.</span></span>

4.  <span data-ttu-id="2d2f4-185">В меню **Политика** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-185">On the **Policy** menu, select **Commit**.</span></span>

## <span data-ttu-id="2d2f4-186">Запуск опубликованного приложения из командной строки на клиентском компьютере</span><span class="sxs-lookup"><span data-stu-id="2d2f4-186">Running a Published Application from a Command Line on the Client</span></span>


<span data-ttu-id="2d2f4-187">Администратор может запускать опубликованные приложения из любого места, такого как ярлык на рабочем столе, с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="2d2f4-187">The administrator can run published applications from any location, such as a desktop shortcut, using the following command:</span></span>

``` syntax
"<Install path>\Manager\KidaroCommands.exe" /run "<published application name>" "<MED-V workspace name>"
```

**<span data-ttu-id="2d2f4-188">Примечание.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-188">Note</span></span>**  
<span data-ttu-id="2d2f4-189">Рабочая область MED-V, в которой определено опубликованное приложение, должна выполняться.</span><span class="sxs-lookup"><span data-stu-id="2d2f4-189">The MED-V workspace in which the published application is defined must be running.</span></span>



## <span data-ttu-id="2d2f4-190">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2d2f4-190">Related topics</span></span>


[<span data-ttu-id="2d2f4-191">Изменение опубликованного приложения с помощью дополнительных параметров</span><span class="sxs-lookup"><span data-stu-id="2d2f4-191">How to Edit a Published Application with Advanced Settings</span></span>](how-to-edit-a-published-application-with-advanced-settings.md)

[<span data-ttu-id="2d2f4-192">Использование пользовательского интерфейса консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="2d2f4-192">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="2d2f4-193">Создание рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="2d2f4-193">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)









