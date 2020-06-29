---
title: Выбор версии AGPM для установки
description: Выбор версии AGPM для установки
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: b09ea8161b6801c62552f1c0d0ef8455dc111e2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819099"
---
# <span data-ttu-id="41270-103">Выбор версии AGPM для установки</span><span class="sxs-lookup"><span data-stu-id="41270-103">Choosing Which Version of AGPM to Install</span></span>


<span data-ttu-id="41270-104">Каждый выпуск управления групповыми политиками MicrosoftAdvanced поддерживает определенные версии операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="41270-104">Each release of MicrosoftAdvanced Group Policy Management (AGPM) supports specific versions of the Windows operating system.</span></span> <span data-ttu-id="41270-105">Мы настоятельно рекомендуем использовать клиент и сервер РАСШИРЕНного использования РАСШИРЕНного взаимодействия в той же строке операционной системы.</span><span class="sxs-lookup"><span data-stu-id="41270-105">We strongly recommend that you run the AGPM Client and AGPM Server on the same line of operating systems.</span></span> <span data-ttu-id="41270-106">Например, Windows 10 с Windows Server 2016, Windows 8.1 и Windows Server2012 R2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="41270-106">For example, Windows 10 with Windows Server 2016, Windows8.1 with Windows Server2012 R2, and so on.</span></span>

<span data-ttu-id="41270-107">Рекомендуем установить сервер расширенного управления групповыми политиками в новейшей версии операционной системы домена.</span><span class="sxs-lookup"><span data-stu-id="41270-107">We recommend that you install the AGPM Server on the most recent version of the operating system in the domain.</span></span> <span data-ttu-id="41270-108">С помощью консоли управления групповыми политиками (GPMC) можно архивировать и восстанавливать объекты групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="41270-108">AGPM uses the Group Policy Management Console (GPMC) to back up and restore Group Policy Objects (GPOs).</span></span> <span data-ttu-id="41270-109">Поскольку новые версии GPMC предоставляют дополнительные параметры политики, недоступные в более ранних версиях, вы можете управлять дополнительными параметрами политики, используя самую последнюю версию операционной системы.</span><span class="sxs-lookup"><span data-stu-id="41270-109">Because newer versions of the GPMC provide additional policy settings that are not available in earlier versions, you can manage more policy settings by using the most recent version of the operating system.</span></span>

<span data-ttu-id="41270-110">Все версии расширенного управления групповыми политиками могут управлять только параметрами политики, которые были введены в той же или более ранней версии операционной системы, в которой работает служба управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="41270-110">All versions of AGPM can manage only the policy settings that were introduced in the same version or an earlier version of the operating system on which AGPM is running.</span></span> <span data-ttu-id="41270-111">Например, если установить пакет обновления 2 (SP2) для Windows Server 2012, вы можете управлять параметрами политики, которые были введены в Windows Server 2012 или более ранней версии, но вы не можете управлять параметрами политики, которые появились позже в Windows 8.1 или Windows Server2012 R2.</span><span class="sxs-lookup"><span data-stu-id="41270-111">For example, if you install AGPM4.0 SP2 on Windows Server 2012, you can manage policy settings that were introduced in Windows Server 2012 or earlier, but you cannot manage policy settings that were introduced later, in Windows8.1 or Windows Server2012 R2.</span></span>

