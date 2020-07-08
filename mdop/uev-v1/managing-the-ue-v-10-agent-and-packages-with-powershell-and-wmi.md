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
# Управление агентом и пакетами UE-V 1.0 с помощью PowerShell и инструментария WMI


Вы можете использовать WMI и PowerShell для управления конфигурацией и синхронизацией агента Microsoft User Experience Virtualization (UE-V).

**Развертывание агента UE-V с помощью PowerShell**

1.  Поэтапный файл установщика UE-V в общедоступном сетевом общем доступе.

    **Примечание.**  
    Используйте AgentSetup.exe для развертывания 32-и 64-разрядных версий агента UE-V Agent. Для каждой архитектуры доступны файлы установщика Windows версии, AgentSetupx86.msi и AgentSetupx64.msi. Чтобы позднее удалить агент UE-V с помощью файла установки, необходимо использовать тот же тип файлов.



2.  Для установки агента используйте одну из следующих команд PowerShell.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Настройка агента UE-V с помощью PowerShell**

1.  Используйте учетную запись с правами администратора, чтобы открыть окно PowerShell. Импортируйте модуль PowerShell UE-V с помощью следующей команды.

    ``` syntax
    Import-module UEV
    ```

2.  Используйте следующие команды PowerShell для настройки агента.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Команда PowerShell</strong></p></td>
    <td align="left"><p><strong>Описание</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-UevConfiguration</p>
    <p></p></td>
    <td align="left"><p>Просмотр эффективных параметров агента UE-V. Параметры для определенного пользователя имеют приоритет над параметрами компьютера.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Get-UevConfiguration-CurrentComputerUser</p>
    <p></p></td>
    <td align="left"><p>Просмотр значений параметров агента UE-V только для текущего пользователя.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-UevConfiguration-Computer</p></td>
    <td align="left"><p>Просмотрите значения параметров конфигурации агента UE-V для всех пользователей компьютера.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-SettingsStoragePath &lt; путь к _settings_storage_location&gt;</p></td>
    <td align="left"><p>Определение места хранения параметров для компьютера.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-SettingsStoragePath &lt; путь к _settings_storage_location&gt;</p></td>
    <td align="left"><p>Определите расположение для хранения параметров пользователя.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-SyncTimeoutInMilliseconds timeout ( &lt; в миллисекундах)&gt;</p></td>
    <td align="left"><p>Настройка времени ожидания синхронизации в миллисекундах</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-SyncTimeoutInMilliseconds &lt; время ожидания в миллисекундах&gt;</p></td>
    <td align="left"><p>Задайте время ожидания синхронизации для текущего пользователя.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-Computer-MaxPackageSizeInBytes &lt; size (байт)&gt;</p></td>
    <td align="left"><p>Настройте агент UE-V, чтобы сообщить о том, что размер файла пакета параметров достигнет определенного порогового значения. Установка порогового размера пакета в байтах.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; Размер в байтах&gt;</p></td>
    <td align="left"><p>Установите пороговое значение порогового значения для текущего пользователя.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-Computer – SettingsTemplateCatalogPath &lt; путь к каталогу&gt;</p></td>
    <td align="left"><p>Задайте путь к каталогу шаблонов параметров.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Метод Sync Set-UevConfiguration-Computer-PowerSchool &lt;&gt;</p></td>
    <td align="left"><p>Задайте метод синхронизации: OfflineFiles или None.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Метод Sync Set-UevConfiguration-CurrentComputerUser-PowerSchool &lt;&gt;</p></td>
    <td align="left"><p>Задайте метод синхронизации для текущего пользователя: OfflineFiles или None (нет).</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UEVConfiguration-Computer – EnableSettingsImportNotify</p></td>
    <td align="left"><p>Включите уведомление о задержке импорта параметров пользователя.</p>
    <p>Используйте – DisableSettingsImportNotify, чтобы отключить уведомление.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</p></td>
    <td align="left"><p>Включите уведомление для текущего пользователя, когда задерживается импорт параметров пользователя.</p>
    <p>Используйте – DisableSettingsImportNotify, чтобы отключить уведомление.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UEVConfiguration-Computer-SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>Укажите время в секундах, по истечении которого пользователь будет уведомлен</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>Укажите время в секундах перед уведомлением для текущего пользователя.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration – Computer – DisableSync</p></td>
    <td align="left"><p>Отключите UE-V для всех пользователей компьютера.</p>
    <p>Используйте параметр – EnableSync для включения или повторного включения.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-DisableSync</p></td>
    <td align="left"><p>Отключите UE-V для текущего пользователя на компьютере.</p>
    <p>Используйте параметр – EnableSync для включения или повторного включения.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Clear-UevConfiguration — имя компьютера- &lt; параметр&gt;</p></td>
    <td align="left"><p>Удалите определенные параметры для всех пользователей на компьютере.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Clear-UevConfiguration — CurrentComputerUser — &lt; имя параметра&gt;</p></td>
    <td align="left"><p>Удалите определенный параметр только для текущего пользователя.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Export- &lt; файл миграции параметров UevConfiguration&gt;</p></td>
    <td align="left"><p>Экспортируйте конфигурацию компьютера UE-V в файл миграции параметров. Файл должен иметь расширение ". uev".</p>
    <p>Командлет экспорта экспортирует все параметры агента UE-V, которые можно настроить с помощью параметра-Computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>&lt;Файл миграции параметров импорта и UevConfiguration&gt;</p></td>
    <td align="left"><p>Импорт конфигурации компьютера UE-V из файла миграции параметров (uev-файла).</p></td>
    </tr>
    </tbody>
    </table>



