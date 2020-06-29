---
title: Управление шаблонами расположений параметров UE-V 2. x с помощью Windows PowerShell и WMI
description: Управление шаблонами расположений параметров UE-V 2. x с помощью Windows PowerShell и WMI
author: dansimp
ms.assetid: b5253050-acc3-4274-90d0-1fa4c480331d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9788ff1a11f1c70e52b75dd2187a198f5472f77f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812880"
---
# Управление шаблонами расположений параметров UE-V 2. x с помощью Windows PowerShell и WMI


Виртуализация взаимодействия с пользователем Microsoft (UE-V) 2,0, 2,1 и 2,1 SP1 используют шаблоны расположения XML-параметров для определения параметров, которые захватывает и применяется виртуализация пользователя. UE-V включает набор стандартных шаблонов расположений параметров. Кроме того, оно включает в себя средство для создания настраиваемых шаблонов расположения параметров с помощью UE-V Generator. После создания и развертывания шаблонов расположений параметров можно управлять этими шаблонами с помощью Windows PowerShell и инструментария управления Windows (WMI). Полный список командлетов PowerShell для UE-V можно найти в [справочнике по командлетам UE-v 2](https://go.microsoft.com/fwlink/p/?LinkId=393495) ( https://go.microsoft.com/fwlink/p/?LinkId=393495) .

## Управление шаблонами расположений параметров UE-V 2 с помощью Windows PowerShell


Возможности WMI и Windows PowerShell для UE-V включают возможность включать, отключать, регистрировать, обновлять и отменять регистрацию шаблонов расположений параметров. С помощью этих функций вы можете автоматизировать процесс регистрации, обновления и отмены регистрации шаблонов с помощью агента UE-V Agent. Вы также можете вручную зарегистрировать шаблоны с помощью WMI и команд Windows PowerShell. С помощью этих функций в сочетании с электронным решением для распространения программного обеспечения, групповой политикой или другим методом автоматического развертывания, таким как сценарий, вы можете автоматизировать этот процесс.

Для обновления, регистрации и отмены регистрации шаблона расположений параметров необходимы разрешения администратора. Для включения, отключения и использования шаблонов списков не требуются разрешения администратора.

***<em>Управление шаблонами расположений параметров с помощью Windows PowerShellell</em>***

1.  Используйте учетную запись с правами администратора, чтобы открыть командную команду Windows PowerShell.

2.  Используйте указанные ниже командлеты Windows PowerShell для регистрации и управления шаблонами расположений параметров UE-V.

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
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p>Список всех шаблонов расположений параметров, зарегистрированных на компьютере.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p>Перечисляются все шаблоны расположений параметров, которые зарегистрированы на компьютере, где имя приложения или шаблона содержит &lt; строку &gt; .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p>Перечисляются все шаблоны расположений параметров, которые зарегистрированы на компьютере, где идентификатор шаблона содержит &lt; строку &gt; .</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p>Перечисляются все шаблоны расположений параметров, которые зарегистрированы на компьютере, где имя приложения или шаблона или идентификатор шаблона содержат &lt; строку &gt; .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Получает имя программы и сведения о версии, которые зависят от идентификатора шаблона.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p>Получает эффективный список приложений для Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p>Получает список приложений Windows, настроенных для компьютера.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>Получает список приложений для Windows, которые настроены для текущего пользователя.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Регистрирует один или несколько шаблонов расположений параметров с UE-V с помощью относительных путей и (или) подстановочных знаков в путях к файлам. После регистрации шаблона UE-V синхронизирует параметры, определенные в шаблоне, между компьютерами с зарегистрированным шаблоном.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Регистрирует один или несколько шаблонов расположений параметров с UE-V с помощью литеральных путей, где ни один из символов не может интерпретироваться как подстановочные знаки. После регистрации шаблона UE-V синхронизирует параметры, определенные в шаблоне, между компьютерами с зарегистрированным шаблоном.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Отмена регистрации шаблона расположения параметров с UE-V. При отмене регистрации шаблона UE-V больше не синхронизирует параметры, определенные в шаблоне, между компьютерами.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p>Отмена регистрации всех шаблонов расположений параметров с UE-V. При отмене регистрации шаблона UE-V больше не синхронизирует параметры, определенные в шаблоне, между компьютерами.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Обновляет один или несколько шаблонов расположений параметров с более поздней версией шаблона. Используйте относительные пути и (или) подстановочные знаки в путях к файлам. Новый шаблон должен иметь более новую версию, чем существующий шаблон.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Обновляет один или несколько шаблонов расположений параметров с более поздней версией шаблона. Используйте полные пути к файлам шаблонов, в которых нельзя интерпретировать символы как подстановочные знаки. Новый шаблон должен иметь более новую версию, чем существующий шаблон.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Удаление одного или нескольких приложений для Windows из списка компьютеров приложений Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>Удаляет приложение для Windows из списка текущих приложений пользователя Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p>Удаляет все приложения для Windows из списка компьютеров приложений Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Удаляет одно или несколько приложений для Windows из текущего пользователя в списке приложений Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p>Удаляет все приложения для Windows из списка текущих приложений пользователя Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Отключает шаблон расположения параметров для текущего пользователя компьютера.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Отключение одного или нескольких приложений для Windows в списке приложений Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Отключение одного или нескольких приложений для Windows в текущем списке приложений пользователя Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Включает шаблон расположения параметров для текущего пользователя компьютера.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Включает одно или несколько приложений для Windows в списке приложений Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Включает одно или несколько приложений для Windows в списке приложений для Windows текущего пользователя.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Определяет соответствие одного или нескольких шаблонов расположению параметров с XML-схемой. Может использовать относительные пути и подстановочные знаки.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Определяет соответствие одного или нескольких шаблонов расположению параметров с XML-схемой. Путь должен представлять собой полный путь к файлу шаблона, но не содержит подстановочных знаков.</p></td>
    </tr>
    </tbody>
    </table>



Функции UE-V Windows PowerShell позволяют управлять группой шаблонов параметров, которые развернуты в Организации. Чтобы управлять группой шаблонов с помощью Windows PowerShell, выполните указанные ниже действия.

**Управление группой шаблонов расположений параметров с помощью Windows PowerShell**

1.  Измените или обновите шаблоны расположения нужных параметров.

2.  Если вы хотите изменить или обновить шаблоны расположений параметров, разверните эти шаблоны расположений в папку, доступную на локальном компьютере.

3.  На локальном компьютере откройте окно Windows PowerShell с правами администратора.

4.  Отмените регистрацию всех ранее зарегистрированных версий шаблонов, введя указанную ниже команду.

    ``` syntax
    Unregister-UevTemplate -All
    ```

    Эта команда отменяет регистрацию всех активных шаблонов на компьютере.

5.  Зарегистрируйте обновленные шаблоны, введя указанную ниже команду.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    Эта команда регистрирует все шаблоны расположений параметров, которые находятся в указанной папке шаблона.

### <a href="" id="win8applist"></a>Список приложений для Windows

Заполнив список приложений для Windows в списке приложений для Windows, вы указываете, будет ли это приложение включено или отключено для синхронизации параметров. Приложения определяются в списке по их названию семейства пакетов и следует ли включать или отключать синхронизацию параметров для этого приложения. При использовании этих параметров вместе с параметром "непоставленный режим синхронизации по умолчанию" можно управлять синхронизацией приложений для Windows.

Чтобы отобразить имя семейства пакетов установленных приложений для Windows, в командной строке Windows PowerShell введите:

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

Чтобы отобразить список приложений для Windows, которые могут синхронизировать параметры на компьютере с именем семейства пакетов, включенным состоянием и включенным источником, в командной строке Windows PowerShell введите: `Get-UevAppxPackage`

**Определения свойств Get-UevAppxPackage**

<a href="" id="displayname"></a>**DisplayName**  
Имя, которое отображается для пользователя в приложении центра параметров компании. `DisplayName`Свойство является производным от `PackageFamilyName` Свойства.

<a href="" id="packagefamilyname"></a>**PackageFamilyName**  
Имя пакета, установленного для текущего пользователя.

<a href="" id="enabled"></a>**Включено**  
Определяет, настроены ли параметры для приложения для синхронизации.

<a href="" id="enabledsource"></a>**EnabledSource**  
Расположение, в котором задана конфигурация, включающая или отключающее приложение. Возможные значения: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*и *PolicyUser*.

<a href="" id="notset"></a>**NotSet (Не задано)**  
Политика не настроена для синхронизации этого приложения.

<a href="" id="localmachine"></a>**Хранилище**  
Включенное состояние задается в разделе реестра на локальном компьютере.

<a href="" id="localuser"></a>**LocalUser**  
Включенное состояние задается в разделе реестра текущего пользователя.

<a href="" id="policymachine"></a>**PolicyMachine**  
Включенное состояние задается в разделе Политика раздела локальный компьютер в реестре.

Чтобы получить список приложений для Windows, настраиваемый пользователем, в командной строке Windows PowerShell введите: `Get-UevAppxPackage –CurrentComputerUser`

Чтобы получить список приложений для Windows, настроенный на компьютере, в командной строке Windows PowerShell введите: `Get-UevAppxPackage –Computer`

Для параметра CurrentComputerUser или Computer командлет возвращает список приложений для Windows, которые настроены на уровне пользователя или компьютера.

**Определения свойств**

<a href="" id="displayname"></a>**DisplayName**  
Имя, которое отображается для пользователя в приложении центра параметров компании. `DisplayName`Свойство является производным от `PackageFamilyName` Свойства.

<a href="" id="packagefamilyname"></a>**PackageFamilyName**  
Имя пакета, установленного для текущего пользователя.

<a href="" id="enabled"></a>**Включено**  
Определяет, настроены ли параметры для приложения для синхронизации определенного коммутатора, то есть **пользователя** или **компьютера**.

<a href="" id="installed"></a>**Установлено**  
Значение true, если приложение (например, PackageFamilyName установлен для текущего пользователя).

### Управление шаблонами расположений параметров UE-V 2 с помощью WMI

Виртуализация взаимодействия с пользователем предоставляет следующий набор команд WMI. Администраторы могут использовать эти интерфейсы для управления шаблонами расположений параметров из Windows PowerShell и автоматизации задач администрирования шаблонов.

**Управление шаблонами расположений параметров с помощью WMI**

1.  Используйте учетную запись с правами администратора, чтобы открыть окно Windows PowerShell.

2.  Используйте следующие команды WMI для регистрации и управления шаблонами расположений параметров UE-V.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left">Описание</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p>Список всех шаблонов расположений параметров, зарегистрированных для компьютера.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p>Получает имя программы и сведения о версии, которые зависят от имени шаблона.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p>Получает эффективный список приложений для Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-WmiObject-Namespace root\Microsoft\UEV MachineConfiguredWindows8App</p></td>
    <td align="left"><p>Получает список приложений Windows, настроенных для компьютера.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p>Получает список приложений для Windows, которые настроены для текущего пользователя.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p>Регистрирует шаблон расположения параметров с UE-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Отмена регистрации шаблона расположения параметров с UE-V. После отмены регистрации шаблона UE-V больше не синхронизирует параметры, определенные в шаблоне, между компьютерами.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>Обновляет шаблон расположений параметров с UE-V. Новый шаблон должен иметь более новую версию, чем существующий.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Удаление одного или нескольких приложений для Windows из списка компьютеров приложений Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Удаляет одно или несколько приложений для Windows из текущего пользователя в списке приложений Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Отключает один или несколько шаблонов расположений параметров с UE-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Отключение одного или нескольких приложений для Windows в списке приложений Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Отключение одного или нескольких приложений для Windows в текущем списке приложений пользователя Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Включает шаблон расположений параметров с UE-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Включает приложения для Windows в списке приложений Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Позволяет приложениям для Windows в списке приложений для Windows текущего пользователя.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>Определяет, соответствует ли указанный шаблон расположению параметров своей XML-схеме.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### Развертывание агента UE-V с помощью Windows PowerShell

**Развертывание агента UE-V с помощью Windows PowerShell**

1.  Поэтапный пакет установки агента UE-V в общедоступном сетевом общем доступе.

    **Примечание.**  
    Используйте AgentSetup.exe для развертывания 32-и 64-разрядных версий агента UE-V Agent. Для каждой архитектуры доступны пакеты установщика Windows, AgentSetupx86.msi и AgentSetupx64.msi. Чтобы позднее удалить агент UE-V с помощью файла установки, необходимо использовать тот же тип файлов.



2.  Используйте одну из следующих команд Windows PowerShell, чтобы установить агент UE-V Agent.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**У вас есть предложение UE-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **У вас возникла ошибка UE-V**? Воспользуйтесь [форумом на сайте UE-V TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Статьи по теме


[Администрирование UE-V 2. x с помощью Windows PowerShell и WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Администрирование UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









