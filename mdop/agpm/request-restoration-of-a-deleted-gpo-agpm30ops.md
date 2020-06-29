---
title: Запрос на восстановление удаленного объекта групповой политики
description: Запрос на восстановление удаленного объекта групповой политики
author: dansimp
ms.assetid: dcc3baea-8af7-4886-a301-98b6ac5819cd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f85620ed7d9afe676caabe4ce0f7da4fd8d5ae13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820369"
---
# <span data-ttu-id="ebff7-103">Запрос на восстановление удаленного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="ebff7-103">Request Restoration of a Deleted GPO</span></span>


<span data-ttu-id="ebff7-104">Если вы не являетесь утверждающим или администратором РАСШИРЕНного управления правами (полный доступ), вы должны запросить восстановление удаленного объекта групповой политики (GPO) из корзины, чтобы вернуть его в архив.</span><span class="sxs-lookup"><span data-stu-id="ebff7-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the restoration of a deleted Group Policy Object (GPO) from the Recycle Bin to return it to the archive.</span></span>

<span data-ttu-id="ebff7-105">Для выполнения этой процедуры требуется учетная запись пользователя с ролью "редактор" или необходимыми разрешениями в расширенном управлении групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="ebff7-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="ebff7-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="ebff7-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="ebff7-107">Запрос восстановления удаленного объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="ebff7-107">To request the restoration of a deleted GPO</span></span>**

1.  <span data-ttu-id="ebff7-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ebff7-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="ebff7-109">На вкладке " **содержимое** " щелкните вкладку " **Корзина** ", чтобы отобразить удаленные объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ebff7-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="ebff7-110">Щелкните правой кнопкой мыши объект групповой политики, который вы хотите восстановить, и выберите команду **восстановить**.</span><span class="sxs-lookup"><span data-stu-id="ebff7-110">Right-click the GPO you want to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="ebff7-111">Если у вас нет специального разрешения на восстановление объектов групповой политики, необходимо отправить запрос на восстановление удаленного объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ebff7-111">Unless you have special permission to restore GPOs, you must submit a request for restoration of the deleted GPO.</span></span> <span data-ttu-id="ebff7-112">Чтобы получить копию запроса, введите свой адрес электронной почты в поле **"копия"** .</span><span class="sxs-lookup"><span data-stu-id="ebff7-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="ebff7-113">Введите Примечание, которое будет отображаться в контрольной записи для объекта групповой политики, и нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="ebff7-113">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="ebff7-114">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="ebff7-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ebff7-115">Объект групповой политики удаляется из вкладки " **Корзина** " и отображается на вкладке " **управляемые** ".</span><span class="sxs-lookup"><span data-stu-id="ebff7-115">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="ebff7-116">**Примечание**  Если объект групповой политики был удален из рабочей среды, его восстановление в архиве не будет автоматически развертываться в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="ebff7-116">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="ebff7-117">Чтобы вернуть GPO в производственную среду, разверните объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ebff7-117">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="ebff7-118">Дополнительные сведения можно найти [в разделе Развертывание объекта групповой политики](deploy-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="ebff7-118">For information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).</span></span>

 

### <span data-ttu-id="ebff7-119">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="ebff7-119">Additional considerations</span></span>

-   <span data-ttu-id="ebff7-120">Для выполнения этой процедуры необходимо быть редактором по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ebff7-120">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="ebff7-121">В частности, необходимо иметь **содержимое списка** и разрешение на **изменение параметров** для GPO.</span><span class="sxs-lookup"><span data-stu-id="ebff7-121">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="ebff7-122">Чтобы отменить запрос перед его утверждением, откройте вкладку **Ожидание** . Щелкните объект групповой политики правой кнопкой мыши и выберите команду **снять**.</span><span class="sxs-lookup"><span data-stu-id="ebff7-122">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="ebff7-123">Объект групповой политики будет возвращен на вкладку " **Корзина** ".</span><span class="sxs-lookup"><span data-stu-id="ebff7-123">The GPO will be returned to the **Recycle Bin** tab.</span></span>

### <span data-ttu-id="ebff7-124">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="ebff7-124">Additional references</span></span>

-   [<span data-ttu-id="ebff7-125">Удаление, восстановление и уничтожение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="ebff7-125">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





