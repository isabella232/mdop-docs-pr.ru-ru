---
title: Расшифровка отчетов MBAM
description: Расшифровка отчетов MBAM
author: dansimp
ms.assetid: 34e4aaeb-7f89-41a1-b816-c6fe8397b060
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa64a4724c87a42774e569b556013bfec2ed5514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822869"
---
# <span data-ttu-id="f4875-103">Расшифровка отчетов MBAM</span><span class="sxs-lookup"><span data-stu-id="f4875-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="f4875-104">Средства администрирования и мониторинга Microsoft BitLocker (MBAM) создают различные отчеты для мониторинга использования и соответствия требованиям BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f4875-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="f4875-105">В этой статье описаны отчеты MBAM для обеспечения соответствия требованиям в масштабах предприятия, отдельных компьютеров, совместимости оборудования и восстановления ключей.</span><span class="sxs-lookup"><span data-stu-id="f4875-105">This topic describes the MBAM reports for enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span>

## <span data-ttu-id="f4875-106">Общие сведения об отчетах</span><span class="sxs-lookup"><span data-stu-id="f4875-106">Understanding Reports</span></span>


<span data-ttu-id="f4875-107">Чтобы получить доступ к функции "отчеты" MBAM, откройте веб-сайт администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4875-107">To access the Reports feature of MBAM, open the MBAM administration website.</span></span> <span data-ttu-id="f4875-108">В области навигации выберите пункт **отчеты** .</span><span class="sxs-lookup"><span data-stu-id="f4875-108">Select **Reports** in the navigation pane.</span></span> <span data-ttu-id="f4875-109">Затем в области основная область содержимого щелкните вкладку с типом отчета: **отчет о соответствии требованиям предприятия** **, отчет об** **оборудовании, отчет аудита оборудования**или **отчет аудита восстановления**.</span><span class="sxs-lookup"><span data-stu-id="f4875-109">Then, in the main content pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

### <span data-ttu-id="f4875-110">Отчет о соответствии требованиям предприятия</span><span class="sxs-lookup"><span data-stu-id="f4875-110">Enterprise Compliance Report</span></span>

<span data-ttu-id="f4875-111">В отчете о соответствии требованиям предприятия содержатся сведения об общих требованиях к BitLocker в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f4875-111">An Enterprise Compliance Report provides information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="f4875-112">Доступные фильтры для этого отчета позволяют сузить результаты поиска в соответствии с состоянием соответствия требованиям и состоянием ошибки.</span><span class="sxs-lookup"><span data-stu-id="f4875-112">The available filters for this report allow you to narrow your search results according to Compliance state and Error status.</span></span> <span data-ttu-id="f4875-113">Этот отчет выполняется каждые шесть часов.</span><span class="sxs-lookup"><span data-stu-id="f4875-113">This report runs every six hours.</span></span>

