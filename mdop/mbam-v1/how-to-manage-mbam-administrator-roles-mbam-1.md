---
title: Управление ролями администратора MBAM
description: Управление ролями администратора MBAM
author: dansimp
ms.assetid: c0f25a42-dbff-418d-a776-4fe23ee07d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d00b8ebf66d2b066afae33e67298691285ce9fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812968"
---
# <span data-ttu-id="ca553-103">Управление ролями администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="ca553-103">How to Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="ca553-104">После завершения настройки администрирования и мониторинга Microsoft BitLocker (MBAM) для всех функций сервера администраторам необходимо предоставить доступ к этим функциям сервера.</span><span class="sxs-lookup"><span data-stu-id="ca553-104">After Microsoft BitLocker Administration and Monitoring (MBAM) Setup is complete for all server features, administrative users must be granted access to these server features.</span></span> <span data-ttu-id="ca553-105">Рекомендуется, чтобы администраторы, которые будут управлять и использовать функции сервера MBAM, были назначены группам безопасности Active Directory, а затем эти группы должны быть добавлены в соответствующую административную локальную группу MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca553-105">As a best practice, administrators who will manage or use MBAM server features, should be assigned to Active Directory security groups and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

**<span data-ttu-id="ca553-106">Управление членством в роли администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="ca553-106">To manage MBAM Administrator Role memberships</span></span>**

1.  <span data-ttu-id="ca553-107">Назначение административных пользователей группам безопасности в службах ActiveDirectoryDomain.</span><span class="sxs-lookup"><span data-stu-id="ca553-107">Assign administrative users to security groups in ActiveDirectoryDomain Services.</span></span>

2.  <span data-ttu-id="ca553-108">Для соответствующих функций добавьте группы безопасности служб ActiveDirectoryDomain в роли для MBAM локальных групп администраторов Microsoft BitLocker на сервере администрирования и наблюдения за ними.</span><span class="sxs-lookup"><span data-stu-id="ca553-108">Add ActiveDirectoryDomain Services security groups to the roles for MBAM administrative local groups on the Microsoft BitLocker Administration and Monitoring server for the respective features.</span></span> <span data-ttu-id="ca553-109">Ниже указаны роли пользователей.</span><span class="sxs-lookup"><span data-stu-id="ca553-109">The user roles are as follows:</span></span>

    -   <span data-ttu-id="ca553-110">**MBAM System Administrators** имеет доступ ко всем функциям администрирования и мониторинга Microsoft BitLocker на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca553-110">**MBAM System Administrators** have access to all Microsoft BitLocker Administration and Monitoring features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="ca553-111">**Пользователи оборудования MBAM** имеют доступ к функциям совместимости оборудования на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca553-111">**MBAM Hardware Users** have access to the Hardware Compatibility features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="ca553-112">**Пользователи службы поддержки MBAM** имеют доступ к параметрам управления TPM и восстановлению дисков на веб-сайте администрирования MBAM, но при использовании любого из этих параметров необходимо заполнить все поля.</span><span class="sxs-lookup"><span data-stu-id="ca553-112">**MBAM Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM administration website, but must fill in all fields when they use either option.</span></span>

    -   <span data-ttu-id="ca553-113">**Пользователи отчетов MBAM** имеют доступ к отчетам о соответствии и аудиту на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca553-113">**MBAM Report Users** have access to the Compliance and Audit reports in the MBAM administration website.</span></span>

    -   <span data-ttu-id="ca553-114">**MBAM с дополнительными справочными** специалистами имеют доступ к параметрам управление TPM и восстановлением дисков на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca553-114">**MBAM Advanced Helpdesk Uses** have access to the Manage TPM and Drive Recovery options in the MBAM administration website.</span></span> <span data-ttu-id="ca553-115">Эти пользователи не обязаны заполнять все поля при использовании любого из этих параметров.</span><span class="sxs-lookup"><span data-stu-id="ca553-115">These users are not required to fill in all fields when they use either option.</span></span>

    <span data-ttu-id="ca553-116">Дополнительные сведения о ролях для администрирования и мониторинга Microsoft BitLocker можно найти в разделе [Планирование ролей администратора для MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ca553-116">For more information about roles for Microsoft BitLocker Administration and Monitoring, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

## <span data-ttu-id="ca553-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ca553-117">Related topics</span></span>


[<span data-ttu-id="ca553-118">Администрирование компонентов MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="ca553-118">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





