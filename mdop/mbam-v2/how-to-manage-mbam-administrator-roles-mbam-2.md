---
title: Управление ролями администратора MBAM
description: Управление ролями администратора MBAM
author: dansimp
ms.assetid: 813ac0c4-3cf9-47af-b4cb-9395fd915e5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14e9128904b448b20e0596a2630627b7ca8e711d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825119"
---
# <span data-ttu-id="6d9cd-103">Управление ролями администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="6d9cd-103">How to Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="6d9cd-104">После завершения настройки администрирования и мониторинга Microsoft BitLocker (MBAM) для всех функций сервера пользователи должны иметь права администратора.</span><span class="sxs-lookup"><span data-stu-id="6d9cd-104">After Microsoft BitLocker Administration and Monitoring (MBAM) Setup is complete for all server features, administrative users will have to be granted access to them.</span></span> <span data-ttu-id="6d9cd-105">Рекомендуется, чтобы администраторы, которые будут управлять и использовать компоненты сервера администрирования Microsoft BitLocker и наблюдения за ним, могли назначаться группам безопасности доменных служб, а затем эти группы должны быть добавлены в соответствующую административную локальную группу MBAM.</span><span class="sxs-lookup"><span data-stu-id="6d9cd-105">As a best practice, administrators who will manage or use Microsoft BitLocker Administration and Monitoring Server features should be assigned to Domain Services security groups, and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

**<span data-ttu-id="6d9cd-106">Управление членством в роли администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="6d9cd-106">To manage MBAM Administrator Role memberships</span></span>**

1.  <span data-ttu-id="6d9cd-107">Назначение административных пользователей группам безопасности в доменных службах ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="6d9cd-107">Assign administrative users to security groups in ActiveDirectory Domain Services.</span></span>

2.  <span data-ttu-id="6d9cd-108">Добавляйте в роли группы безопасности ActiveDirectory для MBAM локальных групп администраторов сервера MBAM для соответствующих функций.</span><span class="sxs-lookup"><span data-stu-id="6d9cd-108">Add ActiveDirectory security groups to the roles for MBAM administrative local groups on the MBAM server for the respective features.</span></span>

    -   <span data-ttu-id="6d9cd-109">**MBAM System Administrators** имеет доступ ко всем функциям MBAM на веб-сайте администрирования MBAM и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="6d9cd-109">**MBAM System Administrators** have access to all MBAM features in the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="6d9cd-110">**Пользователи службы поддержки MBAM** имеют доступ к параметрам "Управление TPM" и "Восстановление диска" на веб-сайте администрирования MBAM и мониторинга, но при использовании любого из этих параметров необходимо заполнить все поля.</span><span class="sxs-lookup"><span data-stu-id="6d9cd-110">**MBAM Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM Administration and Monitoring website, but must fill in all fields when they use either option.</span></span>

    -   <span data-ttu-id="6d9cd-111">**Пользователи отчетов MBAM** имеют доступ к отчетам о соответствии и аудиту на веб-сайте администрирования MBAM и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="6d9cd-111">**MBAM Report Users** have access to the Compliance and Audit reports in the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="6d9cd-112">**Пользователи расширенной службы поддержки MBAM** могут получить доступ к параметрам "Управление TPM" и "Восстановление диска" на веб-сайте администрирования MBAM и мониторинга, но не обязаны заполнять все поля при использовании любого из этих параметров.</span><span class="sxs-lookup"><span data-stu-id="6d9cd-112">**MBAM Advanced Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM Administration and Monitoring website, but are not required to fill in all fields when they use either option.</span></span>

    <span data-ttu-id="6d9cd-113">Дополнительные сведения о ролях для администрирования и мониторинга Microsoft BitLocker можно найти в разделе [Планирование ролей администратора для MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="6d9cd-113">For more information about roles for Microsoft BitLocker Administration and Monitoring, see [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).</span></span>

## <span data-ttu-id="6d9cd-114">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="6d9cd-114">Related topics</span></span>


[<span data-ttu-id="6d9cd-115">Администрирование компонентов MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6d9cd-115">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





