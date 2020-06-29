---
title: Настройка интеграции System Center Configuration Manager с MBAM 2.5
description: Настройка интеграции System Center Configuration Manager с MBAM 2.5
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812445"
---
# <span data-ttu-id="439be-103">Настройка интеграции System Center Configuration Manager с MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="439be-103">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span>


<span data-ttu-id="439be-104">В этой статье объясняется, как настроить администрирование и мониторинг Microsoft BitLocker (MBAM), чтобы использовать топологию интеграции System Center Configuration Manager, которая интегрирует MBAM с Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="439be-104">This topic explains how to configure Microsoft BitLocker Administration and Monitoring (MBAM) to use the System Center Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span>

<span data-ttu-id="439be-105">В этой статье объясняется, как настроить интеграцию Configuration Manager с помощью:</span><span class="sxs-lookup"><span data-stu-id="439be-105">The instructions explain how to configure Configuration Manager Integration by using:</span></span>

-   <span data-ttu-id="439be-106">Командлет Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="439be-106">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="439be-107">Мастер настройки сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="439be-107">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="439be-108">Инструкции основываются на рекомендованной архитектуре на [высоком уровне архитектуры для MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="439be-108">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="439be-109">Прежде чем приступить к настройке, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="439be-109">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="439be-110">Шаг</span><span class="sxs-lookup"><span data-stu-id="439be-110">Step</span></span></th>
<th align="left"><span data-ttu-id="439be-111">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="439be-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="439be-112">Изучите рекомендованную архитектуру для MBAM.</span><span class="sxs-lookup"><span data-stu-id="439be-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)"><span data-ttu-id="439be-113">Высокоуровневая архитектура MBAM 2.5 с топологией интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="439be-113">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="439be-114">Проверка поддерживаемых конфигураций для MBAM.</span><span class="sxs-lookup"><span data-stu-id="439be-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="439be-115">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="439be-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="439be-116">Заполните необходимые условия на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="439be-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="439be-117">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="439be-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="439be-118">Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="439be-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="439be-119">Установка программного обеспечения сервера MBAM на каждый сервер, на котором будет настроена функция сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="439be-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="439be-120">Примечание.</span><span class="sxs-lookup"><span data-stu-id="439be-120">Note</span></span></strong><br/><p><span data-ttu-id="439be-121">Для этой топологии необходимо установить консоль Configuration Manager на компьютере, на котором устанавливается программное обеспечение сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="439be-121">For this topology, you must install the Configuration Manager console on the computer where you are installing the MBAM Server software.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="439be-122">Установка программного обеспечения MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="439be-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="439be-123">Изучите предварительные требования для Windows PowerShell (применимо только в том случае, если вы собираетесь использовать командлеты Windows PowerShell для настройки MBAM).</span><span class="sxs-lookup"><span data-stu-id="439be-123">Review Windows PowerShell prerequisites (applicable only if you are going to use Windows PowerShell cmdlets to configure MBAM).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="439be-124">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="439be-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="439be-125">Настройка интеграции Configuration Manager с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="439be-125">To configure Configuration Manager Integration by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="439be-126">Прежде чем приступить к настройке, прочтите раздел [Настройка функций сервера MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) , чтобы просмотреть предварительные требования для использования Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="439be-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="439be-127">С помощью командлета Windows PowerShell **Enable-MbamCMIntegration** можно настроить отчеты.</span><span class="sxs-lookup"><span data-stu-id="439be-127">Use the **Enable-MbamCMIntegration** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="439be-128">Чтобы получить сведения об этом командлете, введите **Get-Help Enable-MbamCMIntegration**.</span><span class="sxs-lookup"><span data-stu-id="439be-128">To get information about this cmdlet, type **Get-Help Enable-MbamCMIntegration**.</span></span>

**<span data-ttu-id="439be-129">Настройка интеграции System Center Configuration Manager с помощью мастера</span><span class="sxs-lookup"><span data-stu-id="439be-129">To configure the System Center Configuration Manager Integration by using the wizard</span></span>**

