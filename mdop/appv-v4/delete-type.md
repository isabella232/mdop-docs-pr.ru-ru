---
title: DELETE TYPE (УДАЛИТЬ ТИП)
description: DELETE TYPE (УДАЛИТЬ ТИП)
author: dansimp
ms.assetid: f2852723-c894-49f3-a3c5-56f9648bb9ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0df68c0a0efcd0e269410d1580f7b0a82301c46d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821689"
---
# <span data-ttu-id="4e1d5-103">DELETE TYPE (УДАЛИТЬ ТИП)</span><span class="sxs-lookup"><span data-stu-id="4e1d5-103">DELETE TYPE</span></span>


<span data-ttu-id="4e1d5-104">Удаляет указанную связь типа файлов.</span><span class="sxs-lookup"><span data-stu-id="4e1d5-104">Removes the specified file type association.</span></span>

`SFTMIME DELETE TYPE:file-extension [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4e1d5-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="4e1d5-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="4e1d5-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4e1d5-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e1d5-107">Тип: &lt; расширение файла&gt;</span><span class="sxs-lookup"><span data-stu-id="4e1d5-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e1d5-108">Расширение имени файла, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4e1d5-108">The file name extension to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e1d5-109">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="4e1d5-109">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e1d5-110">Если задано значение, указывает на то, что глобальную ассоциацию для расширения имени файла следует удалить.</span><span class="sxs-lookup"><span data-stu-id="4e1d5-110">If specified, indicates that the global association for the file name extension should be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e1d5-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="4e1d5-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e1d5-112">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="4e1d5-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e1d5-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="4e1d5-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e1d5-114">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="4e1d5-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e1d5-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="4e1d5-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e1d5-116">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="4e1d5-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4e1d5-117">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="4e1d5-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e1d5-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="4e1d5-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e1d5-119">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="4e1d5-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4e1d5-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4e1d5-120">Related topics</span></span>


[<span data-ttu-id="4e1d5-121">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="4e1d5-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