**<span data-ttu-id="f4875-114">Поля отчета о соответствии требованиям предприятия</span><span class="sxs-lookup"><span data-stu-id="f4875-114">Enterprise Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4875-115">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="f4875-115">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f4875-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f4875-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-117">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="f4875-117">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-118">Указанное пользователем DNS-имя, которое управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4875-118">The user-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-119">Доменное имя</span><span class="sxs-lookup"><span data-stu-id="f4875-119">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-120">Полное доменное имя, в котором находится клиентский компьютер и управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4875-120">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-121">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f4875-121">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-122">Состояние соответствия для компьютера согласно политике, указанной для компьютера.</span><span class="sxs-lookup"><span data-stu-id="f4875-122">The state of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="f4875-123">Возможные состояния несовместимы и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="f4875-123">The possible states are Noncompliant and Compliant.</span></span> <span data-ttu-id="f4875-124">Дополнительные сведения можно найти в статье сведения о требованиях к корпоративным требованиям.</span><span class="sxs-lookup"><span data-stu-id="f4875-124">For more information, see Enterprise Compliance Report Compliance States in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-125">Исключение</span><span class="sxs-lookup"><span data-stu-id="f4875-125">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-126">Состояние оборудования компьютера для определения идентификации типа оборудования и того, является ли компьютер исключенным из политики.</span><span class="sxs-lookup"><span data-stu-id="f4875-126">The state of the computer hardware for determining the identification of the hardware type and whether the computer is exempt from policy.</span></span> <span data-ttu-id="f4875-127">Существует три возможных состояния: неизвестное оборудование (тип оборудования не определен в MBAM), аппаратное освобождение (тип оборудования определен и был помечен как освобожденный от политики MBAM), и не исключено (определение оборудования определено и не исключено из политики).</span><span class="sxs-lookup"><span data-stu-id="f4875-127">There are three possible states: Hardware Unknown (the hardware type has not been identified by MBAM), Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy), and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-128">Пользователи устройств</span><span class="sxs-lookup"><span data-stu-id="f4875-128">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-129">Известные пользователи на компьютере, управляемом с помощью MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4875-129">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-130">Сведения о статусе соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f4875-130">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-131">Сообщения об ошибках и состоянии, связанные с состоянием соответствия компьютера согласно указанной политике.</span><span class="sxs-lookup"><span data-stu-id="f4875-131">Error and status messages about the compliance state of the computer in accordance to the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-132">Последний контакт</span><span class="sxs-lookup"><span data-stu-id="f4875-132">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-133">Дата и время последнего обращения компьютера к серверу для отправки отчета о состоянии соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="f4875-133">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="f4875-134">Это время можно настраивать.</span><span class="sxs-lookup"><span data-stu-id="f4875-134">This time is configurable.</span></span> <span data-ttu-id="f4875-135">Просмотрите параметры политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4875-135">See MBAM policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f4875-136">Корпоративное состояние отчета о соответствии требованиям</span><span class="sxs-lookup"><span data-stu-id="f4875-136">Enterprise Compliance Report Compliance states</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4875-137">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f4875-137">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="f4875-138">Исключение</span><span class="sxs-lookup"><span data-stu-id="f4875-138">Exemption</span></span></th>
<th align="left"><span data-ttu-id="f4875-139">Описание</span><span class="sxs-lookup"><span data-stu-id="f4875-139">Description</span></span></th>
<th align="left"><span data-ttu-id="f4875-140">Действие пользователя</span><span class="sxs-lookup"><span data-stu-id="f4875-140">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-141">Несоответствующих</span><span class="sxs-lookup"><span data-stu-id="f4875-141">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-142">Не исключено</span><span class="sxs-lookup"><span data-stu-id="f4875-142">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-143">На компьютере не установлены соответствия согласно указанной политике, а тип оборудования не указан как исключение из политики.</span><span class="sxs-lookup"><span data-stu-id="f4875-143">The computer is noncompliant according to the specified policy, and the hardware type has not been indicated as exempt from policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-144">Щелкните <strong> имя компьютера </strong> , чтобы развернуть отчет о соответствии компьютера и определить, соответствует ли состояние каждого устройства указанной политике.</span><span class="sxs-lookup"><span data-stu-id="f4875-144">Click <strong>Computer Name</strong> to expand the Computer Compliance Report and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="f4875-145">Если состояние шифрования указывает на то, что компьютер не зашифрован, шифрование может продолжать выполняться, или на компьютере может быть обнаружена ошибка.</span><span class="sxs-lookup"><span data-stu-id="f4875-145">If the encryption state indicates that the computer is not encrypted, encryption might still be in process, or there might be an error on the computer.</span></span> <span data-ttu-id="f4875-146">Если ошибка не возникает, вероятная причина заключается в том, что компьютер по-прежнему находится в процессе подключения или установки состояния шифрования.</span><span class="sxs-lookup"><span data-stu-id="f4875-146">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="f4875-147">Чтобы определить, изменилось ли состояние, вернитесь позже.</span><span class="sxs-lookup"><span data-stu-id="f4875-147">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-148">SDMI</span><span class="sxs-lookup"><span data-stu-id="f4875-148">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-149">Не исключено</span><span class="sxs-lookup"><span data-stu-id="f4875-149">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-150">Компьютер соответствует требованиям указанной политики.</span><span class="sxs-lookup"><span data-stu-id="f4875-150">The computer is compliant in accordance with the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-151">Никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="f4875-151">No Action needed.</span></span> <span data-ttu-id="f4875-152">При необходимости вы можете просмотреть отчет о соответствии компьютера, чтобы подтвердить состояние компьютера.</span><span class="sxs-lookup"><span data-stu-id="f4875-152">Optionally, you can view the Computer Compliance Report to confirm the state of the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-153">SDMI</span><span class="sxs-lookup"><span data-stu-id="f4875-153">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-154">Аппаратное освобождение</span><span class="sxs-lookup"><span data-stu-id="f4875-154">Hardware Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-155">При исключении типа оборудования.</span><span class="sxs-lookup"><span data-stu-id="f4875-155">If the Hardware type is exempt.</span></span> <span data-ttu-id="f4875-156">Независимо от того, как настроена политика или отдельное состояние каждого жесткого диска, общее состояние считается совместимым.</span><span class="sxs-lookup"><span data-stu-id="f4875-156">Regardless of how the policy is set or the individual status of each hard-drive, the overall state is considered to be compliant.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-157">Никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="f4875-157">No action needed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-158">SDMI</span><span class="sxs-lookup"><span data-stu-id="f4875-158">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-159">Неизвестная аппаратура</span><span class="sxs-lookup"><span data-stu-id="f4875-159">Hardware Unknown</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-160">MBAM распознает тип оборудования, но MBAM не знает, будет ли он исключен.</span><span class="sxs-lookup"><span data-stu-id="f4875-160">MBAM recognizes the hardware type, but MBAM does not know whether it is exempt or not exempt.</span></span> <span data-ttu-id="f4875-161">Это случается, если администратор не установил состояние совместимости для оборудования.</span><span class="sxs-lookup"><span data-stu-id="f4875-161">This occurs if the administrator has not set the Compatible status for the hardware.</span></span> <span data-ttu-id="f4875-162">Таким образом, MBAM по умолчанию возвращает соответствующее состояние.</span><span class="sxs-lookup"><span data-stu-id="f4875-162">Therefore, MBAM reverts to Compliant status by default.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-163">Это начальное состояние вновь развернутого клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4875-163">This is the initial state of a newly deployed MBAM client.</span></span> <span data-ttu-id="f4875-164">Обычно это переходное состояние.</span><span class="sxs-lookup"><span data-stu-id="f4875-164">It is typically only a transient state.</span></span> <span data-ttu-id="f4875-165">Даже если администратор пометил оборудование как совместимое, может быть задана значительная задержка или настраиваемое время ожидания перед тем, как клиентский компьютер снова сообщит об этом.</span><span class="sxs-lookup"><span data-stu-id="f4875-165">Even if the administrator has marked the Hardware as Compatible, there can be a significant delay or configurable wait time before the client computer reports back in.</span></span> <span data-ttu-id="f4875-166">Обратите внимание на время последнего контакта и снова после указанного интервала убедитесь в том, что состояние изменилось.</span><span class="sxs-lookup"><span data-stu-id="f4875-166">Make note of the time of Last Contact, and check in again after the specified interval to see if the state has changed.</span></span> <span data-ttu-id="f4875-167">Если состояние не изменилось, может возникнуть ошибка для этого компьютера или типа оборудования.</span><span class="sxs-lookup"><span data-stu-id="f4875-167">If the state has not changed, there may be an error for this computer or hardware type.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f4875-168">Отчет о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="f4875-168">Computer Compliance Report</span></span>

