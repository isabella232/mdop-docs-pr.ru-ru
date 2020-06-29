---
title: Создание баз данных App-V 4.5 с помощью сценариев SQL
description: Создание баз данных App-V 4.5 с помощью сценариев SQL
author: dansimp
ms.assetid: 6cd0b180-163e-463f-a658-939ab9a7cfa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9ab2c102a43701bfdeaac49359b4ca3c4a063fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825979"
---
# <span data-ttu-id="c4bdf-103">Создание баз данных App-V 4.5 с помощью сценариев SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-103">Creating App-V 4.5 Databases Using SQL Scripting</span></span>


**<span data-ttu-id="c4bdf-104">Для кого предназначено это решение?</span><span class="sxs-lookup"><span data-stu-id="c4bdf-104">Who is this solution intended for?</span></span>** <span data-ttu-id="c4bdf-105">Специалисты по информационным технологиям, управляющие базами данных Application Virtualization (App-V) 4,5.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-105">Information technology professionals who manage Application Virtualization (App-V) 4.5 databases.</span></span>

**<span data-ttu-id="c4bdf-106">Как это руководство поможет вам?</span><span class="sxs-lookup"><span data-stu-id="c4bdf-106">How can this guide help you?</span></span>** <span data-ttu-id="c4bdf-107">Это решение описывает и документирует процедуры для установки сервера Application Virtualization, если администратор не имеет привилегий sysadmin для сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-107">This solution explains and documents the procedure to install the Microsoft Application Virtualization Server when the administrator installing does not have “sysadmin” privileges to the SQL Server.</span></span>

## <span data-ttu-id="c4bdf-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="c4bdf-108">Overview</span></span>


<span data-ttu-id="c4bdf-109">Одной из проблем, возникающих при установке Microsoft Application Virtualization 4,5 (App-V), является то, что пользователь, устанавливающий компоненты сервера, не только является администратором локального компьютера, но и обладает правами администратора SQL на сервере SQL Server, на котором будет размещено хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-109">One of the challenges of installing Microsoft Application Virtualization 4.5 (App-V) is that the install program assumes that the user installing the server features will not only be a local computer administrator, but also have SQL administrator privileges on the SQL server that will host the Data Store.</span></span> <span data-ttu-id="c4bdf-110">Это требование основано на том факте, что база данных, а также соответствующие роли и разрешения создаются как часть установки.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-110">This requirement is based on the fact that the database, as well as the appropriate roles and permissions, are created as part of the install.</span></span> <span data-ttu-id="c4bdf-111">Тем не менее, в большинстве организаций серверы SQL Server управляются отдельно от группы инфраструктуры, в которой будет устанавливаться приложение App-V.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-111">However, in most enterprises, SQL servers are managed separately from the infrastructure team who will be installing App-V.</span></span> <span data-ttu-id="c4bdf-112">Эти требования безопасности затрудняют получение администраторами SQL разрешений, необходимых для установки и предоставления администратором инфраструктуры. Аналогичным образом у администраторов SQL не будет разрешений, необходимых для установки продукта для группы инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-112">These security requirements will make it difficult to get SQL administrators to give the infrastructure administrator installing App-V adequate rights; similarly, the SQL administrators will not have the required privileges to install the product for the infrastructure team.</span></span>

<span data-ttu-id="c4bdf-113">В настоящее время у администратора, пытающегося установить приложение App-V, должны быть полномочия SQL "sysadmin".</span><span class="sxs-lookup"><span data-stu-id="c4bdf-113">Currently, an administrator attempting the installation of App-V must have SQL “sysadmin” privileges.</span></span> <span data-ttu-id="c4bdf-114">В предыдущих версиях продукта Настройка, разрешенная для администраторов SQL, может либо создать временную учетную запись системного администратора, либо присутствовать во время установки, чтобы предоставить учетные данные с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-114">In previous versions of the product the setup allowed for the SQL administrators to either create a temporary “sysadmin” account or be present during installation to provide credentials with “sysadmin” privileges.</span></span> <span data-ttu-id="c4bdf-115">В этом выпуске сценарии предоставляются в выпущенном продукте для всех администраторов, которые будут использоваться при реализации инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-115">In this release, scripts are provided in the released product for all administrators to use when implementing their infrastructure.</span></span>

