---
title: Управление агентом и пакетами UE-V 1.0 с помощью PowerShell и инструментария WMI
description: Управление агентом и пакетами UE-V 1.0 с помощью PowerShell и инструментария WMI
author: dansimp
ms.assetid: c8989b01-1769-4e69-82b1-4aadb261d2d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79268e3384aaaf08bdd4e9b92d74b039ce96596a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819299"
---
# <span data-ttu-id="8ec1b-103">Управление агентом и пакетами UE-V 1.0 с помощью PowerShell и инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="8ec1b-103">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>


<span data-ttu-id="8ec1b-104">Вы можете использовать WMI и PowerShell для управления конфигурацией и синхронизацией агента Microsoft User Experience Virtualization (UE-V).</span><span class="sxs-lookup"><span data-stu-id="8ec1b-104">You can use WMI and PowerShell to manage Microsoft User Experience Virtualization (UE-V) Agent configuration and synchronization behavior.</span></span>

**<span data-ttu-id="8ec1b-105">Развертывание агента UE-V с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec1b-105">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="8ec1b-106">Поэтапный файл установщика UE-V в общедоступном сетевом общем доступе.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-106">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="8ec1b-107">Примечание.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-107">Note</span></span>**  
    <span data-ttu-id="8ec1b-108">Используйте AgentSetup.exe для развертывания 32-и 64-разрядных версий агента UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-108">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="8ec1b-109">Для каждой архитектуры доступны файлы установщика Windows версии, AgentSetupx86.msi и AgentSetupx64.msi.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-109">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="8ec1b-110">Чтобы позднее удалить агент UE-V с помощью файла установки, необходимо использовать тот же тип файлов.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-110">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="8ec1b-111">Для установки агента используйте одну из следующих команд PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-111">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="8ec1b-112">Настройка агента UE-V с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec1b-112">How to configure the UE-V Agent with PowerShell</span></span>**

