---
title: Оценка MBAM 1.0
description: Оценка MBAM 1.0
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825252"
---
# <span data-ttu-id="80da5-103">Оценка MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="80da5-103">Evaluating MBAM 1.0</span></span>


<span data-ttu-id="80da5-104">Прежде чем развертывать администрирование и мониторинг Microsoft BitLocker (MBAM) в рабочей среде, вы должны оценить его в лабораторной среде.</span><span class="sxs-lookup"><span data-stu-id="80da5-104">Before you deploy Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a lab environment.</span></span> <span data-ttu-id="80da5-105">В этой статье описано, как настроить MBAM в среде единого сервера лаборатории для целей оценки.</span><span class="sxs-lookup"><span data-stu-id="80da5-105">You can use the information in this topic to set up MBAM in a single server lab environment for evaluation purposes only.</span></span>

<span data-ttu-id="80da5-106">Несмотря на то, что фактические этапы развертывания очень похожи на сценарий, описанный в статье [Установка и настройка MBAM на одном сервере](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), в этом разделе содержатся дополнительные сведения о том, как настроить среду оценки MBAM в течение минимального периода времени.</span><span class="sxs-lookup"><span data-stu-id="80da5-106">While the actual deployment steps are very similar to the scenario that is described in [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), this topic contains additional information to enable you to set up an MBAM evaluation environment in the least amount of time.</span></span>

## <span data-ttu-id="80da5-107">Настройка лабораторной среды</span><span class="sxs-lookup"><span data-stu-id="80da5-107">Set up the Lab Environment</span></span>