<span data-ttu-id="c4bdf-116">В этом документе обсуждается сценарий, в котором установка должна быть разделена на две отдельных задачи: создание базы данных SQL и установка функций сервера App-V.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-116">This whitepaper discusses the scenario in which the install will need to be divided into two separate tasks: creating the SQL database, and installing the App-V server features.</span></span> <span data-ttu-id="c4bdf-117">Администраторы SQL могут просматривать сценарии SQL и вносить изменения для устранения конфликтов с другими базами данных или для поддержки интеграции с другими инструментами.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-117">The SQL administrators would be able to review the SQL scripts and make modifications to resolve any conflicts with other databases, or to support integration with other tools.</span></span> <span data-ttu-id="c4bdf-118">В результате сценариев можно разрешить администраторам SQL подготовить базу данных, чтобы администраторам инфраструктуры не придавались дополнительные права на доступ к SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-118">The result of the scripts is to allow SQL administrators to prepare the database so that the infrastructure administrators do not have to be granted any advanced rights on the SQL server.</span></span> <span data-ttu-id="c4bdf-119">Это важно в средах, в которых политики безопасности не будут блокироваться.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-119">This is important in environments where security policies would prohibit this.</span></span>

### <span data-ttu-id="c4bdf-120">Процесс создания базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-120">SQL Database Creation Process</span></span>

<span data-ttu-id="c4bdf-121">Скрипты SQL позволяют администраторам SQL создавать требуемую базу данных, а также настраивать разрешения для администраторов App-V для успешной установки и управления средой.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-121">The SQL scripts allow for SQL administrators to create the required database and also set up the privileges for the App-V administrators to successfully install and manage the environment.</span></span> <span data-ttu-id="c4bdf-122">Инструкции по выполнению этих задач описаны ниже в этом документе.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-122">The steps for completing these tasks are listed later in this document.</span></span>

<span data-ttu-id="c4bdf-123">Этот процесс разделяет действия по созданию базы данных и настройке из фактического экземпляра App-V.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-123">This process separates the database creation and configuration actions from the actual App-V installation.</span></span>

**<span data-ttu-id="c4bdf-124">Данные, которые необходимо предоставить администраторам SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-124">Information to be provided to SQL administrators</span></span>**

-   <span data-ttu-id="c4bdf-125">Имя группы рекламных объявлений, которая должна быть администратором App-V</span><span class="sxs-lookup"><span data-stu-id="c4bdf-125">Name of AD group that is going to be the App-V admin’s</span></span>

-   <span data-ttu-id="c4bdf-126">Имя сервера, на котором будет установлен сервер управления App-V</span><span class="sxs-lookup"><span data-stu-id="c4bdf-126">Name of the server where App-V Management Server will be installed</span></span>

**<span data-ttu-id="c4bdf-127">Информация, возвращаемая администраторам инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="c4bdf-127">Information to be returned to the Infrastructure administrators</span></span>**

-   <span data-ttu-id="c4bdf-128">Имя сервера или экземпляра базы данных, а также имя базы данных App-V.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-128">Name of the database server or instance and the name of the App-V database</span></span>

<span data-ttu-id="c4bdf-129">После подготовки базы данных Администраторы App-V смогут выполнить установку App-V без прав администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-129">Once the database has been prepared, the App-V administrators can run the App-V installation without SQL administrator privileges.</span></span>

### <span data-ttu-id="c4bdf-130">Использование сценариев настройки SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-130">Using the SQL Setup Scripts</span></span>

**<span data-ttu-id="c4bdf-131">Требования</span><span class="sxs-lookup"><span data-stu-id="c4bdf-131">Requirements</span></span>**

