---
title: Установка и настройка MBAM на распределенных серверах
description: Установка и настройка MBAM на распределенных серверах
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825659"
---
# <span data-ttu-id="f7e2d-103">Установка и настройка MBAM на распределенных серверах</span><span class="sxs-lookup"><span data-stu-id="f7e2d-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="f7e2d-104">Процедуры, описанные в этом разделе, описывают полную установку функций администрирования и мониторинга Microsoft BitLocker (MBAM) на распределенных серверах.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on distributed servers.</span></span>

<span data-ttu-id="f7e2d-105">Каждый компонент сервера имеет определенные предварительные условия.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="f7e2d-106">Чтобы убедиться в том, что требования к оборудованию и программному обеспечению соблюдены, ознакомьтесь с требованиями к [развертыванию MBAM 1,0](mbam-10-deployment-prerequisites.md) и [MBAM 1,0 поддерживаемые конфигурации](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="f7e2d-106">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="f7e2d-107">Кроме того, для успешного развертывания компонента некоторым функциям потребуется предоставить определенные сведения в процессе установки.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-107">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span>

**<span data-ttu-id="f7e2d-108">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-108">Note</span></span>**  
<span data-ttu-id="f7e2d-109">Чтобы получить файлы журнала установки, необходимо установить MBAM с помощью пакета **msiexec** и параметра \*\*/l &lt; Location &gt; \*\* .</span><span class="sxs-lookup"><span data-stu-id="f7e2d-109">To obtain the setup log files, you have to install MBAM by using the **msiexec** package and the **/l &lt;location&gt;** option.</span></span> <span data-ttu-id="f7e2d-110">Файлы журнала создаются в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="f7e2d-111">Дополнительные файлы журнала установки создаются в папке% temp% пользователя, на котором выполняется установка MBAM.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-111">Additional setup log files are created in the %temp% folder of the user that runs the MBAM installation.</span></span>



## <a href="" id="deploy-the-mbam-server-features-"></a><span data-ttu-id="f7e2d-112">Развертывание функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="f7e2d-112">Deploy the MBAM Server features</span></span>


<span data-ttu-id="f7e2d-113">Ниже описаны действия, которые необходимо выполнить, чтобы установить общие функции MBAM.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-113">The following steps describe how to install the general MBAM features.</span></span>

**<span data-ttu-id="f7e2d-114">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-114">Note</span></span>**  
<span data-ttu-id="f7e2d-115">Убедитесь, что вы используете 32-разрядную настройку на 32-разрядных серверах и на 64-разрядной установке на 64-разрядных серверах.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-115">Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>



**<span data-ttu-id="f7e2d-116">Развертывание функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="f7e2d-116">To Deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="f7e2d-117">Запустите мастер установки MBAM и нажмите кнопку **установить** на странице приветствия.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-117">Start the MBAM installation wizard, and click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="f7e2d-118">Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="f7e2d-119">По умолчанию для установки выбраны все функции MBAM.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="f7e2d-120">Снимите флажки для компонентов, которые вы хотите установить на другом месте.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-120">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="f7e2d-121">Возможности, которые необходимо установить на одном и том же компьютере, должны быть установлены в любой момент.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-121">Features that you want to install on the same computer must be installed all at the same time.</span></span> <span data-ttu-id="f7e2d-122">Функции MBAM должны устанавливаться в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="f7e2d-122">MBAM features must be installed in the following order:</span></span>

    -   <span data-ttu-id="f7e2d-123">База данных восстановления и оборудования</span><span class="sxs-lookup"><span data-stu-id="f7e2d-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="f7e2d-124">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="f7e2d-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="f7e2d-125">Аудит соответствия требованиям и отчеты</span><span class="sxs-lookup"><span data-stu-id="f7e2d-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="f7e2d-126">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="f7e2d-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="f7e2d-127">Шаблон групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="f7e2d-127">MBAM Group Policy Template</span></span>

    **<span data-ttu-id="f7e2d-128">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-128">Note</span></span>**  
    <span data-ttu-id="f7e2d-129">Мастер установки проверяет предварительные требования для установки и выводит недостающие необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-129">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="f7e2d-130">Если все необходимые условия выполнены, установка будет продолжена.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-130">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="f7e2d-131">Если обнаружен отсутствующий предварительный компонент, необходимо устранить недостающие необходимые компоненты и нажать кнопку **проверить необходимые компоненты еще раз**.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-131">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="f7e2d-132">Если все необходимые условия выполнены, установка будет возобновлена.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-132">If all prerequisites are met this time, the installation will resume.</span></span>



4.  <span data-ttu-id="f7e2d-133">В мастере настройки MBAM будут отображены страницы установки для выбранных функций.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-133">The MBAM Setup wizard will display the installation pages for the selected features.</span></span> <span data-ttu-id="f7e2d-134">В следующих разделах описаны процедуры установки для каждой функции.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-134">The following sections describe the installation procedures for each feature.</span></span>

    **<span data-ttu-id="f7e2d-135">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-135">Note</span></span>**  
    <span data-ttu-id="f7e2d-136">Как правило, каждый компонент устанавливается на отдельном сервере.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-136">Typically, each feature is installed on a separate server.</span></span> <span data-ttu-id="f7e2d-137">Если вы хотите установить несколько функций на один сервер, вы можете изменить или устранить некоторые из описанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-137">If you want to install multiple features on a single server, you may change or eliminate some of the following steps.</span></span>



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   <span data-ttu-id="f7e2d-138">Укажите, следует ли использовать обновления Microsoft, чтобы обеспечить безопасность компьютера, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-138">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

6. <span data-ttu-id="f7e2d-139">После того как выбранные сведения о компоненте MBAM будут завершены, вы можете приступить к установке MBAM с помощью мастера настройки.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-139">When the selected MBAM feature information is complete, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="f7e2d-140">Чтобы проанализировать или изменить параметры установки, нажмите кнопку **назад** для перемещения по мастеру.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-140">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="f7e2d-141">Нажмите кнопку " **установить** ", чтобы начать установку.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-141">Click **Install** to begin the installation.</span></span> <span data-ttu-id="f7e2d-142">Нажмите кнопку **Отмена** , чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-142">Click **Cancel** to exit the Wizard.</span></span> <span data-ttu-id="f7e2d-143">При установке устанавливаются выбранные компоненты MBAM и уведомляются о том, что установка завершена.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-143">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

7. <span data-ttu-id="f7e2d-144">Нажмите кнопку **Готово** , чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-144">Click **Finish** to exit the wizard.</span></span>

8. <span data-ttu-id="f7e2d-145">После установки функций сервера MBAM вы можете добавлять пользователей к подходящим MBAM ролям.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-145">Add users to appropriate MBAM roles, after the MBAM server features are installed..</span></span> <span data-ttu-id="f7e2d-146">Дополнительные сведения можно найти в разделе [Планирование ролей администратора для MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f7e2d-146">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="f7e2d-147">Настройка после установки</span><span class="sxs-lookup"><span data-stu-id="f7e2d-147">Post-installation configuration</span></span>**

1.  <span data-ttu-id="f7e2d-148">После завершения настройки MBAM необходимо добавить роли пользователей, чтобы пользователи могли получать доступ к функциям на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-148">After MBAM Setup is finished, you must add user Roles before users can access to features in the MBAM administration website.</span></span> <span data-ttu-id="f7e2d-149">На сервере администрирования и мониторинга добавьте пользователей в следующие локальные группы.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-149">On the Administration and Monitoring Server, add users to the following local groups.</span></span>

    -   <span data-ttu-id="f7e2d-150">**Пользователи оборудования MBAM**: участники этой локальной группы могут получить доступ к компоненту "оборудование" на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-150">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="f7e2d-151">**Пользователи службы поддержки MBAM**: участники этой локальной группы могут получить доступ к восстановлению диска и управлять функциями доверенных платформенных модулей (TPM) на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-151">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage Trusted Platform Modules (TPM) features in the MBAM administration website.</span></span> <span data-ttu-id="f7e2d-152">Все поля в восстановлении диска и Управление TPM являются обязательными полями для пользователя службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-152">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="f7e2d-153">**MBAM опытных пользователей службы поддержки**: участники этой локальной группы имеют расширенный доступ к восстановлению диска и управляют функциями доверенного платформенного модуля на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-153">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="f7e2d-154">Для опытных пользователей службы поддержки требуется только поле "ИД ключа" в восстановлении диска.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-154">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="f7e2d-155">В разделе Управление доверенными платформенными модулями требуется только поле компьютера домена и имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-155">In Manage TPM, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="f7e2d-156">В базе данных "Администрирование", "соответствие" и "Аудит", а также на сервере, на котором размещаются отчеты о соответствии и аудите, добавьте пользователей в следующую локальную группу, чтобы предоставить им доступ к функции "отчеты" на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-156">On the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="f7e2d-157">**Пользователи отчетов MBAM**: участники этой локальной группы могут получать доступ к отчетам на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-157">**MBAM Report Users**: Members of this local group can access the Reports in the MBAM administration website.</span></span>

    **<span data-ttu-id="f7e2d-158">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-158">Note</span></span>**  
    <span data-ttu-id="f7e2d-159">Идентичные пользователи или члены группы в **отчете MBAM** локальная группа пользователей должны поддерживаться на всех компьютерах, на которых администрирование MBAM и наблюдение за базой данных функций сервера, соответствие требованиям и аудитом, а также отчеты о соответствии и аудите установлены.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-159">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="f7e2d-160">Проверка установки компонентов сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="f7e2d-160">Validate the MBAM Server feature installation</span></span>


<span data-ttu-id="f7e2d-161">После завершения установки компонента сервера MBAM вы должны убедиться, что установка успешно настроила все необходимые функции для MBAM.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-161">When the MBAM Server feature installation is complete, you should validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="f7e2d-162">Чтобы убедиться в том, что служба MBAM работает, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-162">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="f7e2d-163">Проверка установки MBAM</span><span class="sxs-lookup"><span data-stu-id="f7e2d-163">To validate an MBAM installation</span></span>**

1. <span data-ttu-id="f7e2d-164">На каждом сервере, где развернута функция MBAM, откройте **Панель управления**, нажмите кнопку **программы**и выберите пункт **программы и компоненты**.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-164">On each server, where an MBAM feature is deployed, open **Control Panel**, click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="f7e2d-165">Убедитесь в том, что в списке **программы и компоненты** отображается элемент **Администрирование и мониторинг Microsoft BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="f7e2d-165">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="f7e2d-166">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-166">Note</span></span>**  
   <span data-ttu-id="f7e2d-167">Для проверки установки MBAM необходимо использовать учетную запись домена, которая содержит учетные данные администратора локального компьютера на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-167">To validate the MBAM installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="f7e2d-168">На сервере, на котором установлена база данных восстановления и оборудования, откройте SQL Server Management Studio и убедитесь, что установлена **Восстановление MBAM и** база данных оборудования.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-168">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="f7e2d-169">На сервере, на котором установлена база данных соответствия и аудита, откройте центр администрирования SQL Server и убедитесь, что установлена база данных **состояния соответствия MBAM** .</span><span class="sxs-lookup"><span data-stu-id="f7e2d-169">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status** database is installed.</span></span>

4. <span data-ttu-id="f7e2d-170">На сервере, на котором установлены отчеты о соответствии и аудите, откройте веб-браузер с правами администратора и перейдите на веб-сайт служб SQL Server Reporting Services на домашнюю страницу.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-170">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="f7e2d-171">Расположение по умолчанию для экземпляра служб SQL Server Reporting Services можно найти на сайте http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-171">The default Home location of a SQL Server Reporting Services site instance can be found at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="f7e2d-172">Чтобы найти фактический URL-адрес, используйте Диспетчер конфигураций служб Reporting Services и выберите экземпляры, заданные во время настройки.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-172">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="f7e2d-173">Убедитесь в том, что в списке указана папка **Отчеты соответствие требованиям** , и что она содержит пять отчетов и один источник данных.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-173">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="f7e2d-174">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-174">Note</span></span>**  
   <span data-ttu-id="f7e2d-175">Если службы отчетов SQL Server были настроены как именованный экземпляр, URL-адрес должен выглядеть следующим образом: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="f7e2d-175">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



5. <span data-ttu-id="f7e2d-176">На сервере, на котором установлен компонент "Администрирование и наблюдение", запустите **Диспетчер серверов** и перейдите к пункту " **роли**", выберите **веб-сервер (IIS)**, а затем — **Диспетчер служб Internet Information Services (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-176">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span> <span data-ttu-id="f7e2d-177">В окне **подключения** перейдите на \* &lt; компьютер имя_компьютера &gt; \*, нажмите **сайты**, а затем — **Администрирование и мониторинг Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-177">In **Connections** browse to *&lt;computername&gt;*, click **Sites**, and click **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="f7e2d-178">Убедитесь в том, что указаны **MBAMAdministrationService**, **MBAMComplianceStatusService**и **MBAMRecoveryAndHardwareService** .</span><span class="sxs-lookup"><span data-stu-id="f7e2d-178">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

6. <span data-ttu-id="f7e2d-179">На сервере, на котором установлен компонент "Администрирование" и "наблюдение", откройте веб-браузер с правами администратора и перейдите по следующим адресам на веб-сайте MBAM, чтобы убедиться в том, что они успешно загружены.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-179">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges and browse to the following locations in the MBAM web site, to verify that they load successfully:</span></span>

   -   <span data-ttu-id="f7e2d-180">*http:// &lt; имя_компьютера &gt; /Default.aspx* и убедитесь в том, что все ссылки для навигации и отчетов</span><span class="sxs-lookup"><span data-stu-id="f7e2d-180">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="f7e2d-181">http:// &lt; имя_компьютера &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="f7e2d-181">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="f7e2d-182">http:// &lt; имя_компьютера &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="f7e2d-182">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="f7e2d-183">http:// &lt; имя_компьютера &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="f7e2d-183">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="f7e2d-184">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-184">Note</span></span>**  
   <span data-ttu-id="f7e2d-185">Обычно службы устанавливаются на порт по умолчанию 80 без сетевого шифрования.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-185">Typically, services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="f7e2d-186">Если службы установлены на другом порту, измените URL-адреса, чтобы включить соответствующий порт.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-186">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="f7e2d-187">Например, http://\* &lt; имя_компьютера &gt; : &lt; Port &gt; \*/Default.aspx или http:// <em> &lt; hostheadername &gt; / </em> Default. aspx</span><span class="sxs-lookup"><span data-stu-id="f7e2d-187">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx</span></span>

   <span data-ttu-id="f7e2d-188">Если службы были установлены с сетевым шифрованием, измените http://на https://.</span><span class="sxs-lookup"><span data-stu-id="f7e2d-188">If the services were installed with network encryption, change http:// to https://.</span></span>



~~~
Verify that each web page loads successfully.
~~~

## <span data-ttu-id="f7e2d-189">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f7e2d-189">Related topics</span></span>


[<span data-ttu-id="f7e2d-190">Развертывание инфраструктуры сервера MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="f7e2d-190">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)









