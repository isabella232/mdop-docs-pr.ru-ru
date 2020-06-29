---
title: Обновление с предыдущих версий MBAM
description: Обновление с предыдущих версий MBAM
author: dansimp
ms.assetid: 73b425cf-9cd9-4ebc-a35e-1b3bf18596ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af45d193a5e8001288e70389ff220cb5d8269918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823809"
---
# <span data-ttu-id="79b63-103">Обновление с предыдущих версий MBAM</span><span class="sxs-lookup"><span data-stu-id="79b63-103">Upgrading from Previous Versions of MBAM</span></span>


<span data-ttu-id="79b63-104">Вы можете обновить администрирование и мониторинг Microsoft BitLocker (MBAM) до MBAM 2.0 с изолированной топологией или топологией Configuration Manager, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="79b63-104">You can upgrade Microsoft BitLocker Administration and Monitoring (MBAM) to MBAM2.0, with the Stand-alone topology or Configuration Manager topology, by doing the following:</span></span>

-   <span data-ttu-id="79b63-105">**Замена сервера вручную** — чтобы обновить сервер MBAM, вручную удалите MBAM с помощью установщика или панели управления, а затем установите инфраструктуру MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="79b63-105">**Manual in-place server replacement** – To upgrade the MBAM Server, manually uninstall MBAM by using either the installer or Control Panel, and then install the MBAM2.0 infrastructure.</span></span> <span data-ttu-id="79b63-106">Вам не нужно удалять базы данных.</span><span class="sxs-lookup"><span data-stu-id="79b63-106">You do not have to remove the databases.</span></span> <span data-ttu-id="79b63-107">После удаления сервера MBAM 1,0 базы данных MBAM остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="79b63-107">Uninstalling the MBAM 1.0 Server leaves the MBAM databases intact.</span></span> <span data-ttu-id="79b63-108">Если указаны те же базы данных, что и MBAM 1,0, установка MBAM 2.0 сохраняет данные MBAM 1,0 в базах данных и преобразует базы данных в MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="79b63-108">If you specify the same databases that MBAM 1.0 was using, the MBAM2.0 installation retains MBAM 1.0 data in the databases and converts the databases to work with MBAM2.0.</span></span>

-   <span data-ttu-id="79b63-109">**Обновление распределенного клиента** — если вы используете автономную топологию MBAM, вы можете сразу обновить клиенты MBAM после установки инфраструктуры сервера MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="79b63-109">**Distributed Client Upgrade** - If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 Server infrastructure.</span></span> <span data-ttu-id="79b63-110">Сервер MBAM 2,0 определяет версию существующего клиента и выполняет необходимые действия по обновлению до клиента 2,0.</span><span class="sxs-lookup"><span data-stu-id="79b63-110">The MBAM 2.0 Server detects the version of the existing Client and performs the required steps to upgrade to the 2.0 Client.</span></span>

    <span data-ttu-id="79b63-111">После обновления инфраструктуры сервера MBAM 2,0 клиенты MBAM 1,0 продолжают сообщать об этом на сервер MBAM 2,0, использующий данные для восстановления, но соответствие требованиям будет основываться на политиках в MBAM 1,0.</span><span class="sxs-lookup"><span data-stu-id="79b63-111">After you upgrade the MBAM 2.0 Server infrastructure, MBAM 1.0 Clients continue to report to the MBAM 2.0 Server successfully, escrowing recovery data, but compliance will be based on the policies in MBAM 1.0.</span></span> <span data-ttu-id="79b63-112">Чтобы клиентские компьютеры MBAM на соответствие требованиям политик MBAM 2,0, необходимо обновить клиенты до версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="79b63-112">You must upgrade clients to MBAM 2.0 to have client computers accurately report compliance against the MBAM 2.0 policies.</span></span> <span data-ttu-id="79b63-113">Вы можете обновить клиентские компьютеры до MBAM 2,0 без удаления прежнего клиента, после чего клиент начнет применять и сообщать о политиках MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="79b63-113">You can upgrade the clients to the MBAM 2.0 Client without uninstalling the previous client, and the client will start to apply and report MBAM 2.0 policies.</span></span>

    <span data-ttu-id="79b63-114">Если вы используете MBAM с Configuration Manager, вы должны обновить клиенты MBAM 1,0 до MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="79b63-114">If you are using MBAM with Configuration Manager, you must upgrade the MBAM 1.0 clients to MBAM 2.0.</span></span>

## <span data-ttu-id="79b63-115">Обновление MBAM из двух-серверной архитектуры</span><span class="sxs-lookup"><span data-stu-id="79b63-115">Upgrading MBAM from a Two-Server Architecture</span></span>


