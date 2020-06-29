---
title: Расшифровка отчетов MBAM в диспетчере конфигураций
description: Расшифровка отчетов MBAM в диспетчере конфигураций
author: dansimp
ms.assetid: b2582190-c9de-4e64-bd5a-f31ac1916f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 995d628cafd03c8bdd209e467c9d22169b7e03c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823822"
---
# <span data-ttu-id="29607-103">Расшифровка отчетов MBAM в диспетчере конфигураций</span><span class="sxs-lookup"><span data-stu-id="29607-103">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="29607-104">При установке Microsoft BitLocker Administration и Monitoring (MBAM) с помощью встроенной топологии Configuration Manager, функции соответствия требованиям к оборудованию и отчетов переносятся в инфраструктуру Configuration Manager и из MBAM.</span><span class="sxs-lookup"><span data-stu-id="29607-104">When Microsoft BitLocker Administration and Monitoring (MBAM) is installed with the Configuration Manager Integrated topology, the hardware compliance and reporting features are moved into the Configuration Manager infrastructure and out of MBAM.</span></span> <span data-ttu-id="29607-105">При использовании топологии Configuration Manager вы запускаете отчеты из Configuration Manager, а не из MBAM, за исключением отчета аудита восстановления, доступ к которому можно получить с помощью веб-сайта администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="29607-105">When you use the Configuration Manager topology, you run reports from Configuration Manager rather than from MBAM, except for the Recovery Audit Report, which you continue to access by using the Administration and Monitoring Website.</span></span>

<span data-ttu-id="29607-106">Отчеты для интегрированной топологии Configuration Manager показывают соответствие требованиям BitLocker для предприятия и для отдельных компьютеров и устройств, которые MBAM управлять.</span><span class="sxs-lookup"><span data-stu-id="29607-106">The reports for the Configuration Manager Integrated topology show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="29607-107">Отчеты предоставляют как табличные данные, так и диаграммы и позволяют фильтровать отчеты для просмотра данных с разных точек зрения.</span><span class="sxs-lookup"><span data-stu-id="29607-107">The reports provide both tabular information and charts, and enable you to filter reports to view data from different perspectives.</span></span>

