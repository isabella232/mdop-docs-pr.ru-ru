---
title: Поддерживаемые конфигурации MBAM 2.5
description: Поддерживаемые конфигурации MBAM 2.5
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 8ed7915e33c5e4735a7c58674ed5f7d6da8e9a06
ms.sourcegitcommit: 9087f0a1b5bd3f81a9b790d5e39fdf39c18a2411
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2020
ms.locfileid: "11182931"
---
# <span data-ttu-id="5a99d-103">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5a99d-103">MBAM 2.5 Supported Configurations</span></span>


<span data-ttu-id="5a99d-104">Вы можете выполнить администрирование и мониторинг Microsoft BitLocker (MBAM) 2,5 в изолированной топологии или в топологии интеграции Configuration Manager, которая интегрирует MBAM с System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5a99d-104">You can run Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a Stand-alone topology or in a Configuration Manager Integration topology that integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="5a99d-105">Если вы используете рекомендуемую конфигурацию для любой топологии в рабочей среде, MBAM поддерживает до 500 000 MBAM клиентов.</span><span class="sxs-lookup"><span data-stu-id="5a99d-105">If you use the recommended configuration for either topology in a production environment, MBAM supports up to 500,000 MBAM clients.</span></span> <span data-ttu-id="5a99d-106">Сведения о рекомендуемой архитектуре и функциональных возможностях, которые настроены на каждом сервере для каждой топологии, можно найти в разделе [архитектура высокого уровня для MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="5a99d-106">For information about the recommended architecture and features that are configured on each server for each topology, see [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<span data-ttu-id="5a99d-107">Дополнительные конфигурации, специфичные для топологии интеграции Configuration Manager, приведены в разделе [версии Configuration Manager, которые MBAM поддерживаются](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="5a99d-107">For additional configurations that are specific to the Configuration Manager Integration topology, see [Versions of Configuration Manager that MBAM supports](#bkmk-cm-ramreqs).</span></span>

**<span data-ttu-id="5a99d-108">Примечание.</span><span class="sxs-lookup"><span data-stu-id="5a99d-108">Note</span></span>**  
<span data-ttu-id="5a99d-109">Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="5a99d-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="5a99d-110">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="5a99d-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="5a99d-111">Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5a99d-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



## <span data-ttu-id="5a99d-112">Языки, поддерживаемые MBAM</span><span class="sxs-lookup"><span data-stu-id="5a99d-112">MBAM Supported Languages</span></span>


<span data-ttu-id="5a99d-113">В приведенных ниже таблицах показаны языки, которые поддерживаются клиентом MBAM (включая портал Self-Service) и сервер MBAM в MBAM 2,5 и MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="5a99d-113">The following tables show the languages that are supported for the MBAM Client (including the Self-Service Portal) and the MBAM Server in MBAM 2.5 and MBAM 2.5 SP1.</span></span>