<span data-ttu-id="79b63-116">Выполните указанные ниже инструкции, чтобы обновить предыдущую версию MBAM при использовании архитектуры из двух серверов, где на одном сервере размещены компоненты Microsoft SQL Server, и на другом сервере размещены веб-сайты и службы.</span><span class="sxs-lookup"><span data-stu-id="79b63-116">Use the following instructions to upgrade from a previous version of MBAM when you are using a two-server architecture, where one server is hosting the Microsoft SQL Server components, and the other server is hosting the websites and services.</span></span>

**<span data-ttu-id="79b63-117">Обновление MBAM с помощью архитектуры из двух серверов</span><span class="sxs-lookup"><span data-stu-id="79b63-117">To upgrade MBAM from a two-server architecture</span></span>**

1.  <span data-ttu-id="79b63-118">На сервере с возможностями SQL Server на панели управления выберите пункт **программы и компоненты**, а затем удалите **Администрирование и мониторинг Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="79b63-118">On the server with the SQL Server features, in Control Panel, select **Programs and Features**, and then uninstall **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="79b63-119">База данных восстановления и база данных соответствия и аудита остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="79b63-119">The Recovery Database and Compliance and Audit database remain unchanged.</span></span>

2.  <span data-ttu-id="79b63-120">Запустите **MBAMSetup.exe** для версии MBAM 2,0, при необходимости выберите **программу улучшения качества программного**обеспечения, а затем нажмите кнопку **начать**.</span><span class="sxs-lookup"><span data-stu-id="79b63-120">Run **MBAMSetup.exe** for version MBAM 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="79b63-121">Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="79b63-121">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="79b63-122">На странице **Выбор топологии** выберите **изолированную** топологию **интеграции с System Center Configuration Manager** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-122">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="79b63-123">На странице **Выбор устанавливаемых компонентов** снимите флажок **сервер самообслуживания** , сервер **администрирования и мониторинг** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-123">On the **Select features to install** page, clear the **Self-Service Server** and **Administration and Monitoring Server** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="79b63-124">Дождитесь завершения проверок готовности к установке и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-124">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="79b63-125">Если обнаружен отсутствующий предварительный компонент, устраните недостающие необходимые условия и нажмите кнопку **проверить необходимые компоненты еще раз**.</span><span class="sxs-lookup"><span data-stu-id="79b63-125">If a missing prerequisite is detected, resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="79b63-126">На странице **Предоставление учетной записи, используемой для доступа к базам данных MBAM** укажите имя компьютера для сервера, на котором будут размещены сайты и службы, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-126">On the **Provide account used to access the MBAM databases** page, provide the computer name for the server that will host the sites and services, and then click **Next**.</span></span>

8.  <span data-ttu-id="79b63-127">На странице **Настройка базы данных восстановления** укажите имя экземпляра SQL Server и имя базы данных, в которой будут храниться данные для восстановления.</span><span class="sxs-lookup"><span data-stu-id="79b63-127">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="79b63-128">Кроме того, необходимо указать, где будут храниться файлы базы данных и данные журнала.</span><span class="sxs-lookup"><span data-stu-id="79b63-128">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="79b63-129">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-129">Click **Next** to continue.</span></span>

10. <span data-ttu-id="79b63-130">На странице **Настройка базы данных соответствия и аудита** укажите имя экземпляра SQL Server и имя базы данных, в которой будут храниться сведения о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="79b63-130">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span>

11. <span data-ttu-id="79b63-131">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-131">Click **Next** to continue.</span></span>

12. <span data-ttu-id="79b63-132">На странице " **Настройка отчетов о соответствии и аудите** " укажите экземпляр служб SQL Server Reporting Services, на котором будут установлены отчеты о соответствии и аудите, а также укажите учетную запись пользователя домена и пароль для доступа к базе данных "соответствие требованиям" и "Аудит".</span><span class="sxs-lookup"><span data-stu-id="79b63-132">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password to access the Compliance and Audit database.</span></span> <span data-ttu-id="79b63-133">Настройка пароля для этой учетной записи бессрочна.</span><span class="sxs-lookup"><span data-stu-id="79b63-133">Configure the password for this account to never expire.</span></span> <span data-ttu-id="79b63-134">Учетная запись пользователя может получать доступ ко всем данным, доступным для группы "Пользователи отчетов MBAM".</span><span class="sxs-lookup"><span data-stu-id="79b63-134">The user account can access all data available to the MBAM Reports Users group.</span></span>

13. <span data-ttu-id="79b63-135">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-135">Click **Next** to continue.</span></span>

14. <span data-ttu-id="79b63-136">Укажите, следует ли использовать обновления Microsoft, чтобы обеспечить безопасность компьютера, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-136">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="79b63-137">При этом автоматические обновления в Windows не активируются.</span><span class="sxs-lookup"><span data-stu-id="79b63-137">This does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="79b63-138">Если ранее вы выбрали использование центра обновления Майкрософт для этого продукта или другого продукта, страница центра обновления Майкрософт не отображается.</span><span class="sxs-lookup"><span data-stu-id="79b63-138">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

