---
title: Контрольный список планирования MBAM 2.5
description: Контрольный список планирования MBAM 2.5
author: dansimp
ms.assetid: ffe11eb8-44db-4886-8300-6dffec8bcfa4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 505f2890d67f36056ab5bb87df2a894473cd3306
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826542"
---
# <span data-ttu-id="4230c-103">Контрольный список планирования MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4230c-103">MBAM 2.5 Planning Checklist</span></span>


<span data-ttu-id="4230c-104">С помощью перечисленных ниже контрольных списков вы можете подготовить рабочую среду для развертывания Microsoft BitLocker (Администрирование и мониторинг) (MBAM).</span><span class="sxs-lookup"><span data-stu-id="4230c-104">You can use the following checklists to help you prepare your computing environment for the Microsoft BitLocker Administration and Monitoring (MBAM) deployment.</span></span> <span data-ttu-id="4230c-105">Контрольные списки предоставляют высокоуровневый список элементов, которые необходимо предусмотреть при планировании развертывания.</span><span class="sxs-lookup"><span data-stu-id="4230c-105">The checklists provide a high-level list of items to consider when planning the deployment.</span></span> <span data-ttu-id="4230c-106">Для изолированной топологии и топологии интеграции Configuration Manager есть отдельные контрольные списки.</span><span class="sxs-lookup"><span data-stu-id="4230c-106">There are separate checklists for the Stand-alone topology and the Configuration Manager Integration topology.</span></span> <span data-ttu-id="4230c-107">Вам может потребоваться скопировать нужный контрольный список в электронную таблицу и настроить его для использования.</span><span class="sxs-lookup"><span data-stu-id="4230c-107">You might want to copy the desired checklist into a spreadsheet and customize it for your use.</span></span>

