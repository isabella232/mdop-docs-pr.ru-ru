---
title: Планирование высокой доступности MBAM 2.5
description: Планирование высокой доступности MBAM 2.5
author: dansimp
ms.assetid: 1e29b30c-33f1-4a52-9442-8c1391f0049c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 20c304f669cfe9e1484be47dea1b9fcc917aea2c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826942"
---
# <span data-ttu-id="28ebe-103">Планирование высокой доступности MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="28ebe-103">Planning for MBAM 2.5 High Availability</span></span>


<span data-ttu-id="28ebe-104">Администрирование и мониторинг Microsoft BitLocker (MBAM) может обеспечивать высокий уровень доступности с помощью одной или нескольких из описанных ниже технологий, описанных в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="28ebe-104">Microsoft BitLocker Administration and Monitoring (MBAM) can maintain high availability through use of one or more of the following technologies, which are described in the following sections:</span></span>

-   [<span data-ttu-id="28ebe-105">Группы доступности SQL Server AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="28ebe-105">SQL Server AlwaysOn availability groups</span></span>](#bkmk-alwayson)

-   [<span data-ttu-id="28ebe-106">Кластеризация Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="28ebe-106">Microsoft SQL Server clustering</span></span>](#bkmk-sql-clustering)

-   [<span data-ttu-id="28ebe-107">Балансировка сетевой нагрузки IIS</span><span class="sxs-lookup"><span data-stu-id="28ebe-107">IIS Network Load Balancing</span></span>](#bkmk-load-balance)

-   [<span data-ttu-id="28ebe-108">Зеркальное отображение базы данных в SQL Server</span><span class="sxs-lookup"><span data-stu-id="28ebe-108">Database mirroring in SQL Server</span></span>](#bkmk-db-mirroring)

-   [<span data-ttu-id="28ebe-109">Резервное копирование баз данных MBAM с помощью службы теневого копирования томов (VSS)</span><span class="sxs-lookup"><span data-stu-id="28ebe-109">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>](#bkmk-vss)

<span data-ttu-id="28ebe-110">Сведения о том, как развернуть MBAM в конфигурации высокой доступности, можно найти в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="28ebe-110">Use the information in the following sections to help you understand the options to deploy MBAM in a highly available configuration.</span></span>

## <a href="" id="bkmk-alwayson"></a><span data-ttu-id="28ebe-111">Поддержка групп доступности SQL Server AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="28ebe-111">Support for SQL Server AlwaysOn availability groups</span></span>


<span data-ttu-id="28ebe-112">MBAM позволяет настраивать группы доступности баз данных и управлять ими в Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="28ebe-112">MBAM enables you to configure and manage availability groups for the databases in Microsoft SQL Server.</span></span> <span data-ttu-id="28ebe-113">Группа доступности для MBAM поддерживает отказоустойчивую среду, в которой база данных соответствия и аудита и база данных восстановления не переносятся вместе, а не отдельно.</span><span class="sxs-lookup"><span data-stu-id="28ebe-113">An availability group for MBAM supports a failover environment where the Compliance and Audit Database and the Recovery Database fail over together rather than separately.</span></span>

<span data-ttu-id="28ebe-114">Группа доступности поддерживает набор баз данных для чтения и записи и один из четырех наборов соответствующих баз данных-получателей.</span><span class="sxs-lookup"><span data-stu-id="28ebe-114">An availability group supports a set of read/write primary databases and one to four sets of corresponding secondary databases.</span></span> <span data-ttu-id="28ebe-115">Кроме того, дополнительные базы данных можно сделать доступными для разрешения только на чтение, некоторых операций резервного копирования или для обоих параметров.</span><span class="sxs-lookup"><span data-stu-id="28ebe-115">Optionally, secondary databases can be made available for read-only permission, some backup operations, or for both.</span></span>

<span data-ttu-id="28ebe-116">Сведения о настройке групп доступности можно найти в разделе [группы доступности AlwaysOn](https://go.microsoft.com/fwlink/?LinkId=393277).</span><span class="sxs-lookup"><span data-stu-id="28ebe-116">For information about how to set up availability groups, see [AlwaysOn Availability Groups](https://go.microsoft.com/fwlink/?LinkId=393277).</span></span>

## <a href="" id="bkmk-sql-clustering"></a><span data-ttu-id="28ebe-117">Кластеризация Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="28ebe-117">Microsoft SQL Server clustering</span></span>


<span data-ttu-id="28ebe-118">Базу данных проверки соответствия требованиям к MBAM 2,5 и базу данных для восстановления на компьютерах, на которых запущены кластеры SQL Server, можно выполнить.</span><span class="sxs-lookup"><span data-stu-id="28ebe-118">You can run the MBAM 2.5 Compliance and Audit Database and the Recovery Database on computers that are running SQL Server clusters.</span></span>

## <a href="" id="bkmk-load-balance"></a><span data-ttu-id="28ebe-119">Балансировка сетевой нагрузки IIS</span><span class="sxs-lookup"><span data-stu-id="28ebe-119">IIS Network Load Balancing</span></span>


<span data-ttu-id="28ebe-120">С помощью средства балансировки нагрузки сети можно настроить высокодоступную среду для компьютеров, на которых работает веб-сайт администрирования и мониторинга (также называемый службой поддержки), портал самообслуживания и веб-службы, которые развертываются с помощью служб IIS.</span><span class="sxs-lookup"><span data-stu-id="28ebe-120">You can use Network Load Balancing to configure a highly available environment for computers that are running the Administration and Monitoring Website (also known as Help Desk), the Self-Service Portal, and the web services, which are deployed through Internet Information Services (IIS).</span></span>

### <span data-ttu-id="28ebe-121">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="28ebe-121">Prerequisites</span></span>

<span data-ttu-id="28ebe-122">Перед настройкой балансировки нагрузки убедитесь, что выполнены следующие требования:</span><span class="sxs-lookup"><span data-stu-id="28ebe-122">Before configuring load balancing, ensure that you have met the following prerequisites:</span></span>

-   <span data-ttu-id="28ebe-123">Должна быть доступна подсистема балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="28ebe-123">A load balancer must be available.</span></span> <span data-ttu-id="28ebe-124">Вы можете использовать балансировщик нагрузки из Microsoft или другой компании.</span><span class="sxs-lookup"><span data-stu-id="28ebe-124">You can use load balancers from Microsoft or another company.</span></span> <span data-ttu-id="28ebe-125">Дополнительные сведения о технологии Microsoft балансировки нагрузки можно найти в разделе [Создание веб-фермы с помощью серверов IIS](https://go.microsoft.com/fwlink/?LinkId=393326).</span><span class="sxs-lookup"><span data-stu-id="28ebe-125">For more information about Microsoft load balancer technology, see [Build a Web Farm with IIS Servers](https://go.microsoft.com/fwlink/?LinkId=393326).</span></span>

-   <span data-ttu-id="28ebe-126">По крайней мере два сервера работают под управлением служб IIS и удовлетворены всеми необходимыми компонентами MBAM для поддержки своих веб-функций, в том числе ASP.NET MVC 4.</span><span class="sxs-lookup"><span data-stu-id="28ebe-126">At least two servers are running IIS and have met all of the MBAM prerequisites to support its web features, including ASP.NET MVC 4.</span></span>

-   <span data-ttu-id="28ebe-127">Базы данных и отчеты MBAM запущены на сервере.</span><span class="sxs-lookup"><span data-stu-id="28ebe-127">MBAM databases and reports are running on a server.</span></span>

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> <span data-ttu-id="28ebe-128">Специфичные для MBAM изменения, необходимые для обеспечения балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="28ebe-128">MBAM-specific changes that are required to enable Load Balancing</span></span>

<span data-ttu-id="28ebe-129">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="28ebe-129">Complete the following tasks:</span></span>

1.  <span data-ttu-id="28ebe-130">Зарегистрируйте имя субъекта-службы (SPN) для имени виртуального узла под учетной записью домена, которую вы используете для пулов приложений.</span><span class="sxs-lookup"><span data-stu-id="28ebe-130">Register a Service Principal Name (SPN) for the virtual host name under the domain account that you are using for the web application pools.</span></span> <span data-ttu-id="28ebe-131">Например, если имя виртуального узла — mbamvirtual.contoso.com, а учетная запись домена, используемая для пулов веб-приложений, — contoso\\mbamapppooluser, следующая команда регистрирует SPN соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="28ebe-131">For example, if the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\\mbamapppooluser, the following command registers the SPN appropriately.</span></span>

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  <span data-ttu-id="28ebe-132">Настройте следующие веб-функции MBAM:</span><span class="sxs-lookup"><span data-stu-id="28ebe-132">Configure the following MBAM web features:</span></span>

    -   <span data-ttu-id="28ebe-133">На каждом сервере, на котором будут размещаться веб-компоненты MBAM, используйте одну и ту же учетную запись домена для учетных данных администратора пула приложений.</span><span class="sxs-lookup"><span data-stu-id="28ebe-133">On each server that will host the MBAM web features, use the same domain account for the application pool administrative credentials.</span></span>

    -   <span data-ttu-id="28ebe-134">Укажите имя узла, соответствующее имени виртуального узла (DNS-имени) кластера балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="28ebe-134">Specify a host name that matches the virtual host name (DNS name) of the Load Balancing cluster.</span></span> <span data-ttu-id="28ebe-135">Например, при установке MBAM на сервере под названием "NLB1" и именем виртуального узла **mbamvirtual.contoso.com**убедитесь в том, что имя узла, указанное в командлете Windows PowerShell, **mbamvirtual.contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="28ebe-135">For example, when you install MBAM on a server called "NLB1" with a virtual host name of **mbamvirtual.contoso.com**, ensure that the host name that you specify in the Windows PowerShell cmdlet is **mbamvirtual.contoso.com**.</span></span>

3.  <span data-ttu-id="28ebe-136">Если вы настраиваете веб-сайты в веб-ферме с помощью подсистемы балансировки нагрузки, необходимо настроить веб-сайты на использование одного ключа компьютера.</span><span class="sxs-lookup"><span data-stu-id="28ebe-136">If you are configuring the websites in a web farm with a load balancer, you must configure the websites to use the same machine key.</span></span>

    <span data-ttu-id="28ebe-137">Дополнительные сведения можно найти в следующих разделах [элемента machineKey (схема параметров ASP.NET)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx).</span><span class="sxs-lookup"><span data-stu-id="28ebe-137">For more information, see the following sections in [machineKey Element (ASP.NET Settings Schema)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):</span></span>

    -   <span data-ttu-id="28ebe-138">Описание ключа компьютера</span><span class="sxs-lookup"><span data-stu-id="28ebe-138">Machine Key Explained</span></span>

    -   <span data-ttu-id="28ebe-139">Рекомендации по развертыванию веб-фермы</span><span class="sxs-lookup"><span data-stu-id="28ebe-139">Web Farm Deployment Considerations</span></span>

    <span data-ttu-id="28ebe-140">Инструкции по созданию ключа для автоматического создания см. в разделе [Создание ключа компьютера (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).</span><span class="sxs-lookup"><span data-stu-id="28ebe-140">For instructions about how to automatically generate a key, see [Generate a Machine Key (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).</span></span>

<span data-ttu-id="28ebe-141">Сведения о балансировке нагрузки также применимы к кластерам балансировки сетевой нагрузки (NLB) для IIS в Windows Server 2012 или Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="28ebe-141">The information about Load Balancing also applies to IIS Network Load Balancing (NLB) clusters in Windows Server 2012 or Windows Server2008R2.</span></span> <span data-ttu-id="28ebe-142">Функция балансировки нагрузки сети для служб IIS в Windows Server 2012 обычно такая же, как и в Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="28ebe-142">The IIS Network Load Balancing functionality in Windows Server 2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="28ebe-143">Однако некоторые сведения о задачах в Windows Server 2012 отличаются.</span><span class="sxs-lookup"><span data-stu-id="28ebe-143">However, some task details are different in Windows Server 2012.</span></span> <span data-ttu-id="28ebe-144">Сведения о новых способах выполнения задач можно найти [в разделе типичные задачи управления и Навигация в Windows server 2012 R2 Preview и Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).</span><span class="sxs-lookup"><span data-stu-id="28ebe-144">For information about new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

## <a href="" id="bkmk-db-mirroring"></a><span data-ttu-id="28ebe-145">Зеркальное отображение базы данных в SQL Server</span><span class="sxs-lookup"><span data-stu-id="28ebe-145">Database mirroring in SQL Server</span></span>


<span data-ttu-id="28ebe-146">MBAM поддерживает использование зеркального отображения SQL Server, в котором база данных соответствия требованиям и аудита и база данных восстановления зеркально отражаются с помощью двух экземпляров SQL Server для каждой базы данных.</span><span class="sxs-lookup"><span data-stu-id="28ebe-146">MBAM supports the use of SQL Server mirroring, where the Compliance and Audit Database and the Recovery Database are mirrored by using two instances of SQL Server for each database.</span></span> <span data-ttu-id="28ebe-147">Перед реализацией зеркального отображения следует учитывать, что зеркальное отображение выполняется постепенно, в пользу групп доступности, рассмотренных ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="28ebe-147">Before implementing mirroring, be aware that mirroring is slowly being phased out, in favor of availability groups, which are discussed earlier in this topic.</span></span>

<span data-ttu-id="28ebe-148">Для реализации зеркального отображения для MBAM необходимо указать соответствующие строки подключения для конфигурации зеркальной базы данных с помощью командлета Windows PowerShell **Enable-MbamWebApplication** .</span><span class="sxs-lookup"><span data-stu-id="28ebe-148">To implement mirroring for MBAM, you must specify the appropriate connection strings for the mirrored database configuration by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet.</span></span> <span data-ttu-id="28ebe-149">Дополнительные сведения о командлетах Windows PowerShell MBAM 2,5 можно найти в разделе [Настройка серверных функций MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="28ebe-149">For more information about the MBAM 2.5 Windows PowerShell cmdlets, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

### <span data-ttu-id="28ebe-150">Примеры реализации зеркального отображения SQL Server с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="28ebe-150">Examples of implementing SQL Server mirroring by using Windows PowerShell</span></span>

<span data-ttu-id="28ebe-151">В следующих примерах показано, как вы можете реализовать зеркальное отображение SQL Server с помощью командлетов Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28ebe-151">The following examples show how you might implement SQL Server mirroring by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="28ebe-152">Пример 1</span><span class="sxs-lookup"><span data-stu-id="28ebe-152">Example 1</span></span>**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**<span data-ttu-id="28ebe-153">Пример 2</span><span class="sxs-lookup"><span data-stu-id="28ebe-153">Example 2</span></span>**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### <span data-ttu-id="28ebe-154">Дополнительные сведения о зеркальном отображении SQL Server</span><span class="sxs-lookup"><span data-stu-id="28ebe-154">More information about SQL Server mirroring</span></span>

<span data-ttu-id="28ebe-155">Ниже приведены ссылки на дополнительные сведения о настройке зеркального отображения SQL Server.</span><span class="sxs-lookup"><span data-stu-id="28ebe-155">The following links provide more information about configuring SQL Server mirroring:</span></span>

-   [<span data-ttu-id="28ebe-156">Инструкции: Подготовка зеркальной базы данных для зеркального отображения (Transact-SQL)</span><span class="sxs-lookup"><span data-stu-id="28ebe-156">How to: Prepare a Mirror Database for Mirroring (Transact-SQL)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [<span data-ttu-id="28ebe-157">Создание сеанса зеркального отображения базы данных с использованием проверки подлинности Windows (SQL Server Management Studio)</span><span class="sxs-lookup"><span data-stu-id="28ebe-157">Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a><span data-ttu-id="28ebe-158">Резервное копирование баз данных MBAM с помощью службы теневого копирования томов (VSS)</span><span class="sxs-lookup"><span data-stu-id="28ebe-158">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="28ebe-159">MBAM предоставляет средство записи службы теневого копирования тома (VSS), которое называется администратором Microsoft BitLocker и разработчиком управления.</span><span class="sxs-lookup"><span data-stu-id="28ebe-159">MBAM provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer.</span></span> <span data-ttu-id="28ebe-160">Этот модуль записи VSS упрощает резервное копирование базы данных соответствия требованиям и аудита и базы данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="28ebe-160">This VSS writer facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="28ebe-161">Средство записи VSS регистрируется на каждом сервере, на котором вы включаете веб-приложение MBAM.</span><span class="sxs-lookup"><span data-stu-id="28ebe-161">The VSS writer is registered on every server where you enable an MBAM web application.</span></span> <span data-ttu-id="28ebe-162">Средство записи VSS MBAM зависит от модуля записи VSS SQL Server, которое зарегистрировано как часть установки Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="28ebe-162">The MBAM VSS writer depends on the SQL Server VSS Writer, which is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="28ebe-163">Любая технология резервного копирования, использующая средства записи VSS для выполнения резервного копирования, может найти модуль записи VSS MBAM.</span><span class="sxs-lookup"><span data-stu-id="28ebe-163">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS writer.</span></span>



## <span data-ttu-id="28ebe-164">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="28ebe-164">Related topics</span></span>


[<span data-ttu-id="28ebe-165">Планирование развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="28ebe-165">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="28ebe-166">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="28ebe-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="28ebe-167">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="28ebe-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="28ebe-168">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="28ebe-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




