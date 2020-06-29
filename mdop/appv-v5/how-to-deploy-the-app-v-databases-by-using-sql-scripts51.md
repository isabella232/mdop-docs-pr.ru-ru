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
# <span data-ttu-id="2d008-103">Развертывание баз данных App-V с помощью сценариев SQL</span><span class="sxs-lookup"><span data-stu-id="2d008-103">How to Deploy the App-V Databases by Using SQL Scripts</span></span>

<span data-ttu-id="2d008-104">Чтобы использовать сценарии SQL, а не установщик Windows, выполните указанные ниже инструкции.</span><span class="sxs-lookup"><span data-stu-id="2d008-104">Use the following instructions to use SQL scripts, rather than the Windows Installer, to:</span></span>

- <span data-ttu-id="2d008-105">Установка баз данных App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="2d008-105">Install the App-V 5.1 databases</span></span>
- <span data-ttu-id="2d008-106">Обновление баз данных App-V до более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2d008-106">Upgrade the App-V databases to a later version</span></span>

> [!NOTE]
> <span data-ttu-id="2d008-107">Если вы уже развернули базу данных App-V 5,0 с пакетом обновления 3 (SP3), то сценарии SQL не требуется обновлять до версии App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="2d008-107">If you have already deployed the App-V 5.0 SP3 database, the SQL scripts are not required to upgrade to App-V 5.1.</span></span>

## <span data-ttu-id="2d008-108">Установка баз данных App-V с помощью сценариев SQL</span><span class="sxs-lookup"><span data-stu-id="2d008-108">How to install the App-V databases by using SQL scripts</span></span>

1. <span data-ttu-id="2d008-109">Прежде чем устанавливать сценарии базы данных, ознакомьтесь с условиями лицензионного соглашения App-V и сохраните их.</span><span class="sxs-lookup"><span data-stu-id="2d008-109">Before you install the database scripts, review and keep a copy of the App-V license terms.</span></span> <span data-ttu-id="2d008-110">Запустив сценарии базы данных, вы соглашаетесь с условиями лицензионного соглашения.</span><span class="sxs-lookup"><span data-stu-id="2d008-110">By running the database scripts, you are agreeing to the license terms.</span></span> <span data-ttu-id="2d008-111">Если вы не согласны, не используйте это программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="2d008-111">If you do not accept them, you should not use this software.</span></span>
1. <span data-ttu-id="2d008-112">Скопируйте **appv\_server\_setup.exe** из среды выпуска App-V в временное расположение.</span><span class="sxs-lookup"><span data-stu-id="2d008-112">Copy the **appv\_server\_setup.exe** from the App-V release media to a temporary location.</span></span>
1. <span data-ttu-id="2d008-113">В командной строке запустите **appv\_server\_setup.exe** и укажите временное расположение для извлечения сценариев базы данных.</span><span class="sxs-lookup"><span data-stu-id="2d008-113">From a command prompt, run **appv\_server\_setup.exe** and specify a temporary location for extracting the database scripts.</span></span>

    <span data-ttu-id="2d008-114">Пример: appv\_server\_setup.exe/Layout c:\\ &lt; _Temporary Location (путь_ )&gt;</span><span class="sxs-lookup"><span data-stu-id="2d008-114">Example: appv\_server\_setup.exe /layout c:\\&lt;_temporary location path_&gt;</span></span>

1. <span data-ttu-id="2d008-115">Перейдите к созданному временному расположению, откройте папку извлеченные **DatabaseScripts** и просмотрите инструкции в соответствующем файле Readme.txt.</span><span class="sxs-lookup"><span data-stu-id="2d008-115">Browse to the temporary location that you created, open the extracted **DatabaseScripts** folder, and review the appropriate Readme.txt file for instructions:</span></span>

    | <span data-ttu-id="2d008-116">База данных</span><span class="sxs-lookup"><span data-stu-id="2d008-116">Database</span></span> | <span data-ttu-id="2d008-117">Расположение используемого файла Readme.txt</span><span class="sxs-lookup"><span data-stu-id="2d008-117">Location of Readme.txt file to use</span></span> |
    |--|--|
    | <span data-ttu-id="2d008-118">База данных управления</span><span class="sxs-lookup"><span data-stu-id="2d008-118">Management database</span></span> | <span data-ttu-id="2d008-119">Вложенная папка ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="2d008-119">ManagementDatabase subfolder</span></span> |
    | <span data-ttu-id="2d008-120">База данных отчетов</span><span class="sxs-lookup"><span data-stu-id="2d008-120">Reporting database</span></span> | <span data-ttu-id="2d008-121">Вложенная папка ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="2d008-121">ReportingDatabase subfolder</span></span> |

> [!CAUTION]
> <span data-ttu-id="2d008-122">Файл readme.txt в подпапке ManagementDatabase устарел.</span><span class="sxs-lookup"><span data-stu-id="2d008-122">The readme.txt file in the ManagementDatabase subfolder is out of date.</span></span> <span data-ttu-id="2d008-123">Сведения в обновленных файлах readme ниже актуальны и должны заменяться сведениями о файлах readme, которые содержатся в папках **DatabaseScripts** .</span><span class="sxs-lookup"><span data-stu-id="2d008-123">The information in the updated readme files below is the most current and should supersede the readme information provided in the **DatabaseScripts** folders.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d008-124">Сценарий InsertVersionInfo. SQL не требуется для версий базы данных управления App-V более поздней версии, чем App-V 5,0 с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="2d008-124">The InsertVersionInfo.sql script is not required for versions of the App-V management database later than App-V 5.0 SP3.</span></span>

<span data-ttu-id="2d008-125">Сценарий Permissions. SQL должен обновляться в соответствии с **шагом 2** в [статье 3031340 базы знаний](https://support.microsoft.com/kb/3031340).</span><span class="sxs-lookup"><span data-stu-id="2d008-125">The Permissions.sql script should be updated according to **Step 2** in [KB article 3031340](https://support.microsoft.com/kb/3031340).</span></span> <span data-ttu-id="2d008-126">**Шаг 1** не требуется для версий App-v, более поздних, чем App-v 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="2d008-126">**Step 1** is not required for versions of App-V later than App-V 5.0 SP3.</span></span>

## <span data-ttu-id="2d008-127">Содержимое файла сведений о обновленной базе данных для управления</span><span class="sxs-lookup"><span data-stu-id="2d008-127">Updated management database README file content</span></span>

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

## <span data-ttu-id="2d008-128">Обновленный контент файла сведений о базе данных отчетов</span><span class="sxs-lookup"><span data-stu-id="2d008-128">Updated reporting database README file content</span></span>

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

**<span data-ttu-id="2d008-129">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="2d008-129">Got an App-V issue?</span></span>** <span data-ttu-id="2d008-130">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="2d008-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="2d008-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2d008-131">Related topics</span></span>

[<span data-ttu-id="2d008-132">Развертывание сервера App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2d008-132">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

[<span data-ttu-id="2d008-133">Порядок развертывания сервера App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2d008-133">How to Deploy the App-V 5.1 Server</span></span>](how-to-deploy-the-app-v-51-server.md)
