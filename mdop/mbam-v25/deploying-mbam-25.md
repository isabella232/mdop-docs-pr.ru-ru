---
title: Развертывание MBAM 2.5
description: Развертывание MBAM 2.5
author: dansimp
ms.assetid: 45403607-1f4d-42fe-8413-0d4da01808a6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0cfa0a190530186211cd96884b2e32e9c65881f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826282"
---
# <span data-ttu-id="11c2b-103">Развертывание MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="11c2b-103">Deploying MBAM 2.5</span></span>


<span data-ttu-id="11c2b-104">С помощью этих сведений можно определить, какие действия вы можете выполнить для развертывания и настройки служб администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5, чтобы перейти на MBAM 2,5 от предыдущих версий или удалить MBAM серверные функции.</span><span class="sxs-lookup"><span data-stu-id="11c2b-104">Use this information to identify the procedures you can follow to deploy and configure Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server features to upgrade to MBAM 2.5 from previous versions, or to remove MBAM Server features.</span></span>

## <span data-ttu-id="11c2b-105">Сведения о развертывании</span><span class="sxs-lookup"><span data-stu-id="11c2b-105">Deployment information</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11c2b-106">Описание темы</span><span class="sxs-lookup"><span data-stu-id="11c2b-106">Topic description</span></span></th>
<th align="left"><span data-ttu-id="11c2b-107">Ссылки на разделы</span><span class="sxs-lookup"><span data-stu-id="11c2b-107">Links to topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="11c2b-108">Параметры топологии развертывания.</span><span class="sxs-lookup"><span data-stu-id="11c2b-108">Deployment topology options.</span></span></p></li>
<li><p><span data-ttu-id="11c2b-109">Установка программного обеспечения сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="11c2b-109">How to install the MBAM Server software.</span></span></p></li>
<li><p><span data-ttu-id="11c2b-110">Настройка функций сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="11c2b-110">How to configure the MBAM Server features.</span></span></p></li>
</ul></td>
<td align="left"><p><a href="deploying-the-mbam-25-server-infrastructure.md" data-raw-source="[Deploying the MBAM 2.5 Server Infrastructure](deploying-the-mbam-25-server-infrastructure.md)"><span data-ttu-id="11c2b-111">Развертывание инфраструктуры сервера MBAM 2.5 Server</span><span class="sxs-lookup"><span data-stu-id="11c2b-111">Deploying the MBAM 2.5 Server Infrastructure</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11c2b-112">Сведения о том, как загружать и развертывать шаблоны групповой политики MBAM, необходимые для управления клиентами MBAM и политиками шифрования BitLocker в корпоративной среде.</span><span class="sxs-lookup"><span data-stu-id="11c2b-112">How to download and deploy the MBAM Group Policy Templates, which are required to manage MBAM Clients and BitLocker encryption policies in the enterprise.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-25-group-policy-objects.md" data-raw-source="[Deploying MBAM 2.5 Group Policy Objects](deploying-mbam-25-group-policy-objects.md)"><span data-ttu-id="11c2b-113">Развертывание объектов групповой политики MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="11c2b-113">Deploying MBAM 2.5 Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11c2b-114">Инструкции по использованию файлов установщика Windows в клиенте MBAM для развертывания клиентского программного обеспечения MBAM.</span><span class="sxs-lookup"><span data-stu-id="11c2b-114">How to use the MBAM Client Windows Installer files to deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)"><span data-ttu-id="11c2b-115">Развертывание клиента MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="11c2b-115">Deploying the MBAM 2.5 Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11c2b-116">Контрольный список, который поможет вам при развертывании функций сервера MBAM и клиента MBAM.</span><span class="sxs-lookup"><span data-stu-id="11c2b-116">Checklist that can assist you in deploying the MBAM Server features and MBAM Client.</span></span></p></td>
<td align="left"><p><a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"><span data-ttu-id="11c2b-117">Контрольный список необходимых компонентов развертывания MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="11c2b-117">MBAM 2.5 Deployment Checklist</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11c2b-118">Обновление MBAM из предыдущих версий.</span><span class="sxs-lookup"><span data-stu-id="11c2b-118">How to upgrade MBAM from previous versions.</span></span></p></td>
<td align="left"><p><a href="upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md" data-raw-source="[Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)"><span data-ttu-id="11c2b-119">Обновление с предыдущих версий до MBAM 2.5 или MBAM 2.5 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="11c2b-119">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11c2b-120">Удаление функций и программного обеспечения сервера MBAM.</span><span class="sxs-lookup"><span data-stu-id="11c2b-120">How to remove MBAM Server features or software.</span></span></p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)"><span data-ttu-id="11c2b-121">Удаление компонентов или программного обеспечения MBAM Server</span><span class="sxs-lookup"><span data-stu-id="11c2b-121">Removing MBAM Server Features or Software</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="11c2b-122">Другие ресурсы для развертывания MBAM</span><span class="sxs-lookup"><span data-stu-id="11c2b-122">Other resources for deploying MBAM</span></span>


[<span data-ttu-id="11c2b-123">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="11c2b-123">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="11c2b-124">Начало работы с MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="11c2b-124">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="11c2b-125">Планирование для MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="11c2b-125">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

[<span data-ttu-id="11c2b-126">Операции MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="11c2b-126">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)

[<span data-ttu-id="11c2b-127">Устранение неполадок MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="11c2b-127">Troubleshooting MBAM 2.5</span></span>](troubleshooting-mbam-25.md)

[<span data-ttu-id="11c2b-128">Технический справочник по MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="11c2b-128">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="11c2b-129">Развертывание MBAM 2.5 в изолированной конфигурации</span><span class="sxs-lookup"><span data-stu-id="11c2b-129">Deploying MBAM 2.5 in a stand-alone configuration</span></span>](https://support.microsoft.com/kb/3046555)

## <span data-ttu-id="11c2b-130">У вас есть предложение MBAM?</span><span class="sxs-lookup"><span data-stu-id="11c2b-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="11c2b-131">Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="11c2b-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="11c2b-132">Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="11c2b-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





