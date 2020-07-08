---
title: Развертывание сервера App-V 5.1 с помощью сценария
description: Развертывание сервера App-V 5.1 с помощью сценария
author: dansimp
ms.assetid: 15c33d7b-9b61-4dbc-8674-399bb33e5f7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/20/2020
ms.openlocfilehash: 579ca685f677aaaa4f5ebb6ac8d2969fdcbe2cd2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814128"
---
# Развертывание сервера App-V 5.1 с помощью сценария

Для того чтобы завершить настройку сервера **appv\_server\_setup.exe** успешно использовать командную строку, необходимо указать и объединить несколько параметров.

## Установка сервера App-V 5,1 с помощью сценария

- Воспользуйтесь следующими сведениями об установке сервера App-V 5,1 с помощью командной строки.

    > [!NOTE]
    > Сведения из приведенных ниже таблиц также можно вызвать с помощью командной строки, введя следующую команду: **appv\_server\_setup.exe/?**.

### Установка сервера управления и базы данных управления на локальном компьютере

Следующие параметры являются допустимыми и для стандартного, и для настраиваемого экземпляра Microsoft SQL Server.

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /DB_PREDEPLOY_MANAGEMENT
- /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT
- /MANAGEMENT_DB_NAME

**Пример: использование настраиваемого экземпляра Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### Установка сервера управления с помощью существующей базы данных управления на локальном компьютере

Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте указанные ниже параметры (отличия от экземпляра по умолчанию *курсивом*).

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**Пример: использование настраиваемого экземпляра Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### Установка сервера управления с помощью существующей базы данных управления на удаленном компьютере

Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**Пример: использование настраиваемого экземпляра Microsoft SQL Server.**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### Установка базы данных управления и сервера управления на одном и том же компьютере

Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**Пример: использование настраиваемого экземпляра Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Установка базы данных управления на компьютере, отличном от сервера управления

Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**Пример: использование настраиваемого экземпляра Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Установка сервера публикаций

Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры.

- /PUBLISHING_SERVER
- /PUBLISHING_MGT_SERVER
- /PUBLISHING_WEBSITE_NAME
- /PUBLISHING_WEBSITE_PORT

**Пример: использование настраиваемого экземпляра Microsoft SQL Server.**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### Установка сервера отчетов и базы данных отчетов на локальном компьютере

Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).

- /REPORTING _SERVER
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /REPORTING _DB_NAME

Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):

- /REPORTING _SERVER
- */REPORTING _ADMINACCOUNT*
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_CUSTOM_SQLINSTANCE*
- /REPORTING _DB_NAME

**Пример: использование настраиваемого экземпляра Microsoft SQL Server.**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### Установка сервера отчетов и использование существующей базы данных отчетов на локальном компьютере

Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).

- /REPORTING _SERVER
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):

- /REPORTING _SERVER
- */REPORTING _ADMINACCOUNT*
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**Пример: использование настраиваемого экземпляра Microsoft SQL Server.**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### Установка сервера отчетов с помощью существующей базы данных отчетов на удаленном компьютере

Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).

- /REPORTING _SERVER
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):

- /REPORTING _SERVER
- */REPORTING _ADMINACCOUNT*
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**Пример: использование настраиваемого экземпляра Microsoft SQL Server.**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### Установка базы данных отчетов на том же компьютере, что и сервер отчетов

Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).

- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /REPORTING _DB_NAME
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):

- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_CUSTOM_SQLINSTANCE*
- /REPORTING _DB_NAME
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**Пример: использование настраиваемого экземпляра Microsoft SQL Server.**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Установка базы данных отчетов на компьютере, отличном от сервера отчетов

Чтобы использовать экземпляр Microsoft SQL Server по умолчанию, используйте указанные ниже параметры (отличие от настраиваемого экземпляра *курсивом*).

- /DB_PREDEPLOY_REPORTING
- /REPORTING _DB_SQLINSTANCE_USE_DEFAULT
- /REPORTING _DB_NAME
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Чтобы использовать настраиваемый экземпляр Microsoft SQL Server, используйте эти параметры (отличия от экземпляра по умолчанию *курсивом*):