<span data-ttu-id="f4875-169">В отчете о соответствии компьютера отображаются сведения, относящиеся к компьютеру или пользователю.</span><span class="sxs-lookup"><span data-stu-id="f4875-169">The Computer Compliance Report displays information that is specific to a computer or user.</span></span>

<span data-ttu-id="f4875-170">В отчете о соответствии компьютера выводятся подробные сведения о шифровании и соответствующие политики для каждого диска компьютера, включая диски операционной системы и несъемные диски с данными.</span><span class="sxs-lookup"><span data-stu-id="f4875-170">The Computer Compliance Report provides detailed encryption information and applicable policies for each drive on a computer, including operating system drives and fixed data drives.</span></span> <span data-ttu-id="f4875-171">Чтобы просмотреть этот тип отчета, щелкните имя компьютера в отчете о соответствии требованиям предприятия или введите имя компьютера в отчете соответствие требованиям компьютера.</span><span class="sxs-lookup"><span data-stu-id="f4875-171">To view this report type, click the computer name in the Enterprise Compliance Report or type the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="f4875-172">Чтобы просмотреть сведения о каждом диске, разверните элемент имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="f4875-172">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="f4875-173">**Примечание**  Этот отчет не предоставляет состояние шифрования для съемных томов с данными.</span><span class="sxs-lookup"><span data-stu-id="f4875-173">**Note** This report does not provide encryption status for Removable Data Volumes.</span></span>

 

