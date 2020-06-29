---
title: Контрольный список для оценки бизнес-приложений для UE-V 1.0
description: Контрольный список для оценки бизнес-приложений для UE-V 1.0
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826459"
---
# <span data-ttu-id="11733-103">Контрольный список для оценки бизнес-приложений для UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="11733-103">Checklist for Evaluating Line-of-Business Applications for UE-V 1.0</span></span>


<span data-ttu-id="11733-104">Для оценки того, какие бизнес-приложения должны быть включены в развертывание UE-V, учитывайте следующее:</span><span class="sxs-lookup"><span data-stu-id="11733-104">To evaluate which line-of-business applications should be included in your UE-V deployment, consider the following:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="11733-105">Описание</span><span class="sxs-lookup"><span data-stu-id="11733-105">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="11733-106">Содержит ли приложение параметры, доступные пользователю для настройки?</span><span class="sxs-lookup"><span data-stu-id="11733-106">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="11733-107">Важно ли пользователю, что эти параметры перемещаются?</span><span class="sxs-lookup"><span data-stu-id="11733-107">Is it important for the user that these settings roam?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="11733-108">Параметры пользователя уже управляются решением политики управления приложениями или параметрами.</span><span class="sxs-lookup"><span data-stu-id="11733-108">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="11733-109">UE-V применяет параметры приложения при запуске приложения и параметры Windows для событий входа, разблокировки и удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="11733-109">UE-V applies application settings at application launch and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="11733-110">Если вы используете UE-V с другими решениями политики настройки, пользователи могут столкнуться с несогласованностью во всех перемещаемых параметрах.</span><span class="sxs-lookup"><span data-stu-id="11733-110">If you use UE-V with other settings policy solutions, users might experience inconsistency across roamed settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="11733-111">Специфичны ли параметры приложения для компьютера?</span><span class="sxs-lookup"><span data-stu-id="11733-111">Are the application settings specific to the computer?</span></span> <span data-ttu-id="11733-112">Настройки приложения и настройки, связанные с оборудованием или конкретными конфигурациями компьютера, не всегда перемещаются по сеансам и могут привести к плохому взаимодействию с приложением.</span><span class="sxs-lookup"><span data-stu-id="11733-112">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently roam across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="11733-113">Параметры магазина приложений находятся в каталоге Program Files или в каталоге файлов, расположенном в <strong> каталоге Users </strong> \ [имя пользователя] \ <strong> AppData </strong>  \  <strong> LocalLow </strong> ?</span><span class="sxs-lookup"><span data-stu-id="11733-113">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong> \ [User name] \ <strong>AppData</strong> \ <strong>LocalLow</strong> directory?</span></span> <span data-ttu-id="11733-114">Данные приложения, которые хранятся в одном из этих расположений, обычно не должны перемещаться вместе с пользователем, так как эти данные являются специфическими для компьютера, или данные слишком велики для перемещения.</span><span class="sxs-lookup"><span data-stu-id="11733-114">Application data that is stored in either of these locations usually should not roam with the user, because this data is specific to the computer or because the data is too large to roam.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="11733-115">Сохраняет ли приложение все параметры в файле, которые содержат другие данные приложения, которые не должны перемещаться?</span><span class="sxs-lookup"><span data-stu-id="11733-115">Does the application store any settings in a file that contains other application data that should not roam?</span></span> <span data-ttu-id="11733-116">UE-V синхронизирует файлы как единый блок.</span><span class="sxs-lookup"><span data-stu-id="11733-116">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="11733-117">Если параметры хранятся в файлах, которые содержат данные приложения, отличные от параметров, то синхронизация этих дополнительных данных может привести к плохому взаимодействию с приложением.</span><span class="sxs-lookup"><span data-stu-id="11733-117">If settings are stored in files that include application data other than settings, then synchronizing this additional data may cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="11733-118">Насколько велики файлы, содержащие параметры?</span><span class="sxs-lookup"><span data-stu-id="11733-118">How large are the files that contain the settings?</span></span> <span data-ttu-id="11733-119">Производительность синхронизации параметров может зависеть от больших файлов.</span><span class="sxs-lookup"><span data-stu-id="11733-119">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="11733-120">Включение больших файлов может повлиять на производительность синхронизации параметров.</span><span class="sxs-lookup"><span data-stu-id="11733-120">Including large files can impact the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="11733-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="11733-121">Related topics</span></span>


[<span data-ttu-id="11733-122">Планирование методов конфигурации UE-V</span><span class="sxs-lookup"><span data-stu-id="11733-122">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

[<span data-ttu-id="11733-123">Планирование UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="11733-123">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

 

 





