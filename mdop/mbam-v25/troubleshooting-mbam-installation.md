---
title: Устранение неполадок, возникающих при установке MBAM 2.5
description: Введение устранения неполадок с установкой MBAM 2.5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 6ea152792801c630fa365f37d1668d1a4d84b3a5
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910634"
---
# <a name="troubleshooting-mbam-25-installation-problems"></a>Устранение неполадок, возникающих при установке MBAM 2.5

В этой статье повеяна устранение неполадок с установкой Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 в автономных конфигурациях.

## <a name="referring-mbam-log-files-for-troubleshooting"></a>Ссылки на файлы журналов MBAM для устранения неполадок

MBAM включает ведение журнала для установки сервера, установки клиента и событий. Этот журнал следует использовать для устранения неполадок. 
 
### <a name="mbam-server-installation-log-files"></a>Файлы журнала установки сервера MBAM

MBAMServerSetup.exe создает следующие файлы журнала в папке %temp% пользователя во время установки MBAM:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14 номеров>.log**

MBAMServerSetup.exe записываю действия, принятые во время установки MBAM и установки функций сервера MBAM:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers>_0_MBAMServer.msi.log**

MBAMServerSetup.exe журналы дополнительных действий, которые были приняты во время установки.

### <a name="mbam-client-installation-log-file"></a>Файл журнала установки клиента MBAM

Установка клиента записуется в следующем файле журнала в папке %temp% (или настраиваемом расположении, в зависимости от того, как был установлен клиент): <br />**MSI \<five random characters\> .log**

В этом журнале содержатся действия, которые принимаются во время установки клиента MBAM.
 
### <a name="mbam-client-event-logging-channel"></a>Канал ведения журнала событий для клиентов MBAM

MBAM имеет отдельные каналы ведения журнала событий. Файлы журналов администратора, аналитики и операционных журналов находятся в viewer событий в журнале **Приложений**и служб  >  **Microsoft**  >  **Windows**  >  **MBAM**.

В следующей таблице приводится краткое описание каждого журнала событий.
 
|Журнал событий| Описание|
|----------|-------|
|Microsoft-Windows-MBAM/Admin|  Содержит сообщения об ошибках|
|Microsoft-Windows-MBAM/Analytic|   Содержит расширенные сведения о журнале|
|Microsoft-Windows-MBAM/Operational|    Содержит сообщения об успехе|

### <a name="mbam-server-event-logging-channel"></a>Канал ведения журнала событий на сервере MBAM

Файлы журнала находятся в viewer событий, в журнале **Приложения**и Службы  >  **Microsoft**  >  **Windows**  >  **MBAM**. В следующей таблице представлены журналы событий сервера, которые были представлены в MBAM 2.5:

|Журнал событий| Описание|
|--------|-------------|
|Microsoft-Windows-MBAM/Admin|  Содержит сообщения об ошибках|
|Microsoft-Windows-MBAM/Analytic|   Содержит расширенные сведения о журнале|
|Microsoft-Windows-MBAM/Operational|    Содержит сообщения об успехе|

### <a name="mbam-web-service-logs"></a>Журналы веб-служб MBAM

Каждый журнал веб-службы MBAM записывает сведения о журнале в файл SVCLOG. По умолчанию каждая веб-служба записывает файл трассировки в папку, которая использует свое имя в папке C:\inetpub\Microsoft BitLocker Management Solution\Logs.

Вы можете использовать средство просмотра трассировки службы (часть Microsoft Visual Studio) для проверки трассировок svclog.

## <a name="troubleshooting-encryption-and-reporting-issues"></a>Устранение проблем с шифрованием и отчетами

В этом разделе содержатся сведения об устранении неполадок для функциональных возможностей сервера, функциональных возможностей клиентов, параметров конфигурации и известных проблем:
 
### <a name="mbam-client-installation-group-policy-settings"></a>Установка клиента MBAM, параметры групповой политики

Определите, установлен ли агент MBAM на клиентском компьютере. При установке MBAM создается служба с именем Клиентская служба управления BitLocker. Эта служба настроена для автоматического запуска. Определите, запущена ли служба.

