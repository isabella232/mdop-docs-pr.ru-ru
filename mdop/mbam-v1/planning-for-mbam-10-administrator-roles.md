---
title: Планирование ролей администратора MBAM 1.0
description: Планирование ролей администратора MBAM 1.0
author: dansimp
ms.assetid: 95be0eb4-25e9-43ca-a8e7-27373d35544d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 104d650824330ea990881c520a7811511f496dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825889"
---
# <span data-ttu-id="3e2a0-103">Планирование ролей администратора MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="3e2a0-103">Planning for MBAM 1.0 Administrator Roles</span></span>


<span data-ttu-id="3e2a0-104">В этой статье описаны роли администраторов, доступные в администрировании и мониторинге Microsoft BitLocker (MBAM), а также расположения серверов, на которых создаются локальные группы.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-104">This topic includes and describes the administrator roles that are available in Microsoft BitLocker Administration and Monitoring (MBAM), as well as the server locations where the local groups are created.</span></span>

## <span data-ttu-id="3e2a0-105">Роли администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="3e2a0-105">MBAM Administrator roles</span></span>


<a href="" id="---------------mbam-system-administrators"></a> **<span data-ttu-id="3e2a0-106">Системные администраторы MBAM</span><span class="sxs-lookup"><span data-stu-id="3e2a0-106">MBAM System Administrators</span></span>**  
<span data-ttu-id="3e2a0-107">Администраторы в этой роли имеют доступ ко всем функциям MBAM.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-107">Administrators in this role have access to all MBAM features.</span></span> <span data-ttu-id="3e2a0-108">Локальная группа для этой роли установлена на сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-108">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-hardware-users"></a> **<span data-ttu-id="3e2a0-109">Пользователи MBAM оборудования</span><span class="sxs-lookup"><span data-stu-id="3e2a0-109">MBAM Hardware Users</span></span>**  
<span data-ttu-id="3e2a0-110">Администраторы этой роли имеют доступ к функциям возможностей оборудования из MBAM.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-110">Administrators in this role have access to the Hardware Capability features from MBAM.</span></span> <span data-ttu-id="3e2a0-111">Локальная группа для этой роли установлена на сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-111">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-helpdesk-users"></a> **<span data-ttu-id="3e2a0-112">Пользователи службы поддержки MBAM</span><span class="sxs-lookup"><span data-stu-id="3e2a0-112">MBAM Helpdesk Users</span></span>**  
<span data-ttu-id="3e2a0-113">Администраторы этой роли имеют доступ к функциям службы поддержки из MBAM.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-113">Administrators in this role have access to the Helpdesk features from MBAM.</span></span> <span data-ttu-id="3e2a0-114">Локальная группа для этой роли установлена на сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-114">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam--report-users"></a> **<span data-ttu-id="3e2a0-115">Пользователи отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="3e2a0-115">MBAM Report Users</span></span>**  
<span data-ttu-id="3e2a0-116">Администраторы этой роли имеют доступ к функции "отчеты о соответствии и аудиту" в MBAM.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-116">Administrators in this role have access to the Compliance and Audit Reports feature from MBAM.</span></span> <span data-ttu-id="3e2a0-117">Локальная группа для этой роли устанавливается на сервере администрирования и мониторинга, базу данных соответствия требованиям и аудита, а также на сервере, на котором размещаются отчеты о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-117">The local group for this role is installed on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports.</span></span>

<a href="" id="---------------mbam--advanced-helpdesk-users"></a> **<span data-ttu-id="3e2a0-118">MBAM опытных пользователей службы поддержки</span><span class="sxs-lookup"><span data-stu-id="3e2a0-118">MBAM Advanced Helpdesk Users</span></span>**  
<span data-ttu-id="3e2a0-119">Администраторы этой роли увеличивают доступ к функциям службы поддержки из MBAM.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-119">Administrators in this role have increased access to the Helpdesk features from MBAM.</span></span> <span data-ttu-id="3e2a0-120">Локальная группа для этой роли установлена на сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-120">The local group for this role is installed on the Administration and Monitoring Server.</span></span> <span data-ttu-id="3e2a0-121">Если пользователь является членом пользователей службы поддержки MBAM и MBAM опытных пользователей службы поддержки, то разрешения пользователей расширенной службы поддержки MBAM перезаписывают разрешения пользователей службы поддержки MBAM.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-121">If a user is a member of both MBAM Helpdesk Users and MBAM Advanced Helpdesk Users, the MBAM Advanced Helpdesk Users permissions will overwrite the MBAM Helpdesk User permissions.</span></span>

<span data-ttu-id="3e2a0-122">**Важно!**  Для просмотра отчетов пользователь, который является администратором, должен быть членом группы безопасности " **Пользователи отчетов MBAM** " на сервере администрирования и мониторинга сервера, соответствия требованиям и аудита базы данных и на сервере, на котором размещается функция соответствия требованиям и отчетов.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-122">**Important** To view the reports, an administrative user must be a member of the **MBAM Report Users** security group on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Reports feature.</span></span> <span data-ttu-id="3e2a0-123">Рекомендуется создать в Active Directory группу безопасности с правами доступа к локальной группе безопасности " **Пользователи MBAM отчетов** " на сервере администрирования и мониторинга и на сервере, на котором размещается соответствие и отчеты.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-123">As a best practice, create a security group in Active Directory with rights on the local **MBAM Report Users** security group on both the Administration and Monitoring Server and on the server that hosts the Compliance and Reports.</span></span>

 

## <span data-ttu-id="3e2a0-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3e2a0-124">Related topics</span></span>


[<span data-ttu-id="3e2a0-125">Подготовка среды для развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="3e2a0-125">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)

 

 





