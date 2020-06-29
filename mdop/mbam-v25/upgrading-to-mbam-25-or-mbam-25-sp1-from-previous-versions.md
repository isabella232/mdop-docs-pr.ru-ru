---
title: Обновление с предыдущих версий до MBAM 2.5 или MBAM 2.5 с пакетом обновления 1 (SP1)
description: Обновление с предыдущих версий до MBAM 2.5 или MBAM 2.5 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: a9edb4b8-5d5e-42ab-8db6-619db2878e50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 07a03ebbbfce45f7f69a85000e18ddf1a58e53ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812752"
---
# <span data-ttu-id="652f8-103">Обновление с предыдущих версий до MBAM 2.5 или MBAM 2.5 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="652f8-103">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>


<span data-ttu-id="652f8-104">В этом разделе описывается процесс обновления сервера администрирования и мониторинга Microsoft BitLocker (MBAM) и клиента MBAM из более ранних версий MBAM.</span><span class="sxs-lookup"><span data-stu-id="652f8-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server and the MBAM Client from earlier versions of MBAM.</span></span>

<span data-ttu-id="652f8-105">**Примечание**  Вы можете перейти непосредственно к MBAM 2,5 или MBAM 2,5 SP1 из любой предыдущей версии MBAM.</span><span class="sxs-lookup"><span data-stu-id="652f8-105">**Note** You can upgrade directly to MBAM 2.5 or MBAM 2.5 SP1 from any previous version of MBAM.</span></span>

 

## <span data-ttu-id="652f8-106">Перед началом обновления</span><span class="sxs-lookup"><span data-stu-id="652f8-106">Before you start the upgrade</span></span>


