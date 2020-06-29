---
title: Поиск и фильтрация списка объектов групповой политики
description: Поиск и фильтрация списка объектов групповой политики
author: dansimp
ms.assetid: 1bc58a38-033c-4aed-9eb4-c239827f5501
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5646a51a37a4ca9195fb9ef858e8c5920ca7738a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820262"
---
# <span data-ttu-id="b4549-103">Поиск и фильтрация списка объектов групповой политики</span><span class="sxs-lookup"><span data-stu-id="b4549-103">Search and Filter the List of GPOs</span></span>


<span data-ttu-id="b4549-104">С помощью расширенного управления групповыми политиками вы можете выполнить поиск по списку объектов групповой политики (GPO) и их атрибутов, чтобы отфильтровать список объектов GPO.</span><span class="sxs-lookup"><span data-stu-id="b4549-104">In Advanced Group Policy Management (AGPM), you can search the list of Group Policy Objects (GPOs) and their attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="b4549-105">Например, можно выполнить поиск объектов групповой политики с определенным именем, состоянием или примечанием.</span><span class="sxs-lookup"><span data-stu-id="b4549-105">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="b4549-106">Вы также можете искать объекты GPO, которые были изменены администратором групповой политики или определенной датой.</span><span class="sxs-lookup"><span data-stu-id="b4549-106">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

## <span data-ttu-id="b4549-107">Выполнение сложного поиска</span><span class="sxs-lookup"><span data-stu-id="b4549-107">Performing a complex search</span></span>


<span data-ttu-id="b4549-108">Вы можете выполнить сложный поиск с помощью атрибута "GPO" формата *1: строка поиска 1 атрибут GPO 2: Поиск строки 2... строки поиска по всем столбцам*.</span><span class="sxs-lookup"><span data-stu-id="b4549-108">You can perform a complex search by using the format *GPO attribute 1: search string 1 GPO attribute 2: search string 2…all-column search strings*.</span></span> <span data-ttu-id="b4549-109">При поиске не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="b4549-109">The search is not case-sensitive.</span></span>

-   <span data-ttu-id="b4549-110">**Атрибут GPO:** Заголовок любого столбца в списке объектов групповой политики в РАСШИРЕНном наборе, кроме **версии компьютера** или **пользователя**.</span><span class="sxs-lookup"><span data-stu-id="b4549-110">**GPO attribute:** Any column heading in the list of GPOs in AGPM other than **Computer Version** or **User Version**.</span></span> <span data-ttu-id="b4549-111">Атрибуты GPO включают имя GPO, состояние, пользователя, который последним изменил объект групповой политики, дату и время последнего изменения объекта групповой политики, Примечание, состояние GPO и фильтр WMI, примененный к объекту групповой политики.</span><span class="sxs-lookup"><span data-stu-id="b4549-111">GPO attributes include the GPO name, state, user who most recently changed the GPO, date and time when the GPO was most recently changed, comment, GPO status, and WMI filter applied to the GPO.</span></span>

-   <span data-ttu-id="b4549-112">**Строка поиска:** Текст, для которого нужно выполнить поиск в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="b4549-112">**Search string:** Text for which to search in the specified column.</span></span> <span data-ttu-id="b4549-113">Если строка содержит пробелы, ее необходимо заключить в кавычки.</span><span class="sxs-lookup"><span data-stu-id="b4549-113">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

-   <span data-ttu-id="b4549-114">**Строки для поиска по столбцам:** Текст, для которого нужно выполнить поиск во всех столбцах списка (GPO), кроме **версии компьютера** и **пользовательской версии**.</span><span class="sxs-lookup"><span data-stu-id="b4549-114">**All-column search strings:** Text for which to search in all columns in the list of GPOs in AGPM other than **Computer Version** and **User Version**.</span></span> <span data-ttu-id="b4549-115">Вы можете добавить несколько строк, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="b4549-115">You can include multiple strings separated by spaces.</span></span> <span data-ttu-id="b4549-116">Если строка содержит пробелы, ее необходимо заключить в кавычки.</span><span class="sxs-lookup"><span data-stu-id="b4549-116">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

