---
title: Контрольный список подготовки к установке App-V
description: Контрольный список подготовки к установке App-V
author: dansimp
ms.assetid: 3af609b1-2c09-4edb-b083-b913b6d5e8c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 70e71d3dea02daeadedb4cff78c58302ac743dda
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819789"
---
# <span data-ttu-id="1b358-103">Контрольный список подготовки к установке App-V</span><span class="sxs-lookup"><span data-stu-id="1b358-103">App-V Pre-Installation Checklist</span></span>


<span data-ttu-id="1b358-104">Приведенный ниже контрольный список предназначен для того, чтобы создать высокоуровневый список элементов, которые необходимо принять, и ознакомиться с действиями, которые необходимо выполнить перед установкой серверов Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="1b358-104">The following checklist is intended to provide a high-level list of items to consider and outlines the steps you should take before you install the Microsoft Application Virtualization (App-V) servers.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1b358-105">Шаг</span><span class="sxs-lookup"><span data-stu-id="1b358-105">Step</span></span></th>
<th align="left"><span data-ttu-id="1b358-106">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="1b358-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1b358-107">Убедитесь в том, что ваша вычислительная среда соответствует поддерживаемым настройкам для App-V.</span><span class="sxs-lookup"><span data-stu-id="1b358-107">Ensure your computing environment meets the supported configurations required for App-V.</span></span></p></td>
<td align="left"><p><a href="application-virtualization-deployment-requirements.md" data-raw-source="[Application Virtualization Deployment Requirements](application-virtualization-deployment-requirements.md)"><span data-ttu-id="1b358-108">Требования при развертывании Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="1b358-108">Application Virtualization Deployment Requirements</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1b358-109">Настройте необходимые группы и учетные записи Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1b358-109">Configure the necessary Active Directory groups and accounts.</span></span></p></td>
<td align="left"><p><a href="configuring-prerequisite-groups-in-active-directory-for-app-v.md" data-raw-source="[Configuring Prerequisite Groups in Active Directory for App-V](configuring-prerequisite-groups-in-active-directory-for-app-v.md)"><span data-ttu-id="1b358-110">Настройка необходимых групп в Active Directory для App-V</span><span class="sxs-lookup"><span data-stu-id="1b358-110">Configuring Prerequisite Groups in Active Directory for App-V</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1b358-111">Настройте параметры информационных служб Интернета (IIS) на сервере, на котором запущены службы IIS.</span><span class="sxs-lookup"><span data-stu-id="1b358-111">Configure the Internet Information Services (IIS) settings on the server that is running IIS.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-windows-server-2008-for-app-v-management-servers.md" data-raw-source="[How to Configure Windows Server 2008 for App-V Management Servers](how-to-configure-windows-server-2008-for-app-v-management-servers.md)"><span data-ttu-id="1b358-112">Настройка Windows Server 2008 для серверов App-V Management Server</span><span class="sxs-lookup"><span data-stu-id="1b358-112">How to Configure Windows Server 2008 for App-V Management Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1b358-113">Настройте сервер, на котором выполняются службы IIS, как доверенный для делегирования.</span><span class="sxs-lookup"><span data-stu-id="1b358-113">Configure the server that is running IIS to be trusted for delegation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1b358-114">Примечание.</span><span class="sxs-lookup"><span data-stu-id="1b358-114">Note</span></span></strong><br/><p><span data-ttu-id="1b358-115">Это необходимо только в том случае, если установка сервера управления App-V выполняется с помощью распределенной архитектуры системы, то есть при установке консоли управления App-V, веб-службы управления и базы данных на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="1b358-115">This is required only if you are installing the App-V Management Server by using a distributed system architecture, that is, if you install the App-V Management Console, the Management Web Service, and the database on different computers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-configure-the-server-to-be-trusted-for-delegation.md" data-raw-source="[How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)"><span data-ttu-id="1b358-116">Настройка сервера для разрешения делегирования</span><span class="sxs-lookup"><span data-stu-id="1b358-116">How to Configure the Server to be Trusted for Delegation</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1b358-117">Установите Microsoft SQL Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1b358-117">Install Microsoft SQL Server 2008.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="[Install SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=181924)"><span data-ttu-id="1b358-118">Установите SQL Server 2008 </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924"> https://go.microsoft.com/fwlink/?LinkId=181924 </a> ).</span><span class="sxs-lookup"><span data-stu-id="1b358-118">Install SQL Server 2008</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924">https://go.microsoft.com/fwlink/?LinkId=181924</a>).</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="1b358-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1b358-119">Related topics</span></span>


[<span data-ttu-id="1b358-120">Контрольные списки развертывания и обновления Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="1b358-120">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

[<span data-ttu-id="1b358-121">Контрольный список установки App-V</span><span class="sxs-lookup"><span data-stu-id="1b358-121">App-V Installation Checklist</span></span>](app-v-installation-checklist.md)









