---
title: Выполнение задач утверждающего
description: Выполнение задач утверждающего
author: dansimp
ms.assetid: 6f6310b3-19c1-47c9-8615-964ddd10ce14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fc77a1dd9a3d54e637ae4baeb452d327672ed250
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820429"
---
# <span data-ttu-id="f41ad-103">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="f41ad-103">Performing Approver Tasks</span></span>


<span data-ttu-id="f41ad-104">Утверждающее лицо — это человек, уполномоченный администратору управления ГРУППОВыми политиками (полный доступ) для создания, развертывания и удаления объектов групповой политики (GPO), а также для утверждения или отклонения запросов (обычно из редакторов) для создания, развертывания и удаления GPO.</span><span class="sxs-lookup"><span data-stu-id="f41ad-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="f41ad-105">**Важно!**  Убедитесь в том, что вы подключаетесь к центральному архиву для GPO.</span><span class="sxs-lookup"><span data-stu-id="f41ad-105">**Important** Ensure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="f41ad-106">Дополнительные сведения можно найти [в разделе Настройка подключения к серверу расширенного конфигурирования](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="f41ad-106">For more information, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

 

-   [<span data-ttu-id="f41ad-107">Утверждение или отклонение ожидающего действия</span><span class="sxs-lookup"><span data-stu-id="f41ad-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action.md)

-   [<span data-ttu-id="f41ad-108">Создание, администрирование и импорт объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f41ad-108">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

-   [<span data-ttu-id="f41ad-109">Регистрация объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f41ad-109">Check In a GPO</span></span>](check-in-a-gpo-approver.md)

-   [<span data-ttu-id="f41ad-110">Развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f41ad-110">Deploy a GPO</span></span>](deploy-a-gpo.md)

-   [<span data-ttu-id="f41ad-111">Откат к предыдущей версии объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f41ad-111">Roll Back to a Previous Version of a GPO</span></span>](roll-back-to-a-previous-version-of-a-gpo.md)

-   [<span data-ttu-id="f41ad-112">Удаление, восстановление и уничтожение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f41ad-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

<span data-ttu-id="f41ad-113">**Примечание**  Так как роль утверждающего включает разрешения для роли рецензента, утверждающий также может просматривать параметры и сравнивать GPO.</span><span class="sxs-lookup"><span data-stu-id="f41ad-113">**Note** Because the Approver role includes the permissions for the Reviewer role, an Approver can also review settings and compare GPOs.</span></span> <span data-ttu-id="f41ad-114">Дополнительные сведения приведены в разделе [выполнение задач рецензента](performing-reviewer-tasks.md) .</span><span class="sxs-lookup"><span data-stu-id="f41ad-114">See [Performing Reviewer Tasks](performing-reviewer-tasks.md) for more information.</span></span>

 

### <span data-ttu-id="f41ad-115">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="f41ad-115">Additional considerations</span></span>

<span data-ttu-id="f41ad-116">По умолчанию для роли утверждающего предоставляются следующие разрешения:</span><span class="sxs-lookup"><span data-stu-id="f41ad-116">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="f41ad-117">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="f41ad-117">List Contents</span></span>

-   <span data-ttu-id="f41ad-118">Чтение параметров</span><span class="sxs-lookup"><span data-stu-id="f41ad-118">Read Settings</span></span>

-   <span data-ttu-id="f41ad-119">Создание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f41ad-119">Create GPO</span></span>

-   <span data-ttu-id="f41ad-120">Развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f41ad-120">Deploy GPO</span></span>

-   <span data-ttu-id="f41ad-121">Удаление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f41ad-121">Delete GPO</span></span>

<span data-ttu-id="f41ad-122">Кроме того, утверждающий имеет полный контроль над объектами групповой политики, которые он создал или управлял.</span><span class="sxs-lookup"><span data-stu-id="f41ad-122">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 





