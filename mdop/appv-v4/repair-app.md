---
title: REPAIR APP (ВОССТАНОВИТЬ ПРИЛОЖЕНИЕ)
description: REPAIR APP (ВОССТАНОВИТЬ ПРИЛОЖЕНИЕ)
author: dansimp
ms.assetid: 892b556b-612d-4531-890e-4cfc2ac88d9f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 791628efd22b0ad429a09e48a82e2d55b45783bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815722"
---
# <span data-ttu-id="417db-103">REPAIR APP (ВОССТАНОВИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="417db-103">REPAIR APP</span></span>


<span data-ttu-id="417db-104">Эта команда сбрасывает личные параметры для приложения.</span><span class="sxs-lookup"><span data-stu-id="417db-104">This command resets your personal settings for an application.</span></span>

`SFTMIME REPAIR APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="417db-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="417db-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="417db-106">Описание</span><span class="sxs-lookup"><span data-stu-id="417db-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="417db-107">Приложение: &lt; приложение&gt;</span><span class="sxs-lookup"><span data-stu-id="417db-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="417db-108">Имя и версия (необязательно) приложения.</span><span class="sxs-lookup"><span data-stu-id="417db-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="417db-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="417db-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="417db-110">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="417db-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="417db-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="417db-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="417db-112">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="417db-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="417db-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="417db-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="417db-114">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="417db-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="417db-115">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="417db-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="417db-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="417db-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="417db-117">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="417db-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="417db-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="417db-118">Related topics</span></span>


[<span data-ttu-id="417db-119">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="417db-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





