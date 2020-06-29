---
title: Импорт объекта групповой политики из рабочей среды
description: Импорт объекта групповой политики из рабочей среды
author: dansimp
ms.assetid: ffa02b2a-2a43-4fc0-a06e-7d4b59022cc3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 239ac6938645325292bfc647ef89a77710c5f074
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820679"
---
# <span data-ttu-id="43307-103">Импорт объекта групповой политики из рабочей среды</span><span class="sxs-lookup"><span data-stu-id="43307-103">Import a GPO from Production</span></span>


<span data-ttu-id="43307-104">Если изменения вносятся в контролируемый объект групповой политики (GPO) за пределами расширенного управления групповыми политиками, вы можете импортировать его копию из рабочей среды и сохранить ее в архиве, чтобы перевести Архив и производственную среду в устойчивое состояние.</span><span class="sxs-lookup"><span data-stu-id="43307-104">If changes are made to a controlled Group Policy object (GPO) outside of Advanced Group Policy Management (AGPM), you can import a copy of the GPO from the production environment and save it to the archive to bring the archive and the production environment to a consistent state.</span></span> <span data-ttu-id="43307-105">(Чтобы импортировать неподдерживаемый объект групповой политики, контролируйте объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="43307-105">(To import an uncontrolled GPO, control the GPO.</span></span> <span data-ttu-id="43307-106">Дополнительные сведения [о том, как запросить контроль ранее неуправления GPO](request-control-of-a-previously-uncontrolled-gpo.md).)</span><span class="sxs-lookup"><span data-stu-id="43307-106">See [Request Control of a Previously Uncontrolled GPO](request-control-of-a-previously-uncontrolled-gpo.md).)</span></span>

<span data-ttu-id="43307-107">Для выполнения этой процедуры требуется учетная запись пользователя с ролью "редактор", утверждающего или администратором расширенного управления групповыми политиками (полный доступ) или необходимыми разрешениями в расширенном управлении групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="43307-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="43307-108">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="43307-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="43307-109">Импорт объекта групповой политики из рабочей среды</span><span class="sxs-lookup"><span data-stu-id="43307-109">To import a GPO from the production environment</span></span>**

1.  <span data-ttu-id="43307-110">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="43307-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="43307-111">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="43307-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="43307-112">Щелкните объект групповой политики правой кнопкой мыши и выберите команду **Импорт из производства**.</span><span class="sxs-lookup"><span data-stu-id="43307-112">Right-click the GPO, and then click **Import from Production**.</span></span>

4.  <span data-ttu-id="43307-113">Введите Примечание для контрольного следа объекта групповой политики, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="43307-113">Type a comment for the audit trail of the GPO, then click **OK**.</span></span>

### <span data-ttu-id="43307-114">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="43307-114">Additional considerations</span></span>

-   <span data-ttu-id="43307-115">Для выполнения этой процедуры вы должны быть редактором, утверждающим или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="43307-115">By default, you must be an Editor, Approver, or AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="43307-116">В частности, необходимо иметь **содержимое списка** и либо **изменить параметры**, либо **развернуть объект групповой политики**, либо **удалить разрешения GPO** для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="43307-116">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="43307-117">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="43307-117">Additional references</span></span>

-   [<span data-ttu-id="43307-118">Создание, администрирование и импорт объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="43307-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor.md)

 

 





