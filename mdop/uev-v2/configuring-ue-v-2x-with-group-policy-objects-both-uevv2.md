---
title: Настройка объектов групповой политики UE-V 2.x
description: Настройка объектов групповой политики UE-V 2.x
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6c9636df36a53cbf65bf1904965f2809484b99c
ms.sourcegitcommit: bdc377477a8cc9e973fbcdd67c2f07b882c5d61e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "11494064"
---
# <a name="configuring-ue-v-2x-with-group-policy-objects"></a><span data-ttu-id="f4de6-103">Настройка объектов групповой политики UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="f4de6-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="f4de6-104">Для компьютеров можно определить некоторые параметры групповой политики для пользователей Microsoft Experience (UE-V) 2.0, 2.1 и 2.1 SP1 Group Policy, а для пользователей — другие параметры групповой политики.</span><span class="sxs-lookup"><span data-stu-id="f4de6-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="f4de6-105">Сведения об установке файлов групповой политики UE-V ADMX см. в материалах Установки шаблонов групповой политики [ADMX UE-V 2.](https://technet.microsoft.com/library/dn458891.aspx#admx)</span><span class="sxs-lookup"><span data-stu-id="f4de6-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="f4de6-106">Следующие параметры политики можно настроить для UE-V.</span><span class="sxs-lookup"><span data-stu-id="f4de6-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="f4de6-107">Параметры групповой политики</span><span class="sxs-lookup"><span data-stu-id="f4de6-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4de6-108">Имя параметра групповой политики</span><span class="sxs-lookup"><span data-stu-id="f4de6-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="f4de6-109">Target</span><span class="sxs-lookup"><span data-stu-id="f4de6-109">Target</span></span></th>
<th align="left"><span data-ttu-id="f4de6-110">Описание параметра групповой политики</span><span class="sxs-lookup"><span data-stu-id="f4de6-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="f4de6-111">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="f4de6-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4de6-112">Настройка метода синхронизации</span><span class="sxs-lookup"><span data-stu-id="f4de6-112">Configure Sync Method</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-113">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="f4de6-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-114">С помощью этого параметра групповой политики можно настроить использование функции поставщика синхронизации виртуализации пользовательского опыта (UE-V).</span><span class="sxs-lookup"><span data-stu-id="f4de6-114">By using this Group Policy setting, you can configure whether User Experience Virtualization (UE-V) uses the sync provider feature.</span></span> <span data-ttu-id="f4de6-115">Этот параметр политики также позволяет включить уведомление при задержке импорта параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="f4de6-115">This policy setting also lets you enable a notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-116">Включить этот параметр, чтобы настроить агент UE-V не использовать поставщика синхронизации или использовать внешний движок синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f4de6-116">Enable this setting to configure the UE-V agent not to use the sync provider, or to use the external synchronization engine.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4de6-117">Свяжитесь с текстом ссылки на ИТ</span><span class="sxs-lookup"><span data-stu-id="f4de6-117">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-118">Только компьютеры</span><span class="sxs-lookup"><span data-stu-id="f4de6-118">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-119">Этот параметр групповой политики указывает текст гиперссылки URL-адреса контактов в Центре параметров компании.</span><span class="sxs-lookup"><span data-stu-id="f4de6-119">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-120">Если включить этот параметр групповой политики, Центр параметров компании отображает указанный текст в ссылке на URL-адрес контактной группы.</span><span class="sxs-lookup"><span data-stu-id="f4de6-120">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4de6-121">Свяжитесь с ИТ-АДРЕСом</span><span class="sxs-lookup"><span data-stu-id="f4de6-121">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-122">Только компьютеры</span><span class="sxs-lookup"><span data-stu-id="f4de6-122">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-123">В этом параметре групповой политики указывается URL-адрес контактной ИТ-ссылки в Центре параметров компании.</span><span class="sxs-lookup"><span data-stu-id="f4de6-123">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-124">Если включить этот параметр, центр параметров компании связывается с ИТ-текстовыми ссылками на указанный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f4de6-124">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="f4de6-125">Ссылка может быть любого стандартного протокола, например HTTP или mailto.</span><span class="sxs-lookup"><span data-stu-id="f4de6-125">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4de6-126">Уведомление о первом использовании</span><span class="sxs-lookup"><span data-stu-id="f4de6-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-127">Только компьютеры</span><span class="sxs-lookup"><span data-stu-id="f4de6-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-128">Этот параметр групповой политики включает уведомление в области уведомлений, которая появляется при UE-V</span><span class="sxs-lookup"><span data-stu-id="f4de6-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="f4de6-129">агент запускается впервые.</span><span class="sxs-lookup"><span data-stu-id="f4de6-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-130">Включено значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4de6-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4de6-131">Ping the settings storage location before sync</span><span class="sxs-lookup"><span data-stu-id="f4de6-131">Ping the settings storage location before sync</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-132">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="f4de6-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-133">Этот параметр политики позволяет конфигурации поставщика синхронизации UE-V для ping пути хранения параметров, прежде чем пытаться синхронизировать параметры для проверки подключения.</span><span class="sxs-lookup"><span data-stu-id="f4de6-133">This policy setting allows configuration of the UE-V sync provider to ping the settings storage path before attempting to sync settings in order to verify the connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-134">Включить или отключить этот параметр групповой политики.</span><span class="sxs-lookup"><span data-stu-id="f4de6-134">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4de6-135">Пороговое предупреждение о размере пакета параметров</span><span class="sxs-lookup"><span data-stu-id="f4de6-135">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-136">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="f4de6-136">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-137">Этот параметр групповой политики позволяет настроить агент UE-V для отчета, когда размер файла пакета параметров достигает определенного порогового значения.</span><span class="sxs-lookup"><span data-stu-id="f4de6-137">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-138">Укажите предпочтительный порог для параметров размеров пакета в килобайтах (КБ).</span><span class="sxs-lookup"><span data-stu-id="f4de6-138">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="f4de6-139">По умолчанию агент UE-V не имеет порогового значения размера файла пакета.</span><span class="sxs-lookup"><span data-stu-id="f4de6-139">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4de6-140">Путь хранения параметров</span><span class="sxs-lookup"><span data-stu-id="f4de6-140">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-141">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="f4de6-141">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-142">Этот параметр групповой политики настраивает место хранения параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="f4de6-142">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-143">Введите путь и переменные, такие как \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="f4de6-143">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4de6-144">Путь каталога шаблонов параметров</span><span class="sxs-lookup"><span data-stu-id="f4de6-144">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-145">Только компьютеры</span><span class="sxs-lookup"><span data-stu-id="f4de6-145">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-146">Этот параметр групповой политики настраивает места хранения шаблонов расположения настраиваемых параметров.</span><span class="sxs-lookup"><span data-stu-id="f4de6-146">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="f4de6-147">Этот параметр политики также настраивает, следует ли использовать каталог для замены шаблонов Microsoft по умолчанию, установленных агентом UE-V.</span><span class="sxs-lookup"><span data-stu-id="f4de6-147">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-148">Введите путь универсальной конвенции имен (UNC), например \Server\TemplateShare или расположение папки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f4de6-148">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="f4de6-149">Выберите поле для замены шаблонов Microsoft по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4de6-149">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4de6-150">Синхронизация параметров по счетчикам подключений</span><span class="sxs-lookup"><span data-stu-id="f4de6-150">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-151">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="f4de6-151">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-152">Этот параметр групповой политики определяет, синхронизирует ли UE-V параметры с дозированных подключений.</span><span class="sxs-lookup"><span data-stu-id="f4de6-152">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-153">По умолчанию агент UE-V не синхронизирует параметры с помощью дозированных подключений.</span><span class="sxs-lookup"><span data-stu-id="f4de6-153">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4de6-154">Синхронизация параметров для дозаторных подключений даже при роуминге</span><span class="sxs-lookup"><span data-stu-id="f4de6-154">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-155">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="f4de6-155">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-156">Этот параметр групповой политики определяет, синхронизирует ли UE-V параметры для дозированных подключений за пределами сети домашнего поставщика, например, когда подключение к данным находится в режиме роуминга.</span><span class="sxs-lookup"><span data-stu-id="f4de6-156">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-157">По умолчанию UE-V не синхронизирует параметры с помощью дозированных подключений в режиме роуминга.</span><span class="sxs-lookup"><span data-stu-id="f4de6-157">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4de6-158">Время синхронизации</span><span class="sxs-lookup"><span data-stu-id="f4de6-158">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-159">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="f4de6-159">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-160">Этот параметр групповой политики настраивает количество миллисекунд, которые компьютер ждет перед выходом времени, когда он извлекает параметры пользователя из удаленного расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="f4de6-160">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="f4de6-161">Если удаленное расположение хранилища недоступно, а пользователь не использует поставщика синхронизации, запуск приложения задерживается на этом много миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="f4de6-161">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-162">Укажите предпочтительное время синхронизации в миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="f4de6-162">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="f4de6-163">Значение по умолчанию — 2000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="f4de6-163">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4de6-164">Синхронизация параметров Windows</span><span class="sxs-lookup"><span data-stu-id="f4de6-164">Synchronize Windows settings</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f4de6-165">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="f4de6-165">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-166">Этот параметр групповой политики настраивает синхронизацию параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="f4de6-166">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-167">Выберите, какие параметры Windows синхронизируются между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="f4de6-167">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="f4de6-168">По умолчанию темы Windows, параметры рабочего стола и параметры Простота доступа синхронизируются между компьютерами одной и той же версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f4de6-168">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4de6-169">Значок Tray</span><span class="sxs-lookup"><span data-stu-id="f4de6-169">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-170">Только компьютеры</span><span class="sxs-lookup"><span data-stu-id="f4de6-170">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-171">Этот параметр групповой политики включает значок лотка UE-V.</span><span class="sxs-lookup"><span data-stu-id="f4de6-171">This Group Policy setting enables the UE-V tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-172">Включено значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4de6-172">The default is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4de6-173">Использование виртуализации пользовательских интерфейсов (UE-V)</span><span class="sxs-lookup"><span data-stu-id="f4de6-173">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-174">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="f4de6-174">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-175">Этот параметр групповой политики позволяет включить или отключить UE-V.</span><span class="sxs-lookup"><span data-stu-id="f4de6-175">This Group Policy setting lets you enable or disable UE-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-176">Включить или отключить этот параметр групповой политики.</span><span class="sxs-lookup"><span data-stu-id="f4de6-176">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4de6-177">Конфигурация VDI</span><span class="sxs-lookup"><span data-stu-id="f4de6-177">VDI Configuration</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-178">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="f4de6-178">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-179">Этот параметр политики настраивает синхронизацию данных отката UE-V для компьютеров, работающих в среде VDI с пулом.</span><span class="sxs-lookup"><span data-stu-id="f4de6-179">This policy setting configures the synchronization of UE-V rollback information for computers running in a pooled VDI environment.</span></span> <span data-ttu-id="f4de6-180">Если эта политика включена, состояние отката UE-V копируется в расположение хранилища параметров при входе и восстанавливается при входе в систему.</span><span class="sxs-lookup"><span data-stu-id="f4de6-180">If this policy is enabled, the UE-V rollback state is copied to the settings storage location on logout and restored on login.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-181">Включить или отключить этот параметр групповой политики.</span><span class="sxs-lookup"><span data-stu-id="f4de6-181">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f4de6-182">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f4de6-182">Note</span></span>**  
<span data-ttu-id="f4de6-183">Кроме того, параметры групповой политики доступны для многих настольных приложений и приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="f4de6-183">In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="f4de6-184">Эти параметры можно использовать, чтобы включить или отключить синхронизацию параметров для определенных приложений.</span><span class="sxs-lookup"><span data-stu-id="f4de6-184">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="f4de6-185">Параметры групповой политики Приложения Windows</span><span class="sxs-lookup"><span data-stu-id="f4de6-185">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4de6-186">Имя параметра групповой политики</span><span class="sxs-lookup"><span data-stu-id="f4de6-186">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="f4de6-187">Target</span><span class="sxs-lookup"><span data-stu-id="f4de6-187">Target</span></span></th>
<th align="left"><span data-ttu-id="f4de6-188">Описание параметра групповой политики</span><span class="sxs-lookup"><span data-stu-id="f4de6-188">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="f4de6-189">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="f4de6-189">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4de6-190">Не синхронизируются приложения Windows</span><span class="sxs-lookup"><span data-stu-id="f4de6-190">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-191">Компьютеры и пользователи</span><span class="sxs-lookup"><span data-stu-id="f4de6-191">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-192">Этот параметр групповой политики определяет, синхронизирует ли агент UE-V параметры для приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="f4de6-192">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-193">По умолчанию необходимо синхронизировать приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="f4de6-193">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4de6-194">Список приложений Windows</span><span class="sxs-lookup"><span data-stu-id="f4de6-194">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-195">Компьютер и пользователь</span><span class="sxs-lookup"><span data-stu-id="f4de6-195">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-196">В этом параметре перечислены имена семейных пакетов приложений Windows и прямо сообщается, синхронизирует ли UE-V параметры приложения.</span><span class="sxs-lookup"><span data-stu-id="f4de6-196">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-197">С помощью этого параметра можно указать, что параметры приложения никогда не синхронизируются UE-V, даже если параметры всех других приложений Windows синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="f4de6-197">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4de6-198">Синхронизация незасвеченных приложений Windows</span><span class="sxs-lookup"><span data-stu-id="f4de6-198">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-199">Компьютер и пользователь</span><span class="sxs-lookup"><span data-stu-id="f4de6-199">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-200">Этот параметр групповой политики определяет поведение синхронизации параметров по умолчанию для приложений UE-V для Windows, которые явно не указаны в списке приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="f4de6-200">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4de6-201">Агент UE-V по умолчанию синхронизирует только параметры тех приложений Windows, которые включены в список приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="f4de6-201">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f4de6-202">Дополнительные сведения о синхронизации приложений Windows см. в [списке приложений Windows.](https://technet.microsoft.com/library/dn458925.aspx#win8applist)</span><span class="sxs-lookup"><span data-stu-id="f4de6-202">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="f4de6-203">Настройка параметров групповой политики на компьютере</span><span class="sxs-lookup"><span data-stu-id="f4de6-203">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="f4de6-204">Используйте консоль управления групповой политикой (GPMC) или Advanced Group Policy Management (AGPM) на компьютере, который выступает в качестве контроллера домена для управления настройками групповой политики для компьютеров UE-V.</span><span class="sxs-lookup"><span data-stu-id="f4de6-204">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="f4de6-205">Перейдите **к конфигурации компьютера,** **выберите политики,** выберите **административные**шаблоны, щелкните **компоненты Windows,** а затем выберите виртуализацию **microsoft User Experience**.</span><span class="sxs-lookup"><span data-stu-id="f4de6-205">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="f4de6-206">Выберите параметр групповой политики, который необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="f4de6-206">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="f4de6-207">Настройка параметров групповой политики, нацеленных на пользователя</span><span class="sxs-lookup"><span data-stu-id="f4de6-207">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="f4de6-208">Чтобы управлять настройками групповой политики для UE-V, используйте консоль управления групповой политикой (GPMC) или средство advanced Group Policy Management (AGPM) в Пакете оптимизации рабочего стола Майкрософт (MDOP) на компьютере контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="f4de6-208">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="f4de6-209">Перейдите **к конфигурации пользователя,** **выберите политики,** выберите **административные**шаблоны, щелкните **компоненты Windows,** а затем выберите виртуализацию **microsoft User Experience**.</span><span class="sxs-lookup"><span data-stu-id="f4de6-209">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="f4de6-210">Выберите измененный параметр групповой политики.</span><span class="sxs-lookup"><span data-stu-id="f4de6-210">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="f4de6-211">Агент UE-V использует следующий порядок приоритета для определения синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f4de6-211">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="f4de6-212">Порядок приоритета для ПАРАМЕТРОВ UE-V</span><span class="sxs-lookup"><span data-stu-id="f4de6-212">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="f4de6-213">Настраиваемые пользователем параметры, управляемые настройками групповой политики. Эти параметры конфигурации хранятся в ключе реестра групповой политикой в `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` соответствии с .</span><span class="sxs-lookup"><span data-stu-id="f4de6-213">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="f4de6-214">Настраиваемые на компьютер параметры, управляемые настройками групповой политики. Эти параметры конфигурации хранятся в ключе реестра групповой политикой под `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="f4de6-214">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="f4de6-215">Параметры конфигурации, определенные текущим пользователем с помощью Windows PowerShell или инструментов управления Windows (WMI) — эти параметры конфигурации хранятся агентом UE-V в этом расположении реестра: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="f4de6-215">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="f4de6-216">Параметры конфигурации, определенные для компьютера с помощью Windows PowerShell или WMI.</span><span class="sxs-lookup"><span data-stu-id="f4de6-216">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="f4de6-217">Эти параметры конфигурации хранятся агентом UE-V в этом расположении реестра: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="f4de6-217">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="f4de6-218">**Есть предложение для UE-V?**</span><span class="sxs-lookup"><span data-stu-id="f4de6-218">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="f4de6-219">Добавьте или проголосуйте по [предложениям здесь](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="f4de6-219">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="f4de6-220">**Есть проблема UE-V?**</span><span class="sxs-lookup"><span data-stu-id="f4de6-220">**Got a UE-V issue**?</span></span> <span data-ttu-id="f4de6-221">Используйте [форум UE-V TechNet.](https://social.technet.microsoft.com/Forums/home?forum=mdopuev)</span><span class="sxs-lookup"><span data-stu-id="f4de6-221">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4de6-222">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f4de6-222">Related topics</span></span>


[<span data-ttu-id="f4de6-223">Администрирование UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="f4de6-223">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="f4de6-224">Управление конфигурациями UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="f4de6-224">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 
