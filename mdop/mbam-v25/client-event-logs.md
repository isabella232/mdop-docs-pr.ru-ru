---
title: Журналы событий клиента
description: Журналы событий клиента
author: dansimp
ms.assetid: d5c2f270-db6a-45f1-8557-8c6fb28fd568
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7324d07bf018944fcbe24168bba2e9abea9cea41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824192"
---
# <span data-ttu-id="7d09b-103">Журналы событий клиента</span><span class="sxs-lookup"><span data-stu-id="7d09b-103">Client Event Logs</span></span>

<span data-ttu-id="7d09b-104">Журналы событий клиента MBAM находятся в окне просмотра событий — Журналы приложений и служб — путь Microsoft – Windows – MBAM-Operational.</span><span class="sxs-lookup"><span data-stu-id="7d09b-104">MBAM Client event logs are located in Event Viewer – Applications and Services Logs – Microsoft – Windows – MBAM - Operational path.</span></span>
<span data-ttu-id="7d09b-105">В приведенной ниже таблице указаны коды событий, которые могут возникать в клиенте MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d09b-105">The following table contains event IDs that can occur on the MBAM Client.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7d09b-106">Идентификатор события</span><span class="sxs-lookup"><span data-stu-id="7d09b-106">Event ID</span></span></th>
<th align="left"><span data-ttu-id="7d09b-107">Канал</span><span class="sxs-lookup"><span data-stu-id="7d09b-107">Channel</span></span></th>
<th align="left"><span data-ttu-id="7d09b-108">Символ события</span><span class="sxs-lookup"><span data-stu-id="7d09b-108">Event symbol</span></span></th>
<th align="left"><span data-ttu-id="7d09b-109">Сообщение</span><span class="sxs-lookup"><span data-stu-id="7d09b-109">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-110">1,1</span><span class="sxs-lookup"><span data-stu-id="7d09b-110">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-111">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-111">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-112">VolumeEnactmentSuccessful</span><span class="sxs-lookup"><span data-stu-id="7d09b-112">VolumeEnactmentSuccessful</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-113">Политики MBAM были успешно применены.</span><span class="sxs-lookup"><span data-stu-id="7d09b-113">The MBAM policies were applied successfully.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-114">2</span><span class="sxs-lookup"><span data-stu-id="7d09b-114">2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-115">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-115">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-116">VolumeEnactmentFailed</span><span class="sxs-lookup"><span data-stu-id="7d09b-116">VolumeEnactmentFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-117">При применении политик MBAM произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="7d09b-117">An error occurred while applying MBAM policies.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-118">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="7d09b-118">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-119">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-119">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-120">TransferStatusDataSuccessful</span><span class="sxs-lookup"><span data-stu-id="7d09b-120">TransferStatusDataSuccessful</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-121">Данные о состоянии шифрования успешно отправлены.</span><span class="sxs-lookup"><span data-stu-id="7d09b-121">The encryption status data was sent successfully.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-122">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="7d09b-122">4</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-123">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-123">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-124">TransferStatusDataFailed</span><span class="sxs-lookup"><span data-stu-id="7d09b-124">TransferStatusDataFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-125">Произошла ошибка при отправке данных о состоянии шифрования.</span><span class="sxs-lookup"><span data-stu-id="7d09b-125">An error occurred while sending encryption status data.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-126">No8</span><span class="sxs-lookup"><span data-stu-id="7d09b-126">8</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-127">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-127">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-128">SystemVolumeNotFound</span><span class="sxs-lookup"><span data-stu-id="7d09b-128">SystemVolumeNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-129">Системный том отсутствует.</span><span class="sxs-lookup"><span data-stu-id="7d09b-129">The system volume is missing.</span></span> <span data-ttu-id="7d09b-130">SystemVolume требуется для шифрования диска с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="7d09b-130">SystemVolume is needed to encrypt the operating system drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-131">@</span><span class="sxs-lookup"><span data-stu-id="7d09b-131">9</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-132">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-132">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-133">TPMNotFound</span><span class="sxs-lookup"><span data-stu-id="7d09b-133">TPMNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-134">Отсутствует оборудование доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="7d09b-134">The TPM hardware is missing.</span></span> <span data-ttu-id="7d09b-135">TPM нужен, чтобы зашифровать диск операционной системы с помощью любого предохранителя доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="7d09b-135">TPM is needed to encrypt the operating system drive with any TPM protector.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-136">5-10</span><span class="sxs-lookup"><span data-stu-id="7d09b-136">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-137">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-137">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-138">MachineHWExempted</span><span class="sxs-lookup"><span data-stu-id="7d09b-138">MachineHWExempted</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-139">Компьютер исключен из шифрования.</span><span class="sxs-lookup"><span data-stu-id="7d09b-139">The computer is exempted from Encryption.</span></span> <span data-ttu-id="7d09b-140">Состояние оборудования компьютера: исключено</span><span class="sxs-lookup"><span data-stu-id="7d09b-140">Machine’s hardware status: Exempted</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-141">11</span><span class="sxs-lookup"><span data-stu-id="7d09b-141">11</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-142">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-142">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-143">MachineHWUnknown</span><span class="sxs-lookup"><span data-stu-id="7d09b-143">MachineHWUnknown</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-144">Компьютер исключен из шифрования.</span><span class="sxs-lookup"><span data-stu-id="7d09b-144">The computer is exempted from encryption.</span></span> <span data-ttu-id="7d09b-145">Состояние оборудования компьютера: неизвестно</span><span class="sxs-lookup"><span data-stu-id="7d09b-145">Machine’s hardware status: Unknown</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-146">12</span><span class="sxs-lookup"><span data-stu-id="7d09b-146">12</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-147">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-147">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-148">HWCheckFailed</span><span class="sxs-lookup"><span data-stu-id="7d09b-148">HWCheckFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-149">Проверка аппаратного освобождения не пройдена.</span><span class="sxs-lookup"><span data-stu-id="7d09b-149">Hardware exemption check failed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-150">рис</span><span class="sxs-lookup"><span data-stu-id="7d09b-150">13</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-151">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-151">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-152">UserIsExempted</span><span class="sxs-lookup"><span data-stu-id="7d09b-152">UserIsExempted</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-153">Пользователь исключен из шифрования.</span><span class="sxs-lookup"><span data-stu-id="7d09b-153">The user is exempt from encryption.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-154">дюймов</span><span class="sxs-lookup"><span data-stu-id="7d09b-154">14</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-155">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-155">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-156">UserIsWaiting</span><span class="sxs-lookup"><span data-stu-id="7d09b-156">UserIsWaiting</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-157">Пользователь запросил исключение.</span><span class="sxs-lookup"><span data-stu-id="7d09b-157">The user requested an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-158">10-15</span><span class="sxs-lookup"><span data-stu-id="7d09b-158">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-159">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-159">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-160">UserExemptionCheckFailed</span><span class="sxs-lookup"><span data-stu-id="7d09b-160">UserExemptionCheckFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-161">Проверка освобождения пользователей завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="7d09b-161">User exemption check failed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-162">шестнадцат</span><span class="sxs-lookup"><span data-stu-id="7d09b-162">16</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-163">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-163">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-164">UserPostponed</span><span class="sxs-lookup"><span data-stu-id="7d09b-164">UserPostponed</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-165">Пользователь отложил процесс шифрования.</span><span class="sxs-lookup"><span data-stu-id="7d09b-165">The user postponed the encryption process.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-166">18</span><span class="sxs-lookup"><span data-stu-id="7d09b-166">17</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-167">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-167">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-168">TPMInitializationFailed</span><span class="sxs-lookup"><span data-stu-id="7d09b-168">TPMInitializationFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-169">Инициализация TPM завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="7d09b-169">TPM initialization failed.</span></span> <span data-ttu-id="7d09b-170">Пользователь отклонил изменения в BIOS.</span><span class="sxs-lookup"><span data-stu-id="7d09b-170">The user rejected the BIOS changes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-171">18</span><span class="sxs-lookup"><span data-stu-id="7d09b-171">18</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-172">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-172">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-173">CoreServiceDown</span><span class="sxs-lookup"><span data-stu-id="7d09b-173">CoreServiceDown</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-174">Не удается подключиться к службе восстановления MBAM и оборудования.</span><span class="sxs-lookup"><span data-stu-id="7d09b-174">Unable to connect to the MBAM Recovery and Hardware service.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-175">19</span><span class="sxs-lookup"><span data-stu-id="7d09b-175">19</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-176">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-176">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-177">CoreServiceUp</span><span class="sxs-lookup"><span data-stu-id="7d09b-177">CoreServiceUp</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-178">Успешно подключено к службе восстановления MBAM и оборудования.</span><span class="sxs-lookup"><span data-stu-id="7d09b-178">Successfully connected to the MBAM Recovery and Hardware service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-179">средняя</span><span class="sxs-lookup"><span data-stu-id="7d09b-179">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-180">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-180">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-181">PolicyMismatch</span><span class="sxs-lookup"><span data-stu-id="7d09b-181">PolicyMismatch</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-182">Политика MBAM в конфликте или повреждена.</span><span class="sxs-lookup"><span data-stu-id="7d09b-182">The MBAM policy is in conflict or corrupt.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-183">Порт</span><span class="sxs-lookup"><span data-stu-id="7d09b-183">21</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-184">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-184">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-185">ConflictingOSVolumePolicies</span><span class="sxs-lookup"><span data-stu-id="7d09b-185">ConflictingOSVolumePolicies</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-186">Обнаружен конфликт политик шифрования тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7d09b-186">Detected OS volume encryption policies conflict.</span></span> <span data-ttu-id="7d09b-187">Проверьте политики BitLocker и MBAM, связанные с защитой диска ОС.</span><span class="sxs-lookup"><span data-stu-id="7d09b-187">Check BitLocker and MBAM policies related to OS drive protectors.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-188">максималь</span><span class="sxs-lookup"><span data-stu-id="7d09b-188">22</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-189">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-189">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-190">ConflictingFDDVolumePolicies</span><span class="sxs-lookup"><span data-stu-id="7d09b-190">ConflictingFDDVolumePolicies</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-191">Обнаружены неисправленные политики шифрования тома для диска с данными.</span><span class="sxs-lookup"><span data-stu-id="7d09b-191">Detected Fixed Data Drive volume encryption policies conflict.</span></span> <span data-ttu-id="7d09b-192">Проверьте политики BitLocker и MBAM, связанные с защитой ФЛОППИ стример.</span><span class="sxs-lookup"><span data-stu-id="7d09b-192">Check BitLocker and MBAM policies related to FDD drive protectors.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-193">отображал</span><span class="sxs-lookup"><span data-stu-id="7d09b-193">27</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-194">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-194">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-195">EncryptionFailedNoDra</span><span class="sxs-lookup"><span data-stu-id="7d09b-195">EncryptionFailedNoDra</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-196">При шифровании произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="7d09b-196">An error occurred while encrypting.</span></span> <span data-ttu-id="7d09b-197">В режиме FIPS для предустановленных компьютеров с Windows 8,1 требуется предохранитель агента восстановления данных (DRA).</span><span class="sxs-lookup"><span data-stu-id="7d09b-197">A Data Recovery Agent (DRA) protector is required in FIPS mode for pre-Windows 8.1 machines.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-198">Плот</span><span class="sxs-lookup"><span data-stu-id="7d09b-198">28</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-199">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-199">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-200">TpmOwnerAuthEscrowed</span><span class="sxs-lookup"><span data-stu-id="7d09b-200">TpmOwnerAuthEscrowed</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-201">OwnerAuth доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="7d09b-201">The TPM OwnerAuth has been escrowed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-202">составляет</span><span class="sxs-lookup"><span data-stu-id="7d09b-202">29</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-203">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-203">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-204">RecoveryKeyEscrowed</span><span class="sxs-lookup"><span data-stu-id="7d09b-204">RecoveryKeyEscrowed</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-205">Ключ восстановления BitLocker для тома был заблокирован.</span><span class="sxs-lookup"><span data-stu-id="7d09b-205">The BitLocker recovery key for the volume has been escrowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-206">30</span><span class="sxs-lookup"><span data-stu-id="7d09b-206">30</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-207">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-207">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-208">RecoveryKeyReset</span><span class="sxs-lookup"><span data-stu-id="7d09b-208">RecoveryKeyReset</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-209">Раздел восстановления BitLocker для тома обновлен.</span><span class="sxs-lookup"><span data-stu-id="7d09b-209">The BitLocker recovery key for the volume has been updated.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-210">31</span><span class="sxs-lookup"><span data-stu-id="7d09b-210">31</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-211">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-211">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-212">EnforcePolicyDateSet</span><span class="sxs-lookup"><span data-stu-id="7d09b-212">EnforcePolicyDateSet</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-213"><em> &lt; &gt; </em> Установленная для тома Дата политики принудительного применения</span><span class="sxs-lookup"><span data-stu-id="7d09b-213">The enforce policy date, <em>&lt;date&gt;</em>, has been set for the volume</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-214">32</span><span class="sxs-lookup"><span data-stu-id="7d09b-214">32</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-215">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-215">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-216">EnforcePolicyDateCleared</span><span class="sxs-lookup"><span data-stu-id="7d09b-216">EnforcePolicyDateCleared</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-217"><em> &lt; &gt; </em> Для тома была очищена Дата политики принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="7d09b-217">The enforce policy date, <em>&lt;date&gt;</em>, has been cleared for the volume.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-218">33</span><span class="sxs-lookup"><span data-stu-id="7d09b-218">33</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-219">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-219">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-220">TpmLockOutResetSucceeded</span><span class="sxs-lookup"><span data-stu-id="7d09b-220">TpmLockOutResetSucceeded</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-221">Сброс блокировки доверенного платформенного модуля выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="7d09b-221">Successfully reset TPM lockout.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-222">34</span><span class="sxs-lookup"><span data-stu-id="7d09b-222">34</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-223">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-223">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-224">TpmLockOutResetFailed</span><span class="sxs-lookup"><span data-stu-id="7d09b-224">TpmLockOutResetFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-225">Не удалось сбросить блокировку доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="7d09b-225">Failed to reset TPM lockout.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-226">35</span><span class="sxs-lookup"><span data-stu-id="7d09b-226">35</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-227">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-227">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-228">TpmOwnerAuthRetrievalSucceeded</span><span class="sxs-lookup"><span data-stu-id="7d09b-228">TpmOwnerAuthRetrievalSucceeded</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-229">OwnerAuth доверенного платформенного модуля из MBAM Services успешно получено.</span><span class="sxs-lookup"><span data-stu-id="7d09b-229">Successfully retrieved TPM OwnerAuth from MBAM services.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-230">36</span><span class="sxs-lookup"><span data-stu-id="7d09b-230">36</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-231">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-231">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-232">TpmOwnerAuthRetrievalFailed</span><span class="sxs-lookup"><span data-stu-id="7d09b-232">TpmOwnerAuthRetrievalFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-233">Не удалось получить OwnerAuth TPM из служб MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d09b-233">Failed to retrieve TPM OwnerAuth from MBAM services.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-234">37</span><span class="sxs-lookup"><span data-stu-id="7d09b-234">37</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-235">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-235">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-236">WmiProviderDllSearchPathUpdateFailed</span><span class="sxs-lookup"><span data-stu-id="7d09b-236">WmiProviderDllSearchPathUpdateFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-237">Не удалось обновить путь поиска DLL для поставщика WMI.</span><span class="sxs-lookup"><span data-stu-id="7d09b-237">Failed to update the DLL search path for WMI provider.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-238">38</span><span class="sxs-lookup"><span data-stu-id="7d09b-238">38</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-239">Admin</span><span class="sxs-lookup"><span data-stu-id="7d09b-239">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-240">TimedOutWaitingForWmiProvider</span><span class="sxs-lookup"><span data-stu-id="7d09b-240">TimedOutWaitingForWmiProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-241">Прекращение ожидания агента — ожидается экземпляр поставщика WMI MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d09b-241">Agent Stopping - Timed-out waiting for MBAM WMI Provider Instance.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-242">39</span><span class="sxs-lookup"><span data-stu-id="7d09b-242">39</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-243">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-243">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-244">RemovableDriveMounted</span><span class="sxs-lookup"><span data-stu-id="7d09b-244">RemovableDriveMounted</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-245">Съемный диск был подключен.</span><span class="sxs-lookup"><span data-stu-id="7d09b-245">Removable drive was mounted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-246">40</span><span class="sxs-lookup"><span data-stu-id="7d09b-246">40</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-247">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-247">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-248">RemovableDriveDismounted</span><span class="sxs-lookup"><span data-stu-id="7d09b-248">RemovableDriveDismounted</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-249">Съемный диск был отсоединен.</span><span class="sxs-lookup"><span data-stu-id="7d09b-249">Removable drive was unmounted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-250">41</span><span class="sxs-lookup"><span data-stu-id="7d09b-250">41</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-251">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-251">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-252">FailedToEnactEndpointUnreachable</span><span class="sxs-lookup"><span data-stu-id="7d09b-252">FailedToEnactEndpointUnreachable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-253">Не удалось подключиться к MBAM восстановления и службе оборудования, поскольку MBAM политики не будут успешно применены к тому.</span><span class="sxs-lookup"><span data-stu-id="7d09b-253">Failure to connect to the MBAM Recovery and Hardware service prevented MBAM policies from being applied successfully to the volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d09b-254">42</span><span class="sxs-lookup"><span data-stu-id="7d09b-254">42</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-255">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-255">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-256">FailedToEnactLockedVolume</span><span class="sxs-lookup"><span data-stu-id="7d09b-256">FailedToEnactLockedVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-257">Состояние заблокированного тома не позволило успешно применить политики MBAM к тому.</span><span class="sxs-lookup"><span data-stu-id="7d09b-257">Locked volume state prevented MBAM policies from being applied successfully to the volume.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d09b-258">43</span><span class="sxs-lookup"><span data-stu-id="7d09b-258">43</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-259">Действующие</span><span class="sxs-lookup"><span data-stu-id="7d09b-259">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-260">TransferStatusDataFailedEndpointUnreachable</span><span class="sxs-lookup"><span data-stu-id="7d09b-260">TransferStatusDataFailedEndpointUnreachable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d09b-261">Не удалось подключиться к службе соответствия требованиям MBAM, так как она не позволила передать данные о состоянии шифрования.</span><span class="sxs-lookup"><span data-stu-id="7d09b-261">Failure to connect to the MBAM Compliance and Status service prevented the transfer of encryption status data.</span></span></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="7d09b-262">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7d09b-262">Related topics</span></span>
[<span data-ttu-id="7d09b-263">Технический справочник по MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7d09b-263">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="7d09b-264">Журналы событий сервера</span><span class="sxs-lookup"><span data-stu-id="7d09b-264">Server Event Logs</span></span>](server-event-logs.md)

 


## <span data-ttu-id="7d09b-265">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="7d09b-265">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="7d09b-266">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="7d09b-266">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="7d09b-267">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="7d09b-267">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





