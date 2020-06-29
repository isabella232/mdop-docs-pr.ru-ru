---
title: Определение различий между объектами групповой политики, версиями объекта групповой политики или шаблонами
description: Определение различий между объектами групповой политики, версиями объекта групповой политики или шаблонами
author: dansimp
ms.assetid: 3f03c368-162b-450f-be6c-2807c3e8d741
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bf5a7c71b431c787dcb2b16fe9a19f7ff9b06046
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820762"
---
# <span data-ttu-id="8e505-103">Определение различий между объектами групповой политики, версиями объекта групповой политики или шаблонами</span><span class="sxs-lookup"><span data-stu-id="8e505-103">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>


<span data-ttu-id="8e505-104">Вы можете создавать отчеты об отличиях на основе HTML или XML для анализа различий между объектами групповой политики (GPO), шаблонами или различными версиями GPO.</span><span class="sxs-lookup"><span data-stu-id="8e505-104">You can generate HTML-based or XML-based difference reports to analyze the differences between Group Policy Objects (GPOs), templates, or different versions of a GPO.</span></span>

<span data-ttu-id="8e505-105">Для выполнения этой процедуры требуется учетная запись пользователя с ролью "рецензент", "редактор", "Утверждающий" или "Администратор расширенного управления групповыми политиками (полный доступ") или необходимыми разрешениями в расширенном управлении групповой политикой (ГРУППОВое управление).</span><span class="sxs-lookup"><span data-stu-id="8e505-105">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM)is required to complete this procedure.</span></span> <span data-ttu-id="8e505-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="8e505-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="8e505-107">Определение различий между GPO, версиями объектов групповой политики или шаблонами</span><span class="sxs-lookup"><span data-stu-id="8e505-107">Identifying differences between GPOs, GPO versions, or templates</span></span>


