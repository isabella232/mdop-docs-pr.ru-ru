---
title: Создание нового управляемого объекта групповой политики
description: Создание нового управляемого объекта групповой политики
author: dansimp
ms.assetid: f89eaae8-7858-4222-ba3f-a93a9d7ea5a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d666edf97459a8499ee0f74155473c692d583ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821102"
---
# <span data-ttu-id="256a3-103">Создание нового управляемого объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="256a3-103">Create a New Controlled GPO</span></span>


<span data-ttu-id="256a3-104">Новые объекты групповой политики (GPO), созданные с помощью папки для **управления изменениями** , будут автоматически управляться, что позволяет им работать.</span><span class="sxs-lookup"><span data-stu-id="256a3-104">New Group Policy Objects (GPOs) created through the **Change Control** folder will automatically be controlled, enabling you to manage them.</span></span>

<span data-ttu-id="256a3-105">Для выполнения этой процедуры необходимо использовать учетную запись пользователя с ролью "полный доступ" и "Администратор расширенного управления групповыми политиками (для опытных пользователей)" или необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="256a3-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="256a3-106">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="256a3-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="256a3-107">Создание объекта групповой политики с управлением изменениями с помощью РАСШИРЕНного управления</span><span class="sxs-lookup"><span data-stu-id="256a3-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="256a3-108">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="256a3-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="256a3-109">Щелкните правой кнопкой мыши **изменить элемент управления**, а затем выберите команду **создать управляемый объект групповой политики**.</span><span class="sxs-lookup"><span data-stu-id="256a3-109">Right-click **Change Control**, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="256a3-110">В диалоговом окне **новый управляемый объект групповой политики** :</span><span class="sxs-lookup"><span data-stu-id="256a3-110">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="256a3-111">Введите имя для нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="256a3-111">Type a name for the new GPO.</span></span>

    2.  <span data-ttu-id="256a3-112">Необязательно: введите Примечание для нового объекта групповой политики, которое будет отображаться в **журнале** для объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="256a3-112">Optional: Type a comment for the new GPO to be displayed in the **History** for the GPO.</span></span>

    3.  <span data-ttu-id="256a3-113">Для немедленного развертывания нового объекта групповой политики в рабочей среде нажмите кнопку **создать Live**.</span><span class="sxs-lookup"><span data-stu-id="256a3-113">To immediately deploy the new GPO to the production environment, click **Create live**.</span></span> <span data-ttu-id="256a3-114">Чтобы создать новый объект групповой политики в автономном режиме без немедленного развертывания, выберите команду **создать автономно**.</span><span class="sxs-lookup"><span data-stu-id="256a3-114">To create the new GPO offline without immediately deploying it, click **Create offline**.</span></span>

    4.  <span data-ttu-id="256a3-115">Выберите шаблон GPO, который будет использоваться в качестве отправной точки для нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="256a3-115">Select the GPO template to use as a starting point for the new GPO.</span></span>

    5.  <span data-ttu-id="256a3-116">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="256a3-116">Click **OK**.</span></span>

4.  <span data-ttu-id="256a3-117">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="256a3-117">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="256a3-118">Новый объект групповой политики отображается в списке объектов групповой политики на вкладке " **управляемые** ".</span><span class="sxs-lookup"><span data-stu-id="256a3-118">The new GPO is displayed in the list of GPOs on the **Controlled** tab.</span></span>

### <span data-ttu-id="256a3-119">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="256a3-119">Additional considerations</span></span>

-   <span data-ttu-id="256a3-120">По умолчанию для выполнения этой процедуры необходимо быть утверждающим или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="256a3-120">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="256a3-121">В частности, необходимо иметь **содержимое списка** и **создать разрешения GPO** для домена.</span><span class="sxs-lookup"><span data-stu-id="256a3-121">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="256a3-122">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="256a3-122">Additional references</span></span>

-   [<span data-ttu-id="256a3-123">Создание, администрирование и импорт объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="256a3-123">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 





