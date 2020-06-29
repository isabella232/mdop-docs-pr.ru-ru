---
title: Развертывание инфраструктуры сервера MBAM 2.5 Server
description: Развертывание инфраструктуры сервера MBAM 2.5 Server
author: dansimp
ms.assetid: e85a60cf-4cc1-4906-8da3-442232c374af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b3ec622ad60c6d5e8528b9e1c38227bc2c463634
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826272"
---
# <span data-ttu-id="d0f90-103">Развертывание инфраструктуры сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="d0f90-103">Deploying the MBAM 2.5 Server Infrastructure</span></span>


<span data-ttu-id="d0f90-104">Для развертывания инфраструктуры сервера администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5 вы можете выполнять следующие три задачи высокого уровня:</span><span class="sxs-lookup"><span data-stu-id="d0f90-104">To deploy the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server infrastructure, you complete the following three high-level tasks:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d0f90-105">Задача</span><span class="sxs-lookup"><span data-stu-id="d0f90-105">Task</span></span></th>
<th align="left"><span data-ttu-id="d0f90-106">Где найти инструкции</span><span class="sxs-lookup"><span data-stu-id="d0f90-106">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0f90-107">Установите серверное программное обеспечение MBAM 2,5 на каждый сервер, на котором вы хотите настроить компонент MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="d0f90-107">Install the MBAM 2.5 Server software on each server where you want to configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="d0f90-108">Установка программного обеспечения MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="d0f90-108">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0f90-109">Настройка баз данных, отчетов, веб-приложений и необязательной топологии интеграции System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d0f90-109">Configure the databases, reports, web applications, and the optional System Center Configuration Manager Integration topology.</span></span></p>
<p><span data-ttu-id="d0f90-110">Вы можете выполнить настройку с помощью мастера конфигурации сервера MBAM или командлетов Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d0f90-110">You can use the MBAM Server Configuration wizard or Windows PowerShell cmdlets to do the configuration.</span></span></p></td>
<td align="left"><p><a href="configuring-the-mbam-25-server-features.md" data-raw-source="[Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md)"><span data-ttu-id="d0f90-111">Настройка компонентов сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="d0f90-111">Configuring the MBAM 2.5 Server Features</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0f90-112">Проверка конфигурации сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="d0f90-112">Validate the MBAM Server configuration.</span></span></p></td>
<td align="left"><p><a href="validating-the-mbam-25-server-feature-configuration.md" data-raw-source="[Validating the MBAM 2.5 Server Feature Configuration](validating-the-mbam-25-server-feature-configuration.md)"><span data-ttu-id="d0f90-113">Проверка конфигурации компонентов MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="d0f90-113">Validating the MBAM 2.5 Server Feature Configuration</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d0f90-114">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d0f90-114">Related topics</span></span>


[<span data-ttu-id="d0f90-115">Развертывание MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d0f90-115">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

 
## <span data-ttu-id="d0f90-116">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="d0f90-116">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d0f90-117">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="d0f90-117">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="d0f90-118">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="d0f90-118">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





