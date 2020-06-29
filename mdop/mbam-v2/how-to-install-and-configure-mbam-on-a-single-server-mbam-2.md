---
title: Установка и настройка MBAM на одном сервере
description: Установка и настройка MBAM на одном сервере
author: dansimp
ms.assetid: 45e6a012-6c8c-4d90-902c-d09de9a0cbea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53e170f421bdce8dd6f771af3902af627a15a085
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824069"
---
# <span data-ttu-id="3a6fb-103">Установка и настройка MBAM на одном сервере</span><span class="sxs-lookup"><span data-stu-id="3a6fb-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="3a6fb-104">В этой статье описано, как установить администрирование и мониторинг Microsoft BitLocker (MBAM) в изолированной топологии на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) in the Stand-alone topology on a single server.</span></span> <span data-ttu-id="3a6fb-105">Используйте односерверную конфигурацию только в тестовой среде.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-105">Use the single-server configuration only in a test environment.</span></span> <span data-ttu-id="3a6fb-106">Для рабочих сред используйте два или более серверов.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-106">For production environments, use two or more servers.</span></span> <span data-ttu-id="3a6fb-107">Если вы устанавливаете администрирование и мониторинг Microsoft BitLocker с помощью топологии Configuration Manager, ознакомьтесь [с разворачиванием MBAM в Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="3a6fb-107">If you are installing Microsoft BitLocker Administration and Monitoring by using the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="3a6fb-108">На приведенной ниже схеме показан пример архитектуры с одним сервером.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-108">The following diagram shows an example of a single-server architecture.</span></span> <span data-ttu-id="3a6fb-109">Описание баз данных и функций можно найти в разделе [архитектура высокого уровня для MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="3a6fb-109">For a description of the databases and features, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

![топология развертывания MBAM 2 для одного сервера](images/mbam2-1-server.gif)

<span data-ttu-id="3a6fb-111">Каждый компонент сервера имеет определенные предварительные условия.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-111">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="3a6fb-112">Чтобы убедиться в том, что требования к оборудованию и программному обеспечению соблюдены, ознакомьтесь с требованиями к [развертыванию MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) и [MBAM 2,0 поддерживаемые конфигурации](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="3a6fb-112">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="3a6fb-113">Кроме того, у некоторых функций также есть информация, которая должна быть предоставлена в процессе установки, чтобы успешно развернуть компонент.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-113">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="3a6fb-114">Кроме того, прежде чем приступить к развертыванию MBAM, вам также необходимо проанализировать [подготовку среды для MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md) .</span><span class="sxs-lookup"><span data-stu-id="3a6fb-114">You should also review [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md) before you start MBAM deployment.</span></span>

**<span data-ttu-id="3a6fb-115">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-115">Note</span></span>**  
<span data-ttu-id="3a6fb-116">Чтобы получить файлы журнала установки, вы можете установить MBAM с помощью пакета msiexec и параметра **/l** &lt; Location &gt; .</span><span class="sxs-lookup"><span data-stu-id="3a6fb-116">To obtain the setup log files, you have use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="3a6fb-117">Файлы журнала создаются в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-117">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="3a6fb-118">Дополнительные файлы журнала установки создаются в папке% Temp% на сервере пользователя, устанавливающего MBAM.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-118">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <span data-ttu-id="3a6fb-119">Установка функций сервера MBAM на одном сервере</span><span class="sxs-lookup"><span data-stu-id="3a6fb-119">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="3a6fb-120">Ниже описаны действия, которые необходимо выполнить, чтобы установить общие функции MBAM.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-120">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="3a6fb-121">Чтобы запустить установку компонентов сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="3a6fb-121">To start the MBAM Server features installation</span></span>**

