---
title: Проверка конфигурации компонентов MBAM 2.5 Server
description: Проверка конфигурации компонентов MBAM 2.5 Server
author: dansimp
ms.assetid: f4983a33-ce18-4186-a471-dd6415940504
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f955e0b9ccb7952995574e4aa981674f7c7667fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827082"
---
# <span data-ttu-id="31ebd-103">Проверка конфигурации компонентов MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="31ebd-103">Validating the MBAM 2.5 Server Feature Configuration</span></span>


<span data-ttu-id="31ebd-104">Когда вы закончите развертывание компонентов сервера Microsoft BitLocker (MBAM) 2,5, мы рекомендуем проверить развертывание, чтобы убедиться, что все возможности успешно настроены.</span><span class="sxs-lookup"><span data-stu-id="31ebd-104">When you finish the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server feature deployment, we recommend that you validate the deployment to ensure that all features have been successfully configured.</span></span> <span data-ttu-id="31ebd-105">Используйте процедуру, соответствующую топологии (отдельное интегрированное приложение или интеграция System Center Configuration Manager), которое вы развернули.</span><span class="sxs-lookup"><span data-stu-id="31ebd-105">Use the procedure that matches the topology (Stand-alone or System Center Configuration Manager Integration) that you deployed.</span></span>

## <span data-ttu-id="31ebd-106">Проверка развертывания сервера MBAM с использованием изолированной топологии</span><span class="sxs-lookup"><span data-stu-id="31ebd-106">Validating the MBAM Server deployment with the Stand-alone topology</span></span>


<span data-ttu-id="31ebd-107">Выполните указанные ниже действия, чтобы проверить развертывание сервера MBAM с помощью изолированной топологии.</span><span class="sxs-lookup"><span data-stu-id="31ebd-107">Use the following steps to validate your MBAM Server deployment with the Stand-alone topology.</span></span>

**<span data-ttu-id="31ebd-108">Проверка развертывания отдельного сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="31ebd-108">To validate a Stand-alone MBAM Server deployment</span></span>**

1.  <span data-ttu-id="31ebd-109">На каждом сервере, на котором развернута функция MBAM **Control Panel** , выберите пункт &gt; **программы** &gt; **и компоненты**панели управления.</span><span class="sxs-lookup"><span data-stu-id="31ebd-109">On each server where an MBAM feature is deployed, click **Control Panel** &gt; **Programs** &gt; **Programs and Features**.</span></span> <span data-ttu-id="31ebd-110">Убедитесь в том, что в списке **программы и компоненты** отображается элемент **Администрирование и мониторинг Microsoft BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="31ebd-110">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

    **<span data-ttu-id="31ebd-111">Примечание.</span><span class="sxs-lookup"><span data-stu-id="31ebd-111">Note</span></span>**  
    <span data-ttu-id="31ebd-112">Для проверки необходимо использовать учетную запись домена, которая содержит учетные данные администратора локального компьютера на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="31ebd-112">To do the validation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="31ebd-113">На сервере, на котором настроена база данных восстановления, откройте центр управления SQL Server Management Studio и убедитесь, что настройка **восстановления MBAM и** базы данных оборудования.</span><span class="sxs-lookup"><span data-stu-id="31ebd-113">On the server where the Recovery Database is configured, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is configured.</span></span>

3.  <span data-ttu-id="31ebd-114">На сервере, на котором настроена база данных соответствия и аудита, откройте центр SQL Server Management Studio и убедитесь в том, что **база данных состояния соответствия MBAM** настроена.</span><span class="sxs-lookup"><span data-stu-id="31ebd-114">On the server where the Compliance and Audit Database is configured, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is configured.</span></span>

