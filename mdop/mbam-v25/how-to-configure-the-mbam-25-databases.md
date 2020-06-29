---
title: Настройка баз данных MBAM 2.5
description: Настройка баз данных MBAM 2.5
author: dansimp
ms.assetid: 66e1c81b-f785-4398-9175-bb5f112c2a35
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c11cb58d8fd9266bd0322e4cf9aa96256b7fbb6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826622"
---
# <span data-ttu-id="74f5a-103">Настройка баз данных MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="74f5a-103">How to Configure the MBAM 2.5 Databases</span></span>


<span data-ttu-id="74f5a-104">В этой статье объясняется, как настроить соответствие (MBAM) и базу данных аудита Microsoft BitLocker (в 2,5), а также базе данных.</span><span class="sxs-lookup"><span data-stu-id="74f5a-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Compliance and Audit Database and the Recovery Database by using:</span></span>

-   <span data-ttu-id="74f5a-105">Командлет Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74f5a-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="74f5a-106">Мастер настройки сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="74f5a-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="74f5a-107">Инструкции основываются на рекомендованной архитектуре на [высоком уровне архитектуры для MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="74f5a-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="74f5a-108">Прежде чем приступить к настройке, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="74f5a-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="74f5a-109">Шаг</span><span class="sxs-lookup"><span data-stu-id="74f5a-109">Step</span></span></th>
<th align="left"><span data-ttu-id="74f5a-110">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="74f5a-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="74f5a-111">Изучите рекомендованную архитектуру для MBAM.</span><span class="sxs-lookup"><span data-stu-id="74f5a-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="74f5a-112">Высокоуровневая архитектура для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="74f5a-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="74f5a-113">Проверка поддерживаемых конфигураций для MBAM.</span><span class="sxs-lookup"><span data-stu-id="74f5a-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="74f5a-114">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="74f5a-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="74f5a-115">Заполните необходимые условия на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="74f5a-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="74f5a-116">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="74f5a-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="74f5a-117">Требования к серверу MBAM 2,5, применимые только к топологии интеграции Configuration Manager </a> (если применимо)</span><span class="sxs-lookup"><span data-stu-id="74f5a-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="74f5a-118">Установите серверное программное обеспечение MBAM на каждый сервер, на котором вы планируете настроить компонент MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="74f5a-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="74f5a-119">Примечание.</span><span class="sxs-lookup"><span data-stu-id="74f5a-119">Note</span></span></strong><br/><p><span data-ttu-id="74f5a-120">Вы можете установить базы данных на удаленном компьютере SQL Server с помощью Windows PowerShell или пакета экспортированного приложения уровня данных (DAC).</span><span class="sxs-lookup"><span data-stu-id="74f5a-120">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="74f5a-121">Дополнительные сведения о пакетах DAC можно найти в разделе <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> приложения уровня данных </a> .</span><span class="sxs-lookup"><span data-stu-id="74f5a-121">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="74f5a-122">Установка программного обеспечения MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="74f5a-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="74f5a-123">Если вы планируете использовать командлеты Windows PowerShell для настройки функций сервера MBAM, изучите необходимые условия для использования Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="74f5a-123">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="74f5a-124">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74f5a-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="74f5a-125">Настройка баз данных с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74f5a-125">To configure the databases by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="74f5a-126">Прежде чем приступить к настройке, прочтите раздел [Настройка функций сервера MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) , чтобы просмотреть предварительные требования для использования Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="74f5a-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="74f5a-127">С помощью командлета Windows PowerShell **Enable-MbamDatabase** можно настроить базы данных.</span><span class="sxs-lookup"><span data-stu-id="74f5a-127">Use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the databases.</span></span> <span data-ttu-id="74f5a-128">Чтобы получить сведения об этом командлете Windows PowerShell, введите **Get-Help Enable-MbamDatabase**.</span><span class="sxs-lookup"><span data-stu-id="74f5a-128">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamDatabase**.</span></span>

