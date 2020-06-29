---
title: Синхронизация событий-триггеров для UE-V 2.x
description: Синхронизация событий-триггеров для UE-V 2.x
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826799"
---
# <span data-ttu-id="4e1c9-103">Синхронизация событий-триггеров для UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="4e1c9-103">Sync Trigger Events for UE-V 2.x</span></span>


<span data-ttu-id="4e1c9-104">Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 и 2,1 SP1 позволяет синхронизировать приложение и параметры Windows для всех устройств, подключенных к домену.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 lets you synchronize your application and Windows settings across all your domain-joined devices.</span></span> <span data-ttu-id="4e1c9-105">*События триггеров синхронизации* определяют, когда агент UE-V синхронизирует эти параметры с расположением хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-105">*Sync trigger events* define when the UE-V Agent synchronizes those settings with the settings storage location.</span></span> <span data-ttu-id="4e1c9-106">UE-V 2 представляет новый *метод синхронизации* с именем *SyncProvider*.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-106">UE-V 2 introduces a new *Sync Method* called the *SyncProvider*.</span></span> <span data-ttu-id="4e1c9-107">Дополнительные сведения о конфигурации метода синхронизации см. в разделе [методы синхронизации для UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="4e1c9-107">For more information about Sync Method configuration, see [Sync Methods for UE-V 2.x](sync-methods-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="4e1c9-108">События триггеров синхронизации UE-V 2</span><span class="sxs-lookup"><span data-stu-id="4e1c9-108">UE-V 2 Sync Trigger Events</span></span>


<span data-ttu-id="4e1c9-109">В приведенной ниже таблице описаны события триггеров для классических приложений и параметры Windows.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-109">The following table explains the trigger events for classic applications and Windows settings.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4e1c9-110">Событие триггера UE-V 2</span><span class="sxs-lookup"><span data-stu-id="4e1c9-110">UE-V 2 Trigger Event</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="4e1c9-111">PowerSchool = SyncProvider</span><span class="sxs-lookup"><span data-stu-id="4e1c9-111">SyncMethod=SyncProvider</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="4e1c9-112">PowerSchool = None</span><span class="sxs-lookup"><span data-stu-id="4e1c9-112">SyncMethod=None</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4e1c9-113">Вход в Windows</span><span class="sxs-lookup"><span data-stu-id="4e1c9-113">Windows Logon</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4e1c9-114">Параметры приложений и Windows импортируются в локальный кэш из места хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-114">Application and Windows settings are imported to the local cache from the settings storage location.</span></span></p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)"><span data-ttu-id="4e1c9-115">Применяются асинхронные параметры Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="4e1c9-115">Asynchronous Windows settings</a> are applied.</span></span></p></li>
<li><p><span data-ttu-id="4e1c9-116">Синхронные параметры Windows будут применены при следующем входе в Windows.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-116">Synchronous Windows settings will be applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="4e1c9-117">Параметры приложения будут применены при запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-117">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4e1c9-118">Параметры приложений и Windows считываются непосредственно из места хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-118">Application and Windows settings are read directly from the settings storage location.</span></span></p></li>
<li><p><span data-ttu-id="4e1c9-119">Применяются асинхронные и синхронные параметры Windows.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-119">Asynchronous and synchronous Windows settings are applied.</span></span></p></li>
<li><p><span data-ttu-id="4e1c9-120">Параметры приложения будут применены при запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-120">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4e1c9-121">Выход из Windows</span><span class="sxs-lookup"><span data-stu-id="4e1c9-121">Windows Logoff</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4e1c9-122">Локальное сохранение изменений и кэширование и копирование параметров асинхронных и синхронных файлов Windows на сервер расположений хранилища параметров, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-122">Store changes locally and cache and copy asynchronous and synchronous Windows settings to the settings storage location server, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e1c9-123">Сохранение изменений, внесенных в асинхронные и синхронные места хранения параметров Windows</span><span class="sxs-lookup"><span data-stu-id="4e1c9-123">Store changes to asynchronous and synchronous Windows settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4e1c9-124">Windows Connect (RDP)/разблокировка</span><span class="sxs-lookup"><span data-stu-id="4e1c9-124">Windows Connect (RDP) / Unlock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4e1c9-125">Синхронизация всех асинхронных параметров Windows из хранилища параметров расположение в локальном кэше (если оно доступно).</span><span class="sxs-lookup"><span data-stu-id="4e1c9-125">Synchronize any asynchronous Windows settings from settings storage location to local cache, if available.</span></span></p>
<p><span data-ttu-id="4e1c9-126">Применение кэшированных параметров Windows</span><span class="sxs-lookup"><span data-stu-id="4e1c9-126">Apply cached Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e1c9-127">Скачивание и применение асинхронных параметров Windows из места хранения параметров</span><span class="sxs-lookup"><span data-stu-id="4e1c9-127">Download and apply asynchronous windows settings from settings storage location</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4e1c9-128">Отключение Windows (RDP)/блокировка</span><span class="sxs-lookup"><span data-stu-id="4e1c9-128">Windows Disconnect (RDP) / Lock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4e1c9-129">Сохранение изменений параметров в локальном кэше для асинхронной настройки Windows.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-129">Store asynchronous Windows settings changes to the local cache.</span></span></p>
<p><span data-ttu-id="4e1c9-130">Синхронизация всех асинхронных параметров Windows из локального кэша с расположением хранения параметров, если оно доступно</span><span class="sxs-lookup"><span data-stu-id="4e1c9-130">Synchronize any asynchronous Windows settings from the local cache to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e1c9-131">Сохранение изменений параметров Windows в местоположении хранения параметров</span><span class="sxs-lookup"><span data-stu-id="4e1c9-131">Store asynchronous Windows settings changes to the settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4e1c9-132">Запуск приложения</span><span class="sxs-lookup"><span data-stu-id="4e1c9-132">Application start</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4e1c9-133">Применение параметров приложения из локального кэша при запуске приложения</span><span class="sxs-lookup"><span data-stu-id="4e1c9-133">Apply application settings from local cache as the application starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e1c9-134">Применение параметров приложения из хранилища параметров при запуске приложения</span><span class="sxs-lookup"><span data-stu-id="4e1c9-134">Apply application settings from settings storage location as the application starts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4e1c9-135">Приложение закрывается</span><span class="sxs-lookup"><span data-stu-id="4e1c9-135">Application closes</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4e1c9-136">Сохранение всех параметров приложения в локальном кэше и копирование параметров в место хранения параметров (при наличии)</span><span class="sxs-lookup"><span data-stu-id="4e1c9-136">Store any application settings changes to the local cache and copy settings to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e1c9-137">Сохранить изменения параметров приложения в местоположении хранения параметров</span><span class="sxs-lookup"><span data-stu-id="4e1c9-137">Store any application settings changes to settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4e1c9-138">Запланированная задача контроллера синхронизации или "Синхронизация сейчас" запускается из центра параметров компании</span><span class="sxs-lookup"><span data-stu-id="4e1c9-138">Sync Controller Scheduled Task or “Sync Now” is run from the Company Settings Center</span></span></strong></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="4e1c9-139">Параметры приложений и Windows синхронизируются между местом хранения параметров и локальным кэшем.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-139">Application and Windows settings are synchronized between the settings storage location and the local cache.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4e1c9-140">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-140">Note</span></span></strong><br/><p><span data-ttu-id="4e1c9-141">Изменения параметров не кэшируются локально, пока приложение не закроется.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-141">Settings changes are not cached locally until an application closes.</span></span> <span data-ttu-id="4e1c9-142">Этот триггер не будет экспортировать изменения, внесенные в приложение, которое выполняется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-142">This trigger will not export changes made to a currently running application.</span></span></p>
<p><span data-ttu-id="4e1c9-143">Для параметров Windows это означает, что любые изменения не будут кэшироваться локально и экспортированы до следующей блокировки (асинхронной) или выхода из нее (асинхронный и синхронный).</span><span class="sxs-lookup"><span data-stu-id="4e1c9-143">For Windows settings, this means that any changes will not be cached locally and exported until the next Lock (Asynchronous) or Logoff (Asynchronous and Synchronous).</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="4e1c9-144">Параметры применяются в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="4e1c9-144">Settings are applied in these cases:</span></span></p>
<ul>
<li><p><span data-ttu-id="4e1c9-145">Асинхронные параметры Windows применяются непосредственно.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-145">Asynchronous Windows settings are applied directly.</span></span></p></li>
<li><p><span data-ttu-id="4e1c9-146">Параметры приложения применяются при запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-146">Application settings are applied when the application starts.</span></span></p></li>
<li><p><span data-ttu-id="4e1c9-147">При следующем входе в Windows применяются как асинхронные, так и синхронные параметры Windows.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-147">Both asynchronous and synchronous Windows settings are applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="4e1c9-148">Параметры приложения Windows (AppX) применяются при следующем обновлении.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-148">Windows app (AppX) settings are applied during the next refresh.</span></span> <span data-ttu-id="4e1c9-149"><a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">Дополнительные сведения приведены в разделе мониторинг параметров приложения </a> .</span><span class="sxs-lookup"><span data-stu-id="4e1c9-149">See <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">Monitor Application Settings</a> for more information.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="4e1c9-150">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="4e1c9-150">NA</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4e1c9-151">Асинхронные параметры, обновленные в удаленном магазине \*</span><span class="sxs-lookup"><span data-stu-id="4e1c9-151">Asynchronous Settings updated on remote store\*</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4e1c9-152">Загрузка и применение новых асинхронных параметров из кэша.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-152">Load and apply new asynchronous settings from the cache.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e1c9-153">Загрузка и применение параметров из центрального сервера</span><span class="sxs-lookup"><span data-stu-id="4e1c9-153">Load and apply settings from central server</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="4e1c9-154">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4e1c9-154">Related topics</span></span>


[<span data-ttu-id="4e1c9-155">Технический справочник по UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="4e1c9-155">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

[<span data-ttu-id="4e1c9-156">Изменение частоты выполнения запланированных задач UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="4e1c9-156">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[<span data-ttu-id="4e1c9-157">Выберите метод конфигурации для UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="4e1c9-157">Choose the Configuration Method for UE-V 2.x</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)









