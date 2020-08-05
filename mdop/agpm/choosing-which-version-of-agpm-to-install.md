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
ms.openlocfilehash: f8a69fb323d9f47c5b906ac3abc6ec59376ee6f7
ms.sourcegitcommit: 0a7dee11289780336d9c24ebbf27c5c1ffee441c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/04/2020
ms.locfileid: "10905606"
---
# <span data-ttu-id="36083-103">Выбор версии AGPM для установки</span><span class="sxs-lookup"><span data-stu-id="36083-103">Choosing Which Version of AGPM to Install</span></span>


<span data-ttu-id="36083-104">Каждый выпуск управления групповыми политиками MicrosoftAdvanced поддерживает определенные версии операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="36083-104">Each release of MicrosoftAdvanced Group Policy Management (AGPM) supports specific versions of the Windows operating system.</span></span> <span data-ttu-id="36083-105">Мы настоятельно рекомендуем использовать клиент и сервер РАСШИРЕНного использования РАСШИРЕНного взаимодействия в той же строке операционной системы.</span><span class="sxs-lookup"><span data-stu-id="36083-105">We strongly recommend that you run the AGPM Client and AGPM Server on the same line of operating systems.</span></span> <span data-ttu-id="36083-106">Например, Windows 10 с Windows Server 2016, Windows 8.1 и Windows Server2012 R2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="36083-106">For example, Windows 10 with Windows Server 2016, Windows8.1 with Windows Server2012 R2, and so on.</span></span>

<span data-ttu-id="36083-107">Рекомендуем установить сервер расширенного управления групповыми политиками в новейшей версии операционной системы домена.</span><span class="sxs-lookup"><span data-stu-id="36083-107">We recommend that you install the AGPM Server on the most recent version of the operating system in the domain.</span></span> <span data-ttu-id="36083-108">С помощью консоли управления групповыми политиками (GPMC) можно архивировать и восстанавливать объекты групповой политики (GPO).</span><span class="sxs-lookup"><span data-stu-id="36083-108">AGPM uses the Group Policy Management Console (GPMC) to back up and restore Group Policy Objects (GPOs).</span></span> <span data-ttu-id="36083-109">Поскольку новые версии GPMC предоставляют дополнительные параметры политики, недоступные в более ранних версиях, вы можете управлять дополнительными параметрами политики, используя самую последнюю версию операционной системы.</span><span class="sxs-lookup"><span data-stu-id="36083-109">Because newer versions of the GPMC provide additional policy settings that are not available in earlier versions, you can manage more policy settings by using the most recent version of the operating system.</span></span>

<span data-ttu-id="36083-110">Все версии расширенного управления групповыми политиками могут управлять только параметрами политики, которые были введены в той же или более ранней версии операционной системы, в которой работает служба управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="36083-110">All versions of AGPM can manage only the policy settings that were introduced in the same version or an earlier version of the operating system on which AGPM is running.</span></span> <span data-ttu-id="36083-111">Например, если установить пакет обновления 2 (SP2) для Windows Server 2012, вы можете управлять параметрами политики, которые были введены в Windows Server 2012 или более ранней версии, но вы не можете управлять параметрами политики, которые появились позже в Windows 8.1 или Windows Server2012 R2.</span><span class="sxs-lookup"><span data-stu-id="36083-111">For example, if you install AGPM4.0 SP2 on Windows Server 2012, you can manage policy settings that were introduced in Windows Server 2012 or earlier, but you cannot manage policy settings that were introduced later, in Windows8.1 or Windows Server2012 R2.</span></span>

