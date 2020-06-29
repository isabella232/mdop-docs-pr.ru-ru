---
title: Расшифровка отчетов MBAM
description: Расшифровка отчетов MBAM
author: dansimp
ms.assetid: 8778f333-760e-4f26-acb4-4e73b6fbb536
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c3ca5e4da4cbcea80c87520f0ecd05e1e7d6be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823812"
---
# <span data-ttu-id="f444b-103">Расшифровка отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="f444b-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="f444b-104">Если при установке средства администрирования и мониторинга Microsoft BitLocker вы выбрали изолированную топологию (MBAM), вы можете запускать различные отчеты в MBAM, чтобы отслеживать использование BitLocker и соответствие требованиям.</span><span class="sxs-lookup"><span data-stu-id="f444b-104">If you chose the Stand-alone topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), you can run different reports in MBAM to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="f444b-105">MBAM сообщает о соответствии требованиям и другие сведения о всех компьютерах и устройствах, которыми он управляет.</span><span class="sxs-lookup"><span data-stu-id="f444b-105">MBAM reports compliance and other information about all of the computers and devices it manages.</span></span> <span data-ttu-id="f444b-106">В этой статье приведены сведения, которые помогут вам понять вопросы администрирования и мониторинга Microsoft BitLocker для обеспечения соответствия требованиям для корпоративных и индивидуальных компьютеров, а также для восстановления ключей.</span><span class="sxs-lookup"><span data-stu-id="f444b-106">The information in this topic can be used to help you understand the Microsoft BitLocker Administration and Monitoring reports for enterprise and individual computer compliance and for key recovery activity.</span></span>

