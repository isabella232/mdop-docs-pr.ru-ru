---
title: Планирование высокого уровня доступности в App-V 5.1
description: Планирование высокого уровня доступности в App-V 5.1
author: dansimp
ms.assetid: 1f190a0e-10ee-4fbe-a602-7e807e943033
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5c8e0e684051859a4caa2c4ef983c040295bc6d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813480"
---
# <span data-ttu-id="62d6d-103">Планирование высокого уровня доступности в App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="62d6d-103">Planning for High Availability with App-V 5.1</span></span>


<span data-ttu-id="62d6d-104">Microsoft Application Virtualization (App-V) 5,1 конфигураций системы может использовать возможности, поддерживающие высокий уровень доступности служб.</span><span class="sxs-lookup"><span data-stu-id="62d6d-104">Microsoft Application Virtualization (App-V) 5.1 system configurations can take advantage of options that maintain a high level of available service.</span></span>

<span data-ttu-id="62d6d-105">Сведения о том, как развертывать App-V 5,1 в высокодоступной конфигурации, можно найти в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="62d6d-105">Use the information in the following sections to help you understand the options to deploy App-V 5.1 in a highly available configuration.</span></span>

-   [<span data-ttu-id="62d6d-106">Поддержка кластеризации Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="62d6d-106">Support for Microsoft SQL Server clustering</span></span>](#bkmk-sqlcluster)

-   [<span data-ttu-id="62d6d-107">Поддержка балансировки нагрузки сети для IIS</span><span class="sxs-lookup"><span data-stu-id="62d6d-107">Support for IIS Network Load Balancing</span></span>](#bkmk-iisloadbal)

-   [<span data-ttu-id="62d6d-108">Поддержка кластерных файловых серверов при работе с режимом SCS</span><span class="sxs-lookup"><span data-stu-id="62d6d-108">Support for clustered file servers when running (SCS) mode</span></span>](#bkmk-clusterscsmode)

-   [<span data-ttu-id="62d6d-109">Поддержка зеркального отображения Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="62d6d-109">Support for Microsoft SQL Server Mirroring</span></span>](#bkmk-sqlmirroring)

-   [<span data-ttu-id="62d6d-110">Поддержка для Microsoft SQL Server всегда включена</span><span class="sxs-lookup"><span data-stu-id="62d6d-110">Support for Microsoft SQL Server Always On</span></span>](#bkmk-sqlalwayson)

## <a href="" id="bkmk-sqlcluster"></a><span data-ttu-id="62d6d-111">Поддержка кластеризации Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="62d6d-111">Support for Microsoft SQL Server clustering</span></span>


<span data-ttu-id="62d6d-112">Базу данных управления App-V и базу данных отчетов можно запускать на компьютерах, на которых запущены кластеры Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="62d6d-112">You can run the App-V Management database and Reporting database on computers that are running Microsoft SQL Server clusters.</span></span> <span data-ttu-id="62d6d-113">Тем не менее, необходимо установить базы данных с помощью сценариев.</span><span class="sxs-lookup"><span data-stu-id="62d6d-113">However, you must install the databases using scripts.</span></span>

<span data-ttu-id="62d6d-114">Инструкции можно найти в разделе [развертывание баз данных App-V с помощью сценариев SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span><span class="sxs-lookup"><span data-stu-id="62d6d-114">For instructions, see [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span></span>

## <a href="" id="bkmk-iisloadbal"></a><span data-ttu-id="62d6d-115">Поддержка балансировки нагрузки сети для IIS</span><span class="sxs-lookup"><span data-stu-id="62d6d-115">Support for IIS Network Load Balancing</span></span>


<span data-ttu-id="62d6d-116">С помощью балансировки сетевой нагрузки служб IIS можно настроить высокодоступную среду для компьютеров, на которых выполняются службы управления приложениями, публикации и создания отчетов, которые развертываются с помощью IIS.</span><span class="sxs-lookup"><span data-stu-id="62d6d-116">You can use Internet Information Services (IIS) Network Load Balancing to configure a highly available environment for computers running the App-V 5.x Management, Publishing, and Reporting services which are deployed through IIS.</span></span>

<span data-ttu-id="62d6d-117">Дополнительные сведения о настройке служб IIS и балансировки сетевой нагрузки на компьютерах с операционными системами Windows Server можно узнать ниже.</span><span class="sxs-lookup"><span data-stu-id="62d6d-117">Review the following for more information about configuring IIS and Network Load Balancing for computers running Windows Server operating systems:</span></span>

-   <span data-ttu-id="62d6d-118">Содержит сведения о настройке служб IIS 7,0.</span><span class="sxs-lookup"><span data-stu-id="62d6d-118">Provides information about configuring Internet Information Services (IIS) 7.0.</span></span>

    <span data-ttu-id="62d6d-119">[Достижение высокой доступности и масштабируемости — ARR и NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span><span class="sxs-lookup"><span data-stu-id="62d6d-119">[Achieving High Availability and Scalability - ARR and NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span></span>

-   <span data-ttu-id="62d6d-120">Настройка Microsoft Windows Server</span><span class="sxs-lookup"><span data-stu-id="62d6d-120">Configuring Microsoft Windows Server</span></span>

    <span data-ttu-id="62d6d-121">[Балансировка сетевой нагрузки](https://go.microsoft.com/fwlink/?LinkId=316370) ( https://go.microsoft.com/fwlink/?LinkId=316370) .</span><span class="sxs-lookup"><span data-stu-id="62d6d-121">[Network Load Balancing](https://go.microsoft.com/fwlink/?LinkId=316370) (https://go.microsoft.com/fwlink/?LinkId=316370).</span></span>

    <span data-ttu-id="62d6d-122">Эти сведения также относятся к кластерам балансировки сетевой нагрузки (NLB) служб IIS в Windows Server2008, Windows Server2008R2 или Windows Server2012.</span><span class="sxs-lookup"><span data-stu-id="62d6d-122">This information also applies to IIS Network Load Balancing (NLB) clusters in Windows Server2008, Windows Server2008R2, or Windows Server2012.</span></span>

    <span data-ttu-id="62d6d-123">**Примечание**  Компоненты балансировки нагрузки сети для служб IIS в Windows Server2012, как правило, совпадают с Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="62d6d-123">**Note** The IIS Network Load Balancing functionality in Windows Server2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="62d6d-124">Однако некоторые сведения о задачах изменяются в Windows Server2012.</span><span class="sxs-lookup"><span data-stu-id="62d6d-124">However, some task details are changed in Windows Server2012.</span></span> <span data-ttu-id="62d6d-125">Сведения о новых способах выполнения задач можно найти [в разделе типичные задачи управления и Навигация в Windows server 2012 R2 Preview и Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) ( https://go.microsoft.com/fwlink/?LinkId=316371) .</span><span class="sxs-lookup"><span data-stu-id="62d6d-125">For information on new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) (https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

     

## <a href="" id="bkmk-clusterscsmode"></a><span data-ttu-id="62d6d-126">Поддержка кластерных файловых серверов при работе с режимом SCS</span><span class="sxs-lookup"><span data-stu-id="62d6d-126">Support for clustered file servers when running (SCS) mode</span></span>


<span data-ttu-id="62d6d-127">Поддерживается приложение App-V 5,1 в режиме общего доступа к хранилищу содержимого (SCS) с кластерными файловыми серверами.</span><span class="sxs-lookup"><span data-stu-id="62d6d-127">Running App-V 5.1 in Share Content Store (SCS) mode with clustered file servers is supported.</span></span>

<span data-ttu-id="62d6d-128">Для включения этой конфигурации можно использовать описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="62d6d-128">The following steps can be used to enable this configuration:</span></span>

-   <span data-ttu-id="62d6d-129">Настройте App-V 5,1 для работы в режиме клиента SCS.</span><span class="sxs-lookup"><span data-stu-id="62d6d-129">Configure App-V 5.1 to run in client SCS mode.</span></span> <span data-ttu-id="62d6d-130">Дополнительные сведения о настройке режима App-V 5,1 SCS можно найти [в разделе Установка клиента App-v 5,1 для общего режима хранения содержимого](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md).</span><span class="sxs-lookup"><span data-stu-id="62d6d-130">For more information about configuring App-V 5.1 SCS mode, see [How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md).</span></span>

-   <span data-ttu-id="62d6d-131">Настройте кластер файлового сервера, настроенный как в режиме "Server2012 Scale out", так и в режиме предварительного **2012** с помощью виртуальной сети SAN.</span><span class="sxs-lookup"><span data-stu-id="62d6d-131">Configure the file server cluster configured in both the Microsoft Server2012 scale out mode and pre **2012** mode with a virtual SAN.</span></span>

<span data-ttu-id="62d6d-132">Для проверки конфигурации можно использовать описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="62d6d-132">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="62d6d-133">Добавьте пакет на сервере публикаций.</span><span class="sxs-lookup"><span data-stu-id="62d6d-133">Add a package on the publishing server.</span></span> <span data-ttu-id="62d6d-134">Дополнительные сведения о добавлении пакета можно найти в разделе [Добавление и обновление пакетов с помощью консоли управления](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="62d6d-134">For more information about adding a package, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md).</span></span>

2.  <span data-ttu-id="62d6d-135">Выполните обновление публикации на компьютере с клиентом App-V 5,1 и откройте приложение.</span><span class="sxs-lookup"><span data-stu-id="62d6d-135">Perform a publishing refresh on the computer running the App-V 5.1 client and open an application.</span></span>

3.  <span data-ttu-id="62d6d-136">Переключите узлы кластера на середину и посредине, чтобы убедиться, что она работает правильно.</span><span class="sxs-lookup"><span data-stu-id="62d6d-136">Switch cluster nodes mid-publishing refresh and mid-streaming to ensure fail-over works correctly.</span></span>

<span data-ttu-id="62d6d-137">Дополнительные сведения о настройке отказоустойчивых кластеров Windows Server можно получить из указанных ниже.</span><span class="sxs-lookup"><span data-stu-id="62d6d-137">Review the following for more information about configuring Windows Server Failover clusters:</span></span>

-   <span data-ttu-id="62d6d-138">[Контрольный список: создание кластеризованного файлового сервера](https://go.microsoft.com/fwlink/?LinkId=316372) ( https://go.microsoft.com/fwlink/?LinkId=316372) .</span><span class="sxs-lookup"><span data-stu-id="62d6d-138">[Checklist: Create a Clustered File Server](https://go.microsoft.com/fwlink/?LinkId=316372) (https://go.microsoft.com/fwlink/?LinkId=316372).</span></span>

-   <span data-ttu-id="62d6d-139">[Используйте общие тома кластера в отказоустойчивом кластере Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316373) ( https://go.microsoft.com/fwlink/?LinkId=316373) .</span><span class="sxs-lookup"><span data-stu-id="62d6d-139">[Use Cluster Shared Volumes in a Windows Server 2012 Failover Cluster](https://go.microsoft.com/fwlink/?LinkId=316373) (https://go.microsoft.com/fwlink/?LinkId=316373).</span></span>

## <a href="" id="bkmk-sqlmirroring"></a><span data-ttu-id="62d6d-140">Поддержка зеркального отображения Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="62d6d-140">Support for Microsoft SQL Server Mirroring</span></span>


<span data-ttu-id="62d6d-141">С помощью зеркального отображения Microsoft SQL Server, в котором база данных сервера App-V 5,1 зеркально используется с двумя экземплярами SQL Server, поддерживается поддержка баз данных сервера управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="62d6d-141">Using Microsoft SQL Server mirroring, where the App-V 5.1 management server database is mirrored utilizing two SQL Server instances, for App-V 5.1 management server databases is supported.</span></span>

<span data-ttu-id="62d6d-142">Ознакомьтесь с дополнительными сведениями о настройке зеркального отображения Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="62d6d-142">Review the following for more information about configuring Microsoft SQL Server Mirroring:</span></span>

-   <span data-ttu-id="62d6d-143">[Инструкции: Подготовка зеркальной базы данных для зеркального отображения (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span><span class="sxs-lookup"><span data-stu-id="62d6d-143">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span></span>

-   <span data-ttu-id="62d6d-144">[Создание сеанса зеркального отображения базы данных с использованием проверки подлинности Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span><span class="sxs-lookup"><span data-stu-id="62d6d-144">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span></span>

<span data-ttu-id="62d6d-145">Для проверки конфигурации можно использовать описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="62d6d-145">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="62d6d-146">Запуск сеанса зеркального отображения Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="62d6d-146">Initiate a Microsoft SQL Server Mirroring session.</span></span>

2.  <span data-ttu-id="62d6d-147">Выберите пункт **отработка отказа** , чтобы назначить новый основной экземпляр Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="62d6d-147">Select **Failover** to designate a new master Microsoft SQL Server instance.</span></span>

3.  <span data-ttu-id="62d6d-148">Убедитесь, что сервер управления App-V 5,1 продолжает работать надлежащим образом после перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="62d6d-148">Verify that the App-V 5.1 management server continues to function as expected after the failover.</span></span>

<span data-ttu-id="62d6d-149">Строку подключения на сервере управления можно изменить, чтобы включить резервный \*\*партнер = &lt; Server2 &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="62d6d-149">The connection string on the management server can be modified to include **failover partner = &lt;server2&gt;**.</span></span> <span data-ttu-id="62d6d-150">Это поможет вам только в том случае, если на сервере-источнике произошел сбой с дополнительным подключением, а на компьютере, на котором запущен клиент App – V 5,1, установлено новое соединение (скажем, после перезагрузки).</span><span class="sxs-lookup"><span data-stu-id="62d6d-150">This will only help when the primary on the mirror has failed over to the secondary and the computer running the App-V 5.1 client is doing a fresh connection (say after reboot).</span></span>

<span data-ttu-id="62d6d-151">Выполните следующие действия, чтобы изменить строку подключения для включения резервного \*\*партнера = &lt; Server2 &gt; \*\*:</span><span class="sxs-lookup"><span data-stu-id="62d6d-151">Use the following steps to modify the connection string to include **failover partner = &lt;server2&gt;**:</span></span>

<span data-ttu-id="62d6d-152">**Важно!**  В этой статье описано, как изменить реестр Windows с помощью редактора реестра.</span><span class="sxs-lookup"><span data-stu-id="62d6d-152">**Important** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="62d6d-153">Если изменить реестр Windows некорректно, это может привести к серьезным неполадкам, которые могут потребовать повторной установки Windows.</span><span class="sxs-lookup"><span data-stu-id="62d6d-153">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="62d6d-154">Перед изменением реестра необходимо создать резервную копию файлов реестра (System. dat и User. dat).</span><span class="sxs-lookup"><span data-stu-id="62d6d-154">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="62d6d-155">Корпорация Майкрософт не несет ответственности за то, что проблемы, которые могут возникнуть при изменении реестра, могут быть устранены.</span><span class="sxs-lookup"><span data-stu-id="62d6d-155">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="62d6d-156">Изменение реестра на свой страх и риск.</span><span class="sxs-lookup"><span data-stu-id="62d6d-156">Change the registry at your own risk.</span></span>

 

1.  <span data-ttu-id="62d6d-157">Войдите на сервер управления и откройте **редактор реестра Regedit**.</span><span class="sxs-lookup"><span data-stu-id="62d6d-157">Login to the management server and open **regedit**.</span></span>

2.  <span data-ttu-id="62d6d-158">Перейдите в раздел **hKey \ _LOCAL \ _MACHINE**  \\  **программного обеспечения**  \\  **Microsoft**  \\  **AppV**  \\  **Server**  \\  **ManagementService**.</span><span class="sxs-lookup"><span data-stu-id="62d6d-158">Navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Server** \\ **ManagementService**.</span></span>

3.  <span data-ttu-id="62d6d-159">Измените значение **управления _SQL \ _CONNECTION \ _STRING** с помощью резервного \*\*партнера = &lt; Server2 &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="62d6d-159">Modify the **MANAGEMENT\_SQL\_CONNECTION\_STRING** value with the **failover partner = &lt;server2&gt;**.</span></span>

4.  <span data-ttu-id="62d6d-160">Перезапустите службу управления с помощью консоли IIS.</span><span class="sxs-lookup"><span data-stu-id="62d6d-160">Restart management service using the IIS console.</span></span>

    <span data-ttu-id="62d6d-161">**Примечание**  Зеркальное отображение базы данных — это список устаревших функций ядра СУБД для Microsoft SQL Server2012 из-за возможности **AlwaysOn** , доступной в Microsoft sql Server 2012.</span><span class="sxs-lookup"><span data-stu-id="62d6d-161">**Note** Database Mirroring is on the list of Deprecated Database Engine Features for Microsoft SQL Server2012 due to the **AlwaysOn** feature available with Microsoft SQL Server 2012.</span></span>

     

<span data-ttu-id="62d6d-162">Чтобы получить дополнительные сведения, щелкните одну из следующих ссылок:</span><span class="sxs-lookup"><span data-stu-id="62d6d-162">Click any of the following links for more information:</span></span>

-   <span data-ttu-id="62d6d-163">[Инструкции: Подготовка зеркальной базы данных для зеркального отображения (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) ( https://go.microsoft.com/fwlink/?LinkId=394235) .</span><span class="sxs-lookup"><span data-stu-id="62d6d-163">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) (https://go.microsoft.com/fwlink/?LinkId=394235).</span></span>

-   <span data-ttu-id="62d6d-164">[Инструкции: Настройка сеанса зеркального отображения базы данных (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) ( https://go.microsoft.com/fwlink/?LinkId=394236) .</span><span class="sxs-lookup"><span data-stu-id="62d6d-164">[How to: Configure a Database Mirroring Session (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) (https://go.microsoft.com/fwlink/?LinkId=394236).</span></span>

-   <span data-ttu-id="62d6d-165">[Создание сеанса зеркального отображения базы данных с использованием проверки подлинности Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) ( https://go.microsoft.com/fwlink/?LinkId=394237) .</span><span class="sxs-lookup"><span data-stu-id="62d6d-165">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) (https://go.microsoft.com/fwlink/?LinkId=394237).</span></span>

-   <span data-ttu-id="62d6d-166">[Устаревшие функции ядра СУБД в SQL server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) ( https://go.microsoft.com/fwlink/?LinkId=394238) .</span><span class="sxs-lookup"><span data-stu-id="62d6d-166">[Deprecated Database Engine Features in SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) (https://go.microsoft.com/fwlink/?LinkId=394238).</span></span>

## <a href="" id="bkmk-sqlalwayson"></a><span data-ttu-id="62d6d-167">Поддержка в конфигурации Microsoft SQL Server всегда включена</span><span class="sxs-lookup"><span data-stu-id="62d6d-167">Support for Microsoft SQL Server Always On configuration</span></span>


<span data-ttu-id="62d6d-168">База данных сервера управления App-V 5,1 поддерживает развертывание на компьютерах с операционной системой Microsoft SQL Server с **постоянной** конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="62d6d-168">The App-V 5.1 management server database supports deployments to computers running Microsoft SQL Server with the **Always On** configuration.</span></span>






## <span data-ttu-id="62d6d-169">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="62d6d-169">Related topics</span></span>


[<span data-ttu-id="62d6d-170">Планирование развертывания App-V</span><span class="sxs-lookup"><span data-stu-id="62d6d-170">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





