---
title: Оценка MBAM 2.0
description: Оценка MBAM 2.0
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824739"
---
# <span data-ttu-id="f1f73-103">Оценка MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f1f73-103">Evaluating MBAM 2.0</span></span>


<span data-ttu-id="f1f73-104">Прежде чем развертывать администрирование и мониторинг Microsoft BitLocker (MBAM) в рабочей среде, вы должны оценить ее в тестовой среде.</span><span class="sxs-lookup"><span data-stu-id="f1f73-104">Before deploying Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a test environment.</span></span> <span data-ttu-id="f1f73-105">Сведения в этом разделе можно использовать для настройки администрирования Microsoft BitLocker и наблюдения за изолированной топологией в односерверной тестовой среде только для целей оценки.</span><span class="sxs-lookup"><span data-stu-id="f1f73-105">The information in this topic can be used to set up Microsoft BitLocker Administration and Monitoring with a Stand-alone topology in a single-server test environment for evaluation purposes only.</span></span> <span data-ttu-id="f1f73-106">Односерверная топология не рекомендуется для рабочих сред.</span><span class="sxs-lookup"><span data-stu-id="f1f73-106">A single-server topology is not recommended for production environments.</span></span>

<span data-ttu-id="f1f73-107">Инструкции по развертыванию MBAM в тестовой среде можно найти в разделе [Установка и настройка MBAM на одном сервере](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="f1f73-107">For instructions on deploying MBAM in a test environment, see [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).</span></span>

## <span data-ttu-id="f1f73-108">Настройка тестовой среды</span><span class="sxs-lookup"><span data-stu-id="f1f73-108">Setting up the Test Environment</span></span>


<span data-ttu-id="f1f73-109">Несмотря на то, что вы настраиваете нерабочий экземпляр MBAM для оценки в тестовой среде, вы должны убедиться, что выполнены необходимые условия и требования к оборудованию и программному обеспечению.</span><span class="sxs-lookup"><span data-stu-id="f1f73-109">Even though you are setting up a non-production instance of MBAM to evaluate in a test environment, you should still verify that you have met the prerequisites and hardware and software requirements.</span></span> <span data-ttu-id="f1f73-110">Прежде чем приступить к установке, ознакомьтесь с [требованиями к развертыванию MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2,0 поддерживаемые конфигурации](mbam-20-supported-configurations-mbam-2.md)и [подготовки среды для MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="f1f73-110">Before you start the installation, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md), and [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md).</span></span>

### <span data-ttu-id="f1f73-111">Планирование развертывания MBAM Evaluation</span><span class="sxs-lookup"><span data-stu-id="f1f73-111">Plan for an MBAM Evaluation Deployment</span></span>

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
<th align="left"><span data-ttu-id="f1f73-112">Задача</span><span class="sxs-lookup"><span data-stu-id="f1f73-112">Task</span></span></th>
<th align="left"><span data-ttu-id="f1f73-113">Ссылки</span><span class="sxs-lookup"><span data-stu-id="f1f73-113">References</span></span></th>
<th align="left"><span data-ttu-id="f1f73-114">Заметки</span><span class="sxs-lookup"><span data-stu-id="f1f73-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f1f73-115">Ознакомьтесь со статьей Приступая к работе с MBAM, чтобы получить основные сведения о продукте перед началом планирования развертывания.</span><span class="sxs-lookup"><span data-stu-id="f1f73-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before beginning deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)"><span data-ttu-id="f1f73-116">Начало работы с MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f1f73-116">Getting Started with MBAM 2.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f1f73-117">Планируйте требования к развертыванию MBAM 2,0 и подготовьте свою рабочую среду.</span><span class="sxs-lookup"><span data-stu-id="f1f73-117">Plan for MBAM 2.0 Deployment Prerequisites and prepare your computing environment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)"><span data-ttu-id="f1f73-118">Необходимые условия для развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f1f73-118">MBAM 2.0 Deployment Prerequisites</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f1f73-119">Спланируйте и настройте требования к групповой политике MBAM.</span><span class="sxs-lookup"><span data-stu-id="f1f73-119">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="f1f73-120">Планирование требований групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f1f73-120">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f1f73-121">Планируйте и создавайте необходимые группы безопасности ActiveDirectoryDomainServices и планируйте требования к членству в локальной группе безопасности MBAM.</span><span class="sxs-lookup"><span data-stu-id="f1f73-121">Plan for and create necessary ActiveDirectoryDomainServices security groups, and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="f1f73-122">Планирование ролей администратора MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f1f73-122">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f1f73-123">Планирование развертывания компонентов сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="f1f73-123">Plan for deploying MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)"><span data-ttu-id="f1f73-124">Планирование развертывания сервера MBAM 2.0 Server</span><span class="sxs-lookup"><span data-stu-id="f1f73-124">Planning for MBAM 2.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f1f73-125">Планируйте развертывание клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="f1f73-125">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="f1f73-126">Планирование развертывания клиента MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f1f73-126">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f1f73-127">Выполнение развертывания MBAM Evaluation</span><span class="sxs-lookup"><span data-stu-id="f1f73-127">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="f1f73-128">После того как вы заполните необходимые настройки планирования и программного обеспечения для подготовки вычислительной среды к установке MBAM, вы можете начать развертывание MBAM Evaluation.</span><span class="sxs-lookup"><span data-stu-id="f1f73-128">After completing the necessary planning and software prerequisite installations to prepare your computing environment for the MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

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
<td align="left"><p><span data-ttu-id="f1f73-129">Ознакомьтесь со сведениями о конфигурации MBAM, чтобы убедиться, что выбранные клиентские и серверные компьютеры поддерживаются для установки компонента MBAM.</span><span class="sxs-lookup"><span data-stu-id="f1f73-129">Review the MBAM supported configurations information to make sure that selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="f1f73-130">Поддерживаемые конфигурации MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f1f73-130">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f1f73-131">Запустите программу установки MBAM, чтобы развернуть компоненты сервера MBAM на одном сервере для ознакомления с целью оценки.</span><span class="sxs-lookup"><span data-stu-id="f1f73-131">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)"><span data-ttu-id="f1f73-132">Установка и настройка MBAM на одном сервере</span><span class="sxs-lookup"><span data-stu-id="f1f73-132">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f1f73-133">Добавляйте группы безопасности ActiveDirectoryDomainServices, созданные на этапе планирования, в соответствующие локальные группы MBAM на новом сервере MBAM.</span><span class="sxs-lookup"><span data-stu-id="f1f73-133">Add ActiveDirectoryDomainServices security groups, that you created during the planning phase, to the appropriate local MBAM Server feature local groups on the new MBAM Server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="f1f73-134">Планирование ролей администраторов MBAM 2,0 </a> и <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Управление РОЛЯМИ администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="f1f73-134">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f1f73-135">Создание и развертывание необходимых объектов групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="f1f73-135">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="f1f73-136">Развертывание объектов групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f1f73-136">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f1f73-137">Развертывание программного обеспечения клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="f1f73-137">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="f1f73-138">Развертывание клиента MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f1f73-138">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f1f73-139">Настройка компьютеров лаборатории для оценки MBAM</span><span class="sxs-lookup"><span data-stu-id="f1f73-139">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="f1f73-140">В этом разделе содержатся сведения, с помощью которых можно ускорить создание отчетов о состоянии клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="f1f73-140">This section contains information that can be used to speed up the MBAM Client status reporting.</span></span> <span data-ttu-id="f1f73-141">Однако эти изменения следует использовать только для целей тестирования.</span><span class="sxs-lookup"><span data-stu-id="f1f73-141">However, these modifications should be used for testing purposes only.</span></span>

