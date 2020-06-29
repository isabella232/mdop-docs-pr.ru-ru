---
title: Устранение неполадок, возникающих при установке MBAM 2.5
description: В этой статье объясняется, как устранить проблемы с установкой MBAM 2,5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: ed56a87496e09601c44028b7f948eda39143e8c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812864"
---
# Устранение неполадок, возникающих при установке MBAM 2.5

В этой статье объясняется, как устранить проблемы с установкой Microsoft BitLocker для администрирования и мониторинга (MBAM) 2,5 в автономной конфигурации.

## Обращение к файлам журнала MBAM для устранения неполадок

MBAM включает ведение журнала для установки сервера, установки клиентов и событий. Это ведение журнала должно быть рекомендовано для устранения неполадок. 
 
### Файлы журнала установки сервера MBAM

MBAMServerSetup.exe создает следующие файлы журнала в папке% temp% пользователя при установке MBAM:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14 номеров>. log**

В MBAMServerSetup.exe регистрируются действия, которые были предприняты при установке компонентов MBAM и MBAM Server.<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers # C1_0_MBAMServer.msi. log**

MBAMServerSetup.exe заносит в журнал дополнительные действия, предпринятые во время установки.

### Файл журнала установки клиента MBAM

Установка клиента записывается в следующем файле журнала в папке% Temp% (или в другом расположении в зависимости от того, как был установлен клиент). <br />**MSI \<five random characters\> . log**

Этот журнал включает действия, которые выполняются во время установки клиента MBAM.
 
### Событие клиента MBAM — канал ведения журнала

В MBAM есть отдельные каналы ведения журнала событий. Файлы журнала администрирования, аналитики и операционной системы находятся в окне "Просмотр событий" в разделе **журналы приложений и служб**в  >  **Microsoft**  >  **Windows**  >  **MBAM**.

В таблице ниже приведено краткое описание каждого журнала событий.
 
|Журнал событий| Описание|
|----------|-------|
|Microsoft-Windows-MBAM/администратор|  Содержат сообщения об ошибках|
|Microsoft-Windows-MBAM/аналитический|   Дополнительные сведения для ведения журнала|
|Microsoft-Windows-MBAM/Operational|    Содержат сообщения об успешном завершении|

### Событие сервера MBAM — канал ведения журнала

Файлы журнала находятся в окне просмотра событий, в разделе **журналы приложений и служб**в  >  **Microsoft**  >  **Windows**  >  **MBAM**. В таблице ниже указаны журналы событий сервера, которые появились в MBAM 2,5:

|Журнал событий| Описание|
|--------|-------------|
|Microsoft-Windows-MBAM/администратор|  Содержат сообщения об ошибках|
|Microsoft-Windows-MBAM/аналитический|   Дополнительные сведения для ведения журнала|
|Microsoft-Windows-MBAM/Operational|    Содержат сообщения об успешном завершении|

### Журналы веб-службы MBAM

Каждый журнал веб-службы MBAM записывает данные журнала в файл SVCLOG. По умолчанию каждая веб-служба записывает файл трассировки в папку, которая использует ее имя в папке Solution\Logs управления C:\inetpub\Microsoft BitLocker.

Вы можете использовать средство просмотра служебной трассировки (часть Microsoft Visual Studio) для просмотра трассировок SVCLOG.

## Устранение неполадок, связанных с шифрованием и отчетами

В этом разделе содержатся сведения об устранении неполадок, возникающих в компонентах сервера, клиентах, параметрах конфигурации и известных проблемах.
 
### Установка клиента MBAM, параметры групповой политики

Определение того, установлен ли агент MBAM на клиентском компьютере. При установке MBAM создается служба, которая называется службой клиента управления BitLocker. Эта служба настроена на автоматический запуск. Определите, работает ли служба.

