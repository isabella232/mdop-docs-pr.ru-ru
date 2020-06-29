---
title: Выполнение задач утверждающего
description: Выполнение задач утверждающего
author: dansimp
ms.assetid: e0a4b7fe-ce69-4755-9104-c7f523ea6b62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a0815bdd6c34a7a23b27075b3b5367757c1f84e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820469"
---
# <span data-ttu-id="7526d-103">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="7526d-103">Performing Approver Tasks</span></span>


<span data-ttu-id="7526d-104">Утверждающее лицо — это человек, уполномоченный администратору управления ГРУППОВыми политиками (полный доступ) для создания, развертывания и удаления объектов групповой политики (GPO), а также для утверждения или отклонения запросов (обычно из редакторов) для создания, развертывания и удаления GPO.</span><span class="sxs-lookup"><span data-stu-id="7526d-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy Objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="7526d-105">**Важно!**  Убедитесь в том, что вы подключаетесь к центральному архиву для GPO.</span><span class="sxs-lookup"><span data-stu-id="7526d-105">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="7526d-106">Дополнительные сведения можно найти в разделе [Настройка подключения к серверу расширенного конфигурирования](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="7526d-106">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

 

-   [<span data-ttu-id="7526d-107">Утверждение или отклонение ожидающего действия</span><span class="sxs-lookup"><span data-stu-id="7526d-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action-agpm40.md)

-   [<span data-ttu-id="7526d-108">Создание и администрирование объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="7526d-108">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-app.md)

-   [<span data-ttu-id="7526d-109">Регистрация объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="7526d-109">Check In a GPO</span></span>](check-in-a-gpo-agpm40.md)

-   [<span data-ttu-id="7526d-110">Развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="7526d-110">Deploy a GPO</span></span>](deploy-a-gpo-agpm40.md)

-   [<span data-ttu-id="7526d-111">Откат до более ранней версии объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="7526d-111">Roll Back to an Earlier Version of a GPO</span></span>](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md)

-   [<span data-ttu-id="7526d-112">Удаление, восстановление и уничтожение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="7526d-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm40.md)

<span data-ttu-id="7526d-113">**Примечание**  Перед утверждением объекта групповой политики утверждающий должен просмотреть содержащиеся в нем параметры политики.</span><span class="sxs-lookup"><span data-stu-id="7526d-113">**Note** Before approving a GPO, an Approver should review the policy settings that it contains.</span></span> <span data-ttu-id="7526d-114">Роль утверждающего включает разрешения для роли рецензента, чтобы утверждающий мог просматривать параметры политики и сравнивать объекты GPO.</span><span class="sxs-lookup"><span data-stu-id="7526d-114">The Approver role includes the permissions for the Reviewer role, so that an Approver can review policy settings and compare GPOs.</span></span> <span data-ttu-id="7526d-115">Дополнительные сведения приведены в разделе [выполнение задач рецензента](performing-reviewer-tasks-agpm40.md) .</span><span class="sxs-lookup"><span data-stu-id="7526d-115">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md) for more information.</span></span>

 

### <span data-ttu-id="7526d-116">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="7526d-116">Additional considerations</span></span>

<span data-ttu-id="7526d-117">По умолчанию для роли утверждающего предоставляются следующие разрешения:</span><span class="sxs-lookup"><span data-stu-id="7526d-117">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="7526d-118">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="7526d-118">List Contents</span></span>

-   <span data-ttu-id="7526d-119">Чтение параметров</span><span class="sxs-lookup"><span data-stu-id="7526d-119">Read Settings</span></span>

-   <span data-ttu-id="7526d-120">Создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="7526d-120">Create GPO</span></span>

-   <span data-ttu-id="7526d-121">Развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="7526d-121">Deploy GPO</span></span>

-   <span data-ttu-id="7526d-122">Удаление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="7526d-122">Delete GPO</span></span>

<span data-ttu-id="7526d-123">Кроме того, утверждающий имеет полный контроль над объектами групповой политики, которые он создал или управлял.</span><span class="sxs-lookup"><span data-stu-id="7526d-123">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 





