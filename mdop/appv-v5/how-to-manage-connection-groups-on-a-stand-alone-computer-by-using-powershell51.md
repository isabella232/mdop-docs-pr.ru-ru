---
title: Управление группами соединений на отдельном компьютере с помощью PowerShell
description: Управление группами соединений на отдельном компьютере с помощью PowerShell
author: dansimp
ms.assetid: e1589eff-d306-40fb-a0ae-727190dafe26
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ab120f7089619fa01885d5182313dc33fc47f827
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813888"
---
# <span data-ttu-id="7e5da-103">Управление группами соединений на отдельном компьютере с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="7e5da-103">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span>


<span data-ttu-id="7e5da-104">Группа соединений App-V позволяет запускать все виртуальные приложения как определенные наборы пакетов в одной виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="7e5da-104">An App-V connection group allows you to run all the virtual applications as a defined set of packages in a single virtual environment.</span></span> <span data-ttu-id="7e5da-105">Например, вы можете виртуализировать приложение и его подключаемые модули с помощью отдельных пакетов, но запускать их вместе в одной группе подключения.</span><span class="sxs-lookup"><span data-stu-id="7e5da-105">For example, you can virtualize an application and its plug-ins by using separate packages, but run them together in a single connection group.</span></span>

<span data-ttu-id="7e5da-106">XML-файл группы подключения определяет группу подключений, которая выполняется на компьютере, на котором установлен клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="7e5da-106">A connection group XML file defines the connection group that runs on the computer where you’ve installed the App-V client.</span></span> <span data-ttu-id="7e5da-107">Сведения о XML-файле группы подключения и его настройке можно найти [в разделе о файле группы подключения](about-the-connection-group-file51.md).</span><span class="sxs-lookup"><span data-stu-id="7e5da-107">For information about the connection group XML file and how to configure it, see [About the Connection Group File](about-the-connection-group-file51.md).</span></span>

<span data-ttu-id="7e5da-108">В этой статье описаны следующие процедуры:</span><span class="sxs-lookup"><span data-stu-id="7e5da-108">This topic explains the following procedures:</span></span>

