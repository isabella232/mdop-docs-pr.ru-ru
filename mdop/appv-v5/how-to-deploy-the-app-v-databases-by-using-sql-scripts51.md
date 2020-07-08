---
title: Развертывание баз данных App-V с помощью сценариев SQL
description: Развертывание баз данных App-V с помощью сценариев SQL
author: dansimp
ms.assetid: 1183b1bc-d4d7-4914-a049-06e82bf2d96d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4695d105c1aa6732efb6b8ed05169cf29e7f972b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814104"
---
# Развертывание баз данных App-V с помощью сценариев SQL

Чтобы использовать сценарии SQL, а не установщик Windows, выполните указанные ниже инструкции.

- Установка баз данных App-V 5,1
- Обновление баз данных App-V до более поздней версии

> [!NOTE]
> Если вы уже развернули базу данных App-V 5,0 с пакетом обновления 3 (SP3), то сценарии SQL не требуется обновлять до версии App-V 5,1.

## Установка баз данных App-V с помощью сценариев SQL

1. Прежде чем устанавливать сценарии базы данных, ознакомьтесь с условиями лицензионного соглашения App-V и сохраните их. Запустив сценарии базы данных, вы соглашаетесь с условиями лицензионного соглашения. Если вы не согласны, не используйте это программное обеспечение.
1. Скопируйте **appv\_server\_setup.exe** из среды выпуска App-V в временное расположение.
1. В командной строке запустите **appv\_server\_setup.exe** и укажите временное расположение для извлечения сценариев базы данных.

    Пример: appv\_server\_setup.exe/Layout c:\\ &lt; _Temporary Location (путь_ )&gt;

1. Перейдите к созданному временному расположению, откройте папку извлеченные **DatabaseScripts** и просмотрите инструкции в соответствующем файле Readme.txt.

    | База данных | Расположение используемого файла Readme.txt |
    |--|--|
    | База данных управления | Вложенная папка ManagementDatabase |
    | База данных отчетов | Вложенная папка ReportingDatabase |

> [!CAUTION]
> Файл readme.txt в подпапке ManagementDatabase устарел. Сведения в обновленных файлах readme ниже актуальны и должны заменяться сведениями о файлах readme, которые содержатся в папках **DatabaseScripts** .

> [!IMPORTANT]
> Сценарий InsertVersionInfo. SQL не требуется для версий базы данных управления App-V более поздней версии, чем App-V 5,0 с пакетом обновления 3 (SP3).

Сценарий Permissions. SQL должен обновляться в соответствии с **шагом 2** в [статье 3031340 базы знаний](https://support.microsoft.com/kb/3031340). **Шаг 1** не требуется для версий App-v, более поздних, чем App-v 5,0 SP3.

## Содержимое файла сведений о обновленной базе данных для управления

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************


Steps to install "AppVManagement" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
    Permissions.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the
    necessary SQL Server client software is installed and available from
    the specified location.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVManagement".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
##     in the file will not work.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. Run the following scripts against the "AppVManagement" database using the
    same account as above in order.

    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
##     Permissions.sql

```

## Обновленный контент файла сведений о базе данных отчетов

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************

Steps to install "AppVReporting" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    UpgradeDatabase.sql
    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
    ScheduleReportingJob.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the 
    necessary SQL Server client software is installed and executable from
    the location you have chosen.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVReporting".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
    in the file will not work.

 3. Review the ScheduleReportingJob.sql file and make sure that the stored proc schedule
    time is acceptable. The default stored proc schedule time is at 12.01 AM (line 84). 
    If this time is not suitable, you can change this to a more suitable time. The time is
##     in the format HHMMSS.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. If upgrading the database, run UpgradeDatabase.sql This will upgrade database schema.

 2. Run the following scripts against the "AppVReporting" database using the
    same account as above in order.

    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
##     ScheduleReportingJob.sql

```

**У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме

[Развертывание сервера App-V 5.1](deploying-the-app-v-51-server.md)

[Порядок развертывания сервера App-V 5.1](how-to-deploy-the-app-v-51-server.md)
