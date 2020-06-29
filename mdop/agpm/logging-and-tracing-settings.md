---
title: Параметры ведения журнала и трассировки
description: Параметры ведения журнала и трассировки
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820589"
---
# <span data-ttu-id="78805-103">Параметры ведения журнала и трассировки</span><span class="sxs-lookup"><span data-stu-id="78805-103">Logging and Tracing Settings</span></span>


<span data-ttu-id="78805-104">Параметры шаблона администрирования для расширенного управления групповыми политиками позволяют централизованно настраивать параметры ведения журнала и трассировки для серверов и клиентов, которым применяется объект групповой политики (GPO) с этими параметрами.</span><span class="sxs-lookup"><span data-stu-id="78805-104">The Administrative Template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure logging and tracing options for AGPM Servers and clients to which a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="78805-105">Следующий параметр доступен в разделе Computer Configuration\\Administrative Templates\\Windows Components\\AGPM в **редакторе объектов групповой политики** при редактировании GPO в консоли управления групповыми политиками (GPMC).</span><span class="sxs-lookup"><span data-stu-id="78805-105">The following setting is available under Computer Configuration\\Administrative Templates\\Windows Components\\AGPM in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="78805-106">Если этот путь не отображается, щелкните правой кнопкой мыши папку **Административные шаблоны**и добавьте шаблон для расширенного управления групповыми политиками (, ADMX. adm).</span><span class="sxs-lookup"><span data-stu-id="78805-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<span data-ttu-id="78805-107">**Расположение файлов трассировки**:</span><span class="sxs-lookup"><span data-stu-id="78805-107">**Trace file locations**:</span></span>

-   <span data-ttu-id="78805-108">Клиент:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="78805-108">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

-   <span data-ttu-id="78805-109">Сервер:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="78805-109">Server: %CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="78805-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="78805-110">Setting</span></span></th>
<th align="left"><span data-ttu-id="78805-111">Эффект</span><span class="sxs-lookup"><span data-stu-id="78805-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="78805-112">Ведение журнала РАСШИРЕНного протоколирования</span><span class="sxs-lookup"><span data-stu-id="78805-112">AGPM Logging</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="78805-113">Если включено, этот параметр определяет, включена ли трассировка, и уровень детализации.</span><span class="sxs-lookup"><span data-stu-id="78805-113">If enabled, this setting configures whether tracing is turned on and the level of detail.</span></span> <span data-ttu-id="78805-114">Этот параметр влияет на клиентские и серверные компоненты с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="78805-114">This setting affects both client and server components of AGPM.</span></span></p>
<p><span data-ttu-id="78805-115">Если отключено или не задано, этот параметр не действует.</span><span class="sxs-lookup"><span data-stu-id="78805-115">If disabled or not configured, this setting has no effect.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="78805-116">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="78805-116">Additional references</span></span>

-   [<span data-ttu-id="78805-117">Параметры административных шаблонов</span><span class="sxs-lookup"><span data-stu-id="78805-117">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 





