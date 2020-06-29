---
title: Создание связывающей группы с опубликованными пользователями и глобально опубликованными пакетами
description: Создание связывающей группы с опубликованными пользователями и глобально опубликованными пакетами
author: dansimp
ms.assetid: 851b8742-0283-4aa6-b3a3-f7f6289824c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 230e687360920c05a214624750eba54dc84b5731
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814365"
---
# <span data-ttu-id="6fba7-103">Создание связывающей группы с опубликованными пользователями и глобально опубликованными пакетами</span><span class="sxs-lookup"><span data-stu-id="6fba7-103">How to Create a Connection Group with User-Published and Globally Published Packages</span></span>


<span data-ttu-id="6fba7-104">Вы можете создавать группы подключений пользователей, которые содержат как опубликованные пользователями, так и глобально опубликованные пакеты, используя один из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="6fba7-104">You can create user-entitled connection groups that contain both user-published and globally published packages, using either of the following methods:</span></span>

-   [<span data-ttu-id="6fba7-105">Использование командлетов PowerShell для создания групп подключений пользователей</span><span class="sxs-lookup"><span data-stu-id="6fba7-105">How to use PowerShell cmdlets to create the user-entitled connection groups</span></span>](#bkmk-posh-userentitled-cg)

-   [<span data-ttu-id="6fba7-106">Использование сервера App-V для создания групп подключений пользователей</span><span class="sxs-lookup"><span data-stu-id="6fba7-106">How to use the App-V Server to create the user-entitled connection groups</span></span>](#bkmk-appvserver-userentitled-cg)

**<span data-ttu-id="6fba7-107">Что нужно знать перед началом работы:</span><span class="sxs-lookup"><span data-stu-id="6fba7-107">What to know before you start:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6fba7-108">Неподдерживаемые сценарии и потенциальные проблемы</span><span class="sxs-lookup"><span data-stu-id="6fba7-108">Unsupported scenarios and potential issues</span></span></th>
<th align="left"><span data-ttu-id="6fba7-109">Результат</span><span class="sxs-lookup"><span data-stu-id="6fba7-109">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6fba7-110">Вы не можете включать опубликованные пользователем пакеты в глобальных группах подключений.</span><span class="sxs-lookup"><span data-stu-id="6fba7-110">You cannot include user-published packages in globally entitled connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fba7-111">Не удается выполнить группу подключения.</span><span class="sxs-lookup"><span data-stu-id="6fba7-111">The connection group will fail.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6fba7-112">Если вы публикуете пакет глобально и затем создаете пользовательскую группу подключения, в которой вы сделали этот пакет необязательными, вы по-прежнему можете выполнить команду <strong> UNPUBLISH-AppvClientPackage &lt; &gt; -Global, </strong> чтобы отменить публикацию пакета, даже если этот пакет используется в другой группе подключения.</span><span class="sxs-lookup"><span data-stu-id="6fba7-112">If you publish a package globally and then create a user-published connection group in which you’ve made that package non-optional, you can still run <strong>Unpublish-AppvClientPackage &lt;package&gt; -global</strong> to unpublish the package, even when that package is being used in another connection group.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fba7-113">Если какие бы то ни было другие группы соединения использовали этот пакет, пакет не будет работать в этих группах подключения.</span><span class="sxs-lookup"><span data-stu-id="6fba7-113">If any other connection groups are using that package, the package will fail in those connection groups.</span></span></p>
<p><span data-ttu-id="6fba7-114">Чтобы избежать непреднамеренной отмены публикации необязательного пакета, который используется в другой группе подключения, мы рекомендуем отслеживать группы, в которых вы использовали необязательный пакет.</span><span class="sxs-lookup"><span data-stu-id="6fba7-114">To avoid inadvertently unpublishing a non-optional package that is being used in another connection group, we recommend that you track the connection groups in which you’ve used a non-optional package.</span></span></p></td>
</tr>
</tbody>
</table>

<a href="" id="bkmk-posh-userentitled-cg"></a>**<span data-ttu-id="6fba7-115">Использование командлетов PowerShell для создания групп подключений пользователей</span><span class="sxs-lookup"><span data-stu-id="6fba7-115">How to use PowerShell cmdlets to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="6fba7-116">Добавьте и опубликуйте пакеты с помощью следующих команд:</span><span class="sxs-lookup"><span data-stu-id="6fba7-116">Add and publish packages by using the following commands:</span></span>

    **<span data-ttu-id="6fba7-117">Add-AppvClientPackage Package1 \ _AppV \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="6fba7-117">Add-AppvClientPackage Package1\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="6fba7-118">Add-AppvClientPackage Package2 \ _AppV \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="6fba7-118">Add-AppvClientPackage Package2\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="6fba7-119">Publish-AppvClientPackage-PackageId Package1 \ _ID-VersionId Package1 \ _Version ID-Global</span><span class="sxs-lookup"><span data-stu-id="6fba7-119">Publish-AppvClientPackage -PackageId Package1\_ID-VersionId Package1\_Version ID -Global</span></span>**

    **<span data-ttu-id="6fba7-120">Publish-AppvClientPackage-PackageId Package2 \ _ID-VersionIdPackage2 \ _ID</span><span class="sxs-lookup"><span data-stu-id="6fba7-120">Publish-AppvClientPackage -PackageId Package2\_ID -VersionIdPackage2\_ID</span></span>**

2.  <span data-ttu-id="6fba7-121">Создайте XML-файл группы подключения.</span><span class="sxs-lookup"><span data-stu-id="6fba7-121">Create the connection group XML file.</span></span> <span data-ttu-id="6fba7-122">Дополнительные сведения можно найти [в разделе о файле группы подключения](about-the-connection-group-file51.md).</span><span class="sxs-lookup"><span data-stu-id="6fba7-122">For more information, see [About the Connection Group File](about-the-connection-group-file51.md).</span></span>

3.  <span data-ttu-id="6fba7-123">Добавьте и опубликуйте группу подключений с помощью следующих команд:</span><span class="sxs-lookup"><span data-stu-id="6fba7-123">Add and publish the connection group by using the following commands:</span></span>

    **<span data-ttu-id="6fba7-124">Подключение Add-AppvClientConnectionGroup _Group \ _XML \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="6fba7-124">Add-AppvClientConnectionGroup Connection\_Group\_XML\_file\_Path</span></span>**

    **<span data-ttu-id="6fba7-125">Enable-AppvClientConnectionGroup-GroupId CG \ _Group \ _ID-VersionId CG \ _Version \ _ID</span><span class="sxs-lookup"><span data-stu-id="6fba7-125">Enable-AppvClientConnectionGroup -GroupId CG\_Group\_ID-VersionId CG\_Version\_ID</span></span>**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**<span data-ttu-id="6fba7-126">Создание групп подключений пользователей с помощью App-V Server</span><span class="sxs-lookup"><span data-stu-id="6fba7-126">How to use the App-V Server to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="6fba7-127">Откройте консоль управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="6fba7-127">Open the App-V 5.1 Management Console.</span></span>

2.  <span data-ttu-id="6fba7-128">Следуйте инструкциям по [публикации пакета с помощью консоли управления](how-to-publish-a-package-by-using-the-management-console-51.md) , чтобы опубликовать пакеты глобально и с учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="6fba7-128">Follow the instructions in [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md) to publish packages globally and to the user.</span></span>

3.  <span data-ttu-id="6fba7-129">Следуйте инструкциям, [чтобы](how-to-create-a-connection-group51.md) создать группу подключения для создания группы подключения и добавить опубликованные пользователем и глобально опубликованные пакеты.</span><span class="sxs-lookup"><span data-stu-id="6fba7-129">Follow the instructions in [How to Create a Connection Group](how-to-create-a-connection-group51.md) to create the connection group, and add the user-published and globally published packages.</span></span>

    <span data-ttu-id="6fba7-130">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="6fba7-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="6fba7-131">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="6fba7-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="6fba7-132">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="6fba7-132">Got an App-V issue?</span></span>** <span data-ttu-id="6fba7-133">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="6fba7-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="6fba7-134">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="6fba7-134">Related topics</span></span>


[<span data-ttu-id="6fba7-135">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="6fba7-135">Managing Connection Groups</span></span>](managing-connection-groups51.md)

[<span data-ttu-id="6fba7-136">Использование дополнительных пакетов в группах соединений</span><span class="sxs-lookup"><span data-stu-id="6fba7-136">How to Use Optional Packages in Connection Groups</span></span>](how-to-use-optional-packages-in-connection-groups51.md)

 

 