Убедитесь, что параметры групповой политики MBAM применяются на клиентском компьютере. Если параметры групповой политики были применены на клиентских компьютерах, создается следующий подмыв ** реестра:HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

Убедитесь, что этот ключ существует и заполняется с помощью значений для параметров групповой политики.

### <a name="mbam-agent-in-the-initial-delay-period"></a>Агент MBAM в начальный период задержки

Клиент MBAM не начинает операцию сразу после установки. Перед началом работы агента MBAM существует начальная случайная задержка в 1-18 минут. В дополнение к начальной задержке задержка составляет не менее 90 минут. (Задержка зависит от параметров групповой политики, настроенных для частоты проверки состояния клиента.) Таким образом, общая задержка перед началом операции клиента — это случайная задержка задержки **  +  *клиентской проверки частоты*запуска.

Если журналы событий Operational и Admin пусты, клиент еще не начал операцию и находится в периоде задержки, который был упомянут ранее. Если вы хотите обойти задержку, выполните следующие действия:
 
1. Остановите службу клиентской службы управления BitLocker.

2. В соответствии **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM** реестра создайте значение **реестра NoStartupDelay,** установите его тип **REG_DWORD,** а затем установите его значение **до 1**.

3. В **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**установите значения **ClientWakeupFrequency** и **StatusReportingFrequency** до **1**. Эти значения будут вернуться к исходным настройкам после обновления групповой политики на компьютере.

4. Запустите службу клиентской службы управления BitLocker.

После начала службы при локальном входе на компьютер и без ошибок следует получить запрос на шифрование компьютера в течение одной минуты. Если вы не получили запрос, необходимо просмотреть журналы администратора MBAM для любых записей об ошибках.

### <a name="computer-does-not-have-a-tpm-device-or-the-tpm-device-is-not-enabled-in-the-bios"></a>Компьютер не имеет устройства TPM, или устройство TPM не включено в BIOS

Просмотрите журнал событий администрирования MBAM. В журнале событий администрирования MBAM вы увидите запись события, напоминаемую ниже:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

Откройте управление TPM (tpm.msc) и проверьте, есть ли на компьютере устройство TPM. Если tpm.msc не показывает устройство, откройте диспетчер устройств (devmgmt.msc) и проверьте, есть ли модуль доверенных платформ под устройствами безопасности. Если вы не видите устройство Доверенный модуль платформы, это может быть верно по одной из следующих причин:

* В вашей системе нет устройства Trusted Platform Module (TPM/Security).

* Устройство TPM отключено в BIOS.

* Устройство TPM включено в BIOS, но управление устройством TPM из параметра операционной системы отключено в BIOS.

* Драйвер Microsoft для устройства TPM не используется. Просмотрите устройства, указанные в диспетчере устройств, чтобы определить драйвер устройства Microsoft TPM.

Если устройство TPM не использует драйвер C:\Windows\System32\tpm.sys, необходимо обновить драйвер, выбрав файл C:\Windows\Inf\tpm.inf.

### <a name="computer-does-not-have-a-valid-system-partition"></a>Компьютер не имеет допустимой раздел SYSTEM

Просмотрите журнал событий администрирования MBAM. В журнале событий администрирования MBAM вы увидите запись события, напоминаемую ниже:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

BitLocker требует раздел SYSTEM, чтобы включить шифрование[(Шифрование диска BitLocker в Windows 7. Часто задамые вопросы).](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)

MBAM не создает раздел системы автоматически. Вы можете использовать утилиту подготовки диска BitLocker (bdehdcfg.exe) для создания раздела системы и перемещения необходимых файлов запуска.

Например, можно использовать команду **%windir%\system32\bdeHdCfg.exe -target default-size 300 -quiet,** чтобы безмолвно подготовить диск перед развертыванием MBAM для шифрования дисков. Это требует перезапуска. Вы также можете сценарий действия, если это необходимо. В следующем документе описывается средство подготовки к диску BitLocker:

