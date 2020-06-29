---
title: Настройка необходимых групп в Active Directory для App-V
description: Настройка необходимых групп в Active Directory для App-V
author: dansimp
ms.assetid: 0010d534-46c0-44a3-b5c1-621b4d5e2c31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa1ab6393dee20203b715311d4e1dfdc4c22c679
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821862"
---
# <span data-ttu-id="56613-103">Настройка необходимых групп в Active Directory для App-V</span><span class="sxs-lookup"><span data-stu-id="56613-103">Configuring Prerequisite Groups in Active Directory for App-V</span></span>


<span data-ttu-id="56613-104">Перед установкой сервера управления Microsoft Application Virtualization (App-V) необходимо создать в Active Directory следующие объекты.</span><span class="sxs-lookup"><span data-stu-id="56613-104">Before you install the Microsoft Application Virtualization (App-V) Management Server, you must create the following objects in Active Directory.</span></span> <span data-ttu-id="56613-105">Приложение App-V использует группы Active Directory для управления доступом к приложениям и административными функциями.</span><span class="sxs-lookup"><span data-stu-id="56613-105">App-V uses Active Directory groups to control access to applications and administrative functions.</span></span> <span data-ttu-id="56613-106">Эти группы будут использоваться в процессе установки сервера и при публикации приложений.</span><span class="sxs-lookup"><span data-stu-id="56613-106">You will use these groups during the server installation process and when publishing applications.</span></span>

## <span data-ttu-id="56613-107">Настройка предварительных групп в службе каталогов Active Directory для виртуализации приложений</span><span class="sxs-lookup"><span data-stu-id="56613-107">Configuring Prerequisite Groups in Active Directory for Application Virtualization</span></span>


<span data-ttu-id="56613-108">В этой таблице перечислены группы Active Directory, необходимые для установки приложения App-V.</span><span class="sxs-lookup"><span data-stu-id="56613-108">This table lists the Active Directory groups that are required for installing App-V.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56613-109">Объект</span><span class="sxs-lookup"><span data-stu-id="56613-109">Object</span></span></th>
<th align="left"><span data-ttu-id="56613-110">Описание</span><span class="sxs-lookup"><span data-stu-id="56613-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56613-111">Организационное подразделение (OU)</span><span class="sxs-lookup"><span data-stu-id="56613-111">Organizational Unit (OU)</span></span></p></td>
<td align="left"><p><span data-ttu-id="56613-112">Создайте подразделение в службе каталогов Active Directory для конкретных групп, необходимых для App-V.</span><span class="sxs-lookup"><span data-stu-id="56613-112">Create an OU in Active Directory for the specific groups required for App-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56613-113">Административная группа App-V</span><span class="sxs-lookup"><span data-stu-id="56613-113">App-V Administrative Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="56613-114">Во время установки сервера управления App-V необходимо выбрать группу Active Directory, которая будет использоваться в качестве группы администраторов App-V для управления административным доступом к консоли управления.</span><span class="sxs-lookup"><span data-stu-id="56613-114">During installation of the App-V Management Server, you must select an Active Directory group to use as the App-V Administrators group to control administrative access to the Management Console.</span></span> <span data-ttu-id="56613-115">Создайте группу безопасности для администраторов App-V и добавьте в эту группу всех пользователей, которые должны использовать консоль управления.</span><span class="sxs-lookup"><span data-stu-id="56613-115">Create a security group for App-V administrators, and add to this group every user who needs to use the Management Console.</span></span> <span data-ttu-id="56613-116">Вы не можете создать эту группу непосредственно из установщика сервера управления App-V.</span><span class="sxs-lookup"><span data-stu-id="56613-116">You cannot create this group directly from the App-V Management Server installer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56613-117">Группа пользователей App-V</span><span class="sxs-lookup"><span data-stu-id="56613-117">App-V Users Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="56613-118">Для App-V требуется, чтобы все учетные записи пользователей, которые обращаются к функциям App-V, были членами политики поставщика, связанной с одной группой, для общего доступа к платформе.</span><span class="sxs-lookup"><span data-stu-id="56613-118">App-V requires that every User account that accesses App-V functions be a member of a provider policy associated with a single group for general platform access.</span></span> <span data-ttu-id="56613-119">Использование существующей группы; Например, пользователи домена, если все пользователи должны иметь доступ к приложению App-V, или создать новую группу.</span><span class="sxs-lookup"><span data-stu-id="56613-119">Use an existing group; for example, Domain Users, if all users are to have access to App-V, or create a new group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56613-120">Группы приложений</span><span class="sxs-lookup"><span data-stu-id="56613-120">Application Groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="56613-121">App-V связывает право на использование отдельного приложения с группой Active Directory.</span><span class="sxs-lookup"><span data-stu-id="56613-121">App-V associates the right to use an individual application with an Active Directory group.</span></span> <span data-ttu-id="56613-122">Создавайте группы Active Directory для каждого приложения и назначайте пользователей этим группам, чтобы управлять доступом пользователей к приложениям.</span><span class="sxs-lookup"><span data-stu-id="56613-122">Create an Active Directory group for each application, and assign users to these groups as needed to control user access to the applications.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="56613-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="56613-123">Related topics</span></span>


[<span data-ttu-id="56613-124">Требования при развертывании Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="56613-124">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

[<span data-ttu-id="56613-125">Настройка Windows Server 2008 для серверов App-V Management Server</span><span class="sxs-lookup"><span data-stu-id="56613-125">How to Configure Windows Server 2008 for App-V Management Servers</span></span>](how-to-configure-windows-server-2008-for-app-v-management-servers.md)

 

 