<span data-ttu-id="c4bdf-132">Ниже приведен список требований для использования сценариев, которые находятся в папке support\\createdb в корне выбранного расположения для извлечения.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-132">The following is a list of requirements for using the scripts which are located in the support\\createdb folder at the root of the selected extract location.</span></span>

-   <span data-ttu-id="c4bdf-133">Сценарии необходимо скопировать в расположении, доступном для записи, на компьютере, на котором они будут запускаться (не забудьте удалить атрибут "только для чтения", после того как они были скопированы), и на этом компьютере должны быть загружены инструменты SQL-клиента (osql — требуется только для запуска примеров пакетных файлов на локальном компьютере).</span><span class="sxs-lookup"><span data-stu-id="c4bdf-133">Scripts must be copied to a writeable location on the computer where they will be run (be sure to remove the read only attribute from these scripts after they have been copied) and SQL client tools must be loaded on that computer (osql is only required for running the sample batch files on the local computer).</span></span>

-   <span data-ttu-id="c4bdf-134">Сервер SQL Server должен поддерживать проверку подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-134">The SQL Server must support Windows Authentication.</span></span>

-   <span data-ttu-id="c4bdf-135">Убедитесь, что экземпляр SQL Server и служба агента SQL Server запущены.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-135">Ensure that the SQL Server Instance and SQL Agent Service are running.</span></span>

-   <span data-ttu-id="c4bdf-136">Войдите в систему с учетной записью домена, которая является администратором SQL (sysadmin) на компьютере, на котором будут выполняться сценарии.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-136">Log on with a domain account that is a SQL administrator (sysadmin) on the computer where the scripts will be done.</span></span>

<span data-ttu-id="c4bdf-137">Сценарии выполняются в учетных данных пользователя, вошедшего в систему.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-137">The scripts runs under the logged-on user’s domain credentials.</span></span>

**<span data-ttu-id="c4bdf-138">Создание базы данных с помощью сценариев SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-138">Database Creation Using SQL Scripts</span></span>**

**<span data-ttu-id="c4bdf-139">Задачи, которые должны выполняться администраторами SQL:</span><span class="sxs-lookup"><span data-stu-id="c4bdf-139">Tasks to be performed by SQL administrators:</span></span>**

1.  <span data-ttu-id="c4bdf-140">Скопируйте сценарии, содержащиеся в папке support\\createdb, из корня выбранного расположения для извлечения на компьютер, на котором будут выполняться сценарии.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-140">Copy the scripts contained in the support\\createdb folder from the root of the selected extract location to the computer where the scripts will be run.</span></span> <span data-ttu-id="c4bdf-141">Следующие файлы необходимы для правильной работы сценариев и должны вызываться в том порядке, в котором они представлены ниже.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-141">The following files are required for the scripts to run properly and must be called in the order presented below.</span></span>

    -   <span data-ttu-id="c4bdf-142">Database. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-142">database.sql</span></span>

    -   <span data-ttu-id="c4bdf-143">Roles. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-143">roles.sql</span></span>

    -   <span data-ttu-id="c4bdf-144">Таблица \ _CODES. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-144">table\_CODES.sql</span></span>

    -   <span data-ttu-id="c4bdf-145">функции \ _before \ _tables. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-145">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="c4bdf-146">Tables. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-146">tables.sql</span></span>

    -   <span data-ttu-id="c4bdf-147">функции. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-147">functions.sql</span></span>

    -   <span data-ttu-id="c4bdf-148">views. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-148">views.sql</span></span>

    -   <span data-ttu-id="c4bdf-149">процедуры. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-149">procedures.sql</span></span>

    -   <span data-ttu-id="c4bdf-150">triggers. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-150">triggers.sql</span></span>

    -   <span data-ttu-id="c4bdf-151">данные \ _codes. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-151">data\_codes.sql</span></span>

    -   <span data-ttu-id="c4bdf-152">данные \ _messages. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-152">data\_messages.sql</span></span>

    -   <span data-ttu-id="c4bdf-153">данные \ _defaults. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-153">data\_defaults.sql</span></span>

    -   <span data-ttu-id="c4bdf-154">Alerts \ _jobs. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-154">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="c4bdf-155">DBVersion. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-155">dbversion.sql</span></span>

