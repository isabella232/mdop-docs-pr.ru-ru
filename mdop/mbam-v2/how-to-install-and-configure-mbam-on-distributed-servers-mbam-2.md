---
title: Установка и настройка MBAM на распределенных серверах
description: Установка и настройка MBAM на распределенных серверах
author: dansimp
ms.assetid: 67b91e6b-ae2e-4e47-9ef2-6819aba95976
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 841b894430d14604f0fd923703708d7a3f588c07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824059"
---
# <span data-ttu-id="51ff7-103">Установка и настройка MBAM на распределенных серверах</span><span class="sxs-lookup"><span data-stu-id="51ff7-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="51ff7-104">В этой статье описано, как установить администрирование и мониторинг Microsoft BitLocker (MBAM) 2,0 в изолированной топологии на распределенных серверах.</span><span class="sxs-lookup"><span data-stu-id="51ff7-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in the Stand-alone topology on distributed servers.</span></span> <span data-ttu-id="51ff7-105">Чтобы просмотреть схему рекомендованной архитектуры, а также описание баз данных и функций, ознакомьтесь с [разворачиванием инфраструктуры сервера MBAM 2,0](deploying-the-mbam-20-server-infrastructure-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="51ff7-105">To see a diagram of the recommended architecture, along with a description of the databases and features, see [Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md).</span></span> <span data-ttu-id="51ff7-106">Сведения о том, как установить администрирование и мониторинг Microsoft BitLocker с помощью топологии Configuration Manager, можно найти в разделе [развертывание MBAM с помощью Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="51ff7-106">To install Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="51ff7-107">Каждый компонент сервера имеет определенные предварительные условия.</span><span class="sxs-lookup"><span data-stu-id="51ff7-107">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="51ff7-108">Чтобы убедиться в том, что требования к оборудованию и программному обеспечению соблюдены, ознакомьтесь с требованиями к [развертыванию MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) и [MBAM 2,0 поддерживаемые конфигурации](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="51ff7-108">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="51ff7-109">Кроме того, для успешного развертывания компонента некоторым функциям потребуется предоставить определенные сведения в процессе установки.</span><span class="sxs-lookup"><span data-stu-id="51ff7-109">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="51ff7-110">Кроме того, прежде чем приступить к развертыванию MBAM, вы также должны ознакомиться с [планированием развертывания сервера MBAM 2,0](planning-for-mbam-20-server-deployment-mbam-2.md) .</span><span class="sxs-lookup"><span data-stu-id="51ff7-110">You should also review [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md) before you start the MBAM deployment.</span></span>

**<span data-ttu-id="51ff7-111">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-111">Note</span></span>**  
<span data-ttu-id="51ff7-112">Чтобы получить файлы журнала установки, необходимо использовать пакет msiexec и параметр **/l** &lt; Location &gt; для установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-112">To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="51ff7-113">Файлы журнала создаются в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="51ff7-113">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="51ff7-114">Дополнительные файлы журнала установки создаются в папке% Temp% на сервере пользователя, устанавливающего MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-114">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <a href="" id="deploying-mbam-server-features-"></a><span data-ttu-id="51ff7-115">Развертывание функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="51ff7-115">Deploying MBAM Server Features</span></span>


<span data-ttu-id="51ff7-116">Ниже описаны действия, которые необходимо выполнить, чтобы установить общие функции MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-116">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="51ff7-117">Запуск мастера установки сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="51ff7-117">To start the MBAM Server installation wizard</span></span>**