-   [<span data-ttu-id="8e505-108">Между двумя объектами групповой политики или шаблонами</span><span class="sxs-lookup"><span data-stu-id="8e505-108">Between two GPOs or templates</span></span>](#bkmk-two-gpos)

-   [<span data-ttu-id="8e505-109">Между объектом групповой политики и шаблоном</span><span class="sxs-lookup"><span data-stu-id="8e505-109">Between a GPO and a template</span></span>](#bkmk-gpo-and-template)

-   [<span data-ttu-id="8e505-110">Между двумя версиями одного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="8e505-110">Between two versions of one GPO</span></span>](#bkmk-two-versions)

-   [<span data-ttu-id="8e505-111">Между версией GPO и шаблоном</span><span class="sxs-lookup"><span data-stu-id="8e505-111">Between a GPO version and a template</span></span>](#bkmk-gpo-version-and-template)

## <a href="" id="bkmk-two-gpos"></a>


**<span data-ttu-id="8e505-112">Определение различий между двумя объектами групповой политики или шаблонами</span><span class="sxs-lookup"><span data-stu-id="8e505-112">To identify differences between two GPOs or templates</span></span>**

1.  <span data-ttu-id="8e505-113">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8e505-113">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8e505-114">На вкладке **содержание** в области сведений щелкните вкладку, чтобы отобразить объекты групповой политики (или шаблоны, если они сравниваются два шаблона).</span><span class="sxs-lookup"><span data-stu-id="8e505-114">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="8e505-115">Выберите два GPO или шаблоны.</span><span class="sxs-lookup"><span data-stu-id="8e505-115">Select the two GPOs or templates.</span></span>

4.  <span data-ttu-id="8e505-116">Щелкните правой кнопкой мыши один из объектов групповой политики или шаблонов, выберите пункт **различия**, а затем — **отчет о формате HTML** или **отчет в формате XML** для отображения отчета о различиях между параметрами объектов групповой политики (GPO) и шаблонов.</span><span class="sxs-lookup"><span data-stu-id="8e505-116">Right-click one of the GPOs or templates, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs or templates.</span></span>

### <a href="" id="bkmk-gpo-and-template"></a>

**<span data-ttu-id="8e505-117">Определение различий между объектом групповой политики и шаблоном</span><span class="sxs-lookup"><span data-stu-id="8e505-117">To identify differences between a GPO and a template</span></span>**

1.  <span data-ttu-id="8e505-118">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8e505-118">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8e505-119">На вкладке **содержание** в области сведений щелкните вкладку, чтобы отобразить объекты групповой политики (или шаблоны, если они сравниваются два шаблона).</span><span class="sxs-lookup"><span data-stu-id="8e505-119">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="8e505-120">Щелкните объект групповой политики правой кнопкой мыши, выберите пункт " **различия**", а затем — пункт " **шаблон**".</span><span class="sxs-lookup"><span data-stu-id="8e505-120">Right-click the GPO, click **Differences**, and then click **Template**.</span></span>

4.  <span data-ttu-id="8e505-121">Выберите шаблон и тип отчета, а затем нажмите кнопку **ОК** , чтобы отобразить отчет о разнице, в котором выводятся общие сведения о параметрах GPO и шаблона.</span><span class="sxs-lookup"><span data-stu-id="8e505-121">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO and template.</span></span>

### <a href="" id="bkmk-two-versions"></a>

**<span data-ttu-id="8e505-122">Определение различий между двумя версиями одного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="8e505-122">To identify differences between two versions of one GPO</span></span>**

1.  <span data-ttu-id="8e505-123">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8e505-123">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8e505-124">На вкладке **содержание** в области сведений щелкните вкладку, чтобы отобразить объекты групповой политики (или шаблоны, если они сравниваются два шаблона).</span><span class="sxs-lookup"><span data-stu-id="8e505-124">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="8e505-125">Дважды щелкните объект групповой политики, чтобы просмотреть его историю, а затем выберите версии для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8e505-125">Double-click the GPO to display its history, and then highlight the versions to be compared.</span></span>

4.  <span data-ttu-id="8e505-126">Щелкните правой кнопкой мыши одну из версий, выберите пункт **различия**, а затем — **отчет HTML** или **отчет в формате XML** для отображения отчета о различиях между параметрами GPO.</span><span class="sxs-lookup"><span data-stu-id="8e505-126">Right-click one of the versions, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs.</span></span>

### <a href="" id="bkmk-gpo-version-and-template"></a>

**<span data-ttu-id="8e505-127">Определение различий между версией GPO и шаблоном</span><span class="sxs-lookup"><span data-stu-id="8e505-127">To identify differences between a GPO version and a template</span></span>**

1.  <span data-ttu-id="8e505-128">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8e505-128">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8e505-129">На вкладке **содержание** в области сведений щелкните вкладку, чтобы отобразить объекты групповой политики (или шаблоны, если они сравниваются два шаблона).</span><span class="sxs-lookup"><span data-stu-id="8e505-129">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="8e505-130">Дважды щелкните объект групповой политики, чтобы просмотреть его историю.</span><span class="sxs-lookup"><span data-stu-id="8e505-130">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="8e505-131">Щелкните правой кнопкой мыши требуемую версию объекта групповой политики, выберите пункт **отличия**, а затем — **шаблон**.</span><span class="sxs-lookup"><span data-stu-id="8e505-131">Right-click the GPO version of interest, click **Differences**, and then click **Template**.</span></span>

5.  <span data-ttu-id="8e505-132">Выберите шаблон и тип отчета, а затем нажмите кнопку **ОК** , чтобы отобразить отчет о разнице, в котором суммируются параметры версии и шаблона объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8e505-132">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO version and template.</span></span>

## <span data-ttu-id="8e505-133">Ключевые для отчетов о различиях</span><span class="sxs-lookup"><span data-stu-id="8e505-133">Key to difference reports</span></span>


<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8e505-134">Символ</span><span class="sxs-lookup"><span data-stu-id="8e505-134">Symbol</span></span></th>
<th align="left"><span data-ttu-id="8e505-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8e505-135">Meaning</span></span></th>
<th align="left"><span data-ttu-id="8e505-136">Цвет</span><span class="sxs-lookup"><span data-stu-id="8e505-136">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8e505-137">Нет</span><span class="sxs-lookup"><span data-stu-id="8e505-137">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e505-138">Элемент существует с одинаковыми параметрами в обоих объектах групповой политики</span><span class="sxs-lookup"><span data-stu-id="8e505-138">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e505-139">Зависит от уровня</span><span class="sxs-lookup"><span data-stu-id="8e505-139">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8e505-140">[#]</span><span class="sxs-lookup"><span data-stu-id="8e505-140">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8e505-141">Элемент существует в обоих объектах GPO, но с измененными параметрами</span><span class="sxs-lookup"><span data-stu-id="8e505-141">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e505-142">Синюю</span><span class="sxs-lookup"><span data-stu-id="8e505-142">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8e505-143">[-]</span><span class="sxs-lookup"><span data-stu-id="8e505-143">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8e505-144">Элемент существует только в первом объекте групповой политики</span><span class="sxs-lookup"><span data-stu-id="8e505-144">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e505-145">Красный</span><span class="sxs-lookup"><span data-stu-id="8e505-145">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8e505-146">[+]</span><span class="sxs-lookup"><span data-stu-id="8e505-146">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8e505-147">Элемент существует только во втором объекте групповой политики</span><span class="sxs-lookup"><span data-stu-id="8e505-147">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e505-148">Зеленый</span><span class="sxs-lookup"><span data-stu-id="8e505-148">Green</span></span></p></td>
</tr>
</tbody>
</table>

 

-   <span data-ttu-id="8e505-149">Для элементов с измененными параметрами измененные параметры определяются при разворачивании элемента.</span><span class="sxs-lookup"><span data-stu-id="8e505-149">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="8e505-150">Значение атрибута в каждом объекте групповой политики отображается в том же порядке, в котором эти объекты отображаются в отчете.</span><span class="sxs-lookup"><span data-stu-id="8e505-150">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="8e505-151">Некоторые изменения в параметрах могут привести к тому, что элемент будет представлен в виде двух различных элементов (один — только в первый объект групповой политики), но только во второй, а не в виде одного из измененных элементов.</span><span class="sxs-lookup"><span data-stu-id="8e505-151">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second) rather than as one item that has changed.</span></span>

### <span data-ttu-id="8e505-152">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="8e505-152">Additional considerations</span></span>

-   <span data-ttu-id="8e505-153">По умолчанию для выполнения этой процедуры необходимо быть рецензентом, редактором, утверждающим или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="8e505-153">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="8e505-154">В частности, необходимо иметь **содержимое списка** и разрешения на **Чтение параметров** для GPO.</span><span class="sxs-lookup"><span data-stu-id="8e505-154">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="8e505-155">Кроме того, чтобы отобразить список объектов групповой политики, необходимо иметь разрешение " **содержимое списка** " для домена.</span><span class="sxs-lookup"><span data-stu-id="8e505-155">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="8e505-156">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="8e505-156">Additional references</span></span>

-   [<span data-ttu-id="8e505-157">Выполнение задач рецензента</span><span class="sxs-lookup"><span data-stu-id="8e505-157">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





