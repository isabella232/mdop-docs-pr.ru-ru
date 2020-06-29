---
title: Сведения о динамической конфигурации App-V 5,1
description: Вы можете использовать динамическую конфигурацию для настройки пакета App-V 5,1 для пользователя. Используйте следующие сведения для создания или изменения существующего файла динамической конфигурации.
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/28/2018
ms.author: dansimp
ms.openlocfilehash: ec8a25da6e139ac329810b1e04f7097cadaa6ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814962"
---
# Сведения о динамической конфигурации App-V 5,1 
С помощью динамической конфигурации можно изменить файл динамической конфигурации, чтобы настроить способ запуска пакета App-V 5,1 для пользователя или группы. Настройка пакета удаляет необходимость повторной последовательности пакетов с использованием нужных параметров.  Кроме того, она позволяет хранить содержимое пакета и пользовательские параметры независимо друг от друга.

Пакеты виртуальных приложений содержат манифест, который предоставляет все основные сведения о пакете. Эти сведения включают значения по умолчанию для параметров пакета и определяют параметры в самой простой форме (без дополнительной настройки). 

При создании пакета секвенсор автоматически создает файлы конфигурации по умолчанию и User Configuration. XML, используя данные манифеста пакета. Таким образом, эти файлы отражают параметры по умолчанию, настроенные во время последовательности. Если вы применяете эти файлы к пакету в форме, созданной секвенсором, пакеты имеют те же параметры по умолчанию, которые поставляются из манифеста. 

Используйте эти созданные файлы для внесения изменений, если это не повлияет прямо на пакет. Если вы хотите добавить, удалить или обновить файлы конфигурации, внесите изменения в сведения о значениях по умолчанию в манифесте.

>[!TIP]
>Порядок чтения файлов:<ul><li>UserConfig.xml</li><li>DeploymentConfig.xml</li><li>Является</li></ul><p>Первый элемент показывает, что получает последнюю прочтение. Таким образом, его содержимое имеет приоритет, а все пакеты по сути содержат параметры по умолчанию из манифеста пакета.<ol><li> Если настройка файла DeploymentConfig.xml и применение настроенных параметров, параметры по умолчанию в манифесте пакета переопределяются. </li><li> После настройки UserConfig.xml и применения настроенных параметров параметры по умолчанию для конфигурации развертывания и манифеста пакета переопределяются. </li></ol>

## Содержимое файла конфигурации пользователя (UserConfig.xml)
Файл UserConfig предоставляет параметры конфигурации, которые применяются для определенного пользователя при развертывании пакета на компьютере с клиентским приложением App-V 5,1.  Эти параметры не влияют на других пользователей на клиенте.

С помощью файла UserConfig можно указать или изменить пользовательские параметры для пакета:

-   Расширения, интегрированные в собственную систему на одного пользователя: сочетания клавиш, сопоставления типов файлов, URL-протоколы, AppPaths, клиенты и COM
-   Виртуальные подсистемы: объекты приложения, переменные среды, изменения в реестре, службы и шрифты
-   Сценарии (только для контекста пользователя)
-   Управление полномочиями (для управления сосуществованием пакета с помощью App-V 4,6)

### Заголовок

Заголовок динамического пользовательского файла конфигурации выглядит так:

```xml
<?xml version="1.0" encoding="utf-8"?><UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">
```

**PackageId** имеет то же значение, которое существует в файле манифеста.


### Body

Основная часть файла динамической конфигурации пользователя может включать все точки расширения приложения, определенные в файле манифеста, а также сведения для настройки виртуальных приложений. В тексте сообщения можно использовать четыре подраздела.

