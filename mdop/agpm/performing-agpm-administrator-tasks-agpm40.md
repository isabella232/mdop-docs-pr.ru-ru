---
title: Выполнение задач администратора AGPM
description: Выполнение задач администратора AGPM
author: dansimp
ms.assetid: bc746f39-bdc9-4e2a-bc48-c3c7905de098
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 609b5b8b27fe24ff93e86bea7113929b1e04984d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822419"
---
# <span data-ttu-id="f68a2-103">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="f68a2-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="f68a2-104">Расширенное управление групповыми политиками позволяет администратору РАСШИРЕНного управления правами (полный доступ) настраивать параметры для всего домена и делегировать разрешения для утверждающих, редакторов, рецензентов и администраторов РАСШИРЕНного доступа.</span><span class="sxs-lookup"><span data-stu-id="f68a2-104">Advanced Group Policy Management (AGPM) lets an AGPM Administrator (Full Control) configure domain-wide options and delegate permissions to Approvers, Editors, Reviewers, and AGPM Administrators.</span></span> <span data-ttu-id="f68a2-105">По умолчанию администратор РАСШИРЕНного управления правами — это кто-то, у кого есть полный доступ (все разрешения РАСШИРЕНного доступа к данным) и который может выполнять задачи, связанные с какой-либо ролью.</span><span class="sxs-lookup"><span data-stu-id="f68a2-105">By default, an AGPM Administrator is someone who has Full Control— all AGPM permissions—and who therefore can perform tasks associated with any role.</span></span>

<span data-ttu-id="f68a2-106">В среде, в которой несколько пользователей разрабатывают объекты групповой политики (GPO), вы можете разрешить всем администраторам выполнять одни и те же задачи и иметь одинаковый уровень доступа.</span><span class="sxs-lookup"><span data-stu-id="f68a2-106">In an environment in which multiple people develop Group Policy Objects (GPOs), you can choose to let all Group Policy administrators perform the same tasks and have the same level of access.</span></span> <span data-ttu-id="f68a2-107">Кроме того, вы можете предоставить администраторам РАСШИРЕНных разрешений делегировать разрешения на доступ к редакторам, которые могут изменять GPO и утверждающие, развертывающие объекты групповой политики в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="f68a2-107">Or, you can choose to let AGPM Administrators delegate permissions to Editors who can change GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="f68a2-108">Администраторы РАСШИРЕНного доступа к данным могут настраивать разрешения в соответствии с потребностями Организации.</span><span class="sxs-lookup"><span data-stu-id="f68a2-108">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   <span data-ttu-id="f68a2-109">[Настройка расширенного управления групповыми политиками](configuring-advanced-group-policy-management-agpm40.md): Настройка соединения с сервером и уведомлений по электронной почте, передача доступа к объектам групповой политики в рабочей среде и Настройка ведения журнала и трассировки для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="f68a2-109">[Configuring Advanced Group Policy Management](configuring-advanced-group-policy-management-agpm40.md): Configure the AGPM Server Connection and e-mail notification, delegate access to GPOs in the production environment, and configure logging and tracing for troubleshooting.</span></span>

-   <span data-ttu-id="f68a2-110">[Управление архивацией](managing-the-archive-agpm40.md): передача доступа к GPO в архиве, ограничение количества версий каждого объекта групповой политики, Импорт объекта групповой политики из другого домена и резервное копирование и восстановление архива.</span><span class="sxs-lookup"><span data-stu-id="f68a2-110">[Managing the Archive](managing-the-archive-agpm40.md): Delegate access to GPOs in the archive, limit the number of versions of each GPO stored, import a GPO from another domain, and back up and restore the archive.</span></span>

-   <span data-ttu-id="f68a2-111">[Управление службой расширенного управления групповыми политиками](managing-the-agpm-service-agpm40.md): Остановите и запустите службу управления групповыми политиками или измените путь к архиву, учетная запись службы расширенного управления групповыми политиками или порт, на котором прослушивается служба</span><span class="sxs-lookup"><span data-stu-id="f68a2-111">[Managing the AGPM Service](managing-the-agpm-service-agpm40.md): Stop and start the AGPM Service or change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span>

