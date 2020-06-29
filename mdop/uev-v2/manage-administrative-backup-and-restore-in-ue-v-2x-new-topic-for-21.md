---
title: Управление административными резервными копиями и восстановлением в UE-V 2. x
description: Управление административными резервными копиями и восстановлением в UE-V 2. x
author: dansimp
ms.assetid: 2eb5ae75-65e5-4afc-adb6-4e83cf4364ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11c168b54b71731c51417b2b7c4737c85f42035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827389"
---
# <span data-ttu-id="32ca0-103">Управление административными резервными копиями и восстановлением в UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="32ca0-103">Manage Administrative Backup and Restore in UE-V 2.x</span></span>


<span data-ttu-id="32ca0-104">Как администратор Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 или 2,1 SP1, вы можете восстановить исходное состояние приложений и параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="32ca0-104">As an administrator of Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1, you can restore application and Windows settings to their original state.</span></span> <span data-ttu-id="32ca0-105">Кроме того, в UE-V 2,1 можно также восстанавливать дополнительные параметры, когда пользователь применяет новое устройство.</span><span class="sxs-lookup"><span data-stu-id="32ca0-105">And new in UE-V 2.1, you can also restore additional settings when a user adopts a new device.</span></span>

## <span data-ttu-id="32ca0-106">Параметры восстановления в UE-V 2,1 или UE-V 2,1 SP1, когда пользователь применяет новое устройство</span><span class="sxs-lookup"><span data-stu-id="32ca0-106">Restore Settings in UE-V 2.1 or UE-V 2.1 SP1 when a User Adopts a New Device</span></span>


<span data-ttu-id="32ca0-107">Чтобы восстановить параметры, когда пользователь применяет новое устройство, вы можете добавить шаблон расположения параметров в профиль **резервного копирования** или **перемещения (по умолчанию)** с помощью командлета PowerShell Set-UevTemplateProfile.</span><span class="sxs-lookup"><span data-stu-id="32ca0-107">To restore settings when a user adopts a new device, you can put a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="32ca0-108">Это позволит синхронизировать параметры компьютера с новым компьютером в дополнение к параметрам пользователя.</span><span class="sxs-lookup"><span data-stu-id="32ca0-108">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="32ca0-109">Шаблоны, назначенные профилю резервного копирования, заархивированы для этого устройства и настроены отдельно для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="32ca0-109">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="32ca0-110">Чтобы выполнить резервное копирование параметров шаблона, используйте в Windows PowerShell следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="32ca0-110">To backup settings for a template, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Set-UevTemplateProfile -ID <TemplateID> -Profile <backup>
```

-   <span data-ttu-id="32ca0-111">&lt;TemplateID &gt; является идентификатором шаблона UE-V</span><span class="sxs-lookup"><span data-stu-id="32ca0-111">&lt;TemplateID&gt; is the UE-V Template ID</span></span>

-   <span data-ttu-id="32ca0-112">&lt;Резервное копирование &gt; может быть как резервным, так и перемещаемым</span><span class="sxs-lookup"><span data-stu-id="32ca0-112">&lt;backup&gt; can either be Backup or Roaming</span></span>

<span data-ttu-id="32ca0-113">При замене устройства пользователя UE-V автоматически восстанавливает параметры, если домен пользователя, имя пользователя и имя устройства совпадают.</span><span class="sxs-lookup"><span data-stu-id="32ca0-113">When replacing a user’s device UE-V automatically restores settings if the user’s domain, username, and device name all match.</span></span> <span data-ttu-id="32ca0-114">Все синхронизированные данные и резервные копии будут восстановлены на устройстве автоматически.</span><span class="sxs-lookup"><span data-stu-id="32ca0-114">All synchronized and any backup data is restored on the device automatically.</span></span>

<span data-ttu-id="32ca0-115">Вы также можете использовать новый командлет PowerShell Restore-UevBackup для восстановления параметров с другого устройства.</span><span class="sxs-lookup"><span data-stu-id="32ca0-115">You can also use the new PowerShell cmdlet, Restore-UevBackup, to restore settings from a different device.</span></span> <span data-ttu-id="32ca0-116">Чтобы клонировать пакеты параметров для нового устройства, используйте в Windows PowerShell следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="32ca0-116">To clone the settings packages for the new device, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Restore-UevBackup –Machine <MachineName>
```

