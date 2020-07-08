---
title: Сведения о динамической конфигурации App-V 5.0
description: Сведения о динамической конфигурации App-V 5.0
author: dansimp
ms.assetid: 88afaca1-68c5-45c4-a074-9371c56b5804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0294a60570d6dea99193c8bd411639c4888ae6b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815032"
---
# Сведения о динамической конфигурации App-V 5.0


Вы можете использовать динамическую конфигурацию для настройки пакета App-V 5,0 для пользователя. Используйте следующие сведения для создания или изменения существующего файла динамической конфигурации.

При изменении файла динамической конфигурации выполняется настройка того, как будет выполняться пакет App-V 5,0 для пользователя или группы. Это поможет вам создать более удобный способ для настройки пакета, изменив необходимость повторной последовательности пакетов с использованием нужных параметров и обеспечивая независимый способ хранения содержимого пакета и пользовательских параметров.

## Дополнительно: Динамическая настройка


Пакеты виртуальных приложений содержат манифест, который предоставляет все основные сведения о пакете. Эти сведения включают значения по умолчанию для параметров пакета и определяют параметры в самой простой форме (без дополнительной настройки). Если вы хотите изменить эти значения по умолчанию для определенного пользователя или группы, вы можете создавать и изменять следующие файлы:

-   Файл конфигурации пользователя

-   Файл конфигурации развертывания

В предыдущих XML-файлах задаются параметры пакета и разрешаются настраиваемые пакеты, не влияя на пакеты напрямую. При создании пакета секвенсор автоматически создает XML-файлы развертывания и конфигурации пользователя по умолчанию с помощью данных манифеста пакета. Таким образом, эти автоматически создаваемые файлы конфигурации отражают параметры по умолчанию, которые пакет по определению не так, как элементы были настроены во время последовательности. Если вы применяете эти файлы конфигурации к пакету в форме, созданной секвенсором, пакеты будут иметь те же параметры по умолчанию, которые поставляются из манифеста. Таким образом, вы получите шаблон для определенного пакета, чтобы приступить к работе, если нужно изменить любое из значений по умолчанию.

**Примечание**  Приведенные ниже сведения можно использовать только для настройки файлов конфигурации секвенсоров, чтобы настроить пакеты для обеспечения конкретных требований пользователей или групп.

 

### Содержимое файла динамической конфигурации

Все добавления, удаления и обновления в файлах конфигурации должны быть связаны со значениями по умолчанию, заданными в манифесте пакета. Ознакомьтесь с приведенной ниже таблицей.

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Файл Configuration. XML пользователя</p></td>
</tr>
<tr class="even">
<td align="left"><p>XML-файл конфигурации развертывания</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Манифест пакета</p></td>
</tr>
</tbody>
</table>

 

В предыдущей таблице показано, как будут прочитаны файлы. Первый элемент показывает, что будет считаться последним, поэтому его содержимое имеет приоритет. Таким образом, все пакеты по сути содержат параметры по умолчанию из манифеста пакета. Если применяется XML-файл конфигурации развертывания с настроенными параметрами, он будет переопределять параметры манифеста пакета по умолчанию. Если файл Configuration. XML с настроенными параметрами применяется до этого, он переопределит конфигурацию развертывания и параметры манифеста пакета по умолчанию.

В списке ниже приведены дополнительные сведения о двух типах файлов.

-   **Файл конфигурации пользователя (UserConfig)** — позволяет указать или изменить пользовательские параметры для пакета. Эти параметры будут применяться к определенному пользователю при развертывании пакета на компьютере, на котором запущен клиент App-V 5,0.

-   **Файл конфигурации развертывания (DEPLOYMENTCONFIG)** — позволяет указать или изменить параметры пакета по умолчанию. Эти параметры будут применяться ко всем пользователям при развертывании пакета на компьютере с клиентским приложением App-V 5,0.

Чтобы настроить параметры для пакета для определенного набора пользователей на компьютере или внести изменения, которые будут применяться к локальным расположениям пользователей, таким как HKCU, следует использовать файл UserConfig. Чтобы изменить параметры пакета по умолчанию для всех пользователей на компьютере или внести изменения, которые будут применяться к глобальным расположениям, например HKEY \ _LOCAL \ _MACHINE и папке All Users, следует использовать файл DeploymentConfig.

Файл UserConfig предоставляет параметры конфигурации, которые можно применять для одного пользователя, не затрагивая других пользователей на клиенте:

