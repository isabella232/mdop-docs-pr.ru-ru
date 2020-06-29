---
title: Сведения о MBAM 2.0 с пакетом обновления 1 (SP1)
description: Сведения о MBAM 2.0 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: 5ba89ed8-bb6e-407b-82c2-e2e36dd1078e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 73b92cd852d4f75f63f3dcba9f18167012b61401
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823552"
---
# Сведения о MBAM 2.0 с пакетом обновления 1 (SP1)

В этой статье описаны изменения в центре администрирования и мониторинга Microsoft BitLocker (MBAM) 2,0 с пакетом обновления 1 (SP1). Общее описание MBAM [в разделе Начало работы с MBAM 2,0](getting-started-with-mbam-20-mbam-2.md).

## <a href="" id="what-s-new-in-mbam-2-0-sp1"></a>Новые возможности MBAM 2,0 с пакетом обновления 1 (SP1)

Эта версия MBAM предоставляет следующие новые функции и возможности.

### Поддержка для Windows 8,1, Windows Server 2012 R2 и System Center 2012 R2 Configuration Manager

Администрирование и мониторинг Microsoft BitLocker (MBAM) 2,0 с пакетом обновления 1 (SP1) добавляет поддержку для Windows 8,1, Windows Server 2012 R2 и System Center 2012 R2 Configuration Manager.

### Поддержка Microsoft SQL Server 2008 R2 с пакетом обновления 2 (SP2)

Администрирование и мониторинг Microsoft BitLocker (MBAM) 2,0 с пакетом обновления 1 (SP1) добавляет поддержку для Microsoft SQL Server 2008 R2 SP2. Если вы используете Microsoft System Center Configuration Manager 2007 R2, вам нужно использовать Microsoft SQL Server 2008 R2 или более позднюю версию.

### Сведения о отзывах пользователей

MBAM 2,0 с пакетом обновления 1 (SP1) содержит свертку исправлений, устраняющих проблемы, обнаруженные с момента выпуска Microsoft BitLocker Administration and Monitoring (MBAM) 2,0. После внесения этих изменений поле "имя компьютера" появляется в отчетах о соответствии компьютера BitLocker и сведения о соответствии требованиям BitLocker Enterprise при запуске MBAM в Microsoft System Center Configuration Manager 2007.

### На портах портала самообслуживания и веб-сайта администрирования и мониторинга должны быть установлены исключения брандмауэра

При настройке портала самообслуживания и веб-сайта администрирования и мониторинга необходимо настроить исключение брандмауэра, чтобы разрешить связь через указанные порты. Ранее при установке сервера MBAM в брандмауэре Windows были автоматически открыты порты.

### Расположение MBAMных отчетов изменилось в Configuration Manager

Отчеты MBAM для интегрированной топологии Configuration Manager теперь доступны во вложенных папках в узле MBAM. Имена вложенных папок представляют язык отчетов во вложенной папке.

### Возможность установки MBAM на сервере первичного сайта при установке MBAM с помощью Configuration Manager

Вы можете установить MBAM на сервере первичного сайта или на сервере сайта центра администрирования при установке MBAM с топологией, интегрированной с Configuration Manager. Ранее вам требовалось установить MBAM на сервере сайта центра администрирования.

**Важно.**  
Сервер, на который устанавливается MBAM, должен быть сервером верхнего уровня в иерархии.



Установка MBAM работает по-другому для Microsoft System Center Configuration Manager 2007 и Microsoft System Center 2012 Configuration Manager, как описано ниже.

-   **Configuration Manager 2007** : Если вы устанавливаете MBAM на сервер первичного сайта, который является частью более крупной иерархии Configuration Manager и имеет родительский сервер центрального сайта, MBAM разрешает родительский сервер центрального сайта и выполняет все действия по установке на этом родительском сервере. Действия по установке включают в себя проверку предварительных требований и установку объектов и отчетов Configuration Manager. Например, если вы установили MBAM на основном сервере сайта, который является дочерним для основного сервера сайта, MBAM устанавливает все объекты и отчеты Configuration Manager на родительский сервер. Если вы установили MBAM на родительский сервер, MBAM выполняет все действия по установке на этом родительском сервере.

-   **Диспетчер конфигураций System Center 2012** : Если вы устанавливаете MBAM на сервер первичного сайта или на сервере центра администрирования, MBAM выполняет все действия по установке на сервере сайта.

### <a href="" id="-------------configuration-manager-console-must-be-installed-on-the--computer-on-which-you-install-the-mbam-server"></a> На компьютере, на котором устанавливается сервер MBAM, должна быть установлена консоль Configuration Manager

При установке MBAM с помощью встроенной топологии Configuration Manager необходимо установить консоль Configuration Manager на том же компьютере, на котором будет установлена MBAM. Если вы используете рекомендованную архитектуру, описанную в разделе [Приступая к работе с помощью MBAM в Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), установите MBAM на сервере основного сайта Configuration Manager.

