---
title: Параметры ведения журнала и трассировки
description: Параметры ведения журнала и трассировки
author: dansimp
ms.assetid: 858b6fbf-65b4-42fa-95a9-69b04e5734d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 078bda16b5fcf968d45e0c4890487471105e8c44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820592"
---
# <span data-ttu-id="fd518-103">Параметры ведения журнала и трассировки</span><span class="sxs-lookup"><span data-stu-id="fd518-103">Logging and Tracing Settings</span></span>


<span data-ttu-id="fd518-104">Параметры шаблона администрирования для расширенного управления групповыми политиками позволяют централизованно настраивать параметры ведения журнала и трассировки для серверов и клиентов, которым применяется объект групповой политики (GPO) с этими параметрами.</span><span class="sxs-lookup"><span data-stu-id="fd518-104">The Administrative template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure logging and tracing options for AGPM Servers and clients to which a Group Policy Object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="fd518-105">Следующий параметр доступен в разделе Computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM при редактировании объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="fd518-105">The following setting is available under Computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span>

<span data-ttu-id="fd518-106">**Расположение файлов трассировки**:</span><span class="sxs-lookup"><span data-stu-id="fd518-106">**Trace file locations**:</span></span>

-   <span data-ttu-id="fd518-107">Клиент:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="fd518-107">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

-   <span data-ttu-id="fd518-108">Сервер:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="fd518-108">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fd518-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="fd518-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="fd518-110">Эффект</span><span class="sxs-lookup"><span data-stu-id="fd518-110">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fd518-111">ГРУППОВое протоколирование: Настройка ведения журнала</span><span class="sxs-lookup"><span data-stu-id="fd518-111">AGPM: Configure logging</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fd518-112">Этот параметр политики позволяет включить и настроить ведение журнала для РАСШИРЕНного протоколирования.</span><span class="sxs-lookup"><span data-stu-id="fd518-112">This policy setting allows you to turn on and configure logging for AGPM.</span></span> <span data-ttu-id="fd518-113">Этот параметр влияет на клиентские и серверные компоненты с расширенным управлением групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="fd518-113">This setting affects both client and server components of AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="fd518-114">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="fd518-114">Additional references</span></span>

-   [<span data-ttu-id="fd518-115">Папка административных шаблонов</span><span class="sxs-lookup"><span data-stu-id="fd518-115">Administrative Templates Folder</span></span>](administrative-templates-folder-agpm30ops.md)

 

 





