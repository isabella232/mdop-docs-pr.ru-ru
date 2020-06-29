---
title: Развертывание клиента App-V
description: Развертывание клиента App-V
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814125"
---
# Развертывание клиента App-V


Чтобы установить клиент служб Microsoft Application Virtualization (App-V) 5,1 и клиент службы удаленных рабочих столов, выполните указанные ниже действия. Необходимо установить версию клиента, соответствующую операционной системе целевого компьютера.

<a href="" id="bkmk-clt-install-prereqs"></a>**Что необходимо сделать перед началом работы**

1. Проверьте и установите необходимые компоненты программного обеспечения.

   Установите необходимое программное обеспечение, соответствующее версии App-V, которую вы устанавливаете:

   -   [Сведения об App-V 5.1](about-app-v-51.md)

   -   [Предварительные требования App-V 5.1](app-v-51-prerequisites.md)

2. Проверка сосуществования клиентов и неподдерживаемых сценариев, применимых к установке:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Развертывание существующих клиентов App-V</p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)">Планирование развертывания программы Sequencer и клиента App-V 5.1</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Неподдерживаемые или ограниченные сценарии установки</p></td>
   <td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">Поддерживаемые конфигурации App-V 5,1 см. в разделе "клиент"</a></p></td>
   </tr>
   </tbody>
   </table>



3. Ознакомьтесь со сведениями о поиске и устранении неполадок в реестре клиента.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Сведения о клиентском реестре</p></td>
<td align="left"><ul>
<li><p>По умолчанию после установки клиента App-V 5,1 сведения о клиенте хранятся в реестре в следующем разделе реестра:</p>
<p><strong>HKEY_LOCAL_MACHINE \ ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ \ MICROSOFT \ APPV \ КЛИЕНТ</strong></p></li>
<li><p>При развертывании виртуализированного пакета на компьютере, на котором запущен клиент App-V, связанные данные пакета хранятся в следующем расположении:</p>
<p><strong>C: \ ProgramData \ App-V</strong></p>
<p>Однако вы можете изменить это расположение с помощью следующего раздела реестра:</p>
<p><strong>HKEY_LOCAL_MACHINE \ ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ \ MICROSOFT \ ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ \ MICROSOFT \ APPV \ КЛИЕНТ \ STREAMING \ PACKAGEINSTALLATIONROOT</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Файлы журнала клиента</p></td>
<td align="left"><ul>
<li><p>Сведения о файле журнала, связанном с клиентом App-V 5,1, можно найти в следующем журнале:</p>
<p><strong>Журналы событий, журналы приложений и служб/Microsoft/AppV</strong></p></li>
<li><p>В приложении App-V 5,0 с пакетом обновления 3 (SP3) некоторые журналы были консолидированы и перемещены в следующее расположение:</p>
<p><strong>Журналы событий, журналы приложений и служб (Microsoft/AppV/ServiceLog)</strong></p>
<p>Список перемещенных журналов можно найти в разделе <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> о приложении App-V 5,0 SP3 </a> .</p></li>
<li><p>Пакеты, которые в настоящее время хранятся на компьютерах, на которых запущен клиент App-V 5,1, сохраняются в следующем расположении:</p>
<p><strong>C:\ProgramData\App-V &amp; lt; код пакета &gt; &amp; lt; ИД версии&gt;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Сведения об устранении неполадок при установке клиента</p></td>
<td align="left"><p>Просмотрите журнал ошибок в <strong> папке% temp% </strong> . Чтобы просмотреть файлы журнала, нажмите кнопку <strong> Пуск </strong> , введите <strong> % temp% </strong> , а затем найдите <strong> Журнал appv_ </strong> .</p></td>
</tr>
</tbody>
</table>



**Установка клиента App-V 5,1**

1.  Скопируйте установочный файл для клиента App-V 5,1 на компьютер, на котором он будет установлен. Выберите один из следующих типов клиентов:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Тип клиента</th>
    <th align="left">Файл для использования</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Стандартная версия клиента</p></td>
    <td align="left"><p><strong>appv_client_setup.exe</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Версия клиента служб удаленных рабочих столов</p></td>
    <td align="left"><p><strong>appv_client_setup_rds.exe</strong></p></td>
    </tr>
    </tbody>
    </table>



2.  Дважды щелкните файл установки и нажмите кнопку **установить**. Перед началом установки установщик проверяет на компьютере отсутствие [необходимых предварительных требований для App-V 5,1](app-v-51-prerequisites.md).

3.  Прочтите и примите условия лицензионного соглашения на использование программного обеспечения, выберите, нужно ли использовать Microsoft Update и нужно ли принимать участие в программе улучшения качества по Майкрософт, и нажмите кнопку **установить**.

