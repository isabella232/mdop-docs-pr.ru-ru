---
title: Управление неконтролируемым объектом групповой политики
description: Управление неконтролируемым объектом групповой политики
author: dansimp
ms.assetid: dc81545c-8da5-4b6f-b266-f01a82e27c6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 418e2a4100e1d824198b7d05034443948ec8a44c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818902"
---
# <span data-ttu-id="b9d12-103">Управление неконтролируемым объектом групповой политики</span><span class="sxs-lookup"><span data-stu-id="b9d12-103">Control an Uncontrolled GPO</span></span>


<span data-ttu-id="b9d12-104">Чтобы предоставить управление изменениями для объекта групповой политики (GPO), необходимо сначала управлять этим объектом.</span><span class="sxs-lookup"><span data-stu-id="b9d12-104">To provide change control for a Group Policy Object (GPO), you must first control the GPO.</span></span>

<span data-ttu-id="b9d12-105">Для выполнения этой процедуры необходимо использовать учетную запись пользователя с ролью "полный доступ" и "Администратор расширенного управления групповыми политиками (для опытных пользователей)" или необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="b9d12-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="b9d12-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="b9d12-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="b9d12-107">Управление неподдерживаемым объектом групповой политики</span><span class="sxs-lookup"><span data-stu-id="b9d12-107">To control an uncontrolled GPO</span></span>**

1.  <span data-ttu-id="b9d12-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="b9d12-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="b9d12-109">На вкладке **содержание** в области сведений щелкните вкладку **неконтрольные** значения, чтобы отобразить неконтрольные объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="b9d12-109">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="b9d12-110">Щелкните правой кнопкой мыши объект групповой политики, для которого нужно настроить управление групповыми политиками, и выберите пункт **элемент управления**.</span><span class="sxs-lookup"><span data-stu-id="b9d12-110">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="b9d12-111">Введите Примечание, которое будет отображаться в журнале объекта групповой политики, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b9d12-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="b9d12-112">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="b9d12-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b9d12-113">Объект групповой политики удаляется из списка на вкладке " **неуправляемый** " и добавляется на вкладку " **управляемые** ".</span><span class="sxs-lookup"><span data-stu-id="b9d12-113">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Controlled** tab.</span></span>

### <span data-ttu-id="b9d12-114">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="b9d12-114">Additional considerations</span></span>

-   <span data-ttu-id="b9d12-115">По умолчанию для выполнения этой процедуры необходимо быть утверждающим или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="b9d12-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="b9d12-116">В частности, необходимо иметь **содержимое списка** и **создать разрешения GPO** для домена.</span><span class="sxs-lookup"><span data-stu-id="b9d12-116">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="b9d12-117">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="b9d12-117">Additional references</span></span>

-   [<span data-ttu-id="b9d12-118">Создание и администрирование объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="b9d12-118">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