<span data-ttu-id="f1f73-142">**Примечание**  В разделе сведения, приведенные в этой статье, описано, как изменить реестр Windows.</span><span class="sxs-lookup"><span data-stu-id="f1f73-142">**Note** The information in following section describes how to modify the Windows registry.</span></span> <span data-ttu-id="f1f73-143">Неправильное использование редактора реестра может привести к серьезным неполадкам, которые могут потребовать повторной установки Windows.</span><span class="sxs-lookup"><span data-stu-id="f1f73-143">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="f1f73-144">Корпорация Майкрософт не гарантирует, что проблемы, возникающие в результате неправильного использования редактора реестра, могут быть устранены.</span><span class="sxs-lookup"><span data-stu-id="f1f73-144">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="f1f73-145">Ответственность за использование редактора реестра.</span><span class="sxs-lookup"><span data-stu-id="f1f73-145">Use Registry Editor at your own risk.</span></span>

 

### <span data-ttu-id="f1f73-146">Изменение параметров частоты отчетов о состоянии клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="f1f73-146">Modify MBAM Client Status Reporting Frequency Settings</span></span>

<span data-ttu-id="f1f73-147">Значения частот для отчетов об пробуждении клиента MBAM и состоянии в 90 минут заданы с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="f1f73-147">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set using Group Policy.</span></span> <span data-ttu-id="f1f73-148">Вы можете использовать реестр Windows, чтобы изменить эти частоты на более низкие значения на клиентских компьютерах MBAM, чтобы ускорить тестирование.</span><span class="sxs-lookup"><span data-stu-id="f1f73-148">You can use the Windows registry to change these frequencies to a lower value on MBAM client computers to help speed up testing.</span></span>

