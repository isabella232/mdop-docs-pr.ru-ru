---
title: Развертывание агента UE-V
description: Развертывание агента UE-V
author: dansimp
ms.assetid: ec1c16c4-4be0-41ff-93bc-3e2b1afb5832
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 19f3b798ad7d3a43b0a274a25dd97b651435de51
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827182"
---
# Развертывание агента UE-V


Агент Microsoft User Experience Virtualization (UE-V) Agent должен выполняться на каждом компьютере, использующем UE-V для перемещения приложений и параметров Windows. Один файл установщика, AgentSetup.exe, устанавливает агент UE-V Agent как в 32-разрядной, так и в 64-разрядной операционной системе. Для агента UE-V используются следующие параметры командной строки:

**Параметры командной строки AgentSetup.exe**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Параметр командной строки</strong></th>
<th align="left"><strong>Определение</strong></th>
<th align="left"><strong>Заметки</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Help или/h или/?</p></td>
<td align="left"><p>Отображает диалоговое окно "использование AgentSetup.exe".</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsStoragePath</p></td>
<td align="left"><p>Указывает путь UNC (Universal Naming Convention), который определяет, где хранятся параметры.</p></td>
<td align="left"><p>% Username% или% ComputerName% принимают переменные среды. Для выполнения сценариев могут потребоваться переменные с экранированием.</p>
<p><strong>По умолчанию </strong> : &lt; нет &gt; (Домашняя страница пользователя Active Directory)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SettingsTemplateCatalogPath</p></td>
<td align="left"><p>Указывает путь UNC, определяющий расположение, которое было проверено для новых шаблонов расположений параметров.</p></td>
<td align="left"><p>Требуется только для шаблонов местоположения настраиваемых параметров</p></td>
</tr>
<tr class="even">
<td align="left"><p>RegisterMSTemplates</p></td>
<td align="left"><p>Указывает, следует ли регистрировать шаблоны Microsoft по умолчанию во время установки.</p></td>
<td align="left"><p>Истина | False</p>
<p><strong>По умолчанию </strong> : истина</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerSchool</p></td>
<td align="left"><p>Указывает, какой метод синхронизации следует использовать.</p></td>
<td align="left"><p>OfflineFiles | Ничего</p>
<p><strong>По умолчанию </strong> : OfflineFiles</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncTimeoutInMilliseconds</p></td>
<td align="left"><p>Задает время ожидания (в миллисекундах), по истечении которого компьютер извлекает параметры пользователя из места хранения параметров.</p></td>
<td align="left"><p><strong>По умолчанию </strong> : 2000 миллисекунд</p>
<p>(подождите до двух секунд)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncEnabled</p></td>
<td align="left"><p>Указывает, включена или отключена синхронизация UE-V.</p></td>
<td align="left"><p>Истина | False</p>
<p><strong>По умолчанию </strong> : истина</p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPackageSizeInBytes</p></td>
<td align="left"><p>Задает размер файла пакета параметров в байтах, когда агент UE-V сообщает, что файлы превышают пороговое значение.</p></td>
<td align="left"><p>&lt;Емкость&gt;</p>
<p><strong>По умолчанию </strong> : нет (порог предупреждения отсутствует)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CEIPEnabled</p></td>
<td align="left"><p>Указывает параметр для участия в программе улучшения качества программного обеспечения. Если установлено значение true, сведения об установщике загружаются на сайт программы улучшения качества программного обеспечения Майкрософт. Если задано значение false, сведения не передаются.</p></td>
<td align="left"><p>Истина | False</p>
<p><strong>По умолчанию </strong> : ложь</p>
<p><strong>В Windows 7 </strong> : истина</p></td>
</tr>
</tbody>
</table>

 

Во время установки параметр командной строки SettingsStoragePath указывает место хранения параметров для значений параметров. Место хранения параметров может быть определено перед развертыванием агента UE-V. Если расположение хранилища параметров не определено, UE-V использует домашний каталог пользователя Active Directory в качестве места хранения параметров. Когда вы указываете конфигурацию SettingsStoragePath во время настройки и используете% username% как часть значения, этот параметр будет перемещаться на всех компьютерах или сеансах, в которых пользователь входит в систему. Если указать переменные%username%\\%ComputerName% в качестве части значения SettingsStoragePath, это сохранит параметры для каждого компьютера.