**<span data-ttu-id="74f5a-129">Настройка базы данных соответствия и аудита с помощью мастера</span><span class="sxs-lookup"><span data-stu-id="74f5a-129">To configure the Compliance and Audit Database by using the wizard</span></span>**

1. <span data-ttu-id="74f5a-130">На сервере, на котором вы хотите настроить базы данных, запустите мастер **настройки сервера MBAM** .</span><span class="sxs-lookup"><span data-stu-id="74f5a-130">On the server where you want to configure the databases, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="74f5a-131">Чтобы открыть мастер, вы можете выбрать **MBAM конфигурации сервера** в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="74f5a-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="74f5a-132">Нажмите кнопку **Добавить новые функции**, выберите **соответствие и база данных для проверки соответствия и** **базы данных восстановления**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="74f5a-132">Click **Add New Features**, select **Compliance and Audit Database** and **Recovery Database**, and then click **Next**.</span></span> <span data-ttu-id="74f5a-133">Мастер проверяет, выполнены ли все необходимые условия для баз данных.</span><span class="sxs-lookup"><span data-stu-id="74f5a-133">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="74f5a-134">Если проверка готовности к установке выполнена успешно, нажмите кнопку **Далее** , чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="74f5a-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="74f5a-135">В противном случае устраните недостающие необходимые компоненты и нажмите кнопку **проверить необходимые компоненты еще раз**.</span><span class="sxs-lookup"><span data-stu-id="74f5a-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="74f5a-136">Введите значения полей в мастере, используя следующие описания:</span><span class="sxs-lookup"><span data-stu-id="74f5a-136">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="74f5a-137">Поле</span><span class="sxs-lookup"><span data-stu-id="74f5a-137">Field</span></span></th>
   <th align="left"><span data-ttu-id="74f5a-138">Описание</span><span class="sxs-lookup"><span data-stu-id="74f5a-138">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="74f5a-139">Имя сервера SQL Server</span><span class="sxs-lookup"><span data-stu-id="74f5a-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="74f5a-140">Имя сервера, на котором настраивается база данных соответствия и аудита.</span><span class="sxs-lookup"><span data-stu-id="74f5a-140">Name of the server where you are configuring the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="74f5a-141">Примечание.</span><span class="sxs-lookup"><span data-stu-id="74f5a-141">Note</span></span></strong><br/><p><span data-ttu-id="74f5a-142">Для включения входящего трафика на порт Microsoft SQL Server необходимо добавить исключение на компьютере с базой данных соответствия требованиям и аудита.</span><span class="sxs-lookup"><span data-stu-id="74f5a-142">You must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="74f5a-143">Номер порта по умолчанию — 1433.</span><span class="sxs-lookup"><span data-stu-id="74f5a-143">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="74f5a-144">Экземпляр базы данных SQL Server</span><span class="sxs-lookup"><span data-stu-id="74f5a-144">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="74f5a-145">Имя экземпляра базы данных, в котором будут храниться данные о соответствии и аудите.</span><span class="sxs-lookup"><span data-stu-id="74f5a-145">Name of the database instance where the compliance and audit data will be stored.</span></span> <span data-ttu-id="74f5a-146">Кроме того, необходимо указать, где будут храниться сведения о базе данных.</span><span class="sxs-lookup"><span data-stu-id="74f5a-146">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="74f5a-147">Имя базы данных</span><span class="sxs-lookup"><span data-stu-id="74f5a-147">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="74f5a-148">Имя базы данных, в которой будут храниться данные соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="74f5a-148">Name of the database that will store the compliance data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="74f5a-149">Примечание.</span><span class="sxs-lookup"><span data-stu-id="74f5a-149">Note</span></span></strong><br/><p><span data-ttu-id="74f5a-150">Если вы обновляете предыдущую версию MBAM, вы должны использовать то же имя базы данных, что и для прежнего развертывания.</span><span class="sxs-lookup"><span data-stu-id="74f5a-150">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="74f5a-151">Пользователь или группа доступа для чтения и записи</span><span class="sxs-lookup"><span data-stu-id="74f5a-151">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="74f5a-152">Пользователь или группа домена, у которых есть разрешение на чтение и запись в эту базу данных, чтобы разрешить веб-приложениям доступ к данным и отчетам в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="74f5a-152">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="74f5a-153">Если вы введете в это поле пользователя, оно должно быть таким же, как значение в <strong> поле Учетная запись домена пула приложений веб-службы </strong> на <strong> странице Настройка веб-приложений </strong> .</span><span class="sxs-lookup"><span data-stu-id="74f5a-153">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="74f5a-154">Если в этом поле ввести группу, значение в <strong> поле Учетная запись домена пула приложений веб-службы </strong> на <strong> странице Настройка веб-приложений </strong> должно быть членом группы, введенной в это поле.</span><span class="sxs-lookup"><span data-stu-id="74f5a-154">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="74f5a-155">Пользователь или группа домена "доступ только для чтения"</span><span class="sxs-lookup"><span data-stu-id="74f5a-155">Read-only access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="74f5a-156">Имя пользователя или группы, которым будет предоставлено разрешение только на чтение для этой базы данных, чтобы разрешить этим отчетам получать доступ к данным о соответствии в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="74f5a-156">Name of the user or group that will have read-only permission to this database to enable the reports to access the compliance data in this database.</span></span></p>
   <p><span data-ttu-id="74f5a-157">Если вы введете в это поле пользователя, он должен быть тем же пользователем, который указан в <strong> поле Учетная запись домена базы данных "соответствие требованиям" и "Аудит" </strong> на <strong> странице "Настройка отчетов" </strong> .</span><span class="sxs-lookup"><span data-stu-id="74f5a-157">If you enter a user in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
   <p><span data-ttu-id="74f5a-158">Если вы ввели в это поле группу, значение, указанное в <strong> поле Учетная запись домена базы данных "соответствие требованиям и аудиту" </strong> на <strong> странице "Настройка отчетов", </strong> должно входить в группу, указанную в этом поле.</span><span class="sxs-lookup"><span data-stu-id="74f5a-158">If you enter a group in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="74f5a-159">Перейдите к следующему разделу, чтобы настроить базу данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="74f5a-159">Continue to the next section to configure the Recovery Database.</span></span>

