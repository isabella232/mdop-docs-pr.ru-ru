---
title: Запуск локально установленного приложения в виртуальной среде с виртуализированными приложениями
description: Запуск локально установленного приложения в виртуальной среде с виртуализированными приложениями
author: dansimp
ms.assetid: 71baf193-a9e8-4ffa-aa7f-e0bffed2e4b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 384a1325b2f363595971f70f25fe0a25cade448d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813296"
---
# Запуск локально установленного приложения в виртуальной среде с виртуализированными приложениями


Локально установленное приложение можно запускать в виртуальной среде вместе с приложениями, которые были виртуализированы с помощью Microsoft Application Virtualization (App-V). Это может потребоваться, если:

-   Вы хотите установить и запустить приложение локально на клиентских компьютерах, но вы хотите виртуализировать и запустить специальные подключаемые модули, которые работают с этим локальным приложением.

-   Устранены неполадки с пакетом клиента App-V и нужно открыть локальное приложение в виртуальной среде App-V.

Используйте один из следующих методов, чтобы открыть локальное приложение в виртуальной среде App-V:

-   [Раздел реестра RunVirtual](#bkmk-runvirtual-regkey)

-   [Командлет PowerShell Get-AppvClientPackage](#bkmk-get-appvclientpackage-posh)

-   [Параметр командной строки/appvpid: &lt; PID&gt;](#bkmk-cl-switch-appvpid)

-   [/Appvve переключателя командной строки: &lt; GUID&gt;](#bkmk-cl-hook-switch-appvve)

Каждый метод выполняется по сути одной задачи, но некоторые из них могут быть более подходящими для некоторых приложений, чем другие, в зависимости от того, выполняется ли уже виртуализированное приложение.

## <a href="" id="bkmk-runvirtual-regkey"></a>Раздел реестра RunVirtual


Чтобы добавить локально установленное приложение в пакет или в виртуальную среду для группы подключения, добавьте подраздел в раздел `RunVirtual` реестра в редакторе реестра, как описано в следующих разделах.

Для управления этим разделом реестра не доступен параметр групповой политики, поэтому необходимо использовать System Center Configuration Manager или другую электронную рассылку программного обеспечения или изменить реестр вручную.

### <a href="" id="bkmk-"></a>Поддерживаемые методы публикации пакетов при использовании RunVirtual

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Версия App-V</th>
<th align="left">Поддерживаемые методы публикации</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 с пакетом обновления 3 (SP3) и App-V 5,1</p></td>
<td align="left"><p>Опубликовано глобально или для пользователей</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5,0 – App-V 5,0 SP2</p></td>
<td align="left"><p>Опубликовано глобально</p></td>
</tr>
</tbody>
</table>

 

### Действия по созданию подраздела

1.  Используя сведения из приведенной ниже таблицы, создайте новый раздел реестра, используя имя исполняемого файла, например **MyApp.exe**.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Метод публикации пакета</th>
    <th align="left">Создание раздела реестра</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Опубликовано глобально</p></td>
    <td align="left"><p>HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\RunVirtual</p>
    <p><strong>Пример </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Опубликовано для пользователя</p></td>
    <td align="left"><p>HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual</p>
    <p><strong>Пример </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Группа подключения может содержать:</p>
    <ul>
    <li><p>Пакеты, публикуемые только глобально или только для пользователей</p></li>
    <li><p>Пакеты, опубликованные глобально и для пользователей</p></li>
    </ul></td>
    <td align="left"><p>HKEY_LOCAL_MACHINE или HKEY_CURRENT_USER Key, но все перечисленные ниже условия должны быть истинными.</p>
    <ul>
    <li><p>Если вы хотите включить в виртуальную среду несколько пакетов, необходимо включить их в группу разрешенных подключений.</p></li>
    <li><p>Создайте только один подраздел для одного из пакетов в группе подключение. Например, если у вас есть один пакет, который опубликован глобально, и другой пакет, опубликованный для пользователя, вы можете создать подраздел для любого из этих пакетов, но не оба. Несмотря на то, что вы создаете подраздел только для одного из пакетов, все пакеты в группе подключения и локальное приложение будут доступны в виртуальной среде.</p></li>
    <li><p>Ключ, под которым создается подраздел, должен соответствовать методу публикации, который вы использовали для пакета.</p>
    <p>Например, если вы опубликовали пакет для пользователя, вы должны создать подраздел в разделе <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  Задайте для нового раздела реестра значение PackageId и VersionId пакета, отделив значения с помощью подчеркивания.

    **Синтаксис**: &lt; PackageId &gt; \ _ &lt; VersionId&gt;

    **Пример**: 4c909996-afc9-4352-b606-0b74542a09c1 \ _Be463724-Oct1-48f1-8604-c4bd7ca92fa

    Приложение в предыдущем примере создаст файл экспорта реестра (REG-файл), как показано ниже.

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a>Командлет PowerShell Get-AppvClientPackage


С помощью командлета **Start-AppVVirtualProcess** можно получить имя пакета, а затем запустить процесс в виртуальной среде указанного пакета. Этот метод позволяет запускать любую команду в контексте пакета App-V, независимо от того, выполняется ли в данный момент пакет.

Используйте приведенный ниже пример синтаксиса и подставьте имя пакета для ** &lt; пакета &gt; **:

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

Если вы не знаете точное имя пакета, вы можете использовать командную строку **Get-AppvClientPackage \ * executable\\** <em> , где ** </em> Executable* — это имя приложения, например: Get-AppvClientPackage \ * Word \ *.

## <a href="" id="bkmk-cl-switch-appvpid"></a>Параметр командной строки/appvpid: &lt; PID&gt;


Вы можете применить к любой команде параметр **/appvpid: &lt; PID &gt; ** , который позволяет выполнить эту команду в виртуальном процессе, который вы выбираете, УКАЗАВ его идентификатор (PID). При использовании этого метода запускается новый исполняемый файл в той же среде App-V, что и уже запущенный исполняемый файл.

Пример. `cmd.exe /appvpid:8108`

Чтобы найти идентификатор процесса (PID) своего процесса App-V, выполните команду **tasklist.exe** из командной строки с повышенными привилегиями.

## <a href="" id="bkmk-cl-hook-switch-appvve"></a>/Appvve переключателя командной строки: &lt; GUID&gt;


С помощью этого переключателя вы можете выполнить локальную команду в виртуальной среде пакета App-V. В отличие от ключа **/appvid** , где виртуальная среда должна быть уже запущена, этот параметр позволяет запустить виртуальную среду.

Максимальное `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

Пример. `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

Чтобы получить GUID пакета и идентификатор GUID версии вашего приложения, выполните командлет **Get-AppvClientPackage** . Объедините переключатель **/appvve** следующим образом:

-   Двоеточие

-   Идентификатор GUID пакета для нужного пакета

-   Подчеркивание

-   НОМЕР версии требуемого пакета

Если вы не знаете точное имя пакета, используйте командную строку **Get-AppvClientPackage \ * executable\\** <em> , где ** </em> Executable* — это имя приложения, например: Get-AppvClientPackage \ * Word \ *.

Этот метод позволяет запускать любую команду в контексте пакета App-V, независимо от того, выполняется ли в данный момент пакет.






## Статьи по теме


[Технический справочник для App-V 5.1](technical-reference-for-app-v-51.md)

 

 





