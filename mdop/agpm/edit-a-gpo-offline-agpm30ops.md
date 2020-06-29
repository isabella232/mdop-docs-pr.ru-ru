---
title: Изменение объекта групповой политики в автономном режиме
description: Изменение объекта групповой политики в автономном режиме
author: dansimp
ms.assetid: 51677d8a-6209-41b5-82ed-4f3be817abc0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74b6ae9fdf11456a9a45cb5504ed97a9bc6aecb4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818622"
---
# <span data-ttu-id="9eade-103">Изменение объекта групповой политики в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="9eade-103">Edit a GPO Offline</span></span>


<span data-ttu-id="9eade-104">Чтобы внести изменения в контролируемый объект групповой политики (GPO), необходимо сначала извлечь копию GPO из архива.</span><span class="sxs-lookup"><span data-stu-id="9eade-104">To make changes to a controlled Group Policy Object (GPO), you must first check out a copy of the GPO from the archive.</span></span> <span data-ttu-id="9eade-105">Никто другой не сможет изменить объект групповой политики, пока он не будет возвращен повторно, что предотвращает появление конфликтующих изменений несколькими администраторами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9eade-105">No one else will be able to modify the GPO until it is checked in again, preventing the introduction of conflicting changes by multiple Group Policy administrators.</span></span> <span data-ttu-id="9eade-106">Завершив изменение объекта групповой политики, вы можете вернуть его в архив, чтобы его можно было просмотреть и развернуть в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="9eade-106">When you have finished modifying the GPO, you check it into the archive so that it can be reviewed and deployed to the production environment.</span></span>

<span data-ttu-id="9eade-107">Для выполнения этой процедуры требуется учетная запись пользователя с ролью редактора или администратора управления групповыми политиками (полного доступа), учетной записи пользователя утверждающего, создавшего GPO, или учетной записи пользователя с необходимыми разрешениями для расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="9eade-107">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="9eade-108">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="9eade-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="9eade-109">Изменение объекта групповой политики в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="9eade-109">Editing a GPO offline</span></span>


<span data-ttu-id="9eade-110">Чтобы изменить объект групповой политики, нужно извлечь его из архива, изменить его в автономном режиме, а затем вернуть его в архив, чтобы его можно было просматривать и развертывать (или изменять другими редакторами).</span><span class="sxs-lookup"><span data-stu-id="9eade-110">To edit a GPO, you check out the GPO from the archive, edit the GPO offline, and then check the GPO into the archive so that it can be reviewed and deployed (or modified by other Editors).</span></span>

