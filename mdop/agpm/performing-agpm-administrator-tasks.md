---
title: Выполнение задач администратора AGPM
description: Выполнение задач администратора AGPM
author: dansimp
ms.assetid: 32e694a7-be64-4943-bce2-2a3a15e5341f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0daa8df93a88ed155e9f894011d4dd835761948b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820479"
---
# <span data-ttu-id="a474f-103">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="a474f-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="a474f-104">Администратор расширенного управления групповыми политиками (полный доступ) настраивает параметры на уровне домена и делегирует разрешения для утверждающих, редакторов, рецензентов и других администраторов управления РАСШИРЕНным доступом.</span><span class="sxs-lookup"><span data-stu-id="a474f-104">An AGPM Administrator (Full Control) configures domain-wide options and delegates permissions to Approvers, Editors, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="a474f-105">По умолчанию Администратор расширенного управления групповыми политиками — это отдельный параметр с разрешениями "полный доступ" (все расширенные разрешения на Управление групповой политикой) и, следовательно, также может выполнять задачи, связанные с какой-либо ролью.</span><span class="sxs-lookup"><span data-stu-id="a474f-105">By default, an AGPM Administrator is an individual with Full Control (all Advanced Group Policy Management \[AGPM\] permissions) and therefore can also perform tasks associated with any role.</span></span>

<span data-ttu-id="a474f-106">В среде, в которой несколько пользователей разрабатывают объекты групповой политики (GPO), вы можете выбрать, будут ли все пользователи с расширенным управлением групповой политикой (ГРУППОВыми политиками) выполнять одни и те же задачи и иметь тот же уровень доступа, а также администраторы, которые могут делегировать им разрешения на доступ к редакторам, которые вносятся в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="a474f-106">In an environment in which multiple people develop Group Policy objects (GPOs), you can choose whether all Advanced Group Policy Management (AGPM) users perform the same tasks and have the same level of access or whether AGPM Administrators delegate permissions to Editors who make changes to GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="a474f-107">Администраторы РАСШИРЕНного доступа к данным могут настраивать разрешения в соответствии с потребностями Организации.</span><span class="sxs-lookup"><span data-stu-id="a474f-107">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   [<span data-ttu-id="a474f-108">Настройка подключения к серверу AGPM</span><span class="sxs-lookup"><span data-stu-id="a474f-108">Configure the AGPM Server Connection</span></span>](configure-the-agpm-server-connection.md)

-   [<span data-ttu-id="a474f-109">Настройка уведомлений по электронной почте</span><span class="sxs-lookup"><span data-stu-id="a474f-109">Configure E-Mail Notification</span></span>](configure-e-mail-notification.md)

-   [<span data-ttu-id="a474f-110">Предоставление доступа на уровне домена</span><span class="sxs-lookup"><span data-stu-id="a474f-110">Delegate Domain-Level Access</span></span>](delegate-domain-level-access.md)

-   [<span data-ttu-id="a474f-111">Передача прав доступа к отдельному объекту групповой политики</span><span class="sxs-lookup"><span data-stu-id="a474f-111">Delegate Access to an Individual GPO</span></span>](delegate-access-to-an-individual-gpo.md)

-   [<span data-ttu-id="a474f-112">Настройка ведения журнала и трассировки</span><span class="sxs-lookup"><span data-stu-id="a474f-112">Configure Logging and Tracing</span></span>](configure-logging-and-tracing.md)

-   [<span data-ttu-id="a474f-113">Управление службой AGPM</span><span class="sxs-lookup"><span data-stu-id="a474f-113">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

    -   [<span data-ttu-id="a474f-114">Запуск и остановка службы AGPM</span><span class="sxs-lookup"><span data-stu-id="a474f-114">Start and Stop the AGPM Service</span></span>](start-and-stop-the-agpm-service.md)

    -   [<span data-ttu-id="a474f-115">Изменение пути к архиву</span><span class="sxs-lookup"><span data-stu-id="a474f-115">Modify the Archive Path</span></span>](modify-the-archive-path.md)

    -   [<span data-ttu-id="a474f-116">Изменение учетной записи службы AGPM</span><span class="sxs-lookup"><span data-stu-id="a474f-116">Modify the AGPM Service Account</span></span>](modify-the-agpm-service-account.md)

    -   [<span data-ttu-id="a474f-117">Изменения порта, который прослушивает служба AGPM</span><span class="sxs-lookup"><span data-stu-id="a474f-117">Modify the Port on Which the AGPM Service Listens</span></span>](modify-the-port-on-which-the-agpm-service-listens.md)

<span data-ttu-id="a474f-118">Кроме того, так как роль администратора РАСШИРЕНного доступа включает разрешения для всех других ролей, администратор РАСШИРЕНного администрирования может выполнять задачи, которые обычно связаны с другими ролями.</span><span class="sxs-lookup"><span data-stu-id="a474f-118">Also, because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks normally associated with any other role.</span></span>

-   <span data-ttu-id="a474f-119">[Выполнение задач утверждающего](performing-approver-tasks.md), таких как создание, развертывание и удаление GPO</span><span class="sxs-lookup"><span data-stu-id="a474f-119">[Performing Approver Tasks](performing-approver-tasks.md), such as creating, deploying, or deleting GPOs</span></span>

-   <span data-ttu-id="a474f-120">[Выполнение задач редактора](performing-editor-tasks.md), таких как редактирование, переименование, назначение подписей и импорт объектов групповой политики, создание шаблонов или Настройка шаблона по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a474f-120">[Performing Editor Tasks](performing-editor-tasks.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

-   <span data-ttu-id="a474f-121">[Выполнение задач рецензента](performing-reviewer-tasks.md), таких как проверка параметров и сравнение GPO</span><span class="sxs-lookup"><span data-stu-id="a474f-121">[Performing Reviewer Tasks](performing-reviewer-tasks.md), such as reviewing settings and comparing GPOs</span></span>

### <span data-ttu-id="a474f-122">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="a474f-122">Additional considerations</span></span>

<span data-ttu-id="a474f-123">По умолчанию роль администратора расширенного управления групповыми политиками имеет полный доступ (все разрешения РАСШИРЕНного доступа к ним).</span><span class="sxs-lookup"><span data-stu-id="a474f-123">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="a474f-124">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="a474f-124">List Contents</span></span>

-   <span data-ttu-id="a474f-125">Чтение параметров</span><span class="sxs-lookup"><span data-stu-id="a474f-125">Read Settings</span></span>

-   <span data-ttu-id="a474f-126">Изменить параметры</span><span class="sxs-lookup"><span data-stu-id="a474f-126">Edit Settings</span></span>

-   <span data-ttu-id="a474f-127">Создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="a474f-127">Create GPO</span></span>

-   <span data-ttu-id="a474f-128">Развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="a474f-128">Deploy GPO</span></span>

-   <span data-ttu-id="a474f-129">Удаление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="a474f-129">Delete GPO</span></span>

-   <span data-ttu-id="a474f-130">Изменение параметров</span><span class="sxs-lookup"><span data-stu-id="a474f-130">Modify Options</span></span>

-   <span data-ttu-id="a474f-131">Изменение параметров безопасности</span><span class="sxs-lookup"><span data-stu-id="a474f-131">Modify Security</span></span>

-   <span data-ttu-id="a474f-132">Создание шаблона</span><span class="sxs-lookup"><span data-stu-id="a474f-132">Create Template</span></span>

<span data-ttu-id="a474f-133">**Параметры изменения** и **изменение разрешений безопасности** уникальны для роли администратора расширенного управления правами.</span><span class="sxs-lookup"><span data-stu-id="a474f-133">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