Убедитесь, что параметры групповой политики MBAM применяются на клиентском компьютере. Если на клиентском компьютере были применены параметры групповой политики, создается следующий подраздел реестра: **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**

Убедитесь в том, что этот раздел существует и заполнен с помощью значений в параметрах групповой политики.

### Агент MBAM в начальном периоде задержки

Клиент MBAM не запускает операцию сразу после установки. Начальная случайная задержка составляет 1 – 18 минут, прежде чем агент MBAM начинает операцию. В дополнение к начальной задержке, задержка не должна быть менее 90 минут. (Задержка зависит от параметров групповой политики, которые настроены на частоту проверки состояния клиента.) Таким образом, Общая задержка перед началом работы клиента — задержка *случайной задержки при запуске*  +  *client checking frequency delay*.

Если журналы событий для операционной и для администраторов пусты, клиент еще не начал операцию и находится в период задержки, упомянутый ранее. Если вы хотите обойти эту задержку, выполните указанные ниже действия.
 
1. Остановите службу клиента управления BitLocker.

2. В разделе реестра **HKEY_LOCAL_MACHINE \software\microsoft\mbam** Создайте значение реестра **NoStartupDelay** , задайте для него тип **REG_DWORD**и установите для него значение **1**.

3. В разделе **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**задайте для параметров **ClientWakeupFrequency** и **StatusReportingFrequency** значение **1**. Эти значения будут возвращены к исходным параметрам после обновления групповой политики на компьютере.

4. Запустите службу клиента управления BitLocker.

После запуска службы при локальном входе на компьютер и отсутствии ошибок вы должны получить запрос на шифрование компьютера в течение одной минуты. Если вы не получили запрос, проверьте, нет ли в журналах администратора MBAM записи об ошибках.

### На компьютере отсутствует доверенный платформенный модуль или устройство TPM не включено в BIOS

Просматривайте журнал событий администратора MBAM. В журнале событий администрирования MBAM появляется запись о событии, аналогичную приведенной ниже.

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

Откройте консоль управления TPM (TPM. msc) и убедитесь, что на компьютере есть устройство TPM. Если в TPM. msc не отображается устройство, откройте Диспетчер устройств (devmgmt. msc) и проверьте наличие доверенного платформенного модуля в разделе "устройства безопасности". Если вы не видите устройство доверенного платформенного модуля, это может быть вызвано одной из указанных ниже причин.

* У вашей системы нет устройства доверенного платформенного модуля (TPM/Security).

* Устройство доверенного платформенного модуля отключено в BIOS.

* В BIOS включено устройство TPM, но управление устройством TPM из параметра операционной системы отключено в BIOS.

* Вы не используете драйвер Microsoft для устройства доверенного платформенного модуля. Ознакомьтесь с устройствами, указанными в диспетчере устройств, чтобы определить драйвер устройства доверенного платформенного модуля (Майкрософт).

Если устройство доверенного платформенного модуля не использует драйвер C:\Windows\System32\tpm.sys, необходимо обновить драйвер, выбрав файл C:\Windows\Inf\tpm.inf.

### На компьютере отсутствует допустимый системный раздел

Просматривайте журнал событий администратора MBAM. В журнале событий администрирования MBAM появляется запись о событии, аналогичную приведенной ниже.

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

