---
title: Настройка игнорирования версии пакета группой соединений
description: Настройка игнорирования версии пакета группой соединений
author: dansimp
ms.assetid: 6ebc1bff-d190-4f4c-a6da-e09a4cca7874
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b64d1938419aef184c5df667bf71b8157de0450a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813960"
---
# <span data-ttu-id="6a551-103">Настройка игнорирования версии пакета группой соединений</span><span class="sxs-lookup"><span data-stu-id="6a551-103">How to Make a Connection Group Ignore the Package Version</span></span>


<span data-ttu-id="6a551-104">Microsoft Application Virtualization (App-V) 5,0 с пакетом обновления 3 (SP3) позволяет настроить группу подключений для использования любой версии пакета, которая упрощает обновление пакета и сокращает количество групп соединений, которые необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="6a551-104">Microsoft Application Virtualization (App-V) 5.0 SP3 enables you to configure a connection group to use any version of a package, which simplifies package upgrades and reduces the number of connection groups you need to create.</span></span>

<span data-ttu-id="6a551-105">Чтобы обновить пакет в более ранних версиях App-V, необходимо выполнить несколько действий, включая отключение группы подключения и изменение XML-файла определения группы подключения.</span><span class="sxs-lookup"><span data-stu-id="6a551-105">To upgrade a package in earlier versions of App-V, you had to perform several steps, including disabling the connection group and modifying the connection group’s XML definition file.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a551-106">Описание задачи с помощью App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="6a551-106">Task description with App-V 5.0 SP3</span></span></th>
<th align="left"><span data-ttu-id="6a551-107">Выполнение задачи с помощью App-V 5,0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="6a551-107">How to perform the task with App-V 5.0 SP3</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a551-108">Вы можете настроить группу подключений таким образом, чтобы она принимала любую версию пакета, которая позволяет обновлять пакет без необходимости отключить группу подключения.</span><span class="sxs-lookup"><span data-stu-id="6a551-108">You can configure a connection group to accept any version of a package, which enables you to upgrade the package without having to disable the connection group.</span></span></p>
<p><strong><span data-ttu-id="6a551-109">Как работает эта функция:</span><span class="sxs-lookup"><span data-stu-id="6a551-109">How the feature works:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="6a551-110">Если группа подключений имеет доступ к нескольким версиям пакета, используется новейшая версия.</span><span class="sxs-lookup"><span data-stu-id="6a551-110">If the connection group has access to multiple versions of a package, the latest version is used.</span></span></p></li>
<li><p><span data-ttu-id="6a551-111">Если группа подключения содержит необязательный пакет с неверной версией, пакет игнорируется и не блокирует создание виртуальной среды группы подключения.</span><span class="sxs-lookup"><span data-stu-id="6a551-111">If the connection group contains an optional package that has an incorrect version, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></li>
<li><p><span data-ttu-id="6a551-112">Если группа подключения содержит необязательный пакет с неверной версией, виртуальная среда группы подключения не может быть создана.</span><span class="sxs-lookup"><span data-stu-id="6a551-112">If the connection group contains a non-optional package that has an incorrect version, the connection group’s virtual environment cannot be created.</span></span></p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a551-113">Метод</span><span class="sxs-lookup"><span data-stu-id="6a551-113">Method</span></span></th>
<th align="left"><span data-ttu-id="6a551-114">Действия</span><span class="sxs-lookup"><span data-stu-id="6a551-114">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a551-115">Сервер App-V Server — консоль управления</span><span class="sxs-lookup"><span data-stu-id="6a551-115">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="6a551-116">На консоли управления выберите пункт <strong> пакеты для </strong> &gt; <strong> групп соединений </strong> .</span><span class="sxs-lookup"><span data-stu-id="6a551-116">In the Management Console, select <strong>PACKAGES</strong> &gt; <strong>CONNECTION GROUPS</strong>.</span></span></p></li>
<li><p><span data-ttu-id="6a551-117">Выберите нужную группу подключений в библиотеке групп соединений.</span><span class="sxs-lookup"><span data-stu-id="6a551-117">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="6a551-118">Нажмите кнопку <strong> изменить </strong> в области подключенные пакеты.</span><span class="sxs-lookup"><span data-stu-id="6a551-118">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="6a551-119">Установите флажок <strong> использовать любую версию </strong> рядом с названием пакета и нажмите кнопку <strong> применить </strong> .</span><span class="sxs-lookup"><span data-stu-id="6a551-119">Select <strong>Use Any Version</strong> check box next to the package name, and click <strong>Apply</strong>.</span></span></p></li>
</ol>
<p><span data-ttu-id="6a551-120">Дополнительные сведения о добавлении и обновлении пакетов можно найти <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)"> в разделе Добавление и обновление пакетов с помощью консоли управления </a> .</span><span class="sxs-lookup"><span data-stu-id="6a551-120">For more about adding or upgrading packages, see <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)">How to Add or Upgrade Packages by Using the Management Console</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a551-121">Клиент App-V на отдельном компьютере</span><span class="sxs-lookup"><span data-stu-id="6a551-121">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="6a551-122">Создайте XML-документ группы подключения.</span><span class="sxs-lookup"><span data-stu-id="6a551-122">Create the connection group XML document.</span></span></p></li>
<li><p><span data-ttu-id="6a551-123">Чтобы обновить пакет, задайте <strong> </strong> для атрибутау Tag пакета <strong> VersionID </strong> звездочку ( <strong>\*</strong> ).</span><span class="sxs-lookup"><span data-stu-id="6a551-123">For the package to be upgraded, set the <strong>Package</strong> tag attribute <strong>VersionID</strong> to an asterisk (<strong>\*</strong>).</span></span></p></li>
<li><p><span data-ttu-id="6a551-124">С помощью следующего командлета добавьте группу подключения и укажите путь к XML-документу группы подключения.</span><span class="sxs-lookup"><span data-stu-id="6a551-124">Use the following cmdlet to add the connection group, and include the path to the connection group XML document:</span></span></p>
<p><strong><span data-ttu-id="6a551-125">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="6a551-125">Add-AppvClientConnectionGroup</span></span></strong></p></li>
<li><p><span data-ttu-id="6a551-126">При обновлении пакета используйте следующие командлеты, чтобы удалить старый пакет, добавить обновленный пакет и опубликовать обновленный пакет.</span><span class="sxs-lookup"><span data-stu-id="6a551-126">When you upgrade a package, use the following cmdlets to remove the old package, add the upgraded package, and publish the upgraded package:</span></span></p>
<ul>
<li><p><span data-ttu-id="6a551-127">RemoveAppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6a551-127">RemoveAppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="6a551-128">Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6a551-128">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="6a551-129">Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6a551-129">Publish-AppvClientPackage</span></span></p></li>
</ul></li>
</ol>
<p><span data-ttu-id="6a551-130">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="6a551-130">For more information, see:</span></span></p>
<ul>
<li><p><span data-ttu-id="6a551-131">Пример XML-файла, <strong> XML-файла группы подключения с дополнительными пакетами </strong> , в этом разделе: <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"> использование необязательных пакетов в группах соединений</span><span class="sxs-lookup"><span data-stu-id="6a551-131">The example XML file, <strong>Connection group XML file with optional packages</strong>, in this section: <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">How to Use Optional Packages in Connection Groups</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="6a551-132">Управление пакетами App-V 5.0, работающими на автономном компьютере, с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="6a551-132">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="6a551-133">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="6a551-133">Related topics</span></span>


[<span data-ttu-id="6a551-134">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="6a551-134">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





