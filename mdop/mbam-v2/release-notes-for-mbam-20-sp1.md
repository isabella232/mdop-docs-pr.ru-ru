---
title: Заметки о выпуске для MBAM 2.0 с пакетом обновления 1 (SP1)
description: Заметки о выпуске для MBAM 2.0 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: b39002ba-33c6-45ec-9d1b-464327b60f5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 54a77fc7a493b36217ae2cdc875226b25fdc6e7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825582"
---
# Заметки о выпуске для MBAM 2.0 с пакетом обновления 1 (SP1)


Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.

Внимательно прочтите эти заметки о выпуске, прежде чем устанавливать администрирование и мониторинг Microsoft BitLocker (MBAM) 2,0 с пакетом обновления 1 (SP1). Эти заметки о выпуске содержат сведения, необходимые для успешной установки средства администрирования BitLocker и мониторинга 2,0 с пакетом обновления 1 (SP1), и они содержат сведения, недоступные в документации по продукту. Если существует разница между этими заметками о выпуске и другой MBAM 2,0 SP1, Последнее изменение должно считаться полномочным. Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> Известные проблемы с MBAM 2,0 SP1


В этом разделе содержатся известные проблемы, возникающие при работе с MBAM 2,0 SP1.

### Для обновления MBAM с помощью интегрированной топологии Configuration Manager и MBAM 2,0 SP1 требуется удаление объектов Configuration Manager вручную.

Если вы используете MBAM в Configuration Manager и хотите перейти на MBAM 2,0 SP1, необходимо вручную удалить все объекты Configuration Manager, которые были установлены в Configuration Manager, в составе MBAM установки. Объекты, которые необходимо удалить вручную, — это MBAM отчеты, MBAM поддерживаемые компьютеры, а также базовые параметры конфигурации защиты BitLocker и связанные с ними элементы конфигурации.

**Временное решение**: обновите объекты Configuration Manager, выполнив указанные ниже действия.

1.  Создавайте резервные копии существующих данных о соответствиях во внешнем файле, как описано ниже.

    **Примечание**  Все существующие данные о соответствии BitLocker будут удалены при удалении существующего базового плана в Configuration Manager. Данные будут повторно сформированы с течением времени, но рекомендуется сохранить копию данных в случае, если вам понадобятся данные о соответствии для определенного компьютера, прежде чем будут восстановлены данные о соответствии требованиям.

     

    1.  Чтобы сохранить данные о соответствии BitLocker с предысторией, откройте отчет **сведения о соответствии требованиям для программы BitLocker Enterprise** .

    2.  Щелкните значок **сохранить** в отчете и выберите **Excel**.

        Сохраненный отчет содержит такие данные, как имя компьютера, имя домена, состояние соответствия требованиям, исключения, пользователи устройства, сведения о состоянии соответствия и Дата и время последнего контакта. Некоторые сведения, такие как подробные сведения о Томе и стойкость шифрования, не сохраняются.

2.  Удалите **MBAM** с сервера с помощью установщика **MBAM** .

3.  Вручную удалите следующие объекты из Configuration Manager:

    -   Семейство поддерживаемых компьютеров MBAM

    -   Базовые показатели защиты BitLocker

    -   Элемент конфигурации защиты диска операционной системы BitLocker

    -   Элемент конфигурации защиты фиксированных дисков с данными BitLocker

4.  Вручную удалите папку "отчеты MBAM" на сайте служб SQL Server Reporting Services Configuration Manager. Для этого выполните следующие действия.

    1.  С помощью Internet Explorer найдите точку служб Reporting Services, например http:// &lt; yourcmserver &gt; /Reports.

    2.  Щелкните соответствующую ссылку на код сайта Configuration Manager.

    3.  Удалите папку MBAM.

5.  Используйте установщик сервера MBAM для переустановки объектов интеграции Configuration Manager. Клиентские компьютеры начинают заново отправлять данные о соответствии требованиям BitLocker с течением времени.

### Кнопка "Отправить" на портале самообслуживания не работает в Internet Explorer10

При использовании Internet Explorer10 для доступа к веб-сайту администрирования и наблюдения кнопка " **Отправить** " на веб-сайте не работает.

