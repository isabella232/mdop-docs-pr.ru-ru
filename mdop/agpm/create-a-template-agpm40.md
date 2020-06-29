---
title: Создание шаблона
description: Создание шаблона
author: dansimp
ms.assetid: b38423af-7d24-437a-98bc-01f1ae891127
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd50dd41863e383b931b8563854a8bbd4ee196d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821072"
---
# <span data-ttu-id="96ffa-103">Создание шаблона</span><span class="sxs-lookup"><span data-stu-id="96ffa-103">Create a Template</span></span>


<span data-ttu-id="96ffa-104">Создание шаблона позволяет сохранить все параметры определенной версии объекта групповой политики (GPO), который будет использоваться в качестве отправной точки для создания новых GPO.</span><span class="sxs-lookup"><span data-stu-id="96ffa-104">Creating a template enables you to save all of the settings of a particular version of a Group Policy Object (GPO) to use as a starting point for creating new GPOs.</span></span>

<span data-ttu-id="96ffa-105">**Примечание**  Шаблон — это нередактируемая статическая версия GPO, используемая в качестве отправной точки для создания новых редактируемых GPO.</span><span class="sxs-lookup"><span data-stu-id="96ffa-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="96ffa-106">Для выполнения этой процедуры требуется учетная запись пользователя с ролью редактора или администратора расширенного управления групповыми политиками (полный доступ) или необходимых разрешений в расширенном управлении групповой политикой (ГРУППОВое управление).</span><span class="sxs-lookup"><span data-stu-id="96ffa-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="96ffa-107">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="96ffa-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="96ffa-108">Создание шаблона на основе существующего объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="96ffa-108">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="96ffa-109">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="96ffa-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="96ffa-110">На вкладке **содержание** в области сведений щелкните вкладку **управляемая** или **неуправляемая** , чтобы отобразить доступные объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="96ffa-110">On the **Contents** tab in the details pane, click the **Controlled** or **Uncontrolled** tab to display available GPOs.</span></span>

3.  <span data-ttu-id="96ffa-111">Щелкните правой кнопкой мыши объект групповой политики, из которого вы хотите создать шаблон, и выберите команду **Сохранить как шаблон**.</span><span class="sxs-lookup"><span data-stu-id="96ffa-111">Right-click the GPO from which you want to create a template, and then click **Save as Template**.</span></span>

4.  <span data-ttu-id="96ffa-112">Введите имя шаблона и примечания, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="96ffa-112">Type a name for the template and a comment, and then click **OK**.</span></span>

5.  <span data-ttu-id="96ffa-113">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="96ffa-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="96ffa-114">Новый шаблон появится на вкладке **шаблоны** .</span><span class="sxs-lookup"><span data-stu-id="96ffa-114">The new template appears on the **Templates** tab.</span></span>

### <span data-ttu-id="96ffa-115">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="96ffa-115">Additional considerations</span></span>

-   <span data-ttu-id="96ffa-116">По умолчанию для выполнения этой процедуры необходимо быть редактором или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="96ffa-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="96ffa-117">В частности, необходимо иметь **содержимое списка** и создать для домена разрешения на доступ к **шаблону** .</span><span class="sxs-lookup"><span data-stu-id="96ffa-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="96ffa-118">Переименование или удаление шаблона не влияет на объекты групповой политики, созданные на основе этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="96ffa-118">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="96ffa-119">Поскольку он не может быть изменен, шаблон не имеет истории.</span><span class="sxs-lookup"><span data-stu-id="96ffa-119">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="96ffa-120">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="96ffa-120">Additional references</span></span>

-   [<span data-ttu-id="96ffa-121">Создание шаблона и настройка шаблона по умолчанию</span><span class="sxs-lookup"><span data-stu-id="96ffa-121">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="96ffa-122">Запрос на создание нового управляемого объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="96ffa-122">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo-agpm40.md)

 

 





