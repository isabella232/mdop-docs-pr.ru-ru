---
title: Настройка шаблона по умолчанию
description: Настройка шаблона по умолчанию
author: dansimp
ms.assetid: e0acf980-437f-4357-b237-298aaebe490d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 870c1d4c13049992509f6aa831966736e6ba25ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820229"
---
# <span data-ttu-id="48f30-103">Настройка шаблона по умолчанию</span><span class="sxs-lookup"><span data-stu-id="48f30-103">Set a Default Template</span></span>


<span data-ttu-id="48f30-104">Как редактор вы можете указать, какие из доступных шаблонов будут предлагаться для всех администраторов групповой политики, которые создают новые объекты групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="48f30-104">As an Editor, you can specify which of the available templates will be the default template suggested for all Group Policy administrators creating new Group Policy objects (GPOs).</span></span>

<span data-ttu-id="48f30-105">**Примечание**  Шаблон — это нередактируемая статическая версия GPO, используемая в качестве отправной точки для создания новых редактируемых GPO.</span><span class="sxs-lookup"><span data-stu-id="48f30-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="48f30-106">Для выполнения этой процедуры требуется учетная запись пользователя с ролью редактора или администратора расширенного управления групповыми политиками (полный доступ) или необходимых разрешений в расширенном управлении групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="48f30-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="48f30-107">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="48f30-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="48f30-108">Настройка шаблона по умолчанию для создания новых объектов групповой политики</span><span class="sxs-lookup"><span data-stu-id="48f30-108">To set the default template for use when creating new GPOs</span></span>**

1.  <span data-ttu-id="48f30-109">В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.</span><span class="sxs-lookup"><span data-stu-id="48f30-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="48f30-110">На вкладке **содержание** в области сведений откройте вкладку **шаблоны** , чтобы просмотреть доступные шаблоны.</span><span class="sxs-lookup"><span data-stu-id="48f30-110">On the **Contents** tab in the details pane, click the **Templates** tab to display available templates.</span></span>

3.  <span data-ttu-id="48f30-111">Щелкните правой кнопкой мыши шаблон, который вы хотите использовать по умолчанию, и выберите команду **по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="48f30-111">Right-click the template that you want to set as the default, and then click **Set as Default**.</span></span>

4.  <span data-ttu-id="48f30-112">Нажмите кнопку **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="48f30-112">Click **Yes** to confirm.</span></span>

5.  <span data-ttu-id="48f30-113">После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="48f30-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="48f30-114">В шаблоне по умолчанию есть синий значок, а состояние — **шаблон (по умолчанию)** на вкладке **шаблоны** .</span><span class="sxs-lookup"><span data-stu-id="48f30-114">The default template has a blue icon and the state is identified as **Template (default)** on the **Templates** tab.</span></span>

### <span data-ttu-id="48f30-115">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="48f30-115">Additional considerations</span></span>

-   <span data-ttu-id="48f30-116">По умолчанию для выполнения этой процедуры необходимо быть редактором или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="48f30-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="48f30-117">В частности, необходимо иметь **содержимое списка** и создать для домена разрешения на доступ к **шаблону** .</span><span class="sxs-lookup"><span data-stu-id="48f30-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="48f30-118">После того как вы настроили шаблон в качестве шаблона по умолчанию, этот шаблон будет выбран в диалоговом окне **новый управляемый объект групповой** политики, когда администраторы групповых политик создают новые GPO.</span><span class="sxs-lookup"><span data-stu-id="48f30-118">After you set a template as the default, that template will be the one initially selected in the **New Controlled GPO** dialog box when Group Policy administrators create new GPOs.</span></span> <span data-ttu-id="48f30-119">Однако они будут иметь возможность выбрать любой другой шаблон GPO, включая \*\* &lt; пустой объект групповой &gt; \*\*политики, в который не включаются никакие параметры.</span><span class="sxs-lookup"><span data-stu-id="48f30-119">However, they will have the option to select any other GPO template, including **&lt;Empty GPO&gt;**, which does not include any settings.</span></span>

-   <span data-ttu-id="48f30-120">Переименование или удаление шаблона не влияет на объекты групповой политики, созданные на основе этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="48f30-120">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="48f30-121">Поскольку он не может быть изменен, шаблон не имеет истории.</span><span class="sxs-lookup"><span data-stu-id="48f30-121">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="48f30-122">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="48f30-122">Additional references</span></span>

-   [<span data-ttu-id="48f30-123">Создание шаблона и настройка шаблона по умолчанию</span><span class="sxs-lookup"><span data-stu-id="48f30-123">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template.md)

-   [<span data-ttu-id="48f30-124">Запрос на создание нового управляемого объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="48f30-124">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo.md)

 

 





