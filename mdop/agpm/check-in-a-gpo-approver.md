---
title: Регистрация объекта групповой политики
description: Регистрация объекта групповой политики
author: dansimp
ms.assetid: e428cfff-651f-4903-bf01-d742714d2fa9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6adbcfa1c2b0d79389bc16dd1dde5afc0a4ec4a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819149"
---
# <span data-ttu-id="078b4-103">Регистрация объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="078b4-103">Check In a GPO</span></span>


<span data-ttu-id="078b4-104">Обычно редакторы должны проверять объекты групповой политики (GPO), которые они изменили, когда их изменения завершены.</span><span class="sxs-lookup"><span data-stu-id="078b4-104">Ordinarily, Editors should check in Group Policy objects (GPOs) that they have edited when their modifications are complete.</span></span> <span data-ttu-id="078b4-105">(Подробные сведения об этом можно найти [в разделе изменение GPO в автономном режиме](edit-a-gpo-offline.md).) Тем не менее, если редактор недоступен, утверждающий также может вернуть объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="078b4-105">(For details, see [Edit a GPO Offline](edit-a-gpo-offline.md).) However, if the Editor is unavailable, an Approver can also check in a GPO.</span></span>

<span data-ttu-id="078b4-106">Для выполнения этой процедуры требуется учетная запись пользователя с ролью "редактор", утверждающего или администратором расширенного управления групповыми политиками (полный доступ) или необходимыми разрешениями в расширенном управлении групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="078b4-106">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="078b4-107">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="078b4-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="078b4-108">Возврат объекта групповой политики, который был извлечен редактором</span><span class="sxs-lookup"><span data-stu-id="078b4-108">To check in a GPO that has been checked out by an Editor</span></span>**

1.  <span data-ttu-id="078b4-109">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="078b4-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="078b4-110">На вкладке **содержание** в области сведений откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="078b4-110">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

    -   <span data-ttu-id="078b4-111">Чтобы отменить изменения, внесенные редактором, щелкните объект групповой политики правой кнопкой мыши, выберите команду **отменить**извлечение и нажмите кнопку **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="078b4-111">To discard any changes made by the Editor, right-click the GPO, click **Undo Check Out**, and then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="078b4-112">Чтобы сохранить изменения, внесенные редактором, щелкните объект правой кнопкой мыши и выберите команду **вернуть**.</span><span class="sxs-lookup"><span data-stu-id="078b4-112">To retain changes made by the Editor, right-click the GPO and then click **Check In**.</span></span>

3.  <span data-ttu-id="078b4-113">Введите Примечание, которое будет отображаться в контрольной записи объекта групповой политики, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="078b4-113">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="078b4-114">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="078b4-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="078b4-115">На вкладке **Управление** состоянием объекта групповой политики считается **возвращенное**.</span><span class="sxs-lookup"><span data-stu-id="078b4-115">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="078b4-116">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="078b4-116">Additional considerations</span></span>

-   <span data-ttu-id="078b4-117">По умолчанию для выполнения этой процедуры необходимо быть редактором, утверждающим или администратором РАСШИРЕНного управления правами (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="078b4-117">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="078b4-118">В частности, необходимо иметь **содержимое списка** и либо **изменить параметры** , либо **развернуть разрешения GPO** для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="078b4-118">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="078b4-119">Если вы не являетесь администратором (или другим администратором групповой политики с разрешениями на **развертывание GPO** ), вы должны быть редактором, который извлек этот GPO.</span><span class="sxs-lookup"><span data-stu-id="078b4-119">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

### <span data-ttu-id="078b4-120">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="078b4-120">Additional references</span></span>

-   [<span data-ttu-id="078b4-121">Выполнение задач утверждающего</span><span class="sxs-lookup"><span data-stu-id="078b4-121">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="078b4-122">Изменение объекта групповой политики в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="078b4-122">Edit a GPO Offline</span></span>](edit-a-gpo-offline.md)

 

 