**<span data-ttu-id="4230c-108">Контрольный список планирования для развертывания MBAM</span><span class="sxs-lookup"><span data-stu-id="4230c-108">Planning checklist for an MBAM deployment</span></span>**

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
<th align="left"><span data-ttu-id="4230c-109">Задача</span><span class="sxs-lookup"><span data-stu-id="4230c-109">Task</span></span></th>
<th align="left"><span data-ttu-id="4230c-110">Ссылки</span><span class="sxs-lookup"><span data-stu-id="4230c-110">References</span></span></th>
<th align="left"><span data-ttu-id="4230c-111">Заметки</span><span class="sxs-lookup"><span data-stu-id="4230c-111">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-112">&quot; &quot; Прежде чем приступить к планированию развертывания, ознакомьтесь со сведениями о начале работы, чтобы ознакомиться с продуктом.</span><span class="sxs-lookup"><span data-stu-id="4230c-112">Review the &quot;Getting started&quot; information to understand the product before you start deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-25.md" data-raw-source="[Getting Started with MBAM 2.5](getting-started-with-mbam-25.md)"><span data-ttu-id="4230c-113">Начало работы с MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4230c-113">Getting Started with MBAM 2.5</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-114">Ознакомьтесь с рекомендуемой архитектурой высокого уровня для развертывания MBAM.</span><span class="sxs-lookup"><span data-stu-id="4230c-114">Review the recommended high-level architecture for an MBAM deployment.</span></span> <span data-ttu-id="4230c-115">Кроме того, может потребоваться просмотреть иллюстрацию и описание отдельных частей (баз данных, веб-сайтов, отчетов) развертывания MBAM.</span><span class="sxs-lookup"><span data-stu-id="4230c-115">You might also want to review an illustration and description of the individual parts (databases, websites, Reports) of an MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="4230c-116">Высокоуровневая архитектура для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4230c-116">High-Level Architecture for MBAM 2.5</span></span></a></p>
<p><a href="illustrated-features-of-an-mbam-25-deployment.md" data-raw-source="[Illustrated Features of an MBAM 2.5 Deployment](illustrated-features-of-an-mbam-25-deployment.md)"><span data-ttu-id="4230c-117">Иллюстрированные функции развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4230c-117">Illustrated Features of an MBAM 2.5 Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-118">Проверьте и заполните необходимые требования для топологий интеграции MBAM и Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4230c-118">Review and complete the prerequisites for the MBAM Stand-alone and Configuration Manager Integration topologies.</span></span></p></td>
<td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="4230c-119">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="4230c-119">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-120">Если вы планируете использовать топологию интеграции Configuration Manager, выполните дополнительные требования, которые применяются только к этой топологии.</span><span class="sxs-lookup"><span data-stu-id="4230c-120">If you plan to use the Configuration Manager Integration topology, complete the additional prerequisites that apply only to this topology.</span></span></p></td>
<td align="left"><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="4230c-121">Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций</span><span class="sxs-lookup"><span data-stu-id="4230c-121">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-122">Ознакомьтесь с требованиями для MBAM 2,5 для клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="4230c-122">Review and meet the MBAM 2.5 prerequisites for the MBAM Client.</span></span></p></td>
<td align="left"><p><a href="prerequisites-for-mbam-25-clients.md" data-raw-source="[Prerequisites for MBAM 2.5 Clients](prerequisites-for-mbam-25-clients.md)"><span data-ttu-id="4230c-123">Необходимые условия для клиентов MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4230c-123">Prerequisites for MBAM 2.5 Clients</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-124">Спланируйте и настройте требования к групповой политике MBAM.</span><span class="sxs-lookup"><span data-stu-id="4230c-124">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="4230c-125">Планирование требований групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4230c-125">Planning for MBAM 2.5 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-126">Планируйте и создавайте необходимые группы безопасности ActiveDirectoryDomainServices.</span><span class="sxs-lookup"><span data-stu-id="4230c-126">Plan for and create the necessary ActiveDirectoryDomainServices security groups.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"><span data-ttu-id="4230c-127">Планирование групп и учетных записей MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4230c-127">Planning for MBAM 2.5 Groups and Accounts</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-128">Спланируйте, как будут защищаться веб-сайты MBAM.</span><span class="sxs-lookup"><span data-stu-id="4230c-128">Plan how you will secure the MBAM websites.</span></span></p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"><span data-ttu-id="4230c-129">Планирование защиты веб-сайтов MBAM</span><span class="sxs-lookup"><span data-stu-id="4230c-129">Planning How to Secure the MBAM Websites</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-130">Проверьте конфигурации, поддерживаемые MBAM, чтобы убедиться, что оборудование соответствует требованиям к системе установки.</span><span class="sxs-lookup"><span data-stu-id="4230c-130">Review the MBAM Supported Configurations to ensure that your hardware meets the installation system requirements.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="4230c-131">Поддерживаемые конфигурации MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4230c-131">MBAM 2.5 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-132">Ознакомьтесь с замечаниями по развертыванию функций сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="4230c-132">Review the considerations for deploying the MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-server-deployment.md" data-raw-source="[Planning for MBAM 2.5 Server Deployment](planning-for-mbam-25-server-deployment.md)"><span data-ttu-id="4230c-133">Планирование развертывания сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="4230c-133">Planning for MBAM 2.5 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-134">Ознакомьтесь с замечаниями по развертыванию клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="4230c-134">Review the considerations for deploying the MBAM Client.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-client-deployment.md" data-raw-source="[Planning for MBAM 2.5 Client Deployment](planning-for-mbam-25-client-deployment.md)"><span data-ttu-id="4230c-135">Планирование развертывания клиента MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4230c-135">Planning for MBAM 2.5 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-136">Проанализируйте требования и шаги, чтобы развернуть MBAM в конфигурации с высокой доступностью.</span><span class="sxs-lookup"><span data-stu-id="4230c-136">Review the requirements and steps to deploy MBAM in a highly available configuration.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-high-availability.md" data-raw-source="[Planning for MBAM 2.5 High Availability](planning-for-mbam-25-high-availability.md)"><span data-ttu-id="4230c-137">Планирование высокой доступности MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4230c-137">Planning for MBAM 2.5 High Availability</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-138">Ознакомьтесь с MBAMми безопасности, относящимися к доверенному платформенному модулю, файлам журналов и прозрачному шифрованию данных.</span><span class="sxs-lookup"><span data-stu-id="4230c-138">Review the MBAM security considerations that pertain to the Trusted Platform Module, log files, and transparent data encryption.</span></span></p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"><span data-ttu-id="4230c-139">Процедуры безопасности MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4230c-139">MBAM 2.5 Security Considerations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="4230c-140">Кроме того, изучите шаги, которые необходимо выполнить, чтобы вычислить MBAM в тестовой среде.</span><span class="sxs-lookup"><span data-stu-id="4230c-140">Optionally, review the steps to evaluate MBAM in a test environment.</span></span></p></td>
<td align="left"><p><a href="evaluating-mbam-25-in-a-test-environment.md" data-raw-source="[Evaluating MBAM 2.5 in a Test Environment](evaluating-mbam-25-in-a-test-environment.md)"><span data-ttu-id="4230c-141">Оценка MBAM 2.5 в тестовой среде</span><span class="sxs-lookup"><span data-stu-id="4230c-141">Evaluating MBAM 2.5 in a Test Environment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="4230c-142">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4230c-142">Related topics</span></span>


[<span data-ttu-id="4230c-143">Планирование для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4230c-143">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

 

 
## <span data-ttu-id="4230c-144">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="4230c-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4230c-145">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="4230c-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="4230c-146">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4230c-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