4.  На странице **Настройка успешно завершена** нажмите кнопку **Закрыть**.

    При установке создаются следующие записи для клиента App-V в **приложениях**.

    -   **.exe**

    -   **.msi**

    -   **языковой пакет**

        **Примечание.**  
        После установки можно удалить только exe – файл.



**Установка клиента App-V 5,1 с помощью сценария**

1. Установите все необходимое программное обеспечение на целевые компьютеры. Узнайте, [что необходимо сделать перед](#bkmk-clt-install-prereqs)началом работы. Если вы установили клиент с помощью MSI-файла, то при отсутствии необходимых условий установка завершится сбоем.

2. Чтобы использовать сценарий для установки клиента App-V 5,1, используйте следующие параметры с **appv\_client\_setup.exe**.

   **Примечание.**  
   Клиентский установщик Windows (MSI) поддерживает один и тот же набор переключателей, за исключением параметра **/log** .

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>/INSTALLDIR</p></td>
   <td align="left"><p>Указывает каталог установки. Пример использования: <strong> /INSTALLDIR = C:\Program Files\AppV Client</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/CEIPOPTIN</p></td>
   <td align="left"><p>Включает участие в программе улучшения качества программного обеспечения. Пример использования: <strong> /CEIPOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/MUOPTIN</p></td>
   <td align="left"><p>Включение центра обновления Майкрософт. Пример использования: <strong> /MUOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/PACKAGEINSTALLATIONROOT</p></td>
   <td align="left"><p>Задает каталог, в который устанавливаются все новые приложения и обновления. Пример использования: <strong> /PACKAGEINSTALLATIONROOT =&#39;C:\App-V packages&#39;</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/PACKAGESOURCEROOT</p></td>
   <td align="left"><p>Переопределяет исходное расположение для загрузки содержимого пакета. Пример использования: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/AUTOLOAD</p></td>
   <td align="left"><p>Указывает, как приложение App-V 5,1 будет загружать новые пакеты для определенного компьютера. Доступны следующие параметры: [1]; Автоматическая загрузка всех пакетов [2]; или автоматически загружает пакеты [0]. <strong> Пример использования:/AUTOLOAD = [0 | 1 | 2]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/SHAREDCONTENTSTOREMODE</p></td>
   <td align="left"><p>Указывает на то, что содержимое потокового пакета не будет сохранено на локальном жестком диске. Пример использования: <strong> /SHAREDCONTENTSTOREMODE = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/MIGRATIONMODE</p></td>
   <td align="left"><p>Позволяет клиенту App-V 5,1 изменять сочетания клавиш и FTAs, связанные с пакетами, созданными с помощью более ранней версии. Пример использования: <strong> /MIGRATIONMODE = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ENABLEPACKAGESCRIPTS</p></td>
   <td align="left"><p>Включает сценарии, определенные в файле манифеста пакета или файлах конфигурации, которые должны выполняться. Пример использования: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/ROAMINGREGISTRYEXCLUSIONS</p></td>
   <td align="left"><p>Указывает пути реестра, которые не будут перемещаться с помощью профиля пользователя. Пример использования: <strong> /ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ROAMINGFILEEXCLUSIONS</p></td>
   <td align="left"><p>Указывает пути к файлам относительно% UserProfile%, которые не перемещаются с помощью профиля пользователя&#39;s. Пример использования: <strong> /ROAMINGFILEEXCLUSIONS &#39;Desktop; мои рисунки&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERNAME</p></td>
   <td align="left"><p>Отображает имя сервера публикаций. Пример использования: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERURL</p></td>
   <td align="left"><p>Отображает URL-адрес сервера публикаций. Пример использования: <strong> /S2PUBLISHINGSERVERURL = \pubserver</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHENABLED-</p></td>
   <td align="left"><p>Включает глобальное обновление публикации. Пример использования: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHONLOGON</p></td>
   <td align="left"><p>Инициирует глобальное обновление публикации при входе пользователя в систему. Пример использования: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVAL-</p></td>
   <td align="left"><p>Указывает интервал обновления публикации, где <strong> 0 </strong> означает, что обновление не выполняется периодически. Пример использования: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>Указывает единицу интервала (часы [0], дни [1]). Пример использования: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHENABLED</p></td>
   <td align="left"><p>Включает обновление публикации пользователей. Пример использования: <strong> /S2USERREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHONLOGON</p></td>
   <td align="left"><p>Инициирует обновление публикации пользователя, когда пользователь входит в систему. Пример использования: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVAL-</p></td>
   <td align="left"><p>Указывает интервал обновления публикации, где <strong> 0 </strong> означает, что обновление не выполняется периодически. Пример использования: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>Указывает единицу интервала (часы [0], дни [1]). Пример использования: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/Log</p></td>
   <td align="left"><p>Задает расположение, в котором сохраняются данные журнала. По умолчанию используется расположение% Temp%. Пример использования: <strong> /log C:\logs\log.log</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/q</p></td>
   <td align="left"><p>Указывает на автоматическую установку.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/REPAIR</p></td>
   <td align="left"><p>Восстановление предыдущей версии клиента.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/NORESTART</p></td>
   <td align="left"><p>Предотвращает перезагрузку компьютера после установки клиента.</p>
   <p>Этот параметр предотвращает перезагрузку компьютера конечного пользователя после установки каждого обновления и позволяет запланировать перезагрузку в удобное для вас время. Например, можно установить приложение App-V 5,1, а затем установить пакет исправлений Y без перезагрузки после установки пакета обновления. После установки необходимо перезагрузить компьютер, прежде чем приступить к работе с приложением-V.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/UNINSTALL</p></td>
   <td align="left"><p>Удаление клиента.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ACCEPTEULA</p></td>
   <td align="left"><p>Принимает лицензионное соглашение. Это необходимо для автоматической установки. Пример использования: <strong> /ACCEPTEULA </strong> или <strong> /ACCEPTEULA = 1 </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/LAYOUT</p></td>
   <td align="left"><p>Задает связанное действие макета. Кроме того, приложение App-V 5,1 будет извлечено из файла установщика Windows (MSI) и файлов сценариев в папку. Значение не ожидается.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/LAYOUTDIR</p></td>
   <td align="left"><p>Указывает каталог макета. Требуется строковое значение. Пример использования: <strong> /LAYOUTDIR = "клиент виртуализации C:\Application" </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/?,/h,/Help</p></td>
   <td align="left"><p>Запросы на помощь по предыдущим параметрам установки.</p></td>
   </tr>
   </tbody>
   </table>



**Установка клиента App-V 5,1 с помощью файла установщика Windows (MSI)**

1.  Установите необходимые компоненты на целевые компьютеры. Узнайте, [что необходимо сделать перед](#bkmk-clt-install-prereqs)началом работы. Если какие – либо условия не выполняются, установка завершится сбоем.

2.  Убедитесь, что на конечных компьютерах нет отложенных перезапусков перед установкой клиента с помощью файлов установщика Windows App-V 5,1 (MSI). Файлы установщика Windows не помечают отложенный перезапуск.

3.  Развернуть один из указанных ниже файлов установщика Windows на целевом компьютере. Указанный вами файл должен соответствовать конфигурации целевого компьютера.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Тип развертывания</th>
    <th align="left">Развертывание файла</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Компьютер работает под управлением 32-разрядной операционной системы Microsoft Windows</p></td>
    <td align="left"><p>appv_client_MSI_x86.msi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Компьютер работает под управлением 64-разрядной операционной системы Microsoft Windows</p></td>
    <td align="left"><p>appv_client_MSI_x64.msi</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Вы разворачиваете клиент служб удаленных рабочих столов App-V 5,1</p></td>
    <td align="left"><p>appv_client_rds_MSI_x64.msi</p></td>
    </tr>
    </tbody>
    </table>



4.  В соответствии с приведенной ниже таблицей выберите соответствующий языковой пакет **. msi** для установки на основе нужного языка для целевого компьютера. **XXXX** в таблице указывает целевой языковой стандарт для языкового пакета.

    **Что нужно знать перед началом работы:**

    -   Языковые пакеты являются общими для стандартного клиента App-V 5,1 и версии служб удаленных рабочих столов клиента App-V 5,1.

    -   Если вы установили клиент App-V 5,1 с помощью **exe**, установщик развернет только языковой пакет, соответствующий операционной системе, работающей на целевом компьютере.

    -   Чтобы развернуть дополнительные языковые пакеты на целевом компьютере, выполните описанные ниже действия, **чтобы установить клиент App-V 5,1 с помощью файла установщика Windows (MSI)**.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Тип развертывания</th>
    <th align="left">Развертывание файла</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Компьютер работает под управлением 32-разрядной операционной системы Microsoft Windows</p></td>
    <td align="left"><p>appv_client_LP_xxxx_ x86.msi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Компьютер работает под управлением 64-разрядной операционной системы Microsoft Windows</p></td>
    <td align="left"><p>appv_client_LP_xxxx_ x64.msi</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Статьи по теме


[Развертывание App-V 5.1](deploying-app-v-51.md)

[Сведения о параметрах конфигурации клиента](about-client-configuration-settings51.md)

[Удаление клиента App-V 5.1](how-to-uninstall-the-app-v-51-client.md)









