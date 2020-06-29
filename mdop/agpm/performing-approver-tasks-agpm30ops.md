---
title: Выполнение задач утверждающего
description: Выполнение задач утверждающего
author: dansimp
ms.assetid: 9f711824-191b-4b4b-a1c6-a3b2116006a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8e4a848608a3be1dbb0632f0145b4fc1d1bc631
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820472"
---
# <span data-ttu-id="33460-103">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="33460-103">Performing Approver Tasks</span></span>


<span data-ttu-id="33460-104">Утверждающее лицо — это человек, уполномоченный администратору управления ГРУППОВыми политиками (полный доступ) для создания, развертывания и удаления объектов групповой политики (GPO), а также для утверждения или отклонения запросов (обычно из редакторов) для создания, развертывания и удаления GPO.</span><span class="sxs-lookup"><span data-stu-id="33460-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy Objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="33460-105">**Важно!**  Убедитесь в том, что вы подключаетесь к центральному архиву для GPO.</span><span class="sxs-lookup"><span data-stu-id="33460-105">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="33460-106">Дополнительные сведения можно найти в разделе [Настройка подключения к серверу расширенного конфигурирования](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="33460-106">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span></span>

 

-   [<span data-ttu-id="33460-107">Утверждение или отклонение ожидающего действия</span><span class="sxs-lookup"><span data-stu-id="33460-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action-agpm30ops.md)

-   [<span data-ttu-id="33460-108">Создание, администрирование и импорт объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="33460-108">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

-   [<span data-ttu-id="33460-109">Регистрация объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="33460-109">Check In a GPO</span></span>](check-in-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="33460-110">Развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="33460-110">Deploy a GPO</span></span>](deploy-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="33460-111">Откат к предыдущей версии объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="33460-111">Roll Back to a Previous Version of a GPO</span></span>](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="33460-112">Удаление, восстановление и уничтожение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="33460-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

<span data-ttu-id="33460-113">**Примечание**  Перед утверждением объекта групповой политики утверждающий должен просмотреть содержащиеся в нем параметры политики.</span><span class="sxs-lookup"><span data-stu-id="33460-113">**Note** Before approving a GPO, an Approver should review the policy settings that it contains.</span></span> <span data-ttu-id="33460-114">Роль утверждающего включает разрешения для роли рецензента, чтобы утверждающий мог просматривать параметры политики и сравнивать объекты GPO.</span><span class="sxs-lookup"><span data-stu-id="33460-114">The Approver role includes the permissions for the Reviewer role, so that an Approver can review policy settings and compare GPOs.</span></span> <span data-ttu-id="33460-115">Дополнительные сведения приведены в разделе [выполнение задач рецензента](performing-reviewer-tasks-agpm30ops.md) .</span><span class="sxs-lookup"><span data-stu-id="33460-115">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md) for more information.</span></span>

 

### <span data-ttu-id="33460-116">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="33460-116">Additional considerations</span></span>

<span data-ttu-id="33460-117">По умолчанию для роли утверждающего предоставляются следующие разрешения:</span><span class="sxs-lookup"><span data-stu-id="33460-117">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="33460-118">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="33460-118">List Contents</span></span>

-   <span data-ttu-id="33460-119">Чтение параметров</span><span class="sxs-lookup"><span data-stu-id="33460-119">Read Settings</span></span>

-   <span data-ttu-id="33460-120">Создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="33460-120">Create GPO</span></span>

-   <span data-ttu-id="33460-121">Развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="33460-121">Deploy GPO</span></span>

-   <span data-ttu-id="33460-122">Удаление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="33460-122">Delete GPO</span></span>

<span data-ttu-id="33460-123">Кроме того, утверждающий имеет полный контроль над объектами групповой политики, которые он создал или управлял.</span><span class="sxs-lookup"><span data-stu-id="33460-123">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 