-   [<span data-ttu-id="7e5da-109">Добавление и публикация пакетов App-V в группе "подключение"</span><span class="sxs-lookup"><span data-stu-id="7e5da-109">To add and publish the App-V packages in the connection group</span></span>](#bkmk-add-pub-pkgs-in-cg)

-   [<span data-ttu-id="7e5da-110">Добавление и включение группы соединений в клиенте App-V</span><span class="sxs-lookup"><span data-stu-id="7e5da-110">To add and enable the connection group on the App-V client</span></span>](#bkmk-add-enable-cg-on-clt)

-   [<span data-ttu-id="7e5da-111">Включение и отключение группы подключений для определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="7e5da-111">To enable or disable a connection group for a specific user</span></span>](#bkmk-enable-cg-for-user-poshtopic)

-   [<span data-ttu-id="7e5da-112">Разрешение только администраторам поддержки групп подключений</span><span class="sxs-lookup"><span data-stu-id="7e5da-112">To allow only administrators to enable connection groups</span></span>](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a><span data-ttu-id="7e5da-113">*Добавление и публикация пакетов App-V в группе "подключение"*\*</span><span class="sxs-lookup"><span data-stu-id="7e5da-113">*To add and publish the App-V packages in the connection group*\*</span></span>

1.  <span data-ttu-id="7e5da-114">Чтобы добавить пакеты App-V 5,1 и опубликовать их на компьютер с клиентом App-V, введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7e5da-114">To add and publish the App-V 5.1 packages to the computer running the App-V client, type the following command:</span></span>

    <span data-ttu-id="7e5da-115">Add-AppvClientPackage — path c:\\tmpstore\\quartfin.AppV | Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="7e5da-115">Add-AppvClientPackage –path c:\\tmpstore\\quartfin.appv | Publish-AppvClientPackage</span></span>

2.  <span data-ttu-id="7e5da-116">Повторите **действия 1** для каждого пакета в группе подключение.</span><span class="sxs-lookup"><span data-stu-id="7e5da-116">Repeat **step 1** of this procedure for each package in the connection group.</span></span>

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**<span data-ttu-id="7e5da-117">Добавление и включение группы соединений в клиенте App-V</span><span class="sxs-lookup"><span data-stu-id="7e5da-117">To add and enable the connection group on the App-V client</span></span>**

1.  <span data-ttu-id="7e5da-118">Чтобы добавить группу подключения, введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7e5da-118">Add the connection group by typing the following command:</span></span>

    <span data-ttu-id="7e5da-119">Add-AppvClientConnectionGroup — Path c:\\tmpstore\\financ.xml</span><span class="sxs-lookup"><span data-stu-id="7e5da-119">Add-AppvClientConnectionGroup –path c:\\tmpstore\\financ.xml</span></span>

2.  <span data-ttu-id="7e5da-120">Включите группу соединения, введя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7e5da-120">Enable the connection group by typing the following command:</span></span>

    <span data-ttu-id="7e5da-121">Enable-AppvClientConnectionGroup-Name "Financial Applications"</span><span class="sxs-lookup"><span data-stu-id="7e5da-121">Enable-AppvClientConnectionGroup –name “Financial Applications”</span></span>

    <span data-ttu-id="7e5da-122">Если на целевом компьютере выполняются любые виртуальные приложения, которые находятся в пакетах, они будут выполняться внутри виртуальной среды группы подключения и будут доступны для всех виртуальных приложений в других пакетах в группе подключения.</span><span class="sxs-lookup"><span data-stu-id="7e5da-122">When any virtual applications that are in the member packages are run on the target computer, they will run inside the connection group’s virtual environment and will be available to all the virtual applications in the other packages in the connection group.</span></span>

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**<span data-ttu-id="7e5da-123">Включение и отключение группы подключений для определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="7e5da-123">To enable or disable a connection group for a specific user</span></span>**

1.  <span data-ttu-id="7e5da-124">Ознакомьтесь с описанием и требованиями к параметрам.</span><span class="sxs-lookup"><span data-stu-id="7e5da-124">Review the parameter description and requirements:</span></span>

    -   <span data-ttu-id="7e5da-125">Этот параметр позволяет администратору включать или отключать группу подключений для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="7e5da-125">The parameter enables an administrator to enable or disable a connection group for a specific user.</span></span>

    -   <span data-ttu-id="7e5da-126">Чтобы использовать этот параметр, необходимо воспользоваться пакетом обновления 2 (SP2) для App-V 5,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="7e5da-126">You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

    -   <span data-ttu-id="7e5da-127">Вы можете запустить этот командлет из сеанса пользователя или администратора.</span><span class="sxs-lookup"><span data-stu-id="7e5da-127">You can run this cmdlet from the user or administrator session.</span></span>

    -   <span data-ttu-id="7e5da-128">Для использования параметра необходимо войти в систему с помощью учетных данных администратора.</span><span class="sxs-lookup"><span data-stu-id="7e5da-128">You must be logged in with administrative credentials to use the parameter.</span></span>

    -   <span data-ttu-id="7e5da-129">Конечный пользователь должен войти в систему.</span><span class="sxs-lookup"><span data-stu-id="7e5da-129">The end user must be logged in.</span></span>

    -   <span data-ttu-id="7e5da-130">Необходимо указать идентификатор безопасности (SID) конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="7e5da-130">You must provide the end user’s security identifier (SID).</span></span>

2.  <span data-ttu-id="7e5da-131">Используйте указанные ниже командлеты и добавьте необязательный параметр **–** код, где **-** то есть идентификатор безопасности конечного пользователя (SID).</span><span class="sxs-lookup"><span data-stu-id="7e5da-131">Use the following cmdlets, and add the optional **–UserSID** parameter, where **-UserSID** represents the end user’s security identifier (SID):</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7e5da-132">Командлет</span><span class="sxs-lookup"><span data-stu-id="7e5da-132">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="7e5da-133">Примеры:</span><span class="sxs-lookup"><span data-stu-id="7e5da-133">Examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7e5da-134">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="7e5da-134">Enable-AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7e5da-135">Enable-AppVClientConnectionGroup "ConnectionGroupA" — в чем заключается S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="7e5da-135">Enable-AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7e5da-136">Disable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="7e5da-136">Disable -AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7e5da-137">Disable-AppVClientConnectionGroup "ConnectionGroupA" — в чем заключается S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="7e5da-137">Disable -AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**<span data-ttu-id="7e5da-138">Разрешение только администраторам поддержки групп подключений</span><span class="sxs-lookup"><span data-stu-id="7e5da-138">To allow only administrators to enable connection groups</span></span>**

1.  <span data-ttu-id="7e5da-139">Ознакомьтесь с описанием и требованием для использования этого командлета:</span><span class="sxs-lookup"><span data-stu-id="7e5da-139">Review the description and requirement for using this cmdlet:</span></span>

    -   <span data-ttu-id="7e5da-140">Используйте этот командлет и параметр, чтобы настроить клиент App-V таким образом, чтобы он мог включать или отключать группы подключения только для администраторов (конечных пользователей).</span><span class="sxs-lookup"><span data-stu-id="7e5da-140">Use this cmdlet and parameter to configure the App-V client to allow only administrators (not end users) to enable or disable connection groups.</span></span>

    -   <span data-ttu-id="7e5da-141">Для использования этого командлета необходимо использовать по крайней мере App-V 5,0 с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="7e5da-141">You must be using at least App-V 5.0 SP3 to use this cmdlet.</span></span>

2.  <span data-ttu-id="7e5da-142">Выполните следующий командлет и параметр:</span><span class="sxs-lookup"><span data-stu-id="7e5da-142">Run the following cmdlet and parameter:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7e5da-143">Командлет</span><span class="sxs-lookup"><span data-stu-id="7e5da-143">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="7e5da-144">Параметры и значения</span><span class="sxs-lookup"><span data-stu-id="7e5da-144">Parameter and values</span></span></th>
    <th align="left"><span data-ttu-id="7e5da-145">Пример.</span><span class="sxs-lookup"><span data-stu-id="7e5da-145">Example</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7e5da-146">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e5da-146">Set-AppvClientConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7e5da-147">–RequirePublishAsAdmin</span><span class="sxs-lookup"><span data-stu-id="7e5da-147">–RequirePublishAsAdmin</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7e5da-148">0 – ложь</span><span class="sxs-lookup"><span data-stu-id="7e5da-148">0 - False</span></span></p></li>
    <li><p><span data-ttu-id="7e5da-149">1 — истина</span><span class="sxs-lookup"><span data-stu-id="7e5da-149">1 - True</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="7e5da-150">Set-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="7e5da-150">Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="7e5da-151">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7e5da-151">Related topics</span></span>


[<span data-ttu-id="7e5da-152">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="7e5da-152">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="7e5da-153">Администрирование App-V 5.1 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="7e5da-153">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)









