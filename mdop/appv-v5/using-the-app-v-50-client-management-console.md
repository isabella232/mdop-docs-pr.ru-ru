---
title: Использование консоли управления клиентами App-V 5.0
description: Использование консоли управления клиентами App-V 5.0
author: dansimp
ms.assetid: 36398307-57dd-40f3-9d4f-b09f44fd37c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8541e5bc59334b9074a3940dad7cdf0114205d4c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813261"
---
# <span data-ttu-id="35ecb-103">Использование консоли управления клиентами App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="35ecb-103">Using the App-V 5.0 Client Management Console</span></span>


<span data-ttu-id="35ecb-104">В этом разделе приводятся сведения о том, как настроить клиент App-V 5,0 и управлять им.</span><span class="sxs-lookup"><span data-stu-id="35ecb-104">This topic provides information about how you can configure and manage the App-V 5.0 client.</span></span>

## <span data-ttu-id="35ecb-105">Изменение конфигурации клиента App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="35ecb-105">Modify App-V 5.0 client configuration</span></span>


<span data-ttu-id="35ecb-106">У клиента App-V 5,0 есть связанные параметры, которые можно настроить, чтобы определить, как клиент будет работать в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="35ecb-106">The App-V 5.0 client has associated settings that can be configured to determine how the client will run in your environment.</span></span> <span data-ttu-id="35ecb-107">Вы можете управлять этими параметрами на компьютере, на котором запущен клиент, или с помощью оболочки PowerShell или групповой политики.</span><span class="sxs-lookup"><span data-stu-id="35ecb-107">You can manage these settings on the computer that runs the client or by using PowerShell or Group Policy.</span></span> <span data-ttu-id="35ecb-108">Дополнительные сведения о том, как изменить клиент с помощью PowerShell или конфигурации групповой политики, можно найти в разделе [изменение конфигурации клиента с помощью PowerShell](how-to-modify-client-configuration-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="35ecb-108">For more information about how to modify the client using PowerShell or Group Policy configuration see, [How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell.md).</span></span>

## <a href="" id="the-app-v-5-0-client-management-console-"></a><span data-ttu-id="35ecb-109">Консоль управления клиентом App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="35ecb-109">The App-V 5.0 client management console</span></span>


<span data-ttu-id="35ecb-110">Вы можете получить сведения о клиенте App-V 5,0 или выполнить определенные задачи с помощью консоли управления клиентом App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="35ecb-110">You can obtain information about the App-V 5.0 client or perform specific tasks by using the App-V 5.0 client management console.</span></span> <span data-ttu-id="35ecb-111">Многие задачи, которые можно выполнять на консоли управления клиентом, также можно выполнять с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="35ecb-111">Many of the tasks that you can perform in the client management console you can also perform by using PowerShell.</span></span> <span data-ttu-id="35ecb-112">Соответствующие командлеты PowerShell для каждого действия также отображаются в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="35ecb-112">The associated PowerShell cmdlets for each action are also displayed in the following table.</span></span> <span data-ttu-id="35ecb-113">Дополнительные сведения об использовании PowerShell можно найти в разделе [Администрирование App-V с помощью PowerShell](administering-app-v-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="35ecb-113">For more information about how to use PowerShell, see [Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md).</span></span>

<span data-ttu-id="35ecb-114">Консоль управления клиентом включает описанные ниже основные вкладки.</span><span class="sxs-lookup"><span data-stu-id="35ecb-114">The client management console contains the following described main tabs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="35ecb-115">TAB</span><span class="sxs-lookup"><span data-stu-id="35ecb-115">Tab</span></span></th>
<th align="left"><span data-ttu-id="35ecb-116">Описание</span><span class="sxs-lookup"><span data-stu-id="35ecb-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="35ecb-117">Обзор</span><span class="sxs-lookup"><span data-stu-id="35ecb-117">Overview</span></span></p></td>
<td align="left"><p><span data-ttu-id="35ecb-118"><strong>Вкладка Обзор </strong> включает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="35ecb-118">The <strong>Overview</strong> tab contains the following elements:</span></span></p>
<ul>
<li><p><span data-ttu-id="35ecb-119">Update (обновление) — используйте <strong> </strong> плитку обновления, чтобы обновить виртуализированное приложение или получить новый виртуализированный пакет.</span><span class="sxs-lookup"><span data-stu-id="35ecb-119">Update – Use the <strong>Update</strong> tile to refresh a virtualized application or to receive a new virtualized package.</span></span></p>
<p><span data-ttu-id="35ecb-120"><strong>Последнее обновление </strong> отображает текущую версию виртуализированного пакета.</span><span class="sxs-lookup"><span data-stu-id="35ecb-120">The <strong>Last Refresh</strong> displays the current version of the virtualized package.</span></span></p></li>
<li><p><span data-ttu-id="35ecb-121">Скачайте все виртуальные приложения — используйте <strong> плитку Download (скачать </strong> ), чтобы скачать все пакеты, подготовленные для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="35ecb-121">Download all virtual applications – Use the <strong>Download</strong> tile to download all of the packages provisioned to the current user.</span></span></p>
<p><span data-ttu-id="35ecb-122">(Связанный командлет PowerShell: <strong> Mount-AppvClientPackage </strong> )</span><span class="sxs-lookup"><span data-stu-id="35ecb-122">(Associated PowerShell cmdlet: <strong>Mount-AppvClientPackage</strong>)</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="35ecb-123">Автономная работа – эта плитка позволяет запретить все автоматические и ручные обновления виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="35ecb-123">Work Offline – Use this tile to disallow all automatic and manual virtual application updates.</span></span></p>
<p><span data-ttu-id="35ecb-124">(Связанный командлет PowerShell: <strong> Set-AppvPublishServer – UserRefreshEnabled – GlobalRefreshEnabled </strong> )</span><span class="sxs-lookup"><span data-stu-id="35ecb-124">(Associated PowerShell cmdlet: <strong>Set-AppvPublishServer –UserRefreshEnabled –GlobalRefreshEnabled</strong>)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="35ecb-125">Виртуальные приложения</span><span class="sxs-lookup"><span data-stu-id="35ecb-125">Virtual Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="35ecb-126">На <strong> </strong> вкладке "виртуальные приложения" отображаются все пакеты, которые были опубликованы для пользователя.</span><span class="sxs-lookup"><span data-stu-id="35ecb-126">The <strong>VIRTUAL APPS</strong> tab displays all of the packages that have been published to the user.</span></span> <span data-ttu-id="35ecb-127">Вы также можете щелкнуть конкретный пакет и просмотреть все приложения, которые являются частью этого пакета.</span><span class="sxs-lookup"><span data-stu-id="35ecb-127">You can also click a specific package and see all of the applications that are part of that package.</span></span> <span data-ttu-id="35ecb-128">Отображаются сведения о пакетах, которые в настоящее время используются и о том, сколько пакетов загружено на компьютер.</span><span class="sxs-lookup"><span data-stu-id="35ecb-128">This displays information about packages that are currently in use and how much of each package has been downloaded to the computer.</span></span> <span data-ttu-id="35ecb-129">Вы также можете запустить и остановить загрузку пакетов.</span><span class="sxs-lookup"><span data-stu-id="35ecb-129">You can also start and stop package downloads.</span></span> <span data-ttu-id="35ecb-130">Кроме того, вы можете восстановить состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="35ecb-130">Additionally, you can repair the user state.</span></span> <span data-ttu-id="35ecb-131">При восстановлении удаляются все пользовательские данные, связанные с пакетом.</span><span class="sxs-lookup"><span data-stu-id="35ecb-131">A repair will delete all user data that is associated with a package.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="35ecb-132">Группы подключений приложений</span><span class="sxs-lookup"><span data-stu-id="35ecb-132">App Connection Groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="35ecb-133">На <strong> вкладке группы подключения приложения </strong> отображаются все группы подключений, доступные для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="35ecb-133">The <strong>APP CONNECTION GROUPS</strong> tab displays all of the connection groups that are available to the current user.</span></span> <span data-ttu-id="35ecb-134">Щелкните нужную группу подключения, чтобы просмотреть все пакеты, которые являются частью выбранной группы.</span><span class="sxs-lookup"><span data-stu-id="35ecb-134">Click a specific connection group to see all of the packages that are part of the selected group.</span></span> <span data-ttu-id="35ecb-135">Будут отображены сведения о уже используемых группах соединений и о том, сколько содержимого группы подключения было скачано на компьютере.</span><span class="sxs-lookup"><span data-stu-id="35ecb-135">This displays information about connection groups that are already in use and how much of the connection group contents have been downloaded to the computer.</span></span> <span data-ttu-id="35ecb-136">Кроме того, вы можете запускать и останавливать загрузку групп подключений.</span><span class="sxs-lookup"><span data-stu-id="35ecb-136">Additionally, you can start and stop connection group downloads.</span></span> <span data-ttu-id="35ecb-137">Вы можете использовать этот раздел для начала восстановления.</span><span class="sxs-lookup"><span data-stu-id="35ecb-137">You can use this section to initiate a repair.</span></span> <span data-ttu-id="35ecb-138">При восстановлении будет удалено все состояние пользователя, связанное с группой подключения.</span><span class="sxs-lookup"><span data-stu-id="35ecb-138">A repair will remove all of the user state that is associated a connection group.</span></span></p>
<p><span data-ttu-id="35ecb-139">(Связанные командлеты PowerShell: download- <strong> Mount-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="35ecb-139">(Associated PowerShell cmdlets: Download - <strong>Mount-AppvClientConnectionGroup</strong>.</span></span> <span data-ttu-id="35ecb-140">Repair ( <strong> восстановить </strong> ) — AppvClientConnectionGroup.)</span><span class="sxs-lookup"><span data-stu-id="35ecb-140">Repair -<strong>AppvClientConnectionGroup</strong>.)</span></span></p>
<p></p></td>
</tr>
</tbody>
</table>

 

[<span data-ttu-id="35ecb-141">Получение доступа к консоли управления клиентами</span><span class="sxs-lookup"><span data-stu-id="35ecb-141">How to Access the Client Management Console</span></span>](how-to-access-the-client-management-console.md)

[<span data-ttu-id="35ecb-142">Настройка клиента для получения обновлений пакетов и групп соединений с сервера публикации</span><span class="sxs-lookup"><span data-stu-id="35ecb-142">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>](how-to-configure-the-client-to-receive-package-and-connection-groups-updates-from-the-publishing-server-beta.md)






## <span data-ttu-id="35ecb-143">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="35ecb-143">Related topics</span></span>


[<span data-ttu-id="35ecb-144">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="35ecb-144">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





