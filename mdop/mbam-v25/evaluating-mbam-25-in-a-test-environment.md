---
title: Оценка MBAM 2.5 в тестовой среде
description: Оценка MBAM 2.5 в тестовой среде
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823152"
---
# <span data-ttu-id="a6c12-103">Оценка MBAM 2.5 в тестовой среде</span><span class="sxs-lookup"><span data-stu-id="a6c12-103">Evaluating MBAM 2.5 in a Test Environment</span></span>


<span data-ttu-id="a6c12-104">В этой статье описано, как настроить тестовую среду для оценки администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5 в изолированной топологии интеграции или диспетчере System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a6c12-104">This topic describes how you can set up a test environment to evaluate Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in the Stand-alone or System Center Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="a6c12-105">Оценка MBAM 2,5 с помощью изолированной топологии</span><span class="sxs-lookup"><span data-stu-id="a6c12-105">Evaluating MBAM 2.5 by using the Stand-alone topology</span></span>


<span data-ttu-id="a6c12-106">Чтобы вычислить MBAM с помощью изолированной топологии, используйте сведения из приведенных ниже таблиц, чтобы установить программное обеспечение сервера MBAM, а затем настройте компоненты сервера MBAM в тестовой среде.</span><span class="sxs-lookup"><span data-stu-id="a6c12-106">To evaluate MBAM by using the Stand-alone topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span>

**<span data-ttu-id="a6c12-107">Оценка MBAM 2,5 с помощью изолированной топологии</span><span class="sxs-lookup"><span data-stu-id="a6c12-107">To evaluate MBAM 2.5 by using the Stand-alone topology</span></span>**

1. <span data-ttu-id="a6c12-108">Прежде чем устанавливать MBAM, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a6c12-108">Before installing MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a6c12-109">Задача</span><span class="sxs-lookup"><span data-stu-id="a6c12-109">Task</span></span></th>
   <th align="left"><span data-ttu-id="a6c12-110">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="a6c12-110">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-111">Убедитесь, что вы установили все необходимое программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="a6c12-111">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="a6c12-112">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="a6c12-112">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a6c12-113">Проверьте требования к оборудованию, ОЗУ и другим требованиям.</span><span class="sxs-lookup"><span data-stu-id="a6c12-113">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="a6c12-114">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-115">Если вы планируете использовать командлеты для настройки MBAM, ознакомьтесь с необходимыми требованиями для использования Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a6c12-115">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="a6c12-116">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6c12-116">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="a6c12-117">Установите программное обеспечение сервера MBAM и настройте необходимые функции.</span><span class="sxs-lookup"><span data-stu-id="a6c12-117">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a6c12-118">Задача</span><span class="sxs-lookup"><span data-stu-id="a6c12-118">Task</span></span></th>
   <th align="left"><span data-ttu-id="a6c12-119">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="a6c12-119">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-120">Установите серверное программное обеспечение MBAM на каждый сервер, на котором вы хотите настроить компонент MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="a6c12-120">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="a6c12-121">Установка программного обеспечения MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="a6c12-121">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a6c12-122">Настройте базу данных соответствия и аудита, а также базу данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="a6c12-122">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="a6c12-123">Настройка баз данных MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-123">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-124">Настройка функции "отчеты".</span><span class="sxs-lookup"><span data-stu-id="a6c12-124">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="a6c12-125">Настройка отчетов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-125">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a6c12-126">Настройте веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="a6c12-126">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="a6c12-127">Настройка веб-приложений MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-127">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="a6c12-128">На клиентском компьютере выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a6c12-128">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="a6c12-129">Установите клиент MBAM на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="a6c12-129">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="a6c12-130">Примените на компьютере объекты групповой политики MBAM (GPO).</span><span class="sxs-lookup"><span data-stu-id="a6c12-130">Apply the MBAM Group Policy Objects (GPOs) to the computer.</span></span>

   3.  <span data-ttu-id="a6c12-131">Задайте указанные ниже разделы реестра, чтобы клиент MBAM быстрее пробудиться и через регулярные интервалы времени.</span><span class="sxs-lookup"><span data-stu-id="a6c12-131">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="a6c12-132">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a6c12-132">Note</span></span>**  
       <span data-ttu-id="a6c12-133">Поскольку эти ключи выключаются из клиента MBAM каждую минуту, рекомендуется использовать эти параметры реестра только в тестовой среде.</span><span class="sxs-lookup"><span data-stu-id="a6c12-133">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="a6c12-134">Перезапустите **службу клиента управления BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="a6c12-134">Restart the **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="a6c12-135">Оценка MBAM 2,5 с помощью топологии интеграции System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a6c12-135">Evaluating MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>