- /DB_PREDEPLOY_REPORTING
- /REPORTING _DB_CUSTOM_SQLINSTANCE
- /REPORTING _DB_NAME
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**Пример: использование настраиваемого экземпляра Microsoft SQL Server.**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Определения параметров

#### Общие параметры

| Параметр | Сведения |
|--|--|
| Параметрами | Указывает на автоматическую установку. |
| /UNINSTALL | Указывает на удаление. |
| /LAYOUT | Задает действие макета. Файлы MSI и Script будут извлечены в папку без фактического их установки. Значение не ожидается. |
| /LAYOUTDIR | Указывает каталог макета. Принимает строковое значение. Пример использования: **/LAYOUTDIR = "сервер виртуализации C:\\Application"** |
| /INSTALLDIR | Указывает каталог установки. Принимает строковое значение. Пример использования: **/INSTALLDIR = "C:\\program Files Files\\Application Virtualization\\Server"** |
| /MUOPTIN | Включение центра обновления Майкрософт. Значение не ожидается. |
| /ACCEPTEULA | Принимает лицензионное соглашение. Это необходимо для автоматической установки. Пример использования: **/ACCEPTEULA** или **/ACCEPTEULA = 1** |

#### Параметры установки сервера управления

|Параметр |Сведения |
|--|--|
| /MANAGEMENT_SERVER | Указывает, что сервер управления будет установлен. Значение не ожидается |
| /MANAGEMENT_ADMINACCOUNT | Указывает учетную запись, которая будет разрешена правами администратора на доступ к серверу управления. Это может быть учетная запись пользователя или группа. Пример использования: **/MANAGEMENT_ADMINACCOUNT = "mydomain\\admin"**. Если не задано **/MANAGEMENT_SERVER** , это будет проигнорировано. |
| /MANAGEMENT_WEBSITE_NAME | Указывает имя веб-сайта, который будет создан для службы управления. Пример использования: **/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V Management Service"** |
| MANAGEMENT_WEBSITE_PORT | Указывает номер порта, который будет использоваться службой управления. Пример использования: **/MANAGEMENT_WEBSITE_PORT = 82** |

#### Параметры для базы данных сервера управления

| Параметр | Сведения |
|--|--|
| /DB_PREDEPLOY_MANAGEMENT | Указывает, что база данных управления будет установлена. Чтобы завершить установку, необходимо иметь разрешения, достаточные для базы данных. Значение не ожидается. |
| /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | Указывает, что необходимо использовать экземпляр SQL по умолчанию. Значение не ожидается. |
| /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | Указывает имя настраиваемого экземпляра SQL, который должен использоваться для создания новой базы данных. Пример использования: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"**. Если не задано **/DB_PREDEPLOY_MANAGEMENT** , это будет проигнорировано. |
| /MANAGEMENT_DB_NAME | Указывает имя новой базы данных управления, которую нужно создать. Пример использования: **/MANAGEMENT_DB_NAME = "AppVMgmtDB"**. Если не задано **/DB_PREDEPLOY_MANAGEMENT** , это будет проигнорировано. |
| /MANAGEMENT_SERVER_MACHINE_USE_LOCAL | Указывает, установлен ли на локальном сервере сервер управления, который будет получать доступ к базе данных. Параметр switched, поэтому значение не ожидается. |
| /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT | Учетная запись удаленного компьютера, на котором будет установлен сервер управления. Пример использования: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\\computername"** |
| /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT | Учетная запись администратора, которая будет использоваться для установки сервера управления. Пример использования: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"** |

#### Параметры для установки сервера публикаций

| Параметр | Сведения |
|--|--|
| /PUBLISHING_SERVER | Указывает, что сервер публикаций будет установлен. Значение не ожидается. |
| /PUBLISHING_MGT_SERVER | Указывает URL-адрес службы управления, к которой будет подключаться сервер публикации. Пример использования: ** &lt; имя сервера управления http:// &gt; : &lt; номер &gt; порта сервера управления**. Если **/PUBLISHING_SERVER** не используется, этот параметр будет проигнорирован. |
| /PUBLISHING_WEBSITE_NAME | Указывает имя веб-сайта, который будет создан для службы публикации. Пример использования: **/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing Service"** |
| /PUBLISHING_WEBSITE_PORT | Указывает номер порта, используемого службой публикации. Пример использования: **/PUBLISHING_WEBSITE_PORT = 83** |

