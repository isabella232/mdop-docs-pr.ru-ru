---
title: Настройка отчетов MBAM 2.5
description: Настройка отчетов MBAM 2.5
author: dansimp
ms.assetid: ec462879-0253-4d9c-83c7-a9bcad479725
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b372bd6bc38a3729aef43354ecf19b2619b7856
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826619"
---
# <span data-ttu-id="20415-103">Настройка отчетов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="20415-103">How to Configure the MBAM 2.5 Reports</span></span>


<span data-ttu-id="20415-104">В этой статье объясняется, как настроить функцию отчетов администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5 с помощью:</span><span class="sxs-lookup"><span data-stu-id="20415-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Reports feature by using:</span></span>

-   <span data-ttu-id="20415-105">Командлет Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="20415-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="20415-106">Мастер настройки сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="20415-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="20415-107">Инструкции основываются на рекомендованной архитектуре на [высоком уровне архитектуры для MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="20415-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="20415-108">Прежде чем приступить к настройке, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="20415-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="20415-109">Шаг</span><span class="sxs-lookup"><span data-stu-id="20415-109">Step</span></span></th>
<th align="left"><span data-ttu-id="20415-110">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="20415-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="20415-111">Изучите рекомендованную архитектуру для MBAM.</span><span class="sxs-lookup"><span data-stu-id="20415-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="20415-112">Высокоуровневая архитектура для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="20415-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="20415-113">Проверка поддерживаемых конфигураций для MBAM.</span><span class="sxs-lookup"><span data-stu-id="20415-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="20415-114">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="20415-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="20415-115">Заполните необходимые условия на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="20415-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="20415-116">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="20415-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="20415-117">Требования к серверу MBAM 2,5, применимые только к топологии интеграции Configuration Manager </a> (если применимо)</span><span class="sxs-lookup"><span data-stu-id="20415-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="20415-118">Установите серверное программное обеспечение MBAM на каждый сервер, на котором вы планируете настроить компонент MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="20415-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="20415-119">Установка программного обеспечения MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="20415-119">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="20415-120">Если вы планируете использовать командлеты Windows PowerShell для настройки функций сервера MBAM, изучите необходимые условия для использования Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="20415-120">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="20415-121">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="20415-121">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="20415-122">Настройка отчетов с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="20415-122">To configure the Reports by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="20415-123">Прежде чем приступить к настройке, прочтите раздел [Настройка функций сервера MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) , чтобы просмотреть предварительные требования для использования Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="20415-123">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="20415-124">С помощью командлета Windows PowerShell **Enable-MbamReport** можно настроить отчеты.</span><span class="sxs-lookup"><span data-stu-id="20415-124">Use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="20415-125">Чтобы получить сведения об этом командлете Windows PowerShell, введите **Get-Help Enable-MbamReport**.</span><span class="sxs-lookup"><span data-stu-id="20415-125">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamReport**.</span></span>

**<span data-ttu-id="20415-126">Настройка отчетов с помощью мастера</span><span class="sxs-lookup"><span data-stu-id="20415-126">To configure the Reports by using the wizard</span></span>**

1. <span data-ttu-id="20415-127">На сервере, на котором вы хотите настроить отчеты, запустите мастер **настройки сервера MBAM** .</span><span class="sxs-lookup"><span data-stu-id="20415-127">On the server where you want to configure the Reports, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="20415-128">Чтобы открыть мастер, вы можете выбрать **MBAM конфигурации сервера** в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="20415-128">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="20415-129">Нажмите кнопку **Добавить новые функции**, выберите пункт **отчеты**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="20415-129">Click **Add New Features**, select **Reports**, and then click **Next**.</span></span> <span data-ttu-id="20415-130">Мастер проверяет, выполнены ли все необходимые условия для отчетов.</span><span class="sxs-lookup"><span data-stu-id="20415-130">The wizard checks that all prerequisites for the Reports have been met.</span></span>

3. <span data-ttu-id="20415-131">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="20415-131">Click **Next** to continue.</span></span>

4. <span data-ttu-id="20415-132">Введите значения полей в мастере, используя следующие описания:</span><span class="sxs-lookup"><span data-stu-id="20415-132">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="20415-133">Поле</span><span class="sxs-lookup"><span data-stu-id="20415-133">Field</span></span></th>
   <th align="left"><span data-ttu-id="20415-134">Описание</span><span class="sxs-lookup"><span data-stu-id="20415-134">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="20415-135">Экземпляр служб SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="20415-135">SQL Server Reporting Services instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="20415-136">Экземпляр служб SQL Server Reporting Services, в котором будут настраиваться отчеты.</span><span class="sxs-lookup"><span data-stu-id="20415-136">Instance of SQL Server Reporting Services where the Reports will be configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="20415-137">Группа домена "роль отчета"</span><span class="sxs-lookup"><span data-stu-id="20415-137">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="20415-138">Имя группы "Пользователи домена", у участников которой есть права на доступ к отчетам на сервере администрирования и мониторинга.</span><span class="sxs-lookup"><span data-stu-id="20415-138">Name of the domain Users group whose members have rights to access the reports on the Administration and Monitoring Server.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="20415-139">Имя сервера SQL Server</span><span class="sxs-lookup"><span data-stu-id="20415-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="20415-140">Имя сервера, на котором настроена база данных соответствия и аудита.</span><span class="sxs-lookup"><span data-stu-id="20415-140">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="20415-141">Экземпляр базы данных SQL Server</span><span class="sxs-lookup"><span data-stu-id="20415-141">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="20415-142">Имя экземпляра SQL Server (например, <em> MSSQLServer </em> ), на котором настроена база данных соответствия и аудита.</span><span class="sxs-lookup"><span data-stu-id="20415-142">Name of the instance of SQL Server (for example, <em>MSSQLSERVER</em>) where the Compliance and Audit Database is configured.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="20415-143">Примечание.</span><span class="sxs-lookup"><span data-stu-id="20415-143">Note</span></span></strong><br/><p><span data-ttu-id="20415-144">Чтобы включить входящий трафик для порта сервера отчетов, необходимо добавить на компьютере с отчетом исключение для входящего трафика (порт по умолчанию — 80).</span><span class="sxs-lookup"><span data-stu-id="20415-144">You must add an exception on the Reports computer to enable inbound traffic on the port of the Reporting Server (the default port is 80).</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="20415-145">Имя базы данных</span><span class="sxs-lookup"><span data-stu-id="20415-145">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="20415-146">Имя базы данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="20415-146">Name of the Compliance and Audit Database.</span></span> <span data-ttu-id="20415-147">По умолчанию имя базы данных имеет <strong> состояние соответствия MBAM </strong> , но вы можете изменить его при настройке базы данных "соответствие" и "Аудит".</span><span class="sxs-lookup"><span data-stu-id="20415-147">By default, the database name is <strong>MBAM Compliance Status</strong>, although you can change the name when you configure the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="20415-148">Примечание.</span><span class="sxs-lookup"><span data-stu-id="20415-148">Note</span></span></strong><br/><p><span data-ttu-id="20415-149">Если вы обновляете предыдущую версию MBAM, вы должны использовать имя базы данных, совпадающее с именем, используемым в предыдущем развертывании.</span><span class="sxs-lookup"><span data-stu-id="20415-149">If you are upgrading from a previous version of MBAM, you must use the same database name as the name used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="20415-150">Учетная запись домена базы данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="20415-150">Compliance and Audit Database domain account</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="20415-151">Учетная запись пользователя домена и пароль для доступа к базе данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="20415-151">Domain user account and password to access the Compliance and Audit Database.</span></span></p>
   <p><span data-ttu-id="20415-152">Если значение, введенное в <strong> поле пользователя или группы домена "доступ только для чтения" </strong> на <strong> странице "Настройка баз данных" </strong> , является пользователем, необходимо указать это же значение в этом поле.</span><span class="sxs-lookup"><span data-stu-id="20415-152">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="20415-153">Если значение, введенное в <strong> поле пользователя или группы домена "доступ только для чтения" </strong> на <strong> странице "Настройка баз данных" </strong> , является группой, значение, введенное в этом поле, должно быть членом этой группы.</span><span class="sxs-lookup"><span data-stu-id="20415-153">If the value that you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group, the value that you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="20415-154">Настройка пароля для этой учетной записи бессрочна.</span><span class="sxs-lookup"><span data-stu-id="20415-154">Configure the password for this account to never expire.</span></span> <span data-ttu-id="20415-155">Учетная запись пользователя должна иметь доступ ко всем данным, доступным группе "Пользователи отчетов MBAM".</span><span class="sxs-lookup"><span data-stu-id="20415-155">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="20415-156">Когда вы закончите ввод, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="20415-156">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="20415-157">Мастер проверяет, выполнены ли все необходимые условия для функции "отчеты".</span><span class="sxs-lookup"><span data-stu-id="20415-157">The wizard checks that all prerequisites for the Reports feature have been met.</span></span>

6. <span data-ttu-id="20415-158">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="20415-158">Click **Next** to continue.</span></span>

7. <span data-ttu-id="20415-159">На странице **сводки** ознакомьтесь с возможностями, которые будут добавлены.</span><span class="sxs-lookup"><span data-stu-id="20415-159">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="20415-160">Примечание.</span><span class="sxs-lookup"><span data-stu-id="20415-160">Note</span></span>**  
   <span data-ttu-id="20415-161">Чтобы создать сценарий Windows PowerShell для записей, которые вы только что сделали, нажмите **экспортировать сценарий PowerShell**, а затем сохраните сценарий.</span><span class="sxs-lookup"><span data-stu-id="20415-161">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



8. <span data-ttu-id="20415-162">Нажмите кнопку **Добавить** , чтобы добавить отчеты на сервер, а затем нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="20415-162">Click **Add** to add the Reports on the server, and then click **Close**.</span></span>



## <span data-ttu-id="20415-163">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="20415-163">Related topics</span></span>


[<span data-ttu-id="20415-164">Журналы событий сервера</span><span class="sxs-lookup"><span data-stu-id="20415-164">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="20415-165">Настройка компонентов сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="20415-165">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="20415-166">Настройка веб-приложений MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="20415-166">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="20415-167">Проверка конфигурации компонентов MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="20415-167">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="20415-168">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="20415-168">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="20415-169">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="20415-169">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="20415-170">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="20415-170">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