15. <span data-ttu-id="79b63-139">На странице **Сводка по установке** просмотрите компоненты, которые будут установлены, и нажмите кнопку **установить** , чтобы начать установку.</span><span class="sxs-lookup"><span data-stu-id="79b63-139">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

**<span data-ttu-id="79b63-140">Удаление компонентов сервера администрирования и мониторинга и завершение обновления</span><span class="sxs-lookup"><span data-stu-id="79b63-140">To uninstall the Administration and Monitoring Server features and to complete the upgrade</span></span>**

1.  <span data-ttu-id="79b63-141">На компьютере, на котором размещены компоненты сервера администрирования и мониторинга, на панели управления выберите пункт **программы и компоненты**и удалите MBAM, чтобы удалить ранее установленные веб-сайты и службы.</span><span class="sxs-lookup"><span data-stu-id="79b63-141">On the computer that hosts the Administration and Monitoring Server features, in Control Panel, select **Programs and Features**, and then uninstall MBAM to remove the previously installed websites and services.</span></span>

2.  <span data-ttu-id="79b63-142">Запустите **MBAMSetup.exe** для версии 2,0, при необходимости выберите **программу улучшения качества программного**обеспечения, а затем нажмите кнопку **начать**.</span><span class="sxs-lookup"><span data-stu-id="79b63-142">Run the **MBAMSetup.exe** for version 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="79b63-143">Прочтите и подтвердите условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, а затем нажмите кнопку **Далее** , чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="79b63-143">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="79b63-144">На странице **Выбор топологии** выберите **изолированную** топологию **интеграции с System Center Configuration Manager** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-144">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="79b63-145">На странице **выберите компоненты для установки** снимите флажки **база данных восстановления** , **базы данных соответствия требованиям** и функции проверки соответствия и **аудита** , а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-145">On the **Select features to install** page, clear the **Recovery Database** and **Compliance and Audit Database** and **Compliance and Audit Reports** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="79b63-146">Дождитесь завершения проверок готовности к установке и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-146">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="79b63-147">Если обнаружен отсутствующий предварительный компонент, сначала устраните недостающие предварительные требования, а затем нажмите кнопку **проверить необходимые компоненты еще раз**.</span><span class="sxs-lookup"><span data-stu-id="79b63-147">If a missing prerequisite is detected, resolve the missing prerequisites first, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="79b63-148">На странице **Настройка безопасности сетевых подключений** укажите, следует ли использовать шифрование SSL для веб-сайтов и служб.</span><span class="sxs-lookup"><span data-stu-id="79b63-148">On the **Configure network communication security** page, choose whether to use Secure Socket Layer (SSL) encryption for the websites and services.</span></span> <span data-ttu-id="79b63-149">Если вы решили зашифровать связь, выберите сертификат центра сертификации (ЦС), который будет использоваться для шифрования.</span><span class="sxs-lookup"><span data-stu-id="79b63-149">If you decide to encrypt the communication, select the certification authority (CA) certificate to use for encryption.</span></span>

    <span data-ttu-id="79b63-150">**Примечание**  Прежде чем этот шаг можно будет выбрать на этой странице, вы должны создать сертификат, прежде чем это сделать.</span><span class="sxs-lookup"><span data-stu-id="79b63-150">**Note** The certificate must be created before this step to enable you to select it on this page.</span></span>

     

8.  <span data-ttu-id="79b63-151">На странице **Настройка расположения базы данных о состоянии соответствия требованиям** укажите имя экземпляра SQL Server и имя базы данных, в которой хранятся данные о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="79b63-151">On the **Configure the location of the Compliance Status database** page, specify the SQL Server instance name and the name of the database that stores the compliance and audit data.</span></span> <span data-ttu-id="79b63-152">Кроме того, необходимо указать, где будут храниться файлы базы данных и данные журнала.</span><span class="sxs-lookup"><span data-stu-id="79b63-152">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="79b63-153">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-153">Click **Next** to continue.</span></span>

10. <span data-ttu-id="79b63-154">В разделе **Настройка расположения на странице базы данных восстановления** укажите имя экземпляра SQL Server и имя базы данных, в которой хранятся данные для восстановления.</span><span class="sxs-lookup"><span data-stu-id="79b63-154">On the **Configure the location of the Recovery Database** page, specify the SQL Server instance name and the name of the database that stores the recovery data.</span></span>

11. <span data-ttu-id="79b63-155">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-155">Click **Next** to continue.</span></span>