Для включения шифрования BitLocker требуется системный раздел ([Шифрование диска BitLocker в Windows 7: часто задаваемые вопросы](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).

MBAM не создает системный раздел автоматически. Вы можете использовать служебную программу подготовки диска для BitLocker (bdehdcfg.exe) для создания системного раздела и перемещения необходимых файлов загрузки.

Например, вы можете использовать команду **% WINDIR% \system32\bdeHdCfg.exe-Target (размер по умолчанию) 300 – quiet** , чтобы подготовить диск без уведомления, прежде чем развертывать MBAM, чтобы зашифровать диски. Для этого требуется перезагрузка. Вы также можете создать сценарий действия, если это необходимо. В следующем документе описан инструмент подготовки диска для BitLocker:

[Описание средства подготовки диска для BitLocker](https://support.microsoft.com/help/933246)

### Диски не отформатированы для использования совместимой файловой системы

Ознакомьтесь со [статьей TechNet о требованиях файловой системы для BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).

### Конфликт групповых политик

В журнале событий администрирования MBAM появляется запись о событии, аналогичную приведенной ниже.

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

Проверьте параметры групповой политики, чтобы убедиться в отсутствии конфликта между параметрами групповой политики MBAM.

Групповую политику следует настроить с помощью шаблона MBAM MDOP, а не шаблона шифрования диска BitLocker.

Пример

В разделе Параметры шифрования диска операционной системы вы выбрали доверенный платформенный модуль в качестве предохранителя, и вы также выбрали параметр **разрешить дополнительные контакты для запуска**. Это конфликтующие параметры, так как для защиты только доверенного платформенного модуля не требуется ПИН-код. Поэтому вы должны отключить параметр расширенные контакты.

### Пользователь мог запрашивать исключение

Если вы включили параметр параметры групповой политики Components\MDOP MBAM (Управление шифрованием для компьютера \ административные шаблоны \ компоненты Windows \client Management\Configure), пользователям будет предложено запросить исключение.

По умолчанию, если пользователь запрашивает исключение, исключение будет действовать в течение 7 дней, и пользователь не сможет получать запросы на шифрование в течение этого периода. (Значение по умолчанию можно увеличить или уменьшить в ходе настройки политики.) После того, как период освобождения будет завершен, пользователю будет предложено выполнить шифрование.

В журнале событий администратора MBAM появляется следующая запись, когда компьютер находится в разделе освобождение пользователей.

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

Если вы хотите вручную переопределять освобождение от пользователя для компьютера, выполните указанные ниже действия.
 
1. Установите для параметра AllowUserExemption значение **0** в следующем разделе реестра: <br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

2. Удалите все значения реестра из следующего подраздела реестра, кроме **AgentVersion**, **EncodedComputerName**и **установленного**.<br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM**

    **Примечание** Чтобы изменения вступили в силу, необходимо перезапустить агент MBAM.

Имейте в виду, что после применения групповой политики на компьютере эти значения могут вернуться к исходным параметрам.

### Неполадка WMI

MBAM использует методы класса win32_encryptablevolume для управления шифрованием BitLocker. Если этот модуль не зарегистрирован или поврежден, клиент MBAM будет работать неправильно, и в журнале событий администратора MBAM появится следующая запись о событии:

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

Кроме того, вы можете заметить, что политики восстановления и оборудования не применяются с кодом ошибки 0x8007007e. Это означает, что указанный модуль не найден.

Чтобы устранить эту проблему, перерегистрируйте класс **Win32_EncryptableVolume** с помощью следующей команды:

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## Устранение проблем с связью с агентом MBAM

В этом разделе содержатся сведения об устранении перечисленных ниже проблем, связанных с связью с агентом MBAM.

### Неверный URL-адрес службы MBAM

Если значение службы состояния соответствия MBAM или служба восстановления и оборудования не задано правильно, в журнале событий администратора MBAM на клиентском компьютере появится запись о событии, похожую на приведенную ниже.

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

Проверьте значения параметров **KeyRecoveryServiceEndPoint** и **StatusReportingServiceEndpoint** в следующем разделе реестра на клиентском компьютере: <br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

По умолчанию URL-адрес KeyRecoveryServiceEndPoint (конечная точка для восстановления MBAM и службы оборудования) имеет следующий формат: <br />
**http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc**

По умолчанию URL-адрес для StatusReportingServiceEndpoint (конечная точка службы отчетов о состоянии MBAM) имеет следующий формат:<br />
**http:// \<servername\> : \<port\> /MBAMComplianceStatusService/StatusReportingService.svc**

> [!Note]
> В URL-адресе не должно быть пробелов.

Если URL-адрес службы неверен, необходимо исправить URL-адрес службы в следующем параметре групповой политики:

**Конфигурация компьютера**  >  **Политики**  >  **Административные шаблоны**  >  **Компоненты Windows**  >  **MBAM MDOP (Управление BitLocker)**  >  **Управление клиентами**  >  **Настройка служб MBAM**

### Проблема с подключением, влияющая на сервер администрирования MBAM

Если между агентом клиента и сервером администрирования MBAM есть проблемы с подключением, агент MBAM не сможет публиковать обновления базы данных. В этом случае в журнале событий администратора MBAM на клиентском компьютере будут замечены ошибки подключения.

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

* Убедитесь в том, что для проверки основных подключений используется команда ping для сервера администрирования MBAM по имени и IP-адресу. Убедитесь, что вы можете подключиться к веб-сайту администрирования MBAM или порту службы, используя Telnet или Portqry.

* Убедитесь, что служба IIS запущена на сервере администрирования и мониторинга MBAM и что веб-служба MBAM прослушивает тот же порт, который настроен на клиентском компьютере MBAM ( `netstat –ano | find "portnumber"` ).

* Убедитесь, что номер порта, настроенный для веб-сайта MBAM, использует диспетчер IIS (inetmgr). Убедитесь, что номер порта совпадает с номером порта, который прослушивает клиент. Убедитесь, что номер порта не является общим для другого приложения. Например, другое приложение на сервере не должно использовать один и тот же порт.

* Если у вас есть брандмауэр, убедитесь, что порт открыт в брандмауэре или прокси-сервере.

* Если связь между клиентом и сервером является безопасной, убедитесь в том, что вы используете допустимый SSL-сертификат.

* Проверьте сетевое соединение между веб-сервером и сервером базы данных, на который будут отправляться данные для вставки. Вы можете проверить подключение к базе данных с веб-сервера на сервер базы данных с помощью администратора источников данных ODBC. Подробные сведения об устранении неполадок подключения к SQL Server можно найти в статье [Устранение неполадок при подключении к ядру СУБД SQL Server](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).

#### Устранение проблем с подключением

Убедитесь, что URL-адрес службы, настроенный на клиенте, задан правильно. Скопируйте значение URL-адреса для KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) из реестра и откройте его в Internet Explorer.

Аналогичным образом скопируйте значение URL-адреса для StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) и откройте его в Internet Explorer.