1.  <span data-ttu-id="3a6fb-122">На сервере, на котором вы хотите установить MBAM, запустите мастер установки MBAM, выпуская **MBAMSetup.exe** .</span><span class="sxs-lookup"><span data-stu-id="3a6fb-122">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="3a6fb-123">На странице **приветствия** при необходимости выберите **программу улучшения качества программного**обеспечения, а затем нажмите кнопку **начать**.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-123">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="3a6fb-124">Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-124">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="3a6fb-125">На странице **Выбор топологии** выберите **изолированную** топологию и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-125">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="3a6fb-126">На странице **выберите** устанавливаемые компоненты выберите компоненты, которые вы хотите установить.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-126">On the **Select features to install** page, select the features that you want to install.</span></span> <span data-ttu-id="3a6fb-127">По умолчанию для установки выбраны все функции MBAM.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-127">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="3a6fb-128">Функции, устанавливаемые на одном и том же компьютере, должны быть установлены одновременно.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-128">Features that are to be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="3a6fb-129">Снимите флажки для функций, которые вы хотите установить на другом месте.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-129">Clear the check boxes for any features that you want to install elsewhere.</span></span> <span data-ttu-id="3a6fb-130">Компоненты MBAM нужно устанавливать в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="3a6fb-130">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="3a6fb-131">База данных восстановления</span><span class="sxs-lookup"><span data-stu-id="3a6fb-131">Recovery Database</span></span>

    -   <span data-ttu-id="3a6fb-132">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="3a6fb-132">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="3a6fb-133">Отчеты о соответствии и аудите</span><span class="sxs-lookup"><span data-stu-id="3a6fb-133">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="3a6fb-134">Сервер самообслуживания</span><span class="sxs-lookup"><span data-stu-id="3a6fb-134">Self-Service Server</span></span>

    -   <span data-ttu-id="3a6fb-135">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="3a6fb-135">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="3a6fb-136">Шаблон групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="3a6fb-136">MBAM Group Policy template</span></span>

    **<span data-ttu-id="3a6fb-137">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-137">Note</span></span>**  
    <span data-ttu-id="3a6fb-138">Мастер установки проверяет предварительные требования для установки и выводит недостающие необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-138">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="3a6fb-139">Если все необходимые условия выполнены, установка будет продолжена.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-139">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="3a6fb-140">Если обнаружен отсутствующий предварительный компонент, необходимо устранить недостающие необходимые компоненты и нажать кнопку **проверить необходимые компоненты еще раз**.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-140">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="3a6fb-141">Если все необходимые условия выполнены, установка возобновляется.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-141">If all prerequisites are met this time, the installation resumes.</span></span>



6.  <span data-ttu-id="3a6fb-142">На странице **Настройка безопасности сетевых подключений** укажите, следует ли шифровать связь между веб-службами на сервере администрирования и сервера мониторинга и на клиентах.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-142">On the **Configure network communication security** page, choose whether to encrypt the communication between the Web Services on the Administration and Monitoring Server and the clients.</span></span> <span data-ttu-id="3a6fb-143">Если вы решили зашифровать связь, выберите сертификат, предоставленный центром сертификации, для использования при шифровании.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-143">If you decide to encrypt the communication, select the certification authority-provisioned certificate to use for encryption.</span></span> <span data-ttu-id="3a6fb-144">Перед тем как выбрать этот этап, вы должны создать сертификат на этой странице, чтобы сделать это.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-144">The certificate must be created prior to this step to enable you to select it on this page.</span></span>

    **<span data-ttu-id="3a6fb-145">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-145">Note</span></span>**  
    <span data-ttu-id="3a6fb-146">Эта страница отображается только в том случае, если вы выбрали портал самообслуживания или сервер администрирования и мониторинга на странице **выберите компоненты для установки** .</span><span class="sxs-lookup"><span data-stu-id="3a6fb-146">This page appears only if you selected the Self-Service Portal or the Administration and Monitoring Server feature on the **Select features to install** page.</span></span>



7.  <span data-ttu-id="3a6fb-147">Нажмите кнопку **Далее**, а затем перейдите к следующему набору шагов, чтобы настроить возможности сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-147">Click **Next**, and then continue to the next set of steps to configure the MBAM Server features.</span></span>

**<span data-ttu-id="3a6fb-148">Настройка функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="3a6fb-148">To configure the MBAM Server features</span></span>**

1.  <span data-ttu-id="3a6fb-149">На странице **Настройка базы данных восстановления** укажите имя экземпляра SQL Server и имя базы данных, в которой будут храниться данные для восстановления.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-149">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="3a6fb-150">Кроме того, необходимо указать, где находятся файлы базы данных и где будут храниться данные журнала.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-150">You must also specify both where the database files will be located and where the log information will be located.</span></span>