**Временное решение**: на сервере, на котором установлен веб-сайт администрирования и наблюдения, установите [исправление для файлов описания браузеров ASP.NET](https://go.microsoft.com/fwlink/?LinkId=317798).

### Международные доменные имена не поддерживаются

MBAM 2,0 с пакетом обновления 1 (SP1) не поддерживает международные доменные имена.

**Временное решение**: нет.

### Отчеты на веб-сайте администрирования и мониторинга выводят предупреждение, если протокол SSL не настроен в SSRS

Если службы отчетов SQLServer (SSRS) не настроены на использование Secure Socket Layer (SSL), при установке сервера MBAM URL-адрес для отчетов будет установлен в значение HTTP вместо HTTPS. Если затем перейти на веб-сайт администрирования и наблюдения и выбрать отчет, появится следующее сообщение: "только безопасное содержимое отображается".

**Временное решение**: чтобы устранить эту проблему, настройте SSL в **диспетчере конфигурации служб Reporting Services** на сервере MBAM, на котором установлены службы отчетов SQLServer. Удалите и повторно установите веб-сайт сервера администрирования и мониторинга.

### При нажатии кнопки "назад" в отчете "Сводка соответствия требованиям" может возникнуть ошибка

При детализации отчета "Сводка соответствия требованиям" и нажатии **обратной** ссылки в отчете SSRS может возникнуть ошибка.

**Временное решение**: нет.

### Шифрование только использованного пространства не работает должным образом

Если после установки клиента MBAM вы зашифруете компьютер в первый раз, а вы настроили объект групповой политики, чтобы реализовать шифрование только занятого пространства, MBAM ошибочно шифрует весь диск вместо того, чтобы шифровать использованное место на диске. Если на компьютере уже установлено шифрование только с помощью шифрования "занято", а не установлен клиент MBAM, то MBAM распознает этот параметр и сообщит о том, что шифрование правильно используется в отчетах о соответствии.

**Временное решение**: нет.

### Неправильное отображение стойкости шифра в отчете о соответствии компьютера

Если вы не настроили определенную стойкость шифра в разделе **Выбор метода шифрования диска и объекта групповой политики стойкости шифра** , то отчет о соответствии компьютера в топологии Configuration Manager всегда будет отображаться как **неизвестный** для стойкости шифра, даже если стойкость шифра использует значение по умолчанию 128-битного шифрования. В отчете показана правильная стойкость шифра, если в объекте групповой политики указана определенная стойкость шифра.

**Временное решение**: всегда устанавливайте определенную стойкость шифра в разделе **Выбор метода шифрования диска и объекта групповой политики стойкости шифра** .

### При распределении состояния соответствия по типу диска старые данные отображаются после обновления элементов конфигурации.

После того как вы обновите элементы конфигурации MBAM в SystemCenter2012 ConfigurationManager, распределение состояния соответствия по типам дисков на панели мониторинга соответствия требованиям для предприятий BitLocker показывает данные, основанные на данных из старых версий элементов конфигурации.

**Временное решение**: нет. Изменение элементов конфигурации MBAM не поддерживается, и отчет может не отображаться должным образом.

### Конфигурация усиленной безопасности может привести к тому, что отчеты отображаются неправильно

Если включена конфигурация усиленной безопасности Internet Explorer (ESC), при попытке просмотреть отчеты на сервере MBAM может появиться сообщение об **отказе в доступе** . По умолчанию конфигурация усиленной безопасности включена для защиты сервера путем уменьшения уязвимости сервера до возможных атак, которые могут возникать в веб-контенте и сценариях приложений.

**Временное решение**: Если при попытке просмотреть отчеты на сервере MBAM появляется сообщение " **отказано в доступе** ", вы можете настроить объект групповой политики или изменить параметры по умолчанию вручную в своем изображении, чтобы отключить конфигурацию усиленной безопасности. Кроме того, вы можете просматривать отчеты с другого компьютера, на котором не включена конфигурация усиленной безопасности.

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> Установка сервера MBAM завершается сбоем при переходе с SQLServer2008 на SQLServer2012

Если вы обновите приложение с SQLServer2008 на SQLServer2012 и попытаетесь установить базу данных соответствия требованиям и аудита или базу данных восстановления, установка завершается сбоем и откатывается назад. Эта проблема возникает из-за того, что необходимый файл SQLCMD.exe был удален во время обновления SQLServer и не может быть найден установщиком MBAM. Строки в файле журнала MSI могут выглядеть примерно следующим образом:

Центр восстановления RunDbInstallScript: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery DB: dbInstance-xxxxxx\\I01RunDbInstallScript DB: sqlScript-c:\\program Files Files\\Microsoft\\Microsoft DB: dbname-Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript \ _Recovery \ _and \ _HardwareRunDbInstallScript восстановления базы данных ЦС: MBAM defaultFileName \ _Recovery \ _and \ _HardwareRunDbInstallScript центра восстановления базы данных ЦС: MBAM-defaultDataPath Центр восстановления I01\\MSSQL\\DATA\\RunDbInstallScript: defaultLogPath-K:\\MSSQL\\MSSQL10. Центр восстановления I01\\MSSQL\\Data\\RunDbInstallScript: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\program Files Files\\Microsoft\\Microsoft, администрирование BitLocker и Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript Recovery DB: Начало работы с базой данных восстановления. После этого файл журнала восстановления для Jet-файла будет находиться в разделе" журнал "базы данных ЦС для восстановления:

Установщик Windows MBAM Server имеет закодированный текст, чтобы найти путь SQLCMD.exe, просматривая строковое значение пути в реестре в разделе HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup. Ключ по-прежнему отображается во время миграции из SQLServer2008 в SQLServer2012, но путь, на который ссылается значение данных, не содержит SQLCMD.exe файл, так как процесс SQLupgrade удалил файл.

Временное **решение**: временно переименуйте строковое значение HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup Path на **path \ _OLD**, а затем снова запустите УСТАНОВЩИК Windows на сервере MBAM. После того как установка завершится успешно и создаст базу данных в SQLServer2012, переименуйте **путь \ _OLD** в **путь**.

## Исправления и статьи базы знаний для MBAM 2,0 с пакетом обновления 1 (SP1)


В этом разделе содержатся исправления и статьи базы знаний для MBAM 2,0 с пакетом обновления 1 (SP1).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Статья базы знаний</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Ссылка</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2831166</p></td>
<td align="left"><p>Установка системы администрирования и наблюдения (MBAM 2,0) для Microsoft BitLocker завершается сбоем, если &quot; уже установлены объекты System Center cm&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)">support.microsoft.com/kb/2831166/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870849</p></td>
<td align="left"><p>Пользователи не могут получить ключ восстановления BitLocker с помощью портала самообслуживания MBAM 2.0.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)">support.microsoft.com/kb/2870849/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2756402</p></td>
<td align="left"><p>Клиент MBAM в описании события не сможет выполнить событие с кодом 4 и кодом ошибки 0x8004100E</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620287</p></td>
<td align="left"><p>Сообщение об ошибке "ошибка сервера в"/Reports "приложение" при выборе вкладки "отчеты" в MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)">support.microsoft.com/kb/2620287/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Ошибка при открытии отчетов о соответствии требованиям предприятия или компьютера в MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>Корпоративная отчетность MBAM не обновляется</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2712461</p></td>
<td align="left"><p>Установка MBAM на контроллере домена не поддерживается</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)">support.microsoft.com/kb/2712461/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2876732</p></td>
<td align="left"><p>Сообщение об ошибке с кодом 0x80071a90 во время отдельного процесса или настройки интеграции Configuration Manager для MBAM 2.0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)">support.microsoft.com/kb/2876732/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2754259</p></td>
<td align="left"><p>MBAM и безопасная сетевая связь</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)">support.microsoft.com/kb/2754259/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>Установка MBAM 2.0 завершается сбоем во время интеграции Configuration Manager с SQL Server 2008</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2668533</p></td>
<td align="left"><p>Установка MBAM завершается сбоем, если неправильно настроена служба SSRS SQL</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)">support.microsoft.com/kb/2668533/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870847</p></td>
<td align="left"><p>Программа установки MBAM 2,0 завершает работу с &quot; ошибкой при получении параметров роли сервера Configuration Manager для &#39;точки служб Reporting Services&#39; роли&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)">support.microsoft.com/kb/2870847/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2870839</p></td>
<td align="left"><p>Корпоративные отчеты MBAM 2.0 не обновляются в автономной топологии MBAM 2.0 из-за сбоя в работе CreateCache задания SQL</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)">support.microsoft.com/kb/2870839/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>Корпоративная отчетность MBAM не обновляется</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2935997</p></td>
<td align="left"><p>MBAM поддерживаемые компьютеры с неправильными отчетами о соответствия требованиям включают Неподдерживаемые продукты</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)">support.microsoft.com/kb/2935997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2612822</p></td>
<td align="left"><p>Запись компьютера отклонена в MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)">support.microsoft.com/kb/2612822/EN-US</a></p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Сведения о MBAM 2.0 с пакетом обновления 1 (SP1)](about-mbam-20-sp1.md)

 

 





