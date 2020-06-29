---
title: Настройка веб-параметров для рабочей области MED-V
description: Настройка веб-параметров для рабочей области MED-V
author: dansimp
ms.assetid: 9a6cd28f-7e4f-468f-830a-7b1d9abd3af3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 770d3fa9a03c9754db86ca348390d0b916de6d5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827069"
---
# <span data-ttu-id="0e2aa-103">Настройка веб-параметров для рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="0e2aa-103">How to Configure Web Settings for a MED-V Workspace</span></span>


<span data-ttu-id="0e2aa-104">Веб-сайты, которые могут отображаться только в более ранних версиях Internet Explorer и не существующих в операционной системе узла, можно просматривать в более ранних версиях Internet Explorer в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-104">Web sites that can only be displayed in older versions of Internet Explorer and that do not exist in the host operating system can be viewed in older versions of Internet Explorer within the MED-V workspace.</span></span> <span data-ttu-id="0e2aa-105">Пользователю не нужно открывать браузер в рабочей области MED-V для просмотра указанных веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-105">The user does not need to open a browser in the MED-V workspace to view the specified Web sites.</span></span> <span data-ttu-id="0e2aa-106">Пользователь может открыть браузер на узле и автоматически перенаправить его в рабочую область MED-V и наоборот.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-106">The user can open a browser on the host and automatically be redirected to the MED-V workspace and vice versa.</span></span>

<span data-ttu-id="0e2aa-107">Ниже описаны действия, которые можно использовать для задания списка правил просмотра веб-сайтов для рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-107">The following procedures describe how you can set a list of Web browsing rules for a MED-V workspace.</span></span> <span data-ttu-id="0e2aa-108">Все сайты, включенные в правила, можно просматривать либо в рабочей области MED-V, либо на узле, определенном администратором.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-108">All sites included in the rules can be browsed either in the MED-V workspace or on the host, as defined by the administrator.</span></span> <span data-ttu-id="0e2aa-109">Все сайты, не определенные в правилах, просматриваются из среды, в которой они были запрошены.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-109">All sites not defined within the rules are browsed from the environment in which they were requested.</span></span> <span data-ttu-id="0e2aa-110">Однако вы также можете настроить их как группу, чтобы просматривать их в рабочей области MED-V или на узле.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-110">However, you can configure them as a group as well, to be browsed in the MED-V workspace or the host.</span></span>

**<span data-ttu-id="0e2aa-111">Примечание.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-111">Note</span></span>**  
<span data-ttu-id="0e2aa-112">Параметры веб-сайта применяются только к Internet Explorer и другим браузерам.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-112">Web settings are applied only to Internet Explorer and to no other browsers.</span></span>



<span data-ttu-id="0e2aa-113">Все веб-параметры настраиваются в модуле **политики** на вкладке " **веб** ".</span><span class="sxs-lookup"><span data-stu-id="0e2aa-113">All Web settings are configured in the **Policy** module, on the **Web** tab.</span></span>

## <span data-ttu-id="0e2aa-114">Настройка веб-параметров для рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="0e2aa-114">How to Configure Web Settings for the MED-V Workspace</span></span>


**<span data-ttu-id="0e2aa-115">Настройка веб-параметров для рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="0e2aa-115">To configure Web settings for the MED-V workspace</span></span>**

1.  <span data-ttu-id="0e2aa-116">Щелкните рабочую область MED-V, которую нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-116">Click the MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="0e2aa-117">Нажмите кнопку **Обзор списка URL-адресов, описанных в таблице ниже** , чтобы перенаправить пользователя на браузер в рабочей области или узле MED-V, когда пользователь переходит по URL-адресу, который соответствует заданным пользователем.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-117">Select the **Browse the list of URLs defined in the following table** check box to redirect the user to a browser within the MED-V workspace or host, when the user browses to a URL that conforms to the Web rules specified.</span></span>

3.  <span data-ttu-id="0e2aa-118">Выберите один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-118">Click one of the following:</span></span>

    -   <span data-ttu-id="0e2aa-119">**В рабочей области**— перенаправление в браузер в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-119">**In the Workspace**—Redirect to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="0e2aa-120">На **узле**— перенаправление в браузер на узле.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-120">**In the host**—Redirect to a browser on the host.</span></span>

4.  <span data-ttu-id="0e2aa-121">Установите флажок **просматривать все другие URL** -адреса, чтобы перенаправить все адреса URL, исключенные из диалоговых правил, на узел или рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-121">Select the **Browse all other URLs** check box to redirect all URLs excluded from the Web rules to the host or MED-V workspace.</span></span>

5.  <span data-ttu-id="0e2aa-122">Выберите один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-122">Click one of the following:</span></span>

    -   <span data-ttu-id="0e2aa-123">**В рабочей области**перенастройте все другие URL-адреса в браузере в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-123">**In the Workspace**—Redirect all other URLs to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="0e2aa-124">**В узле**— перенаправить все другие URL-адреса в браузер на узле.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-124">**In the host**—Redirect all other URLs to a browser on the host.</span></span>