-   Расширения, которые будут интегрированы в собственную систему на каждого пользователя:-сочетания, типы файлов, протоколы URL-адресов, AppPaths, клиенты и COM

-   Виртуальные подсистемы: объекты приложения, переменные среды, изменения в реестре, службы и шрифты

-   Сценарии (только для контекста пользователя)

-   Управление полномочиями (для управления сосуществованием пакета с помощью App-V 4,6)

Файл DeploymentConfig предоставляет параметры конфигурации в двух разделах, один из которых относится к контексту компьютера, а другой — к контексту пользователя, который предоставляет те же возможности, которые указаны в списке UserConfig выше:

-   Все указанные выше параметры UserConfig

-   Расширения, применимые только глобально для всех пользователей

-   Виртуальные подсистемы, которые можно настроить для глобальных компьютеров, например Registry

-   URL-адрес источника продукта

-   Сценарии (только для контекста компьютера)

-   Элементы управления для завершения дочерних процессов

### Структура файла

Структура файла динамической конфигурации App-V 5,0 описана в следующем разделе.

### Файл динамической конфигурации пользователя

**Заголовок** — заголовок динамического пользовательского файла конфигурации выглядит следующим образом:

&lt;? XML Version = "1.0" Encoding = "UTF-8"? &gt; &lt; UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

**PackageId** имеет то же значение, которое существует в файле манифеста.

**Body** — тело файла динамической конфигурации пользователя может включать все точки расширения приложения, определенные в файле манифеста, а также данные для настройки виртуальных приложений. В тексте сообщения можно использовать четыре подраздела.

1. **Приложения** — все расширения приложения, которые содержатся в файле манифеста в пакете, НАЗНАЧАЮТся идентификатору приложения, который также определен в файле манифеста. Это позволяет включать или отключать все расширения для данного приложения в пакете. **Идентификатор приложения** должен существовать в файле манифеста, или он будет игнорироваться.

   &lt;UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

   &lt;Приложения&gt;

   &lt;!--В политике не может быть определено новое приложение. Клиент службы AppV будет игнорировать любые ИДЕНТИФИКАТОРы приложения, которые также не находятся в файле манифеста--&gt;

   &lt;Приложение ID = "{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled = "false"&gt;

   &lt;/Application&gt;

   &lt;/Applications&gt;

   …

   &lt;/UserConfiguration&gt;