2.  <span data-ttu-id="3a6fb-151">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-151">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="3a6fb-152">На странице **Настройка базы данных соответствия и аудита** укажите имя экземпляра SQL Server и имя базы данных, в которой будут храниться сведения о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-152">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="3a6fb-153">Кроме того, необходимо указать расположение файлов базы данных и расположение данных журнала.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-153">You must also specify where the database files will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="3a6fb-154">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-154">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="3a6fb-155">На странице " **Настройка отчетов о соответствии и аудите** " укажите экземпляр служб SQL Server Reporting Services, на котором будут установлены отчеты о соответствии и аудите, а также укажите учетную запись пользователя домена и пароль для доступа к базе данных "соответствие требованиям" и "Аудит".</span><span class="sxs-lookup"><span data-stu-id="3a6fb-155">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password for accessing the Compliance and Audit database.</span></span> <span data-ttu-id="3a6fb-156">Настройка пароля для этой учетной записи бессрочна.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-156">Configure the password for this account to never expire.</span></span> <span data-ttu-id="3a6fb-157">Учетная запись пользователя должна иметь доступ ко всем данным, доступным для группы "Пользователи отчетов MBAM".</span><span class="sxs-lookup"><span data-stu-id="3a6fb-157">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="3a6fb-158">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-158">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="3a6fb-159">На странице **Настройка портала самообслуживания** введите номер порта, имя узла, имя виртуального каталога и путь установки для портала самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    **<span data-ttu-id="3a6fb-160">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-160">Note</span></span>**  
    <span data-ttu-id="3a6fb-161">Номер порта, который вы указали, должен быть неиспользуемым номеру на сервере администрирования и мониторинга, если не указано уникальное имя заголовка узла.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-161">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="3a6fb-162">Если вы используете брандмауэр Windows, этот порт будет открыт автоматически.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-162">If you are using Windows Firewall, the port will be opened automatically.</span></span>



8.  <span data-ttu-id="3a6fb-163">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-163">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="3a6fb-164">Укажите, следует ли использовать обновления Microsoft, чтобы обеспечить безопасность компьютера, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-164">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="3a6fb-165">При этом автоматические обновления в Windows не активируются.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-165">This does not turn on Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="3a6fb-166">На странице " **Настройка сервера администрирования и мониторинга** " введите номер порта, имя узла, имя виртуального каталога и путь установки для веб-сайта службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-166">On the **Configure the Administration and Monitoring Server** page, enter the port number, host name, virtual directory name, and installation path for the Help Desk website.</span></span>

    **<span data-ttu-id="3a6fb-167">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-167">Note</span></span>**  
    <span data-ttu-id="3a6fb-168">Номер порта, который вы указали, должен быть неиспользуемым номеру на сервере администрирования и мониторинга, если не указано уникальное имя заголовка узла.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-168">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="3a6fb-169">Если вы используете брандмауэр Windows, этот порт будет открыт автоматически.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-169">If you are using Windows Firewall, the port will be opened automatically.</span></span>



11. <span data-ttu-id="3a6fb-170">На странице **Сводка по установке** ознакомьтесь со списком компонентов, которые будут установлены, и нажмите кнопку **установить** , чтобы начать установку функций MBAM.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-170">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="3a6fb-171">Нажмите кнопку " **назад** ", чтобы вернуться к мастеру, чтобы просмотреть или изменить параметры установки, или кнопку **"Отмена"** , чтобы выйти из программы установки.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-171">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="3a6fb-172">Программа установки устанавливает функции MBAM и уведомляет о том, что установка завершена.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-172">Setup installs the MBAM features and notifies you that the installation is complete.</span></span>