<span data-ttu-id="b4549-117">Каждый атрибут GPO и пара строк поиска и каждая строка поиска по столбцу объединяются с помощью логической операции и.</span><span class="sxs-lookup"><span data-stu-id="b4549-117">Each GPO attribute and search string pair and each all-column search string are combined by using a logical AND operation.</span></span> <span data-ttu-id="b4549-118">Результат представляет собой список всех GPO, каждый из которых содержит указанную строку поиска и для которых все строки поиска по столбцам отображаются хотя бы в одном столбце.</span><span class="sxs-lookup"><span data-stu-id="b4549-118">The result is a list of all GPOs for which each specified attribute includes the specified search string and for which any all-column search strings appear in at least one column.</span></span> <span data-ttu-id="b4549-119">Поиск возвращает все частично найденные совпадения для строк, чтобы можно было ввести часть имени или имени объекта групповой политики, а также просмотреть список всех GPO, содержащих этот текст в имени.</span><span class="sxs-lookup"><span data-stu-id="b4549-119">The search returns any partial matches for strings so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="b4549-120">Ниже приведены примеры поиска.</span><span class="sxs-lookup"><span data-stu-id="b4549-120">The following are examples of searches:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b4549-121">Описание результата поиска</span><span class="sxs-lookup"><span data-stu-id="b4549-121">Description of search result</span></span></th>
<th align="left"><span data-ttu-id="b4549-122">Поисковый запрос</span><span class="sxs-lookup"><span data-stu-id="b4549-122">Search query</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4549-123">Все GPO, имена которых включают в себя <strong> Безопасность текста </strong> и <strong> Северная Америка </strong> .</span><span class="sxs-lookup"><span data-stu-id="b4549-123">All GPOs with names that include the text <strong>security</strong> and <strong>North America</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="b4549-124">Имя: </strong><strong> </strong><strong> имя безопасности: </strong> &quot; <strong> Северная Америка</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="b4549-124">name:</strong><strong>security</strong><strong>name:</strong>&quot;<strong>North America</strong>&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4549-125">Все извлеченные объекты GPO.</span><span class="sxs-lookup"><span data-stu-id="b4549-125">All checked out GPOs.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="b4549-126">состояние: </strong> &quot; <strong> извлечено</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="b4549-126">state:</strong>&quot;<strong>checked out</strong>&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4549-127">Все GPO, недавно измененные пользователем <strong> администратора </strong> , и недавно измененные в предыдущем месяце.</span><span class="sxs-lookup"><span data-stu-id="b4549-127">All GPOs most recently changed by the user named <strong>Administrator</strong> and most recently changed within the previous month.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="b4549-128">Кем изменено </strong><strong> : </strong><strong> Дата изменения администратора: </strong><strong> lastmonth</span><span class="sxs-lookup"><span data-stu-id="b4549-128">changed by:</strong><strong>Administrator</strong><strong>change date:</strong><strong>lastmonth</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4549-129">Все объекты групповой политики, в которых <strong> брандмауэр Word </strong> входит в последнее примечание и в котором <strong> отображается безопасность Word </strong> в любом столбце.</span><span class="sxs-lookup"><span data-stu-id="b4549-129">All GPOs in which the word <strong>firewall</strong> is included in the most recent comment and in which the word <strong>security</strong> appears in any column.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="b4549-130">Примечание: </strong><strong> </strong><strong> Безопасность брандмауэра</span><span class="sxs-lookup"><span data-stu-id="b4549-130">comment:</strong><strong>firewall</strong><strong>security</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4549-131">Все GPO, у которых есть состояние " <strong> отключено все параметры" </strong> .</span><span class="sxs-lookup"><span data-stu-id="b4549-131">All GPOs that have a status of <strong>All Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="b4549-132">состояние объекта групповой политики: </strong><strong> все</span><span class="sxs-lookup"><span data-stu-id="b4549-132">gpo status:</strong><strong>all</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4549-133">Все GPO, к которым применен фильтр WMI с именем " <strong> Мой фильтр WMI" </strong> и которые имеют состояние " <strong> Параметры конфигурации пользователя" отключены </strong> .</span><span class="sxs-lookup"><span data-stu-id="b4549-133">All GPOs that have a WMI filter named <strong>My WMI Filter</strong> applied and that have a status of <strong>User Configuration Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="b4549-134">фильтр WMI: </strong> &quot; <strong> состояние GPO «мой фильтр WMI» </strong> &quot; <strong> : </strong><strong> пользователь</span><span class="sxs-lookup"><span data-stu-id="b4549-134">wmi filter:</strong>&quot;<strong>My WMI Filter</strong>&quot;<strong>gpo status:</strong><strong>user</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b4549-135">Указание дат</span><span class="sxs-lookup"><span data-stu-id="b4549-135">Specifying dates</span></span>