2.  <span data-ttu-id="c4bdf-156">Просмотр и изменение файла в случае необходимости `database.sql` .</span><span class="sxs-lookup"><span data-stu-id="c4bdf-156">Review and modify, if necessary, the `database.sql` file.</span></span> <span data-ttu-id="c4bdf-157">Параметры по умолчанию будут присвоены имя базе данных "APPVIRTDB".</span><span class="sxs-lookup"><span data-stu-id="c4bdf-157">The default settings will name the database “APPVIRTDB.”</span></span>

    -   <span data-ttu-id="c4bdf-158">При необходимости замените экземпляры `APPVIRTDB` на `database name` , которые будут использоваться.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-158">If necessary replace instances of `APPVIRTDB` with the `database name` that will be used.</span></span>

    -   <span data-ttu-id="c4bdf-159">Измените `FILENAME` свойство в сценарии, указав соответствующий путь для сервера SQL Server, на котором будет создана база данных.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-159">Modify the `FILENAME` property in the script with the appropriate path for the SQL Server where the database will be created.</span></span>

3.  <span data-ttu-id="c4bdf-160">При необходимости проверьте и измените `database name [APPVIRTDB]` `roles.sql` файл в файле Database. SQL.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-160">Review and modify, if necessary, the `database name [APPVIRTDB]` in the `roles.sql` file that was used in the database.sql file.</span></span>

****

### <span data-ttu-id="c4bdf-161">Пример автоматизации процесса с помощью пакетных файлов</span><span class="sxs-lookup"><span data-stu-id="c4bdf-161">Example of how to automate the process using batch files</span></span>

<span data-ttu-id="c4bdf-162">При использовании из двух примеров пакетных файлов, указанных ниже, выполняются сценарии SQL следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c4bdf-162">If used, the two sample batch files provided run the SQL scripts in the following manner:</span></span>

1.  **<span data-ttu-id="c4bdf-163">Create\_schema.bat (1)</span><span class="sxs-lookup"><span data-stu-id="c4bdf-163">Create\_schema.bat (1)</span></span>**

    -   <span data-ttu-id="c4bdf-164">Database. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-164">database.sql</span></span>

    -   <span data-ttu-id="c4bdf-165">Roles. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-165">roles.sql</span></span>

2.  **<span data-ttu-id="c4bdf-166">Create\_tables.bat (2)</span><span class="sxs-lookup"><span data-stu-id="c4bdf-166">Create\_tables.bat (2)</span></span>**

    -   <span data-ttu-id="c4bdf-167">Таблица \ _CODES. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-167">table\_CODES.sql</span></span>

    -   <span data-ttu-id="c4bdf-168">функции \ _before \ _tables. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-168">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="c4bdf-169">Tables. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-169">tables.sql</span></span>

    -   <span data-ttu-id="c4bdf-170">функции. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-170">functions.sql</span></span>

    -   <span data-ttu-id="c4bdf-171">views. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-171">views.sql</span></span>

    -   <span data-ttu-id="c4bdf-172">процедуры. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-172">procedures.sql</span></span>

    -   <span data-ttu-id="c4bdf-173">triggers. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-173">triggers.sql</span></span>

    -   <span data-ttu-id="c4bdf-174">данные \ _codes. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-174">data\_codes.sql</span></span>

    -   <span data-ttu-id="c4bdf-175">данные \ _messages. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-175">data\_messages.sql</span></span>

    -   <span data-ttu-id="c4bdf-176">данные \ _defaults. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-176">data\_defaults.sql</span></span>

    -   <span data-ttu-id="c4bdf-177">Alerts \ _jobs. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-177">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="c4bdf-178">DBVersion. SQL</span><span class="sxs-lookup"><span data-stu-id="c4bdf-178">dbversion.sql</span></span>

