---
title: Уничтожение объекта групповой политики
description: Уничтожение объекта групповой политики
author: dansimp
ms.assetid: d74941a3-beef-46cd-a4ca-80a324dcfadf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5545918c417fce16bfc2369ebc6fc2199390adc6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818649"
---
# <span data-ttu-id="a61c7-103">Уничтожение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="a61c7-103">Destroy a GPO</span></span>


<span data-ttu-id="a61c7-104">Расширенное управление групповыми политиками позволяет утверждающим уничтожить объект групповой политики (GPO), удалить его из корзины и окончательно удалить его, чтобы его нельзя было восстановить.</span><span class="sxs-lookup"><span data-stu-id="a61c7-104">Advanced Group Policy Management (AGPM) enables Approvers to destroy a Group Policy object (GPO), removing it from the Recycle Bin and permanently deleting it so that it can no longer be restored.</span></span>

<span data-ttu-id="a61c7-105">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора (полного доступа) утверждающего или расширенного управления групповыми политиками или необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="a61c7-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="a61c7-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="a61c7-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="a61c7-107">Окончательное удаление объекта групповой политики, чтобы его нельзя было восстановить</span><span class="sxs-lookup"><span data-stu-id="a61c7-107">To permanently delete a GPO so it can no longer be restored</span></span>**

1.  <span data-ttu-id="a61c7-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="a61c7-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="a61c7-109">На вкладке " **содержимое** " щелкните вкладку " **Корзина** ", чтобы отобразить удаленные объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="a61c7-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="a61c7-110">Щелкните правой кнопкой мыши объект групповой политики, который нужно удалить, и выберите команду **уничтожить**.</span><span class="sxs-lookup"><span data-stu-id="a61c7-110">Right-click the GPO to destroy, and then click **Destroy**.</span></span>

4.  <span data-ttu-id="a61c7-111">Нажмите кнопку **Да** , чтобы подтвердить, что вы хотите окончательно удалить выбранный объект групповой политики и все резервные копии из архива.</span><span class="sxs-lookup"><span data-stu-id="a61c7-111">Click **Yes** to confirm that you want to permanently delete the selected GPO and all backups from the archive.</span></span>

5.  <span data-ttu-id="a61c7-112">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="a61c7-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="a61c7-113">Объект групповой политики удаляется из **корзины** на вкладке "Корзина" и окончательно удаляется.</span><span class="sxs-lookup"><span data-stu-id="a61c7-113">The GPO is removed from the **Recycle Bin** tab and is permanently deleted.</span></span>

### <span data-ttu-id="a61c7-114">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="a61c7-114">Additional considerations</span></span>

-   <span data-ttu-id="a61c7-115">По умолчанию для выполнения этой процедуры необходимо быть утверждающим или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="a61c7-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="a61c7-116">В частности, необходимо иметь **содержимое списка** и **удалить разрешения GPO** для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="a61c7-116">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="a61c7-117">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="a61c7-117">Additional references</span></span>

-   [<span data-ttu-id="a61c7-118">Удаление, восстановление и уничтожение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="a61c7-118">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 