**<span data-ttu-id="f4875-174">Поля отчета о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="f4875-174">Computer Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4875-175">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="f4875-175">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f4875-176">Описание</span><span class="sxs-lookup"><span data-stu-id="f4875-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-177">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="f4875-177">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-178">Указанное пользователем DNS-имя компьютера, которое управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4875-178">The user-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-179">Доменное имя</span><span class="sxs-lookup"><span data-stu-id="f4875-179">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-180">Полное доменное имя, в котором находится клиентский компьютер и управляется MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4875-180">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-181">Тип компьютера</span><span class="sxs-lookup"><span data-stu-id="f4875-181">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-182">Тип переносимого компьютера.</span><span class="sxs-lookup"><span data-stu-id="f4875-182">The portability type of computer.</span></span> <span data-ttu-id="f4875-183">Допустимые типы не являются переносимыми и переносимыми.</span><span class="sxs-lookup"><span data-stu-id="f4875-183">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-184">Операционная система</span><span class="sxs-lookup"><span data-stu-id="f4875-184">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-185">Тип операционной системы, установленной на клиентском компьютере с управляемым MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4875-185">Operating System type installed on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-186">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f4875-186">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-187">Общее состояние соответствия компьютера, управляемого MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4875-187">The overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="f4875-188">Допустимые состояния соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="f4875-188">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="f4875-189">Несмотря на то что вы можете иметь совместимые и несоответствующие диски на одном и том же компьютере, это поле указывает на общую совместимость компьютера для указанной политики.</span><span class="sxs-lookup"><span data-stu-id="f4875-189">While it is possible to have Compliant and Noncompliant drives in the same computer, this field indicates the overall computer compliance per specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-190">Сила Cypher политики</span><span class="sxs-lookup"><span data-stu-id="f4875-190">Policy Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-191">Стойкость шифра, выбранная администратором во время MBAM политики.</span><span class="sxs-lookup"><span data-stu-id="f4875-191">The Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="f4875-192">Например, 128-bit с диффузором</span><span class="sxs-lookup"><span data-stu-id="f4875-192">For example, 128-bit with Diffuser</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-193">Диск с операционной системой политики</span><span class="sxs-lookup"><span data-stu-id="f4875-193">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-194">Указывает, требуется ли шифрование для O/S и типа предохранителя, как применимо.</span><span class="sxs-lookup"><span data-stu-id="f4875-194">Indicates whether encryption is required for the O/S and the protector type as applicable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-195">Фиксированный диск с данными политики</span><span class="sxs-lookup"><span data-stu-id="f4875-195">Policy Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-196">Указывает, требуется ли шифрование для жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="f4875-196">Indicates whether encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-197">Съемный диск с данными политики</span><span class="sxs-lookup"><span data-stu-id="f4875-197">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-198">Указывает, требуется ли шифрование для съемного диска.</span><span class="sxs-lookup"><span data-stu-id="f4875-198">Indicates whether encryption is required for the Removable Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-199">Пользователи устройств</span><span class="sxs-lookup"><span data-stu-id="f4875-199">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-200">Обеспечивает идентификацию известных пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f4875-200">Provides the identity of known users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-201">Исключение</span><span class="sxs-lookup"><span data-stu-id="f4875-201">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-202">Указывает, распознается ли тип аппаратуры компьютера MBAM, и, если известно, указывает, обозначен ли компьютер как освобожденный от политики.</span><span class="sxs-lookup"><span data-stu-id="f4875-202">Indicates whether the computer hardware type is recognized by MBAM and, if known, whether the computer has been indicated as exempt from policy.</span></span> <span data-ttu-id="f4875-203">Есть три состояния: оборудование неизвестно (тип оборудования не определен пользователем MBAM); Аппаратный освобождаемый (тип оборудования был идентифицирован и был помечен как исключение из политики MBAM); и не исключено (оборудование определено и не исключено из политики).</span><span class="sxs-lookup"><span data-stu-id="f4875-203">There are three states: Hardware Unknown (the hardware type has not been identified by MBAM); Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy); and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-204">Изготовитель</span><span class="sxs-lookup"><span data-stu-id="f4875-204">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-205">Название изготовителя компьютера, которое отображается в BIOS компьютера.</span><span class="sxs-lookup"><span data-stu-id="f4875-205">The computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-206">Модель</span><span class="sxs-lookup"><span data-stu-id="f4875-206">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-207">Название модели изготовителя компьютера в том виде, в каком оно отображается в BIOS компьютера.</span><span class="sxs-lookup"><span data-stu-id="f4875-207">The computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-208">Сведения о статусе соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f4875-208">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-209">Сообщения об ошибках и состоянии соответствия требованиям компьютера согласно указанной политике.</span><span class="sxs-lookup"><span data-stu-id="f4875-209">Error and status messages of the compliance state of the computer in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-210">Последний контакт</span><span class="sxs-lookup"><span data-stu-id="f4875-210">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-211">Дата и время последнего обращения компьютера к серверу для отправки отчета о состоянии соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="f4875-211">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="f4875-212">T</span><span class="sxs-lookup"><span data-stu-id="f4875-212">T</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f4875-213">Поля "диск" для отчета о соответствии компьютера</span><span class="sxs-lookup"><span data-stu-id="f4875-213">Computer Compliance Report Drive fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4875-214">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="f4875-214">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f4875-215">Описание</span><span class="sxs-lookup"><span data-stu-id="f4875-215">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-216">Буква диска</span><span class="sxs-lookup"><span data-stu-id="f4875-216">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-217">Буква диска компьютера, назначенная пользователем на этот конкретный диск.</span><span class="sxs-lookup"><span data-stu-id="f4875-217">Computer drive letter that was assigned to this particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-218">Тип диска</span><span class="sxs-lookup"><span data-stu-id="f4875-218">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-219">Тип диска.</span><span class="sxs-lookup"><span data-stu-id="f4875-219">Type of drive.</span></span> <span data-ttu-id="f4875-220">Допустимые значения: диск операционной системы и фиксированный диск с данными.</span><span class="sxs-lookup"><span data-stu-id="f4875-220">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="f4875-221">Это физические диски, а не логические тома.</span><span class="sxs-lookup"><span data-stu-id="f4875-221">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-222">Cypher сила</span><span class="sxs-lookup"><span data-stu-id="f4875-222">Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-223">Стойкость шифра, выбранная администратором в течение MBAM политики.</span><span class="sxs-lookup"><span data-stu-id="f4875-223">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-224">Тип предохранителя</span><span class="sxs-lookup"><span data-stu-id="f4875-224">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-225">Тип предохранителя, выбранный с помощью политики, используемой для шифрования операционной системы или фиксированного тома.</span><span class="sxs-lookup"><span data-stu-id="f4875-225">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="f4875-226">Допустимые типы предохранителей на диске операционной системы — TPM или TPM + PIN-код.</span><span class="sxs-lookup"><span data-stu-id="f4875-226">The valid protector types on an operating system drive are TPM or TPM+PIN.</span></span> <span data-ttu-id="f4875-227">Единственный допустимый тип предохранителя для фиксированного тома данных — Password (пароль).</span><span class="sxs-lookup"><span data-stu-id="f4875-227">The only valid protector type for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-228">Состояние предохранителя</span><span class="sxs-lookup"><span data-stu-id="f4875-228">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-229">Это поле указывает на то, включен ли на компьютере Тип предохранителя, указанный в политике.</span><span class="sxs-lookup"><span data-stu-id="f4875-229">This field indicates whether the computer has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="f4875-230">Допустимые состояния: ON и OFF.</span><span class="sxs-lookup"><span data-stu-id="f4875-230">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-231">Состояние шифрования</span><span class="sxs-lookup"><span data-stu-id="f4875-231">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-232">Это текущее состояние шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="f4875-232">This is the current encryption state of the drive.</span></span> <span data-ttu-id="f4875-233">Допустимые состояния шифруются, а не шифруются и шифруются.</span><span class="sxs-lookup"><span data-stu-id="f4875-233">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-234">Состояние соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f4875-234">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-235">Указывает, соответствует ли диск политике.</span><span class="sxs-lookup"><span data-stu-id="f4875-235">Indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="f4875-236">Состояния не соответствуют требованиям и не соответствуют требованиям.</span><span class="sxs-lookup"><span data-stu-id="f4875-236">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-237">Сведения о статусе соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f4875-237">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-238">Сведения об ошибках и сообщениях о состоянии, связанных с состоянием соответствия компьютера.</span><span class="sxs-lookup"><span data-stu-id="f4875-238">Contains error and status messages regarding the compliance state of the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f4875-239">Отчет аудита оборудования</span><span class="sxs-lookup"><span data-stu-id="f4875-239">Hardware Audit Report</span></span>