<span data-ttu-id="80da5-108">Даже если вы настроили нерабочий экземпляр MBAM для оценки в лабораторной среде, вы должны убедиться, что выполнены необходимые требования к развертыванию, требования к оборудованию и программному обеспечению.</span><span class="sxs-lookup"><span data-stu-id="80da5-108">Even when you set up a non-production instance of MBAM to evaluate in a lab environment, you should still verify that you have met the deployment prerequisites and the hardware and software requirements.</span></span> <span data-ttu-id="80da5-109">Дополнительные сведения можно найти в разделе [MBAM 1,0 требования к развертыванию](mbam-10-deployment-prerequisites.md) и [поддерживаемые конфигурации MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="80da5-109">For more information, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="80da5-110">Кроме того, прежде чем приступить к развертыванию MBAMной пробной версии, вам также следует предварительно [подготовить среду для MBAM 1,0](preparing-your-environment-for-mbam-10.md) .</span><span class="sxs-lookup"><span data-stu-id="80da5-110">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM evaluation deployment.</span></span>

### <span data-ttu-id="80da5-111">Планирование развертывания MBAM Evaluation</span><span class="sxs-lookup"><span data-stu-id="80da5-111">Plan for an MBAM Evaluation Deployment</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="80da5-112">Задача</span><span class="sxs-lookup"><span data-stu-id="80da5-112">Task</span></span></th>
<th align="left"><span data-ttu-id="80da5-113">Ссылки</span><span class="sxs-lookup"><span data-stu-id="80da5-113">References</span></span></th>
<th align="left"><span data-ttu-id="80da5-114">Заметки</span><span class="sxs-lookup"><span data-stu-id="80da5-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="80da5-115">Ознакомьтесь со статьей Приступая к работе с MBAM, чтобы получить основные сведения о продукте перед началом планирования развертывания.</span><span class="sxs-lookup"><span data-stu-id="80da5-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before you begin your deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)"><span data-ttu-id="80da5-116">Начало работы с MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="80da5-116">Getting Started with MBAM 1.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p><span data-ttu-id="80da5-117">Подготовьте рабочую среду для установки MBAM.</span><span class="sxs-lookup"><span data-stu-id="80da5-117">Prepare your computing environment for the MBAM installation.</span></span> <span data-ttu-id="80da5-118">Для этого необходимо включить прозрачное шифрование данных (TDE) для экземпляров SQL Server, которые будут размещаться в MBAM базах данных.</span><span class="sxs-lookup"><span data-stu-id="80da5-118">To do so, you must enable the Transparent Data Encryption (TDE) on the SQL Server instances that will host MBAM databases.</span></span> <span data-ttu-id="80da5-119">Чтобы включить TDE в лабораторной среде, вы можете создать SQL-файл для работы с главной базой данных, размещенной в экземпляре SQL Server, который MBAM будет использовать.</span><span class="sxs-lookup"><span data-stu-id="80da5-119">To enable TDE in your lab environment, you can create a .sql file to run against the master database that is hosted on the instance of the SQL Server that MBAM will use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="80da5-120">Примечание.</span><span class="sxs-lookup"><span data-stu-id="80da5-120">Note</span></span></strong><br/><p><span data-ttu-id="80da5-121">Следующий пример можно использовать для создания SQL-файла для лабораторной среды для быстрого включения TDE на экземпляре SQL Server, на котором будут размещаться базы данных MBAM.</span><span class="sxs-lookup"><span data-stu-id="80da5-121">You can use the following example to create a .sql file for your lab environment to quickly enable TDE on the SQL Server instance that will host the MBAM databases.</span></span> <span data-ttu-id="80da5-122">Эти команды сервера SQL Server будут включать TDE с помощью локального подписанного сертификата SQL Server.</span><span class="sxs-lookup"><span data-stu-id="80da5-122">These SQL Server commands will enable TDE by using a locally signed SQL Server certificate.</span></span> <span data-ttu-id="80da5-123">Убедитесь в том, что резервная копия сертификата TDE и связанного ключа шифрования заданы в примере локального пути резервного копирования для <em> C:\Backup </em> .</span><span class="sxs-lookup"><span data-stu-id="80da5-123">Make sure to back up the TDE certificate and its associated encryption key to the example local backup path of <em>C:\Backup</em>.</span></span> <span data-ttu-id="80da5-124">Сертификат и ключ TDE необходимы при восстановлении базы данных или перемещении сертификата и ключа на другой сервер, на котором TDE шифрование на месте.</span><span class="sxs-lookup"><span data-stu-id="80da5-124">The TDE certificate and key are required when recover the database or move the certificate and key to another server that has TDE encryption in place.</span></span></p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)"><span data-ttu-id="80da5-125">Необходимые компоненты развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="80da5-125">MBAM 1.0 Deployment Prerequisites</span></span></a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)"><span data-ttu-id="80da5-126">Шифрование баз данных в SQL Server 2008 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="80da5-126">Database Encryption in SQL Server 2008 Enterprise Edition</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="80da5-127">Спланируйте и настройте требования к групповой политике MBAM.</span><span class="sxs-lookup"><span data-stu-id="80da5-127">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)"><span data-ttu-id="80da5-128">Планирование требований групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="80da5-128">Planning for MBAM 1.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="80da5-129">Планируйте и создавайте необходимые группы безопасности доменных служб Active Directory и планируйте требования к членству в локальной группе безопасности MBAM.</span><span class="sxs-lookup"><span data-stu-id="80da5-129">Plan for and create the necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="80da5-130">Планирование ролей администратора MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="80da5-130">Planning for MBAM 1.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="80da5-131">Планирование развертывания компонентов сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="80da5-131">Plan for MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)"><span data-ttu-id="80da5-132">Планирование развертывания сервера MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="80da5-132">Planning for MBAM 1.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="80da5-133">Планирование развертывания клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="80da5-133">Plan for MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)"><span data-ttu-id="80da5-134">Планирование развертывания клиента MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="80da5-134">Planning for MBAM 1.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="80da5-135">Выполнение развертывания MBAM Evaluation</span><span class="sxs-lookup"><span data-stu-id="80da5-135">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="80da5-136">После того как вы завершите необходимые установки планирования и программного обеспечения, чтобы подготовить рабочую среду к установке MBAM, вы можете начать развертывание MBAM Evaluation.</span><span class="sxs-lookup"><span data-stu-id="80da5-136">After you complete the necessary planning and software prerequisite installations to prepare your computing environment for an MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="80da5-137">Ознакомьтесь со сведениями о поддерживаемых конфигурациях MBAM, чтобы убедиться, что выбранные клиентские и серверные компьютеры поддерживаются для установки компонента MBAM.</span><span class="sxs-lookup"><span data-stu-id="80da5-137">Review the MBAM supported configurations information to make sure that the selected client and server computers are supported for the MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="80da5-138">Поддерживаемые конфигурации MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="80da5-138">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="80da5-139">Запустите программу установки MBAM, чтобы развернуть компоненты сервера MBAM на одном сервере для ознакомления с целью оценки.</span><span class="sxs-lookup"><span data-stu-id="80da5-139">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)"><span data-ttu-id="80da5-140">Установка и настройка MBAM на одном сервере</span><span class="sxs-lookup"><span data-stu-id="80da5-140">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="80da5-141">Добавьте группы безопасности доменных служб Active Directory, созданные на этапе планирования, в соответствующие локальные группы MBAM локального сервера для нового сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="80da5-141">Add the Active Directory Domain Services security groups that you created during the planning phase to the appropriate local MBAM Server feature local groups on the new MBAM server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="80da5-142">Планирование ролей администраторов MBAM 1,0 </a> и <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Управление РОЛЯМИ администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="80da5-142">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="80da5-143">Создание и развертывание необходимых объектов групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="80da5-143">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="80da5-144">Развертывание объектов групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="80da5-144">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="80da5-145">Развертывание программного обеспечения клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="80da5-145">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="80da5-146">Развертывание клиента MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="80da5-146">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="80da5-147">Настройка компьютеров лаборатории для оценки MBAM</span><span class="sxs-lookup"><span data-stu-id="80da5-147">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="80da5-148">Вы можете изменить параметры частоты в отчетах о состоянии клиента MBAM с помощью редактора реестра.</span><span class="sxs-lookup"><span data-stu-id="80da5-148">You can change the frequency settings on the MBAM Client status reporting by using Registry Editor.</span></span> <span data-ttu-id="80da5-149">Однако эти изменения следует использовать только для целей тестирования.</span><span class="sxs-lookup"><span data-stu-id="80da5-149">However, these modifications should be used for testing purposes only.</span></span>