4.  <span data-ttu-id="31ebd-115">На сервере, на котором настроена функция отчеты, откройте веб-браузер с учетными данными администратора и перейдите на сайт "Главная" на сайте служб SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="31ebd-115">On the server where the Reports feature is configured, open a web browser with administrative credentials and browse to the "Home" of the SQL Server Reporting Services site.</span></span>

    <span data-ttu-id="31ebd-116">Расположение по умолчанию для экземпляра сервера служб SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="31ebd-116">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

    <span data-ttu-id="31ebd-117">HTTP (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *Port* &gt; /Reports.aspx</span><span class="sxs-lookup"><span data-stu-id="31ebd-117">http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports.aspx</span></span>

    <span data-ttu-id="31ebd-118">Чтобы найти фактический URL-адрес, используйте Диспетчер конфигураций служб Reporting Services и выберите экземпляры, заданные во время настройки.</span><span class="sxs-lookup"><span data-stu-id="31ebd-118">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that you specified during setup.</span></span>

5.  <span data-ttu-id="31ebd-119">Убедитесь в том, что в папке Reporting ( **Администрирование и мониторинг) Microsoft BitLocker** есть источник данных, именуемый **MaltaDataSource** , а также языковые папки.</span><span class="sxs-lookup"><span data-stu-id="31ebd-119">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** as well as the language folders.</span></span> <span data-ttu-id="31ebd-120">Источник данных включает папки с именами, представляющими языки (например, EN-US).</span><span class="sxs-lookup"><span data-stu-id="31ebd-120">The data source contains folders with names that represent languages (for example, en-us).</span></span> <span data-ttu-id="31ebd-121">Отчеты находятся в папках языка.</span><span class="sxs-lookup"><span data-stu-id="31ebd-121">The reports are in the language folders.</span></span>

    **<span data-ttu-id="31ebd-122">Примечание.</span><span class="sxs-lookup"><span data-stu-id="31ebd-122">Note</span></span>**  
    <span data-ttu-id="31ebd-123">Если службы отчетов SQL Server (SSRS) были настроены как именованный экземпляр, URL-адрес должен выглядеть следующим образом: HTTP (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *Port* &gt; /Reports\_ &lt; *SSRSInstanceName*&gt;</span><span class="sxs-lookup"><span data-stu-id="31ebd-123">If SQL Server Reporting Services (SSRS) was configured as a named instance, the URL should resemble the following: http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports\_&lt;*SSRSInstanceName*&gt;</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring Website (also known as Help Desk) and select a report, the following message appears: "Only Secure Content is Displayed." To show the report, click **Show All Content**.
~~~



6. <span data-ttu-id="31ebd-124">На сервере, на котором настроена функция администрирования и веб-сайта мониторинга, запустите **Диспетчер серверов**, перейдите к пункту **роли**и выберите пункт **веб-сервер (IIS)** &gt; **Manager (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="31ebd-124">On the server where the Administration and Monitoring Website feature is configured, run **Server Manager**, browse to **Roles**, and then select **Web Server (IIS)** &gt; **Internet Information Services (IIS) Manager**.</span></span>

7. <span data-ttu-id="31ebd-125">В окне **подключения**найдите \* &lt; &gt; имя компьютера\* и выберите пункт **сайты** , &gt; **Администрирование и мониторинг Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="31ebd-125">In **Connections**, browse to *&lt;computer name&gt;* and select **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="31ebd-126">Убедитесь в том, что указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="31ebd-126">Verify that the following are listed:</span></span>

   -   **<span data-ttu-id="31ebd-127">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="31ebd-127">MBAMAdministrationService</span></span>**

   -   **<span data-ttu-id="31ebd-128">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="31ebd-128">MBAMComplianceStatusService</span></span>**

   -   **<span data-ttu-id="31ebd-129">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="31ebd-129">MBAMRecoveryAndHardwareService</span></span>**

8. <span data-ttu-id="31ebd-130">На сервере, на котором настроен портал администрирования и веб-сайт для мониторинга и самообслуживания, откройте веб-браузер с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="31ebd-130">On the server where the Administration and Monitoring Website and Self-Service Portal are configured, open a web browser with administrative credentials.</span></span>

9. <span data-ttu-id="31ebd-131">Перейдите на следующие веб-сайты, чтобы убедиться, что они успешно загружены.</span><span class="sxs-lookup"><span data-stu-id="31ebd-131">Browse to the following websites to verify that they load successfully:</span></span>

   -   <span data-ttu-id="31ebd-132">HTTPS (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /HelpDesk/-подтверждение каждой ссылки для навигации и отчетов</span><span class="sxs-lookup"><span data-stu-id="31ebd-132">https(s)://&lt;*MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/HelpDesk/ - confirm each of the links for navigation and reports</span></span>

   -   <span data-ttu-id="31ebd-133">HTTP (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /Selfservice/</span><span class="sxs-lookup"><span data-stu-id="31ebd-133">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/SelfService/</span></span>

   **<span data-ttu-id="31ebd-134">Примечание.</span><span class="sxs-lookup"><span data-stu-id="31ebd-134">Note</span></span>**  
   <span data-ttu-id="31ebd-135">Предполагается, что вы настроили компоненты сервера на порт по умолчанию без сетевого шифрования.</span><span class="sxs-lookup"><span data-stu-id="31ebd-135">It is assumed that you configured the server features on the default port without network encryption.</span></span> <span data-ttu-id="31ebd-136">Если вы настроили компоненты сервера на другом порте или виртуальном каталоге, измените URL-адреса таким образом, чтобы включить соответствующий порт, например:</span><span class="sxs-lookup"><span data-stu-id="31ebd-136">If you configured the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example:</span></span>

   <span data-ttu-id="31ebd-137">HTTP (s):// &lt; *имя узла* &gt; : &lt; *Port* &gt; /HelpDesk/</span><span class="sxs-lookup"><span data-stu-id="31ebd-137">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/HelpDesk/</span></span>

   <span data-ttu-id="31ebd-138">HTTP (s):// &lt; *имя узла* &gt; : &lt; *порт* &gt; / &lt; *виртуальный_каталог*&gt;/</span><span class="sxs-lookup"><span data-stu-id="31ebd-138">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/&lt;*virtualdirectory*&gt;/</span></span>

   <span data-ttu-id="31ebd-139">Если компоненты сервера настроены с помощью шифрования сети, измените http://на https://.</span><span class="sxs-lookup"><span data-stu-id="31ebd-139">If the server features were configured with network encryption, change http:// to https://.</span></span>



10. <span data-ttu-id="31ebd-140">Найдите следующие веб-службы, чтобы убедиться, что они успешно загружены.</span><span class="sxs-lookup"><span data-stu-id="31ebd-140">Browse to the following web services to verify that they load successfully.</span></span> <span data-ttu-id="31ebd-141">Откроется страница, указывающая на то, что служба запущена, но на ней не отображаются метаданные.</span><span class="sxs-lookup"><span data-stu-id="31ebd-141">A page opens to indicate that the service is running, but the page does not display any metadata.</span></span>

    -   <span data-ttu-id="31ebd-142">HTTP (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="31ebd-142">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>

    -   <span data-ttu-id="31ebd-143">HTTP (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /MBAMUserSupportService/UserSupportService.svc</span><span class="sxs-lookup"><span data-stu-id="31ebd-143">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>

    -   <span data-ttu-id="31ebd-144">HTTP (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="31ebd-144">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>

    -   <span data-ttu-id="31ebd-145">HTTP (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="31ebd-145">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>

## <span data-ttu-id="31ebd-146">Проверка развертывания сервера MBAM с помощью топологии интеграции Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="31ebd-146">Validating the MBAM Server deployment with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="31ebd-147">Выполните описанные ниже действия, чтобы проверить развертывание MBAM с помощью топологии интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="31ebd-147">Use the following steps to validate your MBAM deployment with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="31ebd-148">Выполните шаги проверки, соответствующие версии Configuration Manager, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="31ebd-148">Complete the validation steps that match the version of Configuration Manager that you are using.</span></span>

### <a href="" id="validating-the-mbam-server-deployment-with-system-center-2012-configuration-manager-"></a><span data-ttu-id="31ebd-149">Проверка развертывания сервера MBAM с помощью System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="31ebd-149">Validating the MBAM Server deployment with System Center 2012 Configuration Manager</span></span>

<span data-ttu-id="31ebd-150">Выполните следующие действия, чтобы проверить развертывание сервера MBAM, когда вы используете MBAM с System Center 2012 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="31ebd-150">Use these steps to validate your MBAM Server deployment when you are using MBAM with System Center 2012 Configuration Manager.</span></span>

**<span data-ttu-id="31ebd-151">Проверка интеграции Configuration Manager MBAM развертывание сервера — System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="31ebd-151">To validate a Configuration Manager Integration MBAM Server deployment – System Center 2012 Configuration Manager</span></span>**

1.  <span data-ttu-id="31ebd-152">На сервере, на котором развернут Диспетчер конфигураций System Center 2012, откройте меню **программы и компоненты** на **панели управления**и убедитесь, что появился **центр администрирования и наблюдения Microsoft BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="31ebd-152">On the server where System Center 2012 Configuration Manager is deployed, open **Programs and Features** in **Control Panel**, and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="31ebd-153">Примечание.</span><span class="sxs-lookup"><span data-stu-id="31ebd-153">Note</span></span>**  
    <span data-ttu-id="31ebd-154">Для проверки конфигурации необходимо использовать учетную запись домена, которая содержит учетные данные администратора локального компьютера на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="31ebd-154">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="31ebd-155">В консоли Configuration Manager щелкните коллекции ресурсов рабочей области " **ресурсы и соответствие требованиям** " &gt; **Device Collections**и убедитесь, что на экране появится новая коллекция с именем **MBAM поддерживаемые компьютеры** .</span><span class="sxs-lookup"><span data-stu-id="31ebd-155">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Device Collections**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="31ebd-156">На консоли Configuration Manager щелкните **Monitoring** &gt; **Reporting** &gt; **MBAM отчеты о** &gt; **MBAM**рабочей области "Мониторинг рабочих областей".</span><span class="sxs-lookup"><span data-stu-id="31ebd-156">In the Configuration Manager console, click the **Monitoring** workspace &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

4.  <span data-ttu-id="31ebd-157">Убедитесь в том, что папка **MBAM** имеет вложенные папки, имена которых представляют разные языки, а также в том, что в каждой вложенной папке указаны следующие отчеты:</span><span class="sxs-lookup"><span data-stu-id="31ebd-157">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="31ebd-158">Соответствие требованиям компьютера BitLocker</span><span class="sxs-lookup"><span data-stu-id="31ebd-158">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="31ebd-159">Панель мониторинга соответствия требованиям для предприятия BitLocker</span><span class="sxs-lookup"><span data-stu-id="31ebd-159">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="31ebd-160">Сведения о соответствии требованиям BitLocker для предприятий</span><span class="sxs-lookup"><span data-stu-id="31ebd-160">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="31ebd-161">Сводка по соответствию требованиям для предприятий BitLocker</span><span class="sxs-lookup"><span data-stu-id="31ebd-161">BitLocker Enterprise Compliance Summary</span></span>

5.  <span data-ttu-id="31ebd-162">В консоли Configuration Manager выберите **основные ресурсы и** &gt; **базовые параметры соответствия** требованиям рабочей области &gt; **Configuration Baselines**, а также убедитесь, что в списке указана базовая **Защита BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="31ebd-162">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

6.  <span data-ttu-id="31ebd-163">В консоли Configuration Manager выберите элементы конфигурации параметры **соответствия ресурсов и рабочих областей соответствия требованиям** &gt; **Compliance Settings** &gt; **Configuration Items**и убедитесь, что отображаются следующие новые элементы конфигурации:</span><span class="sxs-lookup"><span data-stu-id="31ebd-163">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="31ebd-164">Защита фиксированных дисков с данными BitLocker</span><span class="sxs-lookup"><span data-stu-id="31ebd-164">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="31ebd-165">Защита диска операционной системы BitLocker</span><span class="sxs-lookup"><span data-stu-id="31ebd-165">BitLocker Operating System Drive Protection</span></span>

### <span data-ttu-id="31ebd-166">Проверка развертывания сервера MBAM с помощью Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="31ebd-166">Validating the MBAM Server deployment with Configuration Manager 2007</span></span>

<span data-ttu-id="31ebd-167">Выполните следующие действия, чтобы проверить развертывание сервера MBAM при использовании MBAM в Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="31ebd-167">Use these steps to validate your MBAM Server deployment when you are using MBAM with Configuration Manager 2007.</span></span>

**<span data-ttu-id="31ebd-168">Проверка интеграции Configuration Manager MBAM развертывание сервера — Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="31ebd-168">To validate a Configuration Manager Integration MBAM Server deployment – Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="31ebd-169">На сервере, на котором развернут Configuration Manager 2007, откройте меню **программы и компоненты** на **панели управления** и убедитесь, что отображается **Администрирование и мониторинг Microsoft BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="31ebd-169">On the server where Configuration Manager 2007 is deployed, open **Programs and Features** on **Control Panel** , and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="31ebd-170">Примечание.</span><span class="sxs-lookup"><span data-stu-id="31ebd-170">Note</span></span>**  
    <span data-ttu-id="31ebd-171">Для проверки конфигурации необходимо использовать учетную запись домена, которая содержит учетные данные администратора локального компьютера на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="31ebd-171">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="31ebd-172">На консоли Configuration Manager щелкните **база данных сайта &lt; SiteCode &gt;  -  &lt; ИмяСервера &gt; , &lt; SiteName &gt; ), Управление компьютером**и подтвердите, что отображается новая коллекция под названием **Поддерживаемые компьютеры, поддерживающие MBAM** .</span><span class="sxs-lookup"><span data-stu-id="31ebd-172">In the Configuration Manager console, click **Site Database &lt;SiteCode&gt; - &lt;ServerName&gt;, &lt;SiteName&gt;), Computer Management**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="31ebd-173">На консоли Configuration Manager выберите пункт **отчеты** о &gt; **службах** отчетов &gt; \*\* \\\\ &lt; ServerName &gt; \*\* &gt; **Report Folders** &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="31ebd-173">In the Configuration Manager console, click **Reporting** &gt; **Reporting Services** &gt; **\\\\&lt;ServerName&gt;** &gt; **Report Folders** &gt; **MBAM**.</span></span>

    <span data-ttu-id="31ebd-174">Убедитесь в том, что папка **MBAM** имеет вложенные папки, имена которых представляют разные языки, а также в том, что в каждой вложенной папке указаны следующие отчеты:</span><span class="sxs-lookup"><span data-stu-id="31ebd-174">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="31ebd-175">Соответствие требованиям компьютера BitLocker</span><span class="sxs-lookup"><span data-stu-id="31ebd-175">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="31ebd-176">Панель мониторинга соответствия требованиям для предприятия BitLocker</span><span class="sxs-lookup"><span data-stu-id="31ebd-176">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="31ebd-177">Сведения о соответствии требованиям BitLocker для предприятий</span><span class="sxs-lookup"><span data-stu-id="31ebd-177">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="31ebd-178">Сводка по соответствию требованиям для предприятий BitLocker</span><span class="sxs-lookup"><span data-stu-id="31ebd-178">BitLocker Enterprise Compliance Summary</span></span>

4.  <span data-ttu-id="31ebd-179">В консоли Configuration Manager щелкните базовые шаблоны для **управления требуемой конфигурацией** &gt; **Configuration Baselines**и убедитесь, что в списке указана базовая конфигурация **защиты BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="31ebd-179">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

5.  <span data-ttu-id="31ebd-180">На консоли Configuration Manager щелкните элементы конфигурации для **управления требуемой конфигурацией** &gt; **Configuration Items**и убедитесь, что отображаются следующие новые элементы конфигурации:</span><span class="sxs-lookup"><span data-stu-id="31ebd-180">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="31ebd-181">Защита фиксированных дисков с данными BitLocker</span><span class="sxs-lookup"><span data-stu-id="31ebd-181">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="31ebd-182">Защита диска операционной системы BitLocker</span><span class="sxs-lookup"><span data-stu-id="31ebd-182">BitLocker Operating System Drive Protection</span></span>



## <span data-ttu-id="31ebd-183">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="31ebd-183">Related topics</span></span>


[<span data-ttu-id="31ebd-184">Настройка компонентов сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="31ebd-184">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)


## <span data-ttu-id="31ebd-185">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="31ebd-185">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="31ebd-186">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="31ebd-186">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="31ebd-187">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="31ebd-187">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






