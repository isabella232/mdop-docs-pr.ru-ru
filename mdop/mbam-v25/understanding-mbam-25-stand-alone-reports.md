---
title: Общие сведения об изолированных отчетах MBAM 2.5
description: Общие сведения об изолированных отчетах MBAM 2.5
author: dansimp
ms.assetid: 78b5aaf4-8257-4722-8eb9-e0de48db6a11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45e84c7c3b2bcb1602890c7c5a09592324da691e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812776"
---
# <span data-ttu-id="8666e-103">Общие сведения об изолированных отчетах MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8666e-103">Understanding MBAM 2.5 Stand-alone Reports</span></span>


<span data-ttu-id="8666e-104">В этой статье описаны отчеты, доступные при работе с администрированием и мониторингом Microsoft BitLocker (MBAM) в изолированной топологии.</span><span class="sxs-lookup"><span data-stu-id="8666e-104">This topic describes the reports that are available when you are running Microsoft BitLocker Administration and Monitoring (MBAM) in the Stand-alone topology.</span></span>

**<span data-ttu-id="8666e-105">Примечание.</span><span class="sxs-lookup"><span data-stu-id="8666e-105">Note</span></span>**  
<span data-ttu-id="8666e-106">Если вы используете MBAM с топологией интеграции Configuration Manager, вы создаете отчеты из Configuration Manager, а не из MBAM.</span><span class="sxs-lookup"><span data-stu-id="8666e-106">If you are running MBAM with the Configuration Manager Integration topology, you generate reports from Configuration Manager rather than from MBAM.</span></span> <span data-ttu-id="8666e-107">Дополнительные сведения об этих отчетах можно найти [в разделе Просмотр отчетов MBAM 2,5 для топологии интеграции Configuration Manager](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) .</span><span class="sxs-lookup"><span data-stu-id="8666e-107">See [Viewing MBAM 2.5 Reports for the Configuration Manager Integration Topology](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) for more information about these reports.</span></span>



## <span data-ttu-id="8666e-108">Общие сведения об изолированных отчетах о топологии MBAM</span><span class="sxs-lookup"><span data-stu-id="8666e-108">Understanding the MBAM Stand-alone topology reports</span></span>


<span data-ttu-id="8666e-109">MBAM предоставляет три типа отчетов, которые можно использовать для отслеживания соответствия требованиям BitLocker для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="8666e-109">MBAM provides three report types that you can use to monitor your organization for BitLocker compliance:</span></span>

