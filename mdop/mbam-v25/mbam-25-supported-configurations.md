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
ms.openlocfilehash: 262cd8c259dc37b291cdaf02caf0e20b7515d38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823892"
---
# <span data-ttu-id="13f24-103">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13f24-103">MBAM 2.5 Supported Configurations</span></span>


<span data-ttu-id="13f24-104">Вы можете выполнить администрирование и мониторинг Microsoft BitLocker (MBAM) 2,5 в изолированной топологии или в топологии интеграции Configuration Manager, которая интегрирует MBAM с System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="13f24-104">You can run Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a Stand-alone topology or in a Configuration Manager Integration topology that integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="13f24-105">Если вы используете рекомендуемую конфигурацию для любой топологии в рабочей среде, MBAM поддерживает до 500 000 MBAM клиентов.</span><span class="sxs-lookup"><span data-stu-id="13f24-105">If you use the recommended configuration for either topology in a production environment, MBAM supports up to 500,000 MBAM clients.</span></span> <span data-ttu-id="13f24-106">Сведения о рекомендуемой архитектуре и функциональных возможностях, которые настроены на каждом сервере для каждой топологии, можно найти в разделе [архитектура высокого уровня для MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="13f24-106">For information about the recommended architecture and features that are configured on each server for each topology, see [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<span data-ttu-id="13f24-107">Дополнительные конфигурации, специфичные для топологии интеграции Configuration Manager, приведены в разделе [версии Configuration Manager, которые MBAM поддерживаются](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="13f24-107">For additional configurations that are specific to the Configuration Manager Integration topology, see [Versions of Configuration Manager that MBAM supports](#bkmk-cm-ramreqs).</span></span>

**<span data-ttu-id="13f24-108">Примечание.</span><span class="sxs-lookup"><span data-stu-id="13f24-108">Note</span></span>**  
<span data-ttu-id="13f24-109">Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="13f24-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="13f24-110">Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="13f24-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="13f24-111">Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="13f24-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



## <span data-ttu-id="13f24-112">Языки, поддерживаемые MBAM</span><span class="sxs-lookup"><span data-stu-id="13f24-112">MBAM Supported Languages</span></span>


<span data-ttu-id="13f24-113">В приведенных ниже таблицах показаны языки, которые поддерживаются клиентом MBAM (включая портал самообслуживания) и сервер MBAM в MBAM 2,5 и MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="13f24-113">The following tables show the languages that are supported for the MBAM Client (including the Self-Service Portal) and the MBAM Server in MBAM 2.5 and MBAM 2.5 SP1.</span></span>

**<span data-ttu-id="13f24-114">Поддерживаемые языки в MBAM 2,5 с пакетом обновления 1 (SP1):</span><span class="sxs-lookup"><span data-stu-id="13f24-114">Supported Languages in MBAM 2.5 SP1:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13f24-115">Языки клиента</span><span class="sxs-lookup"><span data-stu-id="13f24-115">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="13f24-116">Языки сервера</span><span class="sxs-lookup"><span data-stu-id="13f24-116">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-117">Чешский (Чешская Республика) cs-CZ</span><span class="sxs-lookup"><span data-stu-id="13f24-117">Czech (Czech Republic) cs-CZ</span></span></p>
<p><span data-ttu-id="13f24-118">Датский (Дания) da-DK</span><span class="sxs-lookup"><span data-stu-id="13f24-118">Danish (Denmark) da-DK</span></span></p>
<p><span data-ttu-id="13f24-119">Нидерландский (Нидерланды) nl-NL</span><span class="sxs-lookup"><span data-stu-id="13f24-119">Dutch (Netherlands) nl-NL</span></span></p>
<p><span data-ttu-id="13f24-120">Английский (США) EN-US</span><span class="sxs-lookup"><span data-stu-id="13f24-120">English (United States) en-US</span></span></p>
<p><span data-ttu-id="13f24-121">Финский (Финляндия) Fi-FI</span><span class="sxs-lookup"><span data-stu-id="13f24-121">Finnish (Finland) fi-FI</span></span></p>
<p><span data-ttu-id="13f24-122">Французский (Франция) fr-FR</span><span class="sxs-lookup"><span data-stu-id="13f24-122">French (France) fr-FR</span></span></p>
<p><span data-ttu-id="13f24-123">Немецкий (Германия) de-DE</span><span class="sxs-lookup"><span data-stu-id="13f24-123">German (Germany) de-DE</span></span></p>
<p><span data-ttu-id="13f24-124">Греческий (Греция) Эль-GR</span><span class="sxs-lookup"><span data-stu-id="13f24-124">Greek (Greece) el-GR</span></span></p>
<p><span data-ttu-id="13f24-125">Венгерский (Венгрия) hu-HU</span><span class="sxs-lookup"><span data-stu-id="13f24-125">Hungarian (Hungary) hu-HU</span></span></p>
<p><span data-ttu-id="13f24-126">Итальянский (Италия) IT-IT</span><span class="sxs-lookup"><span data-stu-id="13f24-126">Italian (Italy) it-IT</span></span></p>
<p><span data-ttu-id="13f24-127">Японский (Япония) ja-JP</span><span class="sxs-lookup"><span data-stu-id="13f24-127">Japanese (Japan) ja-JP</span></span></p>
<p><span data-ttu-id="13f24-128">Корейский (Корея) ko-KR</span><span class="sxs-lookup"><span data-stu-id="13f24-128">Korean (Korea) ko-KR</span></span></p>
<p><span data-ttu-id="13f24-129">Норвежский (букмол, Норвегия) без датаграмм</span><span class="sxs-lookup"><span data-stu-id="13f24-129">Norwegian, Bokmål (Norway) nb-NO</span></span></p>
<p><span data-ttu-id="13f24-130">Польский (Польша) PL-PL</span><span class="sxs-lookup"><span data-stu-id="13f24-130">Polish (Poland) pl-PL</span></span></p>
<p><span data-ttu-id="13f24-131">Португальский (Бразилия) Пт — BR</span><span class="sxs-lookup"><span data-stu-id="13f24-131">Portuguese (Brazil) pt-BR</span></span></p>
<p><span data-ttu-id="13f24-132">Португальский (Португалия), пт</span><span class="sxs-lookup"><span data-stu-id="13f24-132">Portuguese (Portugal) pt-PT</span></span></p>
<p><span data-ttu-id="13f24-133">Русский (Россия) ru-RU</span><span class="sxs-lookup"><span data-stu-id="13f24-133">Russian (Russia) ru-RU</span></span></p>
<p><span data-ttu-id="13f24-134">Словацкий (Словакия) sk-SK</span><span class="sxs-lookup"><span data-stu-id="13f24-134">Slovak (Slovakia) sk-SK</span></span></p>
<p><span data-ttu-id="13f24-135">Испанский (Испания) ES-ES</span><span class="sxs-lookup"><span data-stu-id="13f24-135">Spanish (Spain) es-ES</span></span></p>
<p><span data-ttu-id="13f24-136">Шведский (Швеция) SV-SE</span><span class="sxs-lookup"><span data-stu-id="13f24-136">Swedish (Sweden) sv-SE</span></span></p>
<p><span data-ttu-id="13f24-137">Турецкий (Турция) tr-TR</span><span class="sxs-lookup"><span data-stu-id="13f24-137">Turkish (Turkey) tr-TR</span></span></p>
<p><span data-ttu-id="13f24-138">Словенский (Словения) SL-SI</span><span class="sxs-lookup"><span data-stu-id="13f24-138">Slovenian (Slovenia) sl-SI</span></span></p>
<p><span data-ttu-id="13f24-139">Упрощенный китайский (КНР) zh-CN</span><span class="sxs-lookup"><span data-stu-id="13f24-139">Simplified Chinese (PRC) zh-CN</span></span></p>
<p><span data-ttu-id="13f24-140">Китайский (традиционное письмо, Тайвань) zh-TW</span><span class="sxs-lookup"><span data-stu-id="13f24-140">Traditional Chinese (Taiwan) zh-TW</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="13f24-141">Английский (США) EN-US</span><span class="sxs-lookup"><span data-stu-id="13f24-141">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="13f24-142">Французский (Франция) fr-FR</span><span class="sxs-lookup"><span data-stu-id="13f24-142">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="13f24-143">Немецкий (Германия) de-DE</span><span class="sxs-lookup"><span data-stu-id="13f24-143">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="13f24-144">Итальянский (Италия) IT-IT</span><span class="sxs-lookup"><span data-stu-id="13f24-144">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="13f24-145">Японский (Япония) ja-JP</span><span class="sxs-lookup"><span data-stu-id="13f24-145">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="13f24-146">Корейский (Корея) ko-KR</span><span class="sxs-lookup"><span data-stu-id="13f24-146">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="13f24-147">Португальский (Бразилия) Пт — BR</span><span class="sxs-lookup"><span data-stu-id="13f24-147">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="13f24-148">Русский (Россия) ru-RU</span><span class="sxs-lookup"><span data-stu-id="13f24-148">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="13f24-149">Испанский (Испания) ES-ES</span><span class="sxs-lookup"><span data-stu-id="13f24-149">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="13f24-150">Упрощенный китайский (КНР) zh-CN</span><span class="sxs-lookup"><span data-stu-id="13f24-150">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="13f24-151">Китайский (традиционное письмо, Тайвань) zh-TW</span><span class="sxs-lookup"><span data-stu-id="13f24-151">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="13f24-152">Поддерживаемые языки в MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="13f24-152">Supported Languages in MBAM 2.5:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13f24-153">Языки клиента</span><span class="sxs-lookup"><span data-stu-id="13f24-153">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="13f24-154">Языки сервера</span><span class="sxs-lookup"><span data-stu-id="13f24-154">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="13f24-155">Английский (США) EN-US</span><span class="sxs-lookup"><span data-stu-id="13f24-155">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="13f24-156">Французский (Франция) fr-FR</span><span class="sxs-lookup"><span data-stu-id="13f24-156">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="13f24-157">Немецкий (Германия) de-DE</span><span class="sxs-lookup"><span data-stu-id="13f24-157">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="13f24-158">Итальянский (Италия) IT-IT</span><span class="sxs-lookup"><span data-stu-id="13f24-158">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="13f24-159">Японский (Япония) ja-JP</span><span class="sxs-lookup"><span data-stu-id="13f24-159">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="13f24-160">Корейский (Корея) ko-KR</span><span class="sxs-lookup"><span data-stu-id="13f24-160">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="13f24-161">Португальский (Бразилия) Пт — BR</span><span class="sxs-lookup"><span data-stu-id="13f24-161">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="13f24-162">Русский (Россия) ru-RU</span><span class="sxs-lookup"><span data-stu-id="13f24-162">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="13f24-163">Испанский (Испания) ES-ES</span><span class="sxs-lookup"><span data-stu-id="13f24-163">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="13f24-164">Упрощенный китайский (КНР) zh-CN</span><span class="sxs-lookup"><span data-stu-id="13f24-164">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="13f24-165">Китайский (традиционное письмо, Тайвань) zh-TW</span><span class="sxs-lookup"><span data-stu-id="13f24-165">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="13f24-166">Английский (США) EN-US</span><span class="sxs-lookup"><span data-stu-id="13f24-166">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="13f24-167">Французский (Франция) fr-FR</span><span class="sxs-lookup"><span data-stu-id="13f24-167">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="13f24-168">Немецкий (Германия) de-DE</span><span class="sxs-lookup"><span data-stu-id="13f24-168">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="13f24-169">Итальянский (Италия) IT-IT</span><span class="sxs-lookup"><span data-stu-id="13f24-169">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="13f24-170">Японский (Япония) ja-JP</span><span class="sxs-lookup"><span data-stu-id="13f24-170">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="13f24-171">Корейский (Корея) ko-KR</span><span class="sxs-lookup"><span data-stu-id="13f24-171">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="13f24-172">Португальский (Бразилия) Пт — BR</span><span class="sxs-lookup"><span data-stu-id="13f24-172">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="13f24-173">Русский (Россия) ru-RU</span><span class="sxs-lookup"><span data-stu-id="13f24-173">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="13f24-174">Испанский (Испания) ES-ES</span><span class="sxs-lookup"><span data-stu-id="13f24-174">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="13f24-175">Упрощенный китайский (КНР) zh-CN</span><span class="sxs-lookup"><span data-stu-id="13f24-175">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="13f24-176">Китайский (традиционное письмо, Тайвань) zh-TW</span><span class="sxs-lookup"><span data-stu-id="13f24-176">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="13f24-177">Требования к серверной системе MBAM</span><span class="sxs-lookup"><span data-stu-id="13f24-177">MBAM Server system requirements</span></span>


### <span data-ttu-id="13f24-178">Требования к серверной операционной системе MBAM</span><span class="sxs-lookup"><span data-stu-id="13f24-178">MBAM Server operating system requirements</span></span>

<span data-ttu-id="13f24-179">Настоятельно рекомендуется запускать клиент MBAM и сервер MBAM в одной и той же строке операционной системы.</span><span class="sxs-lookup"><span data-stu-id="13f24-179">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="13f24-180">Например, Windows 10 с Windows Server 2016, Windows 8,1 с Windows Server 2012 R2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="13f24-180">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="13f24-181">В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="13f24-181">The following table lists the operating systems that are supported for the MBAM Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13f24-182">Операционная система</span><span class="sxs-lookup"><span data-stu-id="13f24-182">Operating system</span></span></th>
<th align="left"><span data-ttu-id="13f24-183">Выпуск</span><span class="sxs-lookup"><span data-stu-id="13f24-183">Edition</span></span></th>
<th align="left"><span data-ttu-id="13f24-184">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="13f24-184">Service pack</span></span></th>
<th align="left"><span data-ttu-id="13f24-185">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="13f24-185">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-186">Windows Server2016</span><span class="sxs-lookup"><span data-stu-id="13f24-186">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-187">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="13f24-187">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="13f24-188">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-188">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-189">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="13f24-189">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-190">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="13f24-190">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="13f24-191">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-191">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-192">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13f24-192">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-193">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="13f24-193">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="13f24-194">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-194">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-195">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="13f24-195">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-196">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="13f24-196">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-197">SP1</span><span class="sxs-lookup"><span data-stu-id="13f24-197">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-198">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-198">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="13f24-199">Корпоративный домен должен содержать по крайней мере один контроллер домена Windows Server 2008 (или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="13f24-199">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span>

### <a href="" id="bkmk-stand-alone-ramreqs"></a><span data-ttu-id="13f24-200">MBAM, оперативная память и требования к дисковому пространству — изолированная топология</span><span class="sxs-lookup"><span data-stu-id="13f24-200">MBAM Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="13f24-201">Эти требования предназначены для изолированной топологии MBAM.</span><span class="sxs-lookup"><span data-stu-id="13f24-201">These requirements are for the MBAM Stand-alone topology.</span></span> <span data-ttu-id="13f24-202">Требования к топологии интеграции Configuration Manager можно найти в разделе [процессор сервера MBAM, ОЗУ и требования к дисковому пространству — топология интеграции Configuration Manager](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="13f24-202">For the requirements for the Configuration Manager Integration topology, see [MBAM Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13f24-203">Элемент оборудования</span><span class="sxs-lookup"><span data-stu-id="13f24-203">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="13f24-204">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="13f24-204">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="13f24-205">Рекомендуемое требование</span><span class="sxs-lookup"><span data-stu-id="13f24-205">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-206">Процессор</span><span class="sxs-lookup"><span data-stu-id="13f24-206">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-207">2,33 ГГц</span><span class="sxs-lookup"><span data-stu-id="13f24-207">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-208">2,33 ГГц или выше</span><span class="sxs-lookup"><span data-stu-id="13f24-208">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-209">ОЗУ</span><span class="sxs-lookup"><span data-stu-id="13f24-209">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-210">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-210">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-211">12 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-211">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-212">Свободное место на диске</span><span class="sxs-lookup"><span data-stu-id="13f24-212">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-213">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-213">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-214">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-214">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a><span data-ttu-id="13f24-215">Требования к процессору сервера MBAM, ОЗУ и дисковому пространству — топология интеграции Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="13f24-215">MBAM Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="13f24-216">В таблице ниже перечислены требования к серверному процессору, ОЗУ и дисковому пространству для серверов MBAM при использовании топологии интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="13f24-216">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span> <span data-ttu-id="13f24-217">Требования для изолированной топологии можно найти в разделе [процессор сервера MBAM, ОЗУ и требования к дисковому пространству — изолированная топология](#bkmk-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="13f24-217">For the requirements for the Stand-alone topology, see [MBAM Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13f24-218">Элемент оборудования</span><span class="sxs-lookup"><span data-stu-id="13f24-218">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="13f24-219">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="13f24-219">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="13f24-220">Рекомендуемое требование</span><span class="sxs-lookup"><span data-stu-id="13f24-220">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-221">Процессор</span><span class="sxs-lookup"><span data-stu-id="13f24-221">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-222">2,33 ГГц</span><span class="sxs-lookup"><span data-stu-id="13f24-222">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-223">2,33 ГГц или выше</span><span class="sxs-lookup"><span data-stu-id="13f24-223">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-224">ОЗУ</span><span class="sxs-lookup"><span data-stu-id="13f24-224">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-225">4 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-225">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-226">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-226">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-227">Свободное место на диске</span><span class="sxs-lookup"><span data-stu-id="13f24-227">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-228">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-228">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-229">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-229">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a><span data-ttu-id="13f24-230">Версии Configuration Manager, которые поддерживает MBAM</span><span class="sxs-lookup"><span data-stu-id="13f24-230">Versions of Configuration Manager that MBAM supports</span></span>

<span data-ttu-id="13f24-231">MBAM поддерживает следующие версии Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="13f24-231">MBAM supports the following versions of Configuration Manager.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13f24-232">Поддерживаемая версия</span><span class="sxs-lookup"><span data-stu-id="13f24-232">Supported version</span></span></th>
<th align="left"><span data-ttu-id="13f24-233">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="13f24-233">Service pack</span></span></th>
<th align="left"><span data-ttu-id="13f24-234">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="13f24-234">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-235">Microsoft System Center Configuration Manager (Текущая ветвь), версии до 1902</span><span class="sxs-lookup"><span data-stu-id="13f24-235">Microsoft System Center Configuration Manager (Current Branch), versions up to 1902</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="13f24-236">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-236">64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-237">Microsoft System Center Configuration Manager 1806</span><span class="sxs-lookup"><span data-stu-id="13f24-237">Microsoft System Center Configuration Manager 1806</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="13f24-238">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-238">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-239">Microsoft System Center Configuration Manager (LTSB-Version 1606)</span><span class="sxs-lookup"><span data-stu-id="13f24-239">Microsoft System Center Configuration Manager (LTSB - version 1606)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="13f24-240">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-240">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-241">Microsoft System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="13f24-241">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-242">SP1</span><span class="sxs-lookup"><span data-stu-id="13f24-242">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-243">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-243">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-244">Microsoft System Center Configuration Manager 2007 R2 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="13f24-244">Microsoft System Center Configuration Manager 2007 R2 or later</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="13f24-245">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-245">64-bit</span></span></p>

<span data-ttu-id="13f24-246">&gt;<strong>Примечание </strong> несмотря на то, что Configuration Manager 2007 R2 имеет значение 32, необходимо установить его и SQL Server на 64-разрядную версию операционной системы, чтобы обеспечить соответствие с программным обеспечением 64-bit MBAM.</span><span class="sxs-lookup"><span data-stu-id="13f24-246">&gt;<strong>Note</strong> Although Configuration Manager 2007 R2 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span>
</td>
</tr>
</tbody>
</table>



<span data-ttu-id="13f24-247">Список поддерживаемых конфигураций для сервера Configuration Manager можно найти в соответствующей документации TechNet о версии Configuration Manager, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="13f24-247">For a list of supported configurations for the Configuration Manager Server, see the appropriate TechNet documentation for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="13f24-248">В MBAM отсутствуют дополнительные требования к системе для сервера Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="13f24-248">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="13f24-249">Требования к базам данных SQL Server</span><span class="sxs-lookup"><span data-stu-id="13f24-249">SQL Server database requirements</span></span>

<span data-ttu-id="13f24-250">В приведенной ниже таблице указаны версии Microsoft SQL Server, которые поддерживаются для функций сервера MBAM, включая базу данных восстановления, базу данных соответствия требованиям и журнал аудита, а также функцию отчеты.</span><span class="sxs-lookup"><span data-stu-id="13f24-250">The following table lists the Microsoft SQL Server versions that are supported for the MBAM Server features, which include the Recovery Database, Compliance and Audit Database, and the Reports feature.</span></span> <span data-ttu-id="13f24-251">Требуемые версии применяются к отдельным топологиям или топологии интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="13f24-251">The required versions apply to the Stand-alone or the Configuration Manager Integration topologies.</span></span>

<span data-ttu-id="13f24-252">Необходимо установить SQL Server с параметрами сортировки **SQL \ _Latin1 \ _General \ _CP1 \ _CI \ _AS** .</span><span class="sxs-lookup"><span data-stu-id="13f24-252">You must install SQL Server with the **SQL\_Latin1\_General\_CP1\_CI\_AS** collation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13f24-253">Версия SQL Server</span><span class="sxs-lookup"><span data-stu-id="13f24-253">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="13f24-254">Выпуск</span><span class="sxs-lookup"><span data-stu-id="13f24-254">Edition</span></span></th>
<th align="left"><span data-ttu-id="13f24-255">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="13f24-255">Service pack</span></span></th>
<th align="left"><span data-ttu-id="13f24-256">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="13f24-256">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-257">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="13f24-257">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-258">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="13f24-258">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="13f24-259">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-259">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="13f24-260">Microsoft SQL Server2016</span><span class="sxs-lookup"><span data-stu-id="13f24-260">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-261">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="13f24-261">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-262">SP1</span><span class="sxs-lookup"><span data-stu-id="13f24-262">SP1</span></span></p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p><span data-ttu-id="13f24-263">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-263">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-264">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="13f24-264">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-265">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="13f24-265">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-266">ПАКЕТ ОБНОВЛЕНИЯ 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="13f24-266">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-267">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-267">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-268">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="13f24-268">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-269">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="13f24-269">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-270">ОБНОВЛЕНИЙ</span><span class="sxs-lookup"><span data-stu-id="13f24-270">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-271">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-271">64-bit</span></span></p></td>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-272">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13f24-272">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-273">Standard или Enterprise</span><span class="sxs-lookup"><span data-stu-id="13f24-273">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-274">ОБНОВЛЕНИЙ</span><span class="sxs-lookup"><span data-stu-id="13f24-274">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-275">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-275">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

**<span data-ttu-id="13f24-276">Примечание.</span><span class="sxs-lookup"><span data-stu-id="13f24-276">Note</span></span>**  
<span data-ttu-id="13f24-277">Для поддержки SQL 2016 необходимо установить выпуск за март 2017 для MDOP https://www.microsoft.com/download/details.aspx?id=54967 , а также поддержку sql 2017 вы должны установить выпуск за июль 2018 и сопровождение для MDOP https://www.microsoft.com/download/details.aspx?id=57157 .</span><span class="sxs-lookup"><span data-stu-id="13f24-277">In order to support SQL 2016 you must install the March 2017 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=54967  and to support SQL 2017 you must install the July 2018 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=57157.</span></span> <span data-ttu-id="13f24-278">В общем, всегда используйте Последнее обновление обслуживания, поскольку оно также включает все исправления ошибок и новые возможности.</span><span class="sxs-lookup"><span data-stu-id="13f24-278">In general stay current by always using the most recent servicing update as it also includes all bugfixes and new features.</span></span>


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a><span data-ttu-id="13f24-279">Требования процессора SQL Server, ОЗУ и места на диске — изолированная топология</span><span class="sxs-lookup"><span data-stu-id="13f24-279">SQL Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="13f24-280">В таблице ниже перечислены рекомендуемые требования к серверному процессору, ОЗУ и дисковому пространству для компьютера SQL Server при использовании изолированной топологии.</span><span class="sxs-lookup"><span data-stu-id="13f24-280">The following table lists the recommended server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Stand-alone topology.</span></span> <span data-ttu-id="13f24-281">Используйте эти требования как руководство.</span><span class="sxs-lookup"><span data-stu-id="13f24-281">Use these requirements as a guide.</span></span> <span data-ttu-id="13f24-282">Конкретные требования будут зависеть от количества клиентских компьютеров, которые поддерживаются в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="13f24-282">Your specific requirements will vary based on the number of client computers you are supporting in your enterprise.</span></span> <span data-ttu-id="13f24-283">Сведения о требованиях к топологии интеграции Configuration Manager можно найти в разделе [требования к процессорам SQL Server, ОЗУ и пространству на диске — топология интеграции Configuration Manager](#bkmk-cm-sql-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="13f24-283">To view the requirements for the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-sql-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13f24-284">Элемент оборудования</span><span class="sxs-lookup"><span data-stu-id="13f24-284">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="13f24-285">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="13f24-285">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="13f24-286">Рекомендуемое требование</span><span class="sxs-lookup"><span data-stu-id="13f24-286">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-287">Процессор</span><span class="sxs-lookup"><span data-stu-id="13f24-287">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-288">2,33 ГГц</span><span class="sxs-lookup"><span data-stu-id="13f24-288">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-289">2,33 ГГц или выше</span><span class="sxs-lookup"><span data-stu-id="13f24-289">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-290">ОЗУ</span><span class="sxs-lookup"><span data-stu-id="13f24-290">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-291">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-291">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-292">12 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-292">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-293">Свободное место на диске</span><span class="sxs-lookup"><span data-stu-id="13f24-293">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-294">5 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-294">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-295">5 ГБ или больше</span><span class="sxs-lookup"><span data-stu-id="13f24-295">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a><span data-ttu-id="13f24-296">Требования для процессора SQL Server, ОЗУ и места на диске — топология интеграции Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="13f24-296">SQL Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="13f24-297">В приведенной ниже таблице перечислены требования к серверному процессору, ОЗУ и дисковому пространству для компьютера с Microsoft SQL Server при использовании топологии интеграции Configuration Manager [: изолированная топология процессора SQL Server, ОЗУ и места на диске](#bkmk-sql-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="13f24-297">The following table lists the server processor, RAM, and disk space requirements for the Microsoft SQL Server computer when you are using the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-sql-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13f24-298">Элемент оборудования</span><span class="sxs-lookup"><span data-stu-id="13f24-298">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="13f24-299">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="13f24-299">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="13f24-300">Рекомендуемое требование</span><span class="sxs-lookup"><span data-stu-id="13f24-300">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-301">Процессор</span><span class="sxs-lookup"><span data-stu-id="13f24-301">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-302">2,33 ГГц</span><span class="sxs-lookup"><span data-stu-id="13f24-302">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-303">2,33 ГГц или выше</span><span class="sxs-lookup"><span data-stu-id="13f24-303">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-304">ОЗУ</span><span class="sxs-lookup"><span data-stu-id="13f24-304">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-305">4 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-305">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-306">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-306">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-307">Свободное место на диске</span><span class="sxs-lookup"><span data-stu-id="13f24-307">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-308">5 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-308">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-309">5 ГБ</span><span class="sxs-lookup"><span data-stu-id="13f24-309">5 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="13f24-310">Требования к системе клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="13f24-310">MBAM Client system requirements</span></span>


### <span data-ttu-id="13f24-311">Требования к операционной системе клиента</span><span class="sxs-lookup"><span data-stu-id="13f24-311">Client operating system requirements</span></span>

<span data-ttu-id="13f24-312">Настоятельно рекомендуется запускать клиент MBAM и сервер MBAM в одной и той же строке операционной системы.</span><span class="sxs-lookup"><span data-stu-id="13f24-312">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="13f24-313">Например, Windows 10 с Windows Server 2016, Windows 8,1 с Windows Server 2012 R2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="13f24-313">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="13f24-314">В таблице ниже перечислены операционные системы, которые поддерживаются при установке клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="13f24-314">The following table lists the operating systems that are supported for MBAM Client installation.</span></span> <span data-ttu-id="13f24-315">Те же требования применимы к отдельным топологиям и топологии интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="13f24-315">The same requirements apply to the Stand-alone and the Configuration Manager Integration topologies.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13f24-316">Операционная система</span><span class="sxs-lookup"><span data-stu-id="13f24-316">Operating system</span></span></th>
<th align="left"><span data-ttu-id="13f24-317">Выпуск</span><span class="sxs-lookup"><span data-stu-id="13f24-317">Edition</span></span></th>
<th align="left"><span data-ttu-id="13f24-318">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="13f24-318">Service pack</span></span></th>
<th align="left"><span data-ttu-id="13f24-319">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="13f24-319">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p><span data-ttu-id="13f24-320">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="13f24-320">Windows 10 IoT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="13f24-321">Функции корпоративного уровня</span><span class="sxs-lookup"><span data-stu-id="13f24-321">Enterprise</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p><span data-ttu-id="13f24-322">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-322">32-bit or 64-bit</span></span></p></td>
</tr><br/><tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-323">Windows 10;</span><span class="sxs-lookup"><span data-stu-id="13f24-323">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-324">Функции корпоративного уровня</span><span class="sxs-lookup"><span data-stu-id="13f24-324">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="13f24-325">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-325">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-326">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="13f24-326">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-327">Функции корпоративного уровня</span><span class="sxs-lookup"><span data-stu-id="13f24-327">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="13f24-328">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-328">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-329">Windows 7;</span><span class="sxs-lookup"><span data-stu-id="13f24-329">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-330">Корпоративная или максимальная</span><span class="sxs-lookup"><span data-stu-id="13f24-330">Enterprise or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-331">SP1</span><span class="sxs-lookup"><span data-stu-id="13f24-331">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-332">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-332">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-333">Windows с собой</span><span class="sxs-lookup"><span data-stu-id="13f24-333">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-334">Windows 8,1 и Windows 10 корпоративный</span><span class="sxs-lookup"><span data-stu-id="13f24-334">Windows 8.1 and Windows 10 Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="13f24-335">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-335">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="13f24-336">Требования к ОЗУ для клиента</span><span class="sxs-lookup"><span data-stu-id="13f24-336">Client RAM requirements</span></span>

<span data-ttu-id="13f24-337">Нет требований к ОЗУ, которые относятся к установке клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="13f24-337">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="13f24-338">Системные требования для групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="13f24-338">MBAM Group Policy system requirements</span></span>


<span data-ttu-id="13f24-339">В таблице ниже перечислены операционные системы, которые поддерживаются при установке шаблонов групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="13f24-339">The following table lists the operating systems that are supported for MBAM Group Policy Templates installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13f24-340">Операционная система</span><span class="sxs-lookup"><span data-stu-id="13f24-340">Operating system</span></span></th>
<th align="left"><span data-ttu-id="13f24-341">Выпуск</span><span class="sxs-lookup"><span data-stu-id="13f24-341">Edition</span></span></th>
<th align="left"><span data-ttu-id="13f24-342">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="13f24-342">Service pack</span></span></th>
<th align="left"><span data-ttu-id="13f24-343">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="13f24-343">System architecture</span></span></th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p><span data-ttu-id="13f24-344">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="13f24-344">Windows 10 IoT</span></span></p></td>
      <td align="left"><p><span data-ttu-id="13f24-345">Функции корпоративного уровня</span><span class="sxs-lookup"><span data-stu-id="13f24-345">Enterprise</span></span></p></td>
      <td align="left"><p></p></td>
      <td align="left"><p><span data-ttu-id="13f24-346">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-346">32-bit or 64-bit</span></span></p></td>
 </tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-347">Windows 10;</span><span class="sxs-lookup"><span data-stu-id="13f24-347">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-348">Функции корпоративного уровня</span><span class="sxs-lookup"><span data-stu-id="13f24-348">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="13f24-349">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-349">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-350">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="13f24-350">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-351">Функции корпоративного уровня</span><span class="sxs-lookup"><span data-stu-id="13f24-351">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="13f24-352">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-352">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-353">Windows 7;</span><span class="sxs-lookup"><span data-stu-id="13f24-353">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-354">Корпоративная или максимальная</span><span class="sxs-lookup"><span data-stu-id="13f24-354">Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-355">SP1</span><span class="sxs-lookup"><span data-stu-id="13f24-355">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-356">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-356">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-357">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="13f24-357">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-358">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="13f24-358">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="13f24-359">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-359">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13f24-360">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13f24-360">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-361">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="13f24-361">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="13f24-362">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-362">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13f24-363">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="13f24-363">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-364">Стандартный, корпоративный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="13f24-364">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-365">SP1</span><span class="sxs-lookup"><span data-stu-id="13f24-365">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="13f24-366">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="13f24-366">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="13f24-367">MBAM в Azure IaaS</span><span class="sxs-lookup"><span data-stu-id="13f24-367">MBAM In Azure IaaS</span></span>

<span data-ttu-id="13f24-368">Сервер MBAM может быть развернут в инфраструктуре Azure как служба (IaaS) в какой-либо из поддерживаемых версий ОС, которые подключаются к службе каталогов Active Directory, размещенной в локальной системе или службе каталогов Active Directory, также размещенной в Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="13f24-368">The MBAM server can be deployed in Azure Infrastructure as a Service (IaaS) on any of the supported OS versions listed above, connecting to an Active Directory hosted on premises or an Active Directory also hosted in Azure IaaS.</span></span>  <span data-ttu-id="13f24-369">В [этой статье приведены](https://msdn.microsoft.com/library/azure/jj156090.aspx)сведения о настройке и настройке Active Directory в Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="13f24-369">Documentation for setting up and configuring Active Directory on Azure IaaS is [here](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span>

<span data-ttu-id="13f24-370">Клиент MBAM не поддерживается на виртуальных машинах, а также не поддерживается в Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="13f24-370">The MBAM client is not supported on virtual machines and is also not supported on Azure IaaS.</span></span>


## <span data-ttu-id="13f24-371">Пакеты исправлений</span><span class="sxs-lookup"><span data-stu-id="13f24-371">Service releases</span></span> 

- [<span data-ttu-id="13f24-372">Исправление от апреля 2016</span><span class="sxs-lookup"><span data-stu-id="13f24-372">April 2016 hotfix</span></span>](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="13f24-373">Сентябрь 2016 г.</span><span class="sxs-lookup"><span data-stu-id="13f24-373">September 2016</span></span>](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [<span data-ttu-id="13f24-374">Декабрь 2016 г.</span><span class="sxs-lookup"><span data-stu-id="13f24-374">December 2016</span></span>](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [<span data-ttu-id="13f24-375">Март 2017г.</span><span class="sxs-lookup"><span data-stu-id="13f24-375">March 2017</span></span>](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [<span data-ttu-id="13f24-376">Июнь, 2017г.</span><span class="sxs-lookup"><span data-stu-id="13f24-376">June 2017</span></span>](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="13f24-377">Сентябрь 2017г.</span><span class="sxs-lookup"><span data-stu-id="13f24-377">September 2017</span></span>](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [<span data-ttu-id="13f24-378">Март 2018 г.</span><span class="sxs-lookup"><span data-stu-id="13f24-378">March 2018</span></span>](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="13f24-379">2018 июля</span><span class="sxs-lookup"><span data-stu-id="13f24-379">July 2018</span></span>](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="13f24-380">2019 мая</span><span class="sxs-lookup"><span data-stu-id="13f24-380">May 2019</span></span>](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## <span data-ttu-id="13f24-381">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="13f24-381">Related topics</span></span>


[<span data-ttu-id="13f24-382">Планирование развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13f24-382">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="13f24-383">Подготовка среды для развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13f24-383">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)




## <span data-ttu-id="13f24-384">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="13f24-384">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="13f24-385">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="13f24-385">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="13f24-386">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="13f24-386">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