<span data-ttu-id="a6c12-136">Чтобы оценить MBAM с помощью топологии интеграции Configuration Manager, используйте сведения из приведенных ниже таблиц, чтобы установить программное обеспечение сервера MBAM, а затем настройте компоненты сервера MBAM в тестовой среде.</span><span class="sxs-lookup"><span data-stu-id="a6c12-136">To evaluate MBAM by using the Configuration Manager Integration topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span> <span data-ttu-id="a6c12-137">После установки клиента MBAM на клиентском компьютере вы можете выполнить дополнительные действия, чтобы заставить клиента MBAM сообщать о состоянии компьютера в MBAM быстрее.</span><span class="sxs-lookup"><span data-stu-id="a6c12-137">After installing the MBAM Client on a client computer, you will complete additional steps to force the MBAM Client to report the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="a6c12-138">Оценка MBAM 2,5 с помощью топологии интеграции System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a6c12-138">To evaluate MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>**

1. <span data-ttu-id="a6c12-139">Перед установкой MBAM ознакомьтесь с необходимым программным обеспечением и поддерживаемой конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="a6c12-139">Before installing MBAM, review the prerequisite software and supported configuration.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a6c12-140">Задача</span><span class="sxs-lookup"><span data-stu-id="a6c12-140">Task</span></span></th>
   <th align="left"><span data-ttu-id="a6c12-141">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="a6c12-141">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-142">Убедитесь, что вы установили все необходимое программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="a6c12-142">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="a6c12-143">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="a6c12-143">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="a6c12-144">Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="a6c12-144">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a6c12-145">Проверьте требования к оборудованию, ОЗУ и другим требованиям.</span><span class="sxs-lookup"><span data-stu-id="a6c12-145">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="a6c12-146">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-146">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-147">Если вы планируете использовать командлеты для настройки MBAM, ознакомьтесь с необходимыми требованиями для использования Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a6c12-147">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="a6c12-148">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6c12-148">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a6c12-149">Создание и изменение MOF-файлов.</span><span class="sxs-lookup"><span data-stu-id="a6c12-149">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="a6c12-150">Изменение файла Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="a6c12-150">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="a6c12-151">Создание или изменение файла Sms_def.mof</span><span class="sxs-lookup"><span data-stu-id="a6c12-151">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="a6c12-152">Установите программное обеспечение сервера MBAM и настройте необходимые функции.</span><span class="sxs-lookup"><span data-stu-id="a6c12-152">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a6c12-153">Задача</span><span class="sxs-lookup"><span data-stu-id="a6c12-153">Task</span></span></th>
   <th align="left"><span data-ttu-id="a6c12-154">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="a6c12-154">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-155">Установите серверное программное обеспечение MBAM на каждый сервер, на котором вы хотите настроить компонент MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="a6c12-155">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="a6c12-156">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a6c12-156">Note</span></span></strong><br/><p><span data-ttu-id="a6c12-157">Вы можете установить базы данных на удаленном компьютере SQL Server с помощью Windows PowerShell или пакета экспортированного приложения уровня данных (DAC).</span><span class="sxs-lookup"><span data-stu-id="a6c12-157">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="a6c12-158">Дополнительные сведения о пакетах DAC можно найти в разделе <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> приложения уровня данных </a> .</span><span class="sxs-lookup"><span data-stu-id="a6c12-158">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="a6c12-159">Установка программного обеспечения MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="a6c12-159">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a6c12-160">Настройте базу данных соответствия и аудита, а также базу данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="a6c12-160">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="a6c12-161">Настройка баз данных MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-161">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-162">Настройка функции "отчеты".</span><span class="sxs-lookup"><span data-stu-id="a6c12-162">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="a6c12-163">Настройка отчетов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-163">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a6c12-164">Настройте веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="a6c12-164">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="a6c12-165">Настройка веб-приложений MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-165">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-166">Настройте System Center Configuration Manager, чтобы установить объекты Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a6c12-166">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="a6c12-167">Настройка интеграции System Center Configuration Manager с MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-167">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="a6c12-168">На клиентском компьютере выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a6c12-168">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="a6c12-169">Установите клиент MBAM и клиент Configuration Manager на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="a6c12-169">Install the MBAM Client and the Configuration Manager Client on a client computer.</span></span>

   2.  <span data-ttu-id="a6c12-170">Примените объекты групповой политики MBAM к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="a6c12-170">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="a6c12-171">Задайте указанные ниже разделы реестра, чтобы клиент MBAM быстрее пробудиться и через регулярные интервалы времени.</span><span class="sxs-lookup"><span data-stu-id="a6c12-171">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="a6c12-172">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a6c12-172">Note</span></span>**  
       <span data-ttu-id="a6c12-173">Поскольку эти ключи выключаются из клиента MBAM каждую минуту, рекомендуется использовать эти параметры реестра только в тестовой среде.</span><span class="sxs-lookup"><span data-stu-id="a6c12-173">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="a6c12-174">Перезапустите **службу клиента управления BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="a6c12-174">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="a6c12-175">На панели управления откройте **Configuration Manager**и откройте вкладку **действия** .</span><span class="sxs-lookup"><span data-stu-id="a6c12-175">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="a6c12-176">Выберите " **цикл инвентаризации оборудования**" и нажмите кнопку " **выполнить сейчас**".</span><span class="sxs-lookup"><span data-stu-id="a6c12-176">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="a6c12-177">Этот шаг запускает инвентаризацию оборудования, используя новые классы, импортированные в MOF-файлы, а затем отправляет их на сервер Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a6c12-177">This step runs the hardware inventory by using the new classes that you imported to your .mof files, and then sends the data to the Configuration Manager server.</span></span>

   7.  <span data-ttu-id="a6c12-178">Выберите пункт **Получение политики компьютера & цикл оценки**, а затем нажмите кнопку **выполнить** , чтобы применить объекты групповой политики, которые относятся к этому клиентскому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="a6c12-178">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>