<span data-ttu-id="41270-112">Если версия GPMC на сервере управления ГРУППОВыми политиками старше, чем версия на компьютерах, используемых администраторами для управления групповой политикой, сервер управления ГРУППОВыми политиками не сможет хранить параметры политики, недоступные в более ранней версии GPMC.</span><span class="sxs-lookup"><span data-stu-id="41270-112">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store any policy settings that are not available in the older version of the GPMC.</span></span> <span data-ttu-id="41270-113">Таблицу параметров групповой политики, включенных в Windows, см. в [Справочнике по параметрам групповой политики Windows и Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span><span class="sxs-lookup"><span data-stu-id="41270-113">For a spreadsheet of Group Policy settings included in Windows, see [Group Policy Settings Reference for Windows and Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span></span>

## <span data-ttu-id="41270-114">РАСШИРЕННАЯ ВЕРСИЯ ДЛЯ ВЕРСИИ 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="41270-114">AGPM4.0 SP3</span></span>


<span data-ttu-id="41270-115">Если вы используете на компьютерах под управлением Windows 10 Управление объектами групповой политики, необходимо использовать параметр РАСШИРЕНного обновления для 4,0.</span><span class="sxs-lookup"><span data-stu-id="41270-115">If you are using computers that are running Windows 10 to manage GPOs, you must use AGPM 4.0 SP3.</span></span> <span data-ttu-id="41270-116">На компьютерах под управлением операционной системы Windows 10 невозможно установить более раннюю версию РАСШИРЕНного использования службы.</span><span class="sxs-lookup"><span data-stu-id="41270-116">You cannot install earlier versions of AGPM on computers that are running the Windows 10 operating system.</span></span>

<span data-ttu-id="41270-117">В таблице 1 перечислены операционные системы, для которых вы можете установить пакет управления групповыми политиками версии 4.0 SP3, и параметры политики, которые можно управлять с помощью расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="41270-117">Table 1 lists the operating systems on which you can install AGPM4.0 SP3, and the policy settings that you can manage by using AGPM4.0 SP3.</span></span>

**<span data-ttu-id="41270-118">Таблица 1: РАСШИРЕНная поддержка операционных систем и параметров политики в конфигурации со всеми 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="41270-118">Table 1: AGPM 4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="41270-119">Поддерживаемые конфигурации для сервера РАСШИРЕНного языка</span><span class="sxs-lookup"><span data-stu-id="41270-119">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="41270-120">Поддерживаемые конфигурации для клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="41270-120">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="41270-121">Поддержка РАСШИРЕНных возможностей</span><span class="sxs-lookup"><span data-stu-id="41270-121">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-122">Windows Server 2016 или Windows 10</span><span class="sxs-lookup"><span data-stu-id="41270-122">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-123">Windows Server 2016 или Windows 10</span><span class="sxs-lookup"><span data-stu-id="41270-123">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-124">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="41270-124">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41270-125">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="41270-125">Windows Server2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-126">Windows 10;</span><span class="sxs-lookup"><span data-stu-id="41270-126">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-127">Поддерживается с помощью предостережений, описанных в <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> статьях KB 4015786</span><span class="sxs-lookup"><span data-stu-id="41270-127">Supported with the caveats outlined in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)">KB 4015786</span></span></a>
</p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-128">Windows Server2012 R2 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41270-128">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-129">Windows Server2012 R2 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41270-129">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="41270-130">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41270-131">Windows Server2012 R2, Windows Server 2012 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41270-131">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-132">Windows Server 2012 или Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="41270-132">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-133">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41270-133">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-134">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-134">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-135">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-135">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-136">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41270-136">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41270-137">Windows Server 2012, Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-137">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-138">Windows Server2008 или WindowsVista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-138">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-139">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-139">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-140">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-140">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-141">Windows Server 2012, Windows Server2008R2, Windows 8 и Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-141">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-142">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="41270-142">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41270-143">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-143">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-144">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-144">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-145">Поддерживается, но не может сообщить или изменить параметры политики или элементы предпочтений, существующие только в Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-145">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="41270-146">РАСШИРЕННОЕ ОБНОВЛЕНИЕ ДЛЯ ВЕРСИИ 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="41270-146">AGPM4.0 SP2</span></span>


<span data-ttu-id="41270-147">Если вы используете компьютеры с операционной системой Windows Server2012 R2 или Windows 8.1 для управления объектами групповой политики, необходимо использовать многодоменные версии 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="41270-147">If you are using computers that are running Windows Server2012 R2 or Windows8.1 to manage GPOs, you must use AGPM4.0 SP2.</span></span> <span data-ttu-id="41270-148">Вы не можете установить более ранние версии РАСШИРЕНного использования службы на компьютерах под управлением этих операционных систем.</span><span class="sxs-lookup"><span data-stu-id="41270-148">You cannot install earlier versions of AGPM on computers that are running those operating systems.</span></span>

<span data-ttu-id="41270-149">В таблице 1 перечислены операционные системы, для которых можно установить пакет управления групповыми политиками и параметры политики, которые можно управлять с помощью РАСШИРЕНного обновления для версии 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="41270-149">Table 1 lists the operating systems on which you can install AGPM4.0 SP2, and the policy settings that you can manage by using AGPM4.0 SP2.</span></span>

**<span data-ttu-id="41270-150">Таблица 2. Поддерживаемые операционные системы и параметры политики для РАСШИРЕНной версии 4.0 с пакетом обновления</span><span class="sxs-lookup"><span data-stu-id="41270-150">Table 2: AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="41270-151">Поддерживаемые конфигурации для сервера РАСШИРЕНного языка</span><span class="sxs-lookup"><span data-stu-id="41270-151">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="41270-152">Поддерживаемые конфигурации для клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="41270-152">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="41270-153">Поддержка РАСШИРЕНных возможностей</span><span class="sxs-lookup"><span data-stu-id="41270-153">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-154">Windows Server2012 R2 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41270-154">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-155">Windows Server2012 R2 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41270-155">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-156">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="41270-156">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41270-157">Windows Server2012 R2, Windows Server 2012 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41270-157">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-158">Windows Server 2012 или Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="41270-158">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-159">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41270-159">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-160">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-160">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-161">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-161">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-162">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41270-162">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41270-163">Windows Server 2012, Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-163">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-164">Windows Server2008 или WindowsVista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-164">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-165">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-165">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-166">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-166">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-167">Windows Server 2012, Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-167">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-168">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="41270-168">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41270-169">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-169">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-170">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-170">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-171">Поддерживается, но не может сообщить или изменить параметры политики или элементы предпочтений, существующие только в Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-171">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="41270-172">РАСШИРЕННАЯ ВЕРСИЯ ДЛЯ NT 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="41270-172">AGPM4.0 SP1</span></span>


<span data-ttu-id="41270-173">В таблице 2 перечислены операционные системы, для которых можно установить 4,0 РАСШИРЕНную настройку конфигурации с пакетом обновления 1 (SP1), а также параметры политики, которые можно управлять с помощью РАСШИРЕНного пакета администрирования.</span><span class="sxs-lookup"><span data-stu-id="41270-173">Table 2 lists the operating systems on which you can install AGPM 4.0 SP1, and the policy settings that you can manage by using AGPM4.0 SP1.</span></span>

**<span data-ttu-id="41270-174">Таблица 3: РАСШИРЕНная поддержка операционных систем и параметров политики в версии 4.0 с пакетом обновления (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-174">Table 3: AGPM4.0 SP1 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="41270-175">Поддерживаемые конфигурации для сервера РАСШИРЕНного языка</span><span class="sxs-lookup"><span data-stu-id="41270-175">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="41270-176">Поддерживаемые конфигурации для клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="41270-176">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="41270-177">Поддержка РАСШИРЕНных возможностей</span><span class="sxs-lookup"><span data-stu-id="41270-177">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="41270-178">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-179">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="41270-179">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-180">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="41270-180">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41270-181">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-181">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-182">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-182">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-183">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="41270-183">Supported, but cannot edit policy settings or preference items that exist only in Windows 8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-184">Windows Server 2012, Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-184">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-185">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-185">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-186">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-186">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41270-187">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-187">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-188">Windows Server 2012, Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-188">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-189">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="41270-189">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-190">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-191">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-191">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-192">Поддерживается, но не может сообщать или изменять параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-192">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="41270-193">РАСШИРЕНная версия для версии 4.0</span><span class="sxs-lookup"><span data-stu-id="41270-193">AGPM4.0</span></span>


<span data-ttu-id="41270-194">В таблице 3 перечислены операционные системы, для которых можно установить параметры расширенного управления групповыми политиками 4,0, а также настройки политики, которые можно управлять с помощью служб управления ГРУППОВыми политиками.</span><span class="sxs-lookup"><span data-stu-id="41270-194">Table 3 lists the operating systems on which you can install AGPM 4.0, and the policy settings that you can manage by using AGPM4.0.</span></span>

**<span data-ttu-id="41270-195">Таблица 4: Поддерживаемые операционные системы и параметры политики для РАСШИРЕНной версии 4.0</span><span class="sxs-lookup"><span data-stu-id="41270-195">Table 4: AGPM4.0 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="41270-196">Поддерживаемые операционные системы для сервера РАСШИРЕНного языка</span><span class="sxs-lookup"><span data-stu-id="41270-196">Supported operating systems for the AGPM Server</span></span></th>
<th align="left"><span data-ttu-id="41270-197">Поддерживаемые операционные системы для клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="41270-197">Supported operating systems for the AGPM Client</span></span></th>
<th align="left"><span data-ttu-id="41270-198">Поддержка РАСШИРЕНных возможностей</span><span class="sxs-lookup"><span data-stu-id="41270-198">AGPM Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-199">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-199">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-200">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-200">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-201">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="41270-201">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41270-202">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-202">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-203">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-203">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-204">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-204">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-205">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-205">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-206">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-206">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-207">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="41270-207">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41270-208">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-208">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-209">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-209">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-210">Поддерживается, но не может сообщать или изменять параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="41270-210">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="41270-211">Версии РАСШИРЕНного типа данных, предшествующих РАСШИРЕНному (для версии 4.0)</span><span class="sxs-lookup"><span data-stu-id="41270-211">Versions of AGPM that precede AGPM4.0</span></span>


<span data-ttu-id="41270-212">В таблице 4 перечислены операционные системы, для которых вы можете установить версии РАСШИРЕНного типа, предшествующие РАСШИРЕНию для версии 4.0.</span><span class="sxs-lookup"><span data-stu-id="41270-212">Table 4 lists the operating systems on which you can install the versions of AGPM that precede AGPM4.0.</span></span> <span data-ttu-id="41270-213">Если операционная система не указана в списке, вы не можете установить в этой операционной системе РАСШИРЕНную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="41270-213">If an operating system is not listed, you cannot install AGPM on that operating system.</span></span>

**<span data-ttu-id="41270-214">Таблица 5: Поддерживаемые операционные системы для версий с расширенным управлением групповыми политиками, предшествующих РАСШИРЕНному набору</span><span class="sxs-lookup"><span data-stu-id="41270-214">Table 5: Supported operating systems for versions of AGPM that precede AGPM4.0</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="41270-215">Операционная система</span><span class="sxs-lookup"><span data-stu-id="41270-215">Operating system</span></span></th>
<th align="left"><span data-ttu-id="41270-216">Версия расширенного управления групповыми политиками, которая может быть установлена</span><span class="sxs-lookup"><span data-stu-id="41270-216">Version of AGPM that can be installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-217">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="41270-217">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-218">3,0</span><span class="sxs-lookup"><span data-stu-id="41270-218">3.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41270-219">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="41270-219">Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-220">3,0</span><span class="sxs-lookup"><span data-stu-id="41270-220">3.0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41270-221">WindowsVista без установленного пакета обновления (32-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="41270-221">WindowsVista with no service pack installed (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-222">2,5</span><span class="sxs-lookup"><span data-stu-id="41270-222">2.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41270-223">Windows server2003 (32-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="41270-223">Windows Server2003 (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="41270-224">2,5</span><span class="sxs-lookup"><span data-stu-id="41270-224">2.5</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="41270-225">Получение технологий для MDOP</span><span class="sxs-lookup"><span data-stu-id="41270-225">How to Get MDOP Technologies</span></span>


<span data-ttu-id="41270-226">Компонент РАСШИРЕНной оптимизации для настольных систем (MDOP) 4,0 входит в состав пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="41270-226">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="41270-227">MDOP входит в состав Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="41270-227">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="41270-228">Дополнительные сведения о программе Software Assurance и приобретении MDOP можно найти в [статьях получение MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="41270-228">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="41270-229">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="41270-229">Related topics</span></span>


[<span data-ttu-id="41270-230">Расширенное управление групповыми политиками (AGPM)</span><span class="sxs-lookup"><span data-stu-id="41270-230">Advanced Group Policy Management</span></span>](index.md)

 

 





