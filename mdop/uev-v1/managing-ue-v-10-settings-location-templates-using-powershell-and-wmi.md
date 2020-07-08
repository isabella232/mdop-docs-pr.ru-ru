---
title: Управление шаблонами расположения параметров UE-V 1.0 с помощью PowerShell и инструментария WMI
description: Управление шаблонами расположения параметров UE-V 1.0 с помощью PowerShell и инструментария WMI
author: dansimp
ms.assetid: 4b911c78-a5e9-4199-bfeb-72ab764d47c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8dab0997cdfaf7c96862fcce4bc012c3edfe0c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812493"
---
# Управление шаблонами расположения параметров UE-V 1.0 с помощью PowerShell и инструментария WMI


Microsoft User Experience Virtualization (UE-V) использует шаблоны расположений параметров (XML-файлы), которые определяют параметры, зафиксированные и примененные с помощью виртуализации взаимодействия с пользователем. UE-V включает набор стандартных шаблонов расположений параметров. Кроме того, оно включает в себя средство для создания настраиваемых шаблонов расположения параметров с помощью UE-V Generator. После создания и развертывания шаблонов расположений параметров вы можете управлять этими шаблонами с помощью PowerShell или WMI.

## Управление шаблонами расположений параметров с помощью WMI и PowerShell


Функции WMI и PowerShell в UE-V включают возможность включать, отключать, регистрировать, обновлять и отменять регистрацию шаблонов расположений параметров. С помощью этих функций вы можете автоматизировать процесс регистрации, обновления и отмены регистрации шаблонов с помощью агента UE-V Agent. Вы также можете вручную регистрировать шаблоны с помощью WMI и команд PowerShell. С помощью этих функций в сочетании с электронным решением для распространения программного обеспечения, групповой политикой или другим методом автоматического развертывания, таким как сценарий, вы можете автоматизировать этот процесс.

Для обновления, регистрации и отмены регистрации шаблона расположений параметров необходимы разрешения администратора. Для включения и отключения шаблонов не требуются разрешения администратора.

**Управление шаблонами расположений параметров с помощью PowerShell**

1.  Используйте учетную запись с правами администратора, чтобы открыть окно Windows PowerShell. Чтобы импортировать модуль **PowerShell Microsoft UE-V** , введите в командной строке PowerShell указанную ниже команду.

    ``` syntax
    Import-module UEV
    ```

2.  Используйте следующие командлеты PowerShell для регистрации и управления шаблонами расположений параметров UE-V.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Команда PowerShell</strong></th>
    <th align="left"><strong>Описание</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Get-UevTemplate</p></td>
    <td align="left"><p>Список всех шаблонов расположений параметров, зарегистрированных на компьютере.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Регистрация — UevTemplate</p></td>
    <td align="left"><p>Регистрирует шаблон расположения параметров с UE-V. После регистрации шаблона UE-V синхронизирует параметры, определенные в шаблоне, между компьютерами с зарегистрированным шаблоном.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Отмена регистрации — UevTemplate</p></td>
    <td align="left"><p>Отмена регистрации шаблона расположения параметров с UE-V. После отмены регистрации шаблона UE-V больше не будет синхронизировать параметры, определенные в шаблоне, между компьютерами.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Update-UevTemplate</p></td>
    <td align="left"><p>Обновляет шаблон расположений параметров с более новой версией шаблона. Новый шаблон должен иметь версию, которая позже существующей.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Disable-UevTemplate</p></td>
    <td align="left"><p>Отключает шаблон расположения параметров для текущего пользователя компьютера.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Enable-UevTemplate</p></td>
    <td align="left"><p>Включает шаблон расположения параметров для текущего пользователя компьютера.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Test-UevTemplate</p></td>
    <td align="left"><p>Определяет, соответствует ли указанный шаблон расположению параметров своей XML-схеме.</p></td>
    </tr>
    </tbody>
    </table>

     

