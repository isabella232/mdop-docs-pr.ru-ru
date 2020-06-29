---
title: Контрольный список необходимых компонентов развертывания MBAM 1.0
description: Контрольный список необходимых компонентов развертывания MBAM 1.0
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812536"
---
# <span data-ttu-id="83661-103">Контрольный список необходимых компонентов развертывания MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="83661-103">MBAM 1.0 Deployment Checklist</span></span>


<span data-ttu-id="83661-104">Этот контрольный список разработан для упрощения развертывания администрирования и мониторинга Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="83661-104">This checklist is designed to facilitate your deployment of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

**<span data-ttu-id="83661-105">Примечание.</span><span class="sxs-lookup"><span data-stu-id="83661-105">Note</span></span>**  
<span data-ttu-id="83661-106">В этом контрольном списке описаны рекомендованные шаги и представлен высокоуровневый список элементов, которые следует принимать во время развертывания функций MBAM.</span><span class="sxs-lookup"><span data-stu-id="83661-106">This checklist outlines the recommended steps and provides a high-level list of items to consider when you deploy the MBAM features.</span></span> <span data-ttu-id="83661-107">Мы рекомендуем вам скопировать этот контрольный список в программу для работы с электронными таблицами и настроить ее для удовлетворения конкретных потребностей.</span><span class="sxs-lookup"><span data-stu-id="83661-107">We recommend that you copy this checklist into a spreadsheet program and customize it for your specific needs.</span></span>



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
<th align="left"><span data-ttu-id="83661-108">Задача</span><span class="sxs-lookup"><span data-stu-id="83661-108">Task</span></span></th>
<th align="left"><span data-ttu-id="83661-109">Ссылки</span><span class="sxs-lookup"><span data-stu-id="83661-109">References</span></span></th>
<th align="left"><span data-ttu-id="83661-110">Заметки</span><span class="sxs-lookup"><span data-stu-id="83661-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="83661-111">Заполните этап планирования для подготовки вычислительной среды для MBAM развертывания.</span><span class="sxs-lookup"><span data-stu-id="83661-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)"><span data-ttu-id="83661-112">Контрольный список планирования MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="83661-112">MBAM 1.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="83661-113">Ознакомьтесь со сведениями о поддерживаемых конфигурациях MBAM, чтобы убедиться, что выбранные клиентские и серверные компьютеры поддерживаются для установки компонента MBAM.</span><span class="sxs-lookup"><span data-stu-id="83661-113">Review the information on MBAM supported configurations to make sure that your selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="83661-114">Поддерживаемые конфигурации MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="83661-114">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="83661-115">Запустите программу установки MBAM, чтобы развернуть компоненты сервера MBAM в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="83661-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="83661-116">База данных восстановления и оборудования</span><span class="sxs-lookup"><span data-stu-id="83661-116">Recovery and Hardware Database</span></span></p></li>
<li><p><span data-ttu-id="83661-117">База данных состояния соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="83661-117">Compliance Status Database</span></span></p></li>
<li><p><span data-ttu-id="83661-118">Аудит соответствия требованиям и отчеты</span><span class="sxs-lookup"><span data-stu-id="83661-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="83661-119">Сервер администрирования и мониторинга</span><span class="sxs-lookup"><span data-stu-id="83661-119">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="83661-120">Шаблон групповой политики MBAM</span><span class="sxs-lookup"><span data-stu-id="83661-120">MBAM Group Policy Template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="83661-121">Примечание.</span><span class="sxs-lookup"><span data-stu-id="83661-121">Note</span></span></strong><br/><p><span data-ttu-id="83661-122">Следите за именами серверов, на которых установлены все компоненты.</span><span class="sxs-lookup"><span data-stu-id="83661-122">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="83661-123">Эти данные будут использоваться во время установки.</span><span class="sxs-lookup"><span data-stu-id="83661-123">You will use this information throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)"><span data-ttu-id="83661-124">Развертывание инфраструктуры сервера MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="83661-124">Deploying the MBAM 1.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="83661-125">Добавьте группы безопасности доменных служб Active Directory, созданные на этапе планирования, в соответствующие локальные группы администраторов компонентов сервера MBAM на соответствующих серверах.</span><span class="sxs-lookup"><span data-stu-id="83661-125">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on the appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="83661-126">Планирование ролей администраторов MBAM 1,0 </a> и <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Управление РОЛЯМИ администратора MBAM</span><span class="sxs-lookup"><span data-stu-id="83661-126">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="83661-127">Создание и развертывание необходимых объектов групповой политики MBAM.</span><span class="sxs-lookup"><span data-stu-id="83661-127">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="83661-128">Развертывание объектов групповой политики MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="83661-128">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="83661-129">Развертывание программного обеспечения клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="83661-129">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="83661-130">Развертывание клиента MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="83661-130">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="83661-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="83661-131">Related topics</span></span>


[<span data-ttu-id="83661-132">Развертывание MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="83661-132">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)