-   [<span data-ttu-id="8666e-110">Отчет о соответствии требованиям предприятия</span><span class="sxs-lookup"><span data-stu-id="8666e-110">Enterprise Compliance Report</span></span>](#bkmk-enterprisecompliance)

-   [<span data-ttu-id="8666e-111">Отчет о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="8666e-111">Computer Compliance Report</span></span>](#bkmk-compliance)

-   [<span data-ttu-id="8666e-112">Отчет об аудите восстановления</span><span class="sxs-lookup"><span data-stu-id="8666e-112">Recovery Audit Report</span></span>](#bkmk-recovery)

<span data-ttu-id="8666e-113">Чтобы получить доступ к отчетам MBAM при запуске MBAM в изолированной топологии, откройте веб-браузер и откройте веб-сайт администрирования и наблюдения.</span><span class="sxs-lookup"><span data-stu-id="8666e-113">To access MBAM reports when you are running MBAM in the Stand-alone topology, open a web browser, and then open the Administration and Monitoring Website.</span></span> <span data-ttu-id="8666e-114">В левой строке меню выберите пункт **отчеты** .</span><span class="sxs-lookup"><span data-stu-id="8666e-114">Select **Reports** in the left menu bar.</span></span> <span data-ttu-id="8666e-115">В верхней строке меню выберите отчет, который требуется создать.</span><span class="sxs-lookup"><span data-stu-id="8666e-115">From the top menu bar, select the kind of report that you want to generate.</span></span> <span data-ttu-id="8666e-116">Дополнительные сведения о создании этих отчетов можно найти в разделе [Создание автономных отчетов MBAM 2,5](generating-mbam-25-stand-alone-reports.md).</span><span class="sxs-lookup"><span data-stu-id="8666e-116">For more information about generating these reports, see [Generating MBAM 2.5 Stand-alone Reports](generating-mbam-25-stand-alone-reports.md).</span></span>

### <a href="" id="bkmk-enterprisecompliance"></a><span data-ttu-id="8666e-117">Отчет о соответствии требованиям предприятия</span><span class="sxs-lookup"><span data-stu-id="8666e-117">Enterprise Compliance Report</span></span>

<span data-ttu-id="8666e-118">Этот тип отчета используется для сбора сведений о соответствии общего соответствия требованиям BitLocker в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="8666e-118">Use this report type to collect information about overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="8666e-119">С помощью фильтров можно сузить результаты поиска, чтобы узнать больше о состоянии соответствия требованиям и состоянии ошибки на компьютерах в Организации.</span><span class="sxs-lookup"><span data-stu-id="8666e-119">You can use filters to narrow your search results to learn more about the compliance state and error status of computers in your organization.</span></span>

**<span data-ttu-id="8666e-120">Общие сведения о корпоративном соответствии</span><span class="sxs-lookup"><span data-stu-id="8666e-120">Enterprise Compliance Overview</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8666e-121">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="8666e-121">Column Name</span></span></th>
<th align="left"><span data-ttu-id="8666e-122">Описание</span><span class="sxs-lookup"><span data-stu-id="8666e-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-123">Управляемые компьютеры</span><span class="sxs-lookup"><span data-stu-id="8666e-123">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-124">Количество компьютеров, которым MBAM управлять.</span><span class="sxs-lookup"><span data-stu-id="8666e-124">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-125">% Соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="8666e-125">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-126">Процент соответствия требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="8666e-126">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-127">% Не соответствует требованиям</span><span class="sxs-lookup"><span data-stu-id="8666e-127">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-128">Процент несоответствующих требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="8666e-128">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-129">% Исключении</span><span class="sxs-lookup"><span data-stu-id="8666e-129">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-130">Процент компьютеров, исключаемых из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8666e-130">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-131">% Без исключения</span><span class="sxs-lookup"><span data-stu-id="8666e-131">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-132">Процент компьютеров без исключения из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8666e-132">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-133">SDMI</span><span class="sxs-lookup"><span data-stu-id="8666e-133">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-134">Процент соответствия требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="8666e-134">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-135">Не соответствует требованиям</span><span class="sxs-lookup"><span data-stu-id="8666e-135">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-136">Процент несоответствующих требованиям компьютеров в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="8666e-136">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-137">Облагаемый</span><span class="sxs-lookup"><span data-stu-id="8666e-137">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-138">Общее количество компьютеров, исключаемых из требования шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8666e-138">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-139">Без исключения</span><span class="sxs-lookup"><span data-stu-id="8666e-139">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-140">Общее количество компьютеров без исключения из требований шифрования BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8666e-140">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="8666e-141">Сведения о компьютере в соответствии с требованиями предприятия</span><span class="sxs-lookup"><span data-stu-id="8666e-141">Enterprise Compliance Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8666e-142">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="8666e-142">Column Name</span></span></th>
<th align="left"><span data-ttu-id="8666e-143">Описание</span><span class="sxs-lookup"><span data-stu-id="8666e-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-144">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="8666e-144">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-145">Указанное пользователем DNS-имя, управляемое MBAM.</span><span class="sxs-lookup"><span data-stu-id="8666e-145">User-specified DNS name that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-146">Доменное имя</span><span class="sxs-lookup"><span data-stu-id="8666e-146">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-147">Полное доменное имя, в котором находится клиентский компьютер и управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="8666e-147">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-148">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="8666e-148">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-149">Состояние соответствия для компьютера согласно политике, указанной для компьютера.</span><span class="sxs-lookup"><span data-stu-id="8666e-149">State of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="8666e-150">Состояния не соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="8666e-150">The states are Noncompliant and Compliant.</span></span> <span data-ttu-id="8666e-151">Дополнительные сведения о том, как интерпретировать состояние соответствия требованиям, можно найти в следующей таблице "требования соответствия требованиям предприятия".</span><span class="sxs-lookup"><span data-stu-id="8666e-151">See the following Enterprise Compliance Report Compliance States table for more information about how to interpret compliance states.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-152">Исключение</span><span class="sxs-lookup"><span data-stu-id="8666e-152">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-153">Состояние, указывающее на то, исключен ли этот компьютер из политики BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8666e-153">Status that indicates whether this computer is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-154">Сведения о статусе соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="8666e-154">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-155">Сообщения об ошибках и состоянии, связанные с состоянием соответствия компьютера согласно указанной политике.</span><span class="sxs-lookup"><span data-stu-id="8666e-155">Error and status messages about the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-156">Последний контакт</span><span class="sxs-lookup"><span data-stu-id="8666e-156">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-157">Дата и время последнего обращения компьютера к серверу для отправки отчета о состоянии соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="8666e-157">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="8666e-158">Частота контактов настраивается.</span><span class="sxs-lookup"><span data-stu-id="8666e-158">The contact frequency is configurable.</span></span> <span data-ttu-id="8666e-159">Дополнительные сведения можно найти в разделе Параметры групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="8666e-159">For more information, see the MBAM Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-compliance"></a><span data-ttu-id="8666e-160">Отчет о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="8666e-160">Computer Compliance Report</span></span>

<span data-ttu-id="8666e-161">Этот тип отчета используется для сбора сведений, относящихся к компьютеру или пользователю.</span><span class="sxs-lookup"><span data-stu-id="8666e-161">Use this report type to collect information that is specific to a computer or user.</span></span>

<span data-ttu-id="8666e-162">Чтобы просмотреть этот отчет, щелкните имя компьютера в отчете соответствие требованиям предприятия или введите имя компьютера в отчете соответствие требованиям к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="8666e-162">View this report by clicking the computer name in the Enterprise Compliance Report, or by typing the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="8666e-163">Этот отчет содержит подробные сведения о шифровании каждого диска (операционной системы и несъемных дисков с данными) на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8666e-163">This report shows detailed encryption information about each drive (operating system and fixed data drives) on a computer.</span></span> <span data-ttu-id="8666e-164">Кроме того, она указывает политику, которая применяется к каждому типу дисков на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8666e-164">It also indicates the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="8666e-165">Чтобы просмотреть сведения о каждом диске, разверните элемент имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="8666e-165">To view the details of each drive, expand the Computer Name entry.</span></span>

**<span data-ttu-id="8666e-166">Примечание.</span><span class="sxs-lookup"><span data-stu-id="8666e-166">Note</span></span>**  
<span data-ttu-id="8666e-167">Состояние шифрования тома съемных данных не отображается в этом отчете.</span><span class="sxs-lookup"><span data-stu-id="8666e-167">Removable Data Volume encryption status is not shown in this report.</span></span>



**<span data-ttu-id="8666e-168">Поля отчета о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="8666e-168">Computer Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8666e-169">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="8666e-169">Column Name</span></span></th>
<th align="left"><span data-ttu-id="8666e-170">Описание</span><span class="sxs-lookup"><span data-stu-id="8666e-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-171">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="8666e-171">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-172">Указанное пользователем DNS-имя компьютера, управляемое с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="8666e-172">User-specified DNS computer name that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-173">Доменное имя</span><span class="sxs-lookup"><span data-stu-id="8666e-173">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-174">Полное доменное имя, в котором находится клиентский компьютер и управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="8666e-174">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-175">Тип компьютера</span><span class="sxs-lookup"><span data-stu-id="8666e-175">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-176">Тип компьютера.</span><span class="sxs-lookup"><span data-stu-id="8666e-176">Type of computer.</span></span> <span data-ttu-id="8666e-177">Допустимые типы не являются переносимыми и переносимыми.</span><span class="sxs-lookup"><span data-stu-id="8666e-177">Valid types are Non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-178">Операционная система</span><span class="sxs-lookup"><span data-stu-id="8666e-178">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-179">Тип операционной системы находится на клиентском компьютере, управляемом MBAM.</span><span class="sxs-lookup"><span data-stu-id="8666e-179">Operating system type found on the client computer that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-180">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="8666e-180">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-181">Общее состояние соответствия требованиям для компьютера, управляемого с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="8666e-181">Overall compliance status of the computer that is managed by MBAM.</span></span> <span data-ttu-id="8666e-182">Допустимые состояния соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="8666e-182">Valid states are Compliant and Noncompliant.</span></span></p>
<p><span data-ttu-id="8666e-183">Обратите внимание, что состояние соответствия для каждого устройства (в приведенной ниже таблице) может указывать на разные состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="8666e-183">Notice that the compliance status per drive (see the following table) may indicate different compliance states.</span></span> <span data-ttu-id="8666e-184">Однако это поле представляет это состояние соответствия согласно указанной политике.</span><span class="sxs-lookup"><span data-stu-id="8666e-184">However, this field represents that compliance state, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-185">Стойкость шифра политики</span><span class="sxs-lookup"><span data-stu-id="8666e-185">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-186">Стойкость шифра, выбранная администратором во время MBAM политики (например, 128-bit с диффузором).</span><span class="sxs-lookup"><span data-stu-id="8666e-186">Cipher strength selected by the administrator during MBAM policy specification (for example, 128-bit with diffuser).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-187">Диск с операционной системой политики</span><span class="sxs-lookup"><span data-stu-id="8666e-187">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-188">Указывает, требуется ли шифрование для операционной системы, и отображается соответствующий тип предохранителя.</span><span class="sxs-lookup"><span data-stu-id="8666e-188">Indicates if encryption is required for the operating system and shows the appropriate protector type.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-189">Политика — фиксированный диск с данными</span><span class="sxs-lookup"><span data-stu-id="8666e-189">Policy-Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-190">Указывает, требуется ли шифрование для фиксированного диска с данными.</span><span class="sxs-lookup"><span data-stu-id="8666e-190">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-191">Съемный диск с данными политики</span><span class="sxs-lookup"><span data-stu-id="8666e-191">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-192">Указывает, требуется ли шифрование для съемного диска.</span><span class="sxs-lookup"><span data-stu-id="8666e-192">Indicates if encryption is required for the removable drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-193">Пользователи устройств</span><span class="sxs-lookup"><span data-stu-id="8666e-193">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-194">Известные пользователи на компьютере, управляемом с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="8666e-194">Known users on the computer that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-195">Исключение</span><span class="sxs-lookup"><span data-stu-id="8666e-195">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-196">Состояние, указывающее на то, исключен ли этот компьютер из политики BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8666e-196">Status that indicates whether this computer is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-197">Изготовитель</span><span class="sxs-lookup"><span data-stu-id="8666e-197">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-198">Название изготовителя компьютера, которое отображается в BIOS компьютера.</span><span class="sxs-lookup"><span data-stu-id="8666e-198">Computer manufacturer name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-199">Модель</span><span class="sxs-lookup"><span data-stu-id="8666e-199">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-200">Название модели изготовителя компьютера, как оно отображается в BIOS компьютера.</span><span class="sxs-lookup"><span data-stu-id="8666e-200">Computer manufacturer model name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-201">Сведения о статусе соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="8666e-201">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-202">Сообщения об ошибках и состоянии, связанные с состоянием соответствия компьютера согласно указанной политике.</span><span class="sxs-lookup"><span data-stu-id="8666e-202">Error and status messages about the compliance state of the computer, in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-203">Последний контакт</span><span class="sxs-lookup"><span data-stu-id="8666e-203">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-204">Дата и время последнего обращения компьютера к серверу для отправки отчета о состоянии соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="8666e-204">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="8666e-205">Частота контактов настраивается.</span><span class="sxs-lookup"><span data-stu-id="8666e-205">The contact frequency is configurable.</span></span> <span data-ttu-id="8666e-206">Дополнительные сведения можно найти в разделе Параметры групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="8666e-206">For more information, see the MBAM Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="8666e-207">Поля "диск" для отчета о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="8666e-207">Computer Compliance Report Drive Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8666e-208">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="8666e-208">Column Name</span></span></th>
<th align="left"><span data-ttu-id="8666e-209">Описание</span><span class="sxs-lookup"><span data-stu-id="8666e-209">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-210">Буква диска</span><span class="sxs-lookup"><span data-stu-id="8666e-210">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-211">Буква диска компьютера, назначенная пользователем на определенный диск.</span><span class="sxs-lookup"><span data-stu-id="8666e-211">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-212">Тип диска</span><span class="sxs-lookup"><span data-stu-id="8666e-212">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-213">Тип диска.</span><span class="sxs-lookup"><span data-stu-id="8666e-213">Type of drive.</span></span> <span data-ttu-id="8666e-214">Допустимые значения: диск операционной системы и фиксированный диск с данными.</span><span class="sxs-lookup"><span data-stu-id="8666e-214">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="8666e-215">Это физические диски, а не логические тома.</span><span class="sxs-lookup"><span data-stu-id="8666e-215">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-216">Стойкость шифра</span><span class="sxs-lookup"><span data-stu-id="8666e-216">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-217">Стойкость шифра, выбранная администратором в течение MBAM политики.</span><span class="sxs-lookup"><span data-stu-id="8666e-217">Cipher strength selected by the administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-218">Тип предохранителя</span><span class="sxs-lookup"><span data-stu-id="8666e-218">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-219">Тип предохранителя, выбранный с помощью параметра групповой политики, используемого для шифрования операционной системы или фиксированного объема данных.</span><span class="sxs-lookup"><span data-stu-id="8666e-219">Type of protector selected through the Group Policy setting used to encrypt an operating system or fixed data volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-220">Состояние предохранителя</span><span class="sxs-lookup"><span data-stu-id="8666e-220">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-221">Указывает на то, что компьютер, управляемый MBAM, включил Тип предохранителя, указанный в политике.</span><span class="sxs-lookup"><span data-stu-id="8666e-221">Indicates that the computer being managed by MBAM has enabled the protector type that is specified in the policy.</span></span> <span data-ttu-id="8666e-222">Допустимые состояния: ON и OFF.</span><span class="sxs-lookup"><span data-stu-id="8666e-222">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-223">Состояние шифрования</span><span class="sxs-lookup"><span data-stu-id="8666e-223">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-224">Состояние шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="8666e-224">Encryption state of the drive.</span></span> <span data-ttu-id="8666e-225">Допустимые состояния шифруются, а не шифруются и шифруются.</span><span class="sxs-lookup"><span data-stu-id="8666e-225">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-226">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="8666e-226">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-227">Состояние, указывающее, соответствует ли диск требованиям политики.</span><span class="sxs-lookup"><span data-stu-id="8666e-227">State that indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="8666e-228">Состояния не соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="8666e-228">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-229">Сведения о статусе соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="8666e-229">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-230">Сообщения об ошибках и состоянии соответствия требованиям компьютера согласно указанной политике.</span><span class="sxs-lookup"><span data-stu-id="8666e-230">Error and status messages of the compliance state of the computer, according to the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-recovery"></a><span data-ttu-id="8666e-231">Отчет об аудите восстановления</span><span class="sxs-lookup"><span data-stu-id="8666e-231">Recovery Audit Report</span></span>

<span data-ttu-id="8666e-232">Этот тип отчета используется для аудита пользователей, которые запросили доступ к ключам восстановления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8666e-232">Use this report type to audit users who have requested access to BitLocker recovery keys.</span></span> <span data-ttu-id="8666e-233">В отчете есть несколько фильтров, основанных на нужных критериях фильтрации.</span><span class="sxs-lookup"><span data-stu-id="8666e-233">The report offers several filters based on the desired filtering criteria.</span></span> <span data-ttu-id="8666e-234">Вы можете отфильтровать по определенному типу пользователя (в службе поддержки пользователей или для конечного пользователя), о том, что запрос завершился сбоем или был успешно, определен требуемый тип ключа и диапазон дат, в течение которого произошло извлечение.</span><span class="sxs-lookup"><span data-stu-id="8666e-234">You can filter on a specific type of user (a Help Desk user or an end user), whether the request failed or was successful, the specific type of key requested, and a date range during which the retrieval occurred.</span></span>

**<span data-ttu-id="8666e-235">Поля отчета аудита восстановления</span><span class="sxs-lookup"><span data-stu-id="8666e-235">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8666e-236">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="8666e-236">Column Name</span></span></th>
<th align="left"><span data-ttu-id="8666e-237">Описание</span><span class="sxs-lookup"><span data-stu-id="8666e-237">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-238">Дата и время запроса</span><span class="sxs-lookup"><span data-stu-id="8666e-238">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-239">Дата и время, когда запрос на получение ключа был выполнен конечным пользователем или пользователем службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="8666e-239">Date and time that a key retrieval request was made by an end user or Help Desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-240">Источник запросов аудита</span><span class="sxs-lookup"><span data-stu-id="8666e-240">Audit Request Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-241">Сайт, с которого был инициирован запрос.</span><span class="sxs-lookup"><span data-stu-id="8666e-241">The site from which the request was initiated.</span></span> <span data-ttu-id="8666e-242">У этого элемента может быть одно из двух значений: <strong> портал самообслуживания </strong> или служба <strong> поддержки </strong> .</span><span class="sxs-lookup"><span data-stu-id="8666e-242">This entry will have one of two values: <strong>Self-Service Portal</strong> or <strong>Helpdesk</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-243">Состояние запроса</span><span class="sxs-lookup"><span data-stu-id="8666e-243">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-244">Состояние запроса.</span><span class="sxs-lookup"><span data-stu-id="8666e-244">Status of the request.</span></span> <span data-ttu-id="8666e-245">Допустимые состояния успешно установлены (ключ был получен) или завершился сбоем (ключ не был получен).</span><span class="sxs-lookup"><span data-stu-id="8666e-245">Valid statuses are Successful (the key was retrieved), or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-246">Пользователь службы поддержки</span><span class="sxs-lookup"><span data-stu-id="8666e-246">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-247">Пользователь службы поддержки, который инициировал запрос на получение ключа.</span><span class="sxs-lookup"><span data-stu-id="8666e-247">Help Desk user who initiated the request for key retrieval.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8666e-248">Примечание.</span><span class="sxs-lookup"><span data-stu-id="8666e-248">Note</span></span></strong><br/><p><span data-ttu-id="8666e-249">Если пользователь расширенной справочной службы возводит ключ, не указывая конечного пользователя, <strong> поле конечного пользователя </strong> будет пустым.</span><span class="sxs-lookup"><span data-stu-id="8666e-249">If an Advanced Helpdesk User recovers the key without specifying the end user, the <strong>End User</strong> field will be blank.</span></span> <span data-ttu-id="8666e-250">Пользователь службы поддержки должен указать конечного пользователя, и этот пользователь будет отображаться в этом поле.</span><span class="sxs-lookup"><span data-stu-id="8666e-250">A standard Helpdesk User must specify the end user, and that user will appear in this field.</span></span></p>
<p><span data-ttu-id="8666e-251">При восстановлении с помощью портала самообслуживания будет указан конечный пользователь в этом поле и в <strong> поле конечных пользователей </strong> .</span><span class="sxs-lookup"><span data-stu-id="8666e-251">A recovery via the Self-Service Portal will list the requesting end user both in this field and in the <strong>End User</strong> field.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-252">Конечный пользователь</span><span class="sxs-lookup"><span data-stu-id="8666e-252">End User</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-253">Конечный пользователь, который инициировал запрос на получение ключа.</span><span class="sxs-lookup"><span data-stu-id="8666e-253">End user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-254">Компьютер</span><span class="sxs-lookup"><span data-stu-id="8666e-254">Computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-255">Имя компьютера, на котором был восстановлен компьютер.</span><span class="sxs-lookup"><span data-stu-id="8666e-255">Computer name of the computer that was recovered.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8666e-256">Тип ключа</span><span class="sxs-lookup"><span data-stu-id="8666e-256">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-257">Тип ключа, запрошенный пользователем службы технической поддержки или конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="8666e-257">Type of key that was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="8666e-258">Ниже перечислены три типа ключей, которые MBAM собирает.</span><span class="sxs-lookup"><span data-stu-id="8666e-258">The three types of keys that MBAM collects are:</span></span></p>
<ul>
<li><p><span data-ttu-id="8666e-259">Пароль ключа восстановления (используется для восстановления компьютера в режиме восстановления)</span><span class="sxs-lookup"><span data-stu-id="8666e-259">Recovery Key Password (used to recover a computer in recovery mode)</span></span></p></li>
<li><p><span data-ttu-id="8666e-260">ИД ключа восстановления (используется для восстановления компьютера в режиме восстановления от имени другого пользователя)</span><span class="sxs-lookup"><span data-stu-id="8666e-260">Recovery Key ID (used to recover a computer in recovery mode on behalf of another user)</span></span></p></li>
<li><p><span data-ttu-id="8666e-261">Хеш пароля TPM (используется для восстановления компьютера с заблокированным доверенным платформенным модулем)</span><span class="sxs-lookup"><span data-stu-id="8666e-261">TPM Password Hash (used to recover a computer with a locked TPM)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8666e-262">Описание причины</span><span class="sxs-lookup"><span data-stu-id="8666e-262">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="8666e-263">Причина, по которой указанный тип ключа запрашивался пользователем службы поддержки или конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="8666e-263">Reason the specified key type was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="8666e-264">Причины указаны в разделе Восстановление диска и управление функциями доверенного платформенного модуля на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="8666e-264">The reasons are specified in the Drive Recovery and Manage TPM features of the Administration and Monitoring Website.</span></span> <span data-ttu-id="8666e-265">Допустимые значения — это введенный пользователем текст или один из указанных ниже кодов причин.</span><span class="sxs-lookup"><span data-stu-id="8666e-265">The valid entries are user-entered text or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="8666e-266">Порядок загрузки операционной системы изменился</span><span class="sxs-lookup"><span data-stu-id="8666e-266">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="8666e-267">BIOS изменилась</span><span class="sxs-lookup"><span data-stu-id="8666e-267">BIOS Changed</span></span></p></li>
<li><p><span data-ttu-id="8666e-268">Изменены файлы операционной системы</span><span class="sxs-lookup"><span data-stu-id="8666e-268">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="8666e-269">Потерянный ключ запуска</span><span class="sxs-lookup"><span data-stu-id="8666e-269">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="8666e-270">Потерянный ПИН-код</span><span class="sxs-lookup"><span data-stu-id="8666e-270">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="8666e-271">Сброс доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="8666e-271">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="8666e-272">Утеряна парольная фраза</span><span class="sxs-lookup"><span data-stu-id="8666e-272">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="8666e-273">Потерялась смарт-карта</span><span class="sxs-lookup"><span data-stu-id="8666e-273">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="8666e-274">Сброс блокировки ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="8666e-274">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="8666e-275">Включить доверенный платформенный модуль</span><span class="sxs-lookup"><span data-stu-id="8666e-275">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="8666e-276">Отключение доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="8666e-276">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="8666e-277">Изменение пароля доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="8666e-277">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="8666e-278">Очистить доверенный платформенный модуль</span><span class="sxs-lookup"><span data-stu-id="8666e-278">Clear TPM</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="8666e-279">Примечание.</span><span class="sxs-lookup"><span data-stu-id="8666e-279">Note</span></span>**  
<span data-ttu-id="8666e-280">Результаты отчета можно сохранить в файл, нажав кнопку " **Экспорт** " в строке меню " **отчеты** ".</span><span class="sxs-lookup"><span data-stu-id="8666e-280">Report results can be saved to a file by clicking the **Export** button on the **Reports** menu bar.</span></span>




## <span data-ttu-id="8666e-281">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8666e-281">Related topics</span></span>


[<span data-ttu-id="8666e-282">Мониторинг и создание отчетов по соответствию BitLocker с помощью MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8666e-282">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[<span data-ttu-id="8666e-283">Создание изолированных отчетов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8666e-283">Generating MBAM 2.5 Stand-alone Reports</span></span>](generating-mbam-25-stand-alone-reports.md)



## <span data-ttu-id="8666e-284">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="8666e-284">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8666e-285">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8666e-285">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8666e-286">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8666e-286">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