[Описание средства подготовки диска BitLocker](https://support.microsoft.com/help/933246)

### <a name="drives-are-not-formatted-to-have-a-compatible-file-system"></a>Диски не форматированы, чтобы иметь совместимую файловую систему

Подробнее о требованиях к файловой системе для BitLocker см. в статье [TechNet.](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements)

### <a name="group-policy-conflict"></a>Конфликт групповой политики

В журнале событий администрирования MBAM вы увидите запись события, напоминаемую ниже:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

Проверьте параметры групповой политики, чтобы убедиться, что у вас нет конфликтующих параметров среди параметров групповой политики MBAM.

Следует настроить групповую политику с помощью шаблона MDOP MBAM, а не шаблона шифрования диска BitLocker.

Пример:

В настройках шифрования дисков операционной системы вы выбрали TPM в качестве протектора, а также разрешить расширенные ПИН-коды **для запуска.** Это противоречивые параметры, так как защита только для TPM не требует ПИН-кода. Поэтому необходимо отключить расширенный параметр ПИН-параметров.

### <a name="user-may-have-requested-an-exemption"></a>Пользователь, возможно, запросил освобождение

Если включен параметр Конфигурация компьютера\Административные шаблоны\Windows компоненты\MDOP MBAM (BitLocker Management)\Client Management\Configure user exemption Policy Group Policy, пользователям будет предложено запросить освобождение.

По умолчанию, если пользователь запрашивает освобождение, освобождение будет действительным в течение 7 дней, и пользователь не будет получать подсказки для шифрования в течение этого периода. (Значение по умолчанию может быть увеличено или уменьшено во время конфигурации политики.) После окончания периода освобождения пользователю будет предложено шифровать.

Вы увидите следующую запись в журнале событий администрирования MBAM, когда компьютер находится под исключением пользователей:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

Если вы хотите вручную переопредить освобождение пользователя для компьютера, выполните следующие действия:
 
1. Установите значение AllowUserExemption **до 0** в следующем подкайке реестра: <br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

2. Удаление всех значений реестра в следующем подкоже реестра, за исключением **AgentVersion,** **EncodedComputerName**и **Installed:**<br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM**

    **Примечание** Чтобы изменения вступили в силу, необходимо перезапустить агента MBAM.

Следует помнить, что после применения групповой политики к компьютеру эти значения могут вернуться к исходным настройкам.

### <a name="wmi-issue"></a>Проблема WMI

MBAM использует методы класса win32_encryptablevolume для управления BitLocker. Если этот модуль незарегистрирован или поврежден, клиент MBAM не будет работать правильно, и вы увидите следующую запись события в журнале событий администрирования MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

Кроме того, вы можете заметить, что политики восстановления и оборудования не применяются с кодом 0x8007007e. Это переводится как "Указанный модуль не удалось найти".

Чтобы устранить эту проблему, необходимо **перерегистровать** класс win32_encryptablevolume с помощью следующей команды:

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## <a name="troubleshooting-mbam-agent-communication-issues"></a>Устранение неполадок в связи с агентом MBAM

В этом разделе содержатся сведения об устранении неполадок по следующим вопросам, связанным с коммуникацией агента MBAM:

### <a name="incorrect-mbam-service-url"></a>Неправильный URL-адрес службы MBAM

Если значение службы соответствия требованиям MBAM или службы восстановления и оборудования неверно, на клиентском компьютере будет указана запись события, напоминаемая следующей в журнале событий администрирования MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

Проверка значений **KeyRecoveryServiceEndPoint** и **StatusReportingServiceEndpoint** в следующей подкамере реестра на клиентский компьютер: <br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

По умолчанию URL-адрес keyRecoveryServiceEndPoint (конечной точки восстановления и службы оборудования MBAM) находится в следующем формате: <br />
**http://: \<servername\> \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc**

По умолчанию URL-адрес statusReportingServiceEndpoint (конечная точка службы отчетов о состоянии MBAM) находится в следующем формате:<br />
**http://: \<servername\> \<port\> /MBAMComplianceStatusService/StatusReportingService.svc**

> [!Note]
> В URL-адресе не должно быть пробелов.

Если URL-адрес службы неверен, необходимо исправить URL-адрес службы в следующем параметре групповой политики:

**Конфигурация компьютера**  >  **Политики**  >  **Административные шаблоны**  >  **Windows компоненты**  >  **MDOP MBAM (BitLocker Management)**  >  **Управление клиентом**  >  **Настройка служб MBAM**

### <a name="connectivity-issue-that-affects-the-mbam-administration-server"></a>Проблема подключения, которая влияет на сервер администрирования MBAM

Агент MBAM не сможет размещать какие-либо обновления в базе данных, если между агентом клиента и сервером администрирования MBAM существуют проблемы с подключением. В этом случае вы заметите записи о сбоях подключения в журнале событий администрирования MBAM на клиентском компьютере:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

Основные проверки:

* Проверьте базовую возможность подключения, укатав сервер администрирования MBAM по имени и IP. Проверьте, можно ли подключиться к веб-сайту администрирования MBAM или порту службы с помощью telnet или portqry.

* Убедитесь, что служба IIS работает на сервере администрирования и мониторинга MBAM и что веб-служба MBAM прослушивается в том же порте, который настроен на клиентском компьютере MBAM ( `netstat –ano | find "portnumber"` ).

* Убедитесь, что номер порта, настроенный для веб-сайта MBAM, использует IIS Manager (inetmgr). Убедитесь, что номер порта такой же, как и номер порта, на котором прослушивается клиент. Убедитесь, что номер порта не является общим для другого приложения. Например, другое приложение на сервере не должно использовать тот же порт.

* Если есть брандмауэр, убедитесь, что порт открыт на брандмауэре или прокси-сервере.

* Если связь между клиентом и сервером безопасна, убедитесь, что вы используете допустимый сертификат SSL.

* Проверка подключения к сети между веб-сервером и сервером базы данных, на который отправляются данные для вставки. Подключение базы данных с веб-сервера к серверу базы данных можно проверить с помощью администратора источника данных ODBC. Подробные SQL Server для устранения неполадок подключения доступны в инструкции По устранению неполадок подключение к [SQL Server ядро СУБД](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).

#### <a name="troubleshooting-the-connectivity-issue"></a>Устранение неполадок с подключением

Убедитесь, что URL-адрес службы, настроенный на клиента, является правильным. Скопируйте значение URL-адреса для KeyRecoveryServiceEndPoint** (HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement) **из реестра и откройте его в Internet Explorer.

Аналогично скопируйте значение URL-адреса statusReportingServiceEndpoint** (HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement) **и откройте его в Internet Explorer.

> [!Note]
> Если вы не можете просмотреть URL-адрес с клиентского компьютера, необходимо проверить базовую подключение к сети от клиента к серверу, на который запущен IIS. См. пункты 1, 2, 3 и 4 в предыдущем разделе.

Кроме того, просмотрите журналы приложений на сервере администрирования и мониторинга на любые ошибки.

Вы можете сделать одновременное сетевое трассировку между клиентом и сервером и просмотреть след, чтобы определить причину сбоя подключения между агентом клиента и сервером администрирования MBAM.

> [!Note]
> Если вы можете просматривать URL-адреса службы с клиентского компьютера и в журналах событий администрирования MBAM есть записи об ошибках подключения, это может быть из-за сбоя подключения между сервером администрирования и сервером базы данных.

Если вы можете успешно просматривать URL-адреса службы, а между клиентом и запущенным сервером есть подключение, iiS работает. Однако может возникнуть проблема в связи между сервером, на который работает IIS, и сервером базы данных.

Службы MBAM могут быть не в состоянии подключиться к серверу базы данных из-за сетевой проблемы или неправильного параметра подключения к базе данных. Просмотрите журналы приложений на сервере администрирования и мониторинга. Вы можете видеть ошибки или предупреждения из источника ASP.NET 2.0.50727.0, которые напоминают следующую запись журнала:

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### <a name="possible-causes"></a>Возможные причины

##### <a name="cause-1"></a>Причина 1

При установке компонентов администрирования и мониторинга серверов администратор мог задать имя недействительных экземпляров базы данных или имени базы данных.

Вы можете проверить и исправить строки подключения к базе данных с помощью консоли УПРАВЛЕНИЯ IIS. Для этого откройте диспетчер IIS и просмотрите администрирование и мониторинг Microsoft BitLocker. Для каждой службы, которая указана слева, выполните следующие действия, чтобы изменить строки подключения к базе данных:

1. В **Представлении функций**дважды выберите **строки подключения.**

2. На странице **Строки подключения** выберите строку подключения, которую необходимо изменить.

3. В области **Действия** выберите **Изменить**.

4. В **диалоговом** окне Изменить строку подключения измените свойства, которые необходимо изменить, а затем выберите **ОК.**

##### <a name="cause-2"></a>Причина 2

SQL Server заблокирован в брандмауэре. Проверьте номер порта, на который SQL Server для прослушивания, и убедитесь, что порт открыт в брандмауэре между сервером администрирования и сервером базы данных.

##### <a name="cause-3"></a>Причина 3

Неправильные SQL TCP/IP-привязки сервера. Проверка SQL TCP/IP-привязки в диспетчер конфигурации SQL Server на сервере базы данных. MBAM требует, чтобы протоколы TCP/IP и Named Pipes были подключены к базе данных.

##### <a name="cause-4"></a>Причина 4

Учетная запись NT Authority\Network Service или компьютерная учетная запись сервера администрирования MBAM не имеет необходимых разрешений для подключения к SQL базе данных.

Во время установки компонентов базы данных на сервере базы данных установщик создает две локальные группы: аудит соответствия требованиям MBAM DB Access и MBAM Recovery and Hardware DB Access.

Учетная запись NT Authority\Network Service, компьютерная учетная запись сервера администрирования MBAM и пользователь, устанавливавший компоненты базы данных, автоматически добавляются в эти группы.

Эти группы получили необходимые разрешения в базе данных во время установки. Все пользователи, которые являются частью этой группы, автоматически получают необходимые разрешения в базе данных.

Веб-служба может не подключаться к серверу базы данных из-за проблемы с разрешениями, если одно или несколько из следующих условий верны:

* Упомянутые ранее группы удаляются из локальных групп на сервере базы данных.

* Учетная запись NT Authority\Network Service и компьютерная учетная запись сервера администрирования MBAM не являются членами этих групп.

* Эти группы не имеют необходимых разрешений в базе данных.

Вы заметите ошибки, связанные с разрешениями, в журналах приложений в администрировании MBAM и на сервере мониторинга, если какие-либо из предыдущих условий верны. В этом случае необходимо вручную добавить учетную запись NT Authority\Network Service и компьютерную учетную запись сервера администрирования MBAM и предоставить им общедоступные роли на сервере SQL базы данных, использующем SQL Server Management Studio . https://msdn.microsoft.com/library/aa337562.aspx) .

#### <a name="review-the-web-service-logs"></a>Просмотр журналов веб-служб

Если на сервере администрирования MBAM не регистрируются события в журналах приложений, пора просмотреть журналы веб-служб (.svclog) веб-службы MBAM, которая находится на сервере администрирования и мониторинга MBAM. Для просмотра файла журнала необходимо использовать средство просмотра трассировки службы https://msdn.microsoft.com/library/ms732023.aspx (SvcTraceViewer.exe).

В первую очередь следует исследовать журналы трассировки служб RecoveryandHardwareService и ComplianceStatusService. По умолчанию журналы веб-служб находятся в папке C:\inetpub\Microsoft BitLocker Management Solution\Logs. Там каждая служба пишет свой файл svclog в своей папке.

Просмотрите действия в журнале трассировки службы для любых ошибок или предупреждений. По умолчанию записи ошибок выделены красным цветом. Выберите описание ошибки на правой области просмотра трассировки, чтобы просмотреть подробные сведения о записи ошибки. Ниже приводится пример записи ошибки из журнала трассировки:

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## <a name="re-installation-or-reconfiguration-of-mbam-infrastructure"></a>Переустановка или перенастройка инфраструктуры MBAM

Чтобы повторно установить или перенастроить инфраструктуру MBAM, необходимо знать следующие вещи:

* Учетная запись пула приложений

* Группы MBAM (Helpdesk, Advanced, Report Users Group)

* URL-адрес отчетов MBAM

* SQL Server имя и имена баз данных

* Учетные записи MBAM ReadWrite и ReadOnly

### <a name="application-pool-account"></a>Учетная запись пула приложений

Чтобы найти учетную запись пула приложений, войдите на веб-сервер MBAM, откройте **службы IIS (IIS) Manager,** а затем выберите **пулы приложений:**

![пулы приложений.](images/troubleshooting-MBAM-installation-1.png)

Основное имя службы (SPN) должно быть установлено в этой учетной записи. Этот параметр очень важен для функциональности MBAM.

### <a name="mbam-groups-helpdesk-advanced-report-users-group-and-reports-url"></a>Группы MBAM (url-адрес helpdesk, Advanced, Report Users Group и Reports)

![ГРУППЫ MBAM.](images/troubleshooting-MBAM-installation-2.png)

Это предоставляет такие сведения, как Helpdesk Group, Advanced Helpdesk Group, Report Users Group и URL-адрес отчетов MBAM. URL-адрес отчетов MBAM должен быть указан в установке MBAM и читаться по адресу: http(s)://servername/ReportServer.

### <a name="sql-server-name-and-database-db-names"></a>SQL Server имя и имена баз данных (DB)

Чтобы найти SQL Server и экземпляры, в которых размещены DBs MBAM, войдите на сервер MBAM Web (IIS) и просмотрите подкою реестра folowing:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web**

![Regedit.](images/troubleshooting-MBAM-installation-3.png)

Выделенные части — это строки подключения. Они должны иметь SQL Server, имена баз данных и экземпляры (если они названы).

### <a name="mbam-readwrite-and-readonly-accounts"></a>Учетные записи MBAM ReadWrite и ReadOnly

Эти сведения будут в SQL Server, для которой мы уже нашли имя с веб-сервера.

#### <a name="readwrite-account"></a>Учетная запись ReadWrite

1. Войдите в SQL Management Studio.

2. Щелкните правой **кнопкой мыши восстановление MBAM и оборудование,** выберите **свойства,** а затем выберите **Разрешения**.

Например, имя учетной записи лаборатории **— MBAMWrite.** Учетные записи Пула приложений и ReadWrite должны быть одинаковыми.

![SQL DB.](images/troubleshooting-MBAM-installation-4.png)

![Свойства DB.](images/troubleshooting-MBAM-installation-5.png)

Просмотрите **службу Безопасности,** **а** затем войдите в SQL Management Studio. Просмотрите учетную запись, показанную на предыдущем скриншоте.

![SQL Безопасность.](images/troubleshooting-MBAM-installation-6.png)

Щелкните правой кнопкой мыши учетные записи, перейдите к **сопоставлению**пользователей свойств и найдите базу данных восстановления и оборудования MBAM:

![Сопоставление пользователей.](images/troubleshooting-MBAM-installation-7.png)

#### <a name="readonly-account"></a>Учетная запись ReadOnly

Откройте SQL Server Reporting Services диспетчер конфигурации на сервере SSRS. Выберите **URL-адрес диспетчера отчетов**и просмотрите **URL-адреса:**

![Диспетчер отчетов.](images/troubleshooting-MBAM-installation-8.png)

Выберите **администрирование и мониторинг битлокера**Майкрософт:

![Администрирование и мониторинг bitlocker.](images/troubleshooting-MBAM-installation-9.png)

Выберите **MaltaDatasource:**

![DBs.](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource.](images/troubleshooting-MBAM-installation-11.png)

MaltaDataSource должна иметь имя учетной записи ReadOnly и должна использоваться в установке MBAM.

## <a name="reference"></a>Справочники

Дополнительные сведения доступны в следующих статьях.

[Развертывание MBAM 2.5 в автономных конфигурациях](https://support.microsoft.com/help/3046555)

[Microsoft BitLocker Administration and Monitoring 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
