---
title: Проверка ссылок объекта групповой политики
description: Проверка ссылок объекта групповой политики
author: dansimp
ms.assetid: 3c472448-f16a-493c-a229-5ca60a470965
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe8b40b4401f08a36217237487bf2b2c0c6c0689
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818342"
---
# <span data-ttu-id="8db4a-103">Проверка ссылок объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="8db4a-103">Review GPO Links</span></span>


<span data-ttu-id="8db4a-104">Вы можете отобразить схему, в которой выбранные объекты групповой политики (GPO) или GPO связаны с организационными подразделениями.</span><span class="sxs-lookup"><span data-stu-id="8db4a-104">You can display a diagram showing where a Group Policy object (GPO) or GPOs that you select are linked to organizational units.</span></span> <span data-ttu-id="8db4a-105">Схемы связей GPO обновляются каждый раз, когда объект групповой политики управляется, импортируется или возвращается.</span><span class="sxs-lookup"><span data-stu-id="8db4a-105">GPO link diagrams are updated each time the GPO is controlled, imported, or checked in.</span></span>

<span data-ttu-id="8db4a-106">Для выполнения этой процедуры требуется учетная запись пользователя с ролью "рецензент", "редактор", "Утверждающий" или администратором расширенного управления групповыми политиками (полный доступ) или необходимыми разрешениями в расширенном управлении групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="8db4a-106">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="8db4a-107">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="8db4a-107">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="8db4a-108">Просмотр ссылок GPO</span><span class="sxs-lookup"><span data-stu-id="8db4a-108">Reviewing GPO links</span></span>


-   [<span data-ttu-id="8db4a-109">Для одного или нескольких GPO</span><span class="sxs-lookup"><span data-stu-id="8db4a-109">For one or more GPOs</span></span>](#bkmk-gpos)

-   [<span data-ttu-id="8db4a-110">Для одной или нескольких версий GPO</span><span class="sxs-lookup"><span data-stu-id="8db4a-110">For one or more versions of a GPO</span></span>](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**<span data-ttu-id="8db4a-111">Отображение связей GPO для одного или нескольких объектов групповой политики</span><span class="sxs-lookup"><span data-stu-id="8db4a-111">To display GPO links for one or more GPOs</span></span>**

1.  <span data-ttu-id="8db4a-112">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8db4a-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8db4a-113">На вкладке **содержание** в области сведений перейдите на вкладку **управляемые**, **ожидающие**или **корзины** , чтобы отобразить объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8db4a-113">On the **Contents** tab in the details pane, click the **Controlled**, **Pending**, or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="8db4a-114">Выберите один или несколько объектов групповой политики, для которых нужно отобразить ссылки, щелкните правой кнопкой мыши выделенный объект групповой политики, выберите пункт **Параметры**, а затем — **ссылки на объекты GPO** , чтобы отобразить схему доменов и организационных подразделений со ссылками на выбранные объекты GPO (-ы).</span><span class="sxs-lookup"><span data-stu-id="8db4a-114">Select one or more GPOs for which to display links, right-click a selected GPO, click **Settings**, and then click **GPO Links** to display a diagram of domains and organizational units with links to the selected GPO(s).</span></span>

### <a href="" id="bkmk-gpo-versions"></a>

**<span data-ttu-id="8db4a-115">Отображение связей GPO для одной или нескольких версий GPO</span><span class="sxs-lookup"><span data-stu-id="8db4a-115">To display GPO links for one or more versions of a GPO</span></span>**

1.  <span data-ttu-id="8db4a-116">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8db4a-116">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8db4a-117">На вкладке **содержание** в области сведений откройте вкладку **управляемая** **или корзины** , чтобы отобразить GPO.</span><span class="sxs-lookup"><span data-stu-id="8db4a-117">On the **Contents** tab in the details pane, click the **Controlled** or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="8db4a-118">Дважды щелкните объект групповой политики, чтобы просмотреть его историю.</span><span class="sxs-lookup"><span data-stu-id="8db4a-118">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="8db4a-119">Щелкните правой кнопкой мыши версию объекта групповой политики, для которого нужно просмотреть параметры, выберите пункт **Параметры**, а затем — **отчет HTML** или **отчет XML** , чтобы просмотреть сводку по параметрам объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8db4a-119">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="8db4a-120">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="8db4a-120">Additional considerations</span></span>

-   <span data-ttu-id="8db4a-121">По умолчанию для выполнения этой процедуры необходимо быть рецензентом, редактором, утверждающим или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="8db4a-121">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="8db4a-122">В частности, необходимо иметь **содержимое списка** и разрешения на **Чтение параметров** для GPO.</span><span class="sxs-lookup"><span data-stu-id="8db4a-122">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="8db4a-123">Кроме того, чтобы отобразить список объектов групповой политики, необходимо иметь разрешение " **содержимое списка** " для домена.</span><span class="sxs-lookup"><span data-stu-id="8db4a-123">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="8db4a-124">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="8db4a-124">Additional references</span></span>

-   [<span data-ttu-id="8db4a-125">Выполнение задач рецензента</span><span class="sxs-lookup"><span data-stu-id="8db4a-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 