12. <span data-ttu-id="3a6fb-173">Нажмите кнопку **Готово** , чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-173">Click **Finish** to exit the wizard.</span></span> <span data-ttu-id="3a6fb-174">После установки функций сервера администрирования и мониторинга Microsoft BitLocker перейдите к следующему разделу и следуйте инструкциям, чтобы добавить пользователей в роли администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-174">After the Microsoft BitLocker Administration and Monitoring Server features have been installed, continue to the next section and complete the steps have to add users to the Microsoft BitLocker Administration and Monitoring roles.</span></span> <span data-ttu-id="3a6fb-175">Дополнительные сведения о ролях можно найти в разделе [Планирование ролей администратора для MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="3a6fb-175">For more information about roles, see [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).</span></span>

**<span data-ttu-id="3a6fb-176">Чтобы выполнить настройку после установки, выполните описанные выше действия.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-176">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="3a6fb-177">На сервере администрирования и мониторинга добавьте пользователей в следующие локальные группы, чтобы предоставить им доступ к функциям веб-сайта службы поддержки MBAM.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-177">On the Administration and Monitoring Server, add users to the following local groups to give them access to the MBAM Help Desk website features:</span></span>

    -   <span data-ttu-id="3a6fb-178">**Пользователи службы поддержки MBAM**: участники этой локальной группы могут получить доступ к восстановлению диска и управлять функциями TPM на веб-сайте администрирования MBAM и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-178">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="3a6fb-179">Все поля в восстановлении диска и Управление TPM являются обязательными полями для пользователя службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-179">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="3a6fb-180">**MBAM для опытных пользователей службы поддержки**: участники этой локальной группы имеют расширенный доступ к восстановлению диска и управляют функциями доверенного платформенного модуля на веб-сайте администрирования MBAM и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-180">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="3a6fb-181">Для опытных пользователей службы поддержки требуется только поле " **ИД ключа** " в восстановлении диска.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-181">For Advanced Helpdesk Users, only the **Key ID** field is required in Drive Recovery.</span></span> <span data-ttu-id="3a6fb-182">В разделе Управление доверенными платформенными модулями требуется только поле **компьютера домена** и **имя компьютера** .</span><span class="sxs-lookup"><span data-stu-id="3a6fb-182">In Manage TPM, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="3a6fb-183">На сервере администрирования и мониторинга добавьте пользователей в следующую локальную группу, чтобы разрешить им доступ к функциям отчетов на веб-сайте администрирования и мониторинга MBAM:</span><span class="sxs-lookup"><span data-stu-id="3a6fb-183">On the Administration and Monitoring Server, add users to the following local group to enable them to access the Reports feature on the MBAM Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="3a6fb-184">**Пользователи отчетов MBAM**: участники этой локальной группы могут получать доступ к функциям отчетов на веб-сайте администрирования MBAM и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-184">**MBAM Report Users**: Members of this local group can access the Reports features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="3a6fb-185">Фирменный портал самообслуживания с названием вашей компании, текст уведомления и другие сведения, относящиеся к определенной компании.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-185">Brand the Self-Service Portal with your company name, notice text, and other company-specific information.</span></span> <span data-ttu-id="3a6fb-186">Инструкции можно найти [в разделе как фирменная символика портала самообслуживания](how-to-brand-the-self-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="3a6fb-186">For instructions, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md).</span></span>

    **<span data-ttu-id="3a6fb-187">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-187">Note</span></span>**  
    <span data-ttu-id="3a6fb-188">Идентичные пользователи или члены группы в **отчете MBAM** локальная группа пользователей должны поддерживаться на всех компьютерах, на которых установлены средства администрирования MBAM и мониторинга сервера, база данных соответствия требованиям и аудита, а также отчеты о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-188">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span> <span data-ttu-id="3a6fb-189">Рекомендуемый способ — создать группу безопасности домена и добавить эту группу домена в каждую локальную группу пользователей MBAM отчетов.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-189">The recommended way to do this is to create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="3a6fb-190">При использовании этого процесса можно управлять членством в группах, используя группу домена.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-190">When you use this process, manage the group memberships by way of the domain group.</span></span>



## <span data-ttu-id="3a6fb-191">Проверка установки компонентов сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="3a6fb-191">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="3a6fb-192">После завершения установки администрирования и наблюдения за помощью Microsoft BitLocker убедитесь, что установка успешно настроила все необходимые функции MBAM, необходимые для управления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-192">When the Microsoft BitLocker Administration and Monitoring installation is completed, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="3a6fb-193">Чтобы убедиться в том, что служба MBAM работает, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-193">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="3a6fb-194">Проверка установки компонента сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="3a6fb-194">To validate the MBAM Server feature installation</span></span>**

1. <span data-ttu-id="3a6fb-195">На каждом сервере, на котором развернута функция MBAM, откройте **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-195">On each server where a MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="3a6fb-196">Нажмите кнопку **программы**и выберите пункт **программы и компоненты**.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-196">Select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="3a6fb-197">Убедитесь в том, что в списке **программы и компоненты** отображается элемент **Администрирование и мониторинг Microsoft BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="3a6fb-197">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="3a6fb-198">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-198">Note</span></span>**  
   <span data-ttu-id="3a6fb-199">Для проверки установки необходимо использовать учетную запись домена, которая содержит учетные данные администратора локального компьютера на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-199">To validate the installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="3a6fb-200">На сервере с установленной базой данных восстановления откройте SQL Server Management Studio и убедитесь, что установлена **Восстановление MBAM и** база данных оборудования.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-200">On the server where the Recovery Database is installed, open SQL Server Management Studio, and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="3a6fb-201">На сервере, на котором установлена база данных соответствия и аудита, откройте SQL Server Management Studio и убедитесь, что **база данных состояния соответствия MBAM** установлена.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-201">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio, and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="3a6fb-202">На сервере, на котором установлены отчеты о соответствии и аудите, откройте веб-браузер с учетными данными администратора и перейдите на сайт "Главная" сайта служб SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-202">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="3a6fb-203">Расположением по умолчанию для сайта служб SQL Server Reporting Services является http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-203">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="3a6fb-204">Чтобы найти фактический URL-адрес, используйте Диспетчер конфигураций служб Reporting Services и выберите экземпляры, заданные во время настройки.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-204">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that are specified during setup.</span></span>

   <span data-ttu-id="3a6fb-205">Убедитесь в том, что в папке Reporting (Администрирование и мониторинг) Microsoft BitLocker есть источник данных **MaltaDataSource** и что в папке **en-US** есть четыре отчета.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-205">Confirm that a Reports folder named Microsoft BitLocker Administration and Monitoring contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="3a6fb-206">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-206">Note</span></span>**  
   <span data-ttu-id="3a6fb-207">Если службы отчетов SQL Server были настроены как именованный экземпляр, URL-адрес должен выглядеть следующим образом: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="3a6fb-207">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following: http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="3a6fb-208">На сервере, на котором установлен компонент "Администрирование и наблюдение", запустите **Диспетчер серверов** и перейдите к **ролям**.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-208">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="3a6fb-209">Выберите **веб-сервер (IIS)**, а затем — **Диспетчер служб Internet Information Services (IIS).**</span><span class="sxs-lookup"><span data-stu-id="3a6fb-209">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager.**</span></span>

6. <span data-ttu-id="3a6fb-210">В окне **подключения** откройте вкладку \* &lt; имя_компьютера &gt; \*, выберите **сайты**, а затем — **Администрирование и мониторинг Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-210">In **Connections,** browse to *&lt;computername&gt;*, select **Sites**, and then select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="3a6fb-211">Убедитесь в том, что указаны **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**и **MBAMRecoveryAndHardwareService** .</span><span class="sxs-lookup"><span data-stu-id="3a6fb-211">Verify that **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="3a6fb-212">На сервере, на котором установлены функции администрирования и наблюдения и портал самообслуживания, откройте веб-браузер с учетными данными администратора и перейдите по следующим ссылкам, чтобы убедиться в том, что они успешно загружены.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-212">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully:</span></span>

   -   <span data-ttu-id="3a6fb-213">*http:// &lt; имя_узла &gt; /HelpDesk/Default.aspx* и убедитесь, что каждая из ссылок для навигации и отчетов</span><span class="sxs-lookup"><span data-stu-id="3a6fb-213">*http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="3a6fb-214">http:// &lt; HostName &gt; /Selfservice&gt;/</span><span class="sxs-lookup"><span data-stu-id="3a6fb-214">http://&lt;hostname&gt;/SelfService&gt;/</span></span>*

   -   *<span data-ttu-id="3a6fb-215">http:// &lt; имя_компьютера &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="3a6fb-215">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="3a6fb-216">http:// &lt; HostName &gt; /MBAMUserSupportService/UserSupportService.svc</span><span class="sxs-lookup"><span data-stu-id="3a6fb-216">http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>*

   -   *<span data-ttu-id="3a6fb-217">http:// &lt; имя_компьютера &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="3a6fb-217">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="3a6fb-218">http:// &lt; имя_компьютера &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="3a6fb-218">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="3a6fb-219">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-219">Note</span></span>**  
   <span data-ttu-id="3a6fb-220">Предполагается, что компоненты сервера были установлены на порт по умолчанию без сетевого шифрования.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-220">It is assumed that the server features were installed on the default port without network encryption.</span></span> <span data-ttu-id="3a6fb-221">Если вы установили компоненты сервера на другом порте или виртуальном каталоге, измените URL-адреса таким образом, чтобы он включал соответствующий порт, например *http:// &lt; имя_узла &gt; : &lt; Port &gt; /HelpDesk/Default.ASP*x или*http:// &lt; HostName &gt; : &lt; порт &gt; / &lt; VirtualDirectory &gt; /Default.aspx*</span><span class="sxs-lookup"><span data-stu-id="3a6fb-221">If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.asp*x or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*</span></span>

   <span data-ttu-id="3a6fb-222">Если компоненты сервера были установлены с шифрованием сети, измените http://на https://.</span><span class="sxs-lookup"><span data-stu-id="3a6fb-222">If the server features were installed with network encryption, change http:// to https://.</span></span>



## <span data-ttu-id="3a6fb-223">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3a6fb-223">Related topics</span></span>


[<span data-ttu-id="3a6fb-224">Развертывание инфраструктуры сервера MBAM 2.0 Server</span><span class="sxs-lookup"><span data-stu-id="3a6fb-224">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









