---
title: Сведения о параметрах конфигурации клиента
description: Сведения о параметрах конфигурации клиента
author: dansimp
ms.assetid: 18bb307a-7eda-4dd6-a83e-6afaefd99470
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb547eedf63bf165b1e8f5fd024839b3c2af3e4c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814944"
---
# Сведения о параметрах конфигурации клиента


Клиент Microsoft Application Virtualization (App-V) 5,1 хранит свою конфигурацию в реестре. Вы можете собрать полезные сведения о клиенте, если вы понимаете формат данных в реестре. Вы также можете настроить множество клиентских действий, изменяя записи в реестре. В этом разделе перечислены параметры конфигурации клиента App-V 5,1 и описаны их использование. Вы можете изменить параметры конфигурации клиента с помощью PowerShell. Дополнительные сведения об использовании PowerShell и App-V 5,1 см. в разделе [Администрирование App-v 5,1 с помощью PowerShell](administering-app-v-51-by-using-powershell.md).

## <a href="" id="---------app-v-5-1-client-configuration-settings"></a> Параметры конфигурации клиента App-V 5,1


В следующей таблице приведены сведения о параметрах конфигурации клиента App-V 5,1:

|Имя параметра | Флажок настройки | Описание | Настройка параметров | Значение раздела реестра | Отключенные ключи и значения состояния политики |
|-------------|------------|-------------|-----------------|--------------------|--------------------------------------|
| PackageInstallationRoot | PACKAGEINSTALLATIONROOT | Указывает каталог, в котором будут установлены все новые приложения и обновления. | Строка | Streaming\PackageInstallationRoot | Значение политики не написано (то же, что и не задано) |
| PackageSourceRoot | PACKAGESOURCEROOT | Переопределяет расположение источника для загрузки содержимого пакета. | Строка | Streaming\PackageSourceRoot | Значение политики не написано (то же, что и не задано) |
| AllowHighCostLaunch | Недоступен. |Этот параметр определяет, будут ли виртуализированные приложения запускаться на компьютерах с Windows 10, подключенных через лимитное сетевое подключение (например, 4G). | Истина (включена); False (отключенное состояние) | Streaming\AllowHighCostLaunch | до |
| ReestablishmentRetries | Недоступен. | Задает количество повторений прерванного сеанса. | Integer (0-99) | Streaming\ReestablishmentRetries | Значение политики не написано (то же, что и не задано) |
| ReestablishmentInterval | Недоступен. | Задает количество секунд между попытками повторного установления прерванного сеанса. | Integer (0-3600) | Streaming\ReestablishmentInterval | Значение политики не написано (то же, что и не задано) |
| LocationProvider | Недоступен. | Задает CLSID для совместимой реализации интерфейса IAppvPackageLocationProvider. | Строка | Streaming\LocationProvider | Значение политики не написано (то же, что и не задано) |
| CertFilterForClientSsl | Недоступен. | Указывает путь к действительному сертификату в хранилище сертификатов. | Строка | Streaming\CertFilterForClientSsl | Значение политики не написано (то же, что и не задано) |
| VerifyCertificateRevocationList | Недоступен. | Проверка состояния отзыва сертификата сервера перед Steaming с помощью HTTPS. | Истина (включена); False (отключенное состояние) | Streaming\VerifyCertificateRevocationList | до |
| SharedContentStoreMode | SHAREDCONTENTSTOREMODE | Указывает на то, что содержимое потокового пакета не будет сохранено на локальном жестком диске. | Истина (включена); False (отключенное состояние) | Streaming\SharedContentStoreMode | до |
| Имя<br>**Примечание** Этот параметр невозможно изменить с помощью командлета **Set-AppvclientConfiguration** . Необходимо использовать командлет **Set-AppvPublishingServer** . | PUBLISHINGSERVERNAME | Отображает имя сервера публикации. | Строка | Publishing\Servers\ {serverId} \ FriendlyName | Значение политики не написано (то же, что и не задано) |
| URL-адрес<br>**Примечание** Этот параметр невозможно изменить с помощью командлета **Set-AppvclientConfiguration** . Необходимо использовать командлет **Set-AppvPublishingServer** . | PUBLISHINGSERVERURL | Отображает URL-адрес сервера публикации. | Строка | Publishing\Servers\ {serverId} \ URL-адрес | Значение политики не написано (то же, что и не задано) |
| GlobalRefreshEnabled<br>**Примечание** Этот параметр невозможно изменить с помощью командлета **Set-AppvclientConfiguration** . Необходимо использовать командлет **Set-AppvPublishingServer** . | GLOBALREFRESHENABLED | Включает глобальное обновление публикации (логическое значение) | Истина (включена); False (отключенное состояние) | Publishing\Servers\{serverId}\GlobalEnabled | False |
| GlobalRefreshOnLogon<br>**Примечание** Этот параметр невозможно изменить с помощью командлета **Set-AppvclientConfiguration** . Необходимо использовать командлет **Set-AppvPublishingServer** . | GLOBALREFRESHONLOGON | Запускает глобальное обновление публикации при входе. Значением | Истина (включена); False (отключенное состояние) | Publishing\Servers\{serverId}\GlobalLogonRefresh | False |
| GlobalRefreshInterval<br>**Примечание** Этот параметр невозможно изменить с помощью командлета **Set-AppvclientConfiguration** . Необходимо использовать командлет **Set-AppvPublishingServer** . | GLOBALREFRESHINTERVAL | Задает интервал обновления публикации с помощью GlobalRefreshIntervalUnit. Чтобы отключить обновление пакета, выберите значение 0. | Integer (0-744) | Publishing\Servers\{serverId}\GlobalPeriodicRefreshInterval | до |
| GlobalRefreshIntervalUnit <br>**Примечание** Этот параметр невозможно изменить с помощью командлета **Set-AppvclientConfiguration** . Необходимо использовать командлет **Set-AppvPublishingServer** . | GLOBALREFRESHINTERVALUNI | Указывает единицу интервала (час 0-23, день 0-31). | 0 для часа, 1 — для дня | Publishing\Servers\{serverId}\GlobalPeriodicRefreshIntervalUnit | 1,1 |
| UserRefreshEnabled<br>**Примечание** Этот параметр невозможно изменить с помощью командлета **Set-AppvclientConfiguration** . Необходимо использовать командлет **Set-AppvPublishingServer** . | USERREFRESHENABLED | Включает обновление публикации пользователей (логическое значение). | Истина (включена); False (отключенное состояние) | Publishing\Servers\ {serverId} \ UserEnabled | False |
| UserRefreshOnLogon<br>**Примечание** Этот параметр невозможно изменить с помощью командлета **Set-AppvclientConfiguration** . Необходимо использовать командлет **Set-AppvPublishingServer** . | USERREFRESHONLOGON | Запускает входное обновление публикации пользователя. Значением<br>Подсчет слов (с пробелами): 60 | Истина (включена); False (отключенное состояние) | Publishing\Servers\{serverId}\UserLogonRefresh | False |
| UserRefreshInterval<br>**Примечание** Этот параметр невозможно изменить с помощью командлета **Set-AppvclientConfiguration** . Необходимо использовать командлет **Set-AppvPublishingServer** . | USERREFRESHINTERVAL | Задает интервал обновления публикации с помощью UserRefreshIntervalUnit. Чтобы отключить обновление пакета, выберите значение 0. | Подсчет слов (с пробелами): 85<br>Integer (0-744 часов) | Publishing\Servers\{serverId}\UserPeriodicRefreshInterval | до |
| UserRefreshIntervalUnit<br>**Примечание** Этот параметр невозможно изменить с помощью командлета **Set-AppvclientConfiguration** . Необходимо использовать командлет **Set-AppvPublishingServer** . | USERREFRESHINTERVALUNIT | Указывает единицу интервала (час 0-23, день 0-31). | 0 для часа, 1 — для дня | Publishing\Servers\{serverId}\UserPeriodicRefreshIntervalUnit | 1,1 |
| MigrationMode | MIGRATIONMODE | Режим миграции позволяет клиенту App-V изменять сочетания клавиш и FTA для пакетов, созданных с помощью более ранней версии App-V. | True (включенное состояние); False (отключенное состояние) | Coexistence\MigrationMode | |
| CEIPOPTIN | CEIPOPTIN | Позволяет компьютеру с клиентом App-V 5,1 собирать и возвращать определенные сведения об использовании, чтобы помочь нам усовершенствовать приложение. | 0 для отключения; 1 для включения | Программное обеспечение/Microsoft/AppV/CEIP/CEIPEnable | до | 
| EnablePackageScripts | ENABLEPACKAGESCRIPTS | Включает сценарии, определенные в манифесте пакета для файлов конфигурации, которые должны выполняться. | Истина (включена); False (отключенное состояние) | \Scripting\EnablePackageScripts | | 
| RoamingFileExclusions | ROAMINGFILEEXCLUSIONS | Указывает пути к файлам относительно% UserProfile%, которые не перемещаются вместе с профилем пользователя. Пример использования:/ROAMINGFILEEXCLUSIONS = "Desktop; мои рисунки" | | | |
| RoamingRegistryExclusions | ROAMINGREGISTRYEXCLUSIONS | Указывает пути в реестре, которые не перемещаются вместе с профилем пользователя. Пример использования:/ROAMINGREGISTRYEXCLUSIONS = software\\classes; software\\clients | Строка | Integration\RoamingRegistryExclusions | Значение политики не написано (то же, что и не задано) |
| IntegrationRootUser | Недоступен. | Указывает место для создания символьных ссылок, связанных с текущей версией опубликованного пакета для каждого пользователя. все виртуальные расширения приложения, например сочетания клавиш и сопоставления типов файлов, будут указывать на этот путь. Если путь не указан, символические ссылки не будут использоваться при публикации пакета. Например:%localappdata%\Microsoft\AppV\Client\Integration.| Строка | Integration\IntegrationRootUser | Значение политики не написано (то же, что и не задано) |
|IntegrationRootGlobal | Недоступен.| Указывает место для создания символьных ссылок, связанных с текущей версией глобально опубликованного пакета. все виртуальные расширения приложения, например сочетания клавиш и сопоставления типов файлов, будут указывать на этот путь. Если путь не указан, символические ссылки не будут использоваться при публикации пакета. Например:%allusersprofile%\Microsoft\AppV\Client\Integration | Строка | Integration\IntegrationRootGlobal | Значение политики не написано (то же, что и не задано) |
| VirtualizableExtensions | Недоступен. | Разделенный запятыми список расширений имен файлов, которые можно использовать, чтобы определить, может ли локально установленное приложение выполняться в виртуальной среде.<br>Когда при публикации создаются ярлыки, FTAs и другие точки расширения, App-V сравнивает расширение имени файла со списком, если приложение, связанное с точкой расширения, будет установлено локально. Если расширение найдено, будет добавлен параметр командной строки **RunVirtual** , и приложение будет выполняться практически.<br>Дополнительные сведения о параметре **RunVirtual** можно найти в разделе [выполнение локально установленного приложения в виртуальной среде с виртуализированными приложениями](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications51.md). | Строка | Integration\VirtualizableExtensions | Значение политики не написано |
| ReportingEnabled | Недоступен. | Позволяет клиенту возвращать данные на сервер отчетов. | Истина (включена); False (отключенное состояние) | Reporting\EnableReporting | False |
| ReportingServerURL | Недоступен. | Задает расположение на сервере отчетов, на котором сохраняются сведения о клиенте. | Строка | Reporting\ReportingServer | Значение политики не написано (то же, что и не задано) |
| ReportingDataCacheLimit | Недоступен. | Задает максимальный размер кэша XML в мегабайтах (МБ) для хранения сведений о отчетах. Размер применяется к кэшу в памяти. По достижении этого предела файл журнала будет выполнен. Устанавливается значение от 0 до 1024. | Integer [0-1024] | Reporting\DataCacheLimit | Значение политики не написано (то же, что и не задано) |
| ReportingDataBlockSize| Недоступен. | Задает максимальный размер (в байтах), который должен отправляться серверу для отправки запросов на передачу. Это поможет избежать сбоев при неустранимой передаче данных, если журнал достигает значительного размера. Настройка между 1024 и без ограничений. | Integer [1024-без ограничений] | Reporting\DataBlockSize | Значение политики не написано (то же, что и не задано) |
| ReportingStartTime | Недоступен. | Указывает время, в течение которого клиент отправляет данные на сервер отчетов. Необходимо указать допустимое целое число в диапазоне от 0-23, соответствующее часу дня. По умолчанию **ReportingStartTime** начнется с текущего дня по 10 P. M. или 22.<br>**Примечание** Этот параметр следует настроить на время, когда компьютеры, на которых работает клиент App-V 5,1, не будут работать в автономном режиме. | Целое число (от 0 до 23). | Отчетность \ время начала | Значение политики не написано (то же, что и не задано) |
| ReportingInterval | Недоступен. | Указывает интервал повтора, который будет использоваться клиентом для повторной отправки данных на сервер отчетов. | целое число | Reporting\RetryInterval | Значение политики не написано (то же, что и не задано) |
| ReportingRandomDelay | Недоступен. | Указывает максимальную задержку (в минутах) для данных, отправляемых на сервер отчетов. При запуске запланированной задачи клиент создает произвольную задержку от 0 до **ReportingRandomDelay** и ждет указанное время перед отправкой данных. Это поможет предотвратить конфликты на сервере. | Integer [0-ReportingRandomDelay] | Reporting\RandomDelay | Значение политики не написано (то же, что и не задано) |
| EnableDynamicVirtualization<br>**Важно!** Этот параметр доступен только в приложении App-V 5,0 SP2 или более поздней версии. | Недоступен. | Включает в себя поддерживаемые расширения оболочки, вспомогательные объекты браузера и элементы управления ActiveX, которые должны быть виртуализированы и запущены с виртуальными приложениями. | 1 (включена), 0 (отключено) | HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization | |
| EnablePublishingRefreshUI<br>**Важно!** Этот параметр доступен только для App-V 5,0 SP2. | Недоступен. | Включает индикатор выполнения обновления публикации для компьютера, на котором запущен клиент App-V 5,1. | 1 (включена), 0 (отключено) | HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing | |
| HideUI<br>**Важно!**  Этот параметр доступен только для App-V 5,0 SP2.| Недоступен. | Скрывает индикатор выполнения обновления публикации. | 1 (включена), 0 (отключено) | | |
| ProcessesUsingVirtualComponents | Недоступен. | Указывает список путей процессов (которые могут содержать подстановочные знаки), которые являются кандидатами на использование динамической виртуализации (поддерживаемые расширения оболочки, вспомогательные объекты браузера и элементы ActiveX). Динамическая виртуализация может использовать только процессы, полный путь к которой соответствует одному из этих элементов. | Строка | Virtualization\ProcessesUsingVirtualComponents | Пустая строка. |






## Статьи по теме


[Развертывание Sequencer и клиента App-V 5.1](deploying-the-app-v-51-sequencer-and-client.md)

[Изменение конфигурации клиента App-V 5.1 с помощью шаблона ADMX и групповой политики](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

[Развертывание клиента App-V](how-to-deploy-the-app-v-client-51gb18030.md)

 

 