**<span data-ttu-id="5a99d-114">Поддерживаемые языки в MBAM 2,5 с пакетом обновления 1 (SP1):</span><span class="sxs-lookup"><span data-stu-id="5a99d-114">Supported Languages in MBAM 2.5 SP1:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5a99d-115">Языки клиента</span><span class="sxs-lookup"><span data-stu-id="5a99d-115">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="5a99d-116">Языки сервера</span><span class="sxs-lookup"><span data-stu-id="5a99d-116">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-117">Чешский (Чешская Республика) cs-CZ</span><span class="sxs-lookup"><span data-stu-id="5a99d-117">Czech (Czech Republic) cs-CZ</span></span></p>
<p><span data-ttu-id="5a99d-118">Датский (Дания) da-DK</span><span class="sxs-lookup"><span data-stu-id="5a99d-118">Danish (Denmark) da-DK</span></span></p>
<p><span data-ttu-id="5a99d-119">Нидерландский (Нидерланды) nl-NL</span><span class="sxs-lookup"><span data-stu-id="5a99d-119">Dutch (Netherlands) nl-NL</span></span></p>
<p><span data-ttu-id="5a99d-120">Английский (США) EN-US</span><span class="sxs-lookup"><span data-stu-id="5a99d-120">English (United States) en-US</span></span></p>
<p><span data-ttu-id="5a99d-121">Финский (Финляндия) Fi-FI</span><span class="sxs-lookup"><span data-stu-id="5a99d-121">Finnish (Finland) fi-FI</span></span></p>
<p><span data-ttu-id="5a99d-122">Французский (Франция) fr-FR</span><span class="sxs-lookup"><span data-stu-id="5a99d-122">French (France) fr-FR</span></span></p>
<p><span data-ttu-id="5a99d-123">Немецкий (Германия) de-DE</span><span class="sxs-lookup"><span data-stu-id="5a99d-123">German (Germany) de-DE</span></span></p>
<p><span data-ttu-id="5a99d-124">Греческий (Греция) Эль-GR</span><span class="sxs-lookup"><span data-stu-id="5a99d-124">Greek (Greece) el-GR</span></span></p>
<p><span data-ttu-id="5a99d-125">Венгерский (Венгрия) hu-HU</span><span class="sxs-lookup"><span data-stu-id="5a99d-125">Hungarian (Hungary) hu-HU</span></span></p>
<p><span data-ttu-id="5a99d-126">Итальянский (Италия) IT-IT</span><span class="sxs-lookup"><span data-stu-id="5a99d-126">Italian (Italy) it-IT</span></span></p>
<p><span data-ttu-id="5a99d-127">Японский (Япония) ja-JP</span><span class="sxs-lookup"><span data-stu-id="5a99d-127">Japanese (Japan) ja-JP</span></span></p>
<p><span data-ttu-id="5a99d-128">Корейский (Корея) ko-KR</span><span class="sxs-lookup"><span data-stu-id="5a99d-128">Korean (Korea) ko-KR</span></span></p>
<p><span data-ttu-id="5a99d-129">Норвежский (букмол, Норвегия) без датаграмм</span><span class="sxs-lookup"><span data-stu-id="5a99d-129">Norwegian, Bokmål (Norway) nb-NO</span></span></p>
<p><span data-ttu-id="5a99d-130">Польский (Польша) PL-PL</span><span class="sxs-lookup"><span data-stu-id="5a99d-130">Polish (Poland) pl-PL</span></span></p>
<p><span data-ttu-id="5a99d-131">Португальский (Бразилия) Пт — BR</span><span class="sxs-lookup"><span data-stu-id="5a99d-131">Portuguese (Brazil) pt-BR</span></span></p>
<p><span data-ttu-id="5a99d-132">Португальский (Португалия), пт</span><span class="sxs-lookup"><span data-stu-id="5a99d-132">Portuguese (Portugal) pt-PT</span></span></p>
<p><span data-ttu-id="5a99d-133">Русский (Россия) ru-RU</span><span class="sxs-lookup"><span data-stu-id="5a99d-133">Russian (Russia) ru-RU</span></span></p>
<p><span data-ttu-id="5a99d-134">Словацкий (Словакия) sk-SK</span><span class="sxs-lookup"><span data-stu-id="5a99d-134">Slovak (Slovakia) sk-SK</span></span></p>
<p><span data-ttu-id="5a99d-135">Испанский (Испания) ES-ES</span><span class="sxs-lookup"><span data-stu-id="5a99d-135">Spanish (Spain) es-ES</span></span></p>
<p><span data-ttu-id="5a99d-136">Шведский (Швеция) SV-SE</span><span class="sxs-lookup"><span data-stu-id="5a99d-136">Swedish (Sweden) sv-SE</span></span></p>
<p><span data-ttu-id="5a99d-137">Турецкий (Турция) tr-TR</span><span class="sxs-lookup"><span data-stu-id="5a99d-137">Turkish (Turkey) tr-TR</span></span></p>
<p><span data-ttu-id="5a99d-138">Словенский (Словения) SL-SI</span><span class="sxs-lookup"><span data-stu-id="5a99d-138">Slovenian (Slovenia) sl-SI</span></span></p>
<p><span data-ttu-id="5a99d-139">Упрощенный китайский (КНР) zh-CN</span><span class="sxs-lookup"><span data-stu-id="5a99d-139">Simplified Chinese (PRC) zh-CN</span></span></p>
<p><span data-ttu-id="5a99d-140">Китайский (традиционное письмо, Тайвань) zh-TW</span><span class="sxs-lookup"><span data-stu-id="5a99d-140">Traditional Chinese (Taiwan) zh-TW</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="5a99d-141">Английский (США) EN-US</span><span class="sxs-lookup"><span data-stu-id="5a99d-141">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="5a99d-142">Французский (Франция) fr-FR</span><span class="sxs-lookup"><span data-stu-id="5a99d-142">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="5a99d-143">Немецкий (Германия) de-DE</span><span class="sxs-lookup"><span data-stu-id="5a99d-143">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="5a99d-144">Итальянский (Италия) IT-IT</span><span class="sxs-lookup"><span data-stu-id="5a99d-144">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="5a99d-145">Японский (Япония) ja-JP</span><span class="sxs-lookup"><span data-stu-id="5a99d-145">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="5a99d-146">Корейский (Корея) ko-KR</span><span class="sxs-lookup"><span data-stu-id="5a99d-146">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="5a99d-147">Португальский (Бразилия) Пт — BR</span><span class="sxs-lookup"><span data-stu-id="5a99d-147">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="5a99d-148">Русский (Россия) ru-RU</span><span class="sxs-lookup"><span data-stu-id="5a99d-148">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="5a99d-149">Испанский (Испания) ES-ES</span><span class="sxs-lookup"><span data-stu-id="5a99d-149">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="5a99d-150">Упрощенный китайский (КНР) zh-CN</span><span class="sxs-lookup"><span data-stu-id="5a99d-150">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="5a99d-151">Китайский (традиционное письмо, Тайвань) zh-TW</span><span class="sxs-lookup"><span data-stu-id="5a99d-151">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="5a99d-152">Поддерживаемые языки в MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="5a99d-152">Supported Languages in MBAM 2.5:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5a99d-153">Языки клиента</span><span class="sxs-lookup"><span data-stu-id="5a99d-153">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="5a99d-154">Языки сервера</span><span class="sxs-lookup"><span data-stu-id="5a99d-154">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="5a99d-155">Английский (США) EN-US</span><span class="sxs-lookup"><span data-stu-id="5a99d-155">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="5a99d-156">Французский (Франция) fr-FR</span><span class="sxs-lookup"><span data-stu-id="5a99d-156">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="5a99d-157">Немецкий (Германия) de-DE</span><span class="sxs-lookup"><span data-stu-id="5a99d-157">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="5a99d-158">Итальянский (Италия) IT-IT</span><span class="sxs-lookup"><span data-stu-id="5a99d-158">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="5a99d-159">Японский (Япония) ja-JP</span><span class="sxs-lookup"><span data-stu-id="5a99d-159">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="5a99d-160">Корейский (Корея) ko-KR</span><span class="sxs-lookup"><span data-stu-id="5a99d-160">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="5a99d-161">Португальский (Бразилия) Пт — BR</span><span class="sxs-lookup"><span data-stu-id="5a99d-161">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="5a99d-162">Русский (Россия) ru-RU</span><span class="sxs-lookup"><span data-stu-id="5a99d-162">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="5a99d-163">Испанский (Испания) ES-ES</span><span class="sxs-lookup"><span data-stu-id="5a99d-163">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="5a99d-164">Упрощенный китайский (КНР) zh-CN</span><span class="sxs-lookup"><span data-stu-id="5a99d-164">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="5a99d-165">Китайский (традиционное письмо, Тайвань) zh-TW</span><span class="sxs-lookup"><span data-stu-id="5a99d-165">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="5a99d-166">Английский (США) EN-US</span><span class="sxs-lookup"><span data-stu-id="5a99d-166">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="5a99d-167">Французский (Франция) fr-FR</span><span class="sxs-lookup"><span data-stu-id="5a99d-167">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="5a99d-168">Немецкий (Германия) de-DE</span><span class="sxs-lookup"><span data-stu-id="5a99d-168">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="5a99d-169">Итальянский (Италия) IT-IT</span><span class="sxs-lookup"><span data-stu-id="5a99d-169">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="5a99d-170">Японский (Япония) ja-JP</span><span class="sxs-lookup"><span data-stu-id="5a99d-170">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="5a99d-171">Корейский (Корея) ko-KR</span><span class="sxs-lookup"><span data-stu-id="5a99d-171">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="5a99d-172">Португальский (Бразилия) Пт — BR</span><span class="sxs-lookup"><span data-stu-id="5a99d-172">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="5a99d-173">Русский (Россия) ru-RU</span><span class="sxs-lookup"><span data-stu-id="5a99d-173">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="5a99d-174">Испанский (Испания) ES-ES</span><span class="sxs-lookup"><span data-stu-id="5a99d-174">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="5a99d-175">Упрощенный китайский (КНР) zh-CN</span><span class="sxs-lookup"><span data-stu-id="5a99d-175">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="5a99d-176">Китайский (традиционное письмо, Тайвань) zh-TW</span><span class="sxs-lookup"><span data-stu-id="5a99d-176">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="5a99d-177">Требования к серверной системе MBAM</span><span class="sxs-lookup"><span data-stu-id="5a99d-177">MBAM Server system requirements</span></span>