1.  <span data-ttu-id="8ec1b-113">Используйте учетную запись с правами администратора, чтобы открыть окно PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-113">Use an account with administrator rights to open a PowerShell window.</span></span> <span data-ttu-id="8ec1b-114">Импортируйте модуль PowerShell UE-V с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-114">Import the UE-V PowerShell module by using the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="8ec1b-115">Используйте следующие команды PowerShell для настройки агента.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-115">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="8ec1b-116">Команда PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec1b-116">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="8ec1b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="8ec1b-117">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-118">Get-UevConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ec1b-118">Get-UevConfiguration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-119">Просмотр эффективных параметров агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-119">View the effective UE-V agent settings.</span></span> <span data-ttu-id="8ec1b-120">Параметры для определенного пользователя имеют приоритет над параметрами компьютера.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-121">Get-UevConfiguration-CurrentComputerUser</span><span class="sxs-lookup"><span data-stu-id="8ec1b-121">Get-UevConfiguration - CurrentComputerUser</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-122">Просмотр значений параметров агента UE-V только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-122">View the UE-V agent settings values for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-123">Get-UevConfiguration-Computer</span><span class="sxs-lookup"><span data-stu-id="8ec1b-123">Get-UevConfiguration -Computer</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-124">Просмотрите значения параметров конфигурации агента UE-V для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-124">View the UE-V agent configuration settings values for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-125">Set-UevConfiguration-SettingsStoragePath &lt; путь к _settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-125">Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-126">Определение места хранения параметров для компьютера.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-126">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-127">Set-UevConfiguration-CurrentComputerUser-SettingsStoragePath &lt; путь к _settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-127">Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-128">Определите расположение для хранения параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-128">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-129">Set-UevConfiguration-SyncTimeoutInMilliseconds timeout ( &lt; в миллисекундах)&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-129">Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-130">Настройка времени ожидания синхронизации в миллисекундах</span><span class="sxs-lookup"><span data-stu-id="8ec1b-130">Set the synchronization timeout in milliseconds</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-131">Set-UevConfiguration-CurrentComputerUser-SyncTimeoutInMilliseconds &lt; время ожидания в миллисекундах&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-131">Set-UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-132">Задайте время ожидания синхронизации для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-132">Set the synchronization timeout for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-133">Set-UevConfiguration-Computer-MaxPackageSizeInBytes &lt; size (байт)&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-133">Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-134">Настройте агент UE-V, чтобы сообщить о том, что размер файла пакета параметров достигнет определенного порогового значения.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-134">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="8ec1b-135">Установка порогового размера пакета в байтах.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-135">Set the threshold package size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-136">Set-UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; Размер в байтах&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-136">Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-137">Установите пороговое значение порогового значения для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-137">Set the package size warning threshold for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-138">Set-UevConfiguration-Computer – SettingsTemplateCatalogPath &lt; путь к каталогу&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-138">Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-139">Задайте путь к каталогу шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-139">Set the settings template catalog path.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-140">Метод Sync Set-UevConfiguration-Computer-PowerSchool &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-140">Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-141">Задайте метод синхронизации: OfflineFiles или None.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-141">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-142">Метод Sync Set-UevConfiguration-CurrentComputerUser-PowerSchool &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-142">Set-UevConfiguration -CurrentComputerUser -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-143">Задайте метод синхронизации для текущего пользователя: OfflineFiles или None (нет).</span><span class="sxs-lookup"><span data-stu-id="8ec1b-143">Set the synchronization method for the current user: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-144">Set-UEVConfiguration-Computer – EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="8ec1b-144">Set-UEVConfiguration -Computer –EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-145">Включите уведомление о задержке импорта параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-145">Enable notification to occur when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="8ec1b-146">Используйте – DisableSettingsImportNotify, чтобы отключить уведомление.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-146">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-147">Set-UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="8ec1b-147">Set-UEVConfiguration - CurrentComputerUser -EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-148">Включите уведомление для текущего пользователя, когда задерживается импорт параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-148">Enable notification for the current user when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="8ec1b-149">Используйте – DisableSettingsImportNotify, чтобы отключить уведомление.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-149">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-150">Set-UEVConfiguration-Computer-SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="8ec1b-150">Set-UEVConfiguration -Computer -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-151">Укажите время в секундах, по истечении которого пользователь будет уведомлен</span><span class="sxs-lookup"><span data-stu-id="8ec1b-151">Specify the time in seconds before the user is notified</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-152">Set-UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="8ec1b-152">Set-UEVConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-153">Укажите время в секундах перед уведомлением для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-153">Specify the time in seconds before notification for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-154">Set-UevConfiguration – Computer – DisableSync</span><span class="sxs-lookup"><span data-stu-id="8ec1b-154">Set-UevConfiguration –Computer –DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-155">Отключите UE-V для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-155">Disable UE-V for all the users on the computer.</span></span></p>
    <p><span data-ttu-id="8ec1b-156">Используйте параметр – EnableSync для включения или повторного включения.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-156">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-157">Set-UevConfiguration-CurrentComputerUser-DisableSync</span><span class="sxs-lookup"><span data-stu-id="8ec1b-157">Set-UevConfiguration –CurrentComputerUser -DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-158">Отключите UE-V для текущего пользователя на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-158">Disable UE-V for the current user on the computer.</span></span></p>
    <p><span data-ttu-id="8ec1b-159">Используйте параметр – EnableSync для включения или повторного включения.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-159">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-160">Clear-UevConfiguration — имя компьютера- &lt; параметр&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-160">Clear-UevConfiguration –Computer -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-161">Удалите определенные параметры для всех пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-161">Clear a specific setting for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-162">Clear-UevConfiguration — CurrentComputerUser — &lt; имя параметра&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-162">Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-163">Удалите определенный параметр только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-163">Clear a specific setting for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-164">Export- &lt; файл миграции параметров UevConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-164">Export-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-165">Экспортируйте конфигурацию компьютера UE-V в файл миграции параметров.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-165">Export the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="8ec1b-166">Файл должен иметь расширение ". uev".</span><span class="sxs-lookup"><span data-stu-id="8ec1b-166">The extension of the file must be “.uev”.</span></span></p>
    <p><span data-ttu-id="8ec1b-167">Командлет экспорта экспортирует все параметры агента UE-V, которые можно настроить с помощью параметра-Computer.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-167">The export cmdlet exports all UE-V agent settings that are configurable with the -computer parameter.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-168">&lt;Файл миграции параметров импорта и UevConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-168">Import-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-169">Импорт конфигурации компьютера UE-V из файла миграции параметров (uev-файла).</span><span class="sxs-lookup"><span data-stu-id="8ec1b-169">Import the UE-V computer configuration from a settings migration file (.uev file).</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="8ec1b-170">Экспорт параметров пакета UE-V и восстановление шаблонов UE-V с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec1b-170">How to export UE-V package settings and repair UE-V templates with PowerShell</span></span>**

1.  <span data-ttu-id="8ec1b-171">Откройте окно PowerShell с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-171">Open a PowerShell window as an Administrator.</span></span> <span data-ttu-id="8ec1b-172">Импортируйте модуль PowerShell UE-V с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-172">Import the UE-V PowerShell module with the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="8ec1b-173">Используйте следующие команды PowerShell для настройки агента.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-173">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="8ec1b-174">Команда PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec1b-174">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="8ec1b-175">Описание</span><span class="sxs-lookup"><span data-stu-id="8ec1b-175">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-176">Export-UevPackage MicrosoftCalculator6. pkgx</span><span class="sxs-lookup"><span data-stu-id="8ec1b-176">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-177">Извлекает параметры из файла пакета калькулятора (Майкрософт) и преобразует их в формат XML, пригодный для восприятия.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-177">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-178">Repair-UevTemplateIndex</span><span class="sxs-lookup"><span data-stu-id="8ec1b-178">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-179">Восстанавливает индексы шаблонов расположений параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-179">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="8ec1b-180">Настройка агента UE-V с WMI</span><span class="sxs-lookup"><span data-stu-id="8ec1b-180">How to configure the UE-V Agent with WMI</span></span>**

