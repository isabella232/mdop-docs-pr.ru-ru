---
title: Контрольный список необходимых компонентов развертывания MBAM 2.0
description: Контрольный список необходимых компонентов развертывания MBAM 2.0
author: dansimp
ms.assetid: 7905d31d-f21c-4683-b9c4-95b815e08fab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d8d0ce1a3ff48d4bf2f84e61b4a578b170264a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826439"
---
# <span data-ttu-id="0eb01-103">Контрольный список необходимых компонентов развертывания MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0eb01-103">MBAM 2.0 Deployment Checklist</span></span>


<span data-ttu-id="0eb01-104">Этот контрольный список поможет вам при развертывании Microsoft BitLocker и наблюдении (MBAM) с изолированной топологией.</span><span class="sxs-lookup"><span data-stu-id="0eb01-104">This checklist can be used to help you during Microsoft BitLocker Administration and Monitoring (MBAM) deployment with a Stand-alone topology.</span></span>

**<span data-ttu-id="0eb01-105">Примечание.</span><span class="sxs-lookup"><span data-stu-id="0eb01-105">Note</span></span>**  
<span data-ttu-id="0eb01-106">В этом контрольном списке описаны рекомендованные шаги и высокоуровневый список элементов, которые следует принимать во время развертывания функций администрирования и мониторинга Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0eb01-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="0eb01-107">Рекомендуется скопировать этот контрольный список в программу для работы с электронными таблицами и настроить ее для использования.</span><span class="sxs-lookup"><span data-stu-id="0eb01-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



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
<th align="left"><span data-ttu-id="0eb01-108">Задача</span><span class="sxs-lookup"><span data-stu-id="0eb01-108">Task</span></span></th>
<th align="left"><span data-ttu-id="0eb01-109">Ссылки</span><span class="sxs-lookup"><span data-stu-id="0eb01-109">References</span></span></th>
<th align="left"><span data-ttu-id="0eb01-110">Заметки</span><span class="sxs-lookup"><span data-stu-id="0eb01-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0eb01-111">Заполните этап планирования для подготовки вычислительной среды для MBAM развертывания.</span><span class="sxs-lookup"><span data-stu-id="0eb01-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-planning-checklist-mbam-2.md" data-raw-source="[MBAM 2.0 Planning Checklist](mbam-20-planning-checklist-mbam-2.md)"><span data-ttu-id="0eb01-112">Контрольный список планирования MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0eb01-112">MBAM 2.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0eb01-113">Ознакомьтесь со сведениями о конфигурации, поддерживаемыми MBAM, чтобы убедиться, что выбранные клиентские и серверные компьютеры поддерживаются для установки компонента MBAM.</span><span class="sxs-lookup"><span data-stu-id="0eb01-113">Review the MBAM supported configurations information to make sure selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="0eb01-114">Поддерживаемые конфигурации MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0eb01-114">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0eb01-115">Запустите программу установки MBAM, чтобы развернуть компоненты сервера MBAM в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="0eb01-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="0eb01-116">База данных восстановления</span><span class="sxs-lookup"><span data-stu-id="0eb01-116">Recovery Database</span></span></p></li>
<li><p><span data-ttu-id="0eb01-117">База данных соответствия требованиям и аудита</span><span class="sxs-lookup"><span data-stu-id="0eb01-117">Compliance and Audit Database</span></span></p></li>
<li><p><span data-ttu-id="0eb01-118">Аудит соответствия требованиям и отчеты</span><span class="sxs-lookup"><span data-stu-id="0eb01-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="0eb01-119">Сервер самообслуживания</span><span class="sxs-lookup"><span data-stu-id="0eb01-119">Self-Service Server</span></span></p></li>
<li><p><span data-ttu-id="0eb01-120">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="0eb01-120">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="0eb01-121">Шаблон групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="0eb01-121">MBAM Group Policy template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="0eb01-122">Примечание.</span><span class="sxs-lookup"><span data-stu-id="0eb01-122">Note</span></span></strong><br/><p><span data-ttu-id="0eb01-123">Следите за именами серверов, на которых установлены все компоненты.</span><span class="sxs-lookup"><span data-stu-id="0eb01-123">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="0eb01-124">Эти сведения будут использоваться во время установки.</span><span class="sxs-lookup"><span data-stu-id="0eb01-124">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-20-server-infrastructure-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md)"><span data-ttu-id="0eb01-125">Развертывание инфраструктуры сервера MBAM 2.0 Server</span><span class="sxs-lookup"><span data-stu-id="0eb01-125">Deploying the MBAM 2.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0eb01-126">Добавьте группы безопасности доменных служб Active Directory, созданные на этапе планирования, в соответствующие локальные группы администраторов компонентов сервера MBAM на соответствующих серверах.</span><span class="sxs-lookup"><span data-stu-id="0eb01-126">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="0eb01-127">Планирование ролей администраторов MBAM 2,0 </a> и <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Управление РОЛЯМИ администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="0eb01-127">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0eb01-128">Создание и развертывание необходимых объектов групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="0eb01-128">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="0eb01-129">Развертывание объектов групповой политики MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0eb01-129">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0eb01-130">Развертывание программного обеспечения клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="0eb01-130">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="0eb01-131">Развертывание клиента MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0eb01-131">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="0eb01-132">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0eb01-132">Related topics</span></span>


[<span data-ttu-id="0eb01-133">Развертывание MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0eb01-133">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)









