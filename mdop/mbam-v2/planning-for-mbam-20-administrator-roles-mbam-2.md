---
title: Планирование ролей администратора MBAM 2.0
description: Планирование ролей администратора MBAM 2.0
author: dansimp
ms.assetid: 6f813297-6479-42d3-a21b-896d54466b5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a89a04c0ef074407dc3cd081d351d44023e65e70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824892"
---
# <span data-ttu-id="06df2-103">Планирование ролей администратора MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="06df2-103">Planning for MBAM 2.0 Administrator Roles</span></span>


<span data-ttu-id="06df2-104">В этом разделе перечислены и описаны доступные роли администраторов, которые доступны в администрировании и мониторинге Microsoft BitLocker (MBAM), а также на серверах, где создаются локальные группы.</span><span class="sxs-lookup"><span data-stu-id="06df2-104">This topic lists and describes the available administrator roles that are available in Microsoft BitLocker Administration and Monitoring (MBAM) as well as the server locations where the local groups are created.</span></span>

## <span data-ttu-id="06df2-105">Роли администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="06df2-105">MBAM Administrator Roles</span></span>


<a href="" id="---------------mbam-system-administrators"></a> **<span data-ttu-id="06df2-106">Системные администраторы MBAM</span><span class="sxs-lookup"><span data-stu-id="06df2-106">MBAM System Administrators</span></span>**  
<span data-ttu-id="06df2-107">Администраторы этой роли имеют доступ ко всем функциям администрирования и наблюдения Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="06df2-107">Administrators in this role have access to all Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="06df2-108">Локальная группа для этой роли установлена на сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="06df2-108">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-helpdesk-users"></a> **<span data-ttu-id="06df2-109">Пользователи службы поддержки MBAM</span><span class="sxs-lookup"><span data-stu-id="06df2-109">MBAM Helpdesk Users</span></span>**  
<span data-ttu-id="06df2-110">Администраторы этой роли имеют доступ к возможностям службы поддержки в MBAM.</span><span class="sxs-lookup"><span data-stu-id="06df2-110">Administrators in this role have access to the Help Desk features from MBAM.</span></span> <span data-ttu-id="06df2-111">Локальная группа для этой роли установлена на сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="06df2-111">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-report-users"></a> **<span data-ttu-id="06df2-112">Пользователи отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="06df2-112">MBAM Report Users</span></span>**  
<span data-ttu-id="06df2-113">Администраторы этой роли имеют доступ к отчетам о соответствии и аудиту в MBAM.</span><span class="sxs-lookup"><span data-stu-id="06df2-113">Administrators in this role have access to the Compliance and Audit Reports from MBAM.</span></span> <span data-ttu-id="06df2-114">Локальная группа для этой роли устанавливается на сервере администрирования и мониторинга, базу данных соответствия требованиям и аудита, а также на сервере, на котором размещаются отчеты о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="06df2-114">The local group for this role is installed on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports.</span></span>

<a href="" id="---------------mbam-advanced-helpdesk-users"></a> **<span data-ttu-id="06df2-115">MBAM опытных пользователей службы поддержки</span><span class="sxs-lookup"><span data-stu-id="06df2-115">MBAM Advanced Helpdesk Users</span></span>**  
<span data-ttu-id="06df2-116">Администраторы этой роли увеличивают доступ к возможностям службы поддержки в MBAM.</span><span class="sxs-lookup"><span data-stu-id="06df2-116">Administrators in this role have increased access to the Help Desk features from MBAM.</span></span> <span data-ttu-id="06df2-117">Локальная группа для этой роли установлена на сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="06df2-117">The local group for this role is installed on the Administration and Monitoring Server.</span></span> <span data-ttu-id="06df2-118">Если пользователь является членом пользователей службы поддержки MBAM и MBAM опытных пользователей службы поддержки, то разрешения пользователей на дополнительные службы поддержки MBAM будут переопределять разрешения пользователей службы поддержки MBAM.</span><span class="sxs-lookup"><span data-stu-id="06df2-118">If a user is a member of both MBAM Helpdesk Users and MBAM Advanced Helpdesk Users, the MBAM Advanced Helpdesk Users permissions will override the MBAM Helpdesk User permissions.</span></span>

<span data-ttu-id="06df2-119">**Важно!**  Для просмотра отчетов пользователь, который является администратором, должен быть членом группы безопасности " **Пользователи отчетов MBAM** " на сервере администрирования и мониторинга, а также в базе данных проверки соответствия и аудита, а также на сервере, на котором размещается функция "отчеты о соответствии и аудите".</span><span class="sxs-lookup"><span data-stu-id="06df2-119">**Important** To view reports, an administrative user must be a member of the **MBAM Report Users** security group on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports feature.</span></span> <span data-ttu-id="06df2-120">Рекомендуется создать группу безопасности в доменных службах Active Directory с правами доступа к локальной группе безопасности " **Пользователи MBAM отчетов** " на сервере администрирования и мониторинга и на сервере, на котором размещаются отчеты о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="06df2-120">As a best practice, create a security group in Active Directory Domain Services with rights on the local **MBAM Report Users** security group on both the Administration and Monitoring Server and the server that hosts the Compliance and Audit Reports.</span></span>

 

## <span data-ttu-id="06df2-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="06df2-121">Related topics</span></span>


[<span data-ttu-id="06df2-122">Подготовка среды для развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="06df2-122">Preparing your Environment for MBAM 2.0</span></span>](preparing-your-environment-for-mbam-20-mbam-2.md)

 

 