**<span data-ttu-id="74f5a-160">Настройка базы данных восстановления с помощью мастера</span><span class="sxs-lookup"><span data-stu-id="74f5a-160">To configure the Recovery Database by using the wizard</span></span>**

1. <span data-ttu-id="74f5a-161">Введите значения полей в мастере, используя следующие описания:</span><span class="sxs-lookup"><span data-stu-id="74f5a-161">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="74f5a-162">Поле</span><span class="sxs-lookup"><span data-stu-id="74f5a-162">Field</span></span></th>
   <th align="left"><span data-ttu-id="74f5a-163">Описание</span><span class="sxs-lookup"><span data-stu-id="74f5a-163">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="74f5a-164">Имя сервера SQL Server</span><span class="sxs-lookup"><span data-stu-id="74f5a-164">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="74f5a-165">Имя сервера, на котором вы настраиваете базу данных восстановления.</span><span class="sxs-lookup"><span data-stu-id="74f5a-165">Name of the server where you are configuring the Recovery Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="74f5a-166">Примечание.</span><span class="sxs-lookup"><span data-stu-id="74f5a-166">Note</span></span></strong><br/><p><span data-ttu-id="74f5a-167">Необходимо добавить исключение на компьютере с базой данных восстановления, чтобы включить входящий трафик на порт Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="74f5a-167">You must add an exception on the Recovery Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="74f5a-168">Номер порта по умолчанию — 1433.</span><span class="sxs-lookup"><span data-stu-id="74f5a-168">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="74f5a-169">Экземпляр базы данных SQL Server</span><span class="sxs-lookup"><span data-stu-id="74f5a-169">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="74f5a-170">Имя экземпляра базы данных, в котором будут храниться данные для восстановления.</span><span class="sxs-lookup"><span data-stu-id="74f5a-170">Name of the database instance where the recovery data will be stored.</span></span> <span data-ttu-id="74f5a-171">Кроме того, необходимо указать, где будут храниться сведения о базе данных.</span><span class="sxs-lookup"><span data-stu-id="74f5a-171">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="74f5a-172">Имя базы данных</span><span class="sxs-lookup"><span data-stu-id="74f5a-172">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="74f5a-173">Имя базы данных, в которой будут храниться данные для восстановления.</span><span class="sxs-lookup"><span data-stu-id="74f5a-173">Name of the database that will store the recovery data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="74f5a-174">Примечание.</span><span class="sxs-lookup"><span data-stu-id="74f5a-174">Note</span></span></strong><br/><p><span data-ttu-id="74f5a-175">Если вы обновляете предыдущую версию MBAM, вы должны использовать то же имя базы данных, что и для прежнего развертывания.</span><span class="sxs-lookup"><span data-stu-id="74f5a-175">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="74f5a-176">Пользователь или группа доступа для чтения и записи</span><span class="sxs-lookup"><span data-stu-id="74f5a-176">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="74f5a-177">Пользователь или группа домена, у которых есть разрешение на чтение и запись в эту базу данных, чтобы разрешить веб-приложениям доступ к данным и отчетам в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="74f5a-177">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="74f5a-178">Если вы введете в это поле пользователя, оно должно быть таким же, как значение в <strong> поле Учетная запись домена пула приложений веб-службы </strong> на <strong> странице Настройка веб-приложений </strong> .</span><span class="sxs-lookup"><span data-stu-id="74f5a-178">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="74f5a-179">Если в этом поле ввести группу, значение в <strong> поле Учетная запись домена пула приложений веб-службы </strong> на <strong> странице Настройка веб-приложений </strong> должно быть членом группы, введенной в это поле.</span><span class="sxs-lookup"><span data-stu-id="74f5a-179">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="74f5a-180">Когда вы закончите ввод, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="74f5a-180">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="74f5a-181">Мастер проверяет, выполнены ли все необходимые условия для баз данных.</span><span class="sxs-lookup"><span data-stu-id="74f5a-181">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="74f5a-182">Если проверка готовности к установке выполнена успешно, нажмите кнопку **Далее** , чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="74f5a-182">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="74f5a-183">В противном случае устраните недостающие необходимые условия и нажмите кнопку **Далее** .</span><span class="sxs-lookup"><span data-stu-id="74f5a-183">Otherwise, resolve any missing prerequisites, and then click **Next** again.</span></span>

