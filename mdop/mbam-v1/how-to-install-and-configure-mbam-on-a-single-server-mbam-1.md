---
title: Установка и настройка MBAM на одном сервере
description: Установка и настройка MBAM на одном сервере
author: dansimp
ms.assetid: 55841c63-bad9-44e7-b7fd-ea7037febbd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 225f66493ceafce5461df3fcc6f701e9a2922a5f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824099"
---
# <span data-ttu-id="bfb8b-103">Установка и настройка MBAM на одном сервере</span><span class="sxs-lookup"><span data-stu-id="bfb8b-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="bfb8b-104">Процедуры, описанные в этом разделе, описывают полную установку функций администрирования и мониторинга Microsoft BitLocker (MBAM) на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on a single server.</span></span>

<span data-ttu-id="bfb8b-105">Каждый компонент сервера имеет определенные предварительные условия.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="bfb8b-106">Чтобы убедиться, что требования соблюдены и требования к оборудованию и программному обеспечению, ознакомьтесь с требованиями к [MBAM 1,0](mbam-10-deployment-prerequisites.md) и [MBAM 1,0 поддерживаемые конфигурации](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="bfb8b-106">To verify that you have met the prerequisites and the hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="bfb8b-107">Кроме того, у некоторых функций также есть информация, которая должна быть предоставлена в процессе установки, чтобы успешно развернуть компонент.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-107">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="bfb8b-108">Кроме того, прежде чем приступить к развертыванию MBAM, необходимо предварительно проанализировать [подготовку среды для MBAM 1,0](preparing-your-environment-for-mbam-10.md) .</span><span class="sxs-lookup"><span data-stu-id="bfb8b-108">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM deployment.</span></span>

<span data-ttu-id="bfb8b-109">**Примечание**  Чтобы получить файлы журнала установки, необходимо установить MBAM с помощью пакета **msiexec** и параметра **/l** &lt; Location &gt; .</span><span class="sxs-lookup"><span data-stu-id="bfb8b-109">**Note** To obtain the setup log files, you must install MBAM by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="bfb8b-110">Файлы журнала создаются в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="bfb8b-111">Дополнительные файлы журнала установки создаются в папке% temp% пользователя, устанавливающего MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-111">Additional setup log files are created in the %temp% folder of the user who is installing MBAM.</span></span>

 

## <span data-ttu-id="bfb8b-112">Установка функций сервера MBAM на одном сервере</span><span class="sxs-lookup"><span data-stu-id="bfb8b-112">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="bfb8b-113">Ниже описаны действия, которые необходимо выполнить, чтобы установить общие функции MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-113">The following steps describe how to install general MBAM features.</span></span>

<span data-ttu-id="bfb8b-114">**Примечание**  Убедитесь, что вы используете 32-разрядную настройку на 32-разрядных серверах и на 64-разрядной установке на 64-разрядных серверах.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-114">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="bfb8b-115">Чтобы запустить установку компонентов сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="bfb8b-115">To start MBAM Server features installation</span></span>**

1.  <span data-ttu-id="bfb8b-116">Запустите мастер установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-116">Start the MBAM installation wizard.</span></span> <span data-ttu-id="bfb8b-117">На странице приветствия нажмите кнопку **установить** .</span><span class="sxs-lookup"><span data-stu-id="bfb8b-117">Click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="bfb8b-118">Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="bfb8b-119">По умолчанию для установки выбраны все функции MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="bfb8b-120">Функции, которые будут установлены на одном и том же компьютере, должны быть установлены одновременно.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-120">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="bfb8b-121">Снимите флажки для компонентов, которые вы хотите установить на другом месте.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-121">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="bfb8b-122">Функции MBAM необходимо установить в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="bfb8b-122">You must install the MBAM features in the following order:</span></span>

    -   <span data-ttu-id="bfb8b-123">База данных восстановления и оборудования</span><span class="sxs-lookup"><span data-stu-id="bfb8b-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="bfb8b-124">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="bfb8b-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="bfb8b-125">Аудит соответствия требованиям и отчеты</span><span class="sxs-lookup"><span data-stu-id="bfb8b-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="bfb8b-126">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="bfb8b-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="bfb8b-127">Шаблон групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="bfb8b-127">MBAM Group Policy Template</span></span>

    <span data-ttu-id="bfb8b-128">**Примечание**  Мастер установки проверяет предварительные требования для установки и выводит недостающие необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-128">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="bfb8b-129">Если все необходимые условия выполнены, установка будет продолжена.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-129">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="bfb8b-130">Если обнаружен отсутствующий предварительный компонент, необходимо устранить недостающие необходимые условия и нажать кнопку **проверить необходимые компоненты еще раз**.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-130">If a missing prerequisite is detected, you must resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="bfb8b-131">После того как все необходимые условия будут выполнены, установка продолжится.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-131">After all prerequisites are met, the installation resumes.</span></span>

     

4.  <span data-ttu-id="bfb8b-132">Вам будет предложено настроить безопасность сетевого соединения.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-132">You are prompted to configure the network communication security.</span></span> <span data-ttu-id="bfb8b-133">MBAM может шифровать связь между базой данных восстановления и оборудования, сервером администрирования и мониторинга и клиентами.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-133">MBAM can encrypt the communication between the Recovery and Hardware Database, the Administration and Monitoring Server, and the clients.</span></span> <span data-ttu-id="bfb8b-134">Если вы решили зашифровать связь, вам будет предложено выбрать сертификат, подготовленный центром сертификации, который будет использоваться для шифрования.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-134">If you decide to encrypt the communication, you are asked to select the authority-provisioned certificate that will be used for encryption.</span></span>

5.  <span data-ttu-id="bfb8b-135">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-135">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="bfb8b-136">В мастере настройки MBAM будут отображены страницы установки для выбранных функций.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-136">The MBAM Setup wizard will display the installation pages for the selected features.</span></span>

**<span data-ttu-id="bfb8b-137">Развертывание функций сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="bfb8b-137">To deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="bfb8b-138">В окне **Настройка базы данных восстановления и оборудования** укажите экземпляр SQL Server и имя базы данных, в которой будут храниться данные для восстановления и оборудования.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-138">In the **Configure the Recovery and Hardware database** window, specify the instance of SQL Server and the name of the database that will store the recovery and hardware data.</span></span> <span data-ttu-id="bfb8b-139">Кроме того, необходимо указать расположение файлов базы данных и сведения о журнале.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-139">You must also specify both the database files location and the log information location.</span></span>

2.  <span data-ttu-id="bfb8b-140">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-140">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="bfb8b-141">В окне **Настройка базы данных соответствия и аудита** укажите экземпляр SQL Server и имя базы данных, в которой будут храниться сведения о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-141">In the **Configure the Compliance and Audit database** window, specify the instance of the SQL Server and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="bfb8b-142">Затем укажите расположение файлов базы данных и расположение данных журнала.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-142">Then, specify the database files location and the log information location.</span></span>

4.  <span data-ttu-id="bfb8b-143">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-143">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="bfb8b-144">В окне " **соответствие требованиям и аудиту** " укажите экземпляр службы отчетов, который будет использоваться, и предоставьте учетную запись пользователя домена для доступа к базе данных.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-144">In the **Compliance and Audit Reports** window, specify the report service instance that will be used and provide a domain user account for accessing the database.</span></span> <span data-ttu-id="bfb8b-145">Это должна быть учетная запись пользователя, специально подготовленная для этого использования.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-145">This should be a user account that is provisioned specifically for this use.</span></span> <span data-ttu-id="bfb8b-146">Учетная запись пользователя должна иметь доступ ко всем данным, доступным для группы "Пользователи отчетов MBAM".</span><span class="sxs-lookup"><span data-stu-id="bfb8b-146">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="bfb8b-147">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-147">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="bfb8b-148">В окне **Настройка сервера администрирования и мониторинга** введите название **порта**, **имя узла** (необязательно), а также **путь установки** для сервера администрирования и мониторинга MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-148">In the **Configure the Administration and Monitoring Server** window, enter the **Port Binding**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server.</span></span>

    <span data-ttu-id="bfb8b-149">**Предупреждение**  Номер порта, который вы указали, должен быть неиспользуемым номером порта на сервере администрирования и мониторинга, если не указано уникальное имя заголовка узла.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-149">**Warning** The port number that you specify must be an unused port number on the Administration and Monitoring server, unless a unique host header name is specified.</span></span>

     

8.  <span data-ttu-id="bfb8b-150">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-150">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="bfb8b-151">Укажите, следует ли использовать обновления Microsoft, чтобы обеспечить безопасность компьютера, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-151">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="bfb8b-152">Функция автоматического обновления в Windows не включена в Microsoft Updates.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-152">The Microsoft Updates option does not turn on the Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="bfb8b-153">Когда мастер настройки собрал необходимые сведения о компонентах, установка MBAM готова к началу работы.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-153">When the Setup wizard has collected the necessary feature information, the MBAM installation is ready to start.</span></span> <span data-ttu-id="bfb8b-154">Нажмите кнопку **назад** , чтобы вернуться к просмотру или изменению параметров установки, если вы хотите просмотреть или изменить параметры.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-154">Click **Back** to move back through the wizard if you want to review or change your installation settings.</span></span> <span data-ttu-id="bfb8b-155">Нажмите кнопку " **установить** ", чтобы начать установку.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-155">Click **Install** to begin the installation.</span></span> <span data-ttu-id="bfb8b-156">Нажмите кнопку **"Отмена"** , чтобы выйти из программы установки.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-156">Click **Cancel** to exit Setup.</span></span> <span data-ttu-id="bfb8b-157">Программа установки устанавливает функции MBAM и уведомляет о том, что установка завершена.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-157">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

11. <span data-ttu-id="bfb8b-158">Нажмите кнопку **Готово** , чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-158">Click **Finish** to exit the wizard.</span></span>

12. <span data-ttu-id="bfb8b-159">После установки функций сервера MBAM необходимо добавить пользователей в роли MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-159">After you install MBAM server features, you must add users to the MBAM roles.</span></span> <span data-ttu-id="bfb8b-160">Дополнительные сведения можно найти в разделе [Планирование ролей администратора для MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="bfb8b-160">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="bfb8b-161">Чтобы выполнить настройку после установки, выполните описанные выше действия.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-161">To perform post installation configuration</span></span>**

1.  <span data-ttu-id="bfb8b-162">После завершения настройки необходимо добавить роли пользователей, чтобы предоставить пользователям доступ к функциям на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-162">After Setup is finished, you must add user roles so that you can give users access to features in the MBAM administration website.</span></span> <span data-ttu-id="bfb8b-163">На сервере администрирования и мониторинга добавьте пользователей в следующие локальные группы:</span><span class="sxs-lookup"><span data-stu-id="bfb8b-163">On the Administration and Monitoring Server, add users to the following local groups:</span></span>

    -   <span data-ttu-id="bfb8b-164">**Пользователи оборудования MBAM**: участники этой локальной группы могут получить доступ к компоненту "оборудование" на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-164">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="bfb8b-165">**Пользователи службы поддержки MBAM**: члены этой локальной группы могут получать доступ к восстановлению диска и управлять функциями доверенного платформенного модуля на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-165">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="bfb8b-166">Все поля в восстановлении диска и Управление TPM являются обязательными полями для пользователя службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-166">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="bfb8b-167">**MBAM опытных пользователей службы поддержки**: участники этой локальной группы имеют расширенный доступ к восстановлению диска и управляют функциями доверенного платформенного модуля на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-167">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="bfb8b-168">Для опытных пользователей службы поддержки требуется только поле "ИД ключа" в восстановлении диска.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-168">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="bfb8b-169">Для управления пользователями доверенного платформенного модуля требуется только поле "домен компьютера" и поле "имя компьютера".</span><span class="sxs-lookup"><span data-stu-id="bfb8b-169">For Manage TPM users, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="bfb8b-170">В базе данных администрирования и мониторинга сервера, соответствия требованиям и аудита и на компьютере, на котором размещаются отчеты о соответствии и аудите, добавьте пользователей в следующую локальную группу, чтобы предоставить им доступ к функции "отчеты" на веб-сайте администрирования MBAM:</span><span class="sxs-lookup"><span data-stu-id="bfb8b-170">On the Administration and Monitoring Server, Compliance and Audit Database, and on the computer that hosts the Compliance and Audit Reports, add users to the following local group to enable them to access the Reports feature in the MBAM administration website:</span></span>

    -   <span data-ttu-id="bfb8b-171">**Пользователи отчетов MBAM**: участники этой локальной группы могут получать доступ к функциям отчетов на веб-сайте администрирования MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-171">**MBAM Report Users**: Members of this local group can access the Reports features in the MBAM administration website.</span></span>

    <span data-ttu-id="bfb8b-172">**Примечание**  На всех компьютерах, на которых установлены функции администрирования и мониторинга, а также отчеты о соответствии требованиям и аудите, должны поддерживаться в соответствии с членством пользователей в локальной группе **пользователей отчета MBAM** .</span><span class="sxs-lookup"><span data-stu-id="bfb8b-172">**Note** Identical user membership or group membership of the **MBAM Report Users** local group must be maintained on all computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

    <span data-ttu-id="bfb8b-173">Чтобы сохранить идентичные сведения о членстве на всех компьютерах, следует создать группу безопасности домена и добавить эту группу домена в каждую локальную группу пользователей MBAM отчетов.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-173">To maintain identical memberships on all computers, you should create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="bfb8b-174">После этого вы сможете управлять членством в группах, используя группу домена.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-174">When you do this, you can manage the group memberships by using the domain group.</span></span>

     

## <span data-ttu-id="bfb8b-175">Проверка установки компонентов сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="bfb8b-175">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="bfb8b-176">После завершения установки MBAM убедитесь в том, что установка успешно настроила все необходимые функции MBAM, необходимые для управления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-176">When the MBAM installation is complete, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="bfb8b-177">Чтобы убедиться в том, что служба MBAM работает, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-177">Use the following procedure to confirm that the MBAM service is functional:</span></span>

**<span data-ttu-id="bfb8b-178">Проверка установки компонентов сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="bfb8b-178">To validate MBAM Server feature installation</span></span>**

1. <span data-ttu-id="bfb8b-179">На каждом сервере, на котором развернута функция MBAM, откройте **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-179">On each server where an MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="bfb8b-180">Нажмите кнопку **программы**и выберите пункт **программы и компоненты**.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-180">Click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="bfb8b-181">Убедитесь в том, что в списке **программы и компоненты** отображается элемент **Администрирование и мониторинг Microsoft BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="bfb8b-181">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="bfb8b-182">Примечание.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-182">Note</span></span>**  
   <span data-ttu-id="bfb8b-183">Для проверки установки необходимо использовать учетную запись домена, которая содержит учетные данные администратора локального компьютера на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-183">To validate the installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>

     

2. <span data-ttu-id="bfb8b-184">На сервере, на котором установлена база данных восстановления и оборудования, откройте SQL Server Management Studio и убедитесь, что установлена **Восстановление MBAM и** база данных оборудования.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-184">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="bfb8b-185">На сервере, на котором установлена база данных соответствия и аудита, откройте центр администрирования SQL Server и убедитесь, что установлена проверка **соответствия MBAM и база данных аудита** .</span><span class="sxs-lookup"><span data-stu-id="bfb8b-185">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance and Audit Database** is installed.</span></span>

4. <span data-ttu-id="bfb8b-186">На сервере, на котором установлены отчеты о соответствии и аудите, откройте веб-браузер с правами администратора и перейдите на веб-сайт служб SQL Server Reporting Services на домашнюю страницу.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-186">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="bfb8b-187">Расположением по умолчанию для сайта служб SQL Server Reporting Services является http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-187">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="bfb8b-188">Чтобы найти фактический URL-адрес, используйте Диспетчер конфигураций служб Reporting Services и выберите экземпляры, заданные во время настройки.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-188">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="bfb8b-189">Убедитесь в том, что в списке указана папка **Отчеты соответствие требованиям** , и что она содержит пять отчетов и один источник данных.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-189">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="bfb8b-190">Примечание.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-190">Note</span></span>**  
   <span data-ttu-id="bfb8b-191">Если службы отчетов SQL Server были настроены как именованный экземпляр, URL-адрес должен выглядеть следующим образом: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="bfb8b-191">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>

     

5. <span data-ttu-id="bfb8b-192">На сервере, на котором установлен компонент "Администрирование и наблюдение", запустите **Диспетчер серверов** и перейдите к пункту " **роли**", выберите **веб-сервер (IIS)** и нажмите кнопку " **Диспетчер служб Internet Information Services (IIS)** ".</span><span class="sxs-lookup"><span data-stu-id="bfb8b-192">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and click **Internet Information Services (IIS) Manager**</span></span>

6. <span data-ttu-id="bfb8b-193">В окне " **подключения**" перейдите на сайт \* &lt; ComputerName &gt; \*, выберите **сайты**и выберите пункт **Администрирование и мониторинг Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-193">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="bfb8b-194">Убедитесь в том, что указаны **MBAMAdministrationService**, **MBAMComplianceStatusService**и **MBAMRecoveryAndHardwareService** .</span><span class="sxs-lookup"><span data-stu-id="bfb8b-194">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="bfb8b-195">На сервере, на котором установлен компонент "Администрирование и наблюдение", откройте веб-браузер с правами администратора, а затем перейдите к следующим расположениям на веб-сайте MBAM, чтобы убедиться в том, что они успешно загружены.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-195">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges, and then browse to the following locations in the MBAM website to verify that they load successfully:</span></span>

   -   <span data-ttu-id="bfb8b-196">*http:// &lt; имя_компьютера &gt; /Default.aspx* и убедитесь в том, что все ссылки для навигации и отчетов</span><span class="sxs-lookup"><span data-stu-id="bfb8b-196">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="bfb8b-197">http:// &lt; имя_компьютера &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="bfb8b-197">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="bfb8b-198">http:// &lt; имя_компьютера &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="bfb8b-198">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="bfb8b-199">http:// &lt; имя_компьютера &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="bfb8b-199">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="bfb8b-200">Примечание.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-200">Note</span></span>**  
   <span data-ttu-id="bfb8b-201">Обычно службы устанавливаются на порт по умолчанию 80 без сетевого шифрования.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-201">Typically, the services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="bfb8b-202">Если службы установлены на другом порту, измените URL-адреса, чтобы включить соответствующий порт.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-202">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="bfb8b-203">Например, http://\* &lt; имя_компьютера &gt; : &lt; Port &gt; \*/Default.aspx или http:// <em> &lt; hostheadername &gt; / </em> Default. aspx.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-203">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx.</span></span>

   <span data-ttu-id="bfb8b-204">Если службы установлены с сетевым шифрованием, измените http://на https://.</span><span class="sxs-lookup"><span data-stu-id="bfb8b-204">If the services are installed with network encryption, change http:// to https://.</span></span>

     

## <span data-ttu-id="bfb8b-205">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="bfb8b-205">Related topics</span></span>


[<span data-ttu-id="bfb8b-206">Развертывание инфраструктуры сервера MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bfb8b-206">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