> [!Note]
> Если вам не удается найти URL-адрес на клиентском компьютере, необходимо протестировать базовое подключение клиента к серверу, на котором запущены службы IIS. Просмотрите пункты 1, 2, 3 и 4 в предыдущем разделе.

Кроме того, проверьте журналы приложений на сервере администрирования и мониторинга на наличие ошибок.

Вы можете создать одновременную трассировку сети между клиентом и сервером и проанализировать трассировку, чтобы определить причину сбоя соединения между агентом клиента и сервером администрирования MBAM.

> [!Note]
> Если вы можете найти URL-адреса службы на клиентском компьютере и в журналах событий администрирования MBAM есть ошибки подключения, это может быть вызвано сбоем подключения между сервером администрирования и сервером базы данных.

Если вы можете успешно перейти к обоим URL-адресам службы и есть связь между клиентом и сервером, служба IIS работает. Однако может возникнуть проблема с обменом данными между сервером, на котором запущены службы IIS и сервером базы данных.

Возможно, службы MBAM не смогут подключиться к серверу базы данных из-за сетевой ошибки или неверной настройки строки подключения к базе данных. Просматривайте журналы приложений на сервере администрирования и мониторинга. Вы можете столкнуться с ошибками в записях или предупреждениях исходного ASP.NET 2.0.50727.0, которые похожи на следующую запись в журнале:

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

#### Возможные причины

##### Причина 1