1.  **[Приложения](#applications)** 
2.  **[Подсистем](#subsystems)**
3.  **[UserScripts](#userscripts)**
4.  **[ManagingAuthority](#managingauthority)**

#### Приложения

Все расширения приложения, содержащиеся в файле манифеста в пакете, имеют присвоенный идентификатор приложения, который находится в файле манифеста. Идентификатор приложения позволяет включать или отключать все расширения для данного приложения в пакете. Идентификатор приложения должен находиться в файле манифеста или игнорироваться.

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved"  xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Applications>

<!--No new application can be defined in policy. AppV Client will ignore any application ID that is not also in the Manifest file-->

<Application Id="{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled="false">

</Application>

</Applications>

..

</UserConfiguration>
```

#### Подсистем

AppExtensions и другие подсистемы, упорядоченные как подузлы.

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Subsystems>

..

</Subsystems>

..

</UserConfiguration>
```

Вы можете включать и отключать каждую подсистему с помощью атрибута **Enabled** .

**Расширения** 

Некоторые подсистемы (расширения элементов управления доподсистемой). Эти подсистемы — это сочетания клавиш, сопоставления типов файлов, URL-протоколы, AppPaths, клиенты и COM.

Подсистемы расширения можно включать и отключать независимо от содержимого. Например, если вы включите клавиши быстрого доступа, клиент по умолчанию использует сочетания клавиш, содержащиеся в манифесте. Каждая подсистема расширения может содержать \<Extensions\> узел. Если этот дочерний элемент присутствует, клиент игнорирует содержимое в файле манифеста для этой подсистемы и использует только содержимое в файле конфигурации. 

_**Примеры:**_ 

- Если вы определяете это в файле конфигурации пользователя или развертывания, содержимое манифеста будет игнорироваться.

  ```XML

  <Shortcuts  Enabled="true"\>

  <Extensions>

  ...

  </Extensions>

  </Shortcuts>
  ```
- Если вы определяете только указанные ниже элементы, во время публикации будет интегрировано содержимое манифеста.

  ```XML

  <Shortcuts  Enabled="true"/>
  ```

- Если вы задаете указанные ниже, все сочетания клавиш в манифесте по-прежнему будут игнорироваться. Другими словами, сочетания клавиш не интегрируются.

  ```XML

  <Shortcuts  Enabled="true">

     <Extensions/>

  </Shortcuts>
  ```

_**Поддерживаемые подсистемы расширения:**_ 

Подсистема расширения **клавиш** определяет, какие сочетания клавиш интегрируются в локальную систему.  

```XML

<Subsystems>

<Shortcuts Enabled="true">

  <Extensions>

    <Extension Category="AppV.Shortcut">

      <Shortcut>

        <File>[{Common Programs}]\Microsoft Contoso\Microsoft ContosoApp Filler 2010.lnk</File>

        <Target>[{PackageRoot}]\Contoso\ContosoApp.EXE</Target>


      <Icon>[{Windows}]\Installer\{90140000-0011-0000-0000-0000000FF1CE}\inficon.exe</Icon>

        <Arguments />

        <WorkingDirectory />

        <AppUserModelId>ContosoApp.Filler.3</AppUserModelId>

        <Description>Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.</Description>

        <Hotkey>0</Hotkey>

        <ShowCommand>1</ShowCommand>

      <ApplicationId>[{PackageRoot}]\Contoso\ContosoApp.EXE</ApplicationId>

      </Shortcut>

  </Extension>

  <Extension Category="AppV.Shortcut">

    <Shortcut>

    <File>[{AppData}]\Microsoft\Contoso\Recent\Templates.LNK</File>

      <Target>[{AppData}]\Microsoft\Templates</Target>

      <Icon />

      <Arguments />

      <WorkingDirectory />

      <AppUserModelId />

      <Description />

      <Hotkey>0</Hotkey>

      <ShowCommand>1</ShowCommand>

      <!-- Note the ApplicationId is optional -->

    </Shortcut>

  </Extension>

 </Extensions>

</Shortcuts>
```

**Тип файла связывает** подсистему расширения, связывает типы файлов с программами, открытыми по умолчанию, а также настраивает контекстное меню. 

>[!TIP]
>Подсистему можно настроить с помощью типов MIME.

```XML

<FileTypeAssociations Enabled="true">

<Extensions>

  <Extension Category="AppV.FileTypeAssociation">

    <FileTypeAssociation>

      <FileExtension MimeAssociation="true">

      <Name>.docm</Name>

      <ProgId>contosowordpad.DocumentMacroEnabled.12</ProgId>

      <PerceivedType>document</PerceivedType>

    <ContentType>application/vnd.ms-contosowordpad.document.macroEnabled.12</ContentType>

      <OpenWithList>

        <ApplicationName>wincontosowordpad.exe</ApplicationName>

      </OpenWithList>

     <OpenWithProgIds>

        <ProgId>contosowordpad.8</ProgId>

      </OpenWithProgIds>

      <ShellNew>

        <Command />

        <DataBinary />

        <DataText />

        <FileName />

        <NullFile>true</NullFile>

        <ItemName />

        <IconPath />

        <MenuText />

        <Handler />

      </ShellNew>

    </FileExtension>

    <ProgId>

       <Name>contosowordpad.DocumentMacroEnabled.12</Name>

      <DefaultIcon\>[{Windows}]\Installer\{90140000-0011-0000-0000-000000FF1CE}\contosowordpadicon.exe,15</DefaultIcon>

        <Description>Blah Blah Blah</Description>

        <FriendlyTypeName>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,9182</FriendlyTypeName>

        <InfoTip>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,1424</InfoTip>

        <EditFlags>0</EditFlags>

        <ShellCommands>

          <DefaultCommand>Open</DefaultCommand>

          <ShellCommand>

           <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

             <Name>Edit</Name>

             <FriendlyName>&Edit</FriendlyName>

           <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /vu "%1"</CommandLine>

          </ShellCommand>

          </ShellCommand>

          <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

            <Name>Open</Name>

            <FriendlyName>&Open</FriendlyName>

            <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /n "%1"</CommandLine>

            <DropTargetClassId />

            <DdeExec>

              <Application>mscontosowordpad</Application>

              <Topic>ShellSystem</Topic>

              <IfExec>[SHELLNOOP]</IfExec>

              <DdeCommand>[SetForeground][ShellNewDatabase"%1"]</DdeCommand>

            </DdeExec>

          </ShellCommand>

        </ShellCommands>

      </ProgId>

     </FileTypeAssociation>

   </Extension>

  </Extensions>

  </FileTypeAssociations>
```

Подсистема расширения **URL-протоколов** управляет протоколами URL-адресов, интегрированными в локальный реестр клиентского компьютера, например _mailto:_. 

```XML

<URLProtocols Enabled="true">

<Extensions>

<Extension Category="AppV.URLProtocol">

<URLProtocol>

  <Name>mailto</Name>

  <ApplicationURLProtocol>

  <DefaultIcon>[{ProgramFilesX86}]\MicrosoftContoso\Contoso\contosomail.EXE,-9403</DefaultIcon>

  <EditFlags>2</EditFlags>

  <Description />

  <AppUserModelId />

  <FriendlyTypeName />

  <InfoTip />

<SourceFilter />

  <ShellFolder />

  <WebNavigableCLSID />

  <ExplorerFlags>2</ExplorerFlags>

  <CLSID />

  <ShellCommands>

  <DefaultCommand>open</DefaultCommand>

  <ShellCommand>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>open</Name>

  <CommandLine>[{ProgramFilesX86}\Microsoft Contoso\Contoso\contosomail.EXE" -c OEP.Note /m "%1"</CommandLine>

  <DropTargetClassId />

  <FriendlyName />

  <Extended>0</Extended>

  <LegacyDisable>0</LegacyDisable>

  <SuppressionPolicy>2</SuppressionPolicy>

   <DdeExec>

  <NoActivateHandler />

  <Application>contosomail</Application>

  <Topic>ShellSystem</Topic>

  <IfExec>[SHELLNOOP]</IfExec>

  <DdeCommand>[SetForeground][ShellNewDatabase "%1"]</DdeCommand>

  </DdeExec>

  </ShellCommand>

  </ShellCommands>

  </ApplicationURLProtocol>

  </URLProtocol>

  </Extension>

  </Extension>

  </URLProtocols>
```

Подсистема расширений **клиентских программного обеспечения** позволяет приложению регистрироваться как клиент электронной почты, средство чтения новостей, проигрыватель мультимедиа и делает приложение видимым в пользовательском интерфейсе "Настройка доступа к программам и параметров по умолчанию для компьютера". В большинстве случаев вы должны включать и отключать его. Кроме того, есть элемент управления для включения и отключения клиента электронной почты в специальном варианте, если вы хотите, чтобы другие клиенты по-прежнему были включены только для этого клиента.

```XML

<SoftwareClients Enabled="true">

  <ClientConfiguration EmailEnabled="false" />

</SoftwareClients>
```

Подсистема расширения **AppPaths** открывает приложения, которые зарегистрированы с помощью пути к приложению. Например, если contoso.exe имеет имя " _MyApp_", пользователи могут ввести _MyApp_ в меню "выполнить", а затем открыть contoso.exe.

```XML

<AppPaths Enabled="true">

<Extensions>

<Extension Category="AppV.AppPath">

<AppPath>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>contosomail.exe</Name>

  <ApplicationPath>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationPath>

  <PATHEnvironmentVariablePrefix />

  <CanAcceptUrl>false</CanAcceptUrl>

  <SaveUrl />

</AppPath>

</Extension>

</Extensions>

</AppPaths>
```

Подсистема **com-** расширений позволяет приложению, которое зарегистрировано на ЛОКАЛЬНЫХ серверах com. Режим может быть следующим:

-   Интеграци
-   Знает 
-   Отключено

```XML

<COM Mode="Isolated"/>
```

**Виртуальные объекты ядра**

```XML

<Objects Enabled="false" />
```

**Виртуальный реестр** задает реестр в виртуальном реестре в HKCU.

```XML

<Registry Enabled="true">

<Include>

<Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\ABC">

<Value Type="REG_SZ" Name="Bar" Data="NewValue" />

 </Key>

  <Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**Виртуальная файловая система**

```XML

    <FileSystem Enabled="true" />
```

**Виртуальные шрифты**

```XML

      <Fonts Enabled="false" />
```

**Переменные виртуальных сред**

```XML

<EnvironmentVariables Enabled="true">

<Include>

       <Variable Name="UserPath" Value="%path%;%UserProfile%" />

       <Variable Name="UserLib" Value="%UserProfile%\ABC" />

       </Include>

      <Delete>

       <Variable Name="lib" />

        </Delete>

        </EnvironmentVariables>
```

**Виртуальные службы**

```XML

      <Services Enabled="false" />
```

#### UserScripts

Используйте UserScripts, чтобы настроить или изменить виртуальную среду.  Вы также можете выполнить сценарии во время развертывания или очистить среду после завершения работы приложения. Пример сценария можно найти в файле пользовательской конфигурации, созданной секвенсором. В разделе "сценарии" ниже приведены дополнительные сведения о различных триггерах, которые можно использовать.

#### ManagingAuthority

Используйте ManagingAuthority, если на одном и том же компьютере существуют две версии пакета, один из которых развернут в App-V 4,6, а другой — в App-V 5,0. Чтобы разрешить приложению App-V vNext дополнительные точки расширения App-V 4,6 для именованного пакета, введите в файл UserConfig следующие элементы (где PackageName — идентификатор GUID пакета в App-V 4,6:

```XML

<ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName="032630c0-b8e2-417c-acef-76fc5297fe81" />
```

## Файл конфигурации развертывания (DeploymentConfig.xml)

Файл DeploymentConfig предоставляет параметры конфигурации для контекста компьютера и контекста пользователя, обеспечивая те же возможности, которые указаны в файле UserConfig. Параметр применяется при развертывании пакета на компьютере, на котором запущен клиент App-V 5,1.

Использование файла DeploymentConfig для указания или изменения настраиваемых параметров пакета:

- Все параметры UserConfig
- Расширения, применимые только глобально для всех пользователей
- Виртуальные подсистемы для глобальных машинных папок, например Registry
- URL-адрес источника продукта
- Сценарии (только для контекста компьютера)
- Элементы управления для завершения дочерних процессов

### Заголовок

Заголовок динамического файла конфигурации развертывания выглядит следующим образом:

```XML
<?xml version="1.0" encoding="utf-8"?><DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">
```

**PackageId** имеет то же значение, которое существует в файле манифеста.

### Body

В тексте файла конфигурации динамического развертывания содержатся два раздела:

- **UserConfiguration:** допускает то же содержимое, что и файл конфигурации пользователя, описанный в предыдущем разделе.  При публикации пакета для пользователя любые параметры конфигурации appextensions в этом разделе переопределяют соответствующие параметры в манифесте пакета, если только вы не предоставляли файл конфигурации пользователя. Если вы также предоставляете файл UserConfig, он будет использоваться вместо параметров пользователя в файле конфигурации развертывания. Если опубликовать пакет глобально, то в сочетании с манифестом будет использоваться только содержимое файла конфигурации развертывания. Дополнительные сведения можно найти в разделе [содержимое файла конфигурации пользователя (UserConfig.xml)](#user-configuration-file-contents-userconfigxml).

- **MachineConfiguration:** содержат данные, которые можно настроить только для всего компьютера, а не для определенного пользователя на компьютере. Например, HKEY_LOCAL_MACHINE разделы реестра в VFS.

```XML

<DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">

<UserConfiguration>

...

</UserConfiguration>

<MachineConfiguration>

...

</MachineConfiguration>

...

</MachineConfiguration>

</DeploymentConfiguration>
```

### UserConfiguration

Сведения о параметрах, описанных в этом разделе, можно найти в [содержимом файла конфигурации пользователя (UserConfig.xml)](#user-configuration-file-contents-userconfigxml) . 

### MachineConfiguration

Используйте раздел MachineConfiguration, чтобы настроить данные для всего компьютера; не для определенного пользователя на компьютере. Например, HKEY_LOCAL_MACHINE разделы реестра в виртуальном реестре. Ниже приведено четыре подраздела, которые можно использовать для этого элемента:

1.  **[Подсистем](#subsystems-1)**
2.  **[ProductSourceURLOptOut](#productsourceurloptout)**
3.  **[MachineScripts](#machinescripts)**
4.  **[TerminateChildProcess](#terminatechildprocess)**

#### Подсистем

AppExtensions и другие подсистемы, упорядоченные как подузлы.

```XML

<MachineConfiguration>

  <Subsystems>

  …

  </Subsystems>

…

</MachineConfiguration>
```

Вы можете включать и отключать каждую подсистему с помощью атрибута **Enabled** .

**Расширения** 

Некоторые подсистемы (расширения элементов управления доподсистемой). Подсистема — это возможности приложения, которые используются программами по умолчанию. Для этого типа расширения пакет должен быть опубликован глобально для интеграции с локальной системой. Те же правила для элементов управления и параметров, применимые к расширениям в конфигурации пользователя, также применяются к параметрам в разделе MachineConfiguration.

**Возможности приложения**: используется программами по умолчанию, которые позволяют приложению регистрироваться так:

- Возможность открывать определенные расширения файлов
- Средство "создание" для слота Интернет-браузера "меню" Пуск "
- Возможность открывать определенные типы MIME для Windows

Это расширение также делает виртуальное приложение видимым в пользовательском интерфейсе "Настройка программ по умолчанию".

```XML

<ApplicationCapabilities Enabled="true">

  <Extensions>

   <Extension Category="AppV.ApplicationCapabilities">

    <ApplicationCapabilities>


   <ApplicationId>[{PackageRoot}]\LitView\LitViewBrowser.exe</ApplicationId>

     <Reference>

      <Name>LitView Browser</Name>

      <Path>SOFTWARE\LitView\Browser\Capabilities</Path>

     </Reference>

   <CapabilityGroup>

    <Capabilities>


   <Name>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12345</Name>


   <Description>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12346</Description>

     <Hidden>0</Hidden>

     <EMailSoftwareClient>Lit View E-Mail Client</EMailSoftwareClient>

     <FileAssociationList>

      <FileAssociation Extension=".htm" ProgID="LitViewHTML" />

      <FileAssociation Extension=".html" ProgID="LitViewHTML" />

      <FileAssociation Extension=".shtml" ProgID="LitViewHTML" />

     </FileAssociationList>

     <MIMEAssociationList>

      <MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" />

      <MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" />

     </MIMEAssociationList>

    <URLAssociationList>

      <URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" />

     </URLAssociationList>

     </Capabilities>

  </CapabilityGroup>

   </ApplicationCapabilities>

  </Extension>

</Extensions>

</ApplicationCapabilities>
```

_**Поддерживаемые подсистемы расширения:**_ 

Подсистема расширения **реестра для виртуальной машины** устанавливает раздел реестра в виртуальном реестре в HKEY_LOCAL_MACHINE.

```XML

<Registry>

<Include>

  <Key Path="\REGISTRY\\Machine\Software\ABC">

    <Value Type="REG_SZ" Name="Bar" Data="Baz" />

   </Key>

  <Key Path="\REGISTRY\Machine\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**Виртуальные объекты ядра на уровне компьютера**

```XML

<Objects>

<NotIsolate>

   <Object Name="testObject" />

 </NotIsolate>

</Objects>
```

#### ProductSourceURLOptOut

Используйте ProductSourceURLOptOut, чтобы указать, что URL-адрес пакета можно изменить глобально с помощью _PackageSourceRoot_ (для поддержки сценариев филиалов). Изменения вступят в силу при следующем запуске. 

```XML

<MachineConfiguration>

  ... 

  <ProductSourceURLOptOut Enabled="true" />

  ...

</MachineConfiguration>
```

#### MachineScripts

Пакет можно настроить для выполнения сценариев во время развертывания, публикации или удаления. Пример сценария можно найти в файле конфигурации развертывания, созданном секвенсором. 

В разделе "сценарии" ниже приведены дополнительные сведения о различных триггерах, которые можно использовать.

#### TerminateChildProcess

Можно указать исполняемый файл приложения, дочерние процессы которого завершаются после завершения процесса приложения exe.

```XML

<MachineConfiguration>

  ...   

  <TerminateChildProcesses>

    <Application Path="[{PackageRoot}]\Contoso\ContosoApp.EXE" />

    <Application Path="[{PackageRoot}]\LitView\LitViewBrowser.exe" />

    <Application Path="[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE" />

  </TerminateChildProcesses>

  ...

</MachineConfiguration>
```



## Скрипты

В приведенной ниже таблице описаны различные события сценария и контекст, в котором они могут быть запущены.

| Время выполнения сценария       | Может быть указано в конфигурации развертывания | Может быть указано в конфигурации пользователя | Может выполняться в виртуальной среде пакета | Может выполняться в контексте определенного приложения. | Работа в контексте системы и пользователя: (конфигурация развертывания, Конфигурация пользователя) |
|-----------------------------|----------------------------------------------|----------------------------------------|---------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------|
| AddPackage                  | X                                            |                                        |                                                   |                                                     | (СИСТЕМА, Н/Д)                                                               |
| PublishPackage              | X                                            | X                                      |                                                   |                                                     | (Система, пользователь)                                                              |
| UnpublishPackage            | X                                            | X                                      |                                                   |                                                     | (Система, пользователь)                                                              |
| RemovePackage               | X                                            |                                        |                                                   |                                                     | (СИСТЕМА, Н/Д)                                                               |
| StartProcess                | X                                            | X                                      | X                                                 | X                                                   | (Пользователь, пользователь)                                                                |
| ExitProcess                 | X                                            | X                                      |                                                   | X                                                   | (Пользователь, пользователь)                                                                |
| StartVirtualEnvironment     | X                                            | X                                      | X                                                 |                                                     | (Пользователь, пользователь)                                                                |
| TerminateVirtualEnvironment | X                                            | X                                      |                                                   |                                                     | (Пользователь, пользователь)                                                                |

### Использование нескольких сценариев для одного триггера событий

Приложение App-V 5,1 поддерживает использование нескольких сценариев для одного триггера событий для пакетов App-V, включая пакеты, которые преобразуются из App-V 4,6 в App-V 5,0 или более поздней версии. Чтобы включить использование нескольких сценариев, App-V 5,1 использует приложение для запуска сценариев, именуемое ScriptRunner.exe, которое устанавливается как часть установки клиента App-V.

### Использование нескольких сценариев для одного триггера событий

Для каждого сценария, который необходимо выполнить, передайте этот сценарий в качестве аргумента в приложение ScriptRunner.exe. Затем приложение выполняет каждый сценарий отдельно, вместе с аргументами, указанными для каждого сценария. Используйте только один сценарий (ScriptRunner.exe) для каждого триггера.

> [!NOTE]
> 
> Рекомендуется сначала запустить многострочную строку из командной строки, чтобы убедиться, что все аргументы правильно собраны, прежде чем добавлять их в файл конфигурации развертывания.

### Пример описания сценария и параметра

С помощью приведенного ниже примера файла и таблицы измените файл развертывания или файла конфигурации пользователя, чтобы добавить сценарии, которые нужно выполнить.

```XML
<MachineScripts>
 <AddPackage>
   <Path>ScriptRunner.exe</Path>
   <Arguments>
   -appvscript script1.exe arg1 arg2 –appvscriptrunnerparameters –wait –timeout=10
   -appvscript script2.vbs arg1 arg2
   -appvscript script3.bat arg1 arg2 –appvscriptrunnerparameters –wait –timeout=30 –rollbackonerror
   </Arguments>
   <Wait timeout=”40” RollbackOnError=”true”/>
 </AddPackage>
</MachineScripts>
```


**К параметрам в примере файла относятся:**

#### \<AddPackage\>

Имя триггера событий, для которого выполняется сценарий, например добавление пакета или Публикация пакета.

#### \<Path\>ScriptRunner.exe\</Path\>

Приложение для запуска сценариев, установленное как часть установки клиента App-V.

> [!NOTE]
> 
> Несмотря на то, что ScriptRunner.exe установлено как часть клиента App-V, расположение клиента App-V должно быть в% path% или ScriptRunner не будет выполняться. ScriptRunner.exe, как правило, находятся в C:FilesApplication Virtualizationfolder.

#### \<Arguments\>

`-appvscript` -Маркер, который представляет фактический сценарий, который необходимо выполнить.

`script1.exe` — Имя сценария, который вы хотите выполнить.

`arg1 arg2` — Аргументы для сценария, который необходимо выполнить.

`-appvscriptrunnerparameters` — Маркер, который представляет параметры выполнения для script1.exe.

`-wait` — Маркер, который информирует ScriptRunner о завершении выполнения script1.exe, прежде чем переходить к следующему сценарию.

`-timeout=x` — Маркер, который информирует ScriptRunner о том, чтобы остановить выполнение текущего сценария после x числа секунд. Все остальные указанные сценарии по-прежнему выполняются.

`-rollbackonerror` — Маркер, который информирует ScriptRunner, чтобы остановить выполнение всех сценариев, которые еще не выполнялись, и откатить ошибку в клиенте App-V.

#### \<Wait timeout=”40” RollbackOnError=”true”/\>

Ожидание полного завершения ScriptRunner.exe.

Установите значение таймаута для общего средства выполнения, чтобы оно не превышало сумму значений времени ожидания в отдельных сценариях.

Если какой-либо из отдельных сценариев сообщил об ошибке, а для rollbackonerror задано значение "true", то ScriptRunner сообщит об ошибке в клиенте App-V.

ScriptRunner запускает сценарий, тип файла которого связан с приложением, установленным на компьютере. Если связанное приложение отсутствует или тип файла сценария не связан с каким-либо приложением на компьютере, сценарий не запускается.

### Создание динамического файла конфигурации с помощью файла манифеста App-V 5,1

Вы можете создать файл динамической конфигурации с помощью одного из трех методов: либо вручную, с помощью консоли управления App-V 5,1, либо последовательности пакета, который создает два файла примеров. Дополнительные сведения о том, как создать файл с помощью консоли управления App-V 5,1, можно найти в разделе [Создание настраиваемого файла конфигурации с помощью консоли управления App-v 5,1](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md).

Чтобы создать файл вручную, данные, приведенные выше в предыдущих разделах, можно объединить в один файл. Мы рекомендуем использовать файлы, созданные секвенсором.



- Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).
- Для устранения проблем с приложением-V используйте [Форум TechNet App-v](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме

- [Применение файла конфигурации развертывания с помощью PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

- [Применение файла конфигурации пользователя с помощью PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

- [Операции, связанные с администрированием и использованием App-V 5.1](operations-for-app-v-51.md)

---
