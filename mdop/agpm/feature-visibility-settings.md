---
title: Параметры видимости компонентов
description: Параметры видимости компонентов
author: dansimp
ms.assetid: 9db2ba03-fb75-4f95-9138-ec89b9fc8d01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26f19895d0a9163885779688ba7d89f6d16f2a17
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820809"
---
# <span data-ttu-id="12ff6-103">Параметры видимости компонентов</span><span class="sxs-lookup"><span data-stu-id="12ff6-103">Feature Visibility Settings</span></span>


<span data-ttu-id="12ff6-104">Параметры шаблона администрирования для расширенного управления групповыми политиками позволяют централизованно настраивать видимость узла и **журнала** **изменений** для администраторов групповой политики, которым применен объект групповой политики (GPO) с этими параметрами.</span><span class="sxs-lookup"><span data-stu-id="12ff6-104">The Administrative template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure the visibility of the **Change Control** node and **History** tab for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="12ff6-105">Ниже перечислены параметры, доступные в разделе User Configuration\\Administrative Templates\\Windows Components\\Microsoft (запрещенные и разрешенные Snap-ins\\Extension оснасток) в **редакторе объектов групповой политики** при редактировании GPO в консоли управления групповыми политиками (GPMC).</span><span class="sxs-lookup"><span data-stu-id="12ff6-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\Microsoft Management Console\\Restricted/Permitted Snap-ins\\Extension Snap-ins in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="12ff6-106">Если этот путь не отображается, щелкните правой кнопкой мыши папку **Административные шаблоны**и добавьте шаблон для расширенного управления групповыми политиками (, ADMX. adm).</span><span class="sxs-lookup"><span data-stu-id="12ff6-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="12ff6-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="12ff6-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="12ff6-108">Эффект</span><span class="sxs-lookup"><span data-stu-id="12ff6-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="12ff6-109">Управление изменениями РАСШИРЕНного управления доступом</span><span class="sxs-lookup"><span data-stu-id="12ff6-109">AGPM Change Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12ff6-110">Если этот флажок установлен или не задан, <strong> узел контроль изменений </strong> отображается в консоли управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="12ff6-110">If enabled or not configured, the <strong>Change Control</strong> node is visible in the GPMC.</span></span></p>
<p><span data-ttu-id="12ff6-111">Если <strong> этот элемент отключен, </strong> узел изменения не отображается в консоли управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="12ff6-111">If disabled, the <strong>Change Control</strong> node is not visible in the GPMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="12ff6-112">Расширение ссылки по РАСШИРЕНию</span><span class="sxs-lookup"><span data-stu-id="12ff6-112">AGPM Link Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12ff6-113">Если эта политика включена или не настроена, <strong> </strong> в GPMC появляется вкладка "журнал" для каждого связанного объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="12ff6-113">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each linked GPO.</span></span></p>
<p><span data-ttu-id="12ff6-114">Если этот элемент отключен <strong> , </strong> вкладка История не отображается для связанных объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="12ff6-114">If disabled, the <strong>History</strong> tab is not visible for linked GPOs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="12ff6-115">Расширение объекта групповой политики для РАСШИРЕНного расширения</span><span class="sxs-lookup"><span data-stu-id="12ff6-115">AGPM GPO Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12ff6-116">Если эта политика включена или не настроена, <strong> </strong> в GPMC для каждого объекта групповой политики появляется вкладка "журнал".</span><span class="sxs-lookup"><span data-stu-id="12ff6-116">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each GPO.</span></span></p>
<p><span data-ttu-id="12ff6-117">Если этот элемент отключен, вкладка История недоступна <strong> </strong> для объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="12ff6-117">If disabled, the <strong>History</strong> tab is not visible for GPOs.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="12ff6-118">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="12ff6-118">Additional references</span></span>

-   [<span data-ttu-id="12ff6-119">Параметры административных шаблонов</span><span class="sxs-lookup"><span data-stu-id="12ff6-119">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 