<span data-ttu-id="f1f73-149">Чтобы изменить параметры частоты отчета о состоянии клиента MBAM, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f1f73-149">To modify the MBAM Client status reporting frequency settings:</span></span>

1.  <span data-ttu-id="f1f73-150">С помощью редактора реестра перейдите в **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.</span><span class="sxs-lookup"><span data-stu-id="f1f73-150">Use a registry editor to navigate to **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.</span></span>

2.  <span data-ttu-id="f1f73-151">Измените значения для **ClientWakeupFrequency** и **StatusReportingFrequency** на **1** в качестве минимального значения, поддерживаемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="f1f73-151">Change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client-supported value.</span></span> <span data-ttu-id="f1f73-152">Это изменение приводит к тому, что клиент MBAM сообщает каждую минуту.</span><span class="sxs-lookup"><span data-stu-id="f1f73-152">This change causes the MBAM Client to report every minute.</span></span>

3.  <span data-ttu-id="f1f73-153">Перезапустите **службу клиента управления BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="f1f73-153">Restart **BitLocker Management Client Service**.</span></span>

<span data-ttu-id="f1f73-154">**Примечание**  Чтобы установить этот низкий значения, необходимо вручную настроить их в реестре.</span><span class="sxs-lookup"><span data-stu-id="f1f73-154">**Note** To set values that are this low, you must set them in the registry manually.</span></span>

 

### <span data-ttu-id="f1f73-155">Изменение задержки запуска службы клиента MBAM</span><span class="sxs-lookup"><span data-stu-id="f1f73-155">Modify MBAM Client Service Startup Delay</span></span>

<span data-ttu-id="f1f73-156">В дополнение к частотам вывода клиента на пробуждение и отчет о состоянии возникает случайная задержка до 90 минут, когда служба агента клиента MBAM запускается на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="f1f73-156">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="f1f73-157">Если вы не хотите использовать случайную задержку, создайте параметр **DWORD** для **NoStartupDelay** в разделе **HKLM\\Software\\Microsoft\\MBAM**, установите для него значение **1**, а затем перезапустите **службу клиента управления BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="f1f73-157">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="f1f73-158">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f1f73-158">Related topics</span></span>


[<span data-ttu-id="f1f73-159">Начало работы с MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f1f73-159">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