<span data-ttu-id="f444b-107">**Примечание**  Если вы выбрали топологию Configuration Manager, когда вы установили администрирование и мониторинг Microsoft BitLocker (MBAM), отчеты генерируются из Configuration Manager, а не из MBAM.</span><span class="sxs-lookup"><span data-stu-id="f444b-107">**Note** If you chose the Configuration Manager topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), reports are generated from Configuration Manager rather than from MBAM.</span></span> <span data-ttu-id="f444b-108">Дополнительные сведения об отчетах, которые выполняются из Configuration Manager, можно найти [в разделе сведения об отчетах о MBAM в Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="f444b-108">For more information about reports that are run from Configuration Manager, see [Understanding MBAM Reports in Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).</span></span>

 

## <span data-ttu-id="f444b-109">Общие сведения об отчетах</span><span class="sxs-lookup"><span data-stu-id="f444b-109">Understanding Reports</span></span>


<span data-ttu-id="f444b-110">Для доступа к функциям отчетов в центре администрирования и мониторинга Microsoft BitLocker откройте веб-браузер и откройте веб-сайт администрирования и наблюдения.</span><span class="sxs-lookup"><span data-stu-id="f444b-110">To access the Reports feature of Microsoft BitLocker Administration and Monitoring, open a web browser and open the Administration and Monitoring website.</span></span> <span data-ttu-id="f444b-111">В левой строке меню выберите пункт **отчеты** , а затем в верхней строке меню выберите отчет, который требуется создать.</span><span class="sxs-lookup"><span data-stu-id="f444b-111">Select **Reports** in the left menu bar and then select from the top menu bar the kind of report that you want to generate.</span></span>

### <span data-ttu-id="f444b-112">Отчет о соответствии требованиям предприятия</span><span class="sxs-lookup"><span data-stu-id="f444b-112">Enterprise Compliance Report</span></span>

<span data-ttu-id="f444b-113">Этот тип отчета используется для сбора сведений о соответствии общего соответствия требованиям BitLocker в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f444b-113">Use this report type to collect information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="f444b-114">Вы можете использовать различные фильтры, чтобы сузить результаты поиска до состояния соответствия требованиям и состояния ошибки.</span><span class="sxs-lookup"><span data-stu-id="f444b-114">You can use different filters to narrow your search results to Compliance state and Error status.</span></span> <span data-ttu-id="f444b-115">Данные отчета обновляются каждые шесть часов.</span><span class="sxs-lookup"><span data-stu-id="f444b-115">The report information is updated every six hours.</span></span>

**<span data-ttu-id="f444b-116">Поля отчета о соответствии требованиям предприятия</span><span class="sxs-lookup"><span data-stu-id="f444b-116">Enterprise Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f444b-117">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="f444b-117">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f444b-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f444b-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-119">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="f444b-119">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-120">Указанное пользователем DNS-имя, которое управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="f444b-120">User-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-121">Доменное имя</span><span class="sxs-lookup"><span data-stu-id="f444b-121">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-122">Полное доменное имя, в котором находится клиентский компьютер и управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="f444b-122">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-123">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f444b-123">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-124">Состояние соответствия для компьютера согласно политике, указанной для компьютера.</span><span class="sxs-lookup"><span data-stu-id="f444b-124">State of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="f444b-125">Состояния не соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="f444b-125">The states are Noncompliant and Compliant.</span></span> <span data-ttu-id="f444b-126">Дополнительные сведения о том, как интерпретировать состояние соответствия требованиям, можно найти в таблице "состояние соответствия требованиям предприятия".</span><span class="sxs-lookup"><span data-stu-id="f444b-126">See the Enterprise Compliance Report Compliance States table for more information about how to interpret compliance states.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-127">Сведения о статусе соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f444b-127">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-128">Сообщения об ошибках и состоянии соответствия требованиям компьютера согласно указанной политике.</span><span class="sxs-lookup"><span data-stu-id="f444b-128">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-129">Последний контакт</span><span class="sxs-lookup"><span data-stu-id="f444b-129">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-130">Дата и время последнего обращения компьютера к серверу для отправки отчета о состоянии соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="f444b-130">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="f444b-131">Частота контактов настраивается (см. раздел Параметры политики MBAM).</span><span class="sxs-lookup"><span data-stu-id="f444b-131">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f444b-132">Корпоративное состояние отчета о соответствии требованиям</span><span class="sxs-lookup"><span data-stu-id="f444b-132">Enterprise Compliance Report Compliance States</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f444b-133">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f444b-133">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="f444b-134">Исключение</span><span class="sxs-lookup"><span data-stu-id="f444b-134">Exemption</span></span></th>
<th align="left"><span data-ttu-id="f444b-135">Описание</span><span class="sxs-lookup"><span data-stu-id="f444b-135">Description</span></span></th>
<th align="left"><span data-ttu-id="f444b-136">Действие пользователя</span><span class="sxs-lookup"><span data-stu-id="f444b-136">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-137">Несоответствующих</span><span class="sxs-lookup"><span data-stu-id="f444b-137">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-138">Не исключено</span><span class="sxs-lookup"><span data-stu-id="f444b-138">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-139">Компьютер не соответствует политике в соответствии с указанной политикой.</span><span class="sxs-lookup"><span data-stu-id="f444b-139">The computer is noncompliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-140">Разверните данные отчета о соответствии компьютера, щелкнув <strong> имя компьютера </strong> и определите, соответствует ли состояние каждого диска указанной политике.</span><span class="sxs-lookup"><span data-stu-id="f444b-140">Expand the Computer Compliance Report details by clicking <strong>Computer Name</strong>, and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="f444b-141">Если состояние шифрования указывает на то, что компьютер не зашифрован, возможно, выполняется шифрование или на компьютере возникла ошибка.</span><span class="sxs-lookup"><span data-stu-id="f444b-141">If the encryption state indicates that the computer is not encrypted, encryption may be in process, or there is an error on the computer.</span></span> <span data-ttu-id="f444b-142">Если ошибка не возникает, вероятная причина заключается в том, что компьютер по-прежнему находится в процессе подключения или установки состояния шифрования.</span><span class="sxs-lookup"><span data-stu-id="f444b-142">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="f444b-143">Чтобы определить, изменилось ли состояние, вернитесь позже.</span><span class="sxs-lookup"><span data-stu-id="f444b-143">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-144">SDMI</span><span class="sxs-lookup"><span data-stu-id="f444b-144">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-145">Не исключено</span><span class="sxs-lookup"><span data-stu-id="f444b-145">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-146">В соответствии с указанной политикой компьютер соответствует требованиям.</span><span class="sxs-lookup"><span data-stu-id="f444b-146">The computer is compliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-147">Никаких действий не требуется; состояние компьютера можно подтвердить, просмотрев отчет о соответствии компьютера требованиям.</span><span class="sxs-lookup"><span data-stu-id="f444b-147">No action needed; the state of the computer can be confirmed by viewing the Computer Compliance Report.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f444b-148">Отчет о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="f444b-148">Computer Compliance Report</span></span>

<span data-ttu-id="f444b-149">Этот тип отчета используется для сбора сведений, относящихся к компьютеру или пользователю.</span><span class="sxs-lookup"><span data-stu-id="f444b-149">Use this report type to collect information that is specific to a computer or user.</span></span>

<span data-ttu-id="f444b-150">Этот отчет можно просмотреть, щелкнув имя компьютера в отчете о соответствии требованиям предприятия или введя имя компьютера в отчете соответствие требованиям к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="f444b-150">This report can be viewed by clicking the computer name in the Enterprise Compliance Report, or by typing the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="f444b-151">Отчет о соответствии компьютера содержит подробные сведения о шифровании каждого диска (операционной системы и фиксированных дисков с данными) на компьютере, а также сведения о политике, применяемой к каждому типу дисков на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f444b-151">The Computer Compliance Report provides detailed encryption information about each drive (operating system and fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="f444b-152">Чтобы просмотреть сведения о каждом диске, разверните элемент имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="f444b-152">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="f444b-153">**Примечание**  Состояние шифрования тома съемных данных не будет отображаться в отчете.</span><span class="sxs-lookup"><span data-stu-id="f444b-153">**Note** Removable Data Volume encryption status will not be shown in the report.</span></span>

 

**<span data-ttu-id="f444b-154">Поля отчета о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="f444b-154">Computer Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f444b-155">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="f444b-155">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f444b-156">Описание</span><span class="sxs-lookup"><span data-stu-id="f444b-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-157">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="f444b-157">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-158">Указанное пользователем DNS-имя компьютера, которое управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="f444b-158">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-159">Доменное имя</span><span class="sxs-lookup"><span data-stu-id="f444b-159">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-160">Полное доменное имя, в котором находится клиентский компьютер и управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="f444b-160">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-161">Тип компьютера</span><span class="sxs-lookup"><span data-stu-id="f444b-161">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-162">Тип компьютера.</span><span class="sxs-lookup"><span data-stu-id="f444b-162">Type of computer.</span></span> <span data-ttu-id="f444b-163">Допустимые типы не являются переносимыми и переносимыми.</span><span class="sxs-lookup"><span data-stu-id="f444b-163">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-164">Операционная система</span><span class="sxs-lookup"><span data-stu-id="f444b-164">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-165">Тип операционной системы находится на клиентском компьютере с управляемым MBAM.</span><span class="sxs-lookup"><span data-stu-id="f444b-165">Operating system type found on the MBAM-managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-166">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f444b-166">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-167">Общее состояние соответствия требованиям компьютера, управляемого с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="f444b-167">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="f444b-168">Допустимые состояния соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="f444b-168">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="f444b-169">Обратите внимание, что состояние соответствия для каждого устройства (в приведенной ниже таблице) может указывать на разные состояния соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="f444b-169">Notice that the compliance status per drive (see the following table) may indicate different compliance states.</span></span> <span data-ttu-id="f444b-170">Однако это поле представляет это состояние соответствия согласно указанной политике.</span><span class="sxs-lookup"><span data-stu-id="f444b-170">However, this field represents that compliance state, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-171">Стойкость шифра политики</span><span class="sxs-lookup"><span data-stu-id="f444b-171">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-172">Стойкость шифра, выбранная администратором во время MBAM политики (например, 128-bit с диффузором).</span><span class="sxs-lookup"><span data-stu-id="f444b-172">Cipher strength selected by the administrator during MBAM policy specification (for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-173">Диск с операционной системой политики</span><span class="sxs-lookup"><span data-stu-id="f444b-173">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-174">Указывает, требуется ли шифрование для операционной системы, и отображается соответствующий тип предохранителя.</span><span class="sxs-lookup"><span data-stu-id="f444b-174">Indicates if encryption is required for the operating system and shows the appropriate protector type.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-175">Политика — фиксированный диск с данными</span><span class="sxs-lookup"><span data-stu-id="f444b-175">Policy-Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-176">Указывает, требуется ли шифрование для фиксированного диска с данными.</span><span class="sxs-lookup"><span data-stu-id="f444b-176">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-177">Съемный диск с данными политики</span><span class="sxs-lookup"><span data-stu-id="f444b-177">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-178">Указывает, требуется ли шифрование для съемного диска.</span><span class="sxs-lookup"><span data-stu-id="f444b-178">Indicates if encryption is required for the removable drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-179">Пользователи устройств</span><span class="sxs-lookup"><span data-stu-id="f444b-179">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-180">Известные пользователи на компьютере, управляемом с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="f444b-180">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-181">Изготовитель</span><span class="sxs-lookup"><span data-stu-id="f444b-181">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-182">Название изготовителя компьютера, которое отображается в BIOS компьютера.</span><span class="sxs-lookup"><span data-stu-id="f444b-182">Computer manufacturer name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-183">Модель</span><span class="sxs-lookup"><span data-stu-id="f444b-183">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-184">Название модели изготовителя компьютера, как оно отображается в BIOS компьютера.</span><span class="sxs-lookup"><span data-stu-id="f444b-184">Computer manufacturer model name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-185">Сведения о статусе соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f444b-185">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-186">Сообщения об ошибках и состоянии соответствия требованиям компьютера в соответствии с указанной политикой.</span><span class="sxs-lookup"><span data-stu-id="f444b-186">Error and status messages of the compliance state of the computer, in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-187">Последний контакт</span><span class="sxs-lookup"><span data-stu-id="f444b-187">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-188">Дата и время последнего обращения компьютера к серверу для отправки отчета о состоянии соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="f444b-188">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="f444b-189">Частота контактов настраивается (см. раздел Параметры политики MBAM).</span><span class="sxs-lookup"><span data-stu-id="f444b-189">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f444b-190">Поля "диск" для отчета о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="f444b-190">Computer Compliance Report Drive Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f444b-191">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="f444b-191">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f444b-192">Описание</span><span class="sxs-lookup"><span data-stu-id="f444b-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-193">Буква диска</span><span class="sxs-lookup"><span data-stu-id="f444b-193">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-194">Буква диска компьютера, назначенная пользователем на определенный диск.</span><span class="sxs-lookup"><span data-stu-id="f444b-194">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-195">Тип диска</span><span class="sxs-lookup"><span data-stu-id="f444b-195">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-196">Тип диска.</span><span class="sxs-lookup"><span data-stu-id="f444b-196">Type of drive.</span></span> <span data-ttu-id="f444b-197">Допустимые значения: диск операционной системы и фиксированный диск с данными.</span><span class="sxs-lookup"><span data-stu-id="f444b-197">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="f444b-198">Это физические диски, а не логические тома.</span><span class="sxs-lookup"><span data-stu-id="f444b-198">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-199">Стойкость шифра</span><span class="sxs-lookup"><span data-stu-id="f444b-199">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-200">Стойкость шифра, выбранная администратором в течение MBAM политики.</span><span class="sxs-lookup"><span data-stu-id="f444b-200">Cipher strength selected by the administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-201">Тип предохранителя</span><span class="sxs-lookup"><span data-stu-id="f444b-201">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-202">Тип предохранителя, выбранный с помощью политики, используемой для шифрования операционной системы или фиксированного объема данных.</span><span class="sxs-lookup"><span data-stu-id="f444b-202">Type of protector selected via the policy used to encrypt an operating system or fixed data volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-203">Состояние предохранителя</span><span class="sxs-lookup"><span data-stu-id="f444b-203">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-204">Указывает на то, что компьютер, управляемый MBAM, включил Тип предохранителя, указанный в политике.</span><span class="sxs-lookup"><span data-stu-id="f444b-204">Indicates that the computer being managed by MBAM has enabled the protector type that is specified in the policy.</span></span> <span data-ttu-id="f444b-205">Допустимые состояния: ON и OFF.</span><span class="sxs-lookup"><span data-stu-id="f444b-205">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-206">Состояние шифрования</span><span class="sxs-lookup"><span data-stu-id="f444b-206">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-207">Состояние шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="f444b-207">Encryption state of the drive.</span></span> <span data-ttu-id="f444b-208">Допустимые состояния шифруются, а не шифруются и шифруются.</span><span class="sxs-lookup"><span data-stu-id="f444b-208">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-209">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f444b-209">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-210">Состояние, указывающее, соответствует ли диск требованиям политики.</span><span class="sxs-lookup"><span data-stu-id="f444b-210">State that indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="f444b-211">Состояния не соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="f444b-211">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-212">Сведения о статусе соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f444b-212">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-213">Сообщения об ошибках и состоянии соответствия требованиям компьютера согласно указанной политике.</span><span class="sxs-lookup"><span data-stu-id="f444b-213">Error and status messages of the compliance state of the computer, according to the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f444b-214">Отчет об аудите восстановления</span><span class="sxs-lookup"><span data-stu-id="f444b-214">Recovery Audit Report</span></span>

<span data-ttu-id="f444b-215">Этот тип отчета используется для аудита пользователей, которые запросили доступ к ключам восстановления.</span><span class="sxs-lookup"><span data-stu-id="f444b-215">Use this report type to audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="f444b-216">В отчете есть несколько фильтров, основанных на нужных критериях фильтрации.</span><span class="sxs-lookup"><span data-stu-id="f444b-216">The report offers several filters based on the desired filtering criteria.</span></span> <span data-ttu-id="f444b-217">Пользователи могут фильтровать данные определенного типа: либо пользователя в службе поддержки пользователей, либо конечных пользователей, будь это запрос неудачно или с указанием диапазона дат, в течение которого произошло получение.</span><span class="sxs-lookup"><span data-stu-id="f444b-217">Users can filter on a specific type of user, either a Help Desk user or an end user, whether the request failed or was successful, the specific type of key requested, and a date range during which the retrieval occurred.</span></span> <span data-ttu-id="f444b-218">Администратор может создавать контекстные отчеты на основе необходимых данных.</span><span class="sxs-lookup"><span data-stu-id="f444b-218">The administrator can produce contextual reports based on need.</span></span>

**<span data-ttu-id="f444b-219">Поля отчета аудита восстановления</span><span class="sxs-lookup"><span data-stu-id="f444b-219">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f444b-220">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="f444b-220">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f444b-221">Описание</span><span class="sxs-lookup"><span data-stu-id="f444b-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-222">Дата и время запроса</span><span class="sxs-lookup"><span data-stu-id="f444b-222">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-223">Дата и время, когда запрос на получение ключа был выполнен конечным пользователем или пользователем службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="f444b-223">Date and time that a key retrieval request was made by an end user or Help Desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-224">Состояние запроса</span><span class="sxs-lookup"><span data-stu-id="f444b-224">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-225">Состояние запроса.</span><span class="sxs-lookup"><span data-stu-id="f444b-225">Status of the request.</span></span> <span data-ttu-id="f444b-226">Действительные статусы либо успешно (был получен ключ), либо завершились сбоем (ключ не был получен).</span><span class="sxs-lookup"><span data-stu-id="f444b-226">Valid statuses are either Successful (the key was retrieved), or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-227">Пользователь службы поддержки</span><span class="sxs-lookup"><span data-stu-id="f444b-227">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-228">Пользователь службы поддержки, который инициировал запрос на получение ключа.</span><span class="sxs-lookup"><span data-stu-id="f444b-228">Help Desk user that initiated the request for key retrieval.</span></span> <span data-ttu-id="f444b-229">Примечание. Если пользователь службы поддержки получает ключ от имени конечного пользователя, поле конечного пользователя будет пустым.</span><span class="sxs-lookup"><span data-stu-id="f444b-229">Note: If the Help Desk user retrieves the key on behalf on an end-user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-230">Пользователь</span><span class="sxs-lookup"><span data-stu-id="f444b-230">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-231">Конечный пользователь, который инициировал запрос на получение ключа.</span><span class="sxs-lookup"><span data-stu-id="f444b-231">End user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f444b-232">Тип ключа</span><span class="sxs-lookup"><span data-stu-id="f444b-232">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-233">Тип ключа, запрошенный либо пользователем службы поддержки пользователей, либо конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="f444b-233">Type of key that was requested by either the Help Desk user or the end user.</span></span> <span data-ttu-id="f444b-234">Три типа ключей, которые MBAM собирает: пароль ключа восстановления (используется для восстановления компьютера в режиме восстановления), ИД ключа восстановления (используется для возврата компьютера в режиме восстановления от имени другого пользователя) и хеша пароля ДОВЕРЕНного платформенного модуля (используется для восстановления компьютера с заблокированным доверенным платформенным модулем).</span><span class="sxs-lookup"><span data-stu-id="f444b-234">The three types of keys that MBAM collects are: Recovery Key Password (used to recovery a computer in recovery mode), Recovery Key ID (used to recover a computer in recovery mode on behalf of another user), and TPM Password Hash (used to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f444b-235">Описание причины</span><span class="sxs-lookup"><span data-stu-id="f444b-235">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="f444b-236">Причина, по которой указанный тип ключа запрашивался пользователем службы поддержки или конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="f444b-236">Reason the specified Key Type was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="f444b-237">Причины указаны в разделе Восстановление диска и управление функциями доверенного платформенного модуля на веб-сайте администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="f444b-237">The reasons are specified in the Drive Recovery and Manage TPM features of the Administration and Monitoring website.</span></span> <span data-ttu-id="f444b-238">Допустимые значения: либо введенный пользователем текст, либо один из указанных ниже кодов причин.</span><span class="sxs-lookup"><span data-stu-id="f444b-238">The valid entries are either user-entered text, or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="f444b-239">Порядок загрузки операционной системы изменился</span><span class="sxs-lookup"><span data-stu-id="f444b-239">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="f444b-240">BIOS изменилась</span><span class="sxs-lookup"><span data-stu-id="f444b-240">BIOS Changed</span></span></p></li>
<li><p><span data-ttu-id="f444b-241">Изменены файлы операционной системы</span><span class="sxs-lookup"><span data-stu-id="f444b-241">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="f444b-242">Потерянный ключ запуска</span><span class="sxs-lookup"><span data-stu-id="f444b-242">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="f444b-243">Потерянный ПИН-код</span><span class="sxs-lookup"><span data-stu-id="f444b-243">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="f444b-244">Сброс доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="f444b-244">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="f444b-245">Утеряна парольная фраза</span><span class="sxs-lookup"><span data-stu-id="f444b-245">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="f444b-246">Потерялась смарт-карта</span><span class="sxs-lookup"><span data-stu-id="f444b-246">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="f444b-247">Сброс блокировки ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="f444b-247">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="f444b-248">Включить доверенный платформенный модуль</span><span class="sxs-lookup"><span data-stu-id="f444b-248">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="f444b-249">Отключение доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="f444b-249">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="f444b-250">Изменение пароля доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="f444b-250">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="f444b-251">Очистить доверенный платформенный модуль</span><span class="sxs-lookup"><span data-stu-id="f444b-251">Clear TPM</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f444b-252">**Примечание**  Результаты отчета можно сохранить в файл, нажав кнопку " **Экспорт** " в строке меню "отчеты".</span><span class="sxs-lookup"><span data-stu-id="f444b-252">**Note** Report results can be saved to a file by clicking the **Export** button on the reports menu bar.</span></span> <span data-ttu-id="f444b-253">Дополнительные сведения о том, как выполнять MBAM отчеты, приведены [в разделе Создание отчетов MBAM](how-to-generate-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="f444b-253">For more information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

 

## <span data-ttu-id="f444b-254">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f444b-254">Related topics</span></span>


[<span data-ttu-id="f444b-255">Мониторинг и создание отчетов по соответствию BitLocker с помощью MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f444b-255">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