### <span data-ttu-id="5a99d-178">Требования к серверной операционной системе MBAM</span><span class="sxs-lookup"><span data-stu-id="5a99d-178">MBAM Server operating system requirements</span></span>

<span data-ttu-id="5a99d-179">Настоятельно рекомендуется запускать клиент MBAM и сервер MBAM в одной и той же строке операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5a99d-179">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="5a99d-180">Например, Windows 10 с Windows Server 2016, Windows 8,1 с Windows Server 2012 R2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="5a99d-180">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="5a99d-181">В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="5a99d-181">The following table lists the operating systems that are supported for the MBAM Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5a99d-182">Операционная система</span><span class="sxs-lookup"><span data-stu-id="5a99d-182">Operating system</span></span></th>
<th align="left"><span data-ttu-id="5a99d-183">Выпуск</span><span class="sxs-lookup"><span data-stu-id="5a99d-183">Edition</span></span></th>
<th align="left"><span data-ttu-id="5a99d-184">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="5a99d-184">Service pack</span></span></th>
<th align="left"><span data-ttu-id="5a99d-185">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="5a99d-185">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-186">WindowsServer2019</span><span class="sxs-lookup"><span data-stu-id="5a99d-186">Windows Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-187">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="5a99d-187">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="5a99d-188">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-189">Windows Server2016</span><span class="sxs-lookup"><span data-stu-id="5a99d-189">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-190">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="5a99d-190">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="5a99d-191">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-191">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-192">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5a99d-192">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-193">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="5a99d-193">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-194">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-194">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-195">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a99d-195">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-196">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="5a99d-196">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="5a99d-197">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-197">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-198">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="5a99d-198">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-199">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="5a99d-199">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-200">SP1</span><span class="sxs-lookup"><span data-stu-id="5a99d-200">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-201">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-201">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="5a99d-202">Корпоративный домен должен содержать по крайней мере один контроллер домена Windows Server 2008 (или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="5a99d-202">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span>

