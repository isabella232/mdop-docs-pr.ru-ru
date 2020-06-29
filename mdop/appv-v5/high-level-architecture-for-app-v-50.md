---
title: Высокоуровневая архитектура App-V 5.0
description: Высокоуровневая архитектура App-V 5.0
author: dansimp
ms.assetid: fdf8b841-918f-4672-b352-0f2b9519581b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0ec105ffcc3213e488615603484b2de6bafce4d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814557"
---
# <span data-ttu-id="eb7c2-103">Высокоуровневая архитектура App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="eb7c2-103">High Level Architecture for App-V 5.0</span></span>


<span data-ttu-id="eb7c2-104">Ниже приведены сведения, которые помогут вам упростить развертывание Microsoft Application Virtualization (App-V) 5,0.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-104">Use the following information to help you simplify you Microsoft Application Virtualization (App-V) 5.0 deployment.</span></span>

## <span data-ttu-id="eb7c2-105">Общие сведения об архитектуре</span><span class="sxs-lookup"><span data-stu-id="eb7c2-105">Architecture Overview</span></span>


<span data-ttu-id="eb7c2-106">Стандартная реализация App-V 5,0 состоит из указанных ниже элементов.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-106">A typical App-V 5.0 implementation consists of the following elements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="eb7c2-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="eb7c2-107">Element</span></span></th>
<th align="left"><span data-ttu-id="eb7c2-108">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="eb7c2-108">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb7c2-109">Сервер управления App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="eb7c2-109">App-V 5.0 Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb7c2-110">Сервер управления App-V 5,0 обеспечивает общую функциональность управления для инфраструктуры App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-110">The App-V 5.0 Management server provides overall management functionality for the App-V 5.0 infrastructure.</span></span> <span data-ttu-id="eb7c2-111">Кроме того, вы можете установить более одного экземпляра сервера управления в среде, который предоставляет следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="eb7c2-111">Additionally, you can install more than one instance of the management server in your environment which provides the following benefits:</span></span></p>
<ul>
<li><p><span data-ttu-id="eb7c2-112">Отказоустойчивость и высокая доступность — Установка и настройка сервера управления App-V 5,0 на двух отдельных компьютерах может помочь в ситуации, когда один из серверов недоступен или не в сети.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-112">Fault Tolerance and High Availability – Installing and configuring the App-V 5.0 Management server on two separate computers can help in situations when one of the servers is unavailable or offline.</span></span></p>
<p><span data-ttu-id="eb7c2-113">Кроме того, вы можете повысить доступность App-V 5,0, установив сервер управления на нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-113">You can also help increase App-V 5.0 availability by installing the Management server on multiple computers.</span></span> <span data-ttu-id="eb7c2-114">В этом сценарии служба балансировки нагрузки сети также должна учитываться для сбалансированных запросов сервера.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-114">In this scenario, a network load balancer should also be considered so that server requests are balanced.</span></span></p></li>
<li><p><span data-ttu-id="eb7c2-115">Масштабируемость — вы можете добавлять дополнительные серверы управления, чтобы обеспечить поддержку высокой нагрузки, например, можно установить несколько серверов за подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-115">Scalability – You can add additional management servers as necessary to support a high load, for example you can install multiple servers behind a load balancer.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="eb7c2-116">Сервер публикаций App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="eb7c2-116">App-V 5.0 Publishing Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb7c2-117">Сервер публикаций App-V 5,0 предоставляет функциональные возможности для размещения виртуальных приложений и потоковой передачи данных.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-117">The App-V 5.0 publishing server provides functionality for virtual application hosting and streaming.</span></span> <span data-ttu-id="eb7c2-118">Для сервера публикаций не требуется подключение к базе данных и поддерживаются следующие протоколы:</span><span class="sxs-lookup"><span data-stu-id="eb7c2-118">The publishing server does not require a database connection and supports the following protocols:</span></span></p>
<ul>
<li><p><span data-ttu-id="eb7c2-119">HTTP и HTTPS</span><span class="sxs-lookup"><span data-stu-id="eb7c2-119">HTTP, and HTTPS</span></span></p></li>
</ul>
<p><span data-ttu-id="eb7c2-120">Кроме того, вы можете повысить доступность App-V 5,0, установив сервер публикаций на нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-120">You can also help increase App-V 5.0 availability by installing the Publishing server on multiple computers.</span></span> <span data-ttu-id="eb7c2-121">Служба балансировки нагрузки сети также должна учитываться для сбалансированных запросов сервера.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-121">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb7c2-122">Сервер отчетов App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="eb7c2-122">App-V 5.0 Reporting Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb7c2-123">Сервер отчетов App-V 5,0 позволяет полномочным пользователям запускать и просматривать существующие отчеты App-V 5,0 и специальные отчеты, которые помогут им управлять инфраструктурой App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-123">The App-V 5.0 Reporting server enables authorized users to run and view existing App-V 5.0 reports and ad hoc reports that can help them manage the App-V 5.0 infrastructure.</span></span> <span data-ttu-id="eb7c2-124">Для сервера отчетов требуется подключение к базе данных отчетов App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-124">The Reporting server requires a connection to the App-V 5.0 reporting database.</span></span> <span data-ttu-id="eb7c2-125">Кроме того, вы можете повысить доступность App-V 5,0, установив сервер отчетов на нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-125">You can also help increase App-V 5.0 availability by installing the Reporting server on multiple computers.</span></span> <span data-ttu-id="eb7c2-126">Служба балансировки нагрузки сети также должна учитываться для сбалансированных запросов сервера.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-126">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="eb7c2-127">Клиент App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="eb7c2-127">App-V 5.0 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb7c2-128">Клиент App-V 5,0 позволяет запускать пакеты, созданные с помощью App-V 5,0, на конечных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-128">The App-V 5.0 client enables packages created using App-V 5.0 to run on target computers.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="eb7c2-129">**Примечание**  Если вы используете App-V 5,0 с электронным распространением программного обеспечения (ESD), вы не обязаны использовать сервер управления App-V 5,0, но вы по-прежнему можете использовать функцию создания отчетов и потоковой передачи данных для App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="eb7c2-129">**Note** If you are using App-V 5.0 with Electronic Software Distribution (ESD) you are not required to use the App-V 5.0 Management server, however you can still utilize the reporting and streaming functionality of App-V 5.0.</span></span>

 






## <span data-ttu-id="eb7c2-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="eb7c2-130">Related topics</span></span>


[<span data-ttu-id="eb7c2-131">Начало работы с App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="eb7c2-131">Getting Started with App-V 5.0</span></span>](getting-started-with-app-v-50--rtm.md)

 

 