4. <span data-ttu-id="a6c12-179">На консоли Configuration Manager выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a6c12-179">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="a6c12-180">В области навигации щелкните правой кнопкой мыши **Поддерживаемые компьютеры MBAM**, выберите команду **Обновить членство**, а затем нажмите кнопку **Да** , чтобы заставить клиентский компьютер немедленно сообщить о своей членстве.</span><span class="sxs-lookup"><span data-stu-id="a6c12-180">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="a6c12-181">В области навигации щелкните **Поддерживаемые компьютеры MBAM** , чтобы убедиться в том, что клиентский компьютер указан в коллекции.</span><span class="sxs-lookup"><span data-stu-id="a6c12-181">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="a6c12-182">На клиентском компьютере на панели управления снова откройте **Configuration Manager** и выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a6c12-182">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="a6c12-183">Откройте вкладку **действия** и перезапустите **цикл оценки & политики компьютера**.</span><span class="sxs-lookup"><span data-stu-id="a6c12-183">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="a6c12-184">Откройте вкладку **конфигурации** , выберите базовый план BitLocker и нажмите кнопку **вычислить**.</span><span class="sxs-lookup"><span data-stu-id="a6c12-184">Click the **Configurations** tab, select the BitLocker baseline, and then click **Evaluate**.</span></span>

6. <span data-ttu-id="a6c12-185">На консоли Configuration Manager убедитесь, что клиентский компьютер отображается в отчете соответствие требованиям предприятия.</span><span class="sxs-lookup"><span data-stu-id="a6c12-185">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report: as follows:</span></span>

   1.  <span data-ttu-id="a6c12-186">В области навигации выберите рабочую область " **мониторинг** ".</span><span class="sxs-lookup"><span data-stu-id="a6c12-186">In the navigation pane, select the **Monitoring** workspace.</span></span>

   2.  <span data-ttu-id="a6c12-187">В дереве консоли разверните раздел отчеты **о отчетах** &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="a6c12-187">In the console tree, expand **Overview** &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

   3.  <span data-ttu-id="a6c12-188">Выберите папку, представляющую язык, на котором вы хотите просмотреть отчеты, а затем выберите отчет в области результатов.</span><span class="sxs-lookup"><span data-stu-id="a6c12-188">Select the folder that represents the language in which you want to view reports, and then select the report in the results pane.</span></span>