Возможности UE-V PowerShell позволяют управлять группой шаблонов параметров, развернутых в корпоративной среде. Чтобы управлять группой шаблонов с помощью PowerShell, выполните указанные ниже действия.

**Управление группой шаблонов расположения параметров с помощью PowerShell**

1.  Измените или обновите шаблоны расположения нужных параметров.

2.  Развертывание шаблонов расположений необходимых параметров в папке, доступной на локальном компьютере.

3.  На локальном компьютере откройте окно Windows PowerShell с правами администратора.

4.  Импортируйте модуль PowerShell Microsoft UE-V, введя указанную ниже команду.

    ``` syntax
    Import-module UEV
    ```

5.  Отмените регистрацию всех ранее зарегистрированных версий шаблонов, введя указанную ниже команду.

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    Все активные шаблоны будут отменены на компьютере.

6.  Зарегистрируйте обновленные шаблоны, введя указанную ниже команду.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    Будут зарегистрированы все шаблоны расположений параметров, расположенные в указанной папке шаблона.

Виртуализация взаимодействия с пользователем предоставляет следующий набор команд WMI. Администраторы могут использовать эти интерфейсы для управления шаблонами расположений параметров из Windows PowerShell и автоматизации задач администрирования шаблонов.

**Управление шаблонами расположений параметров с помощью WMI**

1.  Используйте учетную запись с правами администратора, чтобы открыть окно Windows PowerShell.

2.  Используйте следующие команды WMI для регистрации и управления шаблонами расположений параметров UE-V.

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
    <td align="left"><p>Get-WmiObject-Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId, TemplateName, TemplateVersion, Enabled | Форматирование таблицы с автоподбором</p></td>
    <td align="left"><p>Список всех шаблонов расположений параметров, зарегистрированных на компьютере.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-ArgumentList &lt; путь к шаблону&gt;</p></td>
    <td align="left"><p>Регистрирует шаблон расположения параметров с UE-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name UnregisterByTemplateId-ArgumentList &lt; ID шаблона&gt;</p></td>
    <td align="left"><p>Отмена регистрации шаблона расположения параметров с UE-V. После отмены регистрации шаблона UE-V больше не будет синхронизировать параметры, определенные в шаблоне, между компьютерами.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name EnableByTemplateId-ArgumentList &lt; ID шаблона&gt;</p></td>
    <td align="left"><p>Включает шаблон расположений параметров с UE-V</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name DisableByTemplateId-ArgumentList &lt; ID шаблона&gt;</p></td>
    <td align="left"><p>Отключает шаблон расположения параметров с UE-V</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name ArgumentList — &lt; путь к шаблону&gt;</p></td>
    <td align="left"><p>Обновляет шаблон расположений параметров с UE-V. Новый шаблон должен иметь более позднюю версию, чем существующий.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Validate-ArgumentList &lt; путь к шаблону&gt;</p></td>
    <td align="left"><p>Определяет, соответствует ли указанный шаблон расположению параметров своей XML-схеме.</p></td>
    </tr>
    </tbody>
    </table>

     

**Развертывание агента UE-V с помощью PowerShell**

1.  Поэтапный файл установщика UE-V в общедоступном сетевом общем доступе.

    **Примечание**  Используйте AgentSetup.exe для развертывания 32-и 64-разрядных версий агента UE-V Agent. Для каждой архитектуры доступны файлы установщика Windows версии, AgentSetupx86.msi и AgentSetupx64.msi. Чтобы позднее удалить агент UE-V с помощью файла установки, необходимо использовать тот же тип файлов.

     

2.  Для установки агента используйте одну из следующих команд PowerShell.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## Статьи по теме


[Управление агентом и пакетами UE-V 1.0 с помощью PowerShell и инструментария WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[Администрирование UE-V 1.0](administering-ue-v-10.md)

[Операции в UE-V 1.0](operations-for-ue-v-10.md)

 

 





