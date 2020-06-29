---
title: Выполнение задач редактора
description: Выполнение задач редактора
author: dansimp
ms.assetid: 81976a01-2a95-4256-b703-9fb3c884ef34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8e23bb91d8762d19eed9ae817967ba5a57505a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820409"
---
# <span data-ttu-id="79f44-103">Выполнение задач редактора</span><span class="sxs-lookup"><span data-stu-id="79f44-103">Performing Editor Tasks</span></span>


<span data-ttu-id="79f44-104">В расширенном управлении групповыми политиками редактор — это человек, авторизованный администратором РАСШИРЕНного управления правами (полный доступ) для изменения объектов групповой политики (GPO) и создания шаблонов GPO.</span><span class="sxs-lookup"><span data-stu-id="79f44-104">In Advanced Group Policy Management (AGPM), an Editor is a person authorized by an AGPM Administrator (Full Control) to change Group Policy Objects (GPOs) and create GPO templates.</span></span> <span data-ttu-id="79f44-105">Кроме того, редактор может запросить создание, удаление или восстановление объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="79f44-105">Additionally, an Editor can request that a GPO be created, deleted, or restored.</span></span> <span data-ttu-id="79f44-106">Утверждающий должен утвердить запрос для реализации.</span><span class="sxs-lookup"><span data-stu-id="79f44-106">An Approver must approve the request for it to be implemented.</span></span> <span data-ttu-id="79f44-107">Редактор может экспортировать GPO в файл, чтобы его можно было скопировать в домен в другом лесе и импортировать объект групповой политики, скопированный из другого домена.</span><span class="sxs-lookup"><span data-stu-id="79f44-107">An Editor can export a GPO to a file so that it can be copied to a domain in another forest, and import a GPO that was copied from another domain.</span></span>

<span data-ttu-id="79f44-108">**Важно!**  Убедитесь в том, что вы подключаетесь к центральному архиву для GPO.</span><span class="sxs-lookup"><span data-stu-id="79f44-108">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="79f44-109">Дополнительные сведения можно найти в разделе [Настройка подключения к серверу расширенного конфигурирования](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="79f44-109">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

 

-   [<span data-ttu-id="79f44-110">Создание и администрирование объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="79f44-110">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

-   [<span data-ttu-id="79f44-111">Изменение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="79f44-111">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

-   [<span data-ttu-id="79f44-112">Использование тестовой среды</span><span class="sxs-lookup"><span data-stu-id="79f44-112">Using a Test Environment</span></span>](using-a-test-environment.md)

-   [<span data-ttu-id="79f44-113">Запрос на развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="79f44-113">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo-agpm40.md)

-   [<span data-ttu-id="79f44-114">Создание шаблона и настройка шаблона по умолчанию</span><span class="sxs-lookup"><span data-stu-id="79f44-114">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="79f44-115">Удаление и восстановление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="79f44-115">Deleting or Restoring a GPO</span></span>](deleting-or-restoring-a-gpo-agpm40.md)

<span data-ttu-id="79f44-116">**Примечание**  Так как роль редактора включает разрешения для роли рецензента, редактор также может просматривать параметры и сравнивать GPO.</span><span class="sxs-lookup"><span data-stu-id="79f44-116">**Note** Because the Editor role includes the permissions for the Reviewer role, an Editor can also review settings and compare GPOs.</span></span> <span data-ttu-id="79f44-117">Дополнительные сведения приведены в разделе [выполнение задач рецензента](performing-reviewer-tasks-agpm40.md) .</span><span class="sxs-lookup"><span data-stu-id="79f44-117">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md) for more information.</span></span>

 

### <span data-ttu-id="79f44-118">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="79f44-118">Additional considerations</span></span>

<span data-ttu-id="79f44-119">По умолчанию для роли редактора предоставляются следующие разрешения:</span><span class="sxs-lookup"><span data-stu-id="79f44-119">By default, the following permissions are provided for the Editor role:</span></span>

-   <span data-ttu-id="79f44-120">Содержимое списка</span><span class="sxs-lookup"><span data-stu-id="79f44-120">List Contents</span></span>

-   <span data-ttu-id="79f44-121">Чтение параметров</span><span class="sxs-lookup"><span data-stu-id="79f44-121">Read Settings</span></span>

-   <span data-ttu-id="79f44-122">Изменить параметры</span><span class="sxs-lookup"><span data-stu-id="79f44-122">Edit Settings</span></span>

-   <span data-ttu-id="79f44-123">Экспорт GPO</span><span class="sxs-lookup"><span data-stu-id="79f44-123">Export GPO</span></span>

-   <span data-ttu-id="79f44-124">Импорт объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="79f44-124">Import GPO</span></span>

-   <span data-ttu-id="79f44-125">Создание шаблона</span><span class="sxs-lookup"><span data-stu-id="79f44-125">Create Template</span></span>

 

 