2. **Подсистемы** — AppExtensions и другие подсистемы размещаются как подузлы в &lt; подсистемах &gt; .

   &lt;UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

   &lt;Подсистем&gt;

   ..

   &lt;/Subsystems&gt;

   ..

   &lt;/UserConfiguration&gt;

   Каждая подсистема может быть включена или отключена с помощью атрибута**Enabled**. Ниже указаны различные подсистемы и примеры использования.

   **MIME**

   Некоторые подсистемы (расширения элементов управления доподсистемой). К этим подсистемам присвоены следующие подсистемы: сочетания клавиш, сопоставления типов файлов, протоколы URL-адресов, AppPaths, клиенты программного обеспечения и COM

   Подсистемы расширения можно включать и отключать независимо от содержимого.  Таким образом, если включены сочетания клавиш, клиент будет по умолчанию использовать сочетания клавиш, содержащиеся в манифесте. Каждая подсистема расширения может содержать &lt; узел Extensions &gt; . Если этот дочерний элемент присутствует, клиент будет игнорировать содержимое файла манифеста для этой подсистемы и использовать только содержимое в файле конфигурации.

   Пример использования подсистемы сочетаний клавиш:

   1.  Если пользователь задали это значение в динамическом файле конфигурации:

                                    **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions&gt;**

                                                 ...

                                                **&lt;/Extensions&gt;**

                                    **&lt;/Shortcuts&gt;**

                         Content in the manifest will be ignored.   

   2.  Если пользователь задали следующие данные:

                                   **&lt;Shortcuts  Enabled="true"/&gt;**

                         Then the content in the Manifest will be integrated during publishing.

   3.  Если пользователь определяет указанные ниже

                                  **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions/&gt;**

                                    **&lt;/Shortcuts&gt;**

   В этом случае все сочетания клавиш в манифесте будут игнорироваться. Сочетания клавиш не будут интегрированы.

   Поддерживаются следующие подсистемы расширения.

   **Сочетания клавиш:** Этот элемент управления определяет сочетания клавиш, которые будут интегрированы в локальную систему. Ниже приведен пример с двумя сочетаниями клавиш:

   &lt;Подсистем&gt;

   &lt;Сочетания клавиш включены = "истина"&gt;

     &lt;Расширения&gt;

       &lt;Extension Category="AppV.Shortcut"&gt;

         &lt;Shortcut&gt;

           &lt;File&gt;\[{Common Programs}\]\\Microsoft Contoso\\Microsoft ContosoApp Filler 2010.lnk&lt;/File&gt;

           &lt;Target&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/Target&gt;

           &lt;Icon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\inficon.exe&lt;/Icon&gt;

           &lt;Arguments /&gt;

           &lt;WorkingDirectory /&gt;

           &lt;AppUserModelId&gt;ContosoApp.Filler.3&lt;/AppUserModelId&gt;

           &lt;Description&gt;Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.&lt;/Description&gt;

           &lt;Hotkey&gt;0&lt;/Hotkey&gt;

           &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

           &lt;ApplicationId&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/ApplicationId&gt;

         &lt;/Shortcut&gt;

     &lt;/Extension&gt;

     &lt;Extension Category = "AppV. shortcut"&gt;

       &lt;Shortcut&gt;

         &lt;File&gt;\[{AppData}\]\\Microsoft\\Contoso\\Recent\\Templates.LNK&lt;/File&gt;

         &lt;Target&gt;\[{AppData}\]\\Microsoft\\Templates&lt;/Target&gt;

         &lt;Icon /&gt;

         &lt;Arguments /&gt;

         &lt;WorkingDirectory /&gt;

         &lt;AppUserModelId /&gt;

         &lt;Description /&gt;

         &lt;Hotkey&gt;0&lt;/Hotkey&gt;

         &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

         &lt;!-- Note the ApplicationId is optional --&gt;

       &lt;/Shortcut&gt;

     &lt;/Extension&gt;

    &lt;/Extensions&gt;

   &lt;/Shortcuts&gt;

   **Сопоставления типов файлов:** Связывает типы файлов с программами, которые можно открывать по умолчанию, а также настройкой контекстного меню. (Типы MIME также можно настроить с помощью этого susbsystem). Пример сопоставления типов файлов ниже:

   &lt;FileTypeAssociations Enabled = "true"&gt;

   &lt;Расширения&gt;

     &lt;Расширение Category = "AppV. FileTypeAssociation"&gt;

       &lt;FileTypeAssociation&gt;

         &lt;FileExtension MimeAssociation="true"&gt;

         &lt;Name&gt;.docm&lt;/Name&gt;

         &lt;ProgId&gt;contosowordpad.DocumentMacroEnabled.12&lt;/ProgId&gt;

         &lt;PerceivedType&gt;document&lt;/PerceivedType&gt;

         &lt;ContentType&gt;application/vnd.ms-contosowordpad.document.macroEnabled.12&lt;/ContentType&gt;

         &lt;OpenWithList&gt;

           &lt;ApplicationName&gt;wincontosowordpad.exe&lt;/ApplicationName&gt;

         &lt;/OpenWithList&gt;

        &lt;OpenWithProgIds&gt;

           &lt;ProgId&gt;contosowordpad.8&lt;/ProgId&gt;

         &lt;/OpenWithProgIds&gt;

         &lt;ShellNew&gt;

           &lt;Command /&gt;

           &lt;DataBinary /&gt;

           &lt;DataText /&gt;

           &lt;FileName /&gt;

           &lt;NullFile&gt;true&lt;/NullFile&gt;

           &lt;ItemName /&gt;

           &lt;IconPath /&gt;

           &lt;MenuText /&gt;

           &lt;Handler /&gt;

         &lt;/ShellNew&gt;

       &lt;/FileExtension&gt;

       &lt;ProgId&gt;

          &lt;Name&gt;contosowordpad.DocumentMacroEnabled.12&lt;/Name&gt;

           &lt;DefaultIcon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\contosowordpadicon.exe,15&lt;/DefaultIcon&gt;

           &lt;Description&gt;Blah Blah Blah&lt;/Description&gt;

           &lt;FriendlyTypeName&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,9182&lt;/FriendlyTypeName&gt;

           &lt;InfoTip&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,1424&lt;/InfoTip&gt;

           &lt;EditFlags&gt;0&lt;/EditFlags&gt;

           &lt;ShellCommands&gt;

             &lt;DefaultCommand&gt;Open&lt;/DefaultCommand&gt;

             &lt;ShellCommand&gt;

                &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

                &lt;Name&gt;Edit&lt;/Name&gt;

                &lt;FriendlyName&gt;&Edit&lt;/FriendlyName&gt;

                &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /vu "%1"&lt;/CommandLine&gt;

             &lt;/ShellCommand&gt;

             &lt;/ShellCommand&gt;

               &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

               &lt;Name&gt;Open&lt;/Name&gt;

               &lt;FriendlyName&gt;&Open&lt;/FriendlyName&gt;

               &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /n "%1"&lt;/CommandLine&gt;

               &lt;DropTargetClassId /&gt;

               &lt;DdeExec&gt;

                 &lt;Application&gt;mscontosowordpad&lt;/Application&gt;

                 &lt;Topic&gt;ShellSystem&lt;/Topic&gt;

                 &lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;

                 &lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;

               &lt;/DdeExec&gt;

             &lt;/ShellCommand&gt;

           &lt;/ShellCommands&gt;

         &lt;/ProgId&gt;

        &lt;/FileTypeAssociation&gt;

      &lt;/Extension&gt;

     &lt;/Extensions&gt;

     &lt;/FileTypeAssociations&gt;

   **URL-протоколы**: управляет протоколами URL-адресов, которые интегрируются в локальный реестр клиентского компьютера, например "mailto:".

   &lt;URLProtocols Enabled = "true"&gt;

   &lt;Расширения&gt;

   &lt;Расширение Category = "AppV. URLProtocol"&gt;

   &lt;URLProtocol&gt;

     &lt;Name &gt; mailto &lt; /Name&gt;

     &lt;ApplicationURLProtocol&gt;

     &lt;DefaultIcon &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403 &lt; /defaultIcon&gt;

     &lt;EditFlags &gt; 2 &lt; /EditFlags&gt;

     &lt;Nописание&gt;

     &lt;AppUserModelId&gt;

     &lt;FriendlyTypeName /&gt;

     &lt;Плыв&gt;

   &lt;SourceFilter /&gt;

     &lt;ShellFolder /&gt;

     &lt;WebNavigableCLSID /&gt;

     &lt;ExplorerFlags &gt; 2 &lt; /ExplorerFlags&gt;

     &lt;CLSID&gt;

     &lt;ShellCommands&gt;

     &lt;DefaultCommand &gt; Open &lt; /DefaultCommand&gt;

     &lt;ShellCommand&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /applicationId&gt;

     &lt;Имя &gt; Open &lt; /Name&gt;

     &lt;CommandLine &gt; \ [{ProgramFilesX86} \\Microsoft Contoso\\Contoso\\contosomail.EXE "-c OEP. Примечание/m "%1" &lt; /commandline&gt;

     &lt;DropTargetClassId /&gt;

     &lt;Понятно&gt;

     &lt;Расширенная &gt; 0 &lt; /Extended&gt;

     &lt;LegacyDisable &gt; 0 &lt; /LegacyDisable&gt;

     &lt;SuppressionPolicy &gt; 2 &lt; /SuppressionPolicy&gt;

      &lt;DdeExec&gt;

     &lt;NoActivateHandler /&gt;

     &lt;Приложение &gt; contosomail &lt; /Application&gt;

     &lt;Тема &gt; ShellSystem &lt; /Topic&gt;

     &lt;IfExec &gt; \ [SHELLNOOP \] &lt; /IfExec&gt;

     &lt;DdeCommand &gt; \ [SetForeground \] \ [ShellNewDatabase "%1" \] &lt; /DdeCommand&gt;

     &lt;/DdeExec&gt;

     &lt;/ShellCommand&gt;

     &lt;/ShellCommands&gt;

     &lt;/ApplicationURLProtocol&gt;

     &lt;/URLProtocol&gt;

     &lt;/Extension&gt;

     &lt;/Extension&gt;

     &lt;/URLProtocols&gt;

   **Клиенты программного обеспечения**: позволяет приложению регистрироваться как клиент электронной почты, средство чтения новостей, проигрыватель мультимедиа и делает приложение видимым в пользовательском интерфейсе "Настройка доступа к программам и параметров по умолчанию для компьютера". В большинстве случаев вам нужно только включить и отключить его. Кроме того, есть элемент управления для включения и отключения клиента электронной почты в специальном варианте, если вы хотите, чтобы другие клиенты по-прежнему были включены только для этого клиента.

   &lt;SoftwareClients Enabled = "true"&gt;

     &lt;ClientConfiguration EmailEnabled = "ложь"/&gt;

   &lt;/SoftwareClients&gt;

   AppPaths: — Если приложение, например contoso.exe зарегистрировано с именем AppPath "MyApp", оно позволяет ввести "MyApp" в меню "выполнить", и оно откроется contoso.exe.

   &lt;AppPaths Enabled = "true"&gt;

   &lt;Расширения&gt;

   &lt;Расширение Category = "AppV. AppPath"&gt;

   &lt;AppPath&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /applicationId&gt;

     &lt;Name &gt;contosomail.exe&lt; /Name&gt;

     &lt;ApplicationPath &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationPath&gt;

     &lt;PATHEnvironmentVariablePrefix /&gt;

     &lt;CanAcceptUrl &gt; ложь &lt; /CanAcceptUrl&gt;

     &lt;SaveUrl /&gt;

   &lt;/AppPath&gt;

   &lt;/Extension&gt;

   &lt;/Extensions&gt;

   &lt;/AppPaths&gt;

   **Com**: позволяет приложению регистрировать локальные COM-серверы. Режим может быть интегрированным, изолированным или отключенным. Когда Isol.

   &lt;Режим COM = "изолированный"/&gt;

   **Другие параметры**:

   Помимо расширений, другие подсистемы можно включать и отключать и изменять.

   **Виртуальные объекты ядра**:

   &lt;Объекты включены = "ложь"/&gt;

   **Виртуальный реестр**: используется, если вы хотите настроить реестр в виртуальном реестре в HKCU

   &lt;Параметр Registry Enabled = "true"&gt;

   &lt;Включить&gt;

   &lt;Key путь = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\ABC"&gt;

   &lt;Тип значения = "REG \ _SZ" Name = "Bar" Data = "NewValue"/&gt;

    &lt;/Key&gt;

     &lt;Key путь = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\EmptyKey"/&gt;

    &lt;/Include&gt;

   &lt;Удаление&gt;

     &lt;/Registry&gt;

   **Виртуальная файловая система**

         &lt;FileSystem Enabled="true" /&gt;

   **Виртуальные шрифты**

         &lt;Fonts Enabled="false" /&gt;

   **Переменные виртуальных сред**

   &lt;EnvironmentVariables Enabled = "true"&gt;

   &lt;Включить&gt;

          &lt;Variable Name="UserPath" Value="%path%;%UserProfile%" /&gt;

          &lt;Variable Name="UserLib" Value="%UserProfile%\\ABC" /&gt;

          &lt;/Include&gt;

         &lt;Delete&gt;

          &lt;Variable Name="lib" /&gt;

           &lt;/Delete&gt;

           &lt;/EnvironmentVariables&gt;

   **Виртуальные службы**

         &lt;Services Enabled="false" /&gt;

3. **UserScripts** — сценарии можно использовать для настройки или изменения виртуальной среды, а также для выполнения сценариев во время развертывания или удаления, перед выполнением приложения, а также для "очистки" среды после завершения работы приложения. Составьте ссылку на пример файла пользовательской конфигурации, выводимым секвенсором, чтобы просмотреть пример сценария. В разделе "сценарии" ниже приведены дополнительные сведения о различных триггерах, которые можно использовать.

4. **ManagingAuthority** — можно использовать в том случае, если на одном и том же компьютере установлены две версии пакета, один из которых развернут в App-v 4,6, а другой — на App-v 5,0. Чтобы разрешить приложению App-V vNext дополнительные точки расширения App-V 4,6 для именованного пакета, введите в файл UserConfig следующие элементы (где PackageName — идентификатор GUID пакета в App-V 4,6:

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = "032630c0-b8e2-417c-acef-76fc5297fe81"/&gt;

### Файл динамической конфигурации развертывания

**Заголовок** — заголовок файла конфигурации развертывания выглядит следующим образом:

&lt;? XML Version = "1.0" Encoding = "UTF-8"? &gt; &lt; DeploymentConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;

**PackageId** имеет то же значение, которое существует в файле манифеста.

**Body** — тело файла конфигурации развертывания включает два раздела:

-   Раздел "Конфигурация пользователя" — допускает то же содержимое, что и файл конфигурации пользователя, описанный в предыдущем разделе. Когда пакет публикуется для пользователя, любые параметры конфигурации appextensions в этом разделе будут переопределять соответствующие параметры в манифесте пакета, если не указан также файл конфигурации пользователя. Если указан также файл UserConfig, он будет использоваться вместо параметров пользователя в файле конфигурации развертывания. Если пакет опубликован глобально, в сочетании с манифестом будет использоваться только содержимое файла конфигурации развертывания.

-   Раздел "Конфигурация компьютера" — содержат данные, которые можно настроить только для всего компьютера, а не для определенного пользователя на компьютере. Например, Раздел HKEY \ _LOCAL \ _MACHINE разделов реестра в VFS.

&lt;DeploymentConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;

&lt;UserConfiguration&gt;

  ..

&lt;/UserConfiguration&gt;

&lt;MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

&lt;/DeploymentConfiguration&gt;

**Конфигурация пользователя** — используйте предыдущий раздел **файла динамической конфигурации пользователя** для получения сведений о параметрах, которые содержатся в разделе "Конфигурация пользователя" файла конфигурации развертывания.

Конфигурация компьютера: раздел "Конфигурация компьютера" файла конфигурации развертывания используется для настройки сведений, которые можно задать только для всего компьютера, а не для определенного пользователя на компьютере. Например, Раздел HKEY \ _LOCAL \ _MACHINE разделы реестра в виртуальном реестре. Для этого элемента разрешены четыре подраздела.

1.  **Подсистемы** — AppExtensions и другие подсистемы размещаются как подузлы в &lt; подсистемах &gt; .

    &lt;MachineConfiguration&gt;

      &lt;Подсистем&gt;

      ..

      &lt;/Subsystems&gt;

    ..

    &lt;/MachineConfiguration&gt;

    В следующем разделе показаны различные подсистемы и примеры использования.

    **Расширениями**:

    Некоторые подсистемы (расширения подсистем), которые могут применяться только ко всем пользователям. Подсистема — это возможности приложения. Так как это применимо только для всех пользователей, пакет должен быть опубликован глобально для интеграции этого типа расширений в локальную систему. Те же правила для элементов управления и параметров, применимые к расширениям в конфигурации пользователя, также применяются к параметрам в разделе MachineConfiguration.

    **Возможности приложения**: используется программами по умолчанию в интерфейсе операционной системы Windows. Позволяет приложению регистрироваться так, как если бы можно было открывать определенные расширения файлов, как это происходит при открытии определенных типов MIME Windows в меню "Пуск".Это расширение также делает виртуальное приложение видимым в пользовательском интерфейсе "Настройка программ по умолчанию".

    &lt;ApplicationCapabilities Enabled = "true"&gt;

      &lt;Расширения&gt;

       &lt;Расширение Category = "AppV. ApplicationCapabilities"&gt;

        &lt;ApplicationCapabilities&gt;

         &lt;ApplicationId&gt;\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe&lt;/ApplicationId&gt;

         &lt;Reference&gt;

          &lt;Name&gt;LitView Browser&lt;/Name&gt;

          &lt;Path&gt;SOFTWARE\\LitView\\Browser\\Capabilities&lt;/Path&gt;

         &lt;/Reference&gt;

       &lt;CapabilityGroup&gt;

        &lt;Capabilities&gt;

         &lt;Name&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12345&lt;/Name&gt;

         &lt;Description&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12346&lt;/Description&gt;

         &lt;Hidden&gt;0&lt;/Hidden&gt;

         &lt;EMailSoftwareClient&gt;Lit View E-Mail Client&lt;/EMailSoftwareClient&gt;

         &lt;FileAssociationList&gt;

          &lt;FileAssociation Extension=".htm" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".html" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".shtml" ProgID="LitViewHTML" /&gt;

         &lt;/FileAssociationList&gt;

         &lt;MIMEAssociationList&gt;

          &lt;MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" /&gt;

          &lt;MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" /&gt;

         &lt;/MIMEAssociationList&gt;

        &lt;URLAssociationList&gt;

          &lt;URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" /&gt;

         &lt;/URLAssociationList&gt;

         &lt;/Capabilities&gt;

      &lt;/CapabilityGroup&gt;

       &lt;/ApplicationCapabilities&gt;

      &lt;/Extension&gt;

    &lt;/Extensions&gt;

    &lt;/ApplicationCapabilities&gt;

    **Другие параметры**:

    В дополнение к расширениям можно редактировать и другие подсистемы:

    **Виртуальный реестр для всего компьютера**: используется, если вы хотите установить раздел реестра в виртуальном реестре в HKEY \ _Local \ _Machine

    &lt;Реестр&gt;

    &lt;Включить&gt;

      &lt;Key Path = "\\REGISTRY\\Machine\\Software\\ABC"&gt;

        &lt;Value Type="REG\_SZ" Name="Bar" Data="Baz" /&gt;

       &lt;/Key&gt;

      &lt;Key Path = "\\REGISTRY\\Machine\\Software\\EmptyKey"/&gt;

     &lt;/Include&gt;

    &lt;Удаление&gt;

    &lt;/Registry&gt;

    **Виртуальные объекты ядра на уровне компьютера**

    &lt;Object&gt;

    &lt;NotIsolate&gt;

       &lt;Object Name = "testObject"/&gt;

     &lt;/NotIsolate&gt;

    &lt;/Objects&gt;

2.  **ProductSourceURLOptOut**: указывает, можно ли глобально изменить URL-адрес пакета с помощью PackageSourceRoot (для поддержки сценариев филиалов). Значение по умолчанию — false, и изменения параметров вступят в силу при следующем запуске.  

    &lt;MachineConfiguration&gt;

      .. 

      &lt;ProductSourceURLOptOut Enabled = "true"/&gt;

      ..

    &lt;/MachineConfiguration&gt;

3.  **MachineScripts** — пакет можно настроить для выполнения сценариев во время развертывания, публикации или удаления. Составьте ссылку на пример файла конфигурации развертывания, который создается секвенсором, чтобы просмотреть пример сценария. В разделе "сценарии" приведены дополнительные сведения о различных триггерах, которые можно использовать

4.  **TerminateChildProcess**: — можно указать исполняемый файл приложения, дочерние процессы которого будут завершаться после завершения процесса exe-файла приложения.

    &lt;MachineConfiguration&gt;

      ..   

      &lt;TerminateChildProcesses&gt;

        &lt;Application Path="\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE" /&gt;

        &lt;Application Path="\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe" /&gt;

        &lt;Application Path="\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE" /&gt;

      &lt;/TerminateChildProcesses&gt;

      ..

    &lt;/MachineConfiguration&gt;

### Скрипты

В приведенной ниже таблице описаны различные события сценария и контекст, в котором они могут быть запущены.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Время выполнения сценария</th>
<th align="left">Может быть указано в конфигурации развертывания</th>
<th align="left">Может быть указано в конфигурации пользователя</th>
<th align="left">Может выполняться в виртуальной среде пакета</th>
<th align="left">Может выполняться в контексте определенного приложения.</th>
<th align="left">Работа в контексте системы и пользователя: (конфигурация развертывания, Конфигурация пользователя)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(СИСТЕМА, Н/Д)</p></td>
</tr>
<tr class="even">
<td align="left"><p>PublishPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Система, пользователь)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UnpublishPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Система, пользователь)</p></td>
</tr>
<tr class="even">
<td align="left"><p>RemovePackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(СИСТЕМА, Н/Д)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartProcess</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(Пользователь, пользователь)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ExitProcess</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(Пользователь, пользователь)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Пользователь, пользователь)</p></td>
</tr>
<tr class="even">
<td align="left"><p>TerminateVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Пользователь, пользователь)</p></td>
</tr>
</tbody>
</table>

 

### Создание динамического файла конфигурации с помощью файла манифеста App-V 5,0

Вы можете создать файл динамической конфигурации с помощью одного из трех методов: либо вручную, с помощью консоли управления App-V 5,0, либо последовательности пакета, который будет создан с помощью 2 примеров файлов.

Дополнительные сведения о том, как создать файл с помощью консоли управления App-V 5,0, можно найти в разделе [Создание настраиваемого файла конфигурации с помощью консоли управления App-v 5,0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).

Чтобы создать файл вручную, данные, приведенные выше в предыдущих разделах, можно объединить в один файл. Мы рекомендуем использовать файлы, созданные секвенсором.






## Статьи по теме


[Применение файла конфигурации развертывания с помощью PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

[Применение файла конфигурации пользователя с помощью PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell.md)

[Операции, связанные с администрированием и использованием App-V 5.0](operations-for-app-v-50.md)

 

 