**<span data-ttu-id="c4bdf-179">Примечание.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-179">Note</span></span>**  
<span data-ttu-id="c4bdf-180">Будьте внимательны при изменении сценариев и должны быть выполнены только кем-то, у кого есть соответствующие знания.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-180">Careful consideration when modifying the scripts must be taken and should only be done by someone with the appropriate knowledge.</span></span> <span data-ttu-id="c4bdf-181">Кроме того, в примерах файлов должны быть изменены только следующие: **create\_schema.bat**, **create\_tables.bat**, **Database. SQL**и **roles. SQL**.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-181">Also, of the sample files presented only the following should be changed: **create\_schema.bat**, **create\_tables.bat**, **database.sql**, and **roles.sql**.</span></span> <span data-ttu-id="c4bdf-182">Любые другие файлы не должны изменяться каким-либо образом, так как это может привести к тому, что база данных будет создана неправильно, что приводит к сбою установки служб App-V.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-182">All other files should not be modified in any way as this could cause the database to be created incorrectly, which will lead to the failure of App-V services to be installed.</span></span>



<span data-ttu-id="c4bdf-183">Два примера пакетных файлов должны располагаться в том же каталоге, где были скопированы остальные сценарии SQL на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-183">The two sample batch files must be placed in the same directory where the rest of the SQL scripts were copied to on the computer.</span></span>

1.  <span data-ttu-id="c4bdf-184">Запустите образец файла **create\_schema.bat** , чтобы создать базу данных.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-184">Run the sample **create\_schema.bat** file to create the database.</span></span> <span data-ttu-id="c4bdf-185">Выполнение сценария займет несколько секунд, и его не следует прерывать.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-185">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="c4bdf-186">Запустите файл CREATE schema.bat из каталога, в который он был скопирован.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-186">Run the create schema.bat file from the directory where it was copied to.</span></span> <span data-ttu-id="c4bdf-187">Синтаксис: "Create\_schema.bat `SQLSERVERNAME` "</span><span class="sxs-lookup"><span data-stu-id="c4bdf-187">Syntax is: “Create\_schema.bat `SQLSERVERNAME`”</span></span>

        ![AppV46SQLcreatebat](images/appv46sqlcreatebat.bmp)

    -   <span data-ttu-id="c4bdf-189">Если при создании новой базы данных "APPVIRTDB" происходит сбой сценария, проверьте журнал так, как указано, для устранения этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-189">If this script fails during the creation of the new “APPVIRTDB” database, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="c4bdf-190">Чтобы убедиться, что последующие попытки будут работать правильно, необходимо удалить базу данных, созданную с частичным запуском сценариев.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-190">It will be necessary to delete the database that was created with a partial running of the scripts in order to ensure that subsequent attempts will work properly.</span></span>

2.  <span data-ttu-id="c4bdf-191">Запустите `create_tables.bat` файл, чтобы создать таблицы в базе данных.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-191">Run the `create_tables.bat` file to create the tables in the database.</span></span> <span data-ttu-id="c4bdf-192">Выполнение сценария займет несколько секунд, и его не следует прерывать.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-192">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="c4bdf-193">Запустите файл create\_tables.bat из каталога, в который он был скопирован.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-193">Run the create\_tables.bat file from the directory where it was copied.</span></span> <span data-ttu-id="c4bdf-194">Синтаксис: "create\_tables.bat `SQLSERVERNAME DBNAME` "</span><span class="sxs-lookup"><span data-stu-id="c4bdf-194">Syntax is: “create\_tables.bat `SQLSERVERNAME DBNAME`”</span></span>

        ![create\-table.bat SQL App-v 4,6](images/appv46sqlcreate-tablebat.gif)

        <span data-ttu-id="c4bdf-196">Если при создании таблиц происходит сбой сценария, проверьте журнал так, как указано, для устранения этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-196">If the script fails during the creation of the tables, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="c4bdf-197">Перед запуском create\_tables.bat файла на всех последующих попытках потребуется удалить базу данных и выполнить create\_schema.bat.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-197">It will be necessary to delete the database and run create\_schema.bat before attempting to run the create\_tables.bat file on all subsequent attempts.</span></span>