6.  <span data-ttu-id="0e2aa-125">В меню **Политика** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-125">On the **Policy** menu, select **Commit**.</span></span>

## <span data-ttu-id="0e2aa-126">Добавление веб-правила</span><span class="sxs-lookup"><span data-stu-id="0e2aa-126">How to Add a Web Rule</span></span>


**<span data-ttu-id="0e2aa-127">Добавление веб-правила</span><span class="sxs-lookup"><span data-stu-id="0e2aa-127">To add a Web rule</span></span>**

1.  <span data-ttu-id="0e2aa-128">Нажмите кнопку **Обзор списка URL-адресов, указанных в таблице ниже** , чтобы включить правила просмотра веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-128">Select the **Browse the list of URLs defined in the following table** check box to enable the Web browsing rules.</span></span>

2.  <span data-ttu-id="0e2aa-129">Щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-129">Click **Add**.</span></span>

    <span data-ttu-id="0e2aa-130">Добавляется новое веб-правило.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-130">A new Web rule is added.</span></span>

3.  <span data-ttu-id="0e2aa-131">Настройте свойства веб-правила, как описано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-131">Configure the Web rule properties as described in the following table.</span></span>

4.  <span data-ttu-id="0e2aa-132">В меню **Политика** выберите команду **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-132">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="0e2aa-133">Веб-свойства рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="0e2aa-133">MED-V Workspace Web Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0e2aa-134">Свойство</span><span class="sxs-lookup"><span data-stu-id="0e2aa-134">Property</span></span></th>
<th align="left"><span data-ttu-id="0e2aa-135">Описание</span><span class="sxs-lookup"><span data-stu-id="0e2aa-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0e2aa-136">Тип</span><span class="sxs-lookup"><span data-stu-id="0e2aa-136">Type</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="0e2aa-137">Доменный суффикс </strong> — доступ к любому адресу узла, заканчивающимся суффиксом, заданному в <strong> </strong> свойстве Value, и устанавливается в соответствии с параметром, заданным в <strong> браузере веб-страниц </strong> .</span><span class="sxs-lookup"><span data-stu-id="0e2aa-137">Domain suffix</strong>—Access to any host address ending with the suffix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="0e2aa-138">Префикс IP </strong> — доступ ко всем полным или частичным IP-адресам в диапазоне, указанному в <strong> </strong> свойстве Value, и устанавливается в соответствии с параметрами, заданными в <strong> веб-обозревателе </strong> .</span><span class="sxs-lookup"><span data-stu-id="0e2aa-138">IP Prefix</strong>—Access to any full or partial IP address in the range of the prefix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="0e2aa-139">Все локальные адреса </strong> — доступ ко всем адресам без &#39;. &#39; и устанавливается в соответствии с параметрами, заданными при <strong> просмотре веб-страниц </strong> .</span><span class="sxs-lookup"><span data-stu-id="0e2aa-139">All Local Addresses</strong>—Access to all addresses without a &#39;.&#39; and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0e2aa-140">Значение</span><span class="sxs-lookup"><span data-stu-id="0e2aa-140">Value</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0e2aa-141">Если <strong> </strong> в свойстве Type выбран доменный суффикс <strong> </strong> , введите суффикс домена.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-141">If <strong>Domain suffix</strong> is selected in the <strong>Type</strong> property, enter a domain suffix.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="0e2aa-142">Примечание.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-142">Note</span></span></strong><br/><ul>
<li><p><span data-ttu-id="0e2aa-143">Не вводите &quot; \* &quot; перед суффиксом.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-143">Do not enter &quot;\*&quot; before the suffix.</span></span></p></li>
<li><p><span data-ttu-id="0e2aa-144">Доменные суффиксы также поддерживают псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-144">Domain suffixes support aliases as well.</span></span></p></li>
</ul>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="0e2aa-145">Если в <strong> свойстве Type выбран префикс IP </strong> , введите полный или частичный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-145">If IP Prefix is selected in the <strong>Type</strong> property, enter a full or partial IP address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="0e2aa-146">Удаление веб-правила</span><span class="sxs-lookup"><span data-stu-id="0e2aa-146">How to Delete a Web Rule</span></span>


**<span data-ttu-id="0e2aa-147">Удаление веб-правила</span><span class="sxs-lookup"><span data-stu-id="0e2aa-147">To delete a Web rule</span></span>**

1.  <span data-ttu-id="0e2aa-148">В области **веб-страницы** выберите веб-правило, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-148">In the **Web** pane, select the Web rule to delete.</span></span>

2.  <span data-ttu-id="0e2aa-149">Нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-149">Click **Remove**.</span></span>

    <span data-ttu-id="0e2aa-150">Веб-правило будет удалено.</span><span class="sxs-lookup"><span data-stu-id="0e2aa-150">The Web rule is deleted.</span></span>

## <span data-ttu-id="0e2aa-151">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0e2aa-151">Related topics</span></span>


[<span data-ttu-id="0e2aa-152">Использование пользовательского интерфейса консоли управления MED-V</span><span class="sxs-lookup"><span data-stu-id="0e2aa-152">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="0e2aa-153">Создание рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="0e2aa-153">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)









