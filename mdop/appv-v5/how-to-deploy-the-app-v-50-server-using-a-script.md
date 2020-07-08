---
title: Развертывание сервера App-V 5.0 с помощью сценария
description: Развертывание сервера App-V 5.0 с помощью сценария
author: dansimp
ms.assetid: b91a35c8-df9e-4065-9187-abafbe565b84
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: aeb16d166fe7b1c4bb418c212024c49f6b151b94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814168"
---
# Развертывание сервера App-V 5.0 с помощью сценария


Для того чтобы завершить настройку сервера **appv\_server\_setup.exe** успешно использовать командную строку, необходимо указать и объединить несколько параметров.

Чтобы получить дополнительные сведения об установке App-V 5,0 Server с помощью командной строки, воспользуйтесь приведенными ниже таблицами.

>[!NOTE]
> Сведения из приведенных ниже таблиц также можно вызвать с помощью командной строки, введя следующую команду:
>```
> appv\_server\_setup.exe /?
>```

## Общие параметры и примеры

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Установка сервера управления и базы данных управления на локальном компьютере.</p></td>
    <td align="left"><p>Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Пример использования настраиваемого экземпляра Microsoft SQL Server.</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "Служба управления Microsoft AppV"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>
     
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Установка сервера управления с помощью существующей базы данных управления на локальном компьютере.</p></td>
    <td align="left"><p>Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Пример использования настраиваемого экземпляра Microsoft SQL Server.</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "Служба управления Microsoft AppV"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p>
    <p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>  

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Установка сервера управления с помощью существующей базы данных управления на удаленном компьютере.</p></td>
    <td align="left"><p>Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Пример использования настраиваемого экземпляра Microsoft SQL Server.</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "Служба управления Microsoft AppV"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME = "SqlServermachine. имя_домена"</p>
    <p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>
    
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Установка базы данных управления и сервера управления на одном и том же компьютере.</p></td>
    <td align="left"><p>Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Пример использования настраиваемого экземпляра Microsoft SQL Server.</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p>
    <p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p>
    <p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Чтобы установить базу данных управления на компьютере, отличном от сервера управления.</p></td>
    <td align="left"><p>Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Пример использования настраиваемого экземпляра Microsoft SQL Server.</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p>
    <p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</p>
    <p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Установка сервера публикаций.</p></td>
    <td align="left"><p>Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</p>
    <ul>
    <li><p>/PUBLISHING_SERVER</p></li>
    <li><p>/PUBLISHING_MGT_SERVER</p></li>
    <li><p>/PUBLISHING_WEBSITE_NAME</p></li>
    <li><p>/PUBLISHING_WEBSITE_PORT</p></li>
    </ul>
    <p>Пример использования настраиваемого экземпляра Microsoft SQL Server.</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/PUBLISHING_SERVER</p>
    <p>/PUBLISHING_MGT_SERVER = " http://ManagementServerName:ManagementPort "</p>
    <p>/PUBLISHING_WEBSITE_NAME = "Служба публикации Microsoft AppV Service"</p>
    <p>/PUBLISHING_WEBSITE_PORT = "8081"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Установка сервера отчетов и базы данных отчетов на локальном компьютере.</p></td>
    <td align="left"><p>Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    </ul>
    <p>Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _ADMINACCOUNT</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    </ul>
    <p>Пример использования настраиваемого экземпляра Microsoft SQL Server.</p>
    <ul>
    <li><p>/appv_server_setup.exe/QUIET</p></li>
    <li><p>/REPORTING_SERVER</p></li>
    <li><p>/REPORTING_WEBSITE_NAME = "Служба Microsoft AppV Reporting Service"</p></li>
    <li><p>/REPORTING_WEBSITE_PORT = "8082"</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p></li>
    <li><p>/REPORTING_DB_NAME = "AppVReporting"</p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Установка сервера отчетов и использование существующей базы данных отчетов на локальном компьютере.</p></td>
    <td align="left"><p>Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _ADMINACCOUNT</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Пример использования настраиваемого экземпляра Microsoft SQL Server.</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/REPORTING_SERVER</p>
    <p>/REPORTING_WEBSITE_NAME = "Служба Microsoft AppV Reporting Service"</p>
    <p>/REPORTING_WEBSITE_PORT = "8082"</p>
    <p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p>
    <p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXITING_REPORTING_DB_NAME = "AppVReporting"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Установка сервера отчетов с помощью существующей базы данных отчетов на удаленном компьютере.</p></td>
    <td align="left"><p>Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _ADMINACCOUNT</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Пример использования настраиваемого экземпляра Microsoft SQL Server.</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/REPORTING_SERVER</p>
    <p>/REPORTING_WEBSITE_NAME = "Служба Microsoft AppV Reporting Service"</p>
    <p>/REPORTING_WEBSITE_PORT = "8082"</p>
    <p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME = "SqlServerMachine. имя_домена"</p>
    <p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXITING_REPORTING_DB_NAME = "AppVReporting"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Чтобы установить базу данных отчетов на том же компьютере, что и сервер отчетов.</p></td>
    <td align="left"><p>Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    <li><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    <li><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Пример использования настраиваемого экземпляра Microsoft SQL Server.</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_REPORTING</p>
    <p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/REPORTING_DB_NAME = "AppVReporting"</p>
    <p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p>
    <p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Чтобы установить базу данных отчетов на компьютере, отличном от сервера отчетов.</p></td>
    <td align="left"><p>Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    <li><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте следующие параметры:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    <li><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Пример использования настраиваемого экземпляра Microsoft SQL Server.</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_REPORTING</p>
    <p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/REPORTING_DB_NAME = "AppVReporting"</p>
    <p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</p>
    <p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