## <span data-ttu-id="a6c12-189">Оценка MBAM 2,5 с помощью топологии интеграции System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="a6c12-189">Evaluating MBAM 2.5 by using the System Center Configuration Manager 2007 Integration topology</span></span>


<span data-ttu-id="a6c12-190">Чтобы вычислить MBAM с помощью топологии интеграции Configuration Manager, выполните те же действия, что и при установке и настройке MBAM в тестовой среде, как вы используете в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="a6c12-190">To evaluate MBAM by using the Configuration Manager Integration topology, follow the same steps to install and configure MBAM in your test environment as you use in a production environment.</span></span> <span data-ttu-id="a6c12-191">После установки клиента MBAM на клиентском компьютере выполните дополнительные действия, описанные в этой статье, чтобы разрешить клиенту MBAM сообщать о состоянии компьютера в MBAM быстрее.</span><span class="sxs-lookup"><span data-stu-id="a6c12-191">After installing the MBAM Client on a client computer, complete the additional steps in this topic to enable the MBAM Client to start reporting the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="a6c12-192">Оценка MBAM с помощью топологии интеграции Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="a6c12-192">To evaluate MBAM by using the Configuration Manager 2007 Integration topology</span></span>**

1. <span data-ttu-id="a6c12-193">Перед установкой MBAM выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a6c12-193">Before you install MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a6c12-194">Задача</span><span class="sxs-lookup"><span data-stu-id="a6c12-194">Task</span></span></th>
   <th align="left"><span data-ttu-id="a6c12-195">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="a6c12-195">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-196">Убедитесь, что вы установили все необходимое программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="a6c12-196">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="a6c12-197">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="a6c12-197">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="a6c12-198">Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="a6c12-198">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a6c12-199">Проверьте требования к оборудованию, ОЗУ и другим требованиям.</span><span class="sxs-lookup"><span data-stu-id="a6c12-199">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="a6c12-200">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-200">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-201">Создание и изменение MOF-файлов.</span><span class="sxs-lookup"><span data-stu-id="a6c12-201">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="a6c12-202">Изменение файла Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="a6c12-202">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="a6c12-203">Создание или изменение файла Sms_def.mof</span><span class="sxs-lookup"><span data-stu-id="a6c12-203">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="a6c12-204">Установите программное обеспечение сервера MBAM и настройте необходимые функции.</span><span class="sxs-lookup"><span data-stu-id="a6c12-204">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a6c12-205">Задача</span><span class="sxs-lookup"><span data-stu-id="a6c12-205">Task</span></span></th>
   <th align="left"><span data-ttu-id="a6c12-206">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="a6c12-206">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-207">Установите серверное программное обеспечение MBAM на каждый сервер, на котором вы хотите настроить компонент MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="a6c12-207">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="a6c12-208">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a6c12-208">Note</span></span></strong><br/><p><span data-ttu-id="a6c12-209">Вы можете установить базы данных на удаленном компьютере SQL Server с помощью Windows PowerShell или пакета экспортированного приложения уровня данных (DAC).</span><span class="sxs-lookup"><span data-stu-id="a6c12-209">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="a6c12-210">Дополнительные сведения о пакетах DAC можно найти в разделе <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> приложения уровня данных </a> .</span><span class="sxs-lookup"><span data-stu-id="a6c12-210">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="a6c12-211">Установка программного обеспечения MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="a6c12-211">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a6c12-212">Настройте базу данных соответствия и аудита, а также базу данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="a6c12-212">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="a6c12-213">Настройка баз данных MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-213">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-214">Настройка функции "отчеты".</span><span class="sxs-lookup"><span data-stu-id="a6c12-214">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="a6c12-215">Настройка отчетов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-215">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a6c12-216">Настройте веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="a6c12-216">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="a6c12-217">Настройка веб-приложений MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-217">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6c12-218">Настройте System Center Configuration Manager, чтобы установить объекты Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a6c12-218">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="a6c12-219">Настройка интеграции System Center Configuration Manager с MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-219">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="a6c12-220">На клиентском компьютере выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a6c12-220">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="a6c12-221">Установите клиент MBAM на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="a6c12-221">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="a6c12-222">Примените объекты групповой политики MBAM к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="a6c12-222">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="a6c12-223">Задайте указанные ниже разделы реестра, чтобы клиент MBAM быстрее выключаюсь и быстрее.</span><span class="sxs-lookup"><span data-stu-id="a6c12-223">Set the following registry keys to force the MBAM Client to wake up more quickly and at faster intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="a6c12-224">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a6c12-224">Note</span></span>**  
       <span data-ttu-id="a6c12-225">Поскольку эти ключи выключаются из клиента MBAM каждую минуту, рекомендуется использовать эти параметры реестра только в среде оценки.</span><span class="sxs-lookup"><span data-stu-id="a6c12-225">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in an evaluation environment.</span></span>



   4.  <span data-ttu-id="a6c12-226">Перезапустите **службу клиента управления BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="a6c12-226">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="a6c12-227">На панели управления откройте **Configuration Manager**и откройте вкладку **действия** .</span><span class="sxs-lookup"><span data-stu-id="a6c12-227">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="a6c12-228">Выберите пункт **Получение политики компьютера & цикл оценки**, а затем нажмите кнопку **выполнить** , чтобы применить объекты групповой политики, которые относятся к этому клиентскому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="a6c12-228">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>

   7.  <span data-ttu-id="a6c12-229">Выберите " **цикл инвентаризации оборудования**" и нажмите кнопку " **выполнить сейчас**".</span><span class="sxs-lookup"><span data-stu-id="a6c12-229">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="a6c12-230">Это действие запускает инвентаризацию оборудования, используя новые классы, импортированные в MOF-файлы, а затем отправляет их на сервер Configuration Manager Server.</span><span class="sxs-lookup"><span data-stu-id="a6c12-230">This step runs the hardware inventory by using the new classes that you imported to your .mof files and then sends the data to the Configuration Manager server.</span></span>

