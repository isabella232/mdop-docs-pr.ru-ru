---
title: Создание метки для текущей версии объекта групповой политики
description: Создание метки для текущей версии объекта групповой политики
author: dansimp
ms.assetid: 3845211a-0bc9-4875-9906-cb758c443825
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f9e656258591a56397c5a8053b2e98772f57949a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820669"
---
# <span data-ttu-id="01fbe-103">Создание метки для текущей версии объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="01fbe-103">Label the Current Version of a GPO</span></span>


<span data-ttu-id="01fbe-104">Вы можете пометить текущую версию объекта групповой политики (GPO) для упрощения идентификации в ее истории.</span><span class="sxs-lookup"><span data-stu-id="01fbe-104">You can label the current version of a Group Policy Object (GPO) for easy identification in its history.</span></span> <span data-ttu-id="01fbe-105">Вы можете использовать метку для идентификации известной правильной версии, для которой можно выполнить откат в случае возникновения проблемы.</span><span class="sxs-lookup"><span data-stu-id="01fbe-105">You can use a label to identify a known good version to which you could roll back if a problem occurs.</span></span> <span data-ttu-id="01fbe-106">Кроме того, указав несколько GPO с одной и той же меткой, вы можете пометить связанные объекты GPO, которые нужно вернуть в ту же точку, если потребуется выполнить откат позже.</span><span class="sxs-lookup"><span data-stu-id="01fbe-106">Also, by labeling multiple GPOs with the same label at one time, you can mark related GPOs that should be rolled back to the same point if rollback should later be necessary.</span></span>

<span data-ttu-id="01fbe-107">Для выполнения этой процедуры требуется учетная запись пользователя с ролью "редактор", "Утверждающий" или "Администратор расширенного управления групповыми политиками (полный доступ") или необходимыми разрешениями в расширенном управлении групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="01fbe-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="01fbe-108">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="01fbe-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="01fbe-109">Создание метки текущей версии объектов групповой политики в истории</span><span class="sxs-lookup"><span data-stu-id="01fbe-109">To label the current version of GPOs in their histories</span></span>**

1.  <span data-ttu-id="01fbe-110">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="01fbe-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="01fbe-111">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="01fbe-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="01fbe-112">Щелкните объект групповой политики, для которого нужно добавить метку для текущей версии.</span><span class="sxs-lookup"><span data-stu-id="01fbe-112">Click a GPO for which to label the current version.</span></span> <span data-ttu-id="01fbe-113">Чтобы выделить несколько объектов групповой политики, нажмите клавишу SHIFT и, удерживая ее, щелкните последний GPO в группе объектов групповой политики или нажмите клавишу CTRL и выберите отдельные GPO.</span><span class="sxs-lookup"><span data-stu-id="01fbe-113">To select multiple GPOs, press SHIFT and click the last GPO in a contiguous group of GPOs, or press CTRL and click individual GPOs.</span></span> <span data-ttu-id="01fbe-114">Щелкните выделенный объект групповой политики правой кнопкой мыши и выберите пункт **Метка**.</span><span class="sxs-lookup"><span data-stu-id="01fbe-114">Right-click a selected GPO, and then click **Label**.</span></span>

4.  <span data-ttu-id="01fbe-115">Введите метку и Примечание, которое будет отображаться в истории каждого выбранного объекта групповой политики, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="01fbe-115">Type a label and a comment to be displayed in the history of each GPO selected, and then click **OK**.</span></span>

5.  <span data-ttu-id="01fbe-116">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="01fbe-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

### <span data-ttu-id="01fbe-117">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="01fbe-117">Additional considerations</span></span>

-   <span data-ttu-id="01fbe-118">По умолчанию для выполнения этой процедуры необходимо быть редактором, утверждающим или администратором РАСШИРЕНного управления правами (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="01fbe-118">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="01fbe-119">В частности, необходимо иметь **содержимое списка** и либо **изменить параметры** , либо **развернуть разрешения GPO** для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="01fbe-119">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="01fbe-120">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="01fbe-120">Additional references</span></span>

-   [<span data-ttu-id="01fbe-121">Изменение объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="01fbe-121">Editing a GPO</span></span>](editing-a-gpo-agpm30ops.md)

 

 