Файлы установщика Windows (MSI), зависящие от архитектуры, предоставляются для установки агента UE-V в дополнение к Объединенному установщику 32-и 64-разрядной версии. Файлы установки AgentSetupx86.msi или AgentSetupx64.msi меньше файла AgentSetup.exe и могут ускорить развертывание агента. Параметры командной строки для установщика AgentSetup.exe поддерживаются для установки установщика Windows (MSI).

**Примечание**  При установке или удалении агента UE-V вы можете либо использовать файл AgentSetup.exe, либо &lt; файл AgentSetup Arch &gt; . msi, но не оба варианта. Один и тот же файл необходимо использовать для удаления агента UE-V, так как он использовался для установки UE-V Agent.

 

Убедитесь, что при установке агента UE-V используется правильный формат переменной. В таблице ниже приведены примеры параметров развертывания для использования AgentSetup.exe или установочных файлов установщика Windows (MSI).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Тип развертывания</strong></th>
<th align="left"><strong>Описание развертывания</strong></th>
<th align="left"><strong>Пример.</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Командная строка</p></td>
<td align="left"><p>При установке агента UE-V из командной строки используйте формат переменной% ^ username%. Если кавычки необходимы из-за пробелов в пути к хранилищу параметров, используйте файл пакетного сценария для развертывания.</p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Пакетный сценарий</p></td>
<td align="left"><p>При установке агента UE-V из пакетного файла сценария используйте формат переменной%% username%%. Если вы используете этот метод установки, необходимо обменять переменную символом%%. Без этого символа сценарий разворачивает переменную username во время установки, а не во время выполнения, что приводит к тому, что UE-V использует единое хранилище параметров для всех пользователей.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>При установке агента UE-V из запроса PowerShell или сценария PowerShell используйте формат переменной% username%.</p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Электронное распространение программного обеспечения, например развертывание программного обеспечения Configuration Manager.</p></td>
<td align="left"><p>При установке агента UE-V с помощью Configuration Manager используйте формат переменной ^% username ^%.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

**Примечание**  Установка агента U-EV требует наличия прав администратора, и перед запуском агента UE-V может потребоваться перезагрузка компьютера.

 

## Методы развертывания агента UE-V из общей сетевой папке


Для развертывания агента UE-V можно использовать следующие методы:

-   Решение для электронного распространения программного обеспечения, позволяющее установить файл установщика Windows (MSI).

-   Сценарий установки, который ссылается на файл установщика Windows (MSI), хранящийся централизованно в общем доступе.

-   Запуск программы установки на компьютере вручную.

Чтобы развернуть агент UE-V из сетевого общего доступа, выполните указанные ниже действия.

**Установка и настройка агента UE-V для сетевого общего доступа**

1.  Поэтапный файл установки агента UE-V (AgentSetup.exe) в сетевой папке, для которой пользователи имеют разрешение на чтение.

2.  Разверните сценарий на компьютерах пользователей, которые установили агент UE-V Agent. В сценарии должно быть указано место хранения параметров.

**Обновление агента UE-V**

Обновления программного обеспечения агента UE-V будут предоставляться с помощью центра обновления Майкрософт. Во время обновления агента UE-V можно обновить стандартную группу шаблонов расположений параметров для приложений Майкрософт и параметров Windows. Обновления агента UE-V можно развертывать с помощью инфраструктуры для распространения программного обеспечения (ESD) предприятия.

## Статьи по теме


[Развертывание UE-V 1.0](deploying-ue-v-10.md)

[Поддерживаемые конфигурации UE-V 1.0](supported-configurations-for-ue-v-10.md)

[Развертывание места хранения параметров для UE-V 1.0](deploying-the-settings-storage-location-for-ue-v-10.md)

[Установка генератора UE-V](installing-the-ue-v-generator.md)

Развертывание агента виртуализации взаимодействия с пользователем
 

 