## Определения параметров

### Общие параметры

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Параметр</th>
    <th align="left">Сведения</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Параметрами</p></td>
    <td align="left"><p>Указывает на автоматическую установку.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/UNINSTALL</p></td>
    <td align="left"><p>Указывает на удаление.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/LAYOUT</p></td>
    <td align="left"><p>Задает действие макета. Файлы MSI и Script будут извлечены в папку без фактического их установки. Значение не ожидается.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/LAYOUTDIR</p></td>
    <td align="left"><p>Указывает каталог макета. Принимает строковое значение. Например,/LAYOUTDIR = "сервер виртуализации C:\Application"</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/INSTALLDIR</p></td>
    <td align="left"><p>Указывает каталог установки. Принимает строковое значение. Например: /INSTALLDIR = "C:\Program Files\Application Virtualization\Server"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MUOPTIN</p></td>
    <td align="left"><p>Включение центра обновления Майкрософт. Значение не ожидается</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/ACCEPTEULA</p></td>
    <td align="left"><p>Принимает лицензионное соглашение. Это необходимо для автоматической установки. Пример использования: <strong> /ACCEPTEULA </strong> или <strong> /ACCEPTEULA = 1 </strong> .</p></td>
    </tr>
    </tbody>
    </table>

### Параметры установки сервера управления

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Параметр</th>
    <th align="left">Сведения</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER</p></td>
    <td align="left"><p>Указывает, что сервер управления будет установлен. Значение не ожидается</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_ADMINACCOUNT</p></td>
    <td align="left"><p>Указывает учетную запись, которой будет разрешено администратору получить доступ к серверу управления. Эта учетная запись может быть отдельной учетной записью пользователя или группой. Пример использования: <strong> /MANAGEMENT_ADMINACCOUNT = "mydomain\admin" </strong> . Если <strong> </strong> не задано/MANAGEMENT_SERVER, это будет проигнорировано. Указывает учетную запись, которой будет разрешено администратору получить доступ к серверу управления. Это может быть учетная запись пользователя или группа. Например, <strong> /MANAGEMENT_ADMINACCOUNT = &quot; mydomain\admin &quot; </strong> .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_WEBSITE_NAME</p></td>
    <td align="left"><p>Указывает имя веб-сайта, который будет создан для службы управления. Например,/MANAGEMENT_WEBSITE_NAME = "Служба управления Microsoft App-V"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>MANAGEMENT_WEBSITE_PORT</p></td>
    <td align="left"><p>Указывает номер порта, который будет использоваться службой управления. Например,/MANAGEMENT_WEBSITE_PORT = 82.</p></td>
    </tr>
    </tbody>
    </table>