### Новые параметры командной строки для встроенной топологии Configuration Manager

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Параметр командной строки</th>
<th align="left">Описание</th>
<th align="left">Пример.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CM_SSRS_REMOTE_SERVER_NAME</p></td>
<td align="left"><p>Позволяет установить отчеты Configuration Manager на удаленном сервере служб SQL Server Reporting Services (SSRS), который является частью того же сайта Configuration Manager, на который MBAM установлен. Вы можете присвоить этому параметру полное доменное имя сервера роли удаленной точки SSRS.</p></td>
<td align="left"><p>MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME = ssrsServer. contoso. com</p></td>
</tr>
<tr class="even">
<td align="left"><p>CM_REPORTS_ONLY</p></td>
<td align="left"><p>Позволяет устанавливать только отчеты Configuration Manager, не используя другие объекты Configuration Manager, например базовые элементы, коллекции и параметры конфигурации.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот параметр необходимо сочетать с параметром CM_REPORTS_COLLECTION_ID.</p>
</div>
<div>

</div>
<p>Допустимые значения параметров:</p>
<ul>
<li><p>True</p></li>
<li><p>False</p></li>
</ul>
<p>Вы можете сочетать этот параметр с параметром CM_SSRS_REMOTE_SERVER_NAME, если вы хотите установить отчеты только на сервер ролей удаленной точки SSRS.</p>
<p>Если параметр не задан или для него задано значение false, программа установки MBAM устанавливает все объекты Configuration Manager, включая отчеты.</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = true</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CM_REPORTS_COLLECTION_ID</p></td>
<td align="left"><p>Идентификатор существующей коллекции, указывающий коллекцию, для которой будут отображаться данные о соответствии требованиям. Вы можете указать любой идентификатор коллекции. Вы не обязаны использовать идентификатор семейства "MBAM поддерживаемые компьютеры".</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = true</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
</tbody>
</table>



### Возможность включения и отключения текста уведомления портала самообслуживания

MBAM 2,0 с пакетом обновления 1 (SP1) позволяет отключить текст уведомления на портале самообслуживания. Ранее текст уведомления отображается по умолчанию, и вы не можете отключить его.

**Отключение текста уведомления**

1.  На сервере, на котором установлен портал самообслуживания, откройте службы IIS и перейдите к **сайтам &gt; Администрирование Microsoft BitLocker и отслеживайте &gt; &gt; Параметры приложений Selfservice**.

2.  В столбце **имя** выберите **DisplayNotice**и установите для него значение **false**.

### Возможность локализовать инструкцию HelpdeskText, которая указывает пользователям на дополнительные сведения о портале самообслуживания

Вы можете настроить локализованную версию оператора самообслуживания на портале "HelpdeskText", который сообщает конечным пользователям о том, как получить дополнительные сведения о работе с порталом самообслуживания. Если вы настроили локализованный текст для инструкции, как описано в приведенных ниже инструкциях, MBAM отобразит локализованную версию. Если MBAM не удается найти локализованную версию, отобразится значение, заданное в параметре **HelpdeskText** .

**Отображение локализованной версии инструкции HelpdeskText**

1.  На сервере, на котором установлен портал самообслуживания, откройте IIS и перейдите к **сайтам &gt; Администрирование Microsoft BitLocker и отслеживайте &gt; &gt; Параметры приложений Selfservice**.

2.  В области **действия** нажмите кнопку **Добавить** , чтобы открыть диалоговое окно **Добавление параметра приложения** .

