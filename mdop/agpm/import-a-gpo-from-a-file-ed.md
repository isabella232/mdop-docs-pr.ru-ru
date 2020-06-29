---
title: Импорт объекта групповой политики из файла
description: Импорт объекта групповой политики из файла
author: dansimp
ms.assetid: 6e901a52-1101-4fed-9f90-3819b573b378
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15704806f089bb0d8530cd84df64b0889413426
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820722"
---
# <span data-ttu-id="f09ab-103">Импорт объекта групповой политики из файла</span><span class="sxs-lookup"><span data-stu-id="f09ab-103">Import a GPO from a File</span></span>


<span data-ttu-id="f09ab-104">Если вы экспортировали объект групповой политики (GPO) в файл CAB, вы можете импортировать параметры политики из этого GPO в существующий объект GPO в другом лесе.</span><span class="sxs-lookup"><span data-stu-id="f09ab-104">In Advanced Group Policy Management (AGPM), if you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="f09ab-105">Импорт параметров политики в существующий объект групповой политики заменяет все параметры политики в этом GPO.</span><span class="sxs-lookup"><span data-stu-id="f09ab-105">Importing policy settings into an existing GPO replaces all policy settings within that GPO.</span></span> <span data-ttu-id="f09ab-106">Сведения об экспорте параметров GPO в CAB-файл можно найти в разделе [Экспорт объекта групповой политики в файл](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="f09ab-106">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="f09ab-107">Для выполнения этой процедуры требуется учетная запись пользователя с ролью редактора или администратора расширенного управления групповыми политиками (полный доступ) или необходимых разрешений в расширенном управлении групповой политикой (ГРУППОВое управление).</span><span class="sxs-lookup"><span data-stu-id="f09ab-107">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="f09ab-108">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="f09ab-108">Review the details in "Additional considerations" in this topic.</span></span>

## <a href="" id="bkmk-existing"></a>


**<span data-ttu-id="f09ab-109">Импорт параметров политики в существующий объект групповой политики</span><span class="sxs-lookup"><span data-stu-id="f09ab-109">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="f09ab-110">В дереве **консоли управления групповыми политиками** нажмите **изменить элемент управления** в домене, в который вы хотите импортировать параметры политики.</span><span class="sxs-lookup"><span data-stu-id="f09ab-110">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="f09ab-111">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="f09ab-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="f09ab-112">Изучите конечный объект групповой политики, в который вы хотите импортировать параметры политики.</span><span class="sxs-lookup"><span data-stu-id="f09ab-112">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="f09ab-113">Щелкните целевой объект групповой политики правой кнопкой мыши, выберите пункт **Импорт из**, а затем — **файл**.</span><span class="sxs-lookup"><span data-stu-id="f09ab-113">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="f09ab-114">Следуйте указаниям **мастера импорта параметров** для выбора резервной копии GPO, импорта параметров политики для замены ее в ЦЕЛЕВОМ объекте GPO и ввода комментария для контрольного GPO целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="f09ab-114">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="f09ab-115">По умолчанию конечный объект GPO возвращается после завершения работы мастера.</span><span class="sxs-lookup"><span data-stu-id="f09ab-115">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="f09ab-116">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="f09ab-116">Additional considerations</span></span>

-   <span data-ttu-id="f09ab-117">По умолчанию для выполнения этой процедуры необходимо быть редактором или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="f09ab-117">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="f09ab-118">В частности, необходимо иметь **содержимое списка**, **изменить параметры**и **импортировать разрешения GPO** для домена, и объект групповой политики должен быть извлечен вами.</span><span class="sxs-lookup"><span data-stu-id="f09ab-118">Specifically, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span>

-   <span data-ttu-id="f09ab-119">Несмотря на то, что редактор не может импортировать параметры политики в новый объект групповой политики во время его создания, редактор может запросить создание нового объекта групповой политики, а затем импортировать в него параметры политики после ее создания.</span><span class="sxs-lookup"><span data-stu-id="f09ab-119">Although an Editor cannot import policy settings into a new GPO during its creation, an Editor can request the creation of a new GPO and then import policy settings into it after it is created.</span></span>

### <span data-ttu-id="f09ab-120">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="f09ab-120">Additional references</span></span>

-   [<span data-ttu-id="f09ab-121">Использование тестовой среды</span><span class="sxs-lookup"><span data-stu-id="f09ab-121">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





