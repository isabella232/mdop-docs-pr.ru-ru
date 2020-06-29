---
title: Создание отчетов
description: Создание отчетов
author: dansimp
ms.assetid: 9f8ba28e-1993-4c11-a28a-493718051e5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 930b7061d3e5e2fb9951d45b1422915836cbc00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826992"
---
# <span data-ttu-id="cdbe5-103">Создание отчетов</span><span class="sxs-lookup"><span data-stu-id="cdbe5-103">How to Generate Reports</span></span>


<span data-ttu-id="cdbe5-104">Администраторы в MED-V могут создавать следующие типы отчетов.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-104">The following report types can be created by administrators in MED-V:</span></span>

-   <span data-ttu-id="cdbe5-105">[Status (состояние](#bkmk-generatingastatusreport)) — используйте отчет о состоянии, чтобы просмотреть текущее состояние всех активных пользователей и всех рабочих областей MED-V для каждого пользователя на основе определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-105">[Status](#bkmk-generatingastatusreport)—Use the status report to review the current status of all active users and all MED-V workspaces of each user based on a defined period of time.</span></span> <span data-ttu-id="cdbe5-106">Сюда входит Просмотр компьютеров, которые в настоящее время подключены к серверу, или Дата и время последнего подключения к серверу, состояние каждого компьютера и другие необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-106">This includes viewing computers that are currently connected to the server or, if they are not currently connected, the date and time they were last connected to the server, the status of each computer, and other relevant information.</span></span>

-   <span data-ttu-id="cdbe5-107">[Журнал активности](#bkmk-generatinganactivitylogreport)— этот отчет используется для просмотра событий, исходящих от определенного узла или пользователя, в определенном диапазоне дат.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-107">[Activity Log](#bkmk-generatinganactivitylogreport)—Use this report to review events that originated from a specific host or user in a defined date range.</span></span>

-   <span data-ttu-id="cdbe5-108">[Журнал ошибок](#bkmk-generatinganerrorlogreport)— этот отчет используется для просмотра ошибок, происходящих с определенного узла или пользователя в определенном диапазоне дат.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-108">[Error Log](#bkmk-generatinganerrorlogreport)—Use this report to view errors that originated from a specific host or user in a defined date range.</span></span>

<span data-ttu-id="cdbe5-109">Результаты отчета можно сортировать по любому столбцу, щелкнув соответствующее имя столбца.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-109">The report results can be sorted by any column by clicking the appropriate column name.</span></span>

<span data-ttu-id="cdbe5-110">Результаты отчета можно сгруппировать, перетащив заголовок столбца в верхнюю часть отчета.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-110">The report results can be grouped by dragging a column header to the top of the report.</span></span> <span data-ttu-id="cdbe5-111">Перетащите несколько заголовков столбцов, чтобы сгруппировать один столбец после другого.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-111">Drag multiple column headers to group one column after another.</span></span>

## <a href="" id="bkmk-generatingastatusreport"></a><span data-ttu-id="cdbe5-112">Создание отчета о состоянии</span><span class="sxs-lookup"><span data-stu-id="cdbe5-112">How to Generate a Status Report</span></span>


**<span data-ttu-id="cdbe5-113">Создание отчета о состоянии</span><span class="sxs-lookup"><span data-stu-id="cdbe5-113">To generate a status report</span></span>**

1.  <span data-ttu-id="cdbe5-114">Нажмите кнопку Управление **отчетами** .</span><span class="sxs-lookup"><span data-stu-id="cdbe5-114">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="cdbe5-115">В модуле **отчеты** в меню **типы отчетов** выберите **состояние**, а затем — **создать**.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-115">In the **Reports** module, on the **Report Types** menu, select **Status**, and click **Generate**.</span></span>

    <span data-ttu-id="cdbe5-116">Откроется диалоговое окно "Параметры отчета".</span><span class="sxs-lookup"><span data-stu-id="cdbe5-116">The Report Parameters dialog box appears.</span></span>

3.  <span data-ttu-id="cdbe5-117">В диалоговом окне **Параметры отчета** в поле **число дней** введите число или используйте стрелки, чтобы указать количество дней, которые нужно включить в отчет о состоянии, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-117">In the **Report Parameters** dialog box, in the **Number of days** field, enter a number or use the arrows to select the number of days to include in the status report, and click **OK**.</span></span>

    <span data-ttu-id="cdbe5-118">Создается отчет о состоянии.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-118">A status report is generated.</span></span> <span data-ttu-id="cdbe5-119">Параметры отчета описаны в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-119">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="cdbe5-120">Свойства рабочей области для клиента в MED-V</span><span class="sxs-lookup"><span data-stu-id="cdbe5-120">Client MED-V Workspace Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cdbe5-121">Свойство</span><span class="sxs-lookup"><span data-stu-id="cdbe5-121">Property</span></span></th>
<th align="left"><span data-ttu-id="cdbe5-122">Описание</span><span class="sxs-lookup"><span data-stu-id="cdbe5-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-123">Время</span><span class="sxs-lookup"><span data-stu-id="cdbe5-123">Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-124">Дата и время возникновения события.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-124">The date and time the event occurred.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="cdbe5-125">Примечание.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-125">Note</span></span></strong><br/><p><span data-ttu-id="cdbe5-126">По умолчанию события отображаются в порядке убывания дат.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-126">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="cdbe5-127">Однако его можно изменить, щелкнув столбец время получения.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-127">However, it can be changed by clicking the Time Received column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-128">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="cdbe5-128">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-129">Пользователь, который инициировал событие.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-129">The user who initiated the event.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="cdbe5-130">Примечание.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-130">Note</span></span></strong><br/><p><span data-ttu-id="cdbe5-131">Если событие произошло до того, как пользователь вошел в систему, имя пользователя — SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-131">If the event occurred before a user logged on, the user name is SYSTEM.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-132">Имя узла</span><span class="sxs-lookup"><span data-stu-id="cdbe5-132">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-133">Имя главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-133">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-134">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="cdbe5-134">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-135">Имя рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-135">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-136">Имя компьютера рабочей области</span><span class="sxs-lookup"><span data-stu-id="cdbe5-136">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-137">Имя компьютера, на котором запущена Рабочая область MED-V.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-137">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-138">Online</span><span class="sxs-lookup"><span data-stu-id="cdbe5-138">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-139">Текущее состояние клиентского компьютера:</span><span class="sxs-lookup"><span data-stu-id="cdbe5-139">The current state of the client computer:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="cdbe5-140">Прекращена</span><span class="sxs-lookup"><span data-stu-id="cdbe5-140">Stopped</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="cdbe5-141">Начато в &lt; день и время начала рабочей области&gt;</span><span class="sxs-lookup"><span data-stu-id="cdbe5-141">Started at &lt;date and time the workspace was started&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-142">Версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdbe5-142">Client Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-143">Номер версии клиента.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-143">The version number of the client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-144">Версия политики</span><span class="sxs-lookup"><span data-stu-id="cdbe5-144">Policy Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-145">Версия политики, в которой в настоящее время используется рабочая область MED-V.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-145">The policy version that the MED-V workspace is currently using.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-146">Имя изображения</span><span class="sxs-lookup"><span data-stu-id="cdbe5-146">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-147">Имя изображения.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-147">The name of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-148">Версия изображения</span><span class="sxs-lookup"><span data-stu-id="cdbe5-148">Image Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-149">Версия изображения, используемая в настоящее время рабочей областью MED-V.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-149">The image version that the MED-V workspace is currently using.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="cdbe5-150">Примечание.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-150">Note</span></span></strong><br/><p><span data-ttu-id="cdbe5-151">Версия рабочей области для MED-V может быть неизвестной, если она еще не загружена на компьютер.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-151">MED-V workspace version can be Unknown if it has not yet been downloaded onto a computer.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganactivitylogreport"></a><span data-ttu-id="cdbe5-152">Создание отчета по журналу активности</span><span class="sxs-lookup"><span data-stu-id="cdbe5-152">How to Generate an Activity Log Report</span></span>


**<span data-ttu-id="cdbe5-153">Создание отчета по журналу активности</span><span class="sxs-lookup"><span data-stu-id="cdbe5-153">To generate an activity log report</span></span>**

1.  <span data-ttu-id="cdbe5-154">Нажмите кнопку Управление **отчетами** .</span><span class="sxs-lookup"><span data-stu-id="cdbe5-154">Click the **Reports** management button.</span></span>

    <span data-ttu-id="cdbe5-155">Откроется модуль отчеты.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-155">The Reports module appears.</span></span>

2.  <span data-ttu-id="cdbe5-156">В модуле **отчеты** в меню **типы отчетов** выберите пункт **Журнал активности**и нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-156">In the **Reports** module, on the **Report Types** menu, select **Activity Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="cdbe5-157">В диалоговом окне **Параметры отчета** настройте один или несколько из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="cdbe5-157">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="cdbe5-158">**Количество**дней — количество дней, отображаемых в отчете.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-158">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="cdbe5-159">**Имя пользователя содержит**— любое событие, в котором имя пользователя содержит введенный текст, включается в отчет.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-159">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="cdbe5-160">**Имя узла содержит**— любое событие, в котором имя узла содержит введенный текст, включается в отчет.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-160">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="cdbe5-161">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-161">Click **OK**.</span></span>

    <span data-ttu-id="cdbe5-162">Создается отчет с выбранными событиями и датами.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-162">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="cdbe5-163">Параметры отчета описаны в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-163">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="cdbe5-164">Свойства отчета журнала активности</span><span class="sxs-lookup"><span data-stu-id="cdbe5-164">Activity Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cdbe5-165">Свойство</span><span class="sxs-lookup"><span data-stu-id="cdbe5-165">Property</span></span></th>
<th align="left"><span data-ttu-id="cdbe5-166">Описание</span><span class="sxs-lookup"><span data-stu-id="cdbe5-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-167">Идентификатор события</span><span class="sxs-lookup"><span data-stu-id="cdbe5-167">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-168">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-168">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-169">Серьезность</span><span class="sxs-lookup"><span data-stu-id="cdbe5-169">Severity</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="cdbe5-170">Информация, ошибка, предупреждение</span><span class="sxs-lookup"><span data-stu-id="cdbe5-170">Information, Error, Warning</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-171">Категория</span><span class="sxs-lookup"><span data-stu-id="cdbe5-171">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-172">Модуль, на который ссылается отчет.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-172">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-173">Описание</span><span class="sxs-lookup"><span data-stu-id="cdbe5-173">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-174">Описание события.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-174">A description of the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-175">Время получения</span><span class="sxs-lookup"><span data-stu-id="cdbe5-175">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-176">Дата и время получения события на сервере.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-176">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="cdbe5-177">Примечание.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-177">Note</span></span></strong><br/><p><span data-ttu-id="cdbe5-178">Если клиент работает в автономном режиме, сервер получает отчеты, когда клиент подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-178">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="cdbe5-179">Примечание.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-179">Note</span></span></strong><br/><p><span data-ttu-id="cdbe5-180">По умолчанию события отображаются в порядке убывания дат.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-180">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="cdbe5-181">Однако его можно изменить, щелкнув <strong> столбец время получения </strong> .</span><span class="sxs-lookup"><span data-stu-id="cdbe5-181">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-182">Время клиента</span><span class="sxs-lookup"><span data-stu-id="cdbe5-182">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-183">Дата и время, когда событие произошло в соответствии с часами клиента.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-183">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-184">Имя узла</span><span class="sxs-lookup"><span data-stu-id="cdbe5-184">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-185">Имя главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-185">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-186">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="cdbe5-186">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-187">Пользователь, который инициировал событие.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-187">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-188">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="cdbe5-188">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-189">Имя рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-189">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-190">Имя компьютера рабочей области</span><span class="sxs-lookup"><span data-stu-id="cdbe5-190">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-191">Имя компьютера, на котором запущена Рабочая область MED-V.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-191">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganerrorlogreport"></a><span data-ttu-id="cdbe5-192">Создание отчета о журнале ошибок</span><span class="sxs-lookup"><span data-stu-id="cdbe5-192">How to Generate an Error Log Report</span></span>


**<span data-ttu-id="cdbe5-193">Создание отчета о журнале ошибок</span><span class="sxs-lookup"><span data-stu-id="cdbe5-193">To generate an error log report</span></span>**

1.  <span data-ttu-id="cdbe5-194">Нажмите кнопку Управление **отчетами** .</span><span class="sxs-lookup"><span data-stu-id="cdbe5-194">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="cdbe5-195">В модуле " **отчеты** " в меню " **типы отчетов** " выберите " **журнал ошибок**" и нажмите кнопку " **создать**".</span><span class="sxs-lookup"><span data-stu-id="cdbe5-195">In the **Reports** module, on the **Report Types** menu, select **Error Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="cdbe5-196">В диалоговом окне **Параметры отчета** настройте один или несколько из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="cdbe5-196">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="cdbe5-197">**Количество**дней — количество дней, отображаемых в отчете.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-197">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="cdbe5-198">**Имя пользователя содержит**— любое событие, в котором имя пользователя содержит введенный текст, включается в отчет.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-198">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="cdbe5-199">**Имя узла содержит**— любое событие, в котором имя узла содержит введенный текст, включается в отчет.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-199">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="cdbe5-200">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-200">Click **OK**.</span></span>

    <span data-ttu-id="cdbe5-201">Создается отчет с выбранными событиями и датами.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-201">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="cdbe5-202">Параметры отчета описаны в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-202">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="cdbe5-203">Свойства отчета "журнал ошибок"</span><span class="sxs-lookup"><span data-stu-id="cdbe5-203">Error Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cdbe5-204">Свойство</span><span class="sxs-lookup"><span data-stu-id="cdbe5-204">Property</span></span></th>
<th align="left"><span data-ttu-id="cdbe5-205">Описание</span><span class="sxs-lookup"><span data-stu-id="cdbe5-205">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-206">Идентификатор события</span><span class="sxs-lookup"><span data-stu-id="cdbe5-206">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-207">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-207">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-208">Категория</span><span class="sxs-lookup"><span data-stu-id="cdbe5-208">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-209">Модуль, на который ссылается отчет.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-209">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-210">Описание</span><span class="sxs-lookup"><span data-stu-id="cdbe5-210">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-211">Описание события.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-211">A description of the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-212">Время получения</span><span class="sxs-lookup"><span data-stu-id="cdbe5-212">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-213">Дата и время получения события на сервере.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-213">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="cdbe5-214">Примечание.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-214">Note</span></span></strong><br/><p><span data-ttu-id="cdbe5-215">Если клиент работает в автономном режиме, сервер получает отчеты, когда клиент подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-215">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="cdbe5-216">Примечание.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-216">Note</span></span></strong><br/><p><span data-ttu-id="cdbe5-217">По умолчанию события отображаются в порядке убывания дат.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-217">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="cdbe5-218">Однако его можно изменить, щелкнув <strong> столбец время получения </strong> .</span><span class="sxs-lookup"><span data-stu-id="cdbe5-218">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-219">Время клиента</span><span class="sxs-lookup"><span data-stu-id="cdbe5-219">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-220">Дата и время, когда событие произошло в соответствии с часами клиента.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-220">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-221">Имя узла</span><span class="sxs-lookup"><span data-stu-id="cdbe5-221">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-222">Имя главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-222">The name of the host computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdbe5-223">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="cdbe5-223">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-224">Пользователь, который инициировал событие.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-224">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdbe5-225">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="cdbe5-225">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdbe5-226">Имя рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="cdbe5-226">The name of the MED-V workspace.</span></span></p></td>
</tr>
</tbody>
</table>