### <span data-ttu-id="c4bdf-198">Настройка разрешений для базы данных App-V</span><span class="sxs-lookup"><span data-stu-id="c4bdf-198">Setting permissions on the App-V database</span></span>

<span data-ttu-id="c4bdf-199">Следующие учетные записи должны быть созданы на сервере SQL Server с определенными разрешениями и ролями в новой базе данных для установки, развертывания и текущего администрирования среды App-V.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-199">The following accounts will need to be created on the SQL server with specific permissions and roles to the new database for the installation, deployment and ongoing administration of the App-V environment.</span></span>

-   <span data-ttu-id="c4bdf-200">Создайте учетную запись для группы администраторов App-V на сервере SQL Server и в базе данных APPVIRTDB для "Администраторы domain\\App-V" (где "Domain" и "Administrators Administrators") будет изменена в соответствии с вашей средой и добавить их в роль "SFTAdmin" и "SFTEveryone".</span><span class="sxs-lookup"><span data-stu-id="c4bdf-200">Create a login for the App-V administrators group on the SQL Server and the APPVIRTDB database for the “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment) and add them to the SFTAdmin and SFTEveryone database role.</span></span>

    ![сценарий SQL App-v 4,6 Настройка разрешений и ролей](images/appv46sqlscriptsetpermsroles.gif)

-   <span data-ttu-id="c4bdf-202">Предоставьте этой группе разрешение VIEW ANY DEFINITION на глобальном уровне (это позволяет настроить сервер управления виртуализацией приложений (Майкрософт) для проверки того, что имя пользователя для входа на него уже существует).</span><span class="sxs-lookup"><span data-stu-id="c4bdf-202">Grant this group “VIEW ANY DEFINITION” permission at the global level (This allows the Microsoft Application Virtualization Management Server setup process to verify that the Management Server login already exists).</span></span> <span data-ttu-id="c4bdf-203">В разделе MS-SQL 2005 и более поздних ограничений на доступ к метаданным, содержащимся в Master. DB, были добавлены.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-203">Under MS-SQL 2005 and above access restrictions to the metadata contained in master.db were added.</span></span> <span data-ttu-id="c4bdf-204">Пользователь, созданный на предыдущем этапе, по умолчанию не имеет прав, необходимых для установки сервера.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-204">The user created in the previous step will by default not have the rights needed by the server installation.</span></span> <span data-ttu-id="c4bdf-205">Откройте свойства для ранее созданного имени для входа — &gt; защищаемые объекты.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-205">Open the properties of the previously created login, Login Properties-&gt;Securables.</span></span> <span data-ttu-id="c4bdf-206">Добавьте экземпляр базы данных и включите "GRANT" для представления Any View definition, как показано на снимке экрана ниже.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-206">Add the Database instance and enable “GRANT” for “View any definition” as shown in the screenshot below.</span></span>

    ![сценарий SQL App-v 4,6 Grant разрешение VIEW ANY DEF](images/appv46sqlscriptviewanydef.gif)

-   <span data-ttu-id="c4bdf-208">Добавьте роль в таблицу ROLE \ _ASSIGNMENTS для имени для входа, созданного на предыдущем шаге, чтобы предоставить администраторам App-V доступ к консоли управления виртуализации приложений, с ролью = "Администратор" и группой \ _ref = "domain\\App-V Administrators" (где "Domain" и "App-V Administrators") будет изменена в соответствии с вашей средой.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-208">Add a role to the ROLE\_ASSIGNMENTS table for the login created in the previous step to allow App-V administrators access to the Application Virtualization Management Console, with role = “ADMIN” and group\_ref = “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

    ![назначение роли сценария SQL App-v 4,6](images/appv46sqlscriptroleassign.gif)

