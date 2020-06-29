---
title: Управление ранее неуправляемым объектом групповой политики
description: Управление ранее неуправляемым объектом групповой политики
author: dansimp
ms.assetid: 452689a9-4e32-4e3b-8208-56353a82bf36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d7349b16b326a49b701efae5379c313bde0964f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818889"
---
# <span data-ttu-id="96d4d-103">Управление ранее неуправляемым объектом групповой политики</span><span class="sxs-lookup"><span data-stu-id="96d4d-103">Control a Previously Uncontrolled GPO</span></span>


<span data-ttu-id="96d4d-104">Чтобы использовать расширенное управление групповыми политиками для предоставления управления изменениями для объекта групповой политики (GPO), необходимо сначала настроить этот объект с помощью РАСШИРЕНного управления правами.</span><span class="sxs-lookup"><span data-stu-id="96d4d-104">To use Advanced Group Policy Management (AGPM) to provide change control for a Group Policy object (GPO), you must first control the GPO with AGPM.</span></span>

<span data-ttu-id="96d4d-105">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора (полного доступа) утверждающего или расширенного управления групповыми политиками или необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="96d4d-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="96d4d-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="96d4d-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="96d4d-107">Управление ранее неуправлениым объектом групповой политики</span><span class="sxs-lookup"><span data-stu-id="96d4d-107">To control a previously uncontrolled GPO</span></span>**

1.  <span data-ttu-id="96d4d-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="96d4d-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="96d4d-109">На вкладке **содержание** в области сведений щелкните вкладку **неконтрольные** значения, чтобы отобразить неконтрольные объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="96d4d-109">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="96d4d-110">Щелкните правой кнопкой мыши объект групповой политики, для которого нужно настроить управление групповыми политиками, и выберите пункт **элемент управления**.</span><span class="sxs-lookup"><span data-stu-id="96d4d-110">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="96d4d-111">Введите Примечание, которое будет отображаться в журнале объекта групповой политики, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="96d4d-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="96d4d-112">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="96d4d-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="96d4d-113">Объект групповой политики удаляется из списка на вкладке " **неуправляемый** " и добавляется на вкладку " **управляемые** ".</span><span class="sxs-lookup"><span data-stu-id="96d4d-113">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Controlled** tab.</span></span>

### <span data-ttu-id="96d4d-114">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="96d4d-114">Additional considerations</span></span>

-   <span data-ttu-id="96d4d-115">По умолчанию для выполнения этой процедуры необходимо быть утверждающим или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="96d4d-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="96d4d-116">В частности, необходимо иметь **содержимое списка** и **создать разрешения GPO** для домена.</span><span class="sxs-lookup"><span data-stu-id="96d4d-116">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="96d4d-117">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="96d4d-117">Additional references</span></span>

-   [<span data-ttu-id="96d4d-118">Создание, администрирование и импорт объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="96d4d-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

 

 