### Параметры для базы данных сервера управления

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Параметр</th>
    <th align="left">Сведения</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/DB_PREDEPLOY_MANAGEMENT</p></td>
    <td align="left"><p>Указывает, что база данных управления будет установлена. Чтобы завершить установку, необходимо иметь разрешения, достаточные для базы данных. Значение не ожидается</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Указывает, что необходимо использовать экземпляр SQL по умолчанию. Значение не ожидается.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Указывает имя настраиваемого экземпляра SQL, который должен использоваться для создания новой базы данных. Пример использования: <strong> /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER" </strong> . Если не задано/DB_PREDEPLOY_MANAGEMENT, это будет проигнорировано.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_DB_NAME</p></td>
    <td align="left"><p>Указывает имя новой базы данных управления, которую нужно создать. Пример использования: <strong> /MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> . Если не задано/DB_PREDEPLOY_MANAGEMENT, это будет проигнорировано.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
    <td align="left"><p>Указывает, установлен ли на локальном сервере сервер управления, который будет получать доступ к базе данных. Параметр switched, поэтому значение не ожидается.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
    <td align="left"><p>Учетная запись удаленного компьютера, на котором будет установлен сервер управления. Пример использования: <strong> /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"</strong></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
    <td align="left"><p>Учетная запись администратора, которая будет использоваться для установки сервера управления. Пример использования: <strong> /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\alias"</strong></p></td>
    </tr>
    </tbody>
    </table>

### Параметры для установки сервера публикаций

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Параметр</th>
    <th align="left">Сведения</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/PUBLISHING_SERVER</p></td>
    <td align="left"><p>Указывает, что сервер публикаций будет установлен. Значение не ожидается</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/PUBLISHING_MGT_SERVER</p></td>
    <td align="left"><p>Указывает URL-адрес службы управления, к которой будет подключаться сервер публикации. Пример использования: <strong> &lt; имя сервера управления http:// &gt; : &lt; номер порта сервера управления &gt; </strong> . Если/PUBLISHING_SERVER не используется, этот параметр будет проигнорирован.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/PUBLISHING_WEBSITE_NAME</p></td>
    <td align="left"><p>Указывает имя веб-сайта, который будет создан для службы публикации. Например,/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing Service"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/PUBLISHING_WEBSITE_PORT</p></td>
    <td align="left"><p>Указывает номер порта, используемого службой публикации. Например,/PUBLISHING_WEBSITE_PORT = 83</p></td>
    </tr>
    </tbody>
    </table>

### Параметры сервера отчетов

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Параметр</th>
    <th align="left">Сведения</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/REPORTING_SERVER</p></td>
    <td align="left"><p>Указывает, что сервер отчетов будет установлен. Значение не ожидается</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_WEBSITE_NAME</p></td>
    <td align="left"><p>Указывает имя веб-сайта, который будет создан для службы отчетов. Например: /REPORTING_WEBSITE_NAME = &quot; Microsoft App-V ReportingService&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_WEBSITE_PORT</p></td>
    <td align="left"><p>Задает номер порта, который будет использоваться службой отчетов. Например: /REPORTING_WEBSITE_PORT = 82</p></td>
    </tr>
    </tbody>
    </table>

     

