---
title: Настройка включения групп соединений только для администраторов
description: Настройка включения групп соединений только для администраторов
author: dansimp
ms.assetid: 42ca3157-5d85-467b-a148-09404f8f737a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 083d6386f02996d35255f90958705798f2cd5fb9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814453"
---
# <span data-ttu-id="aaa66-103">Настройка включения групп соединений только для администраторов</span><span class="sxs-lookup"><span data-stu-id="aaa66-103">How to Allow Only Administrators to Enable Connection Groups</span></span>


<span data-ttu-id="aaa66-104">Вы можете настроить клиент App-V таким образом, чтобы только администраторы (не конечные пользователи) могли включать или отключать группы подключения.</span><span class="sxs-lookup"><span data-stu-id="aaa66-104">You can configure the App-V client so that only administrators (not end users) can enable or disable connection groups.</span></span> <span data-ttu-id="aaa66-105">В более ранних версиях приложения App-V вы не смогли предотвратить выполнение этих задач конечными пользователями.</span><span class="sxs-lookup"><span data-stu-id="aaa66-105">In earlier versions of App-V, you could not prevent end users from performing these tasks.</span></span>

<span data-ttu-id="aaa66-106">**Примечание** 
 **Эта функция поддерживается начиная с версии App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="aaa66-106">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="aaa66-107">Используйте один из следующих методов, чтобы разрешить или запретить только администраторам включать или отключать группы подключения.</span><span class="sxs-lookup"><span data-stu-id="aaa66-107">Use one of the following methods to allow only administrators to enable or disable connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aaa66-108">Метод</span><span class="sxs-lookup"><span data-stu-id="aaa66-108">Method</span></span></th>
<th align="left"><span data-ttu-id="aaa66-109">Действия</span><span class="sxs-lookup"><span data-stu-id="aaa66-109">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aaa66-110">Параметр групповой политики</span><span class="sxs-lookup"><span data-stu-id="aaa66-110">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="aaa66-111">Включите параметр групповой политики "требуется публикация от имени администратора", который находится в следующем узле объекта групповой политики:</span><span class="sxs-lookup"><span data-stu-id="aaa66-111">Enable the “Require publish as administrator” Group Policy setting, which is located in the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="aaa66-112">Политики конфигурации &gt; компьютера &gt; Административные шаблоны &gt; , &gt; Публикация System App-V &gt;</span><span class="sxs-lookup"><span data-stu-id="aaa66-112">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aaa66-113">Командлет PowerShell</span><span class="sxs-lookup"><span data-stu-id="aaa66-113">PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="aaa66-114">Запустите <strong> командлет Set-AppvClientConfiguration </strong> с <strong> параметром – RequirePublishAsAdmin </strong> .</span><span class="sxs-lookup"><span data-stu-id="aaa66-114">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>–RequirePublishAsAdmin</strong> parameter.</span></span></p>
<p><span data-ttu-id="aaa66-115">Значения параметров:</span><span class="sxs-lookup"><span data-stu-id="aaa66-115">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="aaa66-116">0 – ложь</span><span class="sxs-lookup"><span data-stu-id="aaa66-116">0 - False</span></span></p></li>
<li><p><span data-ttu-id="aaa66-117">1 — истина</span><span class="sxs-lookup"><span data-stu-id="aaa66-117">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="aaa66-118">Пример: </strong> Set-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="aaa66-118">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="aaa66-119">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="aaa66-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="aaa66-120">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="aaa66-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="aaa66-121">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="aaa66-121">Got an App-V issue?</span></span>** <span data-ttu-id="aaa66-122">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="aaa66-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="aaa66-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="aaa66-123">Related topics</span></span>


[<span data-ttu-id="aaa66-124">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="aaa66-124">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





