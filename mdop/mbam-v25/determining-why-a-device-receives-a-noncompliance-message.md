---
title: Определение того, почему устройство получает сообщение о несоответствии
description: Определение того, почему устройство получает сообщение о несоответствии
author: dansimp
ms.assetid: 793df330-a0ee-4759-b53a-95618ac74428
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/22/2017
ms.openlocfilehash: ce1d344676ebf4328506228f1bfa87c76e8036f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824572"
---
# <span data-ttu-id="ee4ac-103">Определение того, почему устройство получает сообщение о несоответствии</span><span class="sxs-lookup"><span data-stu-id="ee4ac-103">Determining why a Device Receives a Noncompliance Message</span></span>


<span data-ttu-id="ee4ac-104">Следующие коды несоответствия предоставлены WMI и описывают причины, по которым в MBAM, как несоответствующие требованиям, сообщается о конкретном устройстве.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-104">The following noncompliance codes are provided by WMI and describe the reasons why a particular device is reported by MBAM as noncompliant.</span></span>

<span data-ttu-id="ee4ac-105">Для просмотра WMI можно использовать предпочтительный метод.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-105">You can use your preferred method to view WMI.</span></span> <span data-ttu-id="ee4ac-106">Если вы используете PowerShell, запустите программу `gwmi -class mbam_volume -Namespace root\microsoft\mbam` из командной строке PowerShell и выполните поиск по запросу ReasonsForNoncompliance.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-106">If you use PowerShell, run `gwmi -class mbam_volume -Namespace root\microsoft\mbam` from a PowerShell prompt and search for ReasonsForNoncompliance.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ee4ac-107">Код без соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="ee4ac-107">Non-Compliance Code</span></span></th>
<th align="left"><span data-ttu-id="ee4ac-108">Причина, по которой не удается получить соответствие</span><span class="sxs-lookup"><span data-stu-id="ee4ac-108">Reason for Non-Compliance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee4ac-109">до</span><span class="sxs-lookup"><span data-stu-id="ee4ac-109">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-110">Стойкость шифра не является AES 256.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-110">Cipher strength not AES 256.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee4ac-111">1,1</span><span class="sxs-lookup"><span data-stu-id="ee4ac-111">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-112">Для MBAM политики требуется, чтобы этот том был зашифрован, но это не так.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-112">MBAM Policy requires this volume to be encrypted but it is not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee4ac-113">2</span><span class="sxs-lookup"><span data-stu-id="ee4ac-113">2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-114">Для политики MBAM требуется, чтобы этот том не был зашифрован, но это так.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-114">MBAM Policy requires this volume to NOT be encrypted, but it is.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee4ac-115">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="ee4ac-115">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-116">Для политики MBAM требуется, чтобы этот том использовал предохранитель доверенного платформенного модуля, но это не так.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-116">MBAM Policy requires this volume use a TPM protector, but it does not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee4ac-117">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="ee4ac-117">4</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-118">Для политики MBAM требуется, чтобы этот том использовал предохранитель TPM + PIN-код, но это не так.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-118">MBAM Policy requires this volume use a TPM+PIN protector, but it does not.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee4ac-119">5</span><span class="sxs-lookup"><span data-stu-id="ee4ac-119">5</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-120">Политика MBAM не позволяет компьютерам доверенного платформенного модуля сообщать о том, что он не соответствует требованиям.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-120">MBAM Policy does not allow non TPM machines to report as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee4ac-121">152</span><span class="sxs-lookup"><span data-stu-id="ee4ac-121">6</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-122">У тома есть предохранитель доверенного платформенного модуля, но доверенный платформенный модуль не отображается (загружен с ключом восстановления после отключения TPM в BIOS).</span><span class="sxs-lookup"><span data-stu-id="ee4ac-122">Volume has a TPM protector but the TPM is not visible (booted with recover key after disabling TPM in BIOS?).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee4ac-123">5-7</span><span class="sxs-lookup"><span data-stu-id="ee4ac-123">7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-124">Для политики MBAM требуется, чтобы этот том использовал предохранитель пароля, но у него нет такого тома.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-124">MBAM Policy requires this volume use a password protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee4ac-125">No8</span><span class="sxs-lookup"><span data-stu-id="ee4ac-125">8</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-126">Для политики MBAM требуется, чтобы этот том не использовал предохранитель пароля, но у него есть один из них.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-126">MBAM Policy requires this volume NOT use a password protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee4ac-127">@</span><span class="sxs-lookup"><span data-stu-id="ee4ac-127">9</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-128">Для политики MBAM требуется, чтобы этот том использовал предохранитель автоматического разблокировки, но у него нет такого тома.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-128">MBAM Policy requires this volume use an auto-unlock protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee4ac-129">5-10</span><span class="sxs-lookup"><span data-stu-id="ee4ac-129">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-130">Для политики MBAM требуется, чтобы этот том не использовал предохранитель автоматического разблокировки, но у него есть один из них.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-130">MBAM Policy requires this volume NOT use an auto-unlock protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee4ac-131">11</span><span class="sxs-lookup"><span data-stu-id="ee4ac-131">11</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-132">Конфликт политики обнаружен, так как MBAM сообщил о том, что этот том соответствует требованиям.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-132">Policy conflict detected preventing MBAM from reporting this volume as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee4ac-133">12</span><span class="sxs-lookup"><span data-stu-id="ee4ac-133">12</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-134">Системный том необходим для шифрования тома операционной системы, но отсутствует.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-134">A system volume is needed to encrypt the OS volume but it is not present.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee4ac-135">рис</span><span class="sxs-lookup"><span data-stu-id="ee4ac-135">13</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-136">Защита тома приостановлена.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-136">Protection is suspended for the volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee4ac-137">дюймов</span><span class="sxs-lookup"><span data-stu-id="ee4ac-137">14</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-138">Автоматическое снятие блокировки в небезопасном режиме без шифрования тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-138">AutoUnlock unsafe unless the OS volume is encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee4ac-139">10-15</span><span class="sxs-lookup"><span data-stu-id="ee4ac-139">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-140">Для политики требуется минимальная Cypher сила — XTS-AES-128 bit, фактическая Cypher сила является менее надежной.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-140">Policy requires minimum cypher strength is XTS-AES-128 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee4ac-141">шестнадцат</span><span class="sxs-lookup"><span data-stu-id="ee4ac-141">16</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee4ac-142">Для политики требуется минимальная Cypher сила — XTS-AES-256 bit, фактическая Cypher сила является менее надежной.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-142">Policy requires minimum cypher strength is XTS-AES-256 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ee4ac-143">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ee4ac-143">Related topics</span></span>


[<span data-ttu-id="ee4ac-144">Технический справочник по MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ee4ac-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="ee4ac-145">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee4ac-145">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## <span data-ttu-id="ee4ac-146">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="ee4ac-146">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ee4ac-147">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="ee4ac-147">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ee4ac-148">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ee4ac-148">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