4. <span data-ttu-id="a6c12-231">На консоли Configuration Manager выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a6c12-231">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="a6c12-232">В области навигации щелкните правой кнопкой мыши **Поддерживаемые компьютеры MBAM**, выберите команду **Обновить членство**, а затем нажмите кнопку **Да** , чтобы заставить клиентский компьютер немедленно сообщить о своей членстве.</span><span class="sxs-lookup"><span data-stu-id="a6c12-232">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="a6c12-233">В области навигации щелкните **Поддерживаемые компьютеры MBAM** , чтобы убедиться в том, что клиентский компьютер указан в коллекции.</span><span class="sxs-lookup"><span data-stu-id="a6c12-233">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="a6c12-234">На клиентском компьютере на панели управления снова откройте **Configuration Manager** и выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a6c12-234">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="a6c12-235">Откройте вкладку **действия** и перезапустите **цикл оценки & политики компьютера**.</span><span class="sxs-lookup"><span data-stu-id="a6c12-235">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="a6c12-236">Откройте вкладку **конфигурации** , выберите базовый план BitLocker и нажмите кнопку **оценить**.</span><span class="sxs-lookup"><span data-stu-id="a6c12-236">Click the **Configurations** tab, select the BitLocker baseline, and click **Evaluate**.</span></span>

6. <span data-ttu-id="a6c12-237">На консоли Configuration Manager убедитесь, что клиентский компьютер отображается в отчете о соответствии требованиям в корпоративной среде, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="a6c12-237">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report, as follows</span></span>

   1.  <span data-ttu-id="a6c12-238">В области навигации разверните узел **Computer Management** &gt; **Reporting** &gt; имя сервера **служб отчетов для службы** управления компьютером &gt; \*\* &lt; &gt; MBAM\*\*.</span><span class="sxs-lookup"><span data-stu-id="a6c12-238">In the navigation pane, expand **Computer Management** &gt; **Reporting** &gt; **Reporting Services** &gt; **&lt;server name&gt;MBAM**.</span></span>

   2.  <span data-ttu-id="a6c12-239">В узле **MBAM** выберите папку, представляющую язык, на котором нужно просмотреть отчеты, а затем выберите отчет в области результатов.</span><span class="sxs-lookup"><span data-stu-id="a6c12-239">Within the **MBAM** node, select the folder that represents the language in which you want to view reports, and then select the report from the results pane.</span></span>


## <span data-ttu-id="a6c12-240">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a6c12-240">Related topics</span></span>


[<span data-ttu-id="a6c12-241">Начало работы с MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a6c12-241">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)


## <span data-ttu-id="a6c12-242">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="a6c12-242">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a6c12-243">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="a6c12-243">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="a6c12-244">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a6c12-244">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>