<span data-ttu-id="32ca0-117">где &lt; MachineName &gt; — это имя компьютера устройства.</span><span class="sxs-lookup"><span data-stu-id="32ca0-117">where &lt;MachineName&gt; is the computer name of the device.</span></span>

<span data-ttu-id="32ca0-118">Шаблоны, например шаблон Office 2013, включающий множество приложений, могут быть включены в перемещаемый профиль (по умолчанию) или в резервную копию.</span><span class="sxs-lookup"><span data-stu-id="32ca0-118">Templates such as the Office 2013 template that include many applications can either all be included in the roamed (default) or backed up profile.</span></span> <span data-ttu-id="32ca0-119">Отдельные приложения в наборе шаблонов следуют группе.</span><span class="sxs-lookup"><span data-stu-id="32ca0-119">Individual apps in a template suite follow the group.</span></span> <span data-ttu-id="32ca0-120">Шаблоны из встроенных в Office 2013 включают как перемещаемые, так и параметры, заданные только для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="32ca0-120">Office 2013 in-box templates include both roaming and backup-only settings.</span></span> <span data-ttu-id="32ca0-121">В перемещаемый профиль нельзя включать параметры, заданные только для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="32ca0-121">Backup-only settings cannot be included in a roaming profile.</span></span>

<span data-ttu-id="32ca0-122">В рамках функции резервного копирования и восстановления UE-V добавил **последнюю известную подходящее (LKG)** к параметрам для возврата к параметрам.</span><span class="sxs-lookup"><span data-stu-id="32ca0-122">As part of the Backup/Restore feature, UE-V added **last known good (LKG)** to the options for rolling back to settings.</span></span> <span data-ttu-id="32ca0-123">В этом выпуске вы можете вернуться к исходным параметрам или параметрам LKG.</span><span class="sxs-lookup"><span data-stu-id="32ca0-123">In this release, you can roll back to either the original settings or LKG settings.</span></span> <span data-ttu-id="32ca0-124">Параметры LKG позволяют пользователям возвращаться к промежуточной и стабильной точке после состояния предварительно UE-V параметров.</span><span class="sxs-lookup"><span data-stu-id="32ca0-124">The LKG settings let users roll back to an intermediate and stable point ahead of the pre-UE-V state of the settings.</span></span>

### <span data-ttu-id="32ca0-125">Резервное копирование и восстановление шаблонов с помощью UE-V</span><span class="sxs-lookup"><span data-stu-id="32ca0-125">How to Backup/Restore Templates with UE-V</span></span>

<span data-ttu-id="32ca0-126">Ниже указаны ключевые компоненты резервного копирования и восстановления UE-V:</span><span class="sxs-lookup"><span data-stu-id="32ca0-126">These are the key backup and restore components of UE-V:</span></span>

-   <span data-ttu-id="32ca0-127">Профили шаблонов</span><span class="sxs-lookup"><span data-stu-id="32ca0-127">Template profiles</span></span>

-   <span data-ttu-id="32ca0-128">Расположение пакетов параметров в шаблоне места хранения параметров</span><span class="sxs-lookup"><span data-stu-id="32ca0-128">Settings packages location within the Settings Storage Location template</span></span>

-   <span data-ttu-id="32ca0-129">Триггер резервного копирования</span><span class="sxs-lookup"><span data-stu-id="32ca0-129">Backup trigger</span></span>

-   <span data-ttu-id="32ca0-130">Восстановление параметров</span><span class="sxs-lookup"><span data-stu-id="32ca0-130">How settings are restored</span></span>

