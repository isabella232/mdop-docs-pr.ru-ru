---
title: Запрос на удаление объекта групповой политики
description: Запрос на удаление объекта групповой политики
author: dansimp
ms.assetid: 576ece5c-dc6d-4b5e-8628-01c15ae2c9a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87368d9f132d1ef7dc6a70fffa0611d33a23aa78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818442"
---
# <span data-ttu-id="1c62e-103">Запрос на удаление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="1c62e-103">Request Deletion of a GPO</span></span>


<span data-ttu-id="1c62e-104">Если вы не являетесь утверждающим или администратором РАСШИРЕНного управления правами (полный доступ), необходимо запросить удаление объекта групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="1c62e-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the deletion of a Group Policy Object (GPO).</span></span>

<span data-ttu-id="1c62e-105">Для выполнения этой процедуры требуется учетная запись пользователя с ролью "редактор" или необходимыми разрешениями в расширенном управлении групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="1c62e-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="1c62e-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="1c62e-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="1c62e-107">Запрос удаления управляемого объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="1c62e-107">To request the deletion of a controlled GPO</span></span>**

1.  <span data-ttu-id="1c62e-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1c62e-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="1c62e-109">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1c62e-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="1c62e-110">Щелкните правой кнопкой мыши объект групповой политики, который вы хотите удалить, и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="1c62e-110">Right-click the GPO you want to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="1c62e-111">Чтобы удалить GPO из архива, не открывая внедренный объект, не находясь в рабочей среде, выберите команду **Удалить GPO из архива**.</span><span class="sxs-lookup"><span data-stu-id="1c62e-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only**.</span></span>

    -   <span data-ttu-id="1c62e-112">Чтобы удалить GPO из архивной и производственной сред, выберите команду **удалить объект групповой политики из архива и из рабочей**среды.</span><span class="sxs-lookup"><span data-stu-id="1c62e-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="1c62e-113">Если у вас нет специального разрешения на удаление объектов групповой политики, необходимо отправить запрос на удаление развернутого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1c62e-113">Unless you have special permission to delete GPOs, you must submit a request for deletion of the deployed GPO.</span></span> <span data-ttu-id="1c62e-114">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="1c62e-114">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="1c62e-115">Введите Примечание, которое будет отображаться в контрольной записи для объекта групповой политики, и нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="1c62e-115">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="1c62e-116">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="1c62e-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="1c62e-117">Объект групповой политики отображается в списке объектов групповой политики на вкладке **ожидающие** . Когда утверждающий утвердил ваш запрос, объект GPO будет перемещен с вкладки " **ожидающие** " на вкладку " **Корзина** ", где ее можно восстановить или уничтожить.</span><span class="sxs-lookup"><span data-stu-id="1c62e-117">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

### <span data-ttu-id="1c62e-118">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="1c62e-118">Additional considerations</span></span>

-   <span data-ttu-id="1c62e-119">Для выполнения этой процедуры необходимо быть редактором по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c62e-119">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="1c62e-120">В частности, необходимо иметь **содержимое списка** и разрешения на **изменение параметров** для GPO.</span><span class="sxs-lookup"><span data-stu-id="1c62e-120">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="1c62e-121">Чтобы отменить запрос перед его утверждением, откройте вкладку **Ожидание** . Щелкните объект групповой политики правой кнопкой мыши и выберите команду **снять**.</span><span class="sxs-lookup"><span data-stu-id="1c62e-121">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="1c62e-122">Объект групповой политики будет возвращен на вкладку " **управляемые** ".</span><span class="sxs-lookup"><span data-stu-id="1c62e-122">The GPO will be returned to the **Controlled** tab.</span></span>

-   <span data-ttu-id="1c62e-123">Чтобы удалить неуправляемый объект групповой политики из производственной среды, не открывая его сначала, в **консоли управления групповыми политиками**нажмите кнопку **лес**, выберите \*\* &lt; пункт &gt; \*\* **домены**, а затем — пункт **объекты групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="1c62e-123">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="1c62e-124">Щелкните ненужный объект групповой политики правой кнопкой мыши и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="1c62e-124">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="1c62e-125">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="1c62e-125">Additional references</span></span>

-   [<span data-ttu-id="1c62e-126">Выполнение задач редактора</span><span class="sxs-lookup"><span data-stu-id="1c62e-126">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

 

 