1.  <span data-ttu-id="51ff7-118">На сервере, на котором вы хотите установить администрирование и мониторинг Microsoft BitLocker, запустите **MBAMSetup.exe** , чтобы запустить мастер установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-118">On the server where you want to install Microsoft BitLocker Administration and Monitoring, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="51ff7-119">На странице **приветствия** при необходимости выберите **программу улучшения качества программного**обеспечения, а затем нажмите кнопку **начать**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-119">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="51ff7-120">Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="51ff7-120">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="51ff7-121">На странице **Выбор топологии** выберите **изолированную** топологию и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-121">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

    **<span data-ttu-id="51ff7-122">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-122">Note</span></span>**  
    <span data-ttu-id="51ff7-123">Если вы хотите установить MBAM с топологией с интегрированной конфигурацией Configuration Manager, ознакомьтесь с разделом [развертывание MBAM с помощью Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="51ff7-123">If you want to install MBAM with the Configuration Manager integrated topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>



5.  <span data-ttu-id="51ff7-124">Выберите компоненты, которые вы хотите установить.</span><span class="sxs-lookup"><span data-stu-id="51ff7-124">Select the features that you want to install.</span></span> <span data-ttu-id="51ff7-125">По умолчанию для установки выбраны все функции MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-125">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="51ff7-126">Снимите флажки для компонентов, которые вы хотите установить на другом месте.</span><span class="sxs-lookup"><span data-stu-id="51ff7-126">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="51ff7-127">Функции, которые будут установлены на одном и том же компьютере, должны быть установлены одновременно.</span><span class="sxs-lookup"><span data-stu-id="51ff7-127">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="51ff7-128">Компоненты MBAM нужно устанавливать в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="51ff7-128">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="51ff7-129">База данных восстановления</span><span class="sxs-lookup"><span data-stu-id="51ff7-129">Recovery Database</span></span>

    -   <span data-ttu-id="51ff7-130">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="51ff7-130">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="51ff7-131">Отчеты о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="51ff7-131">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="51ff7-132">Портал самообслуживания</span><span class="sxs-lookup"><span data-stu-id="51ff7-132">Self-Service Portal</span></span>

    -   <span data-ttu-id="51ff7-133">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="51ff7-133">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="51ff7-134">Шаблон групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="51ff7-134">MBAM Group Policy template</span></span>

    **<span data-ttu-id="51ff7-135">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-135">Note</span></span>**  
    <span data-ttu-id="51ff7-136">Мастер установки проверяет предварительные требования для установки и выводит недостающие необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="51ff7-136">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="51ff7-137">Если все необходимые условия выполнены, установка будет продолжена.</span><span class="sxs-lookup"><span data-stu-id="51ff7-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="51ff7-138">Если обнаружен отсутствующий предварительный компонент, необходимо устранить недостающие необходимые компоненты и нажать кнопку **проверить необходимые компоненты еще раз**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="51ff7-139">Если все необходимые условия выполнены, установка возобновляется.</span><span class="sxs-lookup"><span data-stu-id="51ff7-139">If all prerequisites are met this time, the installation resumes.</span></span>



~~~
The MBAM Setup wizard displays installation pages for the features that you select. The following sections describe the installation procedures for each feature.

**Note**  
For the following instructions, it is assumed that each feature is to be installed on a separate server. If you install multiple features on a single server, you can change or eliminate some steps.
~~~



**<span data-ttu-id="51ff7-140">Установка базы данных восстановления</span><span class="sxs-lookup"><span data-stu-id="51ff7-140">To install the Recovery Database</span></span>**

1.  <span data-ttu-id="51ff7-141">На странице **Настройка базы данных восстановления** укажите имена компьютеров, на которых будет работать Сервер администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="51ff7-141">On the **Configure the Recovery database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="51ff7-142">После развертывания компонента администрирования и сервера мониторинга для подключения к базе данных используется учетная запись домена.</span><span class="sxs-lookup"><span data-stu-id="51ff7-142">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

2.  <span data-ttu-id="51ff7-143">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-143">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="51ff7-144">Укажите имя экземпляра SQL Server и имя базы данных, в которой будут храниться данные для восстановления.</span><span class="sxs-lookup"><span data-stu-id="51ff7-144">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="51ff7-145">Кроме того, необходимо указать, где будет находиться база данных и где будут храниться данные журнала.</span><span class="sxs-lookup"><span data-stu-id="51ff7-145">You must also specify both where the database will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="51ff7-146">Нажмите кнопку **Далее** , чтобы продолжить работу с мастером настройки MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-146">Click **Next** to continue with the MBAM Setup wizard.</span></span>

**<span data-ttu-id="51ff7-147">Установка базы данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="51ff7-147">To install the Compliance and Audit Database</span></span>**

1.  <span data-ttu-id="51ff7-148">На странице **Настройка базы данных соответствия и аудита** укажите учетную запись пользователя, которая будет использоваться для доступа к базе данных для отчетов.</span><span class="sxs-lookup"><span data-stu-id="51ff7-148">On the **Configure the Compliance and Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

2.  <span data-ttu-id="51ff7-149">Укажите имена компьютеров, на которых будет выполняться сервер администрирования и мониторинга, а также отчеты о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="51ff7-149">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Compliance and Audit Reports.</span></span> <span data-ttu-id="51ff7-150">После развертывания сервера администрирования и мониторинга, а также для подключения к базам данных используются учетные записи домена.</span><span class="sxs-lookup"><span data-stu-id="51ff7-150">After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they use their domain accounts to connect to the databases.</span></span>

    **<span data-ttu-id="51ff7-151">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-151">Note</span></span>**  
    <span data-ttu-id="51ff7-152">Если вы устанавливаете базу данных соответствия и аудита без функции "соответствие требованиям и аудиту", необходимо добавить исключение на компьютере с базой данных соответствия требованиям и аудита для включения входящего трафика на порт Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="51ff7-152">If you are installing the Compliance and Audit Database without the Compliance and Audit Reports feature, you must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="51ff7-153">Номер порта по умолчанию — 1433.</span><span class="sxs-lookup"><span data-stu-id="51ff7-153">The default port number is 1433.</span></span>



3.  <span data-ttu-id="51ff7-154">Укажите имя экземпляра SQL Server и имя базы данных, в котором будут храниться данные о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="51ff7-154">Specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="51ff7-155">Кроме того, необходимо указать, где будут храниться сведения о базе данных и журнале.</span><span class="sxs-lookup"><span data-stu-id="51ff7-155">You must also specify where the database and log information will be located.</span></span>

4.  <span data-ttu-id="51ff7-156">Нажмите кнопку **Далее** , чтобы продолжить работу с мастером настройки администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="51ff7-156">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="51ff7-157">Установка отчетов о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="51ff7-157">To install the Compliance and Audit Reports</span></span>**

1.  <span data-ttu-id="51ff7-158">На странице **Настройка отчетов о соответствии и аудите** укажите имя удаленного экземпляра SQL Server (например, &lt; ServerName &gt; ), в котором была установлена база данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="51ff7-158">On the **Configure the Compliance and Audit Reports** page, specify the remote SQL Server instance name (for example, &lt;ServerName&gt;) where the Compliance and Audit Database was installed.</span></span>

    **<span data-ttu-id="51ff7-159">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-159">Note</span></span>**  
    <span data-ttu-id="51ff7-160">Если вы устанавливаете отчеты о соответствии и аудите без сервера администрирования и мониторинга, необходимо добавить исключение на компьютере отчета о соответствии и аудите, чтобы включить входящий трафик на порт сервера отчетов (порт по умолчанию — 80).</span><span class="sxs-lookup"><span data-stu-id="51ff7-160">If you are installing the Compliance and Audit Reports without the Administration and Monitoring Server, you must add an exception on the Compliance and Audit Report computer to enable inbound traffic on the Reporting Server port (the default port is 80).</span></span>



2.  <span data-ttu-id="51ff7-161">Укажите имя базы данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="51ff7-161">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="51ff7-162">По умолчанию имя базы данных имеет состояние соответствия MBAM, но его можно изменить при установке базы данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="51ff7-162">By default, the database name is MBAM Compliance Status, although you can change the name when you install the Compliance and Audit Database.</span></span>

3.  <span data-ttu-id="51ff7-163">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-163">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="51ff7-164">Выберите экземпляр служб SQL Server Reporting Services, в котором будут установлены отчеты о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="51ff7-164">Select the instance of SQL Server Reporting Services where the Compliance and Audit Reports will be installed.</span></span> <span data-ttu-id="51ff7-165">Укажите учетную запись пользователя домена и пароль для доступа к базе данных "соответствие требованиям" и "Аудит".</span><span class="sxs-lookup"><span data-stu-id="51ff7-165">Provide a domain user account and password to access the Compliance and Audit Database.</span></span> <span data-ttu-id="51ff7-166">Настройка пароля для этой учетной записи бессрочна.</span><span class="sxs-lookup"><span data-stu-id="51ff7-166">Configure the password for this account to never expire.</span></span> <span data-ttu-id="51ff7-167">Учетная запись пользователя должна иметь доступ ко всем данным, доступным группе "Пользователи отчетов MBAM".</span><span class="sxs-lookup"><span data-stu-id="51ff7-167">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span>

5.  <span data-ttu-id="51ff7-168">Нажмите кнопку **Далее** , чтобы продолжить работу с мастером настройки администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="51ff7-168">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="51ff7-169">Установка портала самообслуживания</span><span class="sxs-lookup"><span data-stu-id="51ff7-169">To install the Self-Service Portal</span></span>**

1.  <span data-ttu-id="51ff7-170">На странице **Настройка портала самообслуживания** вы можете дополнительно зашифровать связь между порталом самообслуживания и серверами администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="51ff7-170">On the **Configure the Self-Service Portal** page, you can optionally encrypt the communication between the Self-Service Portal and the Administration and Monitoring servers.</span></span> <span data-ttu-id="51ff7-171">Если вы выбрали параметр для шифрования связи, вам будет предложено выбрать сертификат, подготовленный центром сертификации, для использования при шифровании.</span><span class="sxs-lookup"><span data-stu-id="51ff7-171">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2.  <span data-ttu-id="51ff7-172">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-172">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="51ff7-173">Укажите удаленный экземпляр SQL Server (например, \* &lt; ServerName &gt; \*), на котором была установлена база данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="51ff7-173">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4.  <span data-ttu-id="51ff7-174">Укажите имя базы данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="51ff7-174">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="51ff7-175">По умолчанию имя базы данных имеет состояние соответствия MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-175">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="51ff7-176">Однако вы можете изменить имя при установке базы данных "соответствие требованиям" и "Аудит".</span><span class="sxs-lookup"><span data-stu-id="51ff7-176">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5.  <span data-ttu-id="51ff7-177">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-177">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="51ff7-178">Укажите удаленный экземпляр SQL Server (например, \* &lt; ServerName &gt; \*), на котором была установлена база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="51ff7-178">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7.  <span data-ttu-id="51ff7-179">Укажите имя базы данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="51ff7-179">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="51ff7-180">По умолчанию имя базы данных **MBAM восстановлением и оборудованием**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-180">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="51ff7-181">Однако вы можете изменить имя при установке функции восстановления базы данных.</span><span class="sxs-lookup"><span data-stu-id="51ff7-181">However, you can change the name when you install the Recovery Database feature.</span></span>

8.  <span data-ttu-id="51ff7-182">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-182">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="51ff7-183">Введите **номер порта**, **имя узла** (необязательно) и **путь установки** для сервера администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-183">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="51ff7-184">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-184">Note</span></span>**  
    <span data-ttu-id="51ff7-185">Номер порта, который вы указали, должен быть неиспользуемым номеру на сервере администрирования и мониторинга, если не указано уникальное имя заголовка узла.</span><span class="sxs-lookup"><span data-stu-id="51ff7-185">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="51ff7-186">Если вы используете брандмауэр Windows, этот порт будет открыт автоматически.</span><span class="sxs-lookup"><span data-stu-id="51ff7-186">If you are using Windows Firewall, the port will be opened automatically.</span></span>



10. <span data-ttu-id="51ff7-187">Чтобы дополнительно зарегистрировать имя субъекта-службы (SPN) для портала самообслуживания, выберите пункт **зарегистрировать имена субъектов-служб (SPN) этого компьютера в Active Directory (требуется для проверки подлинности Windows)**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-187">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="51ff7-188">Если установить этот флажок, MBAM программа установки не будет пытаться зарегистрировать существующие SPN, и вы сможете вручную зарегистрировать SPN до или после установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-188">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="51ff7-189">Инструкции по регистрации имени участника-службы вручную можно найти в разделе [Регистрация SPN вручную](https://go.microsoft.com/fwlink/?LinkId=286758).</span><span class="sxs-lookup"><span data-stu-id="51ff7-189">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

11. <span data-ttu-id="51ff7-190">Нажмите кнопку **Далее** , чтобы продолжить работу с мастером настройки администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="51ff7-190">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

12. <span data-ttu-id="51ff7-191">Укажите, следует ли использовать обновления Microsoft, чтобы обеспечить безопасность компьютера, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-191">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

13. <span data-ttu-id="51ff7-192">После того как выбранные сведения о компоненте MBAM будут завершены, вы можете приступить к установке MBAM с помощью мастера настройки.</span><span class="sxs-lookup"><span data-stu-id="51ff7-192">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="51ff7-193">Чтобы проанализировать или изменить параметры установки, нажмите кнопку **назад** для перемещения по мастеру.</span><span class="sxs-lookup"><span data-stu-id="51ff7-193">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="51ff7-194">Нажмите кнопку " **установить** ", чтобы начать установку.</span><span class="sxs-lookup"><span data-stu-id="51ff7-194">Click **Install** to start the installation.</span></span> <span data-ttu-id="51ff7-195">Нажмите кнопку **Отмена** , чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="51ff7-195">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="51ff7-196">При установке устанавливаются выбранные компоненты MBAM и уведомляются о том, что установка завершена.</span><span class="sxs-lookup"><span data-stu-id="51ff7-196">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

14. <span data-ttu-id="51ff7-197">Нажмите кнопку **Готово** , чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="51ff7-197">Click **Finish** to exit the wizard.</span></span>

    **<span data-ttu-id="51ff7-198">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-198">Note</span></span>**  
    <span data-ttu-id="51ff7-199">Чтобы настроить портал самообслуживания после установки, назовите портал самообслуживания с названием вашей компании и другими сведениями о компании, чтобы узнать, [как фирменный портал для самостоятельного обслуживания](how-to-brand-the-self-service-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="51ff7-199">To configure the Self-Service Portal after you installed it, brand the Self-Service Portal with your company name and other company-specific information, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md) for instructions.</span></span>



15. <span data-ttu-id="51ff7-200">Если клиентские компьютеры имеют доступ к сети доставки содержимого (CDN), который предоставляет порталу самообслуживания необходимый доступ к определенным файлам JavaScript, вы закончите установку портала самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="51ff7-200">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, you are finished with the Self-Service Portal installation.</span></span> <span data-ttu-id="51ff7-201">Если клиентские компьютеры не имеют доступа к сети CDN (Microsoft), выполните действия, описанные в следующем разделе, чтобы настроить портал самообслуживания для ссылок на файлы JavaScript из доступного источника.</span><span class="sxs-lookup"><span data-stu-id="51ff7-201">If the client computers does not have access to the Microsoft CDN, complete the steps in the next section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

**<span data-ttu-id="51ff7-202">Настройка портала самообслуживания, когда конечные пользователи не могут получить доступ к сети доставки содержимого Майкрософт</span><span class="sxs-lookup"><span data-stu-id="51ff7-202">To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network</span></span>**

1. <span data-ttu-id="51ff7-203">Если клиентские компьютеры имеют доступ к сети доставки содержимого (CDN), который предоставляет порталу самообслуживания необходимый доступ к определенным файлам JavaScript, установка портала самообслуживания завершена.</span><span class="sxs-lookup"><span data-stu-id="51ff7-203">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, the Self-Service Portal installation is completed.</span></span> <span data-ttu-id="51ff7-204">Если клиентские компьютеры не имеют доступа к сети CDN (Microsoft), выполните оставшиеся действия, описанные в этом разделе, чтобы настроить портал самообслуживания для ссылок на файлы JavaScript из доступного источника.</span><span class="sxs-lookup"><span data-stu-id="51ff7-204">If the client computers do not have access to the Microsoft CDN, complete the remaining steps in this section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

2. <span data-ttu-id="51ff7-205">Скачайте четыре файла JavaScript из Microsoft CDN:</span><span class="sxs-lookup"><span data-stu-id="51ff7-205">Download the four JavaScript files from the Microsoft CDN:</span></span>

   -   <span data-ttu-id="51ff7-206">jQuery-1.7.2.min.js[https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span><span class="sxs-lookup"><span data-stu-id="51ff7-206">jQuery-1.7.2.min.js - [https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span></span>

   -   <span data-ttu-id="51ff7-207">MicrosoftAjax.js —[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span><span class="sxs-lookup"><span data-stu-id="51ff7-207">MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span></span>

   -   <span data-ttu-id="51ff7-208">MicrosoftMvcAjax.js[https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span><span class="sxs-lookup"><span data-stu-id="51ff7-208">MicrosoftMvcAjax.js - [https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span></span>

   -   <span data-ttu-id="51ff7-209">MicrosoftMvcValidation.js</span><span class="sxs-lookup"><span data-stu-id="51ff7-209">MicrosoftMvcValidation.js -</span></span> <https://go.microsoft.com/fwlink/p/?LinkId=272285>

3. <span data-ttu-id="51ff7-210">Скопируйте файлы JavaScript в каталог **Scripts** на портале самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="51ff7-210">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="51ff7-211">Этот каталог находится в службе самообслуживания <em> &lt; MBAM в каталогах самостоятельной установки &gt; \\ </em> Website\\Scripts.</span><span class="sxs-lookup"><span data-stu-id="51ff7-211">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

4. <span data-ttu-id="51ff7-212">Откройте **Диспетчер информационных служб Интернета (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-212">Open **Internet Information Services (IIS) Manager**.</span></span>

5. <span data-ttu-id="51ff7-213">Разверните **сайты** &gt; **Администрирование и мониторинг Microsoft BitLocker**и выберите **Selfservice**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-213">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="51ff7-214">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-214">Note</span></span>**  
   <span data-ttu-id="51ff7-215">*Selfservice* — имя виртуального каталога по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51ff7-215">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="51ff7-216">Если во время установки вы выбрали другое имя для этого каталога, не забудьте заменить *Selfservice* в остальных инструкциях на выбранное вами имя.</span><span class="sxs-lookup"><span data-stu-id="51ff7-216">If you chose a different name for this directory during installation, remember to replace *SelfService* in the rest of these instructions with the name you chose.</span></span>



6. <span data-ttu-id="51ff7-217">В средней области дважды щелкните **Параметры приложения**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-217">In the middle pane, double-click **Application Settings**.</span></span>

7. <span data-ttu-id="51ff7-218">Для каждого элемента в списке ниже измените параметры приложения, чтобы они ссылались на новое расположение, заменив &lt; виртуальный каталог на &gt; /Selfservice/(или имя, которое вы выбрали при установке).</span><span class="sxs-lookup"><span data-stu-id="51ff7-218">For each item in the following list, edit the application settings to reference the new location by replacing &lt;virtual directory&gt; with /SelfService/ (or the name you chose during installation).</span></span> <span data-ttu-id="51ff7-219">Например, путь к виртуальному каталогу будет похож на/Selfservice/Scripts/jquery-1.7.2.min.js.</span><span class="sxs-lookup"><span data-stu-id="51ff7-219">For example, the virtual directory path will be similar to /selfservice/scripts/jquery-1.7.2.min.js.</span></span>

   -   <span data-ttu-id="51ff7-220">jQueryPath:/ &lt; Virtual Directory &gt; /Scripts/jQuery-1.7.2.min.js</span><span class="sxs-lookup"><span data-stu-id="51ff7-220">jQueryPath: /&lt;virtual directory&gt;/Scripts/ jQuery-1.7.2.min.js</span></span>

   -   <span data-ttu-id="51ff7-221">MicrosoftAjaxPath:/ &lt; Virtual Directory &gt; /Scripts/MicrosoftAjax.js</span><span class="sxs-lookup"><span data-stu-id="51ff7-221">MicrosoftAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftAjax.js</span></span>

   -   <span data-ttu-id="51ff7-222">MicrosoftMvcAjaxPath:/ &lt; Virtual Directory &gt; /Scripts/MicrosoftMvcAjax.js</span><span class="sxs-lookup"><span data-stu-id="51ff7-222">MicrosoftMvcAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcAjax.js</span></span>

   -   <span data-ttu-id="51ff7-223">MicrosoftMvcValidationPath:/ &lt; Virtual Directory &gt; /Scripts/MicrosoftMvcValidation.js</span><span class="sxs-lookup"><span data-stu-id="51ff7-223">MicrosoftMvcValidationPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcValidation.js</span></span>

**<span data-ttu-id="51ff7-224">Установка компонента сервера администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="51ff7-224">To install the Administration and Monitoring Server feature</span></span>**

1. <span data-ttu-id="51ff7-225">MBAM может шифровать связь между веб-службами и серверами администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="51ff7-225">MBAM can encrypt the communication between the Web Services and the Administration and Monitoring servers.</span></span> <span data-ttu-id="51ff7-226">Если вы выбрали параметр для шифрования связи, вам будет предложено выбрать сертификат, подготовленный центром сертификации, для использования при шифровании.</span><span class="sxs-lookup"><span data-stu-id="51ff7-226">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2. <span data-ttu-id="51ff7-227">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-227">Click **Next** to continue.</span></span>

3. <span data-ttu-id="51ff7-228">Укажите удаленный экземпляр SQL Server (например: \* &lt; ServerName &gt; \*), на котором установлена база данных соответствия и аудита.</span><span class="sxs-lookup"><span data-stu-id="51ff7-228">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4. <span data-ttu-id="51ff7-229">Укажите имя базы данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="51ff7-229">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="51ff7-230">По умолчанию имя базы данных имеет состояние соответствия MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-230">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="51ff7-231">Однако вы можете изменить имя при установке базы данных "соответствие требованиям" и "Аудит".</span><span class="sxs-lookup"><span data-stu-id="51ff7-231">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5. <span data-ttu-id="51ff7-232">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-232">Click **Next** to continue.</span></span>

6. <span data-ttu-id="51ff7-233">Укажите удаленный экземпляр SQL Server (например, \* &lt; ServerName &gt; \*), на котором была установлена база данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="51ff7-233">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7. <span data-ttu-id="51ff7-234">Укажите имя базы данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="51ff7-234">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="51ff7-235">По умолчанию имя базы данных **MBAM восстановлением и оборудованием**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-235">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="51ff7-236">Однако вы можете изменить имя при установке функции восстановления базы данных.</span><span class="sxs-lookup"><span data-stu-id="51ff7-236">However, you can change the name when you install the Recovery Database feature.</span></span>

8. <span data-ttu-id="51ff7-237">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-237">Click **Next** to continue.</span></span>

9. <span data-ttu-id="51ff7-238">Укажите URL-адрес сайта служб SQL Server Reporting Services (SRS) для домашнего использования.</span><span class="sxs-lookup"><span data-stu-id="51ff7-238">Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site.</span></span> <span data-ttu-id="51ff7-239">Расположение по умолчанию для экземпляра сервера служб SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="51ff7-239">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

   <span data-ttu-id="51ff7-240">http:// <em> &lt; NameofMBAMReportsServer &gt; / </em> ReportServer</span><span class="sxs-lookup"><span data-stu-id="51ff7-240">http://<em>&lt;NameofMBAMReportsServer&gt;/</em>ReportServer</span></span>

   **<span data-ttu-id="51ff7-241">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-241">Note</span></span>**  
   <span data-ttu-id="51ff7-242">Если службы отчетов SQL Server были настроены как именованный экземпляр, URL-адрес напоминает следующее: http://\* &lt; NameofMBAMReportsServer &gt; */ReportServer\_* &lt; SRSInstanceName &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="51ff7-242">If SQL Server Reporting Services was configured as a named instance, the URL resembles the following: http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*.</span></span>



10. <span data-ttu-id="51ff7-243">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-243">Click **Next** to continue.</span></span>

11. <span data-ttu-id="51ff7-244">Введите **номер порта**, **имя узла** (необязательно) и **путь установки** для сервера администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-244">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="51ff7-245">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-245">Note</span></span>**  
    <span data-ttu-id="51ff7-246">Номер порта, который вы указали, должен быть неиспользуемым номеру на сервере администрирования и мониторинга, если не указано уникальное имя заголовка узла.</span><span class="sxs-lookup"><span data-stu-id="51ff7-246">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="51ff7-247">Если вы используете брандмауэр Windows, этот порт будет открыт автоматически.</span><span class="sxs-lookup"><span data-stu-id="51ff7-247">If you are using Windows Firewall, the port will be opened automatically.</span></span>



12. <span data-ttu-id="51ff7-248">Чтобы дополнительно зарегистрировать имя субъекта-службы (SPN) для портала самообслуживания, выберите пункт **зарегистрировать имена субъектов-служб (SPN) этого компьютера в Active Directory (требуется для проверки подлинности Windows)**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-248">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="51ff7-249">Если установить этот флажок, MBAM программа установки не будет пытаться зарегистрировать существующие SPN, и вы сможете вручную зарегистрировать SPN до или после установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-249">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="51ff7-250">Инструкции по регистрации имени участника-службы вручную можно найти в разделе [Регистрация SPN вручную](https://go.microsoft.com/fwlink/?LinkId=286758).</span><span class="sxs-lookup"><span data-stu-id="51ff7-250">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

13. <span data-ttu-id="51ff7-251">Нажмите кнопку **Далее** , чтобы продолжить работу с мастером настройки администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="51ff7-251">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

14. <span data-ttu-id="51ff7-252">Укажите, следует ли использовать обновления Microsoft, чтобы обеспечить безопасность компьютера, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-252">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

15. <span data-ttu-id="51ff7-253">После того как выбранные сведения о компоненте MBAM будут завершены, вы можете приступить к установке MBAM с помощью мастера настройки.</span><span class="sxs-lookup"><span data-stu-id="51ff7-253">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="51ff7-254">Чтобы проанализировать или изменить параметры установки, нажмите кнопку **назад** для перемещения по мастеру.</span><span class="sxs-lookup"><span data-stu-id="51ff7-254">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="51ff7-255">Нажмите кнопку **установить** , чтобы выполнить установку.</span><span class="sxs-lookup"><span data-stu-id="51ff7-255">Click **Install** to being the installation.</span></span> <span data-ttu-id="51ff7-256">Нажмите кнопку **Отмена** , чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="51ff7-256">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="51ff7-257">При установке устанавливаются выбранные компоненты MBAM и уведомляются о том, что установка завершена.</span><span class="sxs-lookup"><span data-stu-id="51ff7-257">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

16. <span data-ttu-id="51ff7-258">Нажмите кнопку **Готово** , чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="51ff7-258">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="51ff7-259">Чтобы выполнить настройку после установки, выполните описанные выше действия.</span><span class="sxs-lookup"><span data-stu-id="51ff7-259">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="51ff7-260">На сервере администрирования и мониторинга добавьте пользователей в следующие локальные группы, чтобы предоставить им доступ к функциям на веб-сайте администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-260">On the Administration and Monitoring Server, add users to the following local groups to give them access to the features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="51ff7-261">**Пользователи службы поддержки MBAM**: участники этой локальной группы могут получить доступ к восстановлению диска и управлять функциями TPM на веб-сайте администрирования MBAM и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="51ff7-261">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="51ff7-262">Все поля в восстановлении диска и Управление TPM являются обязательными полями для пользователя службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="51ff7-262">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="51ff7-263">**MBAM для опытных пользователей службы поддержки**: участники этой локальной группы имеют расширенный доступ к восстановлению диска и управляют функциями доверенного платформенного модуля на веб-сайте администрирования MBAM и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="51ff7-263">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="51ff7-264">Для опытных пользователей службы поддержки требуется только поле "ИД ключа" в восстановлении диска.</span><span class="sxs-lookup"><span data-stu-id="51ff7-264">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="51ff7-265">В разделе **Управление доверенными платформенными модулями**требуется только поле **компьютера домена** и **имя компьютера** .</span><span class="sxs-lookup"><span data-stu-id="51ff7-265">In **Manage TPM**, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="51ff7-266">Добавьте пользователей в следующую локальную группу на сервере, на котором размещается сервер администрирования и наблюдения и база данных соответствия и аудита, а также на сервере, на котором размещаются отчеты о соответствии и аудите, чтобы предоставить им доступ к функции "отчеты" на веб-сайте администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-266">On the server that hosts Administration and Monitoring Server and the Compliance and Audit Database and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="51ff7-267">**Пользователи отчетов MBAM**: участники этой локальной группы могут получать доступ к отчетам на веб-сайте администрирования MBAM и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="51ff7-267">**MBAM Report Users**: Members of this local group can access the reports on the MBAM Administration and Monitoring website.</span></span>

    **<span data-ttu-id="51ff7-268">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-268">Note</span></span>**  
    <span data-ttu-id="51ff7-269">Идентичные пользователи или члены группы в **отчете MBAM** локальная группа пользователей должны поддерживаться на всех компьютерах, на которых администрирование MBAM и наблюдение за базой данных функций сервера, соответствие требованиям и аудитом, а также отчеты о соответствии и аудите установлены.</span><span class="sxs-lookup"><span data-stu-id="51ff7-269">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="51ff7-270">Проверка установки компонентов сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="51ff7-270">Validating the MBAM Server Feature Installation</span></span>


<span data-ttu-id="51ff7-271">После завершения установки компонентов сервера администрирования и мониторинга Microsoft BitLocker рекомендуется проверить, успешно ли установлены все необходимые функции для MBAM.</span><span class="sxs-lookup"><span data-stu-id="51ff7-271">When Microsoft BitLocker Administration and Monitoring Server feature installation is completed, we recommend that you validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="51ff7-272">Чтобы убедиться в том, что служба администрирования и наблюдения Microsoft BitLocker работает, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="51ff7-272">Use the following procedure to confirm that the Microsoft BitLocker Administration and Monitoring service is functional.</span></span>

**<span data-ttu-id="51ff7-273">Проверка установки сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="51ff7-273">To validate an MBAM Server installation</span></span>**

1. <span data-ttu-id="51ff7-274">На каждом сервере, на котором развернута функция MBAM, откройте **Панель управления**, выберите " **программы**", а затем выберите " **программы и компоненты**".</span><span class="sxs-lookup"><span data-stu-id="51ff7-274">On each server where an MBAM feature is deployed, open **Control Panel**, select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="51ff7-275">Убедитесь в том, что в списке **программы и компоненты** отображается элемент **Администрирование и мониторинг Microsoft BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="51ff7-275">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="51ff7-276">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-276">Note</span></span>**  
   <span data-ttu-id="51ff7-277">Для проверки установки MBAM необходимо использовать учетную запись домена, которая содержит учетные данные администратора локального компьютера на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="51ff7-277">To validate the MBAM installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="51ff7-278">На сервере с установленной базой данных восстановления откройте SQL Server Management Studio и убедитесь, что установлена **Восстановление MBAM и** база данных оборудования.</span><span class="sxs-lookup"><span data-stu-id="51ff7-278">On the server where the Recovery Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="51ff7-279">На сервере, на котором установлена база данных соответствия и аудита, откройте центр администрирования SQL Server и убедитесь, что установлена **база данных состояния соответствия MBAM** .</span><span class="sxs-lookup"><span data-stu-id="51ff7-279">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="51ff7-280">На сервере, на котором установлены отчеты о соответствии и аудите, откройте веб-браузер с учетными данными администратора и перейдите на сайт "Главная" сайта служб SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="51ff7-280">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="51ff7-281">Расположение по умолчанию для сайта служб SQL Server Reporting Services можно найти на сайте http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx.</span><span class="sxs-lookup"><span data-stu-id="51ff7-281">The default Home location of a SQL Server Reporting Services site instance can be found is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="51ff7-282">Чтобы найти фактический URL-адрес, используйте диспетчер конфигурации служб Reporting Services и выберите экземпляры, заданные во время настройки.</span><span class="sxs-lookup"><span data-stu-id="51ff7-282">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that were specified during setup.</span></span>

   <span data-ttu-id="51ff7-283">Убедитесь в том, что в папке Reporting ( **Администрирование и мониторинг) Microsoft BitLocker** есть источник данных **MaltaDataSource** и что в папке **en-US** есть четыре отчета.</span><span class="sxs-lookup"><span data-stu-id="51ff7-283">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="51ff7-284">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-284">Note</span></span>**  
   <span data-ttu-id="51ff7-285">Если службы отчетов SQL Server были настроены как именованный экземпляр, URL-адрес должен выглядеть следующим образом: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="51ff7-285">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="51ff7-286">На сервере, на котором установлен компонент "Администрирование и наблюдение", запустите **Диспетчер серверов** и перейдите к **ролям**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-286">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="51ff7-287">Выберите **веб-сервер (IIS)**, а затем — **Диспетчер служб Internet Information Services (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-287">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span>

6. <span data-ttu-id="51ff7-288">В окне " **подключения**" перейдите на сайт \* &lt; ComputerName &gt; \*, выберите **сайты**и выберите пункт **Администрирование и мониторинг Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="51ff7-288">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="51ff7-289">Убедитесь в том, что указаны **MBAMAdministrationService**, **MBAMComplianceStatusService**и **MBAMRecoveryAndHardwareService** .</span><span class="sxs-lookup"><span data-stu-id="51ff7-289">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="51ff7-290">На сервере, на котором установлены функции администрирования и наблюдения и портал самообслуживания, откройте веб-браузер с учетными данными администратора и перейдите к следующим расположениям, чтобы убедиться, что они успешно загружены.</span><span class="sxs-lookup"><span data-stu-id="51ff7-290">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully.</span></span>

   **<span data-ttu-id="51ff7-291">Примечание.</span><span class="sxs-lookup"><span data-stu-id="51ff7-291">Note</span></span>**  
   <span data-ttu-id="51ff7-292">URL-адреса, заканчивающиеся на SVC, не отображаются на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="51ff7-292">The URLs ending in “.svc” do not display a website.</span></span> <span data-ttu-id="51ff7-293">Сообщение "успех" указан в сообщении "Публикация метаданных для этой службы сейчас отключена" или с помощью кода похожих на код.</span><span class="sxs-lookup"><span data-stu-id="51ff7-293">Success is indicated by the message “Metadata publishing for this service is currently disabled” or by information resembling code.</span></span> <span data-ttu-id="51ff7-294">Если появляется какое-либо другое сообщение об ошибке или страница не была найдена, страница не загрузилась успешно.</span><span class="sxs-lookup"><span data-stu-id="51ff7-294">If you see some other error message or if the page cannot be found, the page has not loaded successfully.</span></span>



~~~
-   *http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports

-   *http://&lt;hostname&gt;/SelfService&gt;/*

-   *http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc*

-   *http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc*

-   *http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc*

-   *http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc*

**Note**  
It is assumed that the server features were installed on the default port without network encryption. If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.aspx* or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*

If the server features were installed with network encryption, change http:// to https://.
~~~



8. <span data-ttu-id="51ff7-295">Убедитесь, что все веб-страницы успешно загружены.</span><span class="sxs-lookup"><span data-stu-id="51ff7-295">Verify that each webpage loads successfully.</span></span>

## <span data-ttu-id="51ff7-296">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="51ff7-296">Related topics</span></span>


[<span data-ttu-id="51ff7-297">Развертывание инфраструктуры сервера MBAM 2.0 Server</span><span class="sxs-lookup"><span data-stu-id="51ff7-297">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









