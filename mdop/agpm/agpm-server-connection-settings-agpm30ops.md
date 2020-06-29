---
title: Параметры подключения к серверу AGPM
description: Параметры подключения к серверу AGPM
author: dansimp
ms.assetid: 5f03e397-b868-4c49-9cbf-a5f5d0ddcc39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9ee1e67eb2c565bcf833314d82cdf611e2caa85
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812989"
---
# <span data-ttu-id="994a6-103">Параметры подключения к серверу AGPM</span><span class="sxs-lookup"><span data-stu-id="994a6-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="994a6-104">Вы можете использовать параметры шаблона для расширенного управления групповыми политиками, чтобы централизованно настроить подключения к серверу РАСШИРЕНной политики для администраторов групповых политик, которым применен объект групповой политики (GPO) с этими параметрами.</span><span class="sxs-lookup"><span data-stu-id="994a6-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy Object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="994a6-105">Следующие параметры доступны в разделе User Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM при редактировании объекта групповой политики.</span><span class="sxs-lookup"><span data-stu-id="994a6-105">The following settings are available under User Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="994a6-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="994a6-106">Setting</span></span></th>
<th align="left"><span data-ttu-id="994a6-107">Эффект</span><span class="sxs-lookup"><span data-stu-id="994a6-107">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="994a6-108">ГРУППОВое руководство: определение сервера по умолчанию с РАСШИРЕНным доступом (все домены)</span><span class="sxs-lookup"><span data-stu-id="994a6-108">AGPM: Specify default AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="994a6-109">Этот параметр политики позволяет указать используемый по умолчанию сервер РАСШИРЕНного доменных политик для всех доменов.</span><span class="sxs-lookup"><span data-stu-id="994a6-109">This policy setting allows you to specify a default AGPM Server for all domains.</span></span> <span data-ttu-id="994a6-110">Этот параметр используется только клиентами РАСШИРЕНного доступа к данным и ограничивает администраторам групповой политики подключение к другому архиву.</span><span class="sxs-lookup"><span data-stu-id="994a6-110">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to another archive.</span></span> <span data-ttu-id="994a6-111">Вы можете переопределить это значение по умолчанию для отдельных доменов с помощью <strong> параметра "указать серверы расширенного использования функций" </strong> .</span><span class="sxs-lookup"><span data-stu-id="994a6-111">You can override this default for individual domains using the <strong>AGPM: Specify AGPM Servers</strong> setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="994a6-112">ГРУППОВое руководство: Указание серверов с РАСШИРЕНным определением</span><span class="sxs-lookup"><span data-stu-id="994a6-112">AGPM: Specify AGPM Servers</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="994a6-113">Этот параметр политики позволяет указать серверы РАСШИРЕНного выбора для отдельных доменов.</span><span class="sxs-lookup"><span data-stu-id="994a6-113">This policy setting allows you to specify the AGPM Servers for individual domains.</span></span> <span data-ttu-id="994a6-114">Этот параметр используется только клиентами РАСШИРЕНного доступа к данным и ограничивает администраторам групповой политики подключение к другому архиву для указанного домена.</span><span class="sxs-lookup"><span data-stu-id="994a6-114">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to a different archive for the specified domain.</span></span> <span data-ttu-id="994a6-115">Чтобы указать сервер по умолчанию с помощью РАСШИРЕНного использования служб, используйте <strong> параметр групповой политики (все домены) </strong> и используйте этот параметр, чтобы переопределить значение по умолчанию на уровне домена.</span><span class="sxs-lookup"><span data-stu-id="994a6-115">To specify a default AGPM Server, use the <strong>AGPM: Specify default AGPM Server (all domains)</strong> setting and use this policy setting to override the default on a per domain basis.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="994a6-116">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="994a6-116">Additional references</span></span>

-   [<span data-ttu-id="994a6-117">Папка административных шаблонов</span><span class="sxs-lookup"><span data-stu-id="994a6-117">Administrative Templates Folder</span></span>](administrative-templates-folder-agpm30ops.md)

-   [<span data-ttu-id="994a6-118">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="994a6-118">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

 

 