1.  <span data-ttu-id="439be-130">На сервере, на котором вы хотите настроить функцию интеграции System Center Configuration Manager, запустите мастер настройки сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="439be-130">On the server where you want to configure the System Center Configuration Manager Integration feature, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="439be-131">Чтобы открыть мастер, вы можете выбрать **MBAM конфигурации сервера** в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="439be-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2.  <span data-ttu-id="439be-132">Нажмите кнопку **Добавить новые функции**, выберите **Интеграция System Center Configuration Manager**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="439be-132">Click **Add New Features**, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

    <span data-ttu-id="439be-133">Мастер проверяет, выполнены ли все необходимые условия для интеграции Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="439be-133">The wizard checks that all prerequisites for the Configuration Manager Integration have been met.</span></span>

3.  <span data-ttu-id="439be-134">Если проверка готовности к установке выполнена успешно, нажмите кнопку **Далее** , чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="439be-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="439be-135">В противном случае устраните недостающие необходимые компоненты и нажмите кнопку **проверить необходимые компоненты еще раз**.</span><span class="sxs-lookup"><span data-stu-id="439be-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4.  <span data-ttu-id="439be-136">Чтобы ввести значения полей в мастере, воспользуйтесь приведенными ниже описаниями.</span><span class="sxs-lookup"><span data-stu-id="439be-136">Use the following descriptions to enter the field values in the wizard:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="439be-137">Поле</span><span class="sxs-lookup"><span data-stu-id="439be-137">Field</span></span></th>
    <th align="left"><span data-ttu-id="439be-138">Описание</span><span class="sxs-lookup"><span data-stu-id="439be-138">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="439be-139">Сервер служб SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="439be-139">SQL Server Reporting Services server</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="439be-140">Полное доменное имя (FQDN) сервера с ролью точки обслуживания отчетов.</span><span class="sxs-lookup"><span data-stu-id="439be-140">Fully qualified domain name (FQDN) of the server with the Reporting Service point role.</span></span> <span data-ttu-id="439be-141">Это сервер, на который развертываются отчеты диспетчера конфигураций MBAM.</span><span class="sxs-lookup"><span data-stu-id="439be-141">This is the server to which the MBAM Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="439be-142">Если вы не указали сервер, отчеты Configuration Manager будут развернуты на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="439be-142">If you don’t specify a server, the Configuration Manager Reports will be deployed to the local server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="439be-143">Экземпляр служб SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="439be-143">SQL Server Reporting Services instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="439be-144">Имя экземпляра служб SQL Server Reporting Services (SSRS), в котором развертываются отчеты Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="439be-144">Name of the SQL Server Reporting Services (SSRS) instance where the Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="439be-145">Если экземпляр не указан, отчеты Configuration Manager будут развернуты в имени экземпляра служб SSRS по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="439be-145">If you don’t specify an instance, the Configuration Manager Reports will be deployed to the default SSRS instance name.</span></span> <span data-ttu-id="439be-146">Введенное значение игнорируется, если на сервере установлен System Center 2012 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="439be-146">The value you enter is ignored if the server has System Center 2012 Configuration Manager installed.</span></span></p></td>
    </tr>
    </tbody>
    </table>



5.  <span data-ttu-id="439be-147">На странице **сводки** ознакомьтесь с возможностями, которые будут добавлены.</span><span class="sxs-lookup"><span data-stu-id="439be-147">On the **Summary** page, review the features that will be added.</span></span>

    **<span data-ttu-id="439be-148">Примечание.</span><span class="sxs-lookup"><span data-stu-id="439be-148">Note</span></span>**  
    <span data-ttu-id="439be-149">Чтобы создать сценарий Windows PowerShell для только что сделанных записей, нажмите **экспортировать сценарий PowerShell** и сохранить сценарий.</span><span class="sxs-lookup"><span data-stu-id="439be-149">To create a Windows PowerShell script of the entries you just made, click **Export PowerShell Script** and save the script.</span></span>



6.  <span data-ttu-id="439be-150">Нажмите кнопку **Добавить** , чтобы добавить компонент интеграции Configuration Manager на сервер, а затем нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="439be-150">Click **Add** to add the Configuration Manager Integration feature to the server, and then click **Close**.</span></span>



## <span data-ttu-id="439be-151">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="439be-151">Related topics</span></span>


[<span data-ttu-id="439be-152">Настройка компонентов сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="439be-152">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="439be-153">Проверка конфигурации компонентов MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="439be-153">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="439be-154">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="439be-154">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="439be-155">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="439be-155">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="439be-156">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="439be-156">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