<span data-ttu-id="652f8-107">Прежде чем приступить к обновлению, ознакомьтесь с приведенными ниже сведениями.</span><span class="sxs-lookup"><span data-stu-id="652f8-107">Review the following information before you start the upgrade.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="652f8-108">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="652f8-108">What to know before you start</span></span></th>
<th align="left"><span data-ttu-id="652f8-109">Сведения</span><span class="sxs-lookup"><span data-stu-id="652f8-109">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="652f8-110">Если вы устанавливаете веб-сайты MBAM на одном сервере и веб-службах на другом сервере, вы должны использовать командлеты Windows PowerShell для их настройки.</span><span class="sxs-lookup"><span data-stu-id="652f8-110">If you are installing the MBAM websites on one server and the web services on another server, you have to use Windows PowerShell cmdlets to configure them.</span></span></p></td>
<td align="left"><p><span data-ttu-id="652f8-111">Мастер настройки сервера MBAM не поддерживает настройку сайтов на одном сервере и веб-службах на другом сервере.</span><span class="sxs-lookup"><span data-stu-id="652f8-111">The MBAM Server Configuration wizard does not support configuring the websites on one server and the web services on a different server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="652f8-112">Если вы выполняете обновление до MBAM 2.5 или 2,5 SP1 из MBAM 2.0 или 2,0 SP1 в Windows Server2008 R2, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="652f8-112">If you are upgrading to MBAM2.5 or 2.5 SP1 from MBAM2.0 or 2.0 SP1 in Windows Server2008 R2:</span></span></p>
<p><span data-ttu-id="652f8-113">На веб-сайте администрирования и мониторинга и на портале самообслуживания не будет работать, если вы установите необходимое программное обеспечение .NET Framework 4.5 после того, как на компьютере уже установлены службы Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="652f8-113">The Administration and Monitoring Website and the Self-Service Portal will not work if you install the required .NET Framework4.5 software after Internet Information Services (IIS) is already installed.</span></span></p>
<p><span data-ttu-id="652f8-114">Эта проблема возникает из-за того, что ASP.NET не удается правильно зарегистрировать в службах IIS, если платформа .NET Framework установлена после установки IIS.</span><span class="sxs-lookup"><span data-stu-id="652f8-114">This issue occurs because ASP.NET cannot be registered correctly with IIS if the .NET Framework is installed after IIS has already been installed.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="652f8-115">Чтобы устранить эту проблему, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="652f8-115">To resolve this issue:</span></span></strong></p>
<p><span data-ttu-id="652f8-116">Запустите <strong> Aspnet_regiis — i </strong> из следующего местоположения:</span><span class="sxs-lookup"><span data-stu-id="652f8-116">Run <strong>aspnet_regiis –i</strong> from the following location:</span></span></p>
<p><span data-ttu-id="652f8-117">C:\windows\microsoft.net\Framework\v4.0.30319</span><span class="sxs-lookup"><span data-stu-id="652f8-117">C:\windows\microsoft.net\Framework\v4.0.30319</span></span></p>
<p><span data-ttu-id="652f8-118">Дополнительные сведения можно найти в статье: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)"> ASP.NET средства регистрации IIS </a> .</span><span class="sxs-lookup"><span data-stu-id="652f8-118">For more information, see: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)">ASP.NET IIS Registration Tool</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="652f8-119">Зарегистрируйте SPN в учетной записи пула приложений, если выполняются все указанные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="652f8-119">Register an SPN on the application pool account if all of the following are true:</span></span></p>
<ul>
<li><p><span data-ttu-id="652f8-120">Вы обновляете предыдущую версию MBAM.</span><span class="sxs-lookup"><span data-stu-id="652f8-120">You are upgrading from a previous version of MBAM.</span></span></p></li>
<li><p><span data-ttu-id="652f8-121">В настоящее время вы не работаете с веб-сайтами MBAM в конфигурации с балансировкой нагрузки, но вы хотите сделать это, когда вы обновите систему до MBAM 2.5 или 2,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="652f8-121">Currently, you are not running the MBAM websites in a load-balanced or distributed configuration, but you would like to do so when you upgrade to MBAM2.5 or 2.5 SP1.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="652f8-122">Инструкции можно найти <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)"> в разделе Планирование безопасности веб-сайтов MBAM </a> .</span><span class="sxs-lookup"><span data-stu-id="652f8-122">For instructions, see <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)">Planning How to Secure the MBAM Websites</a>.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="652f8-123">Что мы рекомендуем</span><span class="sxs-lookup"><span data-stu-id="652f8-123">What we recommend</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="652f8-124">Зарегистрируйте имя субъекта-службы (SPN) для учетной записи пула приложений, несмотря на то, что для учетной записи компьютера уже могут быть зарегистрированы SPN.</span><span class="sxs-lookup"><span data-stu-id="652f8-124">Register a service principal name (SPN) for the application pool account, even though you may already have registered SPNs for the machine account.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="652f8-125">Зачем мы рекомендуем</span><span class="sxs-lookup"><span data-stu-id="652f8-125">Why we recommend it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="652f8-126">Регистрация SPN в учетной записи пула приложений требуется для настройки веб-сайтов в балансировке нагрузки или распределенной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="652f8-126">Registering an SPN on the application pool account is required to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="652f8-127">Что произойдет, если в учетной записи компьютера уже настроены SPN?</span><span class="sxs-lookup"><span data-stu-id="652f8-127">What happens if SPNs are already configured on a machine account?</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="652f8-128">MBAM будет использовать уже зарегистрированные SPN, и вам не нужно настраивать дополнительные SPN, но вы не сможете настраивать веб-сайты в балансировке нагрузки или распределенной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="652f8-128">MBAM will use the SPNs that you have already registered, and you don’t need to configure additional SPNs, but you are not able to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="652f8-129">Инструкции по обновлению инфраструктуры сервера MBAM</span><span class="sxs-lookup"><span data-stu-id="652f8-129">Steps to upgrade the MBAM Server infrastructure</span></span>


<span data-ttu-id="652f8-130">Выполните действия, описанные в следующих разделах, чтобы обновить MBAM для изолированной топологии или из топологии интеграции System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="652f8-130">Use the steps in the following sections to upgrade MBAM for the Stand-alone topology or the System Center Configuration Manager Integration topology.</span></span>

**<span data-ttu-id="652f8-131">Обновление инфраструктуры сервера MBAM для изолированной топологии</span><span class="sxs-lookup"><span data-stu-id="652f8-131">To upgrade the MBAM Server infrastructure for Stand-alone topology</span></span>**