1.  <span data-ttu-id="8ec1b-181">Виртуализация взаимодействия с пользователем предоставляет следующий набор команд WMI.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-181">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="8ec1b-182">Администраторы могут использовать этот интерфейс для настройки агента UE-V из командной строки и автоматизации типичных задач настройки.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-182">Administrators can use this interface to configure the UE-V agent from the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="8ec1b-183">Используйте учетную запись с правами администратора, чтобы открыть окно PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-183">Use an account with administrator rights to open a PowerShell window.</span></span>

2.  <span data-ttu-id="8ec1b-184">Используйте следующие команды WMI для настройки агента.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-184">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="8ec1b-185">Команда PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec1b-185">PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="8ec1b-186">Описание</span><span class="sxs-lookup"><span data-stu-id="8ec1b-186">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-187">Конфигурация root\Microsoft\UEV Get-WmiObject-Namespace</span><span class="sxs-lookup"><span data-stu-id="8ec1b-187">Get-WmiObject -Namespace root\Microsoft\UEV Configuration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-188">Просмотр активных параметров агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-188">View the active UE-V agent settings.</span></span> <span data-ttu-id="8ec1b-189">Параметры для определенного пользователя имеют приоритет над параметрами компьютера.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-189">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-190">Get-WmiObject-Namespace root\Microsoft\UEV UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ec1b-190">Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-191">Просмотреть конфигурацию агента UE-V, определенную для пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-191">View the UE-V agent configuration that is defined for user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-192">Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ec1b-192">Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-193">Просмотрите конфигурацию агента UE-V, определенную для компьютера.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-193">View the UE-V agent configuration that is defined for computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-194">$config = Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ec1b-194">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="8ec1b-195">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-195">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="8ec1b-196">$config. "Вставить" ()</span><span class="sxs-lookup"><span data-stu-id="8ec1b-196">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-197">Определение места хранения параметров для компьютера.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-197">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-198">$config = Get-WmiObject-Namespace root\Microsoft\UEV UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ec1b-198">$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p>
    <p><span data-ttu-id="8ec1b-199">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-199">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="8ec1b-200">$config. "Вставить" ()</span><span class="sxs-lookup"><span data-stu-id="8ec1b-200">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-201">Определите расположение для хранения параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-201">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-202">$config = Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ec1b-202">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="8ec1b-203">$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-203">$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</span></span></p>
    <p><span data-ttu-id="8ec1b-204">$config. "Вставить" ()</span><span class="sxs-lookup"><span data-stu-id="8ec1b-204">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-205">Задайте время ожидания синхронизации в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-205">Set the synchronization timeout in milliseconds.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-206">$config = Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ec1b-206">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="8ec1b-207">$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-207">$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</span></span></p>
    <p><span data-ttu-id="8ec1b-208">$config. "Вставить" ()</span><span class="sxs-lookup"><span data-stu-id="8ec1b-208">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-209">Настройте агент UE-V, чтобы сообщить о том, что размер файла пакета параметров достигнет определенного порогового значения.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-209">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="8ec1b-210">Укажите размер файла порогового пакета в байтах.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-210">Set the threshold package file size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-211">$config = Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ec1b-211">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="8ec1b-212">$config. PowerSchool = &lt; sync_method&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-212">$config.SyncMethod = &lt;sync_method&gt;</span></span></p>
    <p><span data-ttu-id="8ec1b-213">$config. "Вставить" ()</span><span class="sxs-lookup"><span data-stu-id="8ec1b-213">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-214">Задайте метод синхронизации: OfflineFiles или None.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-214">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8ec1b-215">$config = Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ec1b-215">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="8ec1b-216">$config. &lt; Установка &gt;  =  &lt; значения параметра Name&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-216">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="8ec1b-217">$config. "Вставить" ()</span><span class="sxs-lookup"><span data-stu-id="8ec1b-217">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-218">Обновите конкретный параметр для компьютера.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-218">Update a specific per-computer setting.</span></span> <span data-ttu-id="8ec1b-219">Чтобы снять этот параметр, используйте $null в качестве значения параметра.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-219">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8ec1b-220">$config = Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ec1b-220">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="8ec1b-221">$config. &lt; Установка &gt;  =  &lt; значения параметра Name&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec1b-221">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="8ec1b-222">$config. "Вставить" ()</span><span class="sxs-lookup"><span data-stu-id="8ec1b-222">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8ec1b-223">Обновите конкретный параметр для отдельного пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-223">Update a specific per-user setting.</span></span> <span data-ttu-id="8ec1b-224">Чтобы снять этот параметр, используйте $null в качестве значения параметра.</span><span class="sxs-lookup"><span data-stu-id="8ec1b-224">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## <span data-ttu-id="8ec1b-225">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8ec1b-225">Related topics</span></span>


[<span data-ttu-id="8ec1b-226">Администрирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="8ec1b-226">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="8ec1b-227">Операции в UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="8ec1b-227">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)