12. <span data-ttu-id="79b63-156">На странице **Настройка отчетов о соответствии и аудите** введите URL-адрес экземпляра отчета, настроенного на другом сервере.</span><span class="sxs-lookup"><span data-stu-id="79b63-156">On the **Configure the Compliance and Audit Reports** page, enter the URL for the reporting instance that you configured on the other server.</span></span> <span data-ttu-id="79b63-157">С помощью кнопки " **тест** " убедитесь, что сайт доступен.</span><span class="sxs-lookup"><span data-stu-id="79b63-157">Use the **Test** button to verify that you can reach the site.</span></span>

13. <span data-ttu-id="79b63-158">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-158">Click **Next** to continue.</span></span>

14. <span data-ttu-id="79b63-159">На странице **Настройка портала самообслуживания** введите номер порта, имя узла, имя виртуального каталога и путь установки для портала самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="79b63-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    <span data-ttu-id="79b63-160">**Примечание**  Номер порта, который вы указали, должен быть неиспользуемым номеру на сервере администрирования и мониторинга, если не указано уникальное имя заголовка узла.</span><span class="sxs-lookup"><span data-stu-id="79b63-160">**Note** The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span>

     

15. <span data-ttu-id="79b63-161">На странице **Настройка сервера администрирования и мониторинга** укажите нужный виртуальный каталог для веб-сайта службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="79b63-161">On the **Configure the Administration and Monitoring Server** page, specify the desired virtual directory for the Help Desk website.</span></span>

16. <span data-ttu-id="79b63-162">Укажите, следует ли использовать обновления Microsoft, чтобы обеспечить безопасность компьютера, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="79b63-162">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="79b63-163">На этом этапе не включается функция автоматического обновления в Windows.</span><span class="sxs-lookup"><span data-stu-id="79b63-163">This step does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="79b63-164">Если ранее вы выбрали использование центра обновления Майкрософт для этого продукта или другого продукта, страница центра обновления Майкрософт не отображается.</span><span class="sxs-lookup"><span data-stu-id="79b63-164">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

17. <span data-ttu-id="79b63-165">На странице **Сводка по установке** просмотрите компоненты, которые будут установлены, и нажмите кнопку **установить** , чтобы начать установку.</span><span class="sxs-lookup"><span data-stu-id="79b63-165">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

18. <span data-ttu-id="79b63-166">Чтобы убедиться в том, что обновление прошло успешно, убедитесь, что вы можете подключиться к каждому сайту с другого компьютера домена.</span><span class="sxs-lookup"><span data-stu-id="79b63-166">To validate that the upgrade was successful, verify that you can reach each site from another computer in the domain.</span></span>

## <span data-ttu-id="79b63-167">Обновление клиента MBAM на компьютерах конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="79b63-167">Upgrading the MBAM Client on End-User Computers</span></span>


<span data-ttu-id="79b63-168">Чтобы обновить компьютеры конечных пользователей до клиента MBAM 2,0, запустите **MbamClientSetup.exe** на каждом клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="79b63-168">To upgrade end-user computers to the MBAM 2.0 Client, run **MbamClientSetup.exe** on each client computer.</span></span> <span data-ttu-id="79b63-169">Установщик автоматически обновляет клиент для клиента MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="79b63-169">The installer automatically updates the Client to the MBAM 2.0 Client.</span></span> <span data-ttu-id="79b63-170">Вы можете установить клиент MBAM через электронную систему распространения программного обеспечения, такие инструменты, как доменные службы Active Directory или System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="79b63-170">You can install the MBAM Client through an electronic software distribution system, tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>

<span data-ttu-id="79b63-171">Чтобы проверить обновление клиента, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="79b63-171">To validate the Client upgrade, do the following:</span></span>

1.  <span data-ttu-id="79b63-172">Дождитесь завершения настроенного цикла создания отчета, а затем запустите **SQL Server Management Studio** на компьютере SQL Server.</span><span class="sxs-lookup"><span data-stu-id="79b63-172">Wait until the configured reporting cycle is finished, and then start **SQL Server Management Studio** on the SQL Server computer.</span></span>

2.  <span data-ttu-id="79b63-173">На компьютере SQL Server запустите **Microsoft SQL Server Management Studio**.</span><span class="sxs-lookup"><span data-stu-id="79b63-173">On the SQL Server computer, start **SQL Server Management Studio**.</span></span>

3.  <span data-ttu-id="79b63-174">Убедитесь, что в таблице **RecoveryAndHardwareCore.** Computers указана строка, в которой указано имя компьютера конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="79b63-174">Verify that the **RecoveryAndHardwareCore.Machines** table contains a row that shows the end-user’s computer name.</span></span>

## <span data-ttu-id="79b63-175">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="79b63-175">Related topics</span></span>


[<span data-ttu-id="79b63-176">Развертывание MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="79b63-176">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





