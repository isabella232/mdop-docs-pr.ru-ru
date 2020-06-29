---
title: Выполнение задач администратора AGPM
description: Выполнение задач администратора AGPM
author: dansimp
ms.assetid: 9678b0f4-70a5-411e-a896-afa4dc9ea6c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b412e5b22e46af938d127751fdca1da722a8c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822422"
---
# <span data-ttu-id="8334e-103">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="8334e-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="8334e-104">С помощью расширенного управления групповыми политиками (режимом групповой политики) Администратор РАСШИРЕНного управления правами (полный доступ) настраивает параметры домена и представителей для утверждающих, редакторов, рецензентов и других администраторов управления РАСШИРЕНным доступом.</span><span class="sxs-lookup"><span data-stu-id="8334e-104">In Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) configures domain-wide options and delegates permissions to Approvers, Editors, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="8334e-105">По умолчанию администратор РАСШИРЕНного управления правами — это отдельный пользователь с разрешениями "полный доступ" — все разрешения РАСШИРЕНного доступа, а также кто может выполнять задачи, связанные с какой-либо ролью.</span><span class="sxs-lookup"><span data-stu-id="8334e-105">By default, an AGPM Administrator is an individual with Full Control—all AGPM permissions—and who therefore can perform tasks associated with any role.</span></span>

<span data-ttu-id="8334e-106">В среде, в которой несколько пользователей разрабатывают объекты групповой политики (GPO), вы можете выбрать, будут ли все пользователи с РАСШИРЕНными разрешениями выполнять одни и те же задачи и иметь один и тот же уровень доступа, а также для тех, кто может делегировать им разрешения на доступ к редакторам, которые вносит изменения в объекты групповой политики и утверждающие, развертывающие объекты GPO</span><span class="sxs-lookup"><span data-stu-id="8334e-106">In an environment in which multiple people develop Group Policy Objects (GPOs), you can choose whether all AGPM users perform the same tasks and have the same level of access or whether AGPM Administrators delegate permissions to Editors who make changes to GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="8334e-107">Администраторы РАСШИРЕНного доступа к данным могут настраивать разрешения в соответствии с потребностями Организации.</span><span class="sxs-lookup"><span data-stu-id="8334e-107">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   <span data-ttu-id="8334e-108">[Настройка расширенного управления групповыми политиками](configuring-advanced-group-policy-management.md): Настройка соединения с сервером и уведомлений по электронной почте, передача доступа к объектам групповой политики в рабочей среде и Настройка ведения журнала и трассировки для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="8334e-108">[Configuring Advanced Group Policy Management](configuring-advanced-group-policy-management.md): Configure the AGPM Server Connection and e-mail notification, delegate access to GPOs in the production environment, and configure logging and tracing for troubleshooting.</span></span>

-   <span data-ttu-id="8334e-109">[Управление архивацией](managing-the-archive.md): передача доступа к объектам групповой политики в архиве и ограничение количества версий всех хранимых объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8334e-109">[Managing the Archive](managing-the-archive.md): Delegate access to GPOs in the archive and limit the number of versions of each GPO stored.</span></span>

-   <span data-ttu-id="8334e-110">[Управление службой расширенного управления групповыми политиками](managing-the-agpm-service-agpm30ops.md): Остановите и запустите службу управления групповыми политиками или измените путь к архиву, учетная запись службы расширенного управления групповыми политиками или порт, на котором прослушивается служба</span><span class="sxs-lookup"><span data-stu-id="8334e-110">[Managing the AGPM Service](managing-the-agpm-service-agpm30ops.md): Stop and start the AGPM Service or change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span>

-   <span data-ttu-id="8334e-111">[Перемещайте сервер и Архив с помощью расширенного шаблона обслуживания и архивации](move-the-agpm-server-and-the-archive.md). ПЕРЕМЕСТИТЕ службу расширенного (архивный) или и то, и другое, на другой сервер.</span><span class="sxs-lookup"><span data-stu-id="8334e-111">[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive.md): Move the AGPM Service, the archive, or both to a different server.</span></span>

<span data-ttu-id="8334e-112">Кроме того, так как роль администратора РАСШИРЕНного доступа включает разрешения для всех других ролей, администратор РАСШИРЕНного администрирования может выполнять задачи, которые обычно связаны с другими ролями.</span><span class="sxs-lookup"><span data-stu-id="8334e-112">Also, because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks normally associated with any other role.</span></span>

-   <span data-ttu-id="8334e-113">[Выполнение задач утверждающего](performing-approver-tasks-agpm30ops.md), таких как создание, развертывание и удаление GPO</span><span class="sxs-lookup"><span data-stu-id="8334e-113">[Performing Approver Tasks](performing-approver-tasks-agpm30ops.md), such as creating, deploying, or deleting GPOs</span></span>

-   <span data-ttu-id="8334e-114">[Выполнение задач редактора](performing-editor-tasks-agpm30ops.md), таких как редактирование, переименование, назначение подписей и импорт объектов групповой политики, создание шаблонов или Настройка шаблона по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8334e-114">[Performing Editor Tasks](performing-editor-tasks-agpm30ops.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

-   <span data-ttu-id="8334e-115">[Выполнение задач рецензента](performing-reviewer-tasks-agpm30ops.md), таких как проверка параметров и сравнение GPO</span><span class="sxs-lookup"><span data-stu-id="8334e-115">[Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md), such as reviewing settings and comparing GPOs</span></span>

### <span data-ttu-id="8334e-116">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="8334e-116">Additional considerations</span></span>

<span data-ttu-id="8334e-117">По умолчанию роль администратора расширенного управления групповыми политиками имеет полный доступ (все разрешения РАСШИРЕНного доступа к ним).</span><span class="sxs-lookup"><span data-stu-id="8334e-117">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="8334e-118">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="8334e-118">List Contents</span></span>

-   <span data-ttu-id="8334e-119">Чтение параметров</span><span class="sxs-lookup"><span data-stu-id="8334e-119">Read Settings</span></span>

-   <span data-ttu-id="8334e-120">Изменить параметры</span><span class="sxs-lookup"><span data-stu-id="8334e-120">Edit Settings</span></span>

-   <span data-ttu-id="8334e-121">Создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="8334e-121">Create GPO</span></span>

-   <span data-ttu-id="8334e-122">Развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="8334e-122">Deploy GPO</span></span>

-   <span data-ttu-id="8334e-123">Удаление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="8334e-123">Delete GPO</span></span>

-   <span data-ttu-id="8334e-124">Изменение параметров</span><span class="sxs-lookup"><span data-stu-id="8334e-124">Modify Options</span></span>

-   <span data-ttu-id="8334e-125">Изменение параметров безопасности</span><span class="sxs-lookup"><span data-stu-id="8334e-125">Modify Security</span></span>

-   <span data-ttu-id="8334e-126">Создание шаблона</span><span class="sxs-lookup"><span data-stu-id="8334e-126">Create Template</span></span>

<span data-ttu-id="8334e-127">**Параметры изменения** и **изменение разрешений безопасности** уникальны для роли администратора расширенного управления правами.</span><span class="sxs-lookup"><span data-stu-id="8334e-127">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





