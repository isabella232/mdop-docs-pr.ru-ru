---
title: Импорт объекта групповой политики из рабочей среды
description: Импорт объекта групповой политики из рабочей среды
author: dansimp
ms.assetid: c5b2f40d-1dc7-4dbf-b8b3-4d97ad73e1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea01341e13696f8b06f22e3f352034b60a713f8a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820709"
---
# <span data-ttu-id="29a24-103">Импорт объекта групповой политики из рабочей среды</span><span class="sxs-lookup"><span data-stu-id="29a24-103">Import a GPO from Production</span></span>


<span data-ttu-id="29a24-104">Если изменения вносятся в контролируемый объект групповой политики (GPO) за пределами расширенного управления групповыми политиками, вы можете импортировать ее копию из рабочей среды домена и сохранить ее в архиве, чтобы перевести архивную и производственную среду в устойчивое состояние.</span><span class="sxs-lookup"><span data-stu-id="29a24-104">If changes are made to a controlled Group Policy Object (GPO) outside of Advanced Group Policy Management (AGPM), you can import a copy of the GPO from the production environment of the domain and save it to the archive to bring the archive and the production environment to a consistent state.</span></span> <span data-ttu-id="29a24-105">(Чтобы импортировать неподдерживаемый объект групповой политики, контролируйте объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="29a24-105">(To import an uncontrolled GPO, control the GPO.</span></span> <span data-ttu-id="29a24-106">См.: [Управление неподдерживаемым объектом групповой политики](control-an-uncontrolled-gpo-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="29a24-106">See [Control an Uncontrolled GPO](control-an-uncontrolled-gpo-agpm40.md).)</span></span>

<span data-ttu-id="29a24-107">Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора, утверждающего или расширенного управления групповыми политиками (полного доступа) или необходимых разрешений.</span><span class="sxs-lookup"><span data-stu-id="29a24-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions inAGPM is required to complete this procedure.</span></span> <span data-ttu-id="29a24-108">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="29a24-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="29a24-109">Импорт объекта групповой политики из рабочей среды домена</span><span class="sxs-lookup"><span data-stu-id="29a24-109">To import a GPO from the production environment of the domain</span></span>**

1.  <span data-ttu-id="29a24-110">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="29a24-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="29a24-111">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="29a24-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="29a24-112">Щелкните объект групповой политики правой кнопкой мыши и выберите команду **Импорт из производства**.</span><span class="sxs-lookup"><span data-stu-id="29a24-112">Right-click the GPO, and then click **Import from Production**.</span></span>

4.  <span data-ttu-id="29a24-113">Введите Примечание для контрольного следа объекта групповой политики, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="29a24-113">Type a comment for the audit trail of the GPO, and then click **OK**.</span></span>

### <span data-ttu-id="29a24-114">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="29a24-114">Additional considerations</span></span>

-   <span data-ttu-id="29a24-115">Для выполнения этой процедуры вы должны быть редактором, утверждающим или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="29a24-115">By default, you must be an Editor, Approver, or AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="29a24-116">В частности, необходимо иметь **содержимое списка** и либо **изменить параметры**, либо **развернуть объект групповой политики**, либо **удалить разрешения GPO** для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="29a24-116">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="29a24-117">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="29a24-117">Additional references</span></span>

-   [<span data-ttu-id="29a24-118">Создание и администрирование объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="29a24-118">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





