---
title: Утверждение или отклонение ожидающего действия
description: Утверждение или отклонение ожидающего действия
author: dansimp
ms.assetid: 078ea8b5-9ac5-45fc-9ac1-a1aa629c10b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61014ec46db2beb9a525abe8d9b2b0902b3aa78d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819222"
---
# <span data-ttu-id="ee470-103">Утверждение или отклонение ожидающего действия</span><span class="sxs-lookup"><span data-stu-id="ee470-103">Approve or Reject a Pending Action</span></span>


<span data-ttu-id="ee470-104">Основным обязанностью утверждающего является оценка, утверждение или отклонение запросов на создание объекта групповой политики, развертывание и удаление из редакторов или рецензентов, у которых нет разрешения на выполнение этих действий.</span><span class="sxs-lookup"><span data-stu-id="ee470-104">The core responsibility of an Approver is to evaluate and then approve or reject requests for Group Policy Object (GPO) creation, deployment, and deletion from Editors or Reviewers who do not have permission to complete those actions.</span></span> <span data-ttu-id="ee470-105">Отчеты могут помочь утверждающему лицу оценить новую версию объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ee470-105">Reports can assist an Approver with evaluating a new version of a GPO.</span></span>

<span data-ttu-id="ee470-106">Для выполнения этой процедуры необходимо использовать учетную запись пользователя с ролью "полный доступ" и "Администратор расширенного управления групповыми политиками (для опытных пользователей)" или необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="ee470-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="ee470-107">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="ee470-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="ee470-108">Утверждение или отклонение ожидающего запроса</span><span class="sxs-lookup"><span data-stu-id="ee470-108">To approve or reject a pending request</span></span>**

1.  <span data-ttu-id="ee470-109">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ee470-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="ee470-110">На вкладке **содержание** откройте вкладку **ожидается** , чтобы отобразить ожидающие GPO.</span><span class="sxs-lookup"><span data-stu-id="ee470-110">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

3.  <span data-ttu-id="ee470-111">Щелкните правой кнопкой мыши ожидающий GPO и выберите команду **утвердить** или **отклонить**.</span><span class="sxs-lookup"><span data-stu-id="ee470-111">Right-click a pending GPO, and then click either **Approve** or **Reject**.</span></span>

4.  <span data-ttu-id="ee470-112">Если вы утверждаете развертывание, в диалоговом окне **утверждение ожидающей операции** нажмите кнопку **Дополнительно** , чтобы просмотреть ссылки на объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ee470-112">If approving deployment, click **Advanced** in the **Approve Pending Operation** dialog box to review links to the GPO.</span></span> <span data-ttu-id="ee470-113">Для отображения подробных сведений наведите указатель мыши на элемент дерева.</span><span class="sxs-lookup"><span data-stu-id="ee470-113">Pause the mouse pointer on an item in the tree to display details.</span></span>

    -   <span data-ttu-id="ee470-114">По умолчанию все ссылки на объект групповой политики будут восстановлены.</span><span class="sxs-lookup"><span data-stu-id="ee470-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="ee470-115">Чтобы отменить восстановление ссылки, снимите флажок для этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="ee470-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="ee470-116">Чтобы запретить восстановление всех связей, снимите флажок **Восстановление связей** в диалоговом окне " **Развертывание объекта групповой политики** ".</span><span class="sxs-lookup"><span data-stu-id="ee470-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="ee470-117">Нажмите кнопку **Да** или **ОК** , чтобы подтвердить утверждение или отклонение ожидающего действия.</span><span class="sxs-lookup"><span data-stu-id="ee470-117">Click **Yes** or **OK** to confirm approval or rejection of the pending action.</span></span> <span data-ttu-id="ee470-118">Если вы утвердили запрос, объект групповой политики перемещается на соответствующую вкладку для действия, которое необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="ee470-118">If you have approved the request, the GPO is moved to the appropriate tab for the action performed.</span></span>

    <span data-ttu-id="ee470-119">**Примечание**  Если адрес электронной почты утверждающего абонента включен в поле " **адрес электронной почты** " на вкладке " **Делегирование** **домена** ", утверждающий будет получать ЭЛЕКТРОНную почту из псевдонима расширенного доступа, когда редактор или проверяющий отправляет запрос.</span><span class="sxs-lookup"><span data-stu-id="ee470-119">**Note** If an Approver's e-mail address is included in the **To e-mail address** field on the **Domain** **Delegation** tab, the Approver will receive e-mail from the AGPM alias when an Editor or Reviewer submits a request.</span></span>

     

### <span data-ttu-id="ee470-120">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="ee470-120">Additional considerations</span></span>

-   <span data-ttu-id="ee470-121">По умолчанию для выполнения этой процедуры необходимо быть утверждающим или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="ee470-121">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="ee470-122">В частности, у вас должны быть разрешения, необходимые для выполнения утвержденных запросов.</span><span class="sxs-lookup"><span data-stu-id="ee470-122">Specifically, you must have the permissions required to perform the request that you are approving.</span></span>

### <span data-ttu-id="ee470-123">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="ee470-123">Additional references</span></span>

-   [<span data-ttu-id="ee470-124">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="ee470-124">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

 

 