### <a href="" id="bkmk-stand-alone-ramreqs"></a><span data-ttu-id="5a99d-203">MBAM, оперативная память и требования к дисковому пространству — изолированная топология</span><span class="sxs-lookup"><span data-stu-id="5a99d-203">MBAM Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="5a99d-204">Эти требования предназначены для изолированной топологии MBAM.</span><span class="sxs-lookup"><span data-stu-id="5a99d-204">These requirements are for the MBAM Stand-alone topology.</span></span> <span data-ttu-id="5a99d-205">Требования к топологии интеграции Configuration Manager можно найти в разделе [процессор сервера MBAM, ОЗУ и требования к дисковому пространству — топология интеграции Configuration Manager](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="5a99d-205">For the requirements for the Configuration Manager Integration topology, see [MBAM Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5a99d-206">Элемент оборудования</span><span class="sxs-lookup"><span data-stu-id="5a99d-206">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="5a99d-207">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="5a99d-207">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="5a99d-208">Рекомендуемое требование</span><span class="sxs-lookup"><span data-stu-id="5a99d-208">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-209">Процессор</span><span class="sxs-lookup"><span data-stu-id="5a99d-209">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-210">2,33 ГГц</span><span class="sxs-lookup"><span data-stu-id="5a99d-210">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-211">2,33 ГГц или выше</span><span class="sxs-lookup"><span data-stu-id="5a99d-211">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-212">ОЗУ</span><span class="sxs-lookup"><span data-stu-id="5a99d-212">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-213">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-213">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-214">12 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-214">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-215">Свободное место на диске</span><span class="sxs-lookup"><span data-stu-id="5a99d-215">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-216">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-216">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-217">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-217">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a><span data-ttu-id="5a99d-218">Требования к процессору сервера MBAM, ОЗУ и дисковому пространству — топология интеграции Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="5a99d-218">MBAM Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="5a99d-219">В таблице ниже перечислены требования к серверному процессору, ОЗУ и дисковому пространству для серверов MBAM при использовании топологии интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5a99d-219">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span> <span data-ttu-id="5a99d-220">Требования для изолированной топологии можно найти в разделе [процессор сервера MBAM, ОЗУ и требования к дисковому пространству — изолированная топология](#bkmk-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="5a99d-220">For the requirements for the Stand-alone topology, see [MBAM Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5a99d-221">Элемент оборудования</span><span class="sxs-lookup"><span data-stu-id="5a99d-221">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="5a99d-222">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="5a99d-222">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="5a99d-223">Рекомендуемое требование</span><span class="sxs-lookup"><span data-stu-id="5a99d-223">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-224">Процессор</span><span class="sxs-lookup"><span data-stu-id="5a99d-224">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-225">2,33 ГГц</span><span class="sxs-lookup"><span data-stu-id="5a99d-225">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-226">2,33 ГГц или выше</span><span class="sxs-lookup"><span data-stu-id="5a99d-226">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-227">ОЗУ</span><span class="sxs-lookup"><span data-stu-id="5a99d-227">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-228">4 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-228">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-229">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-229">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-230">Свободное место на диске</span><span class="sxs-lookup"><span data-stu-id="5a99d-230">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-231">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-231">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-232">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-232">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a><span data-ttu-id="5a99d-233">Версии Configuration Manager, которые поддерживает MBAM</span><span class="sxs-lookup"><span data-stu-id="5a99d-233">Versions of Configuration Manager that MBAM supports</span></span>

