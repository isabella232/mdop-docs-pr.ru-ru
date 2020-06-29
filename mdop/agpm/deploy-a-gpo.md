---
title: Развертывание объекта групповой политики
description: Развертывание объекта групповой политики
author: dansimp
ms.assetid: a0a3f292-e3ab-46ae-a0fd-d7b2b4ad8883
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a98bdd758937d86cf8c30c5abf0b49302d377360
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818699"
---
# <span data-ttu-id="8ac15-103">Развертывание объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="8ac15-103">Deploy a GPO</span></span>


<span data-ttu-id="8ac15-104">Расширенное управление групповыми политиками позволяет утверждающему для развертывания нового или измененного объекта групповой политики (GPO) в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="8ac15-104">Advanced Group Policy Management (AGPM) enables an Approver to deploy a new or edited Group Policy object (GPO) to the production environment.</span></span> <span data-ttu-id="8ac15-105">Сведения о повторном развертывании предыдущей версии объекта групповой политики содержатся в разделе [откат к предыдущей версии объекта групповой политики](roll-back-to-a-previous-version-of-a-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="8ac15-105">For information about redeploying a previous version of a GPO, see [Roll Back to a Previous Version of a GPO](roll-back-to-a-previous-version-of-a-gpo.md).</span></span>

<span data-ttu-id="8ac15-106">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора (полного доступа) утверждающего или расширенного управления групповыми политиками или необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="8ac15-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="8ac15-107">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="8ac15-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="8ac15-108">Развертывание объекта групповой политики в рабочей среде</span><span class="sxs-lookup"><span data-stu-id="8ac15-108">To deploy a GPO to the production environment</span></span>**

1.  <span data-ttu-id="8ac15-109">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8ac15-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8ac15-110">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8ac15-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="8ac15-111">Щелкните правой кнопкой мыши объект групповой политики, который нужно развернуть, и нажмите кнопку **развернуть**.</span><span class="sxs-lookup"><span data-stu-id="8ac15-111">Right-click the GPO to be deployed and then click **Deploy**.</span></span>

4.  <span data-ttu-id="8ac15-112">Чтобы просмотреть ссылки на объект групповой политики, нажмите кнопку **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="8ac15-112">To review links to the GPO, click **Advanced**.</span></span> <span data-ttu-id="8ac15-113">Для отображения подробных сведений наведите указатель мыши на узел дерева.</span><span class="sxs-lookup"><span data-stu-id="8ac15-113">Pause the mouse pointer on a node in the tree to display details.</span></span>

    -   <span data-ttu-id="8ac15-114">По умолчанию все ссылки на объект групповой политики будут восстановлены.</span><span class="sxs-lookup"><span data-stu-id="8ac15-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="8ac15-115">Чтобы отменить восстановление ссылки, снимите флажок для этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="8ac15-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="8ac15-116">Чтобы запретить восстановление всех связей, снимите флажок **Восстановление связей** в диалоговом окне " **Развертывание объекта групповой политики** ".</span><span class="sxs-lookup"><span data-stu-id="8ac15-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="8ac15-117">Щелкните **Да**.</span><span class="sxs-lookup"><span data-stu-id="8ac15-117">Click **Yes**.</span></span> <span data-ttu-id="8ac15-118">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="8ac15-118">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

<span data-ttu-id="8ac15-119">**Примечание**  Чтобы проверить, не была ли развернута самая последняя версия объекта групповой политики, на вкладке **управляемые** дважды щелкните объект групповой политики, чтобы просмотреть его **историю**.</span><span class="sxs-lookup"><span data-stu-id="8ac15-119">**Note** To verify whether the most recent version of a GPO has been deployed, on the **Controlled** tab, double-click the GPO to display its **History**.</span></span> <span data-ttu-id="8ac15-120">В **журнале** для объекта групповой политики столбец **State** указывает, был ли развернут объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8ac15-120">In the **History** for the GPO, the **State** column indicates whether a GPO has been deployed.</span></span>

 

### <span data-ttu-id="8ac15-121">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="8ac15-121">Additional considerations</span></span>

-   <span data-ttu-id="8ac15-122">По умолчанию для выполнения этой процедуры необходимо быть утверждающим или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="8ac15-122">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="8ac15-123">В частности, необходимо иметь **содержимое списка** и **развернуть разрешения GPO** для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="8ac15-123">Specifically, you must have **List Contents** and **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="8ac15-124">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="8ac15-124">Additional references</span></span>

-   [<span data-ttu-id="8ac15-125">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="8ac15-125">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

 

 