<span data-ttu-id="f4875-240">Этот отчет поможет вам в аудите изменений состояния совместимости оборудования для определенных компьютеров и их моделей.</span><span class="sxs-lookup"><span data-stu-id="f4875-240">This report can help you audit changes to the Hardware Compatibility status of specific computer makes and models.</span></span> <span data-ttu-id="f4875-241">Чтобы сузить область поиска, в этом отчете содержатся условия отбора, такие как тип изменения и время повторения.</span><span class="sxs-lookup"><span data-stu-id="f4875-241">To help you narrow your search results, this report includes filtering on criteria such as type of change and time of occurrence.</span></span> <span data-ttu-id="f4875-242">Каждое изменение состояния отслеживается пользователем, датой и временем.</span><span class="sxs-lookup"><span data-stu-id="f4875-242">Each state change is tracked by user and date and time.</span></span> <span data-ttu-id="f4875-243">Тип оборудования автоматически заполняется агентом MBAM, который выполняется на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="f4875-243">The Hardware Type is automatically populated by the MBAM agent that runs on the client computer.</span></span> <span data-ttu-id="f4875-244">Этот отчет отслеживает изменения пользователей для данных, собираемых непосредственно с компьютера, управляемого MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4875-244">This report tracks user changes to the information collected directly from the MBAM managed computer.</span></span> <span data-ttu-id="f4875-245">Типичное административное изменение меняется с совместимых на несовместимые.</span><span class="sxs-lookup"><span data-stu-id="f4875-245">A typical administrative change is changing from Compatible to incompatible.</span></span> <span data-ttu-id="f4875-246">Тем не менее, администратор также может изменить любое поле.</span><span class="sxs-lookup"><span data-stu-id="f4875-246">However, the administrator can also revise any field.</span></span>

