---
title: Просмотр отчетов MBAM 2.5 для топологии интеграции диспетчера конфигураций
description: Просмотр отчетов MBAM 2.5 для топологии интеграции диспетчера конфигураций
author: dansimp
ms.assetid: 60d11b2f-3a76-4023-8da4-f89e9f35b790
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3384fee62d302ac47775fe106265456ef119ab47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824042"
---
# <span data-ttu-id="2eb86-103">Просмотр отчетов MBAM 2.5 для топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="2eb86-103">Viewing MBAM 2.5 Reports for the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="2eb86-104">В этой статье описаны отчеты, доступные при настройке администрирования и мониторинга Microsoft BitLocker (MBAM) с топологией интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2eb86-104">This topic describes the reports that are available when you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="2eb86-105">В отчетах выводятся сведения о соответствии BitLocker для предприятия и об отдельных компьютерах и устройствах, которыми управляет MBAM.</span><span class="sxs-lookup"><span data-stu-id="2eb86-105">The reports show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="2eb86-106">Отчеты содержат табличные данные и диаграммы, а также фильтры, позволяющие просматривать данные с разных точек зрения.</span><span class="sxs-lookup"><span data-stu-id="2eb86-106">The reports provide tabular information and charts, and they have filters that let you view data from different perspectives.</span></span>

<span data-ttu-id="2eb86-107">В топологии интеграции Configuration Manager вы можете просматривать отчеты из Configuration Manager, а не с веб-сайта администрирования и мониторинга, за исключением **отчета аудита восстановления**, который вы продолжаете просматривать на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="2eb86-107">In the Configuration Manager Integration topology, you view reports from Configuration Manager rather than from the Administration and Monitoring Website, with the exception of the **Recovery Audit Report**, which you continue to view from the Administration and Monitoring Website.</span></span>

<span data-ttu-id="2eb86-108">Дополнительные сведения о MBAMх отчетов для изолированной топологии можно найти в статьях [Просмотр отчетов MBAM 2,5 для изолированной топологии](viewing-mbam-25-reports-for-the-stand-alone-topology.md).</span><span class="sxs-lookup"><span data-stu-id="2eb86-108">For information about MBAM reports for the Stand-alone topology, see [Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md).</span></span>

## <span data-ttu-id="2eb86-109">Доступ к отчетам в Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2eb86-109">Accessing reports in Configuration Manager</span></span>


<span data-ttu-id="2eb86-110">Чтобы получить доступ к функциям отчетов в диспетчере конфигураций, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-110">To access the Reports feature in Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2eb86-111">Версия Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2eb86-111">Version of Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="2eb86-112">Просмотр отчетов</span><span class="sxs-lookup"><span data-stu-id="2eb86-112">How to view the reports</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-113">SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="2eb86-113">SystemCenter2012 ConfigurationManager</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="2eb86-114">В левой области выберите <strong> рабочую область "Мониторинг" </strong> .</span><span class="sxs-lookup"><span data-stu-id="2eb86-114">In the left pane, select the <strong>Monitoring</strong> workspace.</span></span></p></li>
<li><p><span data-ttu-id="2eb86-115">В дереве разверните раздел отчеты о отчетах <strong> </strong> &gt; <strong> </strong> &gt; <strong> </strong> &gt; <strong> MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="2eb86-115">In the tree, expand <strong>Overview</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reports</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="2eb86-116">Выберите папку, представляющую язык, на котором вы хотите просмотреть отчеты, а затем выберите отчет в области справа.</span><span class="sxs-lookup"><span data-stu-id="2eb86-116">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-117">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="2eb86-117">Configuration Manager 2007</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="2eb86-118">На левой панели разверните элемент службы отчетов о <strong> службе управления компьютером, а затем — </strong> &gt; <strong> </strong> &gt; <strong> </strong> &gt; <strong> &lt; &gt; </strong> &gt; <strong> папки отчета имя сервера </strong> &gt; <strong> MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="2eb86-118">In the left pane, expand <strong>Computer Management</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reporting Services</strong> &gt; <strong>&lt;server name&gt;</strong> &gt; <strong>Report folders</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="2eb86-119">Выберите папку, представляющую язык, на котором вы хотите просмотреть отчеты, а затем выберите отчет в области справа.</span><span class="sxs-lookup"><span data-stu-id="2eb86-119">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2eb86-120">Описание отчетов в Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2eb86-120">Description of reports in Configuration Manager</span></span>


