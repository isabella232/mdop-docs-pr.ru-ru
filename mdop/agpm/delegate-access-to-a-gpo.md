---
title: Передача прав доступа к объекту групповой политики
description: Передача прав доступа к объекту групповой политики
author: dansimp
ms.assetid: f1d6bb6c-d5bf-4080-a6cb-32774689f804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57a71528120b65676d25d952d9f9392dc0250ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818782"
---
# <span data-ttu-id="1ac21-103">Передача прав доступа к объекту групповой политики</span><span class="sxs-lookup"><span data-stu-id="1ac21-103">Delegate Access to a GPO</span></span>


<span data-ttu-id="1ac21-104">Утверждающий может делегировать управление управляемым объектом групповой политики (GPO), который был создан этим **утверждающим**.</span><span class="sxs-lookup"><span data-stu-id="1ac21-104">An Approver can delegate the management of a controlled Group Policy object (GPO) that was **created by that Approver**.</span></span> <span data-ttu-id="1ac21-105">Как и Администратор расширенного управления групповыми политиками (полный доступ), утверждающий может делегировать доступ к такому объекту групповой политики, чтобы выбранные редакторы могли его редактировать, рецензенты могут проверить его, а другие утверждающие могут утвердить его.</span><span class="sxs-lookup"><span data-stu-id="1ac21-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO, so selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="1ac21-106">По умолчанию утверждающий не может делегировать доступ к GPO, созданному другим администратором групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1ac21-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="1ac21-107">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора расширенного управления групповыми политиками (полного доступа), учетная запись пользователя утверждающего, создавшего GPO, или учетная запись пользователя с необходимыми разрешениями для расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="1ac21-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="1ac21-108">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="1ac21-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="1ac21-109">Делегирование управления управляемым объектом групповой политики</span><span class="sxs-lookup"><span data-stu-id="1ac21-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="1ac21-110">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1ac21-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="1ac21-111">На вкладке **содержимое** в области сведений откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики, а затем выберите GPO для делегирования.</span><span class="sxs-lookup"><span data-stu-id="1ac21-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="1ac21-112">Нажмите кнопку **Добавить** , выберите пользователей или группы, которым будет разрешен доступ, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ac21-112">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="1ac21-113">Чтобы настроить разрешения для каждого из них, нажмите кнопку " **Дополнительно** " на вкладке " **содержимое** " и установите для разрешений роль разрешение или запрет.</span><span class="sxs-lookup"><span data-stu-id="1ac21-113">To customize the permissions for each, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="1ac21-114">(Для более детального управления в диалоговом окне **разрешения** нажмите кнопку **Дополнительно** .)</span><span class="sxs-lookup"><span data-stu-id="1ac21-114">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="1ac21-115">Нажмите кнопку **Применить**, а затем в диалоговом окне **разрешения** нажмите кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="1ac21-115">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="1ac21-116">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="1ac21-116">Additional considerations</span></span>

-   <span data-ttu-id="1ac21-117">По умолчанию для выполнения этой процедуры необходимо быть утверждающее, которое создало или управляло объектом групповой политики или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="1ac21-117">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="1ac21-118">В частности, необходимо иметь разрешение на доступ к **содержимому** для домена и **изменить разрешение безопасности** для этого объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="1ac21-118">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

### <span data-ttu-id="1ac21-119">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="1ac21-119">Additional references</span></span>

-   [<span data-ttu-id="1ac21-120">Создание, администрирование и импорт объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="1ac21-120">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

 

 