-   <span data-ttu-id="f68a2-112">[Перемещайте сервер и Архив с помощью расширенного шаблона обслуживания и архивации](move-the-agpm-server-and-the-archive-agpm40.md). ПЕРЕМЕСТИТЕ службу расширенного (архивный) или и то, и другое, на другой сервер.</span><span class="sxs-lookup"><span data-stu-id="f68a2-112">[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md): Move the AGPM Service, the archive, or both to a different server.</span></span>

<span data-ttu-id="f68a2-113">**Примечание**  Так как роль администратора РАСШИРЕНного доступа содержит разрешения для всех других ролей, администратор РАСШИРЕНного администрирования может выполнять задачи, которые обычно связаны с другими ролями.</span><span class="sxs-lookup"><span data-stu-id="f68a2-113">**Note** Because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks usually associated with any other role.</span></span>

<span data-ttu-id="f68a2-114">[Выполнение задач утверждающего](performing-approver-tasks-agpm40.md), таких как создание, развертывание и удаление GPO</span><span class="sxs-lookup"><span data-stu-id="f68a2-114">[Performing Approver Tasks](performing-approver-tasks-agpm40.md), such as creating, deploying, or deleting GPOs</span></span>

<span data-ttu-id="f68a2-115">[Выполнение задач редактора](performing-editor-tasks-agpm40.md), таких как редактирование, переименование, назначение подписей и импорт объектов групповой политики, создание шаблонов или Настройка шаблона по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f68a2-115">[Performing Editor Tasks](performing-editor-tasks-agpm40.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

<span data-ttu-id="f68a2-116">[Выполнение задач рецензента](performing-reviewer-tasks-agpm40.md), таких как проверка параметров и сравнение GPO</span><span class="sxs-lookup"><span data-stu-id="f68a2-116">[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md), such as reviewing settings and comparing GPOs</span></span>

 

### <span data-ttu-id="f68a2-117">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="f68a2-117">Additional considerations</span></span>

<span data-ttu-id="f68a2-118">По умолчанию роль администратора расширенного управления групповыми политиками имеет полный доступ (все разрешения РАСШИРЕНного доступа к ним).</span><span class="sxs-lookup"><span data-stu-id="f68a2-118">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="f68a2-119">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="f68a2-119">List Contents</span></span>

-   <span data-ttu-id="f68a2-120">Чтение параметров</span><span class="sxs-lookup"><span data-stu-id="f68a2-120">Read Settings</span></span>

-   <span data-ttu-id="f68a2-121">Изменить параметры</span><span class="sxs-lookup"><span data-stu-id="f68a2-121">Edit Settings</span></span>

-   <span data-ttu-id="f68a2-122">Создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f68a2-122">Create GPO</span></span>

-   <span data-ttu-id="f68a2-123">Развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f68a2-123">Deploy GPO</span></span>

-   <span data-ttu-id="f68a2-124">Удаление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f68a2-124">Delete GPO</span></span>

-   <span data-ttu-id="f68a2-125">Экспорт GPO</span><span class="sxs-lookup"><span data-stu-id="f68a2-125">Export GPO</span></span>

-   <span data-ttu-id="f68a2-126">Импорт объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f68a2-126">Import GPO</span></span>

-   <span data-ttu-id="f68a2-127">Создание шаблона</span><span class="sxs-lookup"><span data-stu-id="f68a2-127">Create Template</span></span>

-   <span data-ttu-id="f68a2-128">Изменение параметров</span><span class="sxs-lookup"><span data-stu-id="f68a2-128">Modify Options</span></span>

-   <span data-ttu-id="f68a2-129">Изменение параметров безопасности</span><span class="sxs-lookup"><span data-stu-id="f68a2-129">Modify Security</span></span>

<span data-ttu-id="f68a2-130">**Параметры изменения** и **изменение разрешений безопасности** уникальны для роли администратора расширенного управления правами.</span><span class="sxs-lookup"><span data-stu-id="f68a2-130">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





