---
title: Переименование объекта групповой политики или шаблона
description: Переименование объекта групповой политики или шаблона
author: dansimp
ms.assetid: 19d17ddf-8b58-4677-929e-9550fa388b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 44d1cef33d8c0004ef3639311fbf135b4dea9d39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818519"
---
# <span data-ttu-id="6138b-103">Переименование объекта групповой политики или шаблона</span><span class="sxs-lookup"><span data-stu-id="6138b-103">Rename a GPO or Template</span></span>


<span data-ttu-id="6138b-104">Вы можете переименовать управляемый объект групповой политики (GPO) или шаблон.</span><span class="sxs-lookup"><span data-stu-id="6138b-104">You can rename a controlled Group Policy Object (GPO) or a template.</span></span>

<span data-ttu-id="6138b-105">Для выполнения этой процедуры требуется учетная запись пользователя с ролью редактора или администратора управления групповыми политиками (полного доступа), учетной записи пользователя утверждающего, создавшего GPO, или учетной записи пользователя с необходимыми разрешениями для расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="6138b-105">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="6138b-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="6138b-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="6138b-107">Переименование объекта групповой политики или шаблона</span><span class="sxs-lookup"><span data-stu-id="6138b-107">To rename a GPO or template</span></span>**

1.  <span data-ttu-id="6138b-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6138b-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="6138b-109">На вкладке **содержание** откройте вкладку **управляемый** или **шаблон** , чтобы отобразить элемент, который нужно переименовать.</span><span class="sxs-lookup"><span data-stu-id="6138b-109">On the **Contents** tab, click the **Controlled** or **Templates** tab to display the item to rename.</span></span>

3.  <span data-ttu-id="6138b-110">Щелкните правой кнопкой мыши объект групповой политики или шаблон, который нужно переименовать, и выберите команду **Переименовать**.</span><span class="sxs-lookup"><span data-stu-id="6138b-110">Right-click the GPO or template to rename and click **Rename**.</span></span>

4.  <span data-ttu-id="6138b-111">Введите новое имя объекта групповой политики или шаблона и примечания, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6138b-111">Type the new name for the GPO or template and a comment, and then click **OK**.</span></span>

5.  <span data-ttu-id="6138b-112">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="6138b-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="6138b-113">Объект групповой политики или шаблон появится под новым именем на вкладке **содержание** .</span><span class="sxs-lookup"><span data-stu-id="6138b-113">The GPO or template appears under the new name on the **Contents** tab.</span></span>

### <span data-ttu-id="6138b-114">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="6138b-114">Additional considerations</span></span>

-   <span data-ttu-id="6138b-115">По умолчанию для выполнения этой процедуры необходимо быть утверждающее, которое создало или управляло объектом групповой политики, редактором или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="6138b-115">By default, you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="6138b-116">В частности, необходимо иметь **содержимое списка** и разрешение на **изменение параметров** для GPO.</span><span class="sxs-lookup"><span data-stu-id="6138b-116">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="6138b-117">При переименовании объекта групповой политики, который был развернут, имя будет немедленно изменено в архиве.</span><span class="sxs-lookup"><span data-stu-id="6138b-117">When you rename a GPO that has been deployed, the name is immediately changed in the archive.</span></span> <span data-ttu-id="6138b-118">Имя изменяется в рабочей среде только при повторном развертывании объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="6138b-118">The name is changed in the production environment only when the GPO is redeployed.</span></span> <span data-ttu-id="6138b-119">Пока объект групповой политики не будет повторно развернут (или удалена), старое имя по-прежнему используется в производственной среде и, следовательно, нельзя использовать для другого GPO.</span><span class="sxs-lookup"><span data-stu-id="6138b-119">Until the GPO is redeployed (or the production copy is deleted), the old name is still in use in the production environment and therefore cannot be used for another GPO.</span></span> <span data-ttu-id="6138b-120">Аналогичным образом, невозможно повторно переименовать GPO в архиве, пока он не будет развернут (изменяя название производственной копии), или окончательной копии был удален.</span><span class="sxs-lookup"><span data-stu-id="6138b-120">Likewise, the GPO in the archive cannot be renamed back to its original name until the GPO has been deployed (changing the name of the production copy) or the production copy has been deleted.</span></span>

### <span data-ttu-id="6138b-121">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="6138b-121">Additional references</span></span>

-   [<span data-ttu-id="6138b-122">Изменение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="6138b-122">Editing a GPO</span></span>](editing-a-gpo-agpm30ops.md)

 

 