3.  В поле **Name (имя** ) введите **HelpdeskText**\ _ &lt; *Language* &gt; , где &lt; *Language* &gt; — код соответствующего языка для текста. Например, чтобы создать локализованную инструкцию HelpdeskText на испанском языке, вы можете назвать параметр HelpdeskText \ _es-ES. Список допустимых кодов языков, которые можно использовать, приведен в разделе [Справочник по API для поддержки языковых языков (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  В поле **value (значение** ) введите локализованный текст, который будет отображаться для конечных пользователей.

### Возможность локализовать портал самообслуживания HelpdeskURL

Вы можете настроить локализованную версию HelpdeskURL портала самообслуживания, которая будет отображаться для конечных пользователей по умолчанию. Если вы создаете локализованную версию, как описано в приведенных ниже инструкциях, MBAM находит и отображает локализованную версию. Если MBAM не удается найти локализованную версию, выводится URL-адрес, настроенный для параметра HelpDeskURL.

**Отображение локализованной HelpdeskURL**

1.  На сервере, на котором установлен портал самообслуживания, откройте IIS и перейдите к **сайтам &gt; Администрирование Microsoft BitLocker и отслеживайте &gt; &gt; Параметры приложений Selfservice**.

2.  В области **действия** нажмите кнопку **Добавить** , чтобы открыть диалоговое окно **Добавление параметра приложения** .

3.  В поле **Name (имя** ) введите **HelpdeskURL**\ _ &lt; *Language* &gt; (язык), где &lt; *Language* &gt; — код, соответствующий URL-адресу. Например, чтобы создать локализованный HelpdeskURL на испанском языке, вы можете назвать параметр HelpdeskURL \ _es-ES. Список допустимых кодов языков, которые можно использовать, приведен в разделе [Справочник по API на языке поддержки языков (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  В поле **value (значение** ) введите локализованные HelpdeskURL, которые должны отображаться для конечных пользователей.

### Возможность локализовать текст уведомления о портале самообслуживания

Вы можете настроить локализованный текст уведомлений, который будет отображаться для конечных пользователей по умолчанию на портале самообслуживания. Файл notice.txt, в котором отображается текст уведомления, расположен в следующем корневом каталоге:

&lt;Каталог установки самообслуживания *MBAM* &gt; Служба \\Self Website\\

Чтобы отобразить локализованный текст, нужно создать локализованный файл notice.txt и сохранить его в папке определенного языка в следующем каталоге:

&lt;Каталог установки самообслуживания *MBAM* &gt; Служба \\Self Website\\

MBAM отображает текст уведомления, основываясь на указанных ниже правилах.

-   Если вы создаете локализованный файл notice.txt в соответствующей папке языка, MBAM отображает локализованный текст уведомления.

-   Если MBAM не удается найти локализованную версию файла notice.txt, она отобразится в файле notice.txt по умолчанию.

-   Если MBAM не удается найти файл notice.txt по умолчанию, он отображает текст по умолчанию на портале самообслуживания.

**Примечание.**  
Если для браузера конечного пользователя выбран язык, для которого не указана соответствующая языковая вложенная папка или notice.txt, отобразится текст в файле notice.txt в следующем корневом каталоге:

&lt;Каталог установки самообслуживания *MBAM* &gt; Служба \\Self Website\\



**Создание локализованного notice.txt файла**

1.  На сервере, на котором установлен портал самообслуживания, создайте &lt; *language* &gt; папку языка в следующем каталоге, где &lt; *Language* &gt; — имя локализованного языка:

    &lt;Каталог установки самообслуживания *MBAM* &gt; Служба \\Self Website\\

    **Примечание.**  
    Некоторые языковые папки уже существуют, поэтому вам может потребоваться ее создать. Если вы хотите создать папку для языка, ознакомьтесь со справочными материалами о [поддержке языковых версий (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947) и просмотрите список допустимых имен, которые можно использовать для &lt; *language* &gt; папки языка.



2.  Создайте notice.txt файл, содержащий локализованный текст уведомления.

3.  Сохраните файл notice.txt в &lt; *language* &gt; папке Language. Например, чтобы создать локализованный файл notice.txt на испанском языке, вы должны сохранить локализованный файл notice.txt в следующей папке:

    &lt;Каталог установки самообслуживания *MBAM* &gt; Служба \\Self Website\\es-ES

## Обновление до MBAM 2,0 с пакетом обновления 1 (SP1)


Вы можете выполнить обновление до MBAM 2,0 SP1 из любой предыдущей версии MBAM.

### Обновление инфраструктуры MBAM

Вы можете обновить инфраструктуру сервера MBAM до MBAM 2,0 SP1 следующим образом:

**Замена на сервере вручную**: необходимо вручную удалить существующую инфраструктуру сервера MBAM, а затем установить инфраструктуру сервера MBAM 2,0 с пакетом обновления 1 (SP1). Вам не нужно удалять базы данных, чтобы выполнить обновление. Вместо этого вы выбираете существующие базы данных, которые были созданы в предыдущей версии MBAM. После того как MBAM 2,0 с пакетом обновления 1 (SP1) переносит существующие базы данных в MBAM 2,0 SP1.

**Обновление распределенного клиента**: Если вы используете автономную топологию MBAM, вы можете сразу обновить клиенты MBAM после установки инфраструктуры сервера MBAM 2,0 с пакетом обновления 1 (SP1).

После того как вы обновите инфраструктуру сервера MBAM, клиенты MBAM 1,0 или 2,0 будут успешно сообщать сервер MBAM 2,0 SP1 и сохранит данные для восстановления, но соответствие требованиям будет основано на политиках, доступных для версии MBAM клиента, установленной в настоящее время. Чтобы включить отчеты о политиках MBAM 2,0 с пакетом обновления 1 (SP1), необходимо обновить клиентские компьютеры до MBAM 2,0 SP1. Вы можете обновить клиентские компьютеры до MBAM 2,0 с пакетом обновления 1 (SP1) без удаления прежнего клиента, после чего клиент начнет применять и сообщать о них, основываясь на политиках MBAM 2,0 с пакетом обновления 1 (SP1).

Дополнительные сведения об обновлении MBAM серверов можно найти в разделе [Обновление предыдущих версий MBAM](upgrading-from-previous-versions-of-mbam.md).

### Обновление клиента MBAM до MBAM 2,0 с пакетом обновления 1 (SP1)

Чтобы обновить компьютеры конечных пользователей до клиента MBAM 2,0 SP1, запустите **MbamClientSetup.exe** на каждом клиентском компьютере. Установщик автоматически обновляет клиент для клиента MBAM 2,0 SP1. После установки клиентские компьютеры не требуется перезагружать, а клиент MBAM 2,0 SP1 начинает применять и сообщать о политиках MBAM 2,0 с пакетом обновления 1 (SP1).

Если вы используете MBAM с Configuration Manager, вы должны обновить клиентские компьютеры MBAM до MBAM 2,0 с пакетом обновления 1 (SP1).

Дополнительные сведения о том, как обновить клиентские компьютеры MBAM, можно найти в разделе [обновление с предыдущей версии MBAM](upgrading-from-previous-versions-of-mbam.md).

## Установка и обновление до MBAM 2,0 с пакетом обновления 1 (SP1) с помощью Configuration Manager


В этом разделе описаны требования при установке MBAM 2,0 SP1 как новой установки или обновления предыдущей версии MBAM 2,0 с пакетом обновления 1 (SP1).

### Файлы, необходимые для установки MBAM 2,0 с пакетом обновления 1 (SP1), если вы используете MBAM в Configuration Manager

Если вы устанавливаете MBAM в первый раз и используете MBAM 2,0 SP1 с помощью System Center Configuration Manager, вы должны создать или изменить MOF-файлы, чтобы обеспечить правильную работу MBAM в Configuration Manager.

-   **MOF-файл Configuration.**

    -   Если вы используете Configuration Manager 2007, вам необходимо изменить файл Configuration. mof, выполнив шаг 3 из элемента **Обновление файла Configuration. mof, если вы обновите систему до MBAM 2,0 SP1 и используете MBAM с Configuration Manager 2007**, который следует за этим элементом.

    -   Если вы используете System Center 2012 Configuration Manager, измените файл Configuration. mof, следуя инструкциям в разделе [изменение файла Configuration. mof](edit-the-configurationmof-file.md).

-   **SMS \ _def. mof** — следуйте инструкциям в разделе [Создание или изменение файла SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md).

### Обновление файла Configuration. mof при переходе на MBAM 2,0 с пакетом обновления 1 (MBAM) с помощью Configuration Manager 2007

Если вы выполняете обновление до MBAM 2,0 SP1 и используете MBAM с Configuration Manager 2007, необходимо обновить файл Configuration. mof, чтобы убедиться, что MBAM 2,0 SP1 работает правильно.

**Чтобы обновить файл Configuration. mof, выполните указанные ниже действия.**

1.  На сервере Configuration Manager перейдите в расположение файла Configuration. mof.

    &lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv\\

    При установке по умолчанию в качестве расположения установки используется%systemdrive%\\Program Files (x86) \\Microsoft Configuration Manager.

2.  Проверьте блок кода, который вы добавите в файл Configuration. mof, и удалите его. Блок кода будет выглядеть примерно так, как показано на следующем этапе.

3.  Скопируйте приведенный ниже блок кода и добавьте его в файл Configuration. mof, чтобы добавить в файл указанные ниже требуемые классы MBAM:

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 

    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy 64";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

### Перевод MBAM 2,0 SP1

MBAM 2,0 с пакетом обновления 1 (SP1) теперь доступен на следующих языках:

-   Английский (США) EN-US
-   Французский (Франция) fr-FR
-   Итальянский (Италия) IT-IT
-   Немецкий (Германия) de-DE
-   Испанский, Международная Сортировка (Испания) ES-ES
-   Корейский (Корея) ko-KR
-   Японский (Япония) ja-JP
-   Португальский (Бразилия) Пт — BR
-   Русский (Россия) ru-RU
-   Китайская традиционная zh-TW
-   Китайский (упрощенное письмо) — CN

## Получение технологий для MDOP

MBAM 2,0 с пакетом обновления 1 (SP1) входит в состав пакета оптимизации для настольных систем Майкрософт (MDOP). MDOP входит в состав Microsoft Software Assurance. Дополнительные сведения о программе Software Assurance и приобретении MDOP можно найти в [статьях получение MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Статьи по теме

[Заметки о выпуске для MBAM 2.0 с пакетом обновления 1 (SP1)](release-notes-for-mbam-20-sp1.md)