4. <span data-ttu-id="74f5a-184">На странице **сводки** ознакомьтесь с возможностями, которые будут добавлены.</span><span class="sxs-lookup"><span data-stu-id="74f5a-184">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="74f5a-185">Примечание.</span><span class="sxs-lookup"><span data-stu-id="74f5a-185">Note</span></span>**  
   <span data-ttu-id="74f5a-186">Чтобы создать сценарий Windows PowerShell для записей, которые вы только что сделали, нажмите **экспортировать сценарий PowerShell**, а затем сохраните сценарий.</span><span class="sxs-lookup"><span data-stu-id="74f5a-186">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



5. <span data-ttu-id="74f5a-187">Нажмите кнопку **Добавить** , чтобы добавить базы данных MBAM на сервер, а затем нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="74f5a-187">Click **Add** to add the MBAM databases on the server, and then click **Close**.</span></span>



## <span data-ttu-id="74f5a-188">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="74f5a-188">Related topics</span></span>


[<span data-ttu-id="74f5a-189">Журналы событий сервера</span><span class="sxs-lookup"><span data-stu-id="74f5a-189">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="74f5a-190">Настройка компонентов сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="74f5a-190">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="74f5a-191">Настройка отчетов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="74f5a-191">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="74f5a-192">Настройка веб-приложений MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="74f5a-192">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="74f5a-193">Проверка конфигурации компонентов MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="74f5a-193">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="74f5a-194">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="74f5a-194">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="74f5a-195">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="74f5a-195">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="74f5a-196">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="74f5a-196">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