<span data-ttu-id="5a99d-234">MBAM поддерживает следующие версии Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5a99d-234">MBAM supports the following versions of Configuration Manager.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5a99d-235">Поддерживаемая версия</span><span class="sxs-lookup"><span data-stu-id="5a99d-235">Supported version</span></span></th>
<th align="left"><span data-ttu-id="5a99d-236">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="5a99d-236">Service pack</span></span></th>
<th align="left"><span data-ttu-id="5a99d-237">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="5a99d-237">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-238">Microsoft System Center Configuration Manager (Текущая ветвь), версии до 1902</span><span class="sxs-lookup"><span data-stu-id="5a99d-238">Microsoft System Center Configuration Manager (Current Branch), versions up to 1902</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-239">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-239">64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-240">Microsoft System Center Configuration Manager 1806</span><span class="sxs-lookup"><span data-stu-id="5a99d-240">Microsoft System Center Configuration Manager 1806</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-241">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-241">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-242">Microsoft System Center Configuration Manager (LTSB-Version 1606)</span><span class="sxs-lookup"><span data-stu-id="5a99d-242">Microsoft System Center Configuration Manager (LTSB - version 1606)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-243">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-243">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-244">Microsoft System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="5a99d-244">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-245">SP1</span><span class="sxs-lookup"><span data-stu-id="5a99d-245">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-246">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-246">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-247">Microsoft System Center Configuration Manager 2007 R2 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5a99d-247">Microsoft System Center Configuration Manager 2007 R2 or later</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-248">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-248">64-bit</span></span></p>

<span data-ttu-id="5a99d-249">&gt;<strong>Примечание </strong> несмотря на то, что Configuration Manager 2007 R2 имеет значение 32, необходимо установить его и SQL Server на 64-разрядную версию операционной системы, чтобы обеспечить соответствие с программным обеспечением 64-bit MBAM.</span><span class="sxs-lookup"><span data-stu-id="5a99d-249">&gt;<strong>Note</strong> Although Configuration Manager 2007 R2 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span>
</td>
</tr>
</tbody>
</table>



<span data-ttu-id="5a99d-250">Список поддерживаемых конфигураций для сервера Configuration Manager можно найти в соответствующей документации TechNet о версии Configuration Manager, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="5a99d-250">For a list of supported configurations for the Configuration Manager Server, see the appropriate TechNet documentation for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="5a99d-251">В MBAM отсутствуют дополнительные требования к системе для сервера Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5a99d-251">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="5a99d-252">Требования к базам данных SQL Server</span><span class="sxs-lookup"><span data-stu-id="5a99d-252">SQL Server database requirements</span></span>

<span data-ttu-id="5a99d-253">В приведенной ниже таблице указаны версии Microsoft SQL Server, которые поддерживаются для функций сервера MBAM, включая базу данных восстановления, базу данных соответствия требованиям и журнал аудита, а также функцию отчеты.</span><span class="sxs-lookup"><span data-stu-id="5a99d-253">The following table lists the Microsoft SQL Server versions that are supported for the MBAM Server features, which include the Recovery Database, Compliance and Audit Database, and the Reports feature.</span></span> <span data-ttu-id="5a99d-254">Требуемые версии применяются к отдельным топологиям или топологии интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5a99d-254">The required versions apply to the Stand-alone or the Configuration Manager Integration topologies.</span></span>

<span data-ttu-id="5a99d-255">Необходимо установить SQL Server с параметрами сортировки **SQL \ _Latin1 \ _General \ _CP1 \ _CI \ _AS** .</span><span class="sxs-lookup"><span data-stu-id="5a99d-255">You must install SQL Server with the **SQL\_Latin1\_General\_CP1\_CI\_AS** collation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5a99d-256">Версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="5a99d-256">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="5a99d-257">Выпуск</span><span class="sxs-lookup"><span data-stu-id="5a99d-257">Edition</span></span></th>
<th align="left"><span data-ttu-id="5a99d-258">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="5a99d-258">Service pack</span></span></th>
<th align="left"><span data-ttu-id="5a99d-259">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="5a99d-259">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-260">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="5a99d-260">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-261">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="5a99d-261">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-262">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-262">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-263">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="5a99d-263">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-264">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="5a99d-264">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-265">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-265">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-266">Microsoft SQL Server2016</span><span class="sxs-lookup"><span data-stu-id="5a99d-266">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-267">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="5a99d-267">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-268">SP1</span><span class="sxs-lookup"><span data-stu-id="5a99d-268">SP1</span></span></p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p><span data-ttu-id="5a99d-269">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-269">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-270">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="5a99d-270">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-271">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="5a99d-271">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-272">ПАКЕТ ОБНОВЛЕНИЯ 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="5a99d-272">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-273">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-273">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-274">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a99d-274">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-275">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="5a99d-275">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-276">ОБНОВЛЕНИЙ</span><span class="sxs-lookup"><span data-stu-id="5a99d-276">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-277">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-277">64-bit</span></span></p></td>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-278">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5a99d-278">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-279">Standard или Enterprise</span><span class="sxs-lookup"><span data-stu-id="5a99d-279">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-280">ОБНОВЛЕНИЙ</span><span class="sxs-lookup"><span data-stu-id="5a99d-280">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-281">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-281">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

