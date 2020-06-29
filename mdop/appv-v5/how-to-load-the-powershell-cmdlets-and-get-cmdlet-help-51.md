---
title: Загрузка командлетов PowerShell и получение справки по командлетам
description: Загрузка командлетов PowerShell и получение справки по командлетам
author: dansimp
ms.assetid: b6ae5460-2c3a-4030-b132-394d9d5a541e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 32b5bb26331f204acffbf96ea119ac4209c3cd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813949"
---
# <span data-ttu-id="c08f5-103">Загрузка командлетов PowerShell и получение справки по командлетам</span><span class="sxs-lookup"><span data-stu-id="c08f5-103">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span>


<span data-ttu-id="c08f5-104">В этой статье рассказывается, как это делать.</span><span class="sxs-lookup"><span data-stu-id="c08f5-104">What this topic covers:</span></span>

-   [<span data-ttu-id="c08f5-105">Требования для использования командлетов PowerShell</span><span class="sxs-lookup"><span data-stu-id="c08f5-105">Requirements for using PowerShell cmdlets</span></span>](#bkmk-reqs-using-posh)

-   [<span data-ttu-id="c08f5-106">Загрузка командлетов PowerShell</span><span class="sxs-lookup"><span data-stu-id="c08f5-106">Loading the PowerShell cmdlets</span></span>](#bkmk-load-cmdlets)

-   [<span data-ttu-id="c08f5-107">Вызов справки по командлетам PowerShell</span><span class="sxs-lookup"><span data-stu-id="c08f5-107">Getting help for the PowerShell cmdlets</span></span>](#bkmk-get-cmdlet-help)

-   [<span data-ttu-id="c08f5-108">Отображение справки для командлета PowerShell</span><span class="sxs-lookup"><span data-stu-id="c08f5-108">Displaying the help for a PowerShell cmdlet</span></span>](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a><span data-ttu-id="c08f5-109">Требования для использования командлетов PowerShell</span><span class="sxs-lookup"><span data-stu-id="c08f5-109">Requirements for using PowerShell cmdlets</span></span>


<span data-ttu-id="c08f5-110">Ознакомьтесь с приведенными ниже требованиями для использования командлетов PowerShell App-V:</span><span class="sxs-lookup"><span data-stu-id="c08f5-110">Review the following requirements for using the App-V PowerShell cmdlets:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c08f5-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c08f5-111">Requirement</span></span></th>
<th align="left"><span data-ttu-id="c08f5-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="c08f5-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c08f5-113">Пользователи могут запускать командлеты App-V Server только в том случае, если вы предоставляете им доступ с помощью одного из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="c08f5-113">Users can run App-V Server cmdlets only if you grant them access by using one of the following methods:</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="c08f5-114">При развертывании и настройке сервера App-V выполните указанные </strong> ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c08f5-114">When you are deploying and configuring the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="c08f5-115">Укажите группу Active Directory или отдельного пользователя, у которого есть разрешения на управление средой App-V.</span><span class="sxs-lookup"><span data-stu-id="c08f5-115">Specify an Active Directory group or individual user that has permissions to manage the App-V environment.</span></span> <span data-ttu-id="c08f5-116">Узнайте <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> , как развернуть сервер App-V 5,1 </a> .</span><span class="sxs-lookup"><span data-stu-id="c08f5-116">See <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">How to Deploy the App-V 5.1 Server</a>.</span></span></p></li>
<li><p><strong><span data-ttu-id="c08f5-117">После того как вы развернули сервер App-V, </strong> выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c08f5-117">After you’ve deployed the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="c08f5-118">Добавьте дополнительную группу или пользователя Active Directory с помощью консоли управления App-V.</span><span class="sxs-lookup"><span data-stu-id="c08f5-118">Use the App-V Management console to add an additional Active Directory group or user.</span></span> <span data-ttu-id="c08f5-119">Узнайте <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console51.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)"> , как добавить или удалить администратора с помощью консоли управления </a> .</span><span class="sxs-lookup"><span data-stu-id="c08f5-119">See <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console51.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)">How to Add or Remove an Administrator by Using the Management Console</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c08f5-120">Командлеты, для которых требуется Командная строка с повышенными привилегиями</span><span class="sxs-lookup"><span data-stu-id="c08f5-120">Cmdlets that require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c08f5-121">Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c08f5-121">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="c08f5-122">Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c08f5-122">Remove-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="c08f5-123">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="c08f5-123">Set-AppvClientConfiguration</span></span></p></li>
<li><p><span data-ttu-id="c08f5-124">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="c08f5-124">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="c08f5-125">Remove-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="c08f5-125">Remove-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="c08f5-126">Add-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="c08f5-126">Add-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="c08f5-127">Remove-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="c08f5-127">Remove-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="c08f5-128">Send-AppvClientReport</span><span class="sxs-lookup"><span data-stu-id="c08f5-128">Send-AppvClientReport</span></span></p></li>
<li><p><span data-ttu-id="c08f5-129">Set-AppvClientMode</span><span class="sxs-lookup"><span data-stu-id="c08f5-129">Set-AppvClientMode</span></span></p></li>
<li><p><span data-ttu-id="c08f5-130">Set-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c08f5-130">Set-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="c08f5-131">Set-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="c08f5-131">Set-AppvPublishingServer</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c08f5-132">Командлеты, с помощью которых можно запускать конечные пользователи, если не настроить для них необходимость в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="c08f5-132">Cmdlets that end users can run, unless you configure them to require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c08f5-133">Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c08f5-133">Publish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="c08f5-134">Отмена публикации — AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c08f5-134">Unpublish-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="c08f5-135">Чтобы настроить эти командлеты для использования командной строки с повышенными привилегиями, воспользуйтесь одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="c08f5-135">To configure these cmdlets to require an elevated command prompt, use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c08f5-136">Метод</span><span class="sxs-lookup"><span data-stu-id="c08f5-136">Method</span></span></th>
<th align="left"><span data-ttu-id="c08f5-137">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c08f5-137">More resources</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c08f5-138">Запустите <strong> командлет Set-AppvClientConfiguration </strong> с <strong> параметром-RequirePublishAsAdmin </strong> .</span><span class="sxs-lookup"><span data-stu-id="c08f5-138">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>-RequirePublishAsAdmin</strong> parameter.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="c08f5-139">Управление группами соединений на отдельном компьютере с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="c08f5-139">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="c08f5-140">Управление пакетами App-V 5.1, работающими на автономном компьютере, с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="c08f5-140">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c08f5-141">Включите параметр групповой политики "требуется публикация от имени администратора" для клиентов App-V.</span><span class="sxs-lookup"><span data-stu-id="c08f5-141">Enable the “Require publish as administrator” Group Policy setting for App-V Clients.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-51.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md)"><span data-ttu-id="c08f5-142">Публикация пакета с помощью консоли управления</span><span class="sxs-lookup"><span data-stu-id="c08f5-142">How to Publish a Package by Using the Management Console</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a><span data-ttu-id="c08f5-143">Загрузка командлетов PowerShell</span><span class="sxs-lookup"><span data-stu-id="c08f5-143">Loading the PowerShell cmdlets</span></span>

<span data-ttu-id="c08f5-144">Чтобы загрузить модули командлетов PowerShell, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c08f5-144">To load the PowerShell cmdlet modules:</span></span>

1.  <span data-ttu-id="c08f5-145">Откройте Windows PowerShell или интегрированную среду сценариев Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="c08f5-145">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="c08f5-146">Чтобы загрузить командлеты для нужного модуля, введите одну из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="c08f5-146">Type one of the following commands to load the cmdlets for the module you want:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c08f5-147">Компонент App-V</span><span class="sxs-lookup"><span data-stu-id="c08f5-147">App-V component</span></span></th>
<th align="left"><span data-ttu-id="c08f5-148">Команда для ввода</span><span class="sxs-lookup"><span data-stu-id="c08f5-148">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c08f5-149">Сервер App-V</span><span class="sxs-lookup"><span data-stu-id="c08f5-149">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="c08f5-150">Import-Module AppvServer</span><span class="sxs-lookup"><span data-stu-id="c08f5-150">Import-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c08f5-151">Секвенсор App-V</span><span class="sxs-lookup"><span data-stu-id="c08f5-151">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="c08f5-152">Import-Module AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="c08f5-152">Import-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c08f5-153">Клиент App-V</span><span class="sxs-lookup"><span data-stu-id="c08f5-153">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="c08f5-154">Import-Module AppvClient</span><span class="sxs-lookup"><span data-stu-id="c08f5-154">Import-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="c08f5-155">Вызов справки по командлетам PowerShell</span><span class="sxs-lookup"><span data-stu-id="c08f5-155">Getting help for the PowerShell cmdlets</span></span>
<span data-ttu-id="c08f5-156">Начиная с версии App-V 5,0 с пакетом обновления 3 (SP3), Справка по командлетам доступна в двух форматах:</span><span class="sxs-lookup"><span data-stu-id="c08f5-156">Starting in App-V 5.0 SP3, cmdlet help is available in two formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c08f5-157">Формат</span><span class="sxs-lookup"><span data-stu-id="c08f5-157">Format</span></span></th>
<th align="left"><span data-ttu-id="c08f5-158">Описание</span><span class="sxs-lookup"><span data-stu-id="c08f5-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c08f5-159">Как загружаемый модуль</span><span class="sxs-lookup"><span data-stu-id="c08f5-159">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="c08f5-160">Чтобы скачать последнюю справку после загрузки модуля командлета, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c08f5-160">To download the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="c08f5-161">Откройте Windows PowerShell или интегрированную среду сценариев Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="c08f5-161">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="c08f5-162">Чтобы загрузить командлеты для нужного модуля, введите одну из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="c08f5-162">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c08f5-163">Компонент App-V</span><span class="sxs-lookup"><span data-stu-id="c08f5-163">App-V component</span></span></th>
<th align="left"><span data-ttu-id="c08f5-164">Команда для ввода</span><span class="sxs-lookup"><span data-stu-id="c08f5-164">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c08f5-165">Сервер App-V</span><span class="sxs-lookup"><span data-stu-id="c08f5-165">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="c08f5-166">Update-Help-Module AppvServer</span><span class="sxs-lookup"><span data-stu-id="c08f5-166">Update-Help -Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c08f5-167">Секвенсор App-V</span><span class="sxs-lookup"><span data-stu-id="c08f5-167">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="c08f5-168">Update-Help-Module AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="c08f5-168">Update-Help -Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c08f5-169">Клиент App-V</span><span class="sxs-lookup"><span data-stu-id="c08f5-169">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="c08f5-170">Update-Help-Module AppvClient</span><span class="sxs-lookup"><span data-stu-id="c08f5-170">Update-Help -Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c08f5-171">На веб-страницах TechNet</span><span class="sxs-lookup"><span data-stu-id="c08f5-171">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="c08f5-172">Ознакомьтесь с разделом App-V в разделе <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> Автоматизация пакета оптимизации рабочей среды Microsoft для Windows PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="c08f5-172">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-display-help-cmdlet"></a><span data-ttu-id="c08f5-173">Отображение справки для командлета PowerShell</span><span class="sxs-lookup"><span data-stu-id="c08f5-173">Displaying the help for a PowerShell cmdlet</span></span>
<span data-ttu-id="c08f5-174">Чтобы отобразить справку для определенного командлета PowerShell, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c08f5-174">To display help for a specific PowerShell cmdlet:</span></span>

1.  <span data-ttu-id="c08f5-175">Откройте Windows PowerShell или интегрированную среду сценариев Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="c08f5-175">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="c08f5-176">Введите **командлет Get-Help** &lt; *cmdlet* &gt; , например **Get-Help Publish-AppvClientPackage**.</span><span class="sxs-lookup"><span data-stu-id="c08f5-176">Type **Get-Help** &lt;*cmdlet*&gt;, for example, **Get-Help Publish-AppvClientPackage**.</span></span>

<span data-ttu-id="c08f5-177">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="c08f5-177">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="c08f5-178">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="c08f5-178">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="c08f5-179">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="c08f5-179">Got an App-V issue?</span></span>** <span data-ttu-id="c08f5-180">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="c08f5-180">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

 

 





