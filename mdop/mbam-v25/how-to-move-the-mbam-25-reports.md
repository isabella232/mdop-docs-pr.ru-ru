---
title: Перенос отчетов MBAM 2.5
description: Перенос отчетов MBAM 2.5
author: dansimp
ms.assetid: c8223656-ca9d-41c8-94a3-64d07a6b99e9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdef260b4381671a1b9de66565ece0b70876200
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812392"
---
# Перенос отчетов MBAM 2.5


Используйте эти инструкции, чтобы переместить функцию "отчеты" с одного компьютера на другой, а также переместить функцию "отчеты" с сервера A на сервер B.

Ниже приведены высокоуровневые действия по перемещению отчетов.

1.  Остановите все экземпляры веб-сайта администрирования и мониторинга MBAM.

2.  Установите серверное программное обеспечение MBAM 2,5 на сервере B и настройте функцию "отчеты" на сервере B.

3.  Обновите данные соединения отчетов на серверах администрирования и мониторинга MBAM.

4.  Возобновление работы на веб-сайте администрирования и мониторинга MBAM.

**Примечание**  Чтобы выполнить примеры сценариев Windows PowerShell в этом разделе, необходимо обновить политику выполнения Windows PowerShell, чтобы включить сценарии для выполнения. Инструкции приведены в разделе [выполнение сценариев Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) .

 

**Остановка веб-сайта администрирования и мониторинга MBAM**

-   На сервере, на котором запущен веб-сайт администрирования и наблюдения, остановите веб-сайт администрирования и наблюдения с помощью консоли диспетчера служб IIS.

    Для автоматизации этой процедуры можно использовать Windows PowerShell для ввода команды, которая похожа на приведенную ниже.

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**Установка программного обеспечения сервера MBAM и запуск мастера настройки MBAM сервера на сервере B**

1.  Установка программного обеспечения сервера MBAM на сервере B. Инструкции можно найти [в разделе Установка серверного программного обеспечения MBAM 2,5](installing-the-mbam-25-server-software.md).

2.  На сервере B запустите мастер настройки сервера MBAM, выберите команду **Добавить новые функции**и выберите только функции **отчеты** .

    Кроме того, для настройки отчетов можно использовать командлет Windows PowerShell **Enable-MbamReport** .

    Инструкции по настройке отчетов можно найти в разделе [Настройка MBAM отчетов 2,5](how-to-configure-the-mbam-25-reports.md).

**Обновление данных соединения отчетов на сервере администрирования и мониторинга**

1.  На сервере, на котором работает функция отчетов, обновите URL-адрес отчетов с помощью консоли диспетчера служб IIS.

2.  Разверните раздел **Администрирование и мониторинг Microsoft BitLocker**и выберите узел Служба **поддержки** .

3.  В разделе **Управление** **представлениями "функции**" выберите " **Редактор конфигураций**".

4.  В поле **раздел** выберите параметр **appSettings**.

5.  Выберите строку **коллекция** , а затем нажмите кнопку с многоточием **(...)** в правой части панели, чтобы открыть **Редактор коллекции**.

6.  В **редакторе коллекций**выберите строку, содержащую **Microsoft. MBAM. Reports. URL**, и обновите значение **Microsoft. MBAM. Reports. URL** , чтобы оно отражало имя сервера в сервере B.

    Если вы уже настроили функцию "отчеты" на именованном экземпляре служб SQL Server Reporting Services, добавьте или обновите имя экземпляра по URL-адресу, например:

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  Для автоматизации этой процедуры вы можете использовать Windows PowerShell для выполнения команды на сервере администрирования и мониторинга, как показано в следующем примере кода.

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    Используя описания в следующей таблице, замените значения в примере кода значениями, которые соответствуют вашей среде.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Параметр</th>
    <th align="left">Описание</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>$SERVERNAME $</p></td>
    <td align="left"><p>Имя сервера, на который были перемещены отчеты.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$SRSINSTANCENAME $</p></td>
    <td align="left"><p>Имя экземпляра служб SQL Server Reporting Services, которым были перемещены отчеты.</p></td>
    </tr>
    </tbody>
    </table>

     

**Возобновление работы веб-сайта администрирования и мониторинга**

1.  На сервере, на котором запущен веб-сайт администрирования и наблюдения, запустите веб-сайт администрирования и наблюдения с помощью консоли диспетчера служб IIS.

2.  Для автоматизации этой процедуры можно использовать Windows PowerShell для выполнения команды, которая похожа на описанную ниже.

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    **Примечание**  Для выполнения этой команды необходимо добавить в текущий экземпляр Windows PowerShell модуль IIS для Windows PowerShell.

     



## Статьи по теме


[Настройка отчетов MBAM 2.5](how-to-configure-the-mbam-25-reports.md)

[Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[Перенос компонентов MBAM 2.5 на другой сервер](moving-mbam-25-features-to-another-server.md)

 
## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





