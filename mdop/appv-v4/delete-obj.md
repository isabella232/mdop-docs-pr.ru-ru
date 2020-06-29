---
title: DELETE OBJ (УДАЛИТЬ ОБЪЕКТ)
description: DELETE OBJ (УДАЛИТЬ ОБЪЕКТ)
author: dansimp
ms.assetid: fb17a261-f378-4ce6-a538-ab2f0ada0f2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d74fc1ac098d7dc4dd2f28633e9ca58d4211d74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821702"
---
# <span data-ttu-id="e2316-103">DELETE OBJ (УДАЛИТЬ ОБЪЕКТ)</span><span class="sxs-lookup"><span data-stu-id="e2316-103">DELETE OBJ</span></span>


<span data-ttu-id="e2316-104">Удаляет все записи приложения.</span><span class="sxs-lookup"><span data-stu-id="e2316-104">Removes all of your application records.</span></span>

`SFTMIME DELETE OBJ:APP [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e2316-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="e2316-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="e2316-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e2316-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e2316-107">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="e2316-107">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="e2316-108">Если указано, удаляются все приложения.</span><span class="sxs-lookup"><span data-stu-id="e2316-108">If specified, all applications are removed.</span></span> <span data-ttu-id="e2316-109">По умолчанию удаляются только те приложения, к которым у текущего пользователя есть доступ.</span><span class="sxs-lookup"><span data-stu-id="e2316-109">By default, only applications the current user has access to are removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e2316-110">/LOG</span><span class="sxs-lookup"><span data-stu-id="e2316-110">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="e2316-111">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="e2316-111">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e2316-112">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="e2316-112">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="e2316-113">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="e2316-113">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e2316-114">/GUI</span><span class="sxs-lookup"><span data-stu-id="e2316-114">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="e2316-115">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="e2316-115">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e2316-116">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="e2316-116">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e2316-117">/LOGU</span><span class="sxs-lookup"><span data-stu-id="e2316-117">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="e2316-118">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="e2316-118">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e2316-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e2316-119">Related topics</span></span>


[<span data-ttu-id="e2316-120">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="e2316-120">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





