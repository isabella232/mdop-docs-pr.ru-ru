---
title: Удаление объекта групповой политики
description: Удаление объекта групповой политики
author: dansimp
ms.assetid: 85fca371-5707-49c1-aa51-813fc3a58dfc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a6419943604ee5a76d305228bb7418a8525bf33
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820982"
---
# <span data-ttu-id="f686e-103">Удаление объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f686e-103">Delete a GPO</span></span>


<span data-ttu-id="f686e-104">С помощью расширенного управления групповыми политиками утверждающие удаляют управляемый объект групповой политики (GPO), перемещая его в корзину.</span><span class="sxs-lookup"><span data-stu-id="f686e-104">Advanced Group Policy Management (AGPM) enables Approvers to delete a controlled Group Policy object (GPO), moving it to the Recycle Bin.</span></span>

<span data-ttu-id="f686e-105">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора (полного доступа) утверждающего или расширенного управления групповыми политиками или необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="f686e-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="f686e-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="f686e-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="f686e-107">Удаление управляемого объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f686e-107">To delete a controlled GPO</span></span>**

1.  <span data-ttu-id="f686e-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="f686e-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="f686e-109">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="f686e-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="f686e-110">Щелкните правой кнопкой мыши удаляемый объект групповой политики, а затем выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="f686e-110">Right-click the GPO to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="f686e-111">Чтобы удалить GPO из архива, не открывая внедренный объект, не находясь в рабочей среде, выберите команду **Удалить GPO только из архива (без контроля)**.</span><span class="sxs-lookup"><span data-stu-id="f686e-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only (uncontrol)**.</span></span>

    -   <span data-ttu-id="f686e-112">Чтобы удалить GPO из архивной и производственной сред, выберите команду **удалить объект групповой политики из архива и из рабочей**среды.</span><span class="sxs-lookup"><span data-stu-id="f686e-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="f686e-113">Введите Примечание, которое будет отображаться в контрольной записи для объекта групповой политики, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f686e-113">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="f686e-114">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="f686e-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f686e-115">Объект групповой политики удаляется с вкладки " **управляемые** " и отображается на вкладке " **Корзина** ", в которой ее можно восстановить или уничтожить.</span><span class="sxs-lookup"><span data-stu-id="f686e-115">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span> <span data-ttu-id="f686e-116">Если объект групповой политики был удален только из архива, он также отображается на вкладке **неуправление** .</span><span class="sxs-lookup"><span data-stu-id="f686e-116">If the GPO was deleted only from the archive, it is also displayed on the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="f686e-117">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="f686e-117">Additional considerations</span></span>

-   <span data-ttu-id="f686e-118">По умолчанию для удаления развернутого объекта групповой политики необходимо быть утверждающим или администратором РАСШИРЕНного доступа к сети (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="f686e-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to delete a deployed GPO.</span></span> <span data-ttu-id="f686e-119">В частности, необходимо иметь **содержимое списка** и **удалить разрешения GPO** для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="f686e-119">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="f686e-120">По умолчанию для удаления GPO из архива вы должны быть редактором, утверждающим или администратором РАСШИРЕНного доступа (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="f686e-120">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to delete a GPO from the archive.</span></span> <span data-ttu-id="f686e-121">В частности, необходимо иметь **содержимое списка** и либо **изменить параметры** , либо **удалить разрешения GPO** для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="f686e-121">Specifically, you must have **List Contents** and either **Edit Settings** or **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="f686e-122">Чтобы удалить неуправляемый объект групповой политики из производственной среды, не открывая его сначала, в **консоли управления групповыми политиками**нажмите кнопку **лес**, выберите \*\* &lt; пункт &gt; \*\* **домены**, а затем — пункт **объекты групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="f686e-122">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="f686e-123">Щелкните ненужный объект групповой политики правой кнопкой мыши и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="f686e-123">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="f686e-124">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="f686e-124">Additional references</span></span>

-   [<span data-ttu-id="f686e-125">Удаление, восстановление и уничтожение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="f686e-125">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 