**<span data-ttu-id="f4875-247">Поля отчета аудита оборудования</span><span class="sxs-lookup"><span data-stu-id="f4875-247">Hardware Audit Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4875-248">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="f4875-248">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f4875-249">Описание</span><span class="sxs-lookup"><span data-stu-id="f4875-249">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-250">Дата и время</span><span class="sxs-lookup"><span data-stu-id="f4875-250">Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-251">Дата и время внесения изменений в тип оборудования.</span><span class="sxs-lookup"><span data-stu-id="f4875-251">Date and time that a change was made to the Hardware Type.</span></span> <span data-ttu-id="f4875-252">Обратите внимание, что каждый уникальный тип оборудования назначается хотя бы для одной записи.</span><span class="sxs-lookup"><span data-stu-id="f4875-252">Note that every unique hardware type is assigned to at least one entry.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-253">Пользователь</span><span class="sxs-lookup"><span data-stu-id="f4875-253">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-254">Административный пользователь, который внес изменения в определенную запись.</span><span class="sxs-lookup"><span data-stu-id="f4875-254">Administrative user that has made the change for the particular entry.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-255">Тип изменения</span><span class="sxs-lookup"><span data-stu-id="f4875-255">Change Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-256">Тип изменения, внесенного в сведения о типе оборудования.</span><span class="sxs-lookup"><span data-stu-id="f4875-256">Type of change that was made to the hardware type information.</span></span> <span data-ttu-id="f4875-257">Допустимые значения: сложение (добавить запись), обновление (изменить существующий элемент) или удаление (удаление существующей записи).</span><span class="sxs-lookup"><span data-stu-id="f4875-257">Valid values are Addition (new entry), Update (change existing entry), or Deletion (remove existing entry).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-258">Исходное значение</span><span class="sxs-lookup"><span data-stu-id="f4875-258">Original Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-259">Значение спецификации аппаратного типа до внесения изменения.</span><span class="sxs-lookup"><span data-stu-id="f4875-259">Value of the hardware type specification before the change was made.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-260">Текущее значение</span><span class="sxs-lookup"><span data-stu-id="f4875-260">Current Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-261">Значение спецификации аппаратного типа после внесения изменения.</span><span class="sxs-lookup"><span data-stu-id="f4875-261">Value of the hardware type specification after the change was made.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f4875-262">Отчет об аудите восстановления</span><span class="sxs-lookup"><span data-stu-id="f4875-262">Recovery Audit Report</span></span>