<span data-ttu-id="2eb86-121">В отчетах для топологии интеграции Configuration Manager и изолированной топологии есть несколько незначительных отличий.</span><span class="sxs-lookup"><span data-stu-id="2eb86-121">There are a few minor differences in the reports for the Configuration Manager Integration topology and the Stand-alone topology.</span></span> <span data-ttu-id="2eb86-122">В следующих разделах описаны данные в отчетах MBAM для топологии интеграции Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="2eb86-122">The following sections describe the data in the MBAM reports for the Configuration Manager Integration topology:</span></span>

-   [<span data-ttu-id="2eb86-123">Панель мониторинга соответствия требованиям для предприятия BitLocker</span><span class="sxs-lookup"><span data-stu-id="2eb86-123">BitLocker Enterprise Compliance Dashboard</span></span>](#bkmk-dashboard)

-   [<span data-ttu-id="2eb86-124">Сведения о соответствии требованиям BitLocker для предприятий</span><span class="sxs-lookup"><span data-stu-id="2eb86-124">BitLocker Enterprise Compliance Details</span></span>](#bkmk-compliancedetails)

-   [<span data-ttu-id="2eb86-125">Сводка по соответствию требованиям для предприятий BitLocker</span><span class="sxs-lookup"><span data-stu-id="2eb86-125">BitLocker Enterprise Compliance Summary</span></span>](#bkmk-compliancesummary)

-   [<span data-ttu-id="2eb86-126">Отчет о соответствии компьютера BitLocker</span><span class="sxs-lookup"><span data-stu-id="2eb86-126">BitLocker Computer Compliance Report</span></span>](#bkmk-compliancereport)

### <a href="" id="bkmk-dashboard"></a><span data-ttu-id="2eb86-127">Панель мониторинга соответствия требованиям для предприятия BitLocker</span><span class="sxs-lookup"><span data-stu-id="2eb86-127">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="2eb86-128">На панели мониторинга "соответствие требованиям" для предприятий BitLocker доступны следующие графы, которые показывают состояние соответствия требованиям BitLocker в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-128">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="2eb86-129">Распространение состояния соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-129">Compliance Status Distribution</span></span>

-   <span data-ttu-id="2eb86-130">Распространение ошибок, не отвечающих требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-130">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="2eb86-131">Распределение состояния соответствия по типу диска</span><span class="sxs-lookup"><span data-stu-id="2eb86-131">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="2eb86-132">Распространение состояния соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-132">Compliance Status Distribution</span></span>**

<span data-ttu-id="2eb86-133">Эта круговая диаграмма показывает состояние соответствия требованиям компьютеров в рамках предприятия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-133">This pie chart shows compliance status for computers within the enterprise.</span></span> <span data-ttu-id="2eb86-134">Он также показывает процент компьютеров в сравнении с общим количеством компьютеров в выбранной коллекции с этим состоянием соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="2eb86-134">It also shows the percentage of computers, compared to the total number of computers in the selected collection, that has that compliance status.</span></span> <span data-ttu-id="2eb86-135">Также отображается фактическое количество компьютеров с каждым состоянием.</span><span class="sxs-lookup"><span data-stu-id="2eb86-135">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="2eb86-136">Круговая диаграмма показывает следующее состояние соответствия требованиям:</span><span class="sxs-lookup"><span data-stu-id="2eb86-136">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="2eb86-137">SDMI</span><span class="sxs-lookup"><span data-stu-id="2eb86-137">Compliant</span></span>

-   <span data-ttu-id="2eb86-138">Не соответствует требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-138">Non Compliant</span></span>

-   <span data-ttu-id="2eb86-139">Освобождение от пользователя</span><span class="sxs-lookup"><span data-stu-id="2eb86-139">User Exempt</span></span>

-   <span data-ttu-id="2eb86-140">Временный освобождаемый от пользователя</span><span class="sxs-lookup"><span data-stu-id="2eb86-140">Temporary User Exempt</span></span>

-   <span data-ttu-id="2eb86-141">Политика не принудительно применена</span><span class="sxs-lookup"><span data-stu-id="2eb86-141">Policy Not Enforced</span></span>

-   <span data-ttu-id="2eb86-142">Неожиданно.</span><span class="sxs-lookup"><span data-stu-id="2eb86-142">Unknown.</span></span> <span data-ttu-id="2eb86-143">Эти компьютеры сообщили об ошибке состояния или входят в коллекцию, но никогда не сообщали о состоянии соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="2eb86-143">These computers reported a status error, or they are part of the collection, but have never reported their compliance status.</span></span> <span data-ttu-id="2eb86-144">Отсутствие состояния соответствия может возникнуть, если компьютер отключен от Организации.</span><span class="sxs-lookup"><span data-stu-id="2eb86-144">The lack of a compliance status could occur if the computer is disconnected from the organization.</span></span>

**<span data-ttu-id="2eb86-145">Распространение ошибок, не отвечающих требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-145">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="2eb86-146">Эта круговая диаграмма показывает категории компьютеров в сети, которые не соответствуют политике шифрования диска BitLocker, и показывают количество компьютеров в каждой категории.</span><span class="sxs-lookup"><span data-stu-id="2eb86-146">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker Drive Encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="2eb86-147">Каждая категория процентов рассчитывается на основе общего количества компьютеров, не отвечающих требованиям, в семействе.</span><span class="sxs-lookup"><span data-stu-id="2eb86-147">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="2eb86-148">Отложенное шифрование пользователя</span><span class="sxs-lookup"><span data-stu-id="2eb86-148">User postponed encryption</span></span>

-   <span data-ttu-id="2eb86-149">Не удается найти совместимый доверенный платформенный модуль</span><span class="sxs-lookup"><span data-stu-id="2eb86-149">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="2eb86-150">Системный раздел недоступен или достаточен</span><span class="sxs-lookup"><span data-stu-id="2eb86-150">System partition not available or large enough</span></span>

-   <span data-ttu-id="2eb86-151">Конфликт политики</span><span class="sxs-lookup"><span data-stu-id="2eb86-151">Policy conflict</span></span>

-   <span data-ttu-id="2eb86-152">Ожидание автоматической подготовки доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="2eb86-152">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="2eb86-153">Произошла неизвестная ошибка</span><span class="sxs-lookup"><span data-stu-id="2eb86-153">An unknown error has occurred</span></span>

-   <span data-ttu-id="2eb86-154">Нет сведений.</span><span class="sxs-lookup"><span data-stu-id="2eb86-154">No information.</span></span> <span data-ttu-id="2eb86-155">На этих компьютерах не установлен клиент MBAM либо на нем установлен клиент MBAM, но он не активирован (например, служба не работает).</span><span class="sxs-lookup"><span data-stu-id="2eb86-155">These computers do not have the MBAM Client installed, or they have the MBAM Client installed but not activated (for example, the service is not working).</span></span>

**<span data-ttu-id="2eb86-156">Распределение состояния соответствия по типу диска</span><span class="sxs-lookup"><span data-stu-id="2eb86-156">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="2eb86-157">На этой линейчатой диаграмме показано текущее состояние соответствия требованиям BitLocker по типу диска.</span><span class="sxs-lookup"><span data-stu-id="2eb86-157">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="2eb86-158">Состояние **соответствует требованиям** и **не соответствует требованиям**.</span><span class="sxs-lookup"><span data-stu-id="2eb86-158">The statuses are **Compliant** and **Non Compliant**.</span></span> <span data-ttu-id="2eb86-159">Панели отображаются для несъемных дисков с данными и дисков операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2eb86-159">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="2eb86-160">Компьютеры, на которых не установлен фиксированный диск с данными, включаются и отображают значение только на панели **дисков операционной системы** .</span><span class="sxs-lookup"><span data-stu-id="2eb86-160">Computers that do not have a fixed data drive are included and show a value only in the **Operating System Drive** bar.</span></span> <span data-ttu-id="2eb86-161">Диаграмма не содержит пользователей, которым было предоставлено исключение из политики шифрования диска BitLocker или категории "нет политики".</span><span class="sxs-lookup"><span data-stu-id="2eb86-161">The chart does not include users who have been granted an exemption from the BitLocker Drive Encryption policy or the No Policy category.</span></span>

### <a href="" id="bkmk-compliancedetails"></a><span data-ttu-id="2eb86-162">Сведения о соответствии требованиям BitLocker для предприятий</span><span class="sxs-lookup"><span data-stu-id="2eb86-162">BitLocker Enterprise Compliance Details</span></span>

<span data-ttu-id="2eb86-163">В этом отчете выводятся сведения об общем соответствии с требованиями к BitLocker в рамках предприятия для коллекции компьютеров, предназначенных для использования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2eb86-163">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="2eb86-164">Поля сведений о соответствии требованиям для программы BitLocker в корпоративной среде</span><span class="sxs-lookup"><span data-stu-id="2eb86-164">BitLocker Enterprise Compliance Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2eb86-165">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="2eb86-165">Column Name</span></span></th>
<th align="left"><span data-ttu-id="2eb86-166">Описание</span><span class="sxs-lookup"><span data-stu-id="2eb86-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-167">Управляемые компьютеры</span><span class="sxs-lookup"><span data-stu-id="2eb86-167">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-168">Количество компьютеров, которым MBAM управлять.</span><span class="sxs-lookup"><span data-stu-id="2eb86-168">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-169">% Соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-169">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-170">Процент соответствия требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-170">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-171">% Не соответствует требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-171">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-172">Процент несоответствующих требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-172">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-173">% Неизвестное соответствие требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-173">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-174">Процент компьютеров с неизвестным состоянием соответствия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-174">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-175">% Исключении</span><span class="sxs-lookup"><span data-stu-id="2eb86-175">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-176">Процент компьютеров, исключаемых из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2eb86-176">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-177">% Без исключения</span><span class="sxs-lookup"><span data-stu-id="2eb86-177">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-178">Процент компьютеров без исключения из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2eb86-178">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-179">SDMI</span><span class="sxs-lookup"><span data-stu-id="2eb86-179">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-180">Процент соответствия требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-180">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-181">Не соответствует требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-181">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-182">Процент несоответствующих требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-182">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-183">Неизвестное соответствие</span><span class="sxs-lookup"><span data-stu-id="2eb86-183">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-184">Процент компьютеров с неизвестным состоянием соответствия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-184">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-185">Облагаемый</span><span class="sxs-lookup"><span data-stu-id="2eb86-185">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-186">Общее количество компьютеров, исключаемых из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2eb86-186">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-187">Без исключения</span><span class="sxs-lookup"><span data-stu-id="2eb86-187">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-188">Общее количество компьютеров без исключения из требований шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2eb86-188">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="2eb86-189">Состояние сведений о соответствии требованиям в BitLocker для предприятий</span><span class="sxs-lookup"><span data-stu-id="2eb86-189">BitLocker Enterprise Compliance Details States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2eb86-190">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-190">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="2eb86-191">Исключение</span><span class="sxs-lookup"><span data-stu-id="2eb86-191">Exemption</span></span></th>
<th align="left"><span data-ttu-id="2eb86-192">Описание</span><span class="sxs-lookup"><span data-stu-id="2eb86-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-193">Несоответствующих</span><span class="sxs-lookup"><span data-stu-id="2eb86-193">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-194">Не исключено</span><span class="sxs-lookup"><span data-stu-id="2eb86-194">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-195">Компьютер не соответствует политике в соответствии с указанной политикой.</span><span class="sxs-lookup"><span data-stu-id="2eb86-195">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-196">SDMI</span><span class="sxs-lookup"><span data-stu-id="2eb86-196">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-197">Не исключено</span><span class="sxs-lookup"><span data-stu-id="2eb86-197">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-198">Компьютер соответствует требованиям указанной политики.</span><span class="sxs-lookup"><span data-stu-id="2eb86-198">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancesummary"></a><span data-ttu-id="2eb86-199">Сводка по соответствию требованиям для предприятий BitLocker</span><span class="sxs-lookup"><span data-stu-id="2eb86-199">BitLocker Enterprise Compliance Summary</span></span>

<span data-ttu-id="2eb86-200">Этот тип отчета используется для отображения сведений о соответствии общего соответствия требованиям BitLocker для всего предприятия и для отображения соответствия требованиям для отдельных компьютеров, которые находятся в семействе компьютеров, предназначенных для использования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2eb86-200">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="2eb86-201">Поля сводки соответствия требованиям для предприятий BitLocker</span><span class="sxs-lookup"><span data-stu-id="2eb86-201">BitLocker Enterprise Compliance Summary Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2eb86-202">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="2eb86-202">Column Name</span></span></th>
<th align="left"><span data-ttu-id="2eb86-203">Описание</span><span class="sxs-lookup"><span data-stu-id="2eb86-203">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-204">Управляемые компьютеры</span><span class="sxs-lookup"><span data-stu-id="2eb86-204">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-205">Количество компьютеров, которым MBAM управлять.</span><span class="sxs-lookup"><span data-stu-id="2eb86-205">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-206">% Соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-206">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-207">Процент соответствия требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-207">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-208">% Не соответствует требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-208">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-209">Процент несоответствующих требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-209">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-210">% Неизвестное соответствие требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-210">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-211">Процент компьютеров с неизвестным состоянием соответствия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-211">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-212">% Исключении</span><span class="sxs-lookup"><span data-stu-id="2eb86-212">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-213">Процент компьютеров, исключаемых из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2eb86-213">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-214">% Без исключения</span><span class="sxs-lookup"><span data-stu-id="2eb86-214">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-215">Процент компьютеров без исключения из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2eb86-215">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-216">SDMI</span><span class="sxs-lookup"><span data-stu-id="2eb86-216">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-217">Процент соответствия требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-217">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-218">Не соответствует требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-218">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-219">Процент несоответствующих требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-219">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-220">Неизвестное соответствие</span><span class="sxs-lookup"><span data-stu-id="2eb86-220">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-221">Процент компьютеров с неизвестным состоянием соответствия.</span><span class="sxs-lookup"><span data-stu-id="2eb86-221">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-222">Облагаемый</span><span class="sxs-lookup"><span data-stu-id="2eb86-222">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-223">Общее количество компьютеров, исключаемых из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2eb86-223">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-224">Без исключения</span><span class="sxs-lookup"><span data-stu-id="2eb86-224">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-225">Общее количество компьютеров без исключения из требований шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2eb86-225">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="2eb86-226">Сведения о системе соответствия требованиям для предприятий BitLocker</span><span class="sxs-lookup"><span data-stu-id="2eb86-226">BitLocker Enterprise Compliance Summary Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2eb86-227">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="2eb86-227">Column Name</span></span></th>
<th align="left"><span data-ttu-id="2eb86-228">Описание</span><span class="sxs-lookup"><span data-stu-id="2eb86-228">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-229">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="2eb86-229">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-230">Указанное пользователем DNS-имя компьютера, которое управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="2eb86-230">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-231">Доменное имя</span><span class="sxs-lookup"><span data-stu-id="2eb86-231">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-232">Полное доменное имя, в котором находится клиентский компьютер и управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="2eb86-232">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-233">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-233">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-234">Общее состояние соответствия требованиям компьютера, управляемого с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="2eb86-234">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="2eb86-235">Допустимые состояния соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="2eb86-235">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="2eb86-236">Обратите внимание на то, что состояние соответствия для каждого устройства (в приведенной ниже таблице) может указывать на разные состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="2eb86-236">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="2eb86-237">Однако это поле представляет состояние соответствия требованиям в соответствии с указанной политикой.</span><span class="sxs-lookup"><span data-stu-id="2eb86-237">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-238">Исключение</span><span class="sxs-lookup"><span data-stu-id="2eb86-238">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-239">Состояние, указывающее на то, что пользователь не исключен из политики BitLocker или не исключен из нее.</span><span class="sxs-lookup"><span data-stu-id="2eb86-239">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-240">Пользователи устройств</span><span class="sxs-lookup"><span data-stu-id="2eb86-240">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-241">Пользователь устройства.</span><span class="sxs-lookup"><span data-stu-id="2eb86-241">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-242">Сведения о статусе соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-242">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-243">Сообщения об ошибках и состоянии, связанные с состоянием соответствия компьютера согласно указанной политике.</span><span class="sxs-lookup"><span data-stu-id="2eb86-243">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-244">Последний контакт</span><span class="sxs-lookup"><span data-stu-id="2eb86-244">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-245">Дата и время последнего обращения компьютера к серверу для отправки отчета о состоянии соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="2eb86-245">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="2eb86-246">Частота контактов настраивается с помощью параметров групповой политики.</span><span class="sxs-lookup"><span data-stu-id="2eb86-246">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancereport"></a><span data-ttu-id="2eb86-247">Отчет о соответствии компьютера BitLocker</span><span class="sxs-lookup"><span data-stu-id="2eb86-247">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="2eb86-248">Этот тип отчета используется для сбора сведений, относящихся к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="2eb86-248">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="2eb86-249">Отчет о соответствии компьютера требованиям BitLocker содержит подробные сведения о шифровании каждого диска компьютера (операционной системы и несъемные диски с данными).</span><span class="sxs-lookup"><span data-stu-id="2eb86-249">The BitLocker Computer Compliance Report provides detailed encryption information about each drive on a computer (operating system and fixed data drives).</span></span> <span data-ttu-id="2eb86-250">Кроме того, он содержит сведения о политике, применяемой к каждому типу дисков на компьютере.</span><span class="sxs-lookup"><span data-stu-id="2eb86-250">It also provides an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="2eb86-251">Чтобы просмотреть сведения о каждом диске, разверните элемент имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="2eb86-251">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="2eb86-252">**Примечание**  Состояние шифрования тома съемных данных не отображается в этом отчете.</span><span class="sxs-lookup"><span data-stu-id="2eb86-252">**Note** The Removable Data Volume encryption status is not shown in this report.</span></span>

 

**<span data-ttu-id="2eb86-253">Отчет о соответствии компьютера BitLocker: поля сведений о компьютере</span><span class="sxs-lookup"><span data-stu-id="2eb86-253">BitLocker Computer Compliance Report: Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2eb86-254">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="2eb86-254">Column Name</span></span></th>
<th align="left"><span data-ttu-id="2eb86-255">Описание</span><span class="sxs-lookup"><span data-stu-id="2eb86-255">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-256">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="2eb86-256">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-257">Указанное пользователем DNS-имя компьютера, которое управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="2eb86-257">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-258">Доменное имя</span><span class="sxs-lookup"><span data-stu-id="2eb86-258">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-259">Полное доменное имя, в котором находится клиентский компьютер и управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="2eb86-259">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-260">Тип компьютера</span><span class="sxs-lookup"><span data-stu-id="2eb86-260">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-261">Тип компьютера.</span><span class="sxs-lookup"><span data-stu-id="2eb86-261">Type of computer.</span></span> <span data-ttu-id="2eb86-262">Допустимые типы не являются переносимыми и переносимыми.</span><span class="sxs-lookup"><span data-stu-id="2eb86-262">Valid types are Non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-263">Операционная система</span><span class="sxs-lookup"><span data-stu-id="2eb86-263">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-264">Тип операционной системы на клиентском компьютере с управляемым MBAM.</span><span class="sxs-lookup"><span data-stu-id="2eb86-264">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-265">Общее соответствие требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-265">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-266">Общее состояние соответствия требованиям компьютера, управляемого с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="2eb86-266">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="2eb86-267">Допустимые состояния соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="2eb86-267">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="2eb86-268">Обратите внимание на то, что состояние соответствия для каждого устройства (в приведенной ниже таблице) может указывать на разные состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="2eb86-268">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="2eb86-269">Однако это поле представляет состояние соответствия требованиям в соответствии с указанной политикой.</span><span class="sxs-lookup"><span data-stu-id="2eb86-269">However, this field represents that compliance state in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-270">Соответствие требованиям операционной системы</span><span class="sxs-lookup"><span data-stu-id="2eb86-270">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-271">Состояние соответствия требованиям операционной системы, управляемой MBAM.</span><span class="sxs-lookup"><span data-stu-id="2eb86-271">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="2eb86-272">Допустимые состояния соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="2eb86-272">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-273">Соответствие фиксированному диску с данными</span><span class="sxs-lookup"><span data-stu-id="2eb86-273">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-274">Состояние соответствия фиксированному диску с данными, управляемому с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="2eb86-274">Compliance status of the fixed data drive that is managed by MBAM.</span></span> <span data-ttu-id="2eb86-275">Допустимые состояния соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="2eb86-275">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-276">Дата последнего обновления</span><span class="sxs-lookup"><span data-stu-id="2eb86-276">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-277">Дата и время последнего обращения компьютера к серверу для отправки отчета о состоянии соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="2eb86-277">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="2eb86-278">Частота контактов настраивается с помощью параметров групповой политики.</span><span class="sxs-lookup"><span data-stu-id="2eb86-278">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-279">Исключение</span><span class="sxs-lookup"><span data-stu-id="2eb86-279">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-280">Состояние, указывающее на то, что пользователь не исключен из политики BitLocker или не исключен из нее.</span><span class="sxs-lookup"><span data-stu-id="2eb86-280">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-281">Исключенный пользователь</span><span class="sxs-lookup"><span data-stu-id="2eb86-281">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-282">Пользователь, исключаемый из политики BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2eb86-282">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-283">Дата освобождения</span><span class="sxs-lookup"><span data-stu-id="2eb86-283">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-284">Дата, когда был предоставлен доступ к исключению.</span><span class="sxs-lookup"><span data-stu-id="2eb86-284">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-285">Сведения о статусе соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="2eb86-285">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-286">Сообщения об ошибках и состоянии, связанные с состоянием соответствия компьютера согласно указанной политике.</span><span class="sxs-lookup"><span data-stu-id="2eb86-286">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-287">Стойкость шифра политики</span><span class="sxs-lookup"><span data-stu-id="2eb86-287">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-288">Стойкость шифра, выбранная администратором в спецификации политики MBAM (например, 128-bit с диффузором).</span><span class="sxs-lookup"><span data-stu-id="2eb86-288">Cipher strength selected by the Administrator during the MBAM policy specification (for example, 128-bit with diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-289">Политика: диск операционной системы</span><span class="sxs-lookup"><span data-stu-id="2eb86-289">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-290">Указывает, требуется ли шифрование для операционной системы и соответствующего типа предохранителя.</span><span class="sxs-lookup"><span data-stu-id="2eb86-290">Indicates if encryption is required for the operating system and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-291">Политика: несъемный диск с данными</span><span class="sxs-lookup"><span data-stu-id="2eb86-291">Policy: Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-292">Указывает, требуется ли шифрование для фиксированного диска с данными.</span><span class="sxs-lookup"><span data-stu-id="2eb86-292">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-293">Изготовитель</span><span class="sxs-lookup"><span data-stu-id="2eb86-293">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-294">Название изготовителя компьютера, которое отображается в BIOS компьютера.</span><span class="sxs-lookup"><span data-stu-id="2eb86-294">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-295">Модель</span><span class="sxs-lookup"><span data-stu-id="2eb86-295">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-296">Название модели изготовителя компьютера, которое отображается в BIOS компьютера.</span><span class="sxs-lookup"><span data-stu-id="2eb86-296">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-297">Пользователи устройств</span><span class="sxs-lookup"><span data-stu-id="2eb86-297">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-298">Известные пользователи на компьютере, управляемом с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="2eb86-298">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="2eb86-299">Отчет о соответствии компьютера BitLocker: поля громкости компьютера</span><span class="sxs-lookup"><span data-stu-id="2eb86-299">BitLocker Computer Compliance Report: Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2eb86-300">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="2eb86-300">Column Name</span></span></th>
<th align="left"><span data-ttu-id="2eb86-301">Описание</span><span class="sxs-lookup"><span data-stu-id="2eb86-301">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-302">Буква диска</span><span class="sxs-lookup"><span data-stu-id="2eb86-302">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-303">Буква диска компьютера, назначенная пользователем на определенный диск.</span><span class="sxs-lookup"><span data-stu-id="2eb86-303">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-304">Тип диска</span><span class="sxs-lookup"><span data-stu-id="2eb86-304">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-305">Тип диска.</span><span class="sxs-lookup"><span data-stu-id="2eb86-305">Type of drive.</span></span> <span data-ttu-id="2eb86-306">Допустимые значения: диск операционной системы и фиксированный диск с данными.</span><span class="sxs-lookup"><span data-stu-id="2eb86-306">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="2eb86-307">Это физические диски, а не логические тома.</span><span class="sxs-lookup"><span data-stu-id="2eb86-307">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-308">Стойкость шифра</span><span class="sxs-lookup"><span data-stu-id="2eb86-308">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-309">Стойкость шифра, выбранная администратором в течение MBAM политики.</span><span class="sxs-lookup"><span data-stu-id="2eb86-309">Cipher strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-310">Типы предохранителей</span><span class="sxs-lookup"><span data-stu-id="2eb86-310">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-311">Тип предохранителя, выбранный с помощью политики, используемой для шифрования операционной системы или фиксированного диска с данными.</span><span class="sxs-lookup"><span data-stu-id="2eb86-311">Type of protector selected through the policy used to encrypt an operating system or fixed data drive.</span></span> <span data-ttu-id="2eb86-312">Допустимые типы предохранителей для операционной системы — TPM или TPM + PIN-код.</span><span class="sxs-lookup"><span data-stu-id="2eb86-312">The valid protector types for an operating system are TPM or TPM+PIN.</span></span> <span data-ttu-id="2eb86-313">Допустимый тип предохранителя для фиксированного диска с данными — это пароль.</span><span class="sxs-lookup"><span data-stu-id="2eb86-313">The valid protector type for a fixed data drive is a password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2eb86-314">Состояние предохранителя</span><span class="sxs-lookup"><span data-stu-id="2eb86-314">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-315">Указывает на то, что на компьютере, управляемом MBAM, включен тип предохранителя, указанный в политике.</span><span class="sxs-lookup"><span data-stu-id="2eb86-315">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="2eb86-316">Допустимые состояния: ON и OFF.</span><span class="sxs-lookup"><span data-stu-id="2eb86-316">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2eb86-317">Состояние шифрования</span><span class="sxs-lookup"><span data-stu-id="2eb86-317">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="2eb86-318">Состояние шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="2eb86-318">Encryption state of the drive.</span></span> <span data-ttu-id="2eb86-319">Допустимые состояния шифруются, а не шифруются и шифруются.</span><span class="sxs-lookup"><span data-stu-id="2eb86-319">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2eb86-320">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2eb86-320">Related topics</span></span>


[<span data-ttu-id="2eb86-321">Мониторинг и создание отчетов по соответствию BitLocker с помощью MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2eb86-321">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

 

## <span data-ttu-id="2eb86-322">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="2eb86-322">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="2eb86-323">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="2eb86-323">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="2eb86-324">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="2eb86-324">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