**Экспорт параметров пакета UE-V и восстановление шаблонов UE-V с помощью PowerShell**

1.  Откройте окно PowerShell с правами администратора. Импортируйте модуль PowerShell UE-V с помощью следующей команды.

    ``` syntax
    Import-module UEV
    ```

2.  Используйте следующие команды PowerShell для настройки агента.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Команда PowerShell</strong></p></td>
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



**Настройка агента UE-V с WMI**

1.  Виртуализация взаимодействия с пользователем предоставляет следующий набор команд WMI. Администраторы могут использовать этот интерфейс для настройки агента UE-V из командной строки и автоматизации типичных задач настройки.

    Используйте учетную запись с правами администратора, чтобы открыть окно PowerShell.

2.  Используйте следующие команды WMI для настройки агента.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Команда PowerShell</th>
    <th align="left">Описание</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Конфигурация root\Microsoft\UEV Get-WmiObject-Namespace</p>
    <p></p></td>
    <td align="left"><p>Просмотр активных параметров агента UE-V. Параметры для определенного пользователя имеют приоритет над параметрами компьютера.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-WmiObject-Namespace root\Microsoft\UEV UserConfiguration</p></td>
    <td align="left"><p>Просмотреть конфигурацию агента UE-V, определенную для пользователя.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</p></td>
    <td align="left"><p>Просмотрите конфигурацию агента UE-V, определенную для компьютера.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. "Вставить" ()</p></td>
    <td align="left"><p>Определение места хранения параметров для компьютера.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-Namespace root\Microsoft\UEV UserConfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. "Вставить" ()</p></td>
    <td align="left"><p>Определите расположение для хранения параметров пользователя.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</p>
    <p>$config. "Вставить" ()</p></td>
    <td align="left"><p>Задайте время ожидания синхронизации в миллисекундах.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</p>
    <p>$config. "Вставить" ()</p></td>
    <td align="left"><p>Настройте агент UE-V, чтобы сообщить о том, что размер файла пакета параметров достигнет определенного порогового значения. Укажите размер файла порогового пакета в байтах.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. PowerSchool = &lt; sync_method&gt;</p>
    <p>$config. "Вставить" ()</p></td>
    <td align="left"><p>Задайте метод синхронизации: OfflineFiles или None.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; Установка &gt;  =  &lt; значения параметра Name&gt;</p>
    <p>$config. "Вставить" ()</p></td>
    <td align="left"><p>Обновите конкретный параметр для компьютера. Чтобы снять этот параметр, используйте $null в качестве значения параметра.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-Namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; Установка &gt;  =  &lt; значения параметра Name&gt;</p>
    <p>$config. "Вставить" ()</p></td>
    <td align="left"><p>Обновите конкретный параметр для отдельного пользователя. Чтобы снять этот параметр, используйте $null в качестве значения параметра.</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## Статьи по теме


[Администрирование UE-V 1.0](administering-ue-v-10.md)

[Операции в UE-V 1.0](operations-for-ue-v-10.md)