<span data-ttu-id="b4549-136">Вы можете выполнять поиск объектов групповой политики, измененных на определенную дату, в определенное время или в течение интервала времени, используя те же специальные условия, доступные при поиске в Windows.</span><span class="sxs-lookup"><span data-stu-id="b4549-136">You can search for GPOs changed on a specific date, at a specific time, or during a span of time by using the same special terms available when you search in Windows.</span></span> <span data-ttu-id="b4549-137">Если вы вводите определенную дату или время, необходимо использовать формат, который используется в столбце **изменить дату** .</span><span class="sxs-lookup"><span data-stu-id="b4549-137">If entering a specific date or time, you must use the format that is used in the **Change Date** column.</span></span> <span data-ttu-id="b4549-138">Ниже приведены примеры операций поиска в столбце " **Дата изменения** ".</span><span class="sxs-lookup"><span data-stu-id="b4549-138">The following are examples of searches of the **Change Date** column:</span></span>

-   <span data-ttu-id="b4549-139">**Дата изменения:\*\*\*\*10/10/2009**</span><span class="sxs-lookup"><span data-stu-id="b4549-139">**change date:\*\*\*\*10/10/2009**</span></span>

-   <span data-ttu-id="b4549-140">**Дата изменения:\*\*\*\*10/10/2009 9:00:00 AM**</span><span class="sxs-lookup"><span data-stu-id="b4549-140">**change date:\*\*\*\*10/10/2009 9:00:00 AM**</span></span>

-   <span data-ttu-id="b4549-141">**Дата изменения:\*\*\*\*thisweek**</span><span class="sxs-lookup"><span data-stu-id="b4549-141">**change date:\*\*\*\*thisweek**</span></span>

<span data-ttu-id="b4549-142">При поиске в столбце " **Дата изменения** " можно использовать следующие специальные условия, не учитывающие регистр.</span><span class="sxs-lookup"><span data-stu-id="b4549-142">You can use the following special terms, which are not case-sensitive, when you search the **Change Date** column:</span></span>

-   **<span data-ttu-id="b4549-143">Сегодня</span><span class="sxs-lookup"><span data-stu-id="b4549-143">Today</span></span>**

-   **<span data-ttu-id="b4549-144">Вчера</span><span class="sxs-lookup"><span data-stu-id="b4549-144">Yesterday</span></span>**

-   **<span data-ttu-id="b4549-145">ThisWeek</span><span class="sxs-lookup"><span data-stu-id="b4549-145">ThisWeek</span></span>**

-   **<span data-ttu-id="b4549-146">LastWeek</span><span class="sxs-lookup"><span data-stu-id="b4549-146">LastWeek</span></span>**

-   **<span data-ttu-id="b4549-147">ThisMonth</span><span class="sxs-lookup"><span data-stu-id="b4549-147">ThisMonth</span></span>**

-   **<span data-ttu-id="b4549-148">LastMonth</span><span class="sxs-lookup"><span data-stu-id="b4549-148">LastMonth</span></span>**

-   **<span data-ttu-id="b4549-149">TwoMonths (Два месяца)</span><span class="sxs-lookup"><span data-stu-id="b4549-149">TwoMonths</span></span>**

-   **<span data-ttu-id="b4549-150">ThreeMonths (Три месяца)</span><span class="sxs-lookup"><span data-stu-id="b4549-150">ThreeMonths</span></span>**

-   **<span data-ttu-id="b4549-151">ThisYear</span><span class="sxs-lookup"><span data-stu-id="b4549-151">ThisYear</span></span>**

-   **<span data-ttu-id="b4549-152">LastYear</span><span class="sxs-lookup"><span data-stu-id="b4549-152">LastYear</span></span>**

### <span data-ttu-id="b4549-153">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="b4549-153">Additional considerations</span></span>

-   <span data-ttu-id="b4549-154">По умолчанию для выполнения этой процедуры необходимо быть рецензентом, редактором, утверждающим или администратором расширенного управления групповыми политиками (полный доступ).</span><span class="sxs-lookup"><span data-stu-id="b4549-154">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="b4549-155">В частности, для домена требуется разрешение на доступ к **содержимому списка** .</span><span class="sxs-lookup"><span data-stu-id="b4549-155">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="b4549-156">Дополнительные сведения об атрибутах GPO можно найти в статьях [вкладка содержание](contents-tab-features-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="b4549-156">For more information about GPO attributes, see [Contents Tab Features](contents-tab-features-agpm40.md).</span></span>

### <span data-ttu-id="b4549-157">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="b4549-157">Additional references</span></span>

-   [<span data-ttu-id="b4549-158">Средство расширенного управления групповыми политиками 4.0</span><span class="sxs-lookup"><span data-stu-id="b4549-158">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