<span data-ttu-id="f4875-263">Отчет аудита восстановления поможет вам в аудите пользователей, которые запросили доступ к ключам восстановления.</span><span class="sxs-lookup"><span data-stu-id="f4875-263">The Recovery Audit Report can help you audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="f4875-264">Условия фильтрации для этого отчета включают тип пользователя, который сделал запрос, тип запрашиваемого ключа, время повторения, успех или отказ, время возникновения и тип пользователя, запрашивающего (службы поддержки, конечных пользователей).</span><span class="sxs-lookup"><span data-stu-id="f4875-264">The filter criteria for this report includes type of user making the request, type of key requested, time of occurrence, success or fail, time of occurrence, and type of user requesting (help desk, end user).</span></span> <span data-ttu-id="f4875-265">Этот отчет позволяет администраторам создавать контекстные отчеты на основе необходимых данных.</span><span class="sxs-lookup"><span data-stu-id="f4875-265">This report enables administrators to produce contextual reports based on need.</span></span>

**<span data-ttu-id="f4875-266">Поля отчета аудита восстановления</span><span class="sxs-lookup"><span data-stu-id="f4875-266">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4875-267">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="f4875-267">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f4875-268">Описание</span><span class="sxs-lookup"><span data-stu-id="f4875-268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-269">Дата и время запроса</span><span class="sxs-lookup"><span data-stu-id="f4875-269">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-270">Дата и время, когда запрос на получение ключа был выполнен пользователем или пользователем службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="f4875-270">The date and time that a key retrieval request was made by an end user or help desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-271">Состояние запроса</span><span class="sxs-lookup"><span data-stu-id="f4875-271">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-272">Состояние запроса.</span><span class="sxs-lookup"><span data-stu-id="f4875-272">Status of the request.</span></span> <span data-ttu-id="f4875-273">Действительные статусы выполнены либо успешно (ключ был получен), либо произошел сбой (ключ не был получен).</span><span class="sxs-lookup"><span data-stu-id="f4875-273">Valid statuses are either Successful (the key was retrieved) or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-274">Пользователь службы поддержки</span><span class="sxs-lookup"><span data-stu-id="f4875-274">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-275">Пользователь службы поддержки, который инициировал запрос на получение ключа.</span><span class="sxs-lookup"><span data-stu-id="f4875-275">The help desk user who initiated the request for key retrieval.</span></span> <span data-ttu-id="f4875-276">Если пользователь службы технической поддержки получает ключ от имени конечного пользователя, поле конечного пользователя будет пустым.</span><span class="sxs-lookup"><span data-stu-id="f4875-276">If the help desk user retrieves the key on behalf of an end user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-277">Пользователь</span><span class="sxs-lookup"><span data-stu-id="f4875-277">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-278">Конечный пользователь, который инициировал запрос на получение ключа.</span><span class="sxs-lookup"><span data-stu-id="f4875-278">The end user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4875-279">Тип ключа</span><span class="sxs-lookup"><span data-stu-id="f4875-279">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-280">Тип запрашиваемого ключа.</span><span class="sxs-lookup"><span data-stu-id="f4875-280">The type of key that was requested.</span></span> <span data-ttu-id="f4875-281">MBAM собирает три типа ключей: пароль ключа восстановления (для восстановления компьютера в режиме восстановления); ИД ключа восстановления (для восстановления компьютера в режиме восстановления от имени другого пользователя); и хеш пароля доверенного платформенного модуля (TPM) (для восстановления компьютера с заблокированным TPM).</span><span class="sxs-lookup"><span data-stu-id="f4875-281">MBAM collects three key types: Recovery Key Password (to recovery a computer in recovery mode); Recovery Key ID (to recover a computer in recovery mode on behalf of another user); and Trusted Platform Module (TPM) Password Hash (to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4875-282">Описание причины</span><span class="sxs-lookup"><span data-stu-id="f4875-282">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4875-283">Причина, по которой запрошен заданный тип ключа.</span><span class="sxs-lookup"><span data-stu-id="f4875-283">The reason that the specified Key Type was requested.</span></span> <span data-ttu-id="f4875-284">Причины указаны в разделе Восстановление диска и управление функциями доверенного платформенного модуля на веб-сайте администрирования.</span><span class="sxs-lookup"><span data-stu-id="f4875-284">The reasons are specified in the Drive Recovery and Manage TPM features of the Administrative web site.</span></span> <span data-ttu-id="f4875-285">Допустимые значения включают текст, введенный пользователем, или один из указанных ниже кодов причин.</span><span class="sxs-lookup"><span data-stu-id="f4875-285">Valid entries include user-entered text or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="f4875-286">Порядок загрузки операционной системы изменился</span><span class="sxs-lookup"><span data-stu-id="f4875-286">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="f4875-287">BIOS изменилась</span><span class="sxs-lookup"><span data-stu-id="f4875-287">BIOS changed</span></span></p></li>
<li><p><span data-ttu-id="f4875-288">Изменены файлы операционной системы</span><span class="sxs-lookup"><span data-stu-id="f4875-288">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="f4875-289">Потерянный ключ запуска</span><span class="sxs-lookup"><span data-stu-id="f4875-289">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="f4875-290">Потерянный ПИН-код</span><span class="sxs-lookup"><span data-stu-id="f4875-290">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="f4875-291">Сброс доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="f4875-291">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="f4875-292">Утеряна парольная фраза</span><span class="sxs-lookup"><span data-stu-id="f4875-292">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="f4875-293">Потерялась смарт-карта</span><span class="sxs-lookup"><span data-stu-id="f4875-293">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="f4875-294">Сброс блокировки ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="f4875-294">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="f4875-295">Включить доверенный платформенный модуль</span><span class="sxs-lookup"><span data-stu-id="f4875-295">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="f4875-296">Отключение доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="f4875-296">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="f4875-297">Изменение пароля доверенного платформенного модуля</span><span class="sxs-lookup"><span data-stu-id="f4875-297">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="f4875-298">Очистить доверенный платформенный модуль</span><span class="sxs-lookup"><span data-stu-id="f4875-298">Clear TPM</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f4875-299">**Примечание**  Чтобы сохранить результаты отчета в файл, нажмите кнопку " **Экспорт** " в строке меню "отчеты".</span><span class="sxs-lookup"><span data-stu-id="f4875-299">**Note** To save report results to a file, click the **Export** button on the reports menu bar.</span></span>

 

## <span data-ttu-id="f4875-300">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f4875-300">Related topics</span></span>


[<span data-ttu-id="f4875-301">Мониторинг и создание отчетов по соответствию BitLocker с помощью MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="f4875-301">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