-   <span data-ttu-id="c4bdf-210">Создание имени входа для SQL Server и базы данных App-V для сервера управления.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-210">Create login for SQL Server and App-V database for the Management Server.</span></span> <span data-ttu-id="c4bdf-211">Эта учетная запись используется сервером управления виртуализацией приложений Майкрософт для подключения к хранилищу данных и ответственен за обслуживание запросов клиентов для потоковых приложений.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-211">This account is used by the Microsoft Application Virtualization Management Server to connect to the data store and is responsible for servicing client requests for streamed applications.</span></span> <span data-ttu-id="c4bdf-212">В зависимости от того, где нужно установить SQL Server и сервер управления, существует два варианта:</span><span class="sxs-lookup"><span data-stu-id="c4bdf-212">There are two options, depending on where the SQL Server and Management Server are to be installed:</span></span>

    1.  <span data-ttu-id="c4bdf-213">Если сервер управления и SQL Server будут установлены на одном компьютере, добавьте имя входа для службы NT AUTHORITY\\NETWORK и добавьте его в роли базы данных SFTUser и SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-213">If Management Server and SQL Server are going to be installed on the same computer, add a login for NT AUTHORITY\\NETWORK SERVICE and add it to the SFTUser and SFTEveryone database roles.</span></span>

    2.  <span data-ttu-id="c4bdf-214">Если сервер управления и SQL Server должны быть установлены на разных компьютерах, добавьте имя для входа в учетную запись "domain\\App-V Server Name $" (где "App-V Server Name") — это имя сервера, на котором будет установлено сервер управления App-V, и добавьте его в роли базы данных SFTUser и SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-214">If the Management Server and SQL Server are to be installed on different computers, add a login for “domain\\App-V Server Name$” (where “App-V Server Name” is the name of the server where the App-V Management Server will be installed) and add it to the SFTUser and SFTEveryone database roles.</span></span>

-   <span data-ttu-id="c4bdf-215">Откройте окно запроса в окне SQL и выполните следующую команду SQL:</span><span class="sxs-lookup"><span data-stu-id="c4bdf-215">Open the query window on the SQL window and run the following SQL:</span></span>

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    <span data-ttu-id="c4bdf-216">Где APPVIRTDB — это имя базы данных App-V, созданной на сервере SQL Server на предыдущем этапе, и пользователь, который намеревается установить сервер App-v, должен быть членом группы "Администраторы domain\\App-V" (где "Domain" и "Администраторы App-V") будут изменены в соответствии с вашей средой.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-216">Where the APPVIRTDB is the name of the App-V Database created on the SQL Server in the previous step, and the user who is going to do the install of the App-v server needs to be a member of “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

### <span data-ttu-id="c4bdf-217">Задачи, которые должны выполняться администраторами инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="c4bdf-217">Tasks to be performed by the Infrastructure administrators</span></span>

1.  <span data-ttu-id="c4bdf-218">Администратор в группе "Администраторы App-V" должен установить App-V.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-218">Administrator in the “App-V Admins” group should install App-V.</span></span>

    <span data-ttu-id="c4bdf-219">Используйте сведения из администраторов SQL для выбора SQL Server и базы данных, созданной в предыдущих шагах.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-219">Use information from the SQL administrators for selecting the SQL Server and database created in the previous steps.</span></span>