**<span data-ttu-id="80da5-150">Warning</span><span class="sxs-lookup"><span data-stu-id="80da5-150">Warning</span></span>**  
<span data-ttu-id="80da5-151">В этой статье описано, как изменить реестр Windows с помощью редактора реестра.</span><span class="sxs-lookup"><span data-stu-id="80da5-151">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="80da5-152">Если изменить реестр Windows некорректно, это может привести к серьезным неполадкам, которые могут потребовать повторной установки Windows.</span><span class="sxs-lookup"><span data-stu-id="80da5-152">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="80da5-153">Перед изменением реестра необходимо создать резервную копию файлов реестра (System. dat и User. dat).</span><span class="sxs-lookup"><span data-stu-id="80da5-153">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="80da5-154">Корпорация Майкрософт не несет ответственности за то, что проблемы, которые могут возникнуть при изменении реестра, могут быть устранены.</span><span class="sxs-lookup"><span data-stu-id="80da5-154">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="80da5-155">Изменение реестра на свой страх и риск.</span><span class="sxs-lookup"><span data-stu-id="80da5-155">Change the registry at your own risk.</span></span>



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a><span data-ttu-id="80da5-156">Изменение параметров частоты для отчетов о состоянии клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="80da5-156">Modify the Frequency Settings on MBAM Client Status Reporting</span></span>

<span data-ttu-id="80da5-157">Значения частот для отчетов об пробуждении клиента MBAM и состоянии не менее 90 минут, когда они настроены на использование групповой политики.</span><span class="sxs-lookup"><span data-stu-id="80da5-157">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set to use Group Policy.</span></span> <span data-ttu-id="80da5-158">Вы можете изменить эти частоты на клиентских компьютерах MBAM, изменив реестр Windows, чтобы уменьшить значения, что поможет ускорить тестирование.</span><span class="sxs-lookup"><span data-stu-id="80da5-158">You can change these frequencies on MBAM client computers by editing the Windows registry to lower values, which will help speed up the testing.</span></span> <span data-ttu-id="80da5-159">Чтобы изменить параметры частоты в отчетах о состоянии клиента MBAM, используйте редактор реестра для перехода к **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, измените значения для **ClientWakeupFrequency** и **StatusReportingFrequency** на **1** в качестве минимального поддерживаемого клиентом значения, а затем перезапустите службу клиента управления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="80da5-159">To modify the frequency settings on MBAM Client status reporting, use a registry editor to navigate to **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client supported value, and then restart BitLocker Management Client Service.</span></span> <span data-ttu-id="80da5-160">Когда вы сделаете это изменение, клиент MBAM сообщит каждую минуту.</span><span class="sxs-lookup"><span data-stu-id="80da5-160">When you make this change, the MBAM Client will report every minute.</span></span> <span data-ttu-id="80da5-161">Значения этого параметра можно настроить только в том случае, если это было сделано вручную в реестре.</span><span class="sxs-lookup"><span data-stu-id="80da5-161">You can set values this low only when you do so manually in the registry.</span></span>

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a><span data-ttu-id="80da5-162">Изменение задержки запуска службы клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="80da5-162">Modify the Startup Delay on MBAM Client Service</span></span>

<span data-ttu-id="80da5-163">В дополнение к частотам вывода клиента на пробуждение и отчет о состоянии возникает случайная задержка до 90 минут, когда служба агента клиента MBAM запускается на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="80da5-163">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="80da5-164">Если вы не хотите использовать случайную задержку, создайте параметр **DWORD** для **NoStartupDelay** в разделе **HKLM\\Software\\Microsoft\\MBAM**, установите для него значение **1**, а затем перезапустите службу клиента управления BitLocker.</span><span class="sxs-lookup"><span data-stu-id="80da5-164">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart BitLocker Management Client Service.</span></span>

## <span data-ttu-id="80da5-165">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="80da5-165">Related topics</span></span>


[<span data-ttu-id="80da5-166">Начало работы с MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="80da5-166">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)









