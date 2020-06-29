---
title: Оценка MBAM 2.5 в тестовой среде
description: Оценка MBAM 2.5 в тестовой среде
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823152"
---
# Оценка MBAM 2.5 в тестовой среде


В этой статье описано, как настроить тестовую среду для оценки администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5 в изолированной топологии интеграции или диспетчере System Center Configuration Manager.

## Оценка MBAM 2,5 с помощью изолированной топологии


Чтобы вычислить MBAM с помощью изолированной топологии, используйте сведения из приведенных ниже таблиц, чтобы установить программное обеспечение сервера MBAM, а затем настройте компоненты сервера MBAM в тестовой среде.

**Оценка MBAM 2,5 с помощью изолированной топологии**

1. Прежде чем устанавливать MBAM, выполните указанные ниже действия.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Задача</th>
   <th align="left">Где найти инструкции</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Убедитесь, что вы установили все необходимое программное обеспечение.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Проверьте требования к оборудованию, ОЗУ и другим требованиям.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Поддерживаемые конфигурации MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Если вы планируете использовать командлеты для настройки MBAM, ознакомьтесь с необходимыми требованиями для использования Windows PowerShell.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</a></p></td>
   </tr>
   </tbody>
   </table>



2. Установите программное обеспечение сервера MBAM и настройте необходимые функции.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Задача</th>
   <th align="left">Где найти инструкции</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Установите серверное программное обеспечение MBAM на каждый сервер, на котором вы хотите настроить компонент MBAM Server.</p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Установка программного обеспечения MBAM 2.5 Server</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Настройте базу данных соответствия и аудита, а также базу данных восстановления.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Настройка баз данных MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Настройка функции "отчеты".</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Настройка отчетов MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Настройте веб-приложения.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Настройка веб-приложений MBAM 2.5</a></p></td>
   </tr>
   </tbody>
   </table>



3. На клиентском компьютере выполните указанные ниже действия.

   1.  Установите клиент MBAM на клиентском компьютере.

   2.  Примените на компьютере объекты групповой политики MBAM (GPO).

   3.  Задайте указанные ниже разделы реестра, чтобы клиент MBAM быстрее пробудиться и через регулярные интервалы времени.

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Примечание.**  
       Поскольку эти ключи выключаются из клиента MBAM каждую минуту, рекомендуется использовать эти параметры реестра только в тестовой среде.



   4.  Перезапустите **службу клиента управления BitLocker**.

## Оценка MBAM 2,5 с помощью топологии интеграции System Center 2012 Configuration Manager


Чтобы оценить MBAM с помощью топологии интеграции Configuration Manager, используйте сведения из приведенных ниже таблиц, чтобы установить программное обеспечение сервера MBAM, а затем настройте компоненты сервера MBAM в тестовой среде. После установки клиента MBAM на клиентском компьютере вы можете выполнить дополнительные действия, чтобы заставить клиента MBAM сообщать о состоянии компьютера в MBAM быстрее.

**Оценка MBAM 2,5 с помощью топологии интеграции System Center 2012 Configuration Manager**

1. Перед установкой MBAM ознакомьтесь с необходимым программным обеспечением и поддерживаемой конфигурацией.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Задача</th>
   <th align="left">Где найти инструкции</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Убедитесь, что вы установили все необходимое программное обеспечение.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Проверьте требования к оборудованию, ОЗУ и другим требованиям.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Поддерживаемые конфигурации MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Если вы планируете использовать командлеты для настройки MBAM, ознакомьтесь с необходимыми требованиями для использования Windows PowerShell.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Создание и изменение MOF-файлов.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Изменение файла Configuration.mof</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Создание или изменение файла Sms_def.mof</a></p></td>
   </tr>
   </tbody>
   </table>