### Параметры для использования существующей базы данных сервера отчетов

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Параметр</th>
    <th align="left">Сведения</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></td>
    <td align="left"><p>Указывает на то, что Microsoft SQL Server установлен на локальном сервере. Параметр switched, поэтому значение не ожидается.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></td>
    <td align="left"><p>Указывает имя удаленного компьютера, на котором установлен SQL Server. Принимает строковое значение. Например: /EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>EXISTING_ создание отчетов <em> DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Указывает на то, что используется экземпляр SQL по умолчанию. Параметр switched, поэтому значение не ожидается.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING </em> REPORTING_DB_CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Указывает имя настраиваемого экземпляра SQL, который нужно использовать. Принимает строковое значение. Например: /EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYSQLSERVER&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>EXISTING_ СОЗДАНИЕ ОТЧЕТОВ _DB_NAME</p></td>
    <td align="left"><p>Указывает имя существующей базы данных отчетов, которую следует использовать. Принимает строковое значение. Например: /EXISTING_REPORTING_DB_NAME = &quot; AppVReporting&quot;</p></td>
    </tr>
    </tbody>
    </table>

### Параметры для установки базы данных сервера отчетов

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Параметр</th>
    <th align="left">Сведения</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/DB_PREDEPLOY_REPORTING</p></td>
    <td align="left"><p>Указывает, что база данных отчетов будет установлена. Для этой установки требуются разрешения администратора баз данных. Значение не ожидается</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Указывает имя настраиваемого экземпляра SQL, который нужно использовать. Принимает строковое значение. Например: /REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYSQLSERVER&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_DB_NAME</p></td>
    <td align="left"><p>Указывает имя новой базы данных отчетов, которую нужно создать. Принимает строковое значение. Например: /REPORTING_DB_NAME = &quot; AppVMgmtDB&quot;</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
    <td align="left"><p>Указывает на то, что сервер отчетов, на котором будет выполняться доступ к базе данных, установлен на локальном сервере. Параметр switched, поэтому значение не ожидается.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
    <td align="left"><p>Указывает учетную запись компьютера на удаленном компьютере, на котором будет установлен сервер отчетов. Принимает строковое значение. Например: /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot; DOMAIN\COMPUTERNAME&quot;</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
    <td align="left"><p>Указывает учетную запись администратора, которая будет использоваться для установки сервера отчетов App-V. Принимает строковое значение. Например: /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot; domain\alias&quot;</p></td>
    </tr>
    </tbody>
    </table>

### Параметры для использования существующей базы данных сервера управления

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Параметр</th>
    <th align="left">Сведения</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></td>
    <td align="left"><p>Указывает на то, что сервер SQL Server установлен на локальном сервере. Параметр switched, поэтому значение не ожидается. Если указан/DB_PREDEPLOY_MANAGEMENT, это будет проигнорировано.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></td>
    <td align="left"><p>Указывает имя удаленного компьютера, на котором установлен SQL Server. Принимает строковое значение. Например: /EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Указывает на то, что используется экземпляр SQL по умолчанию. Параметр switched, поэтому значение не ожидается. Если указан/DB_PREDEPLOY_MANAGEMENT, это будет проигнорировано.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Указывает имя настраиваемого экземпляра SQL, который будет использоваться. Пример использования <strong> /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement" </strong> . Если указан/DB_PREDEPLOY_MANAGEMENT, это будет проигнорировано.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_NAME</p></td>
    <td align="left"><p>Указывает имя существующей базы данных управления, которую следует использовать. Пример использования: <strong> /EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> . Если указан/DB_PREDEPLOY_MANAGEMENT, это будет проигнорировано.</p>
    <p></p>
    <p><strong>У вас есть предложение App-V </strong> ? Здесь вы можете добавить предложения и проголосовать <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)"> здесь </a> . <strong>У вас есть приложение-V issu </strong> e? Используйте <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)"> Форум TechNet App-V </a> .</p></td>
</tr>
</tbody>
</table>
  

## Статьи по теме

[Развертывание сервера App-V 5.0](deploying-the-app-v-50-server.md)

 

 