**<span data-ttu-id="5a99d-282">Примечание.</span><span class="sxs-lookup"><span data-stu-id="5a99d-282">Note</span></span>**  
<span data-ttu-id="5a99d-283">MBAM имеет максимальный поддерживаемый уровень совместимости 140.</span><span class="sxs-lookup"><span data-stu-id="5a99d-283">MBAM has a maximum supported compatibility level of 140.</span></span> <span data-ttu-id="5a99d-284">Уровень совместимости по умолчанию для новых баз данных, созданных в SQL Server 2019, составляет 150, которые необходимо изменить в 140 или более ранней, с помощью команды ALTER DATABASE после создания базы данных.</span><span class="sxs-lookup"><span data-stu-id="5a99d-284">The default compatibility level for new databases created on SQL Server 2019 is 150 which will need to be altered to 140 or lower, using the ALTER DATABASE command, after the database has been created.</span></span> <span data-ttu-id="5a99d-285">Существующие базы данных, перенесенные из SQL Server 2017 или более ранних версий, останутся на прежнем уровне совместимости и не нуждаются в изменении.</span><span class="sxs-lookup"><span data-stu-id="5a99d-285">Existing databases migrated from SQL server 2017 or below will remain at their previous compatibility level and do not need to be altered.</span></span>

<span data-ttu-id="5a99d-286">Для поддержки SQL 2016 необходимо установить выпуск за март 2017 для MDOP https://www.microsoft.com/download/details.aspx?id=54967  , а также поддержку sql 2017 вы должны установить выпуск за июль 2018 и сопровождение для MDOP https://www.microsoft.com/download/details.aspx?id=57157 .</span><span class="sxs-lookup"><span data-stu-id="5a99d-286">In order to support SQL 2016 you must install the March 2017 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=54967  and to support SQL 2017 you must install the July 2018 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=57157.</span></span> <span data-ttu-id="5a99d-287">В общем, всегда используйте Последнее обновление обслуживания, поскольку оно также включает все исправления ошибок и новые возможности.</span><span class="sxs-lookup"><span data-stu-id="5a99d-287">In general stay current by always using the most recent servicing update as it also includes all bugfixes and new features.</span></span>


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a><span data-ttu-id="5a99d-288">Требования процессора SQL Server, ОЗУ и места на диске — изолированная топология</span><span class="sxs-lookup"><span data-stu-id="5a99d-288">SQL Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="5a99d-289">В таблице ниже перечислены рекомендуемые требования к серверному процессору, ОЗУ и дисковому пространству для компьютера SQL Server при использовании изолированной топологии.</span><span class="sxs-lookup"><span data-stu-id="5a99d-289">The following table lists the recommended server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Stand-alone topology.</span></span> <span data-ttu-id="5a99d-290">Используйте эти требования как руководство.</span><span class="sxs-lookup"><span data-stu-id="5a99d-290">Use these requirements as a guide.</span></span> <span data-ttu-id="5a99d-291">Конкретные требования будут зависеть от количества клиентских компьютеров, которые поддерживаются в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="5a99d-291">Your specific requirements will vary based on the number of client computers you are supporting in your enterprise.</span></span> <span data-ttu-id="5a99d-292">Сведения о требованиях к топологии интеграции Configuration Manager можно найти в разделе [требования к процессорам SQL Server, ОЗУ и пространству на диске — топология интеграции Configuration Manager](#bkmk-cm-sql-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="5a99d-292">To view the requirements for the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-sql-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5a99d-293">Элемент оборудования</span><span class="sxs-lookup"><span data-stu-id="5a99d-293">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="5a99d-294">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="5a99d-294">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="5a99d-295">Рекомендуемое требование</span><span class="sxs-lookup"><span data-stu-id="5a99d-295">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-296">Процессор</span><span class="sxs-lookup"><span data-stu-id="5a99d-296">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-297">2,33 ГГц</span><span class="sxs-lookup"><span data-stu-id="5a99d-297">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-298">2,33 ГГц или выше</span><span class="sxs-lookup"><span data-stu-id="5a99d-298">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-299">ОЗУ</span><span class="sxs-lookup"><span data-stu-id="5a99d-299">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-300">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-300">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-301">12 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-301">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-302">Свободное место на диске</span><span class="sxs-lookup"><span data-stu-id="5a99d-302">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-303">5 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-303">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-304">5 ГБ или больше</span><span class="sxs-lookup"><span data-stu-id="5a99d-304">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a><span data-ttu-id="5a99d-305">Требования для процессора SQL Server, ОЗУ и места на диске — топология интеграции Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="5a99d-305">SQL Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="5a99d-306">В приведенной ниже таблице перечислены требования к серверному процессору, ОЗУ и дисковому пространству для компьютера с Microsoft SQL Server при использовании топологии интеграции Configuration Manager [: изолированная топология процессора SQL Server, ОЗУ и места на диске](#bkmk-sql-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="5a99d-306">The following table lists the server processor, RAM, and disk space requirements for the Microsoft SQL Server computer when you are using the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-sql-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5a99d-307">Элемент оборудования</span><span class="sxs-lookup"><span data-stu-id="5a99d-307">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="5a99d-308">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="5a99d-308">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="5a99d-309">Рекомендуемое требование</span><span class="sxs-lookup"><span data-stu-id="5a99d-309">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-310">Процессор</span><span class="sxs-lookup"><span data-stu-id="5a99d-310">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-311">2,33 ГГц</span><span class="sxs-lookup"><span data-stu-id="5a99d-311">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-312">2,33 ГГц или выше</span><span class="sxs-lookup"><span data-stu-id="5a99d-312">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-313">ОЗУ</span><span class="sxs-lookup"><span data-stu-id="5a99d-313">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-314">4 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-314">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-315">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-315">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-316">Свободное место на диске</span><span class="sxs-lookup"><span data-stu-id="5a99d-316">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-317">5 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-317">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-318">5 ГБ</span><span class="sxs-lookup"><span data-stu-id="5a99d-318">5 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="5a99d-319">Требования к системе клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="5a99d-319">MBAM Client system requirements</span></span>


### <span data-ttu-id="5a99d-320">Требования к операционной системе клиента</span><span class="sxs-lookup"><span data-stu-id="5a99d-320">Client operating system requirements</span></span>

<span data-ttu-id="5a99d-321">Настоятельно рекомендуется запускать клиент MBAM и сервер MBAM в одной и той же строке операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5a99d-321">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="5a99d-322">Например, Windows 10 с Windows Server 2016, Windows 8,1 с Windows Server 2012 R2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="5a99d-322">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="5a99d-323">В таблице ниже перечислены операционные системы, которые поддерживаются при установке клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="5a99d-323">The following table lists the operating systems that are supported for MBAM Client installation.</span></span> <span data-ttu-id="5a99d-324">Те же требования применимы к отдельным топологиям и топологии интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5a99d-324">The same requirements apply to the Stand-alone and the Configuration Manager Integration topologies.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5a99d-325">Операционная система</span><span class="sxs-lookup"><span data-stu-id="5a99d-325">Operating system</span></span></th>
<th align="left"><span data-ttu-id="5a99d-326">Выпуск</span><span class="sxs-lookup"><span data-stu-id="5a99d-326">Edition</span></span></th>
<th align="left"><span data-ttu-id="5a99d-327">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="5a99d-327">Service pack</span></span></th>
<th align="left"><span data-ttu-id="5a99d-328">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="5a99d-328">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p><span data-ttu-id="5a99d-329">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="5a99d-329">Windows 10 IoT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="5a99d-330">Функции корпоративного уровня</span><span class="sxs-lookup"><span data-stu-id="5a99d-330">Enterprise</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p><span data-ttu-id="5a99d-331">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-331">32-bit or 64-bit</span></span></p></td>
</tr><br/><tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-332">Windows 10</span><span class="sxs-lookup"><span data-stu-id="5a99d-332">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-333">Функции корпоративного уровня</span><span class="sxs-lookup"><span data-stu-id="5a99d-333">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-334">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-334">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-335">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5a99d-335">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-336">Функции корпоративного уровня</span><span class="sxs-lookup"><span data-stu-id="5a99d-336">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-337">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-337">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-338">Windows 7;</span><span class="sxs-lookup"><span data-stu-id="5a99d-338">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-339">Корпоративная или максимальная</span><span class="sxs-lookup"><span data-stu-id="5a99d-339">Enterprise or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-340">SP1</span><span class="sxs-lookup"><span data-stu-id="5a99d-340">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-341">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-341">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-342">Windows с собой</span><span class="sxs-lookup"><span data-stu-id="5a99d-342">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-343">Windows 8,1 и Windows 10 корпоративный</span><span class="sxs-lookup"><span data-stu-id="5a99d-343">Windows 8.1 and Windows 10 Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-344">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-344">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="5a99d-345">Требования к ОЗУ для клиента</span><span class="sxs-lookup"><span data-stu-id="5a99d-345">Client RAM requirements</span></span>

<span data-ttu-id="5a99d-346">Нет требований к ОЗУ, которые относятся к установке клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="5a99d-346">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="5a99d-347">Системные требования для групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="5a99d-347">MBAM Group Policy system requirements</span></span>


<span data-ttu-id="5a99d-348">В таблице ниже перечислены операционные системы, которые поддерживаются при установке шаблонов групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="5a99d-348">The following table lists the operating systems that are supported for MBAM Group Policy Templates installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5a99d-349">Операционная система</span><span class="sxs-lookup"><span data-stu-id="5a99d-349">Operating system</span></span></th>
<th align="left"><span data-ttu-id="5a99d-350">Выпуск</span><span class="sxs-lookup"><span data-stu-id="5a99d-350">Edition</span></span></th>
<th align="left"><span data-ttu-id="5a99d-351">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="5a99d-351">Service pack</span></span></th>
<th align="left"><span data-ttu-id="5a99d-352">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="5a99d-352">System architecture</span></span></th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p><span data-ttu-id="5a99d-353">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="5a99d-353">Windows 10 IoT</span></span></p></td>
      <td align="left"><p><span data-ttu-id="5a99d-354">Функции корпоративного уровня</span><span class="sxs-lookup"><span data-stu-id="5a99d-354">Enterprise</span></span></p></td>
      <td align="left"><p></p></td>
      <td align="left"><p><span data-ttu-id="5a99d-355">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-355">32-bit or 64-bit</span></span></p></td>
 </tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-356">Windows 10</span><span class="sxs-lookup"><span data-stu-id="5a99d-356">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-357">Функции корпоративного уровня</span><span class="sxs-lookup"><span data-stu-id="5a99d-357">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-358">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-358">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-359">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5a99d-359">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-360">Функции корпоративного уровня</span><span class="sxs-lookup"><span data-stu-id="5a99d-360">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-361">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-361">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-362">Windows 7;</span><span class="sxs-lookup"><span data-stu-id="5a99d-362">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-363">Корпоративная или максимальная</span><span class="sxs-lookup"><span data-stu-id="5a99d-363">Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-364">SP1</span><span class="sxs-lookup"><span data-stu-id="5a99d-364">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-365">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-365">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-366">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5a99d-366">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-367">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="5a99d-367">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-368">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-368">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a99d-369">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a99d-369">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-370">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="5a99d-370">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5a99d-371">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-371">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a99d-372">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="5a99d-372">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-373">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="5a99d-373">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-374">SP1</span><span class="sxs-lookup"><span data-stu-id="5a99d-374">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a99d-375">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="5a99d-375">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="5a99d-376">MBAM в Azure IaaS</span><span class="sxs-lookup"><span data-stu-id="5a99d-376">MBAM In Azure IaaS</span></span>

<span data-ttu-id="5a99d-377">Сервер MBAM может быть развернут в инфраструктуре Azure как служба (IaaS) в какой-либо из поддерживаемых версий ОС, которые подключаются к службе каталогов Active Directory, размещенной в локальной системе или службе каталогов Active Directory, также размещенной в Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="5a99d-377">The MBAM server can be deployed in Azure Infrastructure as a Service (IaaS) on any of the supported OS versions listed above, connecting to an Active Directory hosted on premises or an Active Directory also hosted in Azure IaaS.</span></span>  <span data-ttu-id="5a99d-378">В [этой статье приведены](https://msdn.microsoft.com/library/azure/jj156090.aspx)сведения о настройке и настройке Active Directory в Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="5a99d-378">Documentation for setting up and configuring Active Directory on Azure IaaS is [here](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span>

<span data-ttu-id="5a99d-379">Клиент MBAM не поддерживается на виртуальных машинах, а также не поддерживается в Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="5a99d-379">The MBAM client is not supported on virtual machines and is also not supported on Azure IaaS.</span></span>


## <span data-ttu-id="5a99d-380">Пакеты исправлений</span><span class="sxs-lookup"><span data-stu-id="5a99d-380">Service releases</span></span> 

- [<span data-ttu-id="5a99d-381">Исправление от апреля 2016</span><span class="sxs-lookup"><span data-stu-id="5a99d-381">April 2016 hotfix</span></span>](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="5a99d-382">Сентябрь 2016 г.</span><span class="sxs-lookup"><span data-stu-id="5a99d-382">September 2016</span></span>](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [<span data-ttu-id="5a99d-383">Декабрь 2016 г.</span><span class="sxs-lookup"><span data-stu-id="5a99d-383">December 2016</span></span>](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [<span data-ttu-id="5a99d-384">Март 2017г.</span><span class="sxs-lookup"><span data-stu-id="5a99d-384">March 2017</span></span>](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [<span data-ttu-id="5a99d-385">Июнь, 2017г.</span><span class="sxs-lookup"><span data-stu-id="5a99d-385">June 2017</span></span>](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="5a99d-386">Сентябрь 2017г.</span><span class="sxs-lookup"><span data-stu-id="5a99d-386">September 2017</span></span>](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [<span data-ttu-id="5a99d-387">Март 2018 г.</span><span class="sxs-lookup"><span data-stu-id="5a99d-387">March 2018</span></span>](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="5a99d-388">2018 июля</span><span class="sxs-lookup"><span data-stu-id="5a99d-388">July 2018</span></span>](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="5a99d-389">2019 мая</span><span class="sxs-lookup"><span data-stu-id="5a99d-389">May 2019</span></span>](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## <span data-ttu-id="5a99d-390">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5a99d-390">Related topics</span></span>


[<span data-ttu-id="5a99d-391">Планирование развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5a99d-391">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="5a99d-392">Подготовка среды для развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5a99d-392">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)




## <span data-ttu-id="5a99d-393">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="5a99d-393">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5a99d-394">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="5a99d-394">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5a99d-395">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5a99d-395">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




