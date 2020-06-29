---
title: Управление агентом UE-V 2. x и пакетами с помощью Windows PowerShell и WMI
description: Управление агентом UE-V 2. x и пакетами с помощью Windows PowerShell и WMI
author: dansimp
ms.assetid: 56e6780b-8b2c-4717-91c8-2af63062ab75
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6a709d2c66266cf33b8e89ddd905aa0f21eb7dfe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826802"
---
# <span data-ttu-id="78086-103">Управление агентом UE-V 2. x и пакетами с помощью Windows PowerShell и WMI</span><span class="sxs-lookup"><span data-stu-id="78086-103">Managing the UE-V 2.x Agent and Packages with Windows PowerShell and WMI</span></span>


<span data-ttu-id="78086-104">Вы можете использовать инструментарий управления Windows (WMI) и Windows PowerShell для управления конфигурацией Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 и 2,1 конфигурации агента SP1 и синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="78086-104">You can use Windows Management Instrumentation (WMI) and Windows PowerShell to manage Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent configuration and synchronization behavior.</span></span> <span data-ttu-id="78086-105">Полный список командлетов PowerShell для UE-V можно найти в [справочнике по командлетам UE-v 2](https://go.microsoft.com/fwlink/?LinkId=393495) ( https://go.microsoft.com/fwlink/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="78086-105">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/?LinkId=393495) (https://go.microsoft.com/fwlink/?LinkId=393495).</span></span>

**<span data-ttu-id="78086-106">Развертывание агента UE-V с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="78086-106">To deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="78086-107">Поэтапный файл установщика UE-V в общедоступном сетевом общем доступе.</span><span class="sxs-lookup"><span data-stu-id="78086-107">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="78086-108">Примечание.</span><span class="sxs-lookup"><span data-stu-id="78086-108">Note</span></span>**  
    <span data-ttu-id="78086-109">Используйте AgentSetup.exe для развертывания 32-и 64-разрядных версий агента UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="78086-109">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="78086-110">Для каждой архитектуры доступны пакеты установщика Windows, AgentSetupx86.msi и AgentSetupx64.msi.</span><span class="sxs-lookup"><span data-stu-id="78086-110">Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="78086-111">Чтобы позднее удалить агент UE-V с помощью файла установки, необходимо использовать тот же тип файлов.</span><span class="sxs-lookup"><span data-stu-id="78086-111">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="78086-112">Используйте одну из следующих команд Windows PowerShell, чтобы установить агент UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="78086-112">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="78086-113">Настройка агента UE-V с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="78086-113">To configure the UE-V Agent by using Windows PowerShell</span></span>**

1. <span data-ttu-id="78086-114">Откройте окно Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="78086-114">Open a Windows PowerShell window.</span></span> <span data-ttu-id="78086-115">Чтобы настроить параметры компьютера, влияющие на всех пользователей компьютера, с помощью параметра *компьютера* , откройте окно с учетной записью с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="78086-115">To manage computer settings that affect all users of the computer by using the *Computer* parameter, open the window with an account that has administrator rights.</span></span>

2. <span data-ttu-id="78086-116">Используйте следующие команды Windows PowerShell для настройки агента.</span><span class="sxs-lookup"><span data-stu-id="78086-116">Use the following Windows PowerShell commands to configure the agent.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="78086-117">Команда Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="78086-117">Windows PowerShell command</span></span></th>
   <th align="left"><span data-ttu-id="78086-118">Описание</span><span class="sxs-lookup"><span data-stu-id="78086-118">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="78086-119">Получает действующие параметры агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="78086-119">Gets the effective UE-V Agent settings.</span></span> <span data-ttu-id="78086-120">Параметры для определенного пользователя имеют приоритет над параметрами компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="78086-121">Возвращает значения параметров агента UE-V только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="78086-121">Gets the UE-V Agent settings values for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-122">Получает значения параметров конфигурации агента UE-V для всех пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="78086-122">Gets the UE-V Agent configuration settings values for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-123">Получает сведения о каждом параметре конфигурации.</span><span class="sxs-lookup"><span data-stu-id="78086-123">Gets the details for each configuration setting.</span></span> <span data-ttu-id="78086-124">Показывает, где настроен параметр, или используется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="78086-124">Displays where the setting is configured or if it uses the default value.</span></span> <span data-ttu-id="78086-125">Отображается, если текущий параметр является допустимым.</span><span class="sxs-lookup"><span data-stu-id="78086-125">Is displayed if the current setting is valid.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-126">Задает текст, отображаемый в центре параметров компании для ссылки на справку.</span><span class="sxs-lookup"><span data-stu-id="78086-126">Sets the text that is displayed in the Company Settings Center for the help link.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-127">Задает URL-адрес ссылки в центре "Параметры компании" для ссылки "Справка".</span><span class="sxs-lookup"><span data-stu-id="78086-127">Sets the URL of the link in the Company Settings Center for the help link.</span></span> <span data-ttu-id="78086-128">Можно использовать любой протокол URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="78086-128">Any URL protocol can be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-129">Настраивает агент UE-V не синхронизировать приложения для Windows для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-129">Configures the UE-V Agent to not synchronize any Windows apps for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-130">Настраивает агент UE-V не синхронизировать никакие приложения для Windows для текущего пользователя компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-130">Configures the UE-V Agent to not synchronize any Windows apps for the current computer user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-131">Настраивает агент UE-V на отображение уведомления при первом запуске агента для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-131">Configures the UE-V Agent to display notification the first time the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-132">Настройка агента UE-V без уведомления при первом запуске агента для всех пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="78086-132">Configures the UE-V Agent to not display notification the first time that the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-133">Настройка агента UE-V для уведомления всех пользователей на компьютере о задержке синхронизации параметров.</span><span class="sxs-lookup"><span data-stu-id="78086-133">Configures the UE-V Agent to notify all users on the computer when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="78086-134"><em> </em> Чтобы отключить уведомление, используйте параметр DisableSettingsImportNotify.</span><span class="sxs-lookup"><span data-stu-id="78086-134">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-135">Настраивает агент UE-V для уведомления текущего пользователя о задержке синхронизации параметров.</span><span class="sxs-lookup"><span data-stu-id="78086-135">Configures the UE-V Agent to notify the current user when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="78086-136"><em> </em> Чтобы отключить уведомление, используйте параметр DisableSettingsImportNotify.</span><span class="sxs-lookup"><span data-stu-id="78086-136">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-137">Настройка агента UE-V для синхронизации всех приложений для Windows, которые не отключены явным образом с помощью списка приложений для Windows для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-137">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for all users of the computer.</span></span> <span data-ttu-id="78086-138">Дополнительные сведения можно найти &quot; в статьях Get-UevAppxPackage &quot; в разделе <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Управление шаблонами расположений параметров ue-V 2. x с помощью Windows PowerShell и WMI </a> .</span><span class="sxs-lookup"><span data-stu-id="78086-138">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="78086-139">С помощью <em> </em> параметра DisableSyncUnlistedWindows8Apps настройте агент UE-V для синхронизации только приложений для Windows, которые явно включены в список приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="78086-139">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-140">Настраивает агент UE-V для синхронизации всех приложений для Windows, которые не отключены явным образом с помощью списка приложений Windows для текущего пользователя на компьютере.</span><span class="sxs-lookup"><span data-stu-id="78086-140">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for the current user on the computer.</span></span> <span data-ttu-id="78086-141">Дополнительные сведения можно найти &quot; в статьях Get-UevAppxPackage &quot; в разделе <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Управление шаблонами расположений параметров ue-V 2. x с помощью Windows PowerShell и WMI </a> .</span><span class="sxs-lookup"><span data-stu-id="78086-141">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="78086-142">С помощью <em> </em> параметра DisableSyncUnlistedWindows8Apps настройте агент UE-V для синхронизации только приложений для Windows, которые явно включены в список приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="78086-142">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-143">Отключение UE-V для всех пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="78086-143">Disables UE-V for all the users on the computer.</span></span></p>
   <p><span data-ttu-id="78086-144">Используйте <em> параметр EnableSync </em> для включения или повторного включения.</span><span class="sxs-lookup"><span data-stu-id="78086-144">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-145">Отключение UE-V для текущего пользователя на компьютере.</span><span class="sxs-lookup"><span data-stu-id="78086-145">Disables UE-V for the current user on the computer.</span></span></p>
   <p><span data-ttu-id="78086-146">Используйте <em> параметр EnableSync </em> для включения или повторного включения.</span><span class="sxs-lookup"><span data-stu-id="78086-146">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-147">Включает значок UE-V в области уведомлений для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-147">Enables the UE-V icon in the notification area for all users of the computer.</span></span></p>
   <p><span data-ttu-id="78086-148"><em> </em> Чтобы отключить этот значок, используйте параметр DisableTrayIcon.</span><span class="sxs-lookup"><span data-stu-id="78086-148">Use the <em>DisableTrayIcon</em> parameter to disable the icon.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-149">Настройка агента UE-V для отправки отчета о том, что размер файла пакета параметров достигает определенного порогового значения для всех пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="78086-149">Configures the UE-V agent to report when a settings package file size reaches the defined threshold for all users on the computer.</span></span> <span data-ttu-id="78086-150">Задает пороговый размер пакета в байтах.</span><span class="sxs-lookup"><span data-stu-id="78086-150">Sets the threshold package size in bytes.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-151">Настраивает агент UE-V для отчета о том, что размер файла пакета параметров достигает определенного порогового значения.</span><span class="sxs-lookup"><span data-stu-id="78086-151">Configures the UE-V agent to report when a settings package file size reaches the defined threshold.</span></span> <span data-ttu-id="78086-152">Задает порог предупреждений о размере пакета для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="78086-152">Sets the package size warning threshold for the current user.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-153">Указывает время в секундах, по истечении которого пользователь будет уведомлен для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-153">Specifies the time in seconds before the user is notified for all users of the computer</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-154">Указывает время в секундах перед отправкой уведомления для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="78086-154">Specifies the time in seconds before notification for the current user is sent.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-155">Определяет расположение хранилища параметров для каждого компьютера для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-155">Defines a per-computer settings storage location for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-156">Определяет расположение хранилища параметров для пользователя.</span><span class="sxs-lookup"><span data-stu-id="78086-156">Defines a per-user settings storage location.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-157">Задает путь к каталогу шаблонов параметров для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-157">Sets the settings template catalog path for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-158">Задает метод синхронизации для всех пользователей компьютера: SyncProvider или None (нет).</span><span class="sxs-lookup"><span data-stu-id="78086-158">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-159">Задает метод синхронизации для текущего пользователя: SyncProvider или None.</span><span class="sxs-lookup"><span data-stu-id="78086-159">Sets the synchronization method for the current user: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-160">Задает время ожидания синхронизации в миллисекундах для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-160">Sets the synchronization time-out in milliseconds for all users of the computer</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-161">Задайте время ожидания синхронизации для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="78086-161">Set the synchronization time-out for the current user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-162">Очищает указанный параметр для всех пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="78086-162">Clears the specified setting for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-163">Очищает указанный параметр только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="78086-163">Clears the specified setting for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-164">Экспорт конфигурации компьютера UE-V в файл миграции параметров.</span><span class="sxs-lookup"><span data-stu-id="78086-164">Exports the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="78086-165">Расширение имени файла должно быть. uev.</span><span class="sxs-lookup"><span data-stu-id="78086-165">The file name extension must be .uev.</span></span></p>
   <p><span data-ttu-id="78086-166"><code>Export</code>Командлет экспортирует все параметры агента UE-V, которые можно настроить с помощью <em> параметра Computer </em> .</span><span class="sxs-lookup"><span data-stu-id="78086-166">The <code>Export</code> cmdlet exports all UE-V Agent settings that are configurable with the <em>Computer</em> parameter.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="78086-167">Импорт конфигурации компьютера UE-V из файла миграции параметров.</span><span class="sxs-lookup"><span data-stu-id="78086-167">Imports the UE-V computer configuration from a settings migration file.</span></span> <span data-ttu-id="78086-168">Расширение имени файла должно быть. uev.</span><span class="sxs-lookup"><span data-stu-id="78086-168">The file name extension must be .uev.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="78086-169">Экспорт параметров пакета UE-V и восстановление шаблонов UE-V с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="78086-169">To export UE-V package settings and repair UE-V templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="78086-170">Откройте окно Windows PowerShell с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="78086-170">Open a Windows PowerShell window as an administrator.</span></span>

2.  <span data-ttu-id="78086-171">Используйте следующие команды Windows PowerShell для настройки агента.</span><span class="sxs-lookup"><span data-stu-id="78086-171">Use the following Windows PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="78086-172">Команда Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="78086-172">Windows PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="78086-173">Описание</span><span class="sxs-lookup"><span data-stu-id="78086-173">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="78086-174">Export-UevPackage MicrosoftCalculator6. pkgx</span><span class="sxs-lookup"><span data-stu-id="78086-174">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="78086-175">Извлекает параметры из файла пакета калькулятора (Майкрософт) и преобразует их в формат XML, пригодный для восприятия.</span><span class="sxs-lookup"><span data-stu-id="78086-175">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="78086-176">Repair-UevTemplateIndex</span><span class="sxs-lookup"><span data-stu-id="78086-176">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="78086-177">Восстанавливает индексы шаблонов расположений параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="78086-177">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="78086-178">Настройка агента UE-V с помощью WMI</span><span class="sxs-lookup"><span data-stu-id="78086-178">To configure the UE-V Agent by using WMI</span></span>**

1.  <span data-ttu-id="78086-179">Виртуализация взаимодействия с пользователем предоставляет следующий набор команд WMI.</span><span class="sxs-lookup"><span data-stu-id="78086-179">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="78086-180">Администраторы могут использовать этот интерфейс для настройки агента UE-V в командной строке и автоматизации стандартных задач настройки.</span><span class="sxs-lookup"><span data-stu-id="78086-180">Administrators can use this interface to configure the UE-V agent at the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="78086-181">Используйте учетную запись с правами администратора, чтобы открыть окно Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="78086-181">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="78086-182">Используйте следующие команды WMI для настройки агента.</span><span class="sxs-lookup"><span data-stu-id="78086-182">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="78086-183">Описание</span><span class="sxs-lookup"><span data-stu-id="78086-183">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="78086-184">Отображает активные параметры агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="78086-184">Displays the active UE-V Agent settings.</span></span> <span data-ttu-id="78086-185">Параметры для определенного пользователя имеют приоритет над параметрами компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-185">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="78086-186">Отображает конфигурацию агента UE-V, определенную для пользователя.</span><span class="sxs-lookup"><span data-stu-id="78086-186">Displays the UE-V Agent configuration that is defined for a user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="78086-187">Выводит конфигурацию агента UE-V, определенную для компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-187">Displays the UE-V Agent configuration that is defined for a computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p><span data-ttu-id="78086-188">Отображает сведения для каждого элемента конфигурации.</span><span class="sxs-lookup"><span data-stu-id="78086-188">Displays the details for each configuration item.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><span data-ttu-id="78086-189">$config. "Вставить" ()</span><span class="sxs-lookup"><span data-stu-id="78086-189">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="78086-190">Определяет место хранения параметров для компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-190">Defines a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="78086-191">Определяет расположение хранилища параметров для пользователя.</span><span class="sxs-lookup"><span data-stu-id="78086-191">Defines a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="78086-192">Задает время ожидания синхронизации в миллисекундах для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-192">Sets the synchronization time-out in milliseconds for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="78086-193">Настраивает агент UE-V для отчета о том, что размер файла пакета параметров достигает определенного порогового значения.</span><span class="sxs-lookup"><span data-stu-id="78086-193">Configures the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="78086-194">Установка порогового размера файла пакета в байтах для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-194">Set the threshold package file size in bytes for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="78086-195">Задает метод синхронизации для всех пользователей компьютера: SyncProvider или None (нет).</span><span class="sxs-lookup"><span data-stu-id="78086-195">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="78086-196">Чтобы включить конкретный параметр для компьютера, снимите этот флажок и используйте <em> $null </em> в качестве значения параметра.</span><span class="sxs-lookup"><span data-stu-id="78086-196">To enable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="78086-197">Использование UserConfiguration для настройки отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="78086-197">Use UserConfiguration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="78086-198">Чтобы отключить конкретный параметр для каждого компьютера, снимите этот параметр и используйте <em> $null </em> в качестве значения параметра.</span><span class="sxs-lookup"><span data-stu-id="78086-198">To disable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="78086-199">Используйте конфигурацию пользователя для параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="78086-199">Use User Configuration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="78086-200">Обновляет определенный параметр на компьютере.</span><span class="sxs-lookup"><span data-stu-id="78086-200">Updates a specific per-computer setting.</span></span> <span data-ttu-id="78086-201">Чтобы снять этот параметр, используйте <em> $null </em> в качестве значения параметра.</span><span class="sxs-lookup"><span data-stu-id="78086-201">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code><span data-ttu-id="78086-202">$config. &lt; Установка &gt;  =  &lt; значения параметра Name&gt;</span><span class="sxs-lookup"><span data-stu-id="78086-202">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="78086-203">Обновляет определенный параметр для каждого пользователя, который является для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="78086-203">Updates a specific per-user setting for all users of the computer.</span></span> <span data-ttu-id="78086-204">Чтобы снять этот параметр, используйте <em> $null </em> в качестве значения параметра.</span><span class="sxs-lookup"><span data-stu-id="78086-204">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**<span data-ttu-id="78086-205">Экспорт параметров пакета UE-V и восстановление шаблонов UE-V с помощью WMI</span><span class="sxs-lookup"><span data-stu-id="78086-205">To export UE-V package settings and repair UE-V templates by using WMI</span></span>**

1.  <span data-ttu-id="78086-206">UE-V предоставляет следующий набор команд WMI.</span><span class="sxs-lookup"><span data-stu-id="78086-206">UE-V provides the following set of WMI commands.</span></span> <span data-ttu-id="78086-207">Администраторы могут использовать этот интерфейс для экспорта пакета или восстановления шаблонов UE-V.</span><span class="sxs-lookup"><span data-stu-id="78086-207">Administrators can use this interface to export a package or repair UE-V templates.</span></span>

2.  <span data-ttu-id="78086-208">Используйте следующие команды WMI.</span><span class="sxs-lookup"><span data-stu-id="78086-208">Use the following WMI commands.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="78086-209">Команда WMI</span><span class="sxs-lookup"><span data-stu-id="78086-209">WMI command</span></span></th>
    <th align="left"><span data-ttu-id="78086-210">Описание</span><span class="sxs-lookup"><span data-stu-id="78086-210">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="78086-211">Извлекает параметры из файла пакета и преобразует их в формат XML, пригодный для восприятия.</span><span class="sxs-lookup"><span data-stu-id="78086-211">Extracts the settings from a package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p><span data-ttu-id="78086-212">Восстанавливает индексы шаблонов расположений параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="78086-212">Repairs the index of the UE-V settings location templates.</span></span> <span data-ttu-id="78086-213">Необходимо запустить от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="78086-213">Must be run as administrator.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## <span data-ttu-id="78086-214">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="78086-214">Related topics</span></span>


[<span data-ttu-id="78086-215">Администрирование UE-V 2. x с помощью Windows PowerShell и WMI</span><span class="sxs-lookup"><span data-stu-id="78086-215">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="78086-216">Администрирование UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="78086-216">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