-   [<span data-ttu-id="9eade-111">Извлечение объекта групповой политики из архива для редактирования</span><span class="sxs-lookup"><span data-stu-id="9eade-111">Check out a GPO from the archive for editing</span></span>](#bkmk-checkout)

-   [<span data-ttu-id="9eade-112">Изменение объекта групповой политики в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="9eade-112">Edit a GPO offline</span></span>](#bkmk-edit)

-   [<span data-ttu-id="9eade-113">Проверка объекта групповой политики в архиве</span><span class="sxs-lookup"><span data-stu-id="9eade-113">Check a GPO into the archive</span></span>](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**<span data-ttu-id="9eade-114">Извлечение объекта групповой политики из архива для редактирования</span><span class="sxs-lookup"><span data-stu-id="9eade-114">To check out a GPO from the archive for editing</span></span>**

1.  <span data-ttu-id="9eade-115">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9eade-115">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="9eade-116">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9eade-116">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="9eade-117">Щелкните правой кнопкой мыши объект групповой политики, который нужно изменить, и **выберите пункт извлечь**.</span><span class="sxs-lookup"><span data-stu-id="9eade-117">Right-click the GPO to be edited, and then click **Check Out**.</span></span>

4.  <span data-ttu-id="9eade-118">Введите Примечание, которое будет отображаться в истории объекта групповой политики, когда он извлечен, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9eade-118">Type a comment to be displayed in the History of the GPO while it is checked out, and then click **OK**.</span></span>

5.  <span data-ttu-id="9eade-119">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9eade-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9eade-120">На вкладке **Управление** состоянием объекта групповой политики теперь вычислено " **извлечено**".</span><span class="sxs-lookup"><span data-stu-id="9eade-120">On the **Controlled** tab, the state of the GPO is now identified as **Checked Out**.</span></span>

### <a href="" id="bkmk-edit"></a>

**<span data-ttu-id="9eade-121">Изменение объекта групповой политики в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="9eade-121">To edit a GPO offline</span></span>**

1.  <span data-ttu-id="9eade-122">На вкладке **Управление** , щелкните правой кнопкой мыши объект групповой политики, который нужно изменить, и выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="9eade-122">On the **Controlled** tab, right-click the GPO to be edited, and then click **Edit**.</span></span>

2.  <span data-ttu-id="9eade-123">В окне **редактора управления групповыми политиками** внесите изменения в автономную копию объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9eade-123">In the **Group Policy Management Editor** window, make changes to an offline copy of the GPO.</span></span>

    <span data-ttu-id="9eade-124">**Примечание**  Чтобы отключить все параметры конфигурации компьютера или все параметры конфигурации, щелкните правой кнопкой мыши GPO в окне **редактора управления групповыми политиками** и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="9eade-124">**Note** To disable all Computer Configuration settings or all User Configuration settings, right-click the GPO in the **Group Policy Management Editor** window and click **Properties**.</span></span> <span data-ttu-id="9eade-125">Выберите **Отключить параметры конфигурации компьютера** или **Отключить параметры конфигурации пользователя** .</span><span class="sxs-lookup"><span data-stu-id="9eade-125">Select **Disable Computer Configuration settings** or **Disable User Configuration settings** as appropriate.</span></span>

     

3.  <span data-ttu-id="9eade-126">Когда вы закончите изменение объекта групповой политики, закройте окно **редактора управления групповыми политиками** .</span><span class="sxs-lookup"><span data-stu-id="9eade-126">When you have finished modifying the GPO, close the **Group Policy Management Editor** window.</span></span>

### <a href="" id="bkmk-checkin"></a>

**<span data-ttu-id="9eade-127">Проверка GPO в архиве</span><span class="sxs-lookup"><span data-stu-id="9eade-127">To check a GPO into the archive</span></span>**

1.  <span data-ttu-id="9eade-128">На вкладке **Управление** сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="9eade-128">On the **Controlled** tab:</span></span>

    -   <span data-ttu-id="9eade-129">Если вы не внесли никаких изменений в объект групповой политики, щелкните его правой кнопкой мыши и выберите команду **отменить**извлечение, а затем нажмите кнопку **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9eade-129">If you have made no changes to the GPO, right-click the GPO and click **Undo Check Out**, and then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="9eade-130">Если вы внесли изменения в GPO, щелкните объект правой кнопкой мыши и выберите команду **вернуть**.</span><span class="sxs-lookup"><span data-stu-id="9eade-130">If you have made changes to the GPO, right-click the GPO and click **Check In**.</span></span>

2.  <span data-ttu-id="9eade-131">Введите Примечание, которое будет отображаться в контрольной записи объекта групповой политики, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9eade-131">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

3.  <span data-ttu-id="9eade-132">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9eade-132">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9eade-133">На вкладке **Управление** состоянием объекта групповой политики считается **возвращенное**.</span><span class="sxs-lookup"><span data-stu-id="9eade-133">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="9eade-134">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="9eade-134">Additional considerations</span></span>

-   <span data-ttu-id="9eade-135">Для извлечения и изменения объекта групповой политики по умолчанию необходимо быть утверждающее, которое создало или управляло объектом групповой политики, редактором или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="9eade-135">To check out and edit a GPO, by default you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="9eade-136">В частности, необходимо иметь **содержимое списка** и разрешения на **изменение параметров** для GPO.</span><span class="sxs-lookup"><span data-stu-id="9eade-136">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span> <span data-ttu-id="9eade-137">Кроме того, чтобы изменить GPO, вы должны быть единственным лицом, которое извлеко объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9eade-137">Additionally, to edit the GPO you must be the individual who has checked out the GPO.</span></span>

-   <span data-ttu-id="9eade-138">Для возврата объекта групповой политики по умолчанию вы должны быть редактором, утверждающим или администратором РАСШИРЕНного доступа (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="9eade-138">To check in a GPO, by default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="9eade-139">В частности, необходимо иметь **содержимое списка** и либо **изменить параметры** , либо **развернуть разрешения GPO** для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="9eade-139">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="9eade-140">Если вы не являетесь администратором (или другим администратором групповой политики с разрешениями на **развертывание GPO** ), вы должны быть редактором, который извлек этот GPO.</span><span class="sxs-lookup"><span data-stu-id="9eade-140">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

-   <span data-ttu-id="9eade-141">При редактировании объекта групповой политики обновление установки программного обеспечения из другого GPO должно ссылаться на развернутый GPO, а не на извлеченную копию.</span><span class="sxs-lookup"><span data-stu-id="9eade-141">When editing a GPO, any Group Policy Software Installation upgrade of a package in another GPO should reference the deployed GPO, and not the checked-out copy.</span></span>

### <span data-ttu-id="9eade-142">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="9eade-142">Additional references</span></span>

-   [<span data-ttu-id="9eade-143">Изменение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9eade-143">Editing a GPO</span></span>](editing-a-gpo-agpm30ops.md)

-   <span data-ttu-id="9eade-144">Просмотр объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9eade-144">Reviewing a GPO</span></span>

    -   [<span data-ttu-id="9eade-145">Проверка параметров объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9eade-145">Review GPO Settings</span></span>](review-gpo-settings-agpm30ops.md)

    -   [<span data-ttu-id="9eade-146">Проверка ссылок объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9eade-146">Review GPO Links</span></span>](review-gpo-links-agpm30ops.md)

    -   [<span data-ttu-id="9eade-147">Определение различий между объектами групповой политики, версиями объекта групповой политики или шаблонами</span><span class="sxs-lookup"><span data-stu-id="9eade-147">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md)

-   <span data-ttu-id="9eade-148">Развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9eade-148">Deploying a GPO</span></span>

    -   [<span data-ttu-id="9eade-149">Запрос на развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9eade-149">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo-agpm30ops.md)

    -   [<span data-ttu-id="9eade-150">Развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="9eade-150">Deploy a GPO</span></span>](deploy-a-gpo-agpm30ops.md)

 

 





