---
title: Удаление объекта групповой политики
description: Удаление объекта групповой политики
author: dansimp
ms.assetid: 66be3dde-653e-4c25-8cb7-00e7090c8d31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c27ddf87a12ed6010c481d93bfc85bb531f3d4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820972"
---
# <span data-ttu-id="7c4e6-103">Удаление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="7c4e6-103">Delete a GPO</span></span>


<span data-ttu-id="7c4e6-104">Возможно, у вас нет разрешения на завершение удаления объекта групповой политики (GPO), но у вас есть разрешение, необходимое для начала процесса и отправки запроса утверждающему лицу.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-104">As an Editor, you may not have permission to complete the deletion of a Group Policy object (GPO), but you do have the permission necessary to begin the process and submit your request to an Approver.</span></span>

<span data-ttu-id="7c4e6-105">Для выполнения этой процедуры требуется учетная запись пользователя с ролью "редактор" или необходимыми разрешениями для расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="7c4e6-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="7c4e6-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="7c4e6-107">Запрос удаления управляемого объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="7c4e6-107">To request the deletion of a controlled GPO</span></span>**

1.  <span data-ttu-id="7c4e6-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="7c4e6-109">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="7c4e6-110">Щелкните правой кнопкой мыши удаляемый объект групповой политики, а затем выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-110">Right-click the GPO to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="7c4e6-111">Чтобы удалить GPO из архива, не открывая внедренный объект, не находясь в рабочей среде, выберите команду **Удалить GPO только из архива (без контроля)**.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only (uncontrol)**.</span></span>

    -   <span data-ttu-id="7c4e6-112">Чтобы удалить GPO из архивной и производственной сред, выберите команду **удалить объект групповой политики из архива и из рабочей**среды.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

        <span data-ttu-id="7c4e6-113">Если у вас нет специального разрешения на удаление объектов групповой политики, необходимо отправить запрос на удаление развернутого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-113">Unless you have special permission to delete GPOs, you must submit a request for deletion of the deployed GPO.</span></span> <span data-ttu-id="7c4e6-114">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="7c4e6-114">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="7c4e6-115">Введите Примечание, которое будет отображаться в контрольной записи для объекта групповой политики, и нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-115">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

4.  <span data-ttu-id="7c4e6-116">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7c4e6-117">Объект групповой политики отображается в списке объектов групповой политики на вкладке **ожидающие** . Когда утверждающий утвердил ваш запрос, объект GPO будет перемещен с вкладки " **ожидающие** " на вкладку " **Корзина** ", где ее можно восстановить или уничтожить.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-117">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

### <span data-ttu-id="7c4e6-118">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="7c4e6-118">Additional considerations</span></span>

-   <span data-ttu-id="7c4e6-119">По умолчанию вы должны быть редактором для запроса удаления развернутого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-119">By default, you must be an Editor to request the deletion of a deployed GPO.</span></span> <span data-ttu-id="7c4e6-120">В частности, необходимо иметь **содержимое списка** и разрешения на **изменение параметров** для GPO.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-120">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="7c4e6-121">По умолчанию для удаления GPO из архива вы должны быть редактором, утверждающим или администратором РАСШИРЕНного доступа (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="7c4e6-121">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to delete a GPO from the archive.</span></span> <span data-ttu-id="7c4e6-122">В частности, необходимо иметь **содержимое списка** и либо **изменить параметры** , либо **удалить разрешения GPO** для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-122">Specifically, you must have **List Contents** and either **Edit Settings** or **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="7c4e6-123">Чтобы отменить запрос перед его утверждением, откройте вкладку **Ожидание** . Щелкните объект групповой политики правой кнопкой мыши и выберите команду **снять**.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-123">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="7c4e6-124">Объект групповой политики будет возвращен на вкладку " **управляемые** ".</span><span class="sxs-lookup"><span data-stu-id="7c4e6-124">The GPO will be returned to the **Controlled** tab.</span></span>

-   <span data-ttu-id="7c4e6-125">Чтобы удалить неуправляемый объект групповой политики из производственной среды, не открывая его сначала, в **консоли управления групповыми политиками**нажмите кнопку **лес**, выберите \*\* &lt; пункт &gt; \*\* **домены**, а затем — пункт **объекты групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-125">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="7c4e6-126">Щелкните ненужный объект групповой политики правой кнопкой мыши и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-126">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="7c4e6-127">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="7c4e6-127">Additional references</span></span>

-   [<span data-ttu-id="7c4e6-128">Выполнение задач редактора</span><span class="sxs-lookup"><span data-stu-id="7c4e6-128">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

 

 





