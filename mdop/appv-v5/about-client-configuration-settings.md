---
title: Сведения о параметрах конфигурации клиента
description: Сведения о параметрах конфигурации клиента
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814941"
---
# Сведения о параметрах конфигурации клиента


Клиент Microsoft Application Virtualization (App-V) 5,0 хранит свою конфигурацию в реестре. Вы можете собрать полезные сведения о клиенте, если вы понимаете формат данных в реестре. Вы также можете настроить множество клиентских действий, изменяя записи в реестре. В этом разделе перечислены параметры конфигурации клиента App-V 5,0 и описаны их использование. Вы можете изменить параметры конфигурации клиента с помощью PowerShell. Дополнительные сведения об использовании PowerShell и App-V 5,0 можно найти [в разделе Администрирование App-V с помощью PowerShell](administering-app-v-by-using-powershell.md).

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> Параметры конфигурации клиента App-V 5,0


В следующей таблице приведены сведения о параметрах конфигурации клиента App-V 5,0:

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
<th align="left">Имя параметра</th>
<th align="left">Флажок настройки</th>
<th align="left">Описание</th>
<th align="left">Настройка параметров</th>
<th align="left">Значение раздела реестра</th>
<th align="left">Отключенные ключи и значения состояния политики</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>PACKAGEINSTALLATIONROOT</p></td>
<td align="left"><p>Указывает каталог, в котором будут установлены все новые приложения и обновления.</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>Streaming\PackageInstallationRoot</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>PACKAGESOURCEROOT</p></td>
<td align="left"><p>Переопределяет расположение источника для загрузки содержимого пакета.</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>Streaming\PackageSourceRoot</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AllowHighCostLaunch</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Этот параметр определяет, будут ли виртуализированные приложения запускаться на компьютерах с Windows 8, подключенных через лимитное сетевое подключение (например, 4G).</p></td>
<td align="left"><p>Истина (включена); False (отключенное состояние)</p></td>
<td align="left"><p>Streaming\AllowHighCostLaunch</p></td>
<td align="left"><p>до</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReestablishmentRetries</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Задает количество повторений прерванного сеанса.</p></td>
<td align="left"><p>Integer (0-99)</p></td>
<td align="left"><p>Streaming\ReestablishmentRetries</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReestablishmentInterval</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Задает количество секунд между попытками повторного установления прерванного сеанса.</p></td>
<td align="left"><p>Integer (0-3600)</p></td>
<td align="left"><p>Streaming\ReestablishmentInterval</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoad</p></td>
<td align="left"><p>AUTOLOAD</p></td>
<td align="left"><p>Определяет способ автоматической загрузки новых пакетов приложением App-V на определенном компьютере.</p></td>
<td align="left"><p>(0x0) None; (0x1) ранее использованный; (0x2) все</p></td>
<td align="left"><p>Streaming\AutoLoad</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocationProvider</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Задает CLSID для совместимой реализации интерфейса IAppvPackageLocationProvider.</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>Streaming\LocationProvider</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="even">
<td align="left"><p>CertFilterForClientSsl</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Указывает путь к действительному сертификату в хранилище сертификатов.</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>Streaming\CertFilterForClientSsl</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VerifyCertificateRevocationList</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Проверка состояния отзыва сертификата сервера перед Steaming с помощью HTTPS.</p></td>
<td align="left"><p>Истина (включена); False (отключенное состояние)</p></td>
<td align="left"><p>Streaming\VerifyCertificateRevocationList</p></td>
<td align="left"><p>до</p></td>
</tr>
<tr class="even">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>SHAREDCONTENTSTOREMODE</p></td>
<td align="left"><p>Указывает на то, что содержимое потокового пакета не будет сохранено на локальном жестком диске.</p></td>
<td align="left"><p>Истина (включена); False (отключенное состояние)</p></td>
<td align="left"><p>Streaming\SharedContentStoreMode</p></td>
<td align="left"><p>до</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Имя</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> . Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERNAME</p></td>
<td align="left"><p>Отображает имя сервера публикации.</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ FriendlyName</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="even">
<td align="left"><p>URL-адрес</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> . Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERURL</p></td>
<td align="left"><p>Отображает URL-адрес сервера публикации.</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ URL-адрес</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshEnabled</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> . Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHENABLED</p></td>
<td align="left"><p>Включает глобальное обновление публикации (логическое значение)</p></td>
<td align="left"><p>Истина (включена); False (отключенное состояние)</p></td>
<td align="left"><p>Publishing\Servers{serverId}\GlobalEnabled</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshOnLogon</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> . Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHONLOGON</p></td>
<td align="left"><p>Запускает глобальное обновление публикации при входе. Значением</p></td>
<td align="left"><p>Истина (включена); False (отключенное состояние)</p></td>
<td align="left"><p>Publishing\Servers{serverId}\GlobalLogonRefresh</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshInterval</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> . Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVAL  </p></td>
<td align="left"><p>Задает интервал обновления публикации с помощью GlobalRefreshIntervalUnit. Чтобы отключить обновление пакета, выберите значение 0.</p></td>
<td align="left"><p>Integer (0-744</p></td>
<td align="left"><p>Publishing\Servers{serverId}\GlobalPeriodicRefreshInterval</p></td>
<td align="left"><p>до</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshIntervalUnit</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> . Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVALUNI</p></td>
<td align="left"><p>Указывает единицу интервала (час 0-23, день 0-31). </p></td>
<td align="left"><p>0 для часа, 1 — для дня</p></td>
<td align="left"><p>Publishing\Servers{serverId}\GlobalPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>1,1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshEnabled</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> . Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHENABLED </p></td>
<td align="left"><p>Включает обновление публикации пользователей (логическое значение).</p></td>
<td align="left"><p>Истина (включена); False (отключенное состояние)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserEnabled</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshOnLogon</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> . Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHONLOGON</p></td>
<td align="left"><p>Запускает входное обновление публикации пользователя. Значением</p>
<p>Подсчет слов (с пробелами): 60</p></td>
<td align="left"><p>Истина (включена); False (отключенное состояние)</p></td>
<td align="left"><p>Publishing\Servers{serverId}\UserLogonRefresh</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshInterval</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> . Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVAL     </p></td>
<td align="left"><p>Задает интервал обновления публикации с помощью UserRefreshIntervalUnit. Чтобы отключить обновление пакета, выберите значение 0.</p>
<p>Подсчет слов (с пробелами): 85</p></td>
<td align="left"><p>Integer (0-744 часов)</p></td>
<td align="left"><p>Publishing\Servers{serverId}\UserPeriodicRefreshInterval</p></td>
<td align="left"><p>до</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshIntervalUnit</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот параметр невозможно изменить с помощью <strong> командлета Set-AppvclientConfiguration </strong> . Необходимо использовать <strong> командлет Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVALUNIT  </p></td>
<td align="left"><p>Указывает единицу интервала (час 0-23, день 0-31). </p></td>
<td align="left"><p>0 для часа, 1 — для дня</p></td>
<td align="left"><p>Publishing\Servers{serverId}\UserPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>1,1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MigrationMode</p></td>
<td align="left"><p>MIGRATIONMODE</p></td>
<td align="left"><p>Режим миграции позволяет клиенту App-V изменять сочетания клавиш и FTA для пакетов, созданных с помощью более ранней версии App-V.</p></td>
<td align="left"><p>True (включенное состояние); False (отключенное состояние)</p></td>
<td align="left"><p>Coexistence\MigrationMode</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>Позволяет компьютеру с клиентом App-V 5,0 собирать и возвращать определенные сведения об использовании, чтобы помочь нам усовершенствовать приложение.</p></td>
<td align="left"><p>0 для отключения; 1 для включения</p></td>
<td align="left"><p>Программное обеспечение/Microsoft/AppV/CEIP/CEIPEnable</p></td>
<td align="left"><p>до</p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePackageScripts</p></td>
<td align="left"><p>ENABLEPACKAGESCRIPTS</p></td>
<td align="left"><p>Включает сценарии, определенные в манифесте пакета для файлов конфигурации, которые должны выполняться.</p></td>
<td align="left"><p>Истина (включена); False (отключенное состояние)</p></td>
<td align="left"><p>\Scripting\EnablePackageScripts</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>RoamingFileExclusions</p></td>
<td align="left"><p>ROAMINGFILEEXCLUSIONS</p></td>
<td align="left"><p>Указывает пути к файлам относительно% UserProfile%, которые не перемещаются с помощью профиля пользователя&#39;s. Пример использования:/ROAMINGFILEEXCLUSIONS =&#39;Desktop; мои рисунки&#39;</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>RoamingRegistryExclusions</p></td>
<td align="left"><p>ROAMINGREGISTRYEXCLUSIONS</p></td>
<td align="left"><p>Указывает пути в реестре, которые не перемещаются вместе с профилем пользователя. Пример использования:/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>Integration\RoamingRegistryExclusions</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="even">
<td align="left"><p>IntegrationRootUser</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Указывает место для создания символьных ссылок, связанных с текущей версией опубликованного пакета для каждого пользователя. все виртуальные расширения приложения, например сочетания клавиш и сопоставления типов файлов, будут указывать на этот путь. Если путь не указан, символические ссылки не будут использоваться при публикации пакета. Например:%localappdata%\Microsoft\AppV\Client\Integration.</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>Integration\IntegrationRootUser</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IntegrationRootGlobal</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Указывает место для создания символьных ссылок, связанных с текущей версией глобально опубликованного пакета. все виртуальные расширения приложения, например сочетания клавиш и сопоставления типов файлов, будут указывать на этот путь. Если путь не указан, символические ссылки не будут использоваться при публикации пакета. Например:%allusersprofile%\Microsoft\AppV\Client\Integration</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>Integration\IntegrationRootGlobal</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="even">
<td align="left"><p>VirtualizableExtensions</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Разделенный запятыми список расширений имен файлов, которые можно использовать, чтобы определить, может ли локально установленное приложение выполняться в виртуальной среде.</p>
<p>Когда при публикации создаются ярлыки, FTAs и другие точки расширения, App-V сравнивает расширение имени файла со списком, если приложение, связанное с точкой расширения, будет установлено локально. Если расширение найдено, <strong> </strong> будет добавлен параметр командной строки RunVirtual, и приложение будет выполняться практически.</p>
<p>Дополнительные сведения о <strong> </strong> параметре RunVirtual можно найти в разделе <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> выполнение локально установленного приложения в виртуальной среде с виртуализированными приложениями </a> .</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>Integration\VirtualizableExtensions</p></td>
<td align="left"><p>Значение политики не написано</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingEnabled</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Позволяет клиенту возвращать данные на сервер отчетов.</p></td>
<td align="left"><p>Истина (включена); False (отключенное состояние)</p></td>
<td align="left"><p>Reporting\EnableReporting</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingServerURL</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Задает расположение на сервере отчетов, на котором сохраняются сведения о клиенте.</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>Reporting\ReportingServer</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingDataCacheLimit</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Задает максимальный размер кэша XML в мегабайтах (МБ) для хранения сведений о отчетах. Размер применяется к кэшу в памяти. По достижении этого предела файл журнала будет выполнен. Устанавливается значение от 0 до 1024.</p></td>
<td align="left"><p>Integer [0-1024]</p></td>
<td align="left"><p>Reporting\DataCacheLimit</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingDataBlockSize</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Задает максимальный размер (в байтах), который должен отправляться серверу для отправки запросов на передачу. Это поможет избежать сбоев при неустранимой передаче данных, если журнал достигает значительного размера. Настройка между 1024 и без ограничений.</p></td>
<td align="left"><p>Integer [1024-без ограничений]</p></td>
<td align="left"><p>Reporting\DataBlockSize</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingStartTime</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Указывает время, в течение которого клиент отправляет данные на сервер отчетов. Необходимо указать допустимое целое число в диапазоне от 0-23, соответствующее часу дня. По умолчанию <strong> ReportingStartTime </strong> начнется с текущего дня по 10 P. M. или 22.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот параметр следует настроить на время, когда компьютеры, на которых работает клиент App-V 5,0, не будут работать в автономном режиме.</p>
</div>
<div>

</div></td>
<td align="left"><p>Целое число (от 0 до 23).</p></td>
<td align="left"><p>Отчетность \ время начала</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingInterval</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Указывает интервал повтора, который будет использоваться клиентом для повторной отправки данных на сервер отчетов.</p></td>
<td align="left"><p>целое число</p></td>
<td align="left"><p>Reporting\RetryInterval</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingRandomDelay</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Указывает максимальную задержку (в минутах) для данных, отправляемых на сервер отчетов. При запуске запланированной задачи клиент создает произвольную задержку от 0 до <strong> ReportingRandomDelay </strong> и ждет указанное время перед отправкой данных. Это поможет предотвратить конфликты на сервере.</p></td>
<td align="left"><p>Integer [0-ReportingRandomDelay]</p></td>
<td align="left"><p>Reporting\RandomDelay</p></td>
<td align="left"><p>Значение политики не написано (то же, что и не задано)</p></td>
</tr>
<tr class="even">
<td align="left"><p>EnableDynamicVirtualization</p>
<div class="alert">
<strong>Важно.</strong><br/><p>Этот параметр доступен только в приложении App-V 5,0 SP2 или более поздней версии.</p>
</div>
<div>

</div></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Включает в себя поддерживаемые расширения оболочки, вспомогательные объекты браузера и элементы управления ActiveX, которые должны быть виртуализированы и запущены с виртуальными приложениями.</p></td>
<td align="left"><p>1 (включена), 0 (отключено)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePublishingRefreshUI</p>
<div class="alert">
<strong>Важно.</strong><br/><p>Этот параметр доступен только для App-V 5,0 SP2.</p>
</div>
<div>

</div></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Включает индикатор выполнения обновления публикации для компьютера, на котором запущен клиент App-V 5,0.</p></td>
<td align="left"><p>1 (включена), 0 (отключено)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>HideUI</p>
<div class="alert">
<strong>Важно.</strong><br/><p>Этот параметр доступен только для App-V 5,0 SP2.</p>
</div>
<div>

</div></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Скрывает индикатор выполнения обновления публикации.</p></td>
<td align="left"><p>1 (включена), 0 (отключено)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>Недоступен.</p></td>
<td align="left"><p>Указывает список путей процессов (которые могут содержать подстановочные знаки), которые являются кандидатами на использование динамической виртуализации (поддерживаемые расширения оболочки, вспомогательные объекты браузера и элементы ActiveX). Динамическая виртуализация может использовать только процессы, полный путь к которой соответствует одному из этих элементов.</p></td>
<td align="left"><p>Строка</p></td>
<td align="left"><p>Virtualization\ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>Пустая строка.</p></td>
</tr>
</tbody>
</table>








## Статьи по теме


[Развертывание программы Sequencer и клиента App-V 5.0](deploying-the-app-v-50-sequencer-and-client.md)

[Изменение конфигурации клиента App-V 5.0 с помощью шаблона ADMX и групповой политики](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[Развертывание клиента App-V](how-to-deploy-the-app-v-client-gb18030.md)