2. Установите программное обеспечение сервера MBAM и настройте необходимые функции.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Задача</th>
   <th align="left">Где найти инструкции</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Установите серверное программное обеспечение MBAM на каждый сервер, на котором вы хотите настроить компонент MBAM Server.</p>
   <div class="alert">
   <strong>Примечание.</strong><br/><p>Вы можете установить базы данных на удаленном компьютере SQL Server с помощью Windows PowerShell или пакета экспортированного приложения уровня данных (DAC). Дополнительные сведения о пакетах DAC можно найти в разделе <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> приложения уровня данных </a> .</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Установка программного обеспечения MBAM 2.5 Server</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Настройте базу данных соответствия и аудита, а также базу данных восстановления.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Настройка баз данных MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Настройка функции "отчеты".</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Настройка отчетов MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Настройте веб-приложения.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Настройка веб-приложений MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Настройте System Center Configuration Manager, чтобы установить объекты Configuration Manager.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Настройка интеграции System Center Configuration Manager с MBAM 2.5</a></p></td>
   </tr>
   </tbody>
   </table>



3. На клиентском компьютере выполните указанные ниже действия.

   1.  Установите клиент MBAM и клиент Configuration Manager на клиентском компьютере.

   2.  Примените объекты групповой политики MBAM к компьютеру.

   3.  Задайте указанные ниже разделы реестра, чтобы клиент MBAM быстрее пробудиться и через регулярные интервалы времени.

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Примечание.**  
       Поскольку эти ключи выключаются из клиента MBAM каждую минуту, рекомендуется использовать эти параметры реестра только в тестовой среде.



   4.  Перезапустите **службу клиента управления BitLocker**.

   5.  На панели управления откройте **Configuration Manager**и откройте вкладку **действия** .

   6.  Выберите " **цикл инвентаризации оборудования**" и нажмите кнопку " **выполнить сейчас**". Этот шаг запускает инвентаризацию оборудования, используя новые классы, импортированные в MOF-файлы, а затем отправляет их на сервер Configuration Manager.

   7.  Выберите пункт **Получение политики компьютера & цикл оценки**, а затем нажмите кнопку **выполнить** , чтобы применить объекты групповой политики, которые относятся к этому клиентскому компьютеру.



4. На консоли Configuration Manager выполните указанные ниже действия.

   1.  В области навигации щелкните правой кнопкой мыши **Поддерживаемые компьютеры MBAM**, выберите команду **Обновить членство**, а затем нажмите кнопку **Да** , чтобы заставить клиентский компьютер немедленно сообщить о своей членстве.

   2.  В области навигации щелкните **Поддерживаемые компьютеры MBAM** , чтобы убедиться в том, что клиентский компьютер указан в коллекции.

5. На клиентском компьютере на панели управления снова откройте **Configuration Manager** и выполните указанные ниже действия.

   1.  Откройте вкладку **действия** и перезапустите **цикл оценки & политики компьютера**.

   2.  Откройте вкладку **конфигурации** , выберите базовый план BitLocker и нажмите кнопку **вычислить**.

6. На консоли Configuration Manager убедитесь, что клиентский компьютер отображается в отчете соответствие требованиям предприятия.

   1.  В области навигации выберите рабочую область " **мониторинг** ".

   2.  В дереве консоли разверните раздел отчеты **о отчетах** &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.

   3.  Выберите папку, представляющую язык, на котором вы хотите просмотреть отчеты, а затем выберите отчет в области результатов.

## Оценка MBAM 2,5 с помощью топологии интеграции System Center Configuration Manager 2007


Чтобы вычислить MBAM с помощью топологии интеграции Configuration Manager, выполните те же действия, что и при установке и настройке MBAM в тестовой среде, как вы используете в рабочей среде. После установки клиента MBAM на клиентском компьютере выполните дополнительные действия, описанные в этой статье, чтобы разрешить клиенту MBAM сообщать о состоянии компьютера в MBAM быстрее.

**Оценка MBAM с помощью топологии интеграции Configuration Manager 2007**