**<span data-ttu-id="32ca0-131">Профили шаблонов</span><span class="sxs-lookup"><span data-stu-id="32ca0-131">Template Profiles</span></span>**

<span data-ttu-id="32ca0-132">Профиль шаблона UE-V определяется при регистрации шаблона на устройстве или после регистрации с помощью служебной программы настройки PowerShell или WMI.</span><span class="sxs-lookup"><span data-stu-id="32ca0-132">A UE-V template profile is defined when the template is registered on the device or post registration through the PowerShell/WMI configuration utility.</span></span> <span data-ttu-id="32ca0-133">Ниже перечислены типы профилей.</span><span class="sxs-lookup"><span data-stu-id="32ca0-133">The profile types include:</span></span>

-   <span data-ttu-id="32ca0-134">Роуминг (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32ca0-134">Roaming (default)</span></span>

-   <span data-ttu-id="32ca0-135">Архивация</span><span class="sxs-lookup"><span data-stu-id="32ca0-135">Backup</span></span>

-   <span data-ttu-id="32ca0-136">На начальном выходе</span><span class="sxs-lookup"><span data-stu-id="32ca0-136">BackupOnly</span></span>

<span data-ttu-id="32ca0-137">Все шаблоны включаются в перемещаемый профиль при их регистрации, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="32ca0-137">All templates are included in the roaming profile when registered unless otherwise specified.</span></span> <span data-ttu-id="32ca0-138">Эти шаблоны синхронизируют параметры для всех устройств с поддержкой UE-V, для которых включен соответствующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="32ca0-138">These templates synchronize settings to all UE-V enabled devices with the corresponding template enabled.</span></span>

<span data-ttu-id="32ca0-139">Шаблоны можно добавить в профиль резервного копирования с помощью PowerShell или WMI, используя командлет Set-UevTemplateProfile.</span><span class="sxs-lookup"><span data-stu-id="32ca0-139">Templates can be added to the Backup Profile with PowerShell or WMI using the Set-UevTemplateProfile cmdlet.</span></span> <span data-ttu-id="32ca0-140">Шаблоны в резервной копии профиля. Создайте резервные копии этих параметров в хранилище параметров в специальном каталоге имени устройства.</span><span class="sxs-lookup"><span data-stu-id="32ca0-140">Templates in the Backup Profile back up these settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="32ca0-141">Указанные параметры заархивированы в указанном месте.</span><span class="sxs-lookup"><span data-stu-id="32ca0-141">Specified settings are backed up to this location.</span></span>

<span data-ttu-id="32ca0-142">Шаблоны, помеченные как ненужные, включают в себя параметры, специфичные для этого устройства, которые не следует синхронизировать, пока не будет явно восстановлен.</span><span class="sxs-lookup"><span data-stu-id="32ca0-142">Templates designated BackupOnly include settings specific to that device that should not be synchronized unless explicitly restored.</span></span> <span data-ttu-id="32ca0-143">Эти параметры хранятся в том же расположении пакета параметров для определенного устройства в местоположении хранения параметров в качестве параметров backedup.</span><span class="sxs-lookup"><span data-stu-id="32ca0-143">These settings are stored in the same device-specific settings package location on the settings storage location as the Backedup Settings.</span></span> <span data-ttu-id="32ca0-144">Эти шаблоны содержат специальный идентификатор, внедренный в шаблон, который указывает, что они должны входить в этот профиль.</span><span class="sxs-lookup"><span data-stu-id="32ca0-144">These templates have a special identifier embedded in the template that specifies they should be part of this profile.</span></span>

**<span data-ttu-id="32ca0-145">Расположение пакетов параметров в шаблоне места хранения параметров</span><span class="sxs-lookup"><span data-stu-id="32ca0-145">Settings packages location within the Settings Storage Location template</span></span>**

<span data-ttu-id="32ca0-146">Параметры перемещаемого профиля хранятся в местоположении хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="32ca0-146">Roaming Profile settings are stored on the settings storage location.</span></span> <span data-ttu-id="32ca0-147">Шаблоны, назначенные для резервной копии или с помощью параметра "на один из профилей", хранят свои настройки в хранилище параметров в специальном каталоге имен устройств.</span><span class="sxs-lookup"><span data-stu-id="32ca0-147">Templates assigned to the Backup or the BackupOnly profile store their settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="32ca0-148">Каждое устройство с шаблонами в этих профилях имеет собственное имя устройства.</span><span class="sxs-lookup"><span data-stu-id="32ca0-148">Each device with templates in these profiles has its own device name.</span></span> <span data-ttu-id="32ca0-149">UE-V не очищает эти каталоги.</span><span class="sxs-lookup"><span data-stu-id="32ca0-149">UE-V does not clean up these directories.</span></span>

**<span data-ttu-id="32ca0-150">Триггер резервного копирования</span><span class="sxs-lookup"><span data-stu-id="32ca0-150">Backup trigger</span></span>**

<span data-ttu-id="32ca0-151">Резервное копирование инициируется теми же событиями, которые инициируют синхронизацию UE-V.</span><span class="sxs-lookup"><span data-stu-id="32ca0-151">Backup is triggered by the same events that trigger a UE-V synchronization.</span></span>

**<span data-ttu-id="32ca0-152">Восстановление параметров</span><span class="sxs-lookup"><span data-stu-id="32ca0-152">How settings are restored</span></span>**

<span data-ttu-id="32ca0-153">При восстановлении устройства пользователя восстанавливаются параметры зарегистрированного шаблона из папки резервного копирования другого устройства, а также все синхронизированные параметры с текущим компьютером.</span><span class="sxs-lookup"><span data-stu-id="32ca0-153">Restoring a user’s device restores the currently registered Template’s settings from another device’s backup folder and all synchronized settings to the current machine.</span></span> <span data-ttu-id="32ca0-154">Параметры восстанавливаются следующими двумя способами:</span><span class="sxs-lookup"><span data-stu-id="32ca0-154">Settings are restored in these two ways:</span></span>

-   **<span data-ttu-id="32ca0-155">Автоматическое восстановление</span><span class="sxs-lookup"><span data-stu-id="32ca0-155">Automatic restore</span></span>**

    <span data-ttu-id="32ca0-156">Если пользовательский путь к хранилищу параметров UE-V, домен и имя компьютера совпадает с текущим пользователем, все параметры для этого пользователя синхронизируются с применением только последних параметров.</span><span class="sxs-lookup"><span data-stu-id="32ca0-156">If the user’s UE-V settings storage path, domain, and Computer name match the current user then all of the settings for that user are synchronized, with only the latest settings applied.</span></span> <span data-ttu-id="32ca0-157">Если пользователь в первый раз входит в систему на новом устройстве и эти условия выполняются, данные параметров применяются к этому устройству.</span><span class="sxs-lookup"><span data-stu-id="32ca0-157">If a user logs on to a new device for the first time and these criteria are met, the settings data is applied to that device.</span></span>

    **<span data-ttu-id="32ca0-158">Примечание.</span><span class="sxs-lookup"><span data-stu-id="32ca0-158">Note</span></span>**  
    <span data-ttu-id="32ca0-159">Специальные возможности и параметры рабочего стола Windows требуют от пользователя повторного входа в Windows для применения.</span><span class="sxs-lookup"><span data-stu-id="32ca0-159">Accessibility and Windows Desktop settings require the user to re-logon to Windows to be applied.</span></span>



-   **<span data-ttu-id="32ca0-160">Восстановление вручную</span><span class="sxs-lookup"><span data-stu-id="32ca0-160">Manual Restore</span></span>**

    <span data-ttu-id="32ca0-161">Если вы хотите помочь пользователям с помощью восстановления устройства во время обновления, вы можете выбрать командлет Restore-UevBackup.</span><span class="sxs-lookup"><span data-stu-id="32ca0-161">If you want to assist users by restoring a device during a refresh, you can choose to use the Restore-UevBackup cmdlet.</span></span> <span data-ttu-id="32ca0-162">Эта команда приводит к тому, что параметры пользователя загружаются из места хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="32ca0-162">This command causes the user’s settings to be downloaded from the Settings Storage Location.</span></span>

## <span data-ttu-id="32ca0-163">Восстановление параметров приложения и Windows в исходном состоянии</span><span class="sxs-lookup"><span data-stu-id="32ca0-163">Restore Application and Windows Settings to Original State</span></span>


<span data-ttu-id="32ca0-164">Команды WMI и Windows PowerShell позволяют восстанавливать параметры приложения и Windows в значениях параметров, которые были установлены на компьютере при первом запуске приложения после установки UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="32ca0-164">WMI and Windows PowerShell commands let you restore application and Windows settings to the settings values that were on the computer the first time that the application started after the UE-V Agent was installed.</span></span> <span data-ttu-id="32ca0-165">Это действие по восстановлению выполняется отдельно для каждого приложения или параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="32ca0-165">This restoring action is performed on a per-application or Windows settings basis.</span></span> <span data-ttu-id="32ca0-166">Эти параметры восстанавливаются при следующем запуске приложения или восстанавливаются при входе пользователя в операционную систему.</span><span class="sxs-lookup"><span data-stu-id="32ca0-166">The settings are restored the next time that the application runs, or the settings are restored when the user logs on to the operating system.</span></span>

**<span data-ttu-id="32ca0-167">Восстановление параметров приложения и параметров Windows с помощью Windows PowerShell для UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="32ca0-167">To restore application settings and Windows settings with Windows PowerShell for UE-V 2.x</span></span>**

1.  <span data-ttu-id="32ca0-168">Откройте окно Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="32ca0-168">Open the Windows PowerShell window.</span></span>

2.  <span data-ttu-id="32ca0-169">Чтобы восстановить параметры приложения и параметры Windows, введите следующий командлет Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="32ca0-169">Enter the following Windows PowerShell cmdlet to restore the application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="32ca0-170">Командлет Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="32ca0-170">Windows PowerShell cmdlet</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="32ca0-171">Описание</span><span class="sxs-lookup"><span data-stu-id="32ca0-171">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Restore-UevUserSetting -&lt;TemplateID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="32ca0-172">Восстанавливает параметры пользователя для приложения или восстанавливает группу параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="32ca0-172">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="32ca0-173">Восстановление параметров приложения и параметров Windows с помощью WMI</span><span class="sxs-lookup"><span data-stu-id="32ca0-173">To restore application settings and Windows settings with WMI</span></span>**

1.  <span data-ttu-id="32ca0-174">Откройте окно Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="32ca0-174">Open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="32ca0-175">Чтобы восстановить параметры приложения и параметры Windows, введите следующую команду WMI.</span><span class="sxs-lookup"><span data-stu-id="32ca0-175">Enter the following WMI command to restore application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="32ca0-176">Команда WMI</span><span class="sxs-lookup"><span data-stu-id="32ca0-176">WMI command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="32ca0-177">Описание</span><span class="sxs-lookup"><span data-stu-id="32ca0-177">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="32ca0-178">Восстанавливает параметры пользователя для приложения или восстанавливает группу параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="32ca0-178">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
UE-V does not provide a settings rollback for Windows apps.
~~~








## <span data-ttu-id="32ca0-179">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="32ca0-179">Related topics</span></span>


[<span data-ttu-id="32ca0-180">Администрирование UE-V 2. x с помощью Windows PowerShell и WMI</span><span class="sxs-lookup"><span data-stu-id="32ca0-180">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="32ca0-181">Администрирование UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="32ca0-181">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









