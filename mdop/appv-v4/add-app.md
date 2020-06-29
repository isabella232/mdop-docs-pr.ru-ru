---
title: ADD APP (ДОБАВИТЬ ПРИЛОЖЕНИЕ)
description: ADD APP (ДОБАВИТЬ ПРИЛОЖЕНИЕ)
author: dansimp
ms.assetid: 329fd0c8-a795-49be-b0fd-1367c5b4a34b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac83c0cf130e8de1d34d42d74e946716e4503246
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819899"
---
# <span data-ttu-id="e4376-103">ADD APP (ДОБАВИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="e4376-103">ADD APP</span></span>


<span data-ttu-id="e4376-104">Добавляет запись приложения.</span><span class="sxs-lookup"><span data-stu-id="e4376-104">Adds an application record.</span></span>

`SFTMIME ADD APP:application /OSD osd-pathname [/ICON icon-pathname] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e4376-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="e4376-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="e4376-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e4376-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4376-107">Приложение: &lt; приложение&gt;</span><span class="sxs-lookup"><span data-stu-id="e4376-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4376-108">Имя и версия (необязательно) приложения.</span><span class="sxs-lookup"><span data-stu-id="e4376-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4376-109">/OSD &lt; OSD — PathName (путь)&gt;</span><span class="sxs-lookup"><span data-stu-id="e4376-109">/OSD &lt;osd-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4376-110">Путь или URL-адрес файла OSD.</span><span class="sxs-lookup"><span data-stu-id="e4376-110">The path or URL for the OSD file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4376-111">/ICON &lt; Icon (путь)&gt;</span><span class="sxs-lookup"><span data-stu-id="e4376-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4376-112">Путь или URL-адрес файла значка.</span><span class="sxs-lookup"><span data-stu-id="e4376-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4376-113">/LOG</span><span class="sxs-lookup"><span data-stu-id="e4376-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4376-114">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="e4376-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4376-115">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="e4376-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4376-116">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="e4376-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4376-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="e4376-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4376-118">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="e4376-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e4376-119">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="e4376-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4376-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="e4376-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4376-121">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="e4376-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e4376-122">**Примечание**  Получившееся имя приложения будет взято из OSD, а не из имени, указанного в APP: &lt; Application &gt; .</span><span class="sxs-lookup"><span data-stu-id="e4376-122">**Note** The resulting name of the application will be taken from the OSD file and not from the name provided in APP:&lt;application&gt;.</span></span>

 

## <span data-ttu-id="e4376-123">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e4376-123">Related topics</span></span>


[<span data-ttu-id="e4376-124">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="e4376-124">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