#### Параметры сервера отчетов

| Параметр | Сведения |
|--|--|
| /REPORTING_SERVER | Указывает, что сервер отчетов будет установлен. Значение не ожидается. |
| /REPORTING_WEBSITE_NAME | Указывает имя веб-сайта, который будет создан для службы отчетов. Пример использования: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"** |
| /REPORTING_WEBSITE_PORT | Задает номер порта, который будет использоваться службой отчетов. Пример использования: **/REPORTING_WEBSITE_PORT = 82** |

#### Параметры для использования существующей базы данных сервера отчетов

| Параметр | Сведения |
|--|--|
| /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL | Указывает на то, что Microsoft SQL Server установлен на локальном сервере. Параметр switched, поэтому значение не ожидается. |
| /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME | Указывает имя удаленного компьютера, на котором установлен SQL Server. Принимает строковое значение. Пример использования: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| EXISTING_ СОЗДАНИЕ ОТЧЕТОВ _DB_SQLINSTANCE_USE_DEFAULT | Указывает на то, что используется экземпляр SQL по умолчанию. Параметр switched, поэтому значение не ожидается. |
| /EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE | Указывает имя настраиваемого экземпляра SQL, который нужно использовать. Принимает строковое значение. Пример использования: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"** |
| EXISTING_ СОЗДАНИЕ ОТЧЕТОВ _DB_NAME | Указывает имя существующей базы данных отчетов, которую следует использовать. Принимает строковое значение. Пример использования: **/EXISTING_REPORTING_DB_NAME = "AppVReporting"** |

#### Параметры для установки базы данных сервера отчетов

| Параметр | Сведения |
|--|--|
| /DB_PREDEPLOY_REPORTING | Указывает, что база данных отчетов будет установлена. Для этой установки требуются разрешения администратора баз данных. Значение не ожидается. |
| /REPORTING_DB_SQLINSTANCE_USE_DEFAULT | Указывает имя настраиваемого экземпляра SQL, который нужно использовать. Принимает строковое значение. Пример использования: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"** |
| /REPORTING_DB_NAME | Указывает имя новой базы данных отчетов, которую нужно создать. Принимает строковое значение. Пример использования: **/REPORTING_DB_NAME = "AppVMgmtDB"** |
| /REPORTING_SERVER_MACHINE_USE_LOCAL | Указывает на то, что сервер отчетов, на котором будет выполняться доступ к базе данных, установлен на локальном сервере. Параметр switched, поэтому значение не ожидается. |
| /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT | Указывает учетную запись компьютера на удаленном компьютере, на котором будет установлен сервер отчетов. Принимает строковое значение. Пример использования: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"** |
| /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT | Указывает учетную запись администратора, которая будет использоваться для установки сервера отчетов App-V. Принимает строковое значение. Пример использования: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"** |

#### Параметры для использования существующей базы данных сервера управления

| Параметр | Сведения |
|--|--|
| /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL | Указывает на то, что сервер SQL Server установлен на локальном сервере. Параметр switched, поэтому значение не ожидается. Если указан **/DB_PREDEPLOY_MANAGEMENT** , это будет проигнорировано. |
| /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME | Указывает имя удаленного компьютера, на котором установлен SQL Server. Принимает строковое значение. Пример использования: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| /EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | Указывает на то, что используется экземпляр SQL по умолчанию. Параметр switched, поэтому значение не ожидается. Если указан **/DB_PREDEPLOY_MANAGEMENT** , это будет проигнорировано. |
| /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | Указывает имя настраиваемого экземпляра SQL, который будет использоваться. Пример использования **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**. Если указан **/DB_PREDEPLOY_MANAGEMENT** , это будет проигнорировано. |
| /EXISTING_MANAGEMENT_DB_NAME | Указывает имя существующей базы данных управления, которую следует использовать. Пример использования: **/EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB"**. Если указан **/DB_PREDEPLOY_MANAGEMENT** , это будет проигнорировано. |

У вас возникла ошибка App-V? Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме

[Развертывание сервера App-V 5.1](deploying-the-app-v-51-server.md)