Возможно, администратор указал недействительное имя или имя базы данных в процессе установки сервера администрирования и мониторинга серверных компонентов.

Вы можете проверить и исправить строки подключения к базе данных с помощью консоли управления IIS. Для этого откройте Диспетчер IIS и перейдите к Администрирование и мониторинг Microsoft BitLocker. Для каждой службы, указанной в левой части экрана, выполните указанные ниже действия, чтобы изменить строки подключения к базе данных.

1. В **представлении функции**дважды щелкните **строку подключения**.

2. На странице **строки соединения** выберите строку подключения, которую вы хотите изменить.

3. На панели **действия** нажмите кнопку **изменить**.

4. В диалоговом окне **изменение строки подключения** измените свойства, которые нужно изменить, а затем нажмите кнопку **ОК**.

##### Причина 2

Порт SQL Server заблокирован в брандмауэре. Проверьте номер порта, на котором установлен SQL Server для прослушивания, и убедитесь, что порт открыт в брандмауэре между сервером администрирования и сервером баз данных.

##### Причина 3

Неверные привязки TCP/IP для сервера SQL Server. Проверьте привязки SQL TCP/IP в диспетчере конфигурации SQL Server на сервере базы данных. Для подключения к базе данных MBAM требуется, чтобы были включены протоколы TCP/IP и именованные каналы.

##### Причина 4

Учетная запись NT Authority\Network Service или сервер администрирования MBAM не имеет необходимых разрешений для подключения к базе данных SQL.

При установке компонентов базы данных на сервере базы данных установщик создает две локальные группы: Проверка соответствия MBAM доступа к БД и восстановление MBAM и доступ к данным оборудования.

Учетная запись NT Authority\Network Service, учетная запись сервера администрирования MBAM и пользователь, который устанавливает компоненты базы данных, автоматически добавляются в эти группы.

Эти группы получают необходимые разрешения на доступ к базе данных во время установки. Все пользователи, входящие в эту группу, автоматически получают необходимые разрешения на доступ к базе данных.

Возможно, веб-служба не подключается к серверу базы данных вследствие проблем с разрешениями, если выполняется одно или несколько из указанных ниже условий.

* Упомянутые ранее группы удаляются из локальных групп на сервере базы данных.

* Учетная запись NT Authority\Network Service и учетная запись сервера администрирования MBAM не являются членами этих групп.

* Эти группы не обладают необходимыми разрешениями для базы данных.

Ошибки, связанные с разрешениями, будут регистрироваться в журналах приложений на сервере администрирования и мониторинга MBAM, если хотя бы одно из предыдущих условий истинно. В этом случае необходимо вручную добавить учетную запись NT Authority\Network Service и сервер администрирования MBAM и предоставить им общую роль сервера базы данных SQL, использующую SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .

#### Просмотр журналов веб-службы

