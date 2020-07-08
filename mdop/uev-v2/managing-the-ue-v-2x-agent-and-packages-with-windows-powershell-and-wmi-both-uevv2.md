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
# Управление агентом UE-V 2. x и пакетами с помощью Windows PowerShell и WMI


Вы можете использовать инструментарий управления Windows (WMI) и Windows PowerShell для управления конфигурацией Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 и 2,1 конфигурации агента SP1 и синхронизацией. Полный список командлетов PowerShell для UE-V можно найти в [справочнике по командлетам UE-v 2](https://go.microsoft.com/fwlink/?LinkId=393495) ( https://go.microsoft.com/fwlink/?LinkId=393495) .

**Развертывание агента UE-V с помощью Windows PowerShell**

1.  Поэтапный файл установщика UE-V в общедоступном сетевом общем доступе.

    **Примечание.**  
    Используйте AgentSetup.exe для развертывания 32-и 64-разрядных версий агента UE-V Agent. Для каждой архитектуры доступны пакеты установщика Windows, AgentSetupx86.msi и AgentSetupx64.msi. Чтобы позднее удалить агент UE-V с помощью файла установки, необходимо использовать тот же тип файлов.



2.  Используйте одну из следующих команд Windows PowerShell, чтобы установить агент UE-V Agent.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Настройка агента UE-V с помощью Windows PowerShell**

1. Откройте окно Windows PowerShell. Чтобы настроить параметры компьютера, влияющие на всех пользователей компьютера, с помощью параметра *компьютера* , откройте окно с учетной записью с правами администратора.

2. Используйте следующие команды Windows PowerShell для настройки агента.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Команда Windows PowerShell</th>
   <th align="left">Описание</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p>Получает действующие параметры агента UE-V. Параметры для определенного пользователя имеют приоритет над параметрами компьютера.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p>Возвращает значения параметров агента UE-V только для текущего пользователя.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p>Получает значения параметров конфигурации агента UE-V для всех пользователей на компьютере.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p>Получает сведения о каждом параметре конфигурации. Показывает, где настроен параметр, или используется значение по умолчанию. Отображается, если текущий параметр является допустимым.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p>Задает текст, отображаемый в центре параметров компании для ссылки на справку.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p>Задает URL-адрес ссылки в центре "Параметры компании" для ссылки "Справка". Можно использовать любой протокол URL-адреса.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>Настраивает агент UE-V не синхронизировать приложения для Windows для всех пользователей компьютера.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>Настраивает агент UE-V не синхронизировать никакие приложения для Windows для текущего пользователя компьютера.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p>Настраивает агент UE-V на отображение уведомления при первом запуске агента для всех пользователей компьютера.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p>Настройка агента UE-V без уведомления при первом запуске агента для всех пользователей на компьютере.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>Настройка агента UE-V для уведомления всех пользователей на компьютере о задержке синхронизации параметров.</p>
   <p><em> </em> Чтобы отключить уведомление, используйте параметр DisableSettingsImportNotify.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>Настраивает агент UE-V для уведомления текущего пользователя о задержке синхронизации параметров.</p>
   <p><em> </em> Чтобы отключить уведомление, используйте параметр DisableSettingsImportNotify.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>Настройка агента UE-V для синхронизации всех приложений для Windows, которые не отключены явным образом с помощью списка приложений для Windows для всех пользователей компьютера. Дополнительные сведения можно найти &quot; в статьях Get-UevAppxPackage &quot; в разделе <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Управление шаблонами расположений параметров ue-V 2. x с помощью Windows PowerShell и WMI </a> .</p>
   <p>С помощью <em> </em> параметра DisableSyncUnlistedWindows8Apps настройте агент UE-V для синхронизации только приложений для Windows, которые явно включены в список приложений для Windows.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>Настраивает агент UE-V для синхронизации всех приложений для Windows, которые не отключены явным образом с помощью списка приложений Windows для текущего пользователя на компьютере. Дополнительные сведения можно найти &quot; в статьях Get-UevAppxPackage &quot; в разделе <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Управление шаблонами расположений параметров ue-V 2. x с помощью Windows PowerShell и WMI </a> .</p>
   <p>С помощью <em> </em> параметра DisableSyncUnlistedWindows8Apps настройте агент UE-V для синхронизации только приложений для Windows, которые явно включены в список приложений для Windows.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p>Отключение UE-V для всех пользователей на компьютере.</p>
   <p>Используйте <em> параметр EnableSync </em> для включения или повторного включения.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p>Отключение UE-V для текущего пользователя на компьютере.</p>
   <p>Используйте <em> параметр EnableSync </em> для включения или повторного включения.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p>Включает значок UE-V в области уведомлений для всех пользователей компьютера.</p>
   <p><em> </em> Чтобы отключить этот значок, используйте параметр DisableTrayIcon.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>Настройка агента UE-V для отправки отчета о том, что размер файла пакета параметров достигает определенного порогового значения для всех пользователей на компьютере. Задает пороговый размер пакета в байтах.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>Настраивает агент UE-V для отчета о том, что размер файла пакета параметров достигает определенного порогового значения. Задает порог предупреждений о размере пакета для текущего пользователя.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>Указывает время в секундах, по истечении которого пользователь будет уведомлен для всех пользователей компьютера.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>Указывает время в секундах перед отправкой уведомления для текущего пользователя.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>Определяет расположение хранилища параметров для каждого компьютера для всех пользователей компьютера.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>Определяет расположение хранилища параметров для пользователя.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p>Задает путь к каталогу шаблонов параметров для всех пользователей компьютера.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>Задает метод синхронизации для всех пользователей компьютера: SyncProvider или None (нет).</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>Задает метод синхронизации для текущего пользователя: SyncProvider или None.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>Задает время ожидания синхронизации в миллисекундах для всех пользователей компьютера.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>Задайте время ожидания синхронизации для текущего пользователя.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>Очищает указанный параметр для всех пользователей на компьютере.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>Очищает указанный параметр только для текущего пользователя.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>Экспорт конфигурации компьютера UE-V в файл миграции параметров. Расширение имени файла должно быть. uev.</p>
   <p><code>Export</code>Командлет экспортирует все параметры агента UE-V, которые можно настроить с помощью <em> параметра Computer </em> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>Импорт конфигурации компьютера UE-V из файла миграции параметров. Расширение имени файла должно быть. uev.</p></td>
   </tr>
   </tbody>
   </table>



**Экспорт параметров пакета UE-V и восстановление шаблонов UE-V с помощью Windows PowerShell**

1.  Откройте окно Windows PowerShell с правами администратора.

2.  Используйте следующие команды Windows PowerShell для настройки агента.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Команда Windows PowerShell</strong></p></td>
    <td align="left"><p><strong>Описание</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Export-UevPackage MicrosoftCalculator6. pkgx</p></td>
    <td align="left"><p>Извлекает параметры из файла пакета калькулятора (Майкрософт) и преобразует их в формат XML, пригодный для восприятия.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Repair-UevTemplateIndex</p></td>
    <td align="left"><p>Восстанавливает индексы шаблонов расположений параметров UE-V.</p></td>
    </tr>
    </tbody>
    </table>



**Настройка агента UE-V с помощью WMI**

1.  Виртуализация взаимодействия с пользователем предоставляет следующий набор команд WMI. Администраторы могут использовать этот интерфейс для настройки агента UE-V в командной строке и автоматизации стандартных задач настройки.

    Используйте учетную запись с правами администратора, чтобы открыть окно Windows PowerShell.

2.  Используйте следующие команды WMI для настройки агента.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left">Описание</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p>Отображает активные параметры агента UE-V. Параметры для определенного пользователя имеют приоритет над параметрами компьютера.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p>Отображает конфигурацию агента UE-V, определенную для пользователя.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p>Выводит конфигурацию агента UE-V, определенную для компьютера.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p>Отображает сведения для каждого элемента конфигурации.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p>$config. "Вставить" ()</p></td>
    <td align="left"><p>Определяет место хранения параметров для компьютера.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Определяет расположение хранилища параметров для пользователя.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Задает время ожидания синхронизации в миллисекундах для всех пользователей компьютера.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Настраивает агент UE-V для отчета о том, что размер файла пакета параметров достигает определенного порогового значения. Установка порогового размера файла пакета в байтах для всех пользователей компьютера.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Задает метод синхронизации для всех пользователей компьютера: SyncProvider или None (нет).</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Чтобы включить конкретный параметр для компьютера, снимите этот флажок и используйте <em> $null </em> в качестве значения параметра. Использование UserConfiguration для настройки отдельных пользователей.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Чтобы отключить конкретный параметр для каждого компьютера, снимите этот параметр и используйте <em> $null </em> в качестве значения параметра. Используйте конфигурацию пользователя для параметров пользователя.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Обновляет определенный параметр на компьютере. Чтобы снять этот параметр, используйте <em> $null </em> в качестве значения параметра.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code>$config. &lt; Установка &gt;  =  &lt; значения параметра Name&gt;</p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Обновляет определенный параметр для каждого пользователя, который является для всех пользователей компьютера. Чтобы снять этот параметр, используйте <em> $null </em> в качестве значения параметра.</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**Экспорт параметров пакета UE-V и восстановление шаблонов UE-V с помощью WMI**

1.  UE-V предоставляет следующий набор команд WMI. Администраторы могут использовать этот интерфейс для экспорта пакета или восстановления шаблонов UE-V.

2.  Используйте следующие команды WMI.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Команда WMI</th>
    <th align="left">Описание</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p>Извлекает параметры из файла пакета и преобразует их в формат XML, пригодный для восприятия.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p>Восстанавливает индексы шаблонов расположений параметров UE-V. Необходимо запустить от имени администратора.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## Статьи по теме


[Администрирование UE-V 2. x с помощью Windows PowerShell и WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Администрирование UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