1.  <span data-ttu-id="652f8-132">Удалите предыдущие версии MBAM из **программ и компонентов** , а также с веб-серверов, чтобы убедиться в том, что данные не записываются из MBAM клиентов в инфраструктуру MBAM.</span><span class="sxs-lookup"><span data-stu-id="652f8-132">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="652f8-133">Инструкции можно найти в разделе [Удаление функций и программного обеспечения сервера MBAM](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span><span class="sxs-lookup"><span data-stu-id="652f8-133">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="652f8-134">Создавайте резервные копии баз данных.</span><span class="sxs-lookup"><span data-stu-id="652f8-134">Back up your databases.</span></span>

3.  <span data-ttu-id="652f8-135">Удалите предыдущие версии MBAM с сервера SQL Server, используя **программы и компоненты**, в том числе серверы SQL Server, на которых размещены отчеты MBAM, с помощью служб отчетов SQL.</span><span class="sxs-lookup"><span data-stu-id="652f8-135">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="652f8-136">Удалите оставшиеся временные файлы или папки сервера MBAM на сервере базы данных и в службах отчетов.</span><span class="sxs-lookup"><span data-stu-id="652f8-136">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

    <span data-ttu-id="652f8-137">**Примечание**  Базы данных не будут удалены, а все данные о соответствии требованиям и данных о том, как в ней сохраняются.</span><span class="sxs-lookup"><span data-stu-id="652f8-137">**Note** The databases will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

4.  <span data-ttu-id="652f8-138">Установите и настройте базы данных, отчеты и веб-приложения MBAM 2.5 или 2,5 SP1 в нужном порядке.</span><span class="sxs-lookup"><span data-stu-id="652f8-138">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, and web applications, in that order.</span></span> <span data-ttu-id="652f8-139">Базы данных будут обновлены на своем своем расположении.</span><span class="sxs-lookup"><span data-stu-id="652f8-139">The databases are upgraded in place.</span></span>

5.  <span data-ttu-id="652f8-140">Обновите объекты групповой политики (GPO) с помощью шаблонов MBAM 2,5, чтобы использовать новые возможности MBAM, например принудительное шифрование.</span><span class="sxs-lookup"><span data-stu-id="652f8-140">Update the Group Policy Objects (GPOs) using the MBAM 2.5 Templates to leverage the new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="652f8-141">Если не обновить объекты групповой политики и клиент MBAM на MBAM 2,5, более ранние версии клиентов MBAM продолжат сообщать о текущих объектах GPO с ограниченными возможностями.</span><span class="sxs-lookup"><span data-stu-id="652f8-141">If you do not update the GPOs and the MBAM client to MBAM 2.5, earlier versions of MBAM clients will continue to report against your current GPOs with reduced functionality.</span></span> <span data-ttu-id="652f8-142">Узнайте, [как получить шаблоны групповой политики для MDOP (ADMX)](https://www.microsoft.com/download/details.aspx?id=41183) , чтобы скачать последние версии шаблонов ADMX.</span><span class="sxs-lookup"><span data-stu-id="652f8-142">See [How to Get MDOP Group Policy (.admx) Templates](https://www.microsoft.com/download/details.aspx?id=41183) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="652f8-143">После того как вы обновите инфраструктуру сервера MBAM, существующие клиентские компьютеры будут успешно передаваться на сервер MBAM 2.5 или 2,5 с пакетом обновления 1 (SP1), и данные восстановления продолжают храниться.</span><span class="sxs-lookup"><span data-stu-id="652f8-143">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

6.  <span data-ttu-id="652f8-144">Установите последнюю версию клиента MBAM 2.5 или 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="652f8-144">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="652f8-145">После развертывания клиентские компьютеры не нужно перезагружать.</span><span class="sxs-lookup"><span data-stu-id="652f8-145">Client computers do not need to be rebooted after the deployment.</span></span>

**<span data-ttu-id="652f8-146">Обновление инфраструктуры MBAM для топологии интеграции System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="652f8-146">To upgrade the MBAM infrastructure for System Center Configuration Manager Integration topology</span></span>**

1.  <span data-ttu-id="652f8-147">Удалите предыдущие версии MBAM из **программ и компонентов** , а также с веб-серверов, чтобы убедиться в том, что данные не записываются из MBAM клиентов в инфраструктуру MBAM.</span><span class="sxs-lookup"><span data-stu-id="652f8-147">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="652f8-148">Инструкции можно найти в разделе [Удаление функций и программного обеспечения сервера MBAM](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span><span class="sxs-lookup"><span data-stu-id="652f8-148">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="652f8-149">Создавайте резервные копии баз данных.</span><span class="sxs-lookup"><span data-stu-id="652f8-149">Back up your databases.</span></span>

3.  <span data-ttu-id="652f8-150">Удалите предыдущие версии MBAM с сервера SQL Server, используя **программы и компоненты**, в том числе серверы SQL Server, на которых размещены отчеты MBAM, с помощью служб отчетов SQL.</span><span class="sxs-lookup"><span data-stu-id="652f8-150">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="652f8-151">Удалите оставшиеся временные файлы или папки сервера MBAM на сервере базы данных и в службах отчетов.</span><span class="sxs-lookup"><span data-stu-id="652f8-151">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

4.  <span data-ttu-id="652f8-152">Удалите MBAM с сервера Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="652f8-152">Uninstall MBAM from the Configuration Manager server.</span></span>

    <span data-ttu-id="652f8-153">**Примечание**  Базы данных и объекты Configuration Manager (базовые и MBAM Поддерживаемые семейства компьютеров и отчеты) не будут удалены, а все данные о соответствии требованиям и восстановлении сохраняются в базе данных.</span><span class="sxs-lookup"><span data-stu-id="652f8-153">**Note** The databases and the Configuration Manager objects (baseline, MBAM supported computers collection, and Reports) will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

5.  <span data-ttu-id="652f8-154">Обновите файлы. mof.</span><span class="sxs-lookup"><span data-stu-id="652f8-154">Update the .mof files.</span></span>

6.  <span data-ttu-id="652f8-155">Установка и настройка баз данных, отчетов, веб-приложений и интеграции Configuration Manager в MBAM 2.5 или 2,5 SP1, а также в том же порядке.</span><span class="sxs-lookup"><span data-stu-id="652f8-155">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, web applications, and Configuration Manager integration, in that order.</span></span> <span data-ttu-id="652f8-156">Базы данных и объекты Configuration Manager обновлены на своем своем расположении.</span><span class="sxs-lookup"><span data-stu-id="652f8-156">The databases and Configuration Manager objects are upgraded in place.</span></span>

7.  <span data-ttu-id="652f8-157">При необходимости обновите объекты групповой политики (GPO) и измените параметры, если вы хотите реализовать новые функции в MBAM, например принудительное шифрование.</span><span class="sxs-lookup"><span data-stu-id="652f8-157">Optionally, update the Group Policy Objects (GPOs), and edit the settings if you want to implement new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="652f8-158">Если вы не обновите объекты групповой политики, MBAM сохранится о текущих объектах GPO.</span><span class="sxs-lookup"><span data-stu-id="652f8-158">If you do not update the GPOs, MBAM will continue to report against your current GPOs.</span></span> <span data-ttu-id="652f8-159">Узнайте, [как получить шаблоны групповой политики для MDOP (ADMX)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) , чтобы скачать последние версии шаблонов ADMX.</span><span class="sxs-lookup"><span data-stu-id="652f8-159">See [How to Get MDOP Group Policy (.admx) Templates](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="652f8-160">После того как вы обновите инфраструктуру сервера MBAM, существующие клиентские компьютеры будут успешно передаваться на сервер MBAM 2.5 или 2,5 с пакетом обновления 1 (SP1), и данные восстановления продолжают храниться.</span><span class="sxs-lookup"><span data-stu-id="652f8-160">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

8.  <span data-ttu-id="652f8-161">Установите последнюю версию клиента MBAM 2.5 или 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="652f8-161">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="652f8-162">После развертывания клиентские компьютеры не нужно перезагружать.</span><span class="sxs-lookup"><span data-stu-id="652f8-162">Client computers do not need to be rebooted after the deployment.</span></span>

## <span data-ttu-id="652f8-163">Поддержка обновления для клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="652f8-163">Upgrade support for the MBAM Client</span></span>


<span data-ttu-id="652f8-164">MBAM поддерживает обновления для клиента MBAM 2.5 из любой более ранней версии клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="652f8-164">MBAM supports upgrades to the MBAM2.5 Client from any earlier version of the MBAM Client.</span></span>

**<span data-ttu-id="652f8-165">Способы установки клиента MBAM:</span><span class="sxs-lookup"><span data-stu-id="652f8-165">Ways to install the MBAM Client:</span></span>**

-   <span data-ttu-id="652f8-166">После установки серверной инфраструктуры MBAM 2.5 Обновите компьютеры, на которых работает клиент MBAM, или постепенно.</span><span class="sxs-lookup"><span data-stu-id="652f8-166">Upgrade the computers running MBAM Client all at once or gradually after you install the MBAM2.5 Server infrastructure.</span></span>

-   <span data-ttu-id="652f8-167">Установите клиент MBAM через электронную систему распространения программного обеспечения или с помощью таких средств, как доменные службы Active Directory или System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="652f8-167">Install the MBAM Client through an electronic software distribution system or through tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>



## <span data-ttu-id="652f8-168">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="652f8-168">Related topics</span></span>


[<span data-ttu-id="652f8-169">Развертывание MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="652f8-169">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="652f8-170">Развертывание клиента MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="652f8-170">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="652f8-171">Настройка компонентов сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="652f8-171">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="652f8-172">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="652f8-172">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="652f8-173">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="652f8-173">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="652f8-174">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="652f8-174">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