Если ни одно из событий не зарегистрировано в журналах приложений на сервере администрирования MBAM, можно просмотреть журналы веб-службы (SVCLOG) веб-службы MBAM, размещенные на сервере администрирования MBAM и сервера мониторинга. Для просмотра файла журнала необходимо использовать средство просмотра трассировки службы (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx .

В первую очередь следует исследовать журналы трассировки служб RecoveryandHardwareService и ComplianceStatusService. По умолчанию журналы веб-службы находятся в папке Solution\Logs управления C:\inetpub\Microsoft BitLocker. Каждая служба записывает файл. svclog в свою папку.

Проверьте активность в журнале трассировки служб на предмет ошибок или предупреждений. По умолчанию записи ошибок выделены красным цветом. Чтобы просмотреть подробные сведения об ошибке, щелкните описание ошибки на правой панели средства просмотра трассировки. Ниже приведен пример записи об ошибке из журнала трассировки.

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

## Переустановка или повторная настройка инфраструктуры MBAM

Для переустановки или повторной настройки инфраструктуры MBAM необходимо знать следующие моменты:

* Учетная запись пула приложений

* Группы MBAM (служба поддержки, Группа "Пользователи отчета")

* URL-адрес отчетов MBAM

* Имя сервера SQL Server и имена баз данных

* Учетные записи MBAM ReadWrite и ReadOnly

### Учетная запись пула приложений

Чтобы найти учетную запись пула приложений, войдите на веб-сервер MBAM, откройте **Диспетчер служб IIS**и выберите **Пулы приложений**.

![пулы приложений](images/troubleshooting-MBAM-installation-1.png)

Имя субъекта-службы (SPN) должно быть установлено в этой учетной записи. Этот параметр очень важен для функциональных возможностей MBAM.

### Группы MBAM (служба поддержки, Группа "Пользователи отчетов" и URL-адрес отчетов)

![Группы MBAM](images/troubleshooting-MBAM-installation-2.png)

Это предоставляет такие сведения, как группа "служба поддержки", Группа "дополнительные службы поддержки", Группа "Пользователи отчетов" и URL-адреса отчетов MBAM. URL-адрес отчетов MBAM должен быть указан в настройке MBAM, и его следует прочитать следующим образом: HTTP (s)://servername/ReportServer.

### Имена сервера SQL Server и имя базы данных (DB)

Чтобы найти имена и экземпляры SQL Server, на которых размещена служба MBAM DBs, войдите в MBAM веб-сервер (IIS) и перейдите к разделу реестра folowing:

**HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\Web**

![Программа](images/troubleshooting-MBAM-installation-3.png)

Выделенные части — это строки соединения. Для них должны быть указаны имя сервера SQL Server, имена баз данных и экземпляры (если оно именовано).

### Учетные записи MBAM ReadWrite и ReadOnly

Эти данные будут храниться в базе данных SQL Server, для которой имя уже найдено на веб-сервере.

#### Учетная запись ReadWrite

1. Войдите в центр управления SQL.

2. Щелкните правой кнопкой мыши **MBAM восстановления и оборудования**, выберите пункт **Свойства**и нажмите кнопку **разрешения**.

Например, имя учетной записи лаборатории — **MBAMWrite**. Учетные записи в пуле приложений и на ReadWrite должны совпадать.

![БАЗА ДАННЫХ SQL](images/troubleshooting-MBAM-installation-4.png)

![Свойства базы данных](images/troubleshooting-MBAM-installation-5.png)

Перейдите к пункту **Безопасность** и войдите в **систему** в SQL Management Studio. Перейдите к учетной записи, показанной на предыдущем снимке экрана.

![Безопасность SQL](images/troubleshooting-MBAM-installation-6.png)

Щелкните Учетные записи правой кнопкой мыши, выберите **Свойства сопоставление пользователей**и найдите базу данных восстановления MBAM и оборудования.

![Сопоставление пользователей](images/troubleshooting-MBAM-installation-7.png)

#### Учетная запись только для чтения

Откройте Диспетчер конфигураций служб SQL Server Reporting Services на сервере SSRS. Выберите **URL-адрес диспетчера отчетов**, а затем найдите **URL-адреса**:

![Диспетчер отчетов](images/troubleshooting-MBAM-installation-8.png)

Выберите **Администрирование и мониторинг Microsoft BitLocker**.

![Администрирование и мониторинг BitLocker](images/troubleshooting-MBAM-installation-9.png)

Выберите **MaltaDatasource**:

![DBs](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource](images/troubleshooting-MBAM-installation-11.png)

Для MaltaDataSource должно быть задано имя учетной записи "только для чтения", и его следует использовать в настройке MBAM.

## Справочные материалы

Дополнительные сведения доступны в следующих статьях.

[Развертывание MBAM 2,5 в автономной конфигурации](https://support.microsoft.com/help/3046555)

[Microsoft BitLocker Administration and Monitoring 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