<span data-ttu-id="36083-112">Если версия GPMC на сервере управления ГРУППОВыми политиками старше, чем версия на компьютерах, используемых администраторами для управления групповой политикой, сервер управления ГРУППОВыми политиками не сможет хранить параметры политики, недоступные в более ранней версии GPMC.</span><span class="sxs-lookup"><span data-stu-id="36083-112">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store any policy settings that are not available in the older version of the GPMC.</span></span> <span data-ttu-id="36083-113">Таблицу параметров групповой политики, включенных в Windows, см. в [Справочнике по параметрам групповой политики Windows и Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span><span class="sxs-lookup"><span data-stu-id="36083-113">For a spreadsheet of Group Policy settings included in Windows, see [Group Policy Settings Reference for Windows and Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span></span>

## <span data-ttu-id="36083-114">РАСШИРЕННАЯ ВЕРСИЯ ДЛЯ ВЕРСИИ 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="36083-114">AGPM4.0 SP3</span></span>


<span data-ttu-id="36083-115">Если вы используете на компьютерах под управлением Windows 10 Управление объектами групповой политики, необходимо использовать параметр РАСШИРЕНного обновления для 4,0.</span><span class="sxs-lookup"><span data-stu-id="36083-115">If you are using computers that are running Windows 10 to manage GPOs, you must use AGPM 4.0 SP3.</span></span> <span data-ttu-id="36083-116">На компьютерах под управлением операционной системы Windows 10 невозможно установить более раннюю версию РАСШИРЕНного использования службы.</span><span class="sxs-lookup"><span data-stu-id="36083-116">You cannot install earlier versions of AGPM on computers that are running the Windows 10 operating system.</span></span>

<span data-ttu-id="36083-117">В таблице 1 перечислены операционные системы, для которых вы можете установить пакет управления групповыми политиками версии 4.0 SP3, и параметры политики, которые можно управлять с помощью расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="36083-117">Table 1 lists the operating systems on which you can install AGPM4.0 SP3, and the policy settings that you can manage by using AGPM4.0 SP3.</span></span>

**<span data-ttu-id="36083-118">Таблица 1: РАСШИРЕНная поддержка операционных систем и параметров политики в конфигурации со всеми 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="36083-118">Table 1: AGPM 4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="36083-119">Поддерживаемые конфигурации для сервера РАСШИРЕНного языка</span><span class="sxs-lookup"><span data-stu-id="36083-119">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="36083-120">Поддерживаемые конфигурации для клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="36083-120">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="36083-121">Поддержка РАСШИРЕНных возможностей</span><span class="sxs-lookup"><span data-stu-id="36083-121">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-122">Windows Server 2019 или Windows 10</span><span class="sxs-lookup"><span data-stu-id="36083-122">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-123">Windows Server 2019 или Windows 10</span><span class="sxs-lookup"><span data-stu-id="36083-123">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-124">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="36083-124">Supported</span></span></p></td>
</tr>
 <tr class="even">
<td align="left"><p><span data-ttu-id="36083-125">Windows Server 2019 или Windows 10</span><span class="sxs-lookup"><span data-stu-id="36083-125">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-126">Windows Server 2019 или Windows 10</span><span class="sxs-lookup"><span data-stu-id="36083-126">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="36083-127">Supported</span></span></p></td>
</tr>
<tr class="edd">
<td align="left"><p><span data-ttu-id="36083-128">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="36083-128">Windows Server2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-129">Windows 10;</span><span class="sxs-lookup"><span data-stu-id="36083-129">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-130">Поддерживается с помощью предостережений, описанных в <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> статьях KB 4015786</span><span class="sxs-lookup"><span data-stu-id="36083-130">Supported with the caveats outlined in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)">KB 4015786</span></span></a>
</p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36083-131">Windows Server2012 R2 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="36083-131">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-132">Windows Server2012 R2 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="36083-132">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="36083-133">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-134">Windows Server2012 R2, Windows Server 2012 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="36083-134">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-135">Windows Server 2012 или Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="36083-135">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-136">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="36083-136">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36083-137">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-137">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-138">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-138">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-139">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="36083-139">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-140">Windows Server 2012, Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-140">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-141">Windows Server2008 или WindowsVista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-141">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-142">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-142">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36083-143">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-143">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-144">Windows Server 2012, Windows Server2008R2, Windows 8 и Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-144">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-145">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="36083-145">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-146">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-146">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-147">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-147">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-148">Поддерживается, но не может сообщить или изменить параметры политики или элементы предпочтений, существующие только в Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-148">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="36083-149">РАСШИРЕННОЕ ОБНОВЛЕНИЕ ДЛЯ ВЕРСИИ 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="36083-149">AGPM4.0 SP2</span></span>


<span data-ttu-id="36083-150">Если вы используете компьютеры с операционной системой Windows Server2012 R2 или Windows 8.1 для управления объектами групповой политики, необходимо использовать многодоменные версии 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="36083-150">If you are using computers that are running Windows Server2012 R2 or Windows8.1 to manage GPOs, you must use AGPM4.0 SP2.</span></span> <span data-ttu-id="36083-151">Вы не можете установить более ранние версии РАСШИРЕНного использования службы на компьютерах под управлением этих операционных систем.</span><span class="sxs-lookup"><span data-stu-id="36083-151">You cannot install earlier versions of AGPM on computers that are running those operating systems.</span></span>

<span data-ttu-id="36083-152">В таблице 1 перечислены операционные системы, для которых можно установить пакет управления групповыми политиками и параметры политики, которые можно управлять с помощью РАСШИРЕНного обновления для версии 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="36083-152">Table 1 lists the operating systems on which you can install AGPM4.0 SP2, and the policy settings that you can manage by using AGPM4.0 SP2.</span></span>

**<span data-ttu-id="36083-153">Таблица 2. Поддерживаемые операционные системы и параметры политики для РАСШИРЕНной версии 4.0 с пакетом обновления</span><span class="sxs-lookup"><span data-stu-id="36083-153">Table 2: AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="36083-154">Поддерживаемые конфигурации для сервера РАСШИРЕНного языка</span><span class="sxs-lookup"><span data-stu-id="36083-154">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="36083-155">Поддерживаемые конфигурации для клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="36083-155">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="36083-156">Поддержка РАСШИРЕНных возможностей</span><span class="sxs-lookup"><span data-stu-id="36083-156">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-157">Windows Server2012 R2 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="36083-157">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-158">Windows Server2012 R2 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="36083-158">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-159">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="36083-159">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36083-160">Windows Server2012 R2, Windows Server 2012 или Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="36083-160">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-161">Windows Server 2012 или Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="36083-161">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-162">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="36083-162">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-163">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-163">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-164">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-164">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-165">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="36083-165">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36083-166">Windows Server 2012, Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-166">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-167">Windows Server2008 или WindowsVista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-167">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-168">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-168">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-169">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-169">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-170">Windows Server 2012, Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-170">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-171">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="36083-171">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36083-172">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-172">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-173">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-173">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-174">Поддерживается, но не может сообщить или изменить параметры политики или элементы предпочтений, существующие только в Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-174">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="36083-175">РАСШИРЕННАЯ ВЕРСИЯ ДЛЯ NT 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="36083-175">AGPM4.0 SP1</span></span>


<span data-ttu-id="36083-176">В таблице 2 перечислены операционные системы, для которых можно установить 4,0 РАСШИРЕНную настройку конфигурации с пакетом обновления 1 (SP1), а также параметры политики, которые можно управлять с помощью РАСШИРЕНного пакета администрирования.</span><span class="sxs-lookup"><span data-stu-id="36083-176">Table 2 lists the operating systems on which you can install AGPM 4.0 SP1, and the policy settings that you can manage by using AGPM4.0 SP1.</span></span>

**<span data-ttu-id="36083-177">Таблица 3: РАСШИРЕНная поддержка операционных систем и параметров политики в версии 4.0 с пакетом обновления (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-177">Table 3: AGPM4.0 SP1 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="36083-178">Поддерживаемые конфигурации для сервера РАСШИРЕНного языка</span><span class="sxs-lookup"><span data-stu-id="36083-178">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="36083-179">Поддерживаемые конфигурации для клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="36083-179">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="36083-180">Поддержка РАСШИРЕНных возможностей</span><span class="sxs-lookup"><span data-stu-id="36083-180">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36083-181">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-182">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36083-182">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-183">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="36083-183">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36083-184">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-184">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-185">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-185">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-186">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="36083-186">Supported, but cannot edit policy settings or preference items that exist only in Windows 8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-187">Windows Server 2012, Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-187">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-188">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-188">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-189">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-189">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36083-190">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-191">Windows Server 2012, Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-191">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-192">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="36083-192">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-193">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-193">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-194">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-194">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-195">Поддерживается, но не может сообщать или изменять параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-195">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="36083-196">РАСШИРЕНная версия для версии 4.0</span><span class="sxs-lookup"><span data-stu-id="36083-196">AGPM4.0</span></span>


<span data-ttu-id="36083-197">В таблице 3 перечислены операционные системы, для которых можно установить параметры расширенного управления групповыми политиками 4,0, а также настройки политики, которые можно управлять с помощью служб управления ГРУППОВыми политиками.</span><span class="sxs-lookup"><span data-stu-id="36083-197">Table 3 lists the operating systems on which you can install AGPM 4.0, and the policy settings that you can manage by using AGPM4.0.</span></span>

**<span data-ttu-id="36083-198">Таблица 4: Поддерживаемые операционные системы и параметры политики для РАСШИРЕНной версии 4.0</span><span class="sxs-lookup"><span data-stu-id="36083-198">Table 4: AGPM4.0 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="36083-199">Поддерживаемые операционные системы для сервера РАСШИРЕНного языка</span><span class="sxs-lookup"><span data-stu-id="36083-199">Supported operating systems for the AGPM Server</span></span></th>
<th align="left"><span data-ttu-id="36083-200">Поддерживаемые операционные системы для клиента с расширенным управлением групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="36083-200">Supported operating systems for the AGPM Client</span></span></th>
<th align="left"><span data-ttu-id="36083-201">Поддержка РАСШИРЕНных возможностей</span><span class="sxs-lookup"><span data-stu-id="36083-201">AGPM Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-202">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-202">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-203">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-203">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-204">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="36083-204">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36083-205">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-205">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-206">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-206">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-207">Поддерживается, но не может изменить параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-207">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-208">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-208">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-209">Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-209">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-210">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="36083-210">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36083-211">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-211">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-212">Windows Server2008 или Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-212">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-213">Поддерживается, но не может сообщать или изменять параметры политики или элементы предпочтений, существующие только в Windows Server2008R2 или Windows7</span><span class="sxs-lookup"><span data-stu-id="36083-213">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="36083-214">Версии РАСШИРЕНного типа данных, предшествующих РАСШИРЕНному (для версии 4.0)</span><span class="sxs-lookup"><span data-stu-id="36083-214">Versions of AGPM that precede AGPM4.0</span></span>


<span data-ttu-id="36083-215">В таблице 4 перечислены операционные системы, для которых вы можете установить версии РАСШИРЕНного типа, предшествующие РАСШИРЕНию для версии 4.0.</span><span class="sxs-lookup"><span data-stu-id="36083-215">Table 4 lists the operating systems on which you can install the versions of AGPM that precede AGPM4.0.</span></span> <span data-ttu-id="36083-216">Если операционная система не указана в списке, вы не можете установить в этой операционной системе РАСШИРЕНную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="36083-216">If an operating system is not listed, you cannot install AGPM on that operating system.</span></span>

**<span data-ttu-id="36083-217">Таблица 5: Поддерживаемые операционные системы для версий с расширенным управлением групповыми политиками, предшествующих РАСШИРЕНному набору</span><span class="sxs-lookup"><span data-stu-id="36083-217">Table 5: Supported operating systems for versions of AGPM that precede AGPM4.0</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="36083-218">Операционная система</span><span class="sxs-lookup"><span data-stu-id="36083-218">Operating system</span></span></th>
<th align="left"><span data-ttu-id="36083-219">Версия расширенного управления групповыми политиками, которая может быть установлена</span><span class="sxs-lookup"><span data-stu-id="36083-219">Version of AGPM that can be installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-220">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="36083-220">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-221">3,0</span><span class="sxs-lookup"><span data-stu-id="36083-221">3.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36083-222">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="36083-222">Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-223">3,0</span><span class="sxs-lookup"><span data-stu-id="36083-223">3.0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36083-224">WindowsVista без установленного пакета обновления (32-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="36083-224">WindowsVista with no service pack installed (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-225">2,5</span><span class="sxs-lookup"><span data-stu-id="36083-225">2.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36083-226">Windows server2003 (32-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="36083-226">Windows Server2003 (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="36083-227">2,5</span><span class="sxs-lookup"><span data-stu-id="36083-227">2.5</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="36083-228">Получение технологий для MDOP</span><span class="sxs-lookup"><span data-stu-id="36083-228">How to Get MDOP Technologies</span></span>


<span data-ttu-id="36083-229">Компонент РАСШИРЕНной оптимизации для настольных систем (MDOP) 4,0 входит в состав пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="36083-229">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="36083-230">MDOP входит в состав Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="36083-230">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="36083-231">Дополнительные сведения о программе Software Assurance и приобретении MDOP можно найти в [статьях получение MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="36083-231">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="36083-232">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="36083-232">Related topics</span></span>


[<span data-ttu-id="36083-233">Расширенное управление групповыми политиками (AGPM)</span><span class="sxs-lookup"><span data-stu-id="36083-233">Advanced Group Policy Management</span></span>](index.md)

 

 





