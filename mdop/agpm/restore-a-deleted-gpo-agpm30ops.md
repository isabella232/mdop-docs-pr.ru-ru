---
title: Восстановление удаленного объекта групповой политики
description: Восстановление удаленного объекта групповой политики
author: dansimp
ms.assetid: 853feb0a-d2d9-4be9-a07e-e113a56a9968
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aae55a654cad44130816af3acc6aad03e96c9959
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818432"
---
# <span data-ttu-id="64987-103">Восстановление удаленного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="64987-103">Restore a Deleted GPO</span></span>


<span data-ttu-id="64987-104">Утверждающие могут восстановить удаленный объект групповой политики (GPO) из корзины и вернуть его в архив.</span><span class="sxs-lookup"><span data-stu-id="64987-104">Approvers can restore a deleted Group Policy Object (GPO) from the Recycle Bin, returning it to the archive.</span></span>

<span data-ttu-id="64987-105">Для выполнения этой процедуры необходимо использовать учетную запись пользователя с ролью "полный доступ" и "Администратор расширенного управления групповыми политиками (для опытных пользователей)" или необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="64987-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="64987-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="64987-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="64987-107">Восстановление удаленного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="64987-107">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="64987-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="64987-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="64987-109">На вкладке " **содержимое** " щелкните вкладку " **Корзина** ", чтобы отобразить удаленные объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="64987-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="64987-110">Щелкните правой кнопкой мыши объект групповой политики, который нужно восстановить, и выберите команду **восстановить**.</span><span class="sxs-lookup"><span data-stu-id="64987-110">Right-click the GPO to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="64987-111">Введите Примечание, которое будет отображаться в журнале объекта групповой политики, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="64987-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="64987-112">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="64987-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="64987-113">Объект групповой политики удаляется из вкладки " **Корзина** " и отображается на вкладке " **управляемые** ".</span><span class="sxs-lookup"><span data-stu-id="64987-113">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="64987-114">**Примечание**  Если объект групповой политики был удален из рабочей среды, его восстановление в архиве не будет автоматически развертываться в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="64987-114">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="64987-115">Чтобы вернуть GPO в производственную среду, разверните объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="64987-115">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="64987-116">Дополнительные сведения можно найти [в разделе Развертывание объекта групповой политики](deploy-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="64987-116">For information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).</span></span>

 

### <span data-ttu-id="64987-117">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="64987-117">Additional considerations</span></span>

-   <span data-ttu-id="64987-118">По умолчанию для выполнения этой процедуры необходимо быть утверждающим или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="64987-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="64987-119">В частности, необходимо иметь **содержимое списка** и либо **развернуть объект GPO** , либо **удалить разрешения GPO** для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="64987-119">Specifically, you must have **List Contents** and either **Deploy GPO** or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="64987-120">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="64987-120">Additional references</span></span>

-   [<span data-ttu-id="64987-121">Удаление, восстановление и уничтожение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="64987-121">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