1. Перед установкой MBAM выполните указанные ниже действия.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Задача</th>
   <th align="left">Где найти инструкции</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Убедитесь, что вы установили все необходимое программное обеспечение.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Проверьте требования к оборудованию, ОЗУ и другим требованиям.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Поддерживаемые конфигурации MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Создание и изменение MOF-файлов.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Изменение файла Configuration.mof</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Создание или изменение файла Sms_def.mof</a></p></td>
   </tr>
   </tbody>
   </table>



2. Установите программное обеспечение сервера MBAM и настройте необходимые функции.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Задача</th>
   <th align="left">Где найти инструкции</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Установите серверное программное обеспечение MBAM на каждый сервер, на котором вы хотите настроить компонент MBAM Server.</p>
   <div class="alert">
   <strong>Примечание.</strong><br/><p>Вы можете установить базы данных на удаленном компьютере SQL Server с помощью Windows PowerShell или пакета экспортированного приложения уровня данных (DAC). Дополнительные сведения о пакетах DAC можно найти в разделе <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> приложения уровня данных </a> .</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Установка программного обеспечения MBAM 2.5 Server</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Настройте базу данных соответствия и аудита, а также базу данных восстановления.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Настройка баз данных MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Настройка функции "отчеты".</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Настройка отчетов MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Настройте веб-приложения.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Настройка веб-приложений MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Настройте System Center Configuration Manager, чтобы установить объекты Configuration Manager.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Настройка интеграции System Center Configuration Manager с MBAM 2.5</a></p></td>
   </tr>
   </tbody>
   </table>



3. На клиентском компьютере выполните указанные ниже действия.

   1.  Установите клиент MBAM на клиентском компьютере.

   2.  Примените объекты групповой политики MBAM к компьютеру.

   3.  Задайте указанные ниже разделы реестра, чтобы клиент MBAM быстрее выключаюсь и быстрее.

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Примечание.**  
       Поскольку эти ключи выключаются из клиента MBAM каждую минуту, рекомендуется использовать эти параметры реестра только в среде оценки.



   4.  Перезапустите **службу клиента управления BitLocker**.

   5.  На панели управления откройте **Configuration Manager**и откройте вкладку **действия** .

   6.  Выберите пункт **Получение политики компьютера & цикл оценки**, а затем нажмите кнопку **выполнить** , чтобы применить объекты групповой политики, которые относятся к этому клиентскому компьютеру.

   7.  Выберите " **цикл инвентаризации оборудования**" и нажмите кнопку " **выполнить сейчас**". Это действие запускает инвентаризацию оборудования, используя новые классы, импортированные в MOF-файлы, а затем отправляет их на сервер Configuration Manager Server.

4. На консоли Configuration Manager выполните указанные ниже действия.

   1.  В области навигации щелкните правой кнопкой мыши **Поддерживаемые компьютеры MBAM**, выберите команду **Обновить членство**, а затем нажмите кнопку **Да** , чтобы заставить клиентский компьютер немедленно сообщить о своей членстве.

   2.  В области навигации щелкните **Поддерживаемые компьютеры MBAM** , чтобы убедиться в том, что клиентский компьютер указан в коллекции.

5. На клиентском компьютере на панели управления снова откройте **Configuration Manager** и выполните указанные ниже действия.

   1.  Откройте вкладку **действия** и перезапустите **цикл оценки & политики компьютера**.

   2.  Откройте вкладку **конфигурации** , выберите базовый план BitLocker и нажмите кнопку **оценить**.

6. На консоли Configuration Manager убедитесь, что клиентский компьютер отображается в отчете о соответствии требованиям в корпоративной среде, как описано ниже.

   1.  В области навигации разверните узел **Computer Management** &gt; **Reporting** &gt; имя сервера **служб отчетов для службы** управления компьютером &gt; ** &lt; &gt; MBAM**.

   2.  В узле **MBAM** выберите папку, представляющую язык, на котором нужно просмотреть отчеты, а затем выберите отчет в области результатов.


## Статьи по теме


[Начало работы с MBAM 2.5](getting-started-with-mbam-25.md)


## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).