2.  <span data-ttu-id="c4bdf-220">Администратор в группе "Администраторы App-V" входит в консоль управления виртуализацией приложений и удаляет следующие объекты из консоли управления.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-220">Administrator in the “App-V Admins” group logs in to Application Virtualization Management Console and deletes the following objects from the Management Console.</span></span>

    **<span data-ttu-id="c4bdf-221">Warning</span><span class="sxs-lookup"><span data-stu-id="c4bdf-221">Warning</span></span>**  
    <span data-ttu-id="c4bdf-222">Это необходимо, так как при использовании обычной настройки некоторые записи в базе данных будут заполнены, которые не заполнены при запуске установки для уже существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-222">This is required as the traditional setup populates certain records in the database that are not populated if you run the install against an already existing database.</span></span> <span data-ttu-id="c4bdf-223">Удалите следующие объекты:</span><span class="sxs-lookup"><span data-stu-id="c4bdf-223">Delete the following objects:</span></span>

    -   <span data-ttu-id="c4bdf-224">В разделе "группы серверов", "Группа серверов по умолчанию", "Удалить" сервер управления виртуализацией приложений "</span><span class="sxs-lookup"><span data-stu-id="c4bdf-224">Under “Server Groups,” “Default Server Group,” delete “Application Virtualization Management Server”</span></span>

    -   <span data-ttu-id="c4bdf-225">В разделе "группы серверов" Удалить "Группа сервера по умолчанию"</span><span class="sxs-lookup"><span data-stu-id="c4bdf-225">Under “Server Groups,” delete “Default Server Group”</span></span>

    -   <span data-ttu-id="c4bdf-226">В разделе "политики поставщика" удалите "поставщик по умолчанию"</span><span class="sxs-lookup"><span data-stu-id="c4bdf-226">Under “Provider Policies,” delete “Default Provider”</span></span>



3.  <span data-ttu-id="c4bdf-227">Администратор в группе "Администраторы" App-V должен создать:</span><span class="sxs-lookup"><span data-stu-id="c4bdf-227">Administrator in the App-V admins group should then create:</span></span>

    -   <span data-ttu-id="c4bdf-228">В разделе "политики поставщика" Создайте новую политику поставщика.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-228">Under “Provider Policies,” create a New Provider Policy</span></span>

    -   <span data-ttu-id="c4bdf-229">Создание группы серверов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c4bdf-229">Create a “Default Server Group”</span></span>

        **<span data-ttu-id="c4bdf-230">Примечание.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-230">Note</span></span>**  
        <span data-ttu-id="c4bdf-231">Вы должны создать группу "сервер по умолчанию", даже если вы не будете использовать ее.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-231">You must create a “Default Server” group even if you will not be used.</span></span> <span data-ttu-id="c4bdf-232">Установщик сервера ищет только "Группа серверов по умолчанию" при попытке добавить сервер.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-232">The server installer only looks for the "Default Server Group" when trying to add the server.</span></span>  <span data-ttu-id="c4bdf-233">Если "Группа сервера по умолчанию" отсутствует, установка завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-233">If there is no "Default Server Group" then the installation will fail.</span></span> <span data-ttu-id="c4bdf-234">Если вы планируете использовать серверные группы, отличные от используемых по умолчанию, необходимо сохранить "группу сервера по умолчанию", если вы планируете добавить последующие серверы управления App-V в инфраструктуру.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-234">If you plan on using server groups other than the default that is fine, it’s just necessary to retain the "Default Server Group" if you plan on adding subsequent App-V Management Servers to your infrastructure.</span></span>



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## <span data-ttu-id="c4bdf-235">Заключение</span><span class="sxs-lookup"><span data-stu-id="c4bdf-235">Conclusion</span></span>


<span data-ttu-id="c4bdf-236">В заключение информация в этом документе позволяет администратору работать с администраторами SQL для разработки пути развертывания, который подходит для обеспечения безопасности и администрирования разделов в Организации.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-236">In conclusion, the information in this document allows an administrator to work with the SQL administrators to develop a deployment path that works for the security and administrative divisions in an organization.</span></span> <span data-ttu-id="c4bdf-237">После прочтения документа и проверки описанных здесь задач администратор должен подготовиться к реализации инфраструктуры App-V в среде этого типа.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-237">After reading this document and testing the tasks documented, an administrator should be ready to implement their App-V infrastructure in this type of environment.</span></span>