<span data-ttu-id="29607-108">В этой статье описаны отчеты MBAM, которые выполняются из Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="29607-108">The information in this topic describes the MBAM reports that you run from Configuration Manager.</span></span> <span data-ttu-id="29607-109">Сведения об отчетах MBAM для изолированной топологии можно найти в разделе [Общие сведения о MBAMх](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="29607-109">For information about MBAM reports for the Stand-alone topology, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

## <span data-ttu-id="29607-110">Доступ к отчетам в Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="29607-110">Accessing Reports in Configuration Manager</span></span>


<span data-ttu-id="29607-111">Чтобы получить доступ к компоненту отчеты в диспетчере конфигураций, откройте **консоль Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="29607-111">To access the Reports feature in Configuration Manager, open the **Configuration Manager console**.</span></span> <span data-ttu-id="29607-112">Чтобы отобразить список доступных отчетов, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="29607-112">To display the list of available reports:</span></span>

-   <span data-ttu-id="29607-113">В Configuration Manager 2007 разверните узел **Управление компьютером** , а затем разверните узел **отчеты** .</span><span class="sxs-lookup"><span data-stu-id="29607-113">In Configuration Manager 2007, expand the **Computer Management** node, and then expand the **Reporting** node.</span></span>

-   <span data-ttu-id="29607-114">В SystemCenter2012 ConfigurationManager в рабочей области мониторинг в разделе **Обзор**разверните узел **отчеты** и выберите пункт **отчеты**.</span><span class="sxs-lookup"><span data-stu-id="29607-114">In SystemCenter2012 ConfigurationManager, in the Monitoring workspace under **Overview**, expand the **Reporting** node and then click **Reports**.</span></span>

### <span data-ttu-id="29607-115">Панель мониторинга соответствия требованиям для предприятия BitLocker</span><span class="sxs-lookup"><span data-stu-id="29607-115">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="29607-116">На панели мониторинга "соответствие требованиям" для предприятий BitLocker доступны следующие графы, которые показывают состояние соответствия требованиям BitLocker в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="29607-116">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="29607-117">Распространение состояния соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-117">Compliance Status Distribution</span></span>

-   <span data-ttu-id="29607-118">Распространение ошибок, не отвечающих требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-118">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="29607-119">Распределение состояния соответствия по типу диска</span><span class="sxs-lookup"><span data-stu-id="29607-119">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="29607-120">Распространение состояния соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-120">Compliance Status Distribution</span></span>**

<span data-ttu-id="29607-121">Эта круговая диаграмма показывает состояние соответствия требованиям компьютера в рамках предприятия и показывает процент компьютеров в сравнении с общим количеством компьютеров в выбранной коллекции, имеющим это состояние соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="29607-121">This pie chart shows computer compliance statuses within the enterprise, and shows the percentage of computers, compared to the total number of computers in the selected collection, that have that compliance status.</span></span> <span data-ttu-id="29607-122">Также отображается фактическое количество компьютеров с каждым состоянием.</span><span class="sxs-lookup"><span data-stu-id="29607-122">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="29607-123">Круговая диаграмма показывает следующее состояние соответствия требованиям:</span><span class="sxs-lookup"><span data-stu-id="29607-123">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="29607-124">SDMI</span><span class="sxs-lookup"><span data-stu-id="29607-124">Compliant</span></span>

-   <span data-ttu-id="29607-125">Не соответствует требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-125">Non Compliant</span></span>

-   <span data-ttu-id="29607-126">Освобождение от пользователя</span><span class="sxs-lookup"><span data-stu-id="29607-126">User Exempt</span></span>

-   <span data-ttu-id="29607-127">Временный освобождаемый от пользователя</span><span class="sxs-lookup"><span data-stu-id="29607-127">Temporary User Exempt</span></span>

-   <span data-ttu-id="29607-128">Политика не принудительно применена</span><span class="sxs-lookup"><span data-stu-id="29607-128">Policy Not Enforced</span></span>

-   <span data-ttu-id="29607-129">Неизвестные — компьютеры, состояние которых сообщило об ошибке, или устройства, которые являются частью коллекции, но не сообщали о состоянии соответствия требованиям, например если они отключены от Организации.</span><span class="sxs-lookup"><span data-stu-id="29607-129">Unknown -computers whose status was reported as an error, or devices that are part of the collection but have never reported their compliance status, for example, if they are disconnected from the organization</span></span>

**<span data-ttu-id="29607-130">Распространение ошибок, не отвечающих требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-130">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="29607-131">Эта круговая диаграмма показывает категории компьютеров в сети, которые не соответствуют политике шифрования диска BitLocker, и показывают количество компьютеров в каждой категории.</span><span class="sxs-lookup"><span data-stu-id="29607-131">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker drive encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="29607-132">Каждая категория процентов рассчитывается на основе общего количества компьютеров, не отвечающих требованиям, в семействе.</span><span class="sxs-lookup"><span data-stu-id="29607-132">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="29607-133">Отложенное шифрование пользователя</span><span class="sxs-lookup"><span data-stu-id="29607-133">User postponed encryption</span></span>

-   <span data-ttu-id="29607-134">Не удается найти совместимый доверенный платформенный модуль</span><span class="sxs-lookup"><span data-stu-id="29607-134">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="29607-135">Системный раздел недоступен или достаточен</span><span class="sxs-lookup"><span data-stu-id="29607-135">System Partition not available or large enough</span></span>

-   <span data-ttu-id="29607-136">Конфликт политики</span><span class="sxs-lookup"><span data-stu-id="29607-136">Policy conflict</span></span>

-   <span data-ttu-id="29607-137">Ожидание автоматической подготовки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="29607-137">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="29607-138">Произошла неизвестная ошибка</span><span class="sxs-lookup"><span data-stu-id="29607-138">An unknown error has occurred</span></span>

-   <span data-ttu-id="29607-139">Нет сведений (на компьютерах, на которых не установлен клиент MBAM или у которого установлен клиент MBAM, но активация не выполнена, например, служба не работает</span><span class="sxs-lookup"><span data-stu-id="29607-139">No information – computers that do not have the MBAM Client installed, or that have the MBAM Client installed but not activated, for example, the service is not working</span></span>

**<span data-ttu-id="29607-140">Распределение состояния соответствия по типу диска</span><span class="sxs-lookup"><span data-stu-id="29607-140">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="29607-141">На этой линейчатой диаграмме показано текущее состояние соответствия требованиям BitLocker по типу диска.</span><span class="sxs-lookup"><span data-stu-id="29607-141">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="29607-142">Состояния "совместимо" и "не соответствует требованиям".</span><span class="sxs-lookup"><span data-stu-id="29607-142">The statuses are “Compliant” and “Non Compliant.”</span></span> <span data-ttu-id="29607-143">Панели отображаются для несъемных дисков с данными и дисков операционной системы.</span><span class="sxs-lookup"><span data-stu-id="29607-143">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="29607-144">Компьютеры, на которых не установлен фиксированный диск с данными, включаются и отображают значение только на панели дисков операционной системы.</span><span class="sxs-lookup"><span data-stu-id="29607-144">Computers that do not have a fixed data drive are included and show a value only in the Operating System Drive bar.</span></span> <span data-ttu-id="29607-145">Диаграмма не содержит пользователей, которым было предоставлено исключение из политики шифрования диска BitLocker или из категории "нет политики".</span><span class="sxs-lookup"><span data-stu-id="29607-145">The chart does not include users who have been granted an exemption from the BitLocker drive encryption policy or the “No Policy” category.</span></span>

### <span data-ttu-id="29607-146">Отчет об соответствиях требованиям для предприятий BitLocker</span><span class="sxs-lookup"><span data-stu-id="29607-146">BitLocker Enterprise Compliance Details Report</span></span>

<span data-ttu-id="29607-147">В этом отчете выводятся сведения об общем соответствии с требованиями к BitLocker в рамках предприятия для коллекции компьютеров, предназначенных для использования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29607-147">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="29607-148">Поля отчета о соответствии требованиям в BitLocker для предприятий</span><span class="sxs-lookup"><span data-stu-id="29607-148">BitLocker Enterprise Compliance Details Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29607-149">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="29607-149">Column Name</span></span></th>
<th align="left"><span data-ttu-id="29607-150">Описание</span><span class="sxs-lookup"><span data-stu-id="29607-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-151">Управляемые компьютеры</span><span class="sxs-lookup"><span data-stu-id="29607-151">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-152">Количество компьютеров, которым MBAM управлять.</span><span class="sxs-lookup"><span data-stu-id="29607-152">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-153">% Соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-153">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-154">Процент соответствия требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="29607-154">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-155">% Не соответствует требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-155">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-156">Процент несоответствующих требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="29607-156">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-157">% Неизвестное соответствие требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-157">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-158">Процент компьютеров, состояние соответствия которых неизвестно.</span><span class="sxs-lookup"><span data-stu-id="29607-158">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-159">% Исключении</span><span class="sxs-lookup"><span data-stu-id="29607-159">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-160">Процент компьютеров, исключаемых из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29607-160">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-161">% Без исключения</span><span class="sxs-lookup"><span data-stu-id="29607-161">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-162">Процент компьютеров, исключаемых из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29607-162">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-163">SDMI</span><span class="sxs-lookup"><span data-stu-id="29607-163">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-164">Процент соответствия требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="29607-164">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-165">Не соответствует требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-165">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-166">Процент несоответствующих требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="29607-166">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-167">Неизвестное соответствие</span><span class="sxs-lookup"><span data-stu-id="29607-167">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-168">Процент компьютеров, состояние соответствия которых неизвестно.</span><span class="sxs-lookup"><span data-stu-id="29607-168">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-169">Облагаемый</span><span class="sxs-lookup"><span data-stu-id="29607-169">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-170">Общее количество компьютеров, исключаемых из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29607-170">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-171">Без исключения</span><span class="sxs-lookup"><span data-stu-id="29607-171">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-172">Общее количество компьютеров без исключения из требований шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29607-172">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="29607-173">Отчет "сведения о соответствии требованиям в корпоративной среде BitLocker" — состояния соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-173">BitLocker Enterprise Compliance Details Report - Compliance States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29607-174">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-174">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="29607-175">Исключение</span><span class="sxs-lookup"><span data-stu-id="29607-175">Exemption</span></span></th>
<th align="left"><span data-ttu-id="29607-176">Описание</span><span class="sxs-lookup"><span data-stu-id="29607-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-177">Несоответствующих</span><span class="sxs-lookup"><span data-stu-id="29607-177">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-178">Не исключено</span><span class="sxs-lookup"><span data-stu-id="29607-178">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-179">Компьютер не соответствует политике в соответствии с указанной политикой.</span><span class="sxs-lookup"><span data-stu-id="29607-179">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-180">SDMI</span><span class="sxs-lookup"><span data-stu-id="29607-180">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-181">Не исключено</span><span class="sxs-lookup"><span data-stu-id="29607-181">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-182">Компьютер соответствует требованиям указанной политики.</span><span class="sxs-lookup"><span data-stu-id="29607-182">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="29607-183">Сводный отчет о соответствиях требованиям для предприятий BitLocker</span><span class="sxs-lookup"><span data-stu-id="29607-183">BitLocker Enterprise Compliance Summary Report</span></span>

<span data-ttu-id="29607-184">Этот тип отчета используется для отображения сведений о соответствии общего соответствия требованиям BitLocker для всего предприятия и для отображения соответствия требованиям для отдельных компьютеров, которые находятся в семействе компьютеров, предназначенных для использования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29607-184">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="29607-185">Поля сводного отчета о соответствиях требованиям для предприятий BitLocker</span><span class="sxs-lookup"><span data-stu-id="29607-185">BitLocker Enterprise Compliance Summary Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29607-186">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="29607-186">Column Name</span></span></th>
<th align="left"><span data-ttu-id="29607-187">Описание</span><span class="sxs-lookup"><span data-stu-id="29607-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-188">Управляемые компьютеры</span><span class="sxs-lookup"><span data-stu-id="29607-188">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-189">Количество компьютеров, которым MBAM управлять.</span><span class="sxs-lookup"><span data-stu-id="29607-189">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-190">% Соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-190">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-191">Процент соответствия требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="29607-191">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-192">% Не соответствует требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-192">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-193">Процент несоответствующих требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="29607-193">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-194">% Неизвестное соответствие требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-194">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-195">Процент компьютеров, состояние соответствия которых неизвестно.</span><span class="sxs-lookup"><span data-stu-id="29607-195">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-196">% Исключении</span><span class="sxs-lookup"><span data-stu-id="29607-196">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-197">Процент компьютеров, исключаемых из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29607-197">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-198">% Без исключения</span><span class="sxs-lookup"><span data-stu-id="29607-198">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-199">Процент компьютеров, исключаемых из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29607-199">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-200">SDMI</span><span class="sxs-lookup"><span data-stu-id="29607-200">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-201">Процент соответствия требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="29607-201">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-202">Не соответствует требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-202">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-203">Процент несоответствующих требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="29607-203">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-204">Неизвестное соответствие</span><span class="sxs-lookup"><span data-stu-id="29607-204">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-205">Процент компьютеров, состояние соответствия которых неизвестно.</span><span class="sxs-lookup"><span data-stu-id="29607-205">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-206">Облагаемый</span><span class="sxs-lookup"><span data-stu-id="29607-206">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-207">Общее количество компьютеров, исключаемых из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29607-207">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-208">Без исключения</span><span class="sxs-lookup"><span data-stu-id="29607-208">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-209">Общее количество компьютеров без исключения из требований шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29607-209">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="29607-210">Сводный отчет о соответствиях требованиям для предприятий BitLocker — сведения о компьютере</span><span class="sxs-lookup"><span data-stu-id="29607-210">BitLocker Enterprise Compliance Summary Report - Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29607-211">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="29607-211">Column Name</span></span></th>
<th align="left"><span data-ttu-id="29607-212">Описание</span><span class="sxs-lookup"><span data-stu-id="29607-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-213">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="29607-213">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-214">Указанное пользователем DNS-имя компьютера, которое управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="29607-214">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-215">Доменное имя</span><span class="sxs-lookup"><span data-stu-id="29607-215">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-216">Полное доменное имя, в котором находится клиентский компьютер и управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="29607-216">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-217">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-217">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-218">Общее состояние соответствия требованиям компьютера, управляемого с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="29607-218">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="29607-219">Допустимые состояния соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="29607-219">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="29607-220">Обратите внимание, что состояние соответствия для каждого диска (приведенная ниже таблица) может указывать на разные состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="29607-220">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="29607-221">Однако это поле представляет состояние соответствия требованиям в соответствии с указанной политикой.</span><span class="sxs-lookup"><span data-stu-id="29607-221">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-222">Исключение</span><span class="sxs-lookup"><span data-stu-id="29607-222">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-223">Состояние, указывающее на то, является ли пользователь исключенным или неисключением из политики BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29607-223">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-224">Пользователи устройств</span><span class="sxs-lookup"><span data-stu-id="29607-224">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-225">Пользователь устройства.</span><span class="sxs-lookup"><span data-stu-id="29607-225">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-226">Сведения о статусе соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-226">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-227">Сообщения об ошибках и состоянии соответствия требованиям компьютера согласно указанной политике.</span><span class="sxs-lookup"><span data-stu-id="29607-227">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-228">Последний контакт</span><span class="sxs-lookup"><span data-stu-id="29607-228">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-229">Дата и время последнего обращения компьютера к серверу для отправки отчета о состоянии соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="29607-229">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="29607-230">Частота контактов настраивается (см. раздел Параметры политики MBAM).</span><span class="sxs-lookup"><span data-stu-id="29607-230">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="29607-231">Отчет о соответствии компьютера BitLocker</span><span class="sxs-lookup"><span data-stu-id="29607-231">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="29607-232">Этот тип отчета используется для сбора сведений, относящихся к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="29607-232">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="29607-233">Отчет о соответствии компьютера содержит подробные сведения о шифровании каждого диска (операционной системы и фиксированных дисков с данными) на компьютере, а также сведения о политике, применяемой к каждому типу дисков на компьютере.</span><span class="sxs-lookup"><span data-stu-id="29607-233">The Computer Compliance Report provides detailed encryption information about each drive (Operating System and Fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="29607-234">Чтобы просмотреть сведения о каждом диске, разверните элемент имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="29607-234">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="29607-235">**Примечание**  Состояние шифрования тома съемных данных не отображается в отчете.</span><span class="sxs-lookup"><span data-stu-id="29607-235">**Note** Removable Data Volume encryption status is not shown in the report.</span></span>

 

**<span data-ttu-id="29607-236">Отчет о соответствии компьютера BitLocker — поля сведений о компьютере</span><span class="sxs-lookup"><span data-stu-id="29607-236">BitLocker Computer Compliance Report – Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29607-237">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="29607-237">Column Name</span></span></th>
<th align="left"><span data-ttu-id="29607-238">Описание</span><span class="sxs-lookup"><span data-stu-id="29607-238">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-239">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="29607-239">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-240">Указанное пользователем DNS-имя компьютера, которое управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="29607-240">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-241">Доменное имя</span><span class="sxs-lookup"><span data-stu-id="29607-241">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-242">Полное доменное имя, в котором находится клиентский компьютер и управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="29607-242">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-243">Тип компьютера</span><span class="sxs-lookup"><span data-stu-id="29607-243">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-244">Тип компьютера.</span><span class="sxs-lookup"><span data-stu-id="29607-244">Type of computer.</span></span> <span data-ttu-id="29607-245">Допустимые типы не являются переносимыми и переносимыми.</span><span class="sxs-lookup"><span data-stu-id="29607-245">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-246">Операционная система</span><span class="sxs-lookup"><span data-stu-id="29607-246">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-247">Тип операционной системы на клиентском компьютере с управляемым MBAM.</span><span class="sxs-lookup"><span data-stu-id="29607-247">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-248">Общее соответствие требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-248">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-249">Общее состояние соответствия требованиям компьютера, управляемого с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="29607-249">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="29607-250">Допустимые состояния соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="29607-250">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="29607-251">Обратите внимание, что состояние соответствия для каждого диска (приведенная ниже таблица) может указывать на разные состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="29607-251">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="29607-252">Однако это поле представляет состояние соответствия требованиям в соответствии с указанной политикой.</span><span class="sxs-lookup"><span data-stu-id="29607-252">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-253">Соответствие требованиям операционной системы</span><span class="sxs-lookup"><span data-stu-id="29607-253">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-254">Состояние соответствия требованиям операционной системы, управляемой MBAM.</span><span class="sxs-lookup"><span data-stu-id="29607-254">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="29607-255">Допустимые состояния соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="29607-255">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-256">Соответствие фиксированному диску с данными</span><span class="sxs-lookup"><span data-stu-id="29607-256">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-257">Состояние соответствия фиксированному диску с данными, управляемому с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="29607-257">Compliance status of the Fixed Data Drive that is managed by MBAM.</span></span> <span data-ttu-id="29607-258">Допустимые состояния соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="29607-258">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-259">Дата последнего обновления</span><span class="sxs-lookup"><span data-stu-id="29607-259">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-260">Дата и время последнего обращения компьютера к серверу для отправки отчета о состоянии соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="29607-260">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="29607-261">Частота контактов настраивается (см. раздел Параметры политики MBAM).</span><span class="sxs-lookup"><span data-stu-id="29607-261">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-262">Исключение</span><span class="sxs-lookup"><span data-stu-id="29607-262">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-263">Состояние, указывающее на то, является ли пользователь исключенным или неисключением из политики BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29607-263">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-264">Исключенный пользователь</span><span class="sxs-lookup"><span data-stu-id="29607-264">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-265">Пользователь, исключаемый из политики BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29607-265">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-266">Дата освобождения</span><span class="sxs-lookup"><span data-stu-id="29607-266">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-267">Дата, когда был предоставлен доступ к исключению.</span><span class="sxs-lookup"><span data-stu-id="29607-267">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-268">Сведения о статусе соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="29607-268">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-269">Сообщения об ошибках и состоянии соответствия требованиям компьютера согласно указанной политике.</span><span class="sxs-lookup"><span data-stu-id="29607-269">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-270">Стойкость шифра политики</span><span class="sxs-lookup"><span data-stu-id="29607-270">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-271">Стойкость шифра, выбранная администратором в течение MBAM политики.</span><span class="sxs-lookup"><span data-stu-id="29607-271">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="29607-272">(например, 128-бит с диффузором).</span><span class="sxs-lookup"><span data-stu-id="29607-272">(for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-273">Политика: диск операционной системы</span><span class="sxs-lookup"><span data-stu-id="29607-273">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-274">Указывает, требуется ли шифрование для O/S и соответствующего типа предохранителя.</span><span class="sxs-lookup"><span data-stu-id="29607-274">Indicates if encryption is required for the O/S and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-275">Политика: несъемный диск с данными</span><span class="sxs-lookup"><span data-stu-id="29607-275">Policy:Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-276">Указывает, требуется ли шифрование для жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="29607-276">Indicates if encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-277">Изготовитель</span><span class="sxs-lookup"><span data-stu-id="29607-277">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-278">Название изготовителя компьютера, которое отображается в BIOS компьютера.</span><span class="sxs-lookup"><span data-stu-id="29607-278">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-279">Модель</span><span class="sxs-lookup"><span data-stu-id="29607-279">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-280">Название модели изготовителя компьютера, которое отображается в BIOS компьютера.</span><span class="sxs-lookup"><span data-stu-id="29607-280">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-281">Пользователи устройств</span><span class="sxs-lookup"><span data-stu-id="29607-281">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-282">Известные пользователи на компьютере, управляемом с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="29607-282">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="29607-283">Отчет о соответствии компьютера BitLocker — поля громкости компьютера</span><span class="sxs-lookup"><span data-stu-id="29607-283">BitLocker Computer Compliance Report – Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29607-284">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="29607-284">Column Name</span></span></th>
<th align="left"><span data-ttu-id="29607-285">Описание</span><span class="sxs-lookup"><span data-stu-id="29607-285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-286">Буква диска</span><span class="sxs-lookup"><span data-stu-id="29607-286">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-287">Буква диска компьютера, назначенная пользователем на определенный диск.</span><span class="sxs-lookup"><span data-stu-id="29607-287">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-288">Тип диска</span><span class="sxs-lookup"><span data-stu-id="29607-288">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-289">Тип диска.</span><span class="sxs-lookup"><span data-stu-id="29607-289">Type of drive.</span></span> <span data-ttu-id="29607-290">Допустимые значения: диск операционной системы и фиксированный диск с данными.</span><span class="sxs-lookup"><span data-stu-id="29607-290">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="29607-291">Это физические диски, а не логические тома.</span><span class="sxs-lookup"><span data-stu-id="29607-291">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-292">Стойкость шифра</span><span class="sxs-lookup"><span data-stu-id="29607-292">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-293">Стойкость шифра, выбранная администратором в течение MBAM политики.</span><span class="sxs-lookup"><span data-stu-id="29607-293">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-294">Типы предохранителей</span><span class="sxs-lookup"><span data-stu-id="29607-294">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-295">Тип предохранителя, выбранный с помощью политики, используемой для шифрования операционной системы или фиксированного тома.</span><span class="sxs-lookup"><span data-stu-id="29607-295">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="29607-296">Допустимые типы предохранителей в операционной системе являются доверенными платформенными модулями или TPM + PIN-кодом и для фиксированного тома данных — Password (пароль).</span><span class="sxs-lookup"><span data-stu-id="29607-296">The valid protector types on an operating system are TPM or TPM+PIN and for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29607-297">Состояние предохранителя</span><span class="sxs-lookup"><span data-stu-id="29607-297">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-298">Указывает на то, что на компьютере, управляемом MBAM, включен тип предохранителя, указанный в политике.</span><span class="sxs-lookup"><span data-stu-id="29607-298">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="29607-299">Допустимые состояния: ON и OFF.</span><span class="sxs-lookup"><span data-stu-id="29607-299">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29607-300">Состояние шифрования</span><span class="sxs-lookup"><span data-stu-id="29607-300">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="29607-301">Состояние шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="29607-301">Encryption state of the drive.</span></span> <span data-ttu-id="29607-302">Допустимые состояния шифруются, а не шифруются и шифруются.</span><span class="sxs-lookup"><span data-stu-id="29607-302">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="29607-303">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="29607-303">Related topics</span></span>


[<span data-ttu-id="29607-304">Использование MBAM с диспетчером конфигураций</span><span class="sxs-lookup"><span data-stu-id="29607-304">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 





