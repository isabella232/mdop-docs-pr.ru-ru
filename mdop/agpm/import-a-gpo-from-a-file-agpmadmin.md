---
title: Импорт объекта групповой политики из файла
description: Импорт объекта групповой политики из файла
author: dansimp
ms.assetid: 2cbcda72-4de3-47ad-aaf8-4fc7341d5a00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 04819dacac8df73f0a61cace0dab8b9fa79b7307
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820752"
---
# <span data-ttu-id="0a809-103">Импорт объекта групповой политики из файла</span><span class="sxs-lookup"><span data-stu-id="0a809-103">Import a GPO from a File</span></span>


<span data-ttu-id="0a809-104">Если вы являетесь администратором расширенного управления групповыми политиками (полный доступ) и вы экспортировали объект групповой политики (GPO) в CAB-файл, вы можете импортировать параметры политики из этого GPO в новый объект групповой политики или существующий GPO в домене другого леса.</span><span class="sxs-lookup"><span data-stu-id="0a809-104">In Advanced Group Policy Management (AGPM), if you are an AGPM Administrator (Full Control) and you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into a new GPO or an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="0a809-105">Сведения об экспорте параметров GPO в CAB-файл можно найти в разделе [Экспорт объекта групповой политики в файл](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="0a809-105">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="0a809-106">Для импорта параметров политики в новый управляемый объект групповой политики требуется учетная запись пользователя с ролью администратора РАСШИРЕНного управления правами или необходимыми разрешениями в РАСШИРЕНном доступе.</span><span class="sxs-lookup"><span data-stu-id="0a809-106">A user account with the AGPM Administrator role or the necessary permissions in AGPM is required to import policy settings into a new controlled GPO.</span></span> <span data-ttu-id="0a809-107">Для импорта параметров политики в существующий объект групповой политики требуется учетная запись пользователя с ролью "редактор" или "Администратор РАСШИРЕНного доступа" или необходимыми разрешениями в РАСШИРЕНном доступе.</span><span class="sxs-lookup"><span data-stu-id="0a809-107">A user account with the Editor or AGPM Administrator role or necessary permissions in AGPM is required to import policy settings into an existing GPO.</span></span> <span data-ttu-id="0a809-108">Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".</span><span class="sxs-lookup"><span data-stu-id="0a809-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="0a809-109">Импорт параметров политики из файла</span><span class="sxs-lookup"><span data-stu-id="0a809-109">Importing policy settings from a file</span></span>


<span data-ttu-id="0a809-110">При импорте параметров политики из файла вы можете импортировать их в новый объект групповой политики или существующий объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="0a809-110">When you import policy settings from a file, you can import them into a new GPO or an existing GPO.</span></span> <span data-ttu-id="0a809-111">Однако при импорте параметров политики в существующий объект групповой политики заменяются все параметры политики, находящиеся в ней.</span><span class="sxs-lookup"><span data-stu-id="0a809-111">However, if you import policy settings into an existing GPO, all policy settings within it are replaced.</span></span>

-   [<span data-ttu-id="0a809-112">Импорт параметров политики в новый управляемый объект групповой политики</span><span class="sxs-lookup"><span data-stu-id="0a809-112">Import policy settings into a new controlled GPO</span></span>](#bkmk-new)

-   [<span data-ttu-id="0a809-113">Импорт параметров политики в существующий объект групповой политики</span><span class="sxs-lookup"><span data-stu-id="0a809-113">Import policy settings into an existing GPO</span></span>](#bkmk-existing)

### <a href="" id="bkmk-new"></a>

**<span data-ttu-id="0a809-114">Импорт параметров политики в новый управляемый объект групповой политики</span><span class="sxs-lookup"><span data-stu-id="0a809-114">To import policy settings into a new controlled GPO</span></span>**

1.  <span data-ttu-id="0a809-115">В дереве **консоли управления групповыми политиками** нажмите **изменить элемент управления** в домене, в который вы хотите импортировать параметры политики.</span><span class="sxs-lookup"><span data-stu-id="0a809-115">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="0a809-116">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="0a809-116">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="0a809-117">Создайте новый управляемый объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="0a809-117">Create a new controlled GPO.</span></span> <span data-ttu-id="0a809-118">В диалоговом окне **новый управляемый объект групповой политики** нажмите кнопку **Импорт** , а затем выберите команду **запустить мастер**.</span><span class="sxs-lookup"><span data-stu-id="0a809-118">In the **New Controlled GPO** dialog box, click **Import** and then click **Launch Wizard**.</span></span> <span data-ttu-id="0a809-119">Дополнительные сведения о том, как создать объект групповой политики, можно найти в разделе [Создание нового объекта групповой политики](create-a-new-controlled-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="0a809-119">For more information about how to create a GPO, see [Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md).</span></span>

4.  <span data-ttu-id="0a809-120">Следуйте инструкциям **мастера импорта параметров** для выбора резервной копии GPO, импорта параметров политики из нее для нового объекта групповой политики и ввода комментария для журнала аудита нового объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="0a809-120">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import policy settings from it for the new GPO, and enter a comment for the audit trail of the new GPO.</span></span>

### <a href="" id="bkmk-existing"></a>

**<span data-ttu-id="0a809-121">Импорт параметров политики в существующий объект групповой политики</span><span class="sxs-lookup"><span data-stu-id="0a809-121">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="0a809-122">В дереве **консоли управления групповыми политиками** нажмите **изменить элемент управления** в домене, в который вы хотите импортировать параметры политики.</span><span class="sxs-lookup"><span data-stu-id="0a809-122">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="0a809-123">На вкладке **содержание** откройте вкладку **Управление** , чтобы отобразить управляемые объекты групповой политики.</span><span class="sxs-lookup"><span data-stu-id="0a809-123">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="0a809-124">Изучите конечный объект групповой политики, в который вы хотите импортировать параметры политики.</span><span class="sxs-lookup"><span data-stu-id="0a809-124">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="0a809-125">Щелкните целевой объект групповой политики правой кнопкой мыши, выберите пункт **Импорт из**, а затем — **файл**.</span><span class="sxs-lookup"><span data-stu-id="0a809-125">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="0a809-126">Следуйте указаниям **мастера импорта параметров** для выбора резервной копии GPO, импорта параметров политики для замены ее в ЦЕЛЕВОМ объекте GPO и ввода комментария для контрольного GPO целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="0a809-126">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="0a809-127">По умолчанию конечный объект GPO возвращается после завершения работы мастера.</span><span class="sxs-lookup"><span data-stu-id="0a809-127">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="0a809-128">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="0a809-128">Additional considerations</span></span>

-   <span data-ttu-id="0a809-129">Для импорта параметров политики в новый управляемый объект групповой политики необходимо иметь **содержимое списка**, **импортировать GPO**и **создавать разрешения GPO** для домена.</span><span class="sxs-lookup"><span data-stu-id="0a809-129">To import policy settings to a new controlled GPO, you must have **List Contents**, **Import GPO**, and **Create GPO** permissions for the domain.</span></span> <span data-ttu-id="0a809-130">По умолчанию для выполнения этой процедуры необходимы права администратора РАСШИРЕНного администрирования.</span><span class="sxs-lookup"><span data-stu-id="0a809-130">By default, you must be an AGPM Administrator to perform this procedure.</span></span>

-   <span data-ttu-id="0a809-131">Для импорта параметров политики в существующий объект групповой политики необходимо иметь **содержимое списка**, **изменить параметры**и импортировать разрешения **GPO** для домена, и этот GPO должен быть извлечен вами.</span><span class="sxs-lookup"><span data-stu-id="0a809-131">To import policy settings to an existing GPO, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span> <span data-ttu-id="0a809-132">По умолчанию для выполнения этой процедуры необходимо быть редактором или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="0a809-132">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span>

### <span data-ttu-id="0a809-133">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="0a809-133">Additional references</span></span>

-   [<span data-ttu-id="0a809-134">Управление архивами</span><span class="sxs-lookup"><span data-stu-id="0a809-134">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





