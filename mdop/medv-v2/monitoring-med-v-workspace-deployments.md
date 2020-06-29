---
title: Мониторинг развертывания рабочей области MED-V
description: Мониторинг развертывания рабочей области MED-V
author: dansimp
ms.assetid: 5de0cb06-b8a9-48a5-b8b3-836954295765
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ec4c7c85326e7945aa3d61b7f96872afe24fe37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827212"
---
# <span data-ttu-id="a8564-103">Мониторинг развертывания рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="a8564-103">Monitoring MED-V Workspace Deployments</span></span>


<span data-ttu-id="a8564-104">Функция мониторинга в Microsoft Enterprise Virtualization (MED-V) 2,0 позволяет выполнять запросы для отдельных рабочих областей MED-V, чтобы определить, будет ли первоначально выполнена настройка после развертывания рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="a8564-104">The monitoring feature in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 lets you run queries on individual MED-V workspaces to determine whether first time setup succeeded throughout your enterprise after the MED-V workspaces are deployed.</span></span> <span data-ttu-id="a8564-105">Наблюдение за успехом первого этапа настройки имеет большое значение, так как MED-V не находится в пригодном для использования состоянии до тех пор, пока не будет выполнена установка первого раза.</span><span class="sxs-lookup"><span data-stu-id="a8564-105">Monitoring the success of first time setup is important because MED-V is not in a usable state until first time setup has been completed successfully.</span></span>

<span data-ttu-id="a8564-106">В этом разделе содержатся сведения и инструкции, которые помогут вам отслеживать успешность или сбой при первом запуске программы.</span><span class="sxs-lookup"><span data-stu-id="a8564-106">This section provides information and instruction to assist you in monitoring the success or failure of first time setup.</span></span>

## <span data-ttu-id="a8564-107">Наблюдение за развертыванием рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="a8564-107">To monitor MED-V workspace deployments</span></span>


<span data-ttu-id="a8564-108">Функция мониторинга состоит из отдельного внутрипроцессного поставщика инструментария управления Windows (WMI), который можно запросить с помощью языка запросов WMI, чтобы выяснить состояние первой настройки для всех конечных пользователей в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="a8564-108">The monitoring feature consists of a coupled in-process Windows Management Instrumentation (WMI) provider that you can query using WMI Query Language to discover the status of first time setup for all end users on a MED-V workspace.</span></span>

<span data-ttu-id="a8564-109">Поставщик WMI реализуется с помощью инфраструктуры расширения поставщика WMI из Microsoft .NET Framework 3,5.</span><span class="sxs-lookup"><span data-stu-id="a8564-109">The WMI provider is implemented by using the WMI Provider Extension framework from the Microsoft .Net Framework 3.5.</span></span> <span data-ttu-id="a8564-110">Поставщик WMI выполняется в контексте локальной службы и сохраняет состояние установки в первый раз в \\ProgramData.</span><span class="sxs-lookup"><span data-stu-id="a8564-110">The WMI provider executes in the context of LocalService and stores the first time setup state securely under \\ProgramData.</span></span>

<span data-ttu-id="a8564-111">Поставщик WMI реализован в пространстве имен **root\\microsoft\\medv** и реализует класс **FTS \ _Status**, который предоставляет метод **SetFtsState**.</span><span class="sxs-lookup"><span data-stu-id="a8564-111">The WMI provider is implemented in the **root\\microsoft\\medv** namespace and implements the class **FTS\_Status**, which exposes the method **SetFtsState**.</span></span> <span data-ttu-id="a8564-112">MED-V использует **SetFtsState** для установки первого состояния установки.</span><span class="sxs-lookup"><span data-stu-id="a8564-112">MED-V uses **SetFtsState** to set the first time setup state.</span></span>

<span data-ttu-id="a8564-113">Класс включает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a8564-113">The class contains the following properties.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a8564-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="a8564-114">Property</span></span></th>
<th align="left"><span data-ttu-id="a8564-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a8564-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a8564-116">Компьютер</span><span class="sxs-lookup"><span data-stu-id="a8564-116">Machine</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a8564-117">Свойство только </strong> для чтения, содержащее имя гостевой виртуальной машины, подготовленное при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="a8564-117">Read Only</strong> property that contains the name of the guest virtual machine provisioned by first time setup.</span></span> <span data-ttu-id="a8564-118">Этот ключ содержит имя, которое гость имел при первой ошибке установки.</span><span class="sxs-lookup"><span data-stu-id="a8564-118">This key contains the name that the guest would have had on first time setup failure.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a8564-119">StatusCode</span><span class="sxs-lookup"><span data-stu-id="a8564-119">StatusCode</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a8564-120">Свойство только </strong> для чтения, которое имеет значение 0, если при первом запуске программы установки была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a8564-120">Read Only</strong> property that contains zero if first time setup succeeded.</span></span> <span data-ttu-id="a8564-121">Любые другие возвращенные значения равны ИДЕНТИФИКАТОРу события, в котором регистрируется ошибка.</span><span class="sxs-lookup"><span data-stu-id="a8564-121">Any other value returned equals the event ID for the error that is logged.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a8564-122">Время</span><span class="sxs-lookup"><span data-stu-id="a8564-122">Time</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a8564-123">Время в формате UTC, когда программа установки завершила свое первое время.</span><span class="sxs-lookup"><span data-stu-id="a8564-123">The UTC time that first time setup completed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a8564-124">Пользователь</span><span class="sxs-lookup"><span data-stu-id="a8564-124">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a8564-125">Пользователь, для которого при первом запуске программы установки произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="a8564-125">The user for which first time setup was run.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a8564-126">В следующем коде показан MOF-файл, который определяет класс **FTS \ _Status** .</span><span class="sxs-lookup"><span data-stu-id="a8564-126">The following code shows the Managed Object Format (MOF) file that defines the **FTS\_Status** class.</span></span>

``` syntax
[dynamic: ToInstance, provider("MedvWmi, Version=2.0.258.0, Culture=neutral, PublicKeyToken=14986c3f172d1c2c")]
class FTS_Status
{
[read, key] string User;
[read] string Machine;
[read] sint32 StatusCode;
[read] datetime Time;
[static, implemented] void SetFtsState([in] sint32 statusCode, [in] string machine);
};
```

<span data-ttu-id="a8564-127">Поскольку основная проблема чаще всего связана с рабочими областями для MED-V, для которых не удалось выполнить начальную настройку, вы можете написать запрос, возвращающий только те из них, которые не выполнялись при первом запуске программы, например:</span><span class="sxs-lookup"><span data-stu-id="a8564-127">Because your main concern is most likely those MED-V workspaces for which first time setup was not completed successfully, you can write your query to only return those that failed first time setup, for example:</span></span>

``` syntax
Select * from FTS_Status where StatusCode != 0
```

<span data-ttu-id="a8564-128">В этом случае функция мониторинга возвращает список таких рабочих областей MED-V, для которых не удалось выполнить начальную настройку, с помощью которых можно выполнить необходимые действия для устранения проблемы.</span><span class="sxs-lookup"><span data-stu-id="a8564-128">In this case, the monitoring feature returns a list of those MED-V workspaces that failed first time setup, which you can use to take the appropriate actions to resolve the failure.</span></span>

## <span data-ttu-id="a8564-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a8564-129">Related topics</span></span>


[<span data-ttu-id="a8564-130">Мониторинг рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="a8564-130">Monitor MED-V Workspaces</span></span>](monitor-med-v-workspaces.md)

[<span data-ttu-id="a8564-131">Проверка параметров первой установки</span><span class="sxs-lookup"><span data-stu-id="a8564-131">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

 

 





