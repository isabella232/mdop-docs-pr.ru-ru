---
title: LOCK APP (ЗАБЛОКИРОВАТЬ ПРИЛОЖЕНИЕ)
description: LOCK APP (ЗАБЛОКИРОВАТЬ ПРИЛОЖЕНИЕ)
author: dansimp
ms.assetid: 30673433-4364-499f-8116-cb135fe2716f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 319271640c2550fc94479e876a59b30d3b2bf7ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816242"
---
# <span data-ttu-id="ea338-103">LOCK APP (ЗАБЛОКИРОВАТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="ea338-103">LOCK APP</span></span>


<span data-ttu-id="ea338-104">Блокирует приложение, указанное в кэше файловой системы.</span><span class="sxs-lookup"><span data-stu-id="ea338-104">Locks the application specified in the file system cache.</span></span>

`SFTMIME LOCK APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ea338-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="ea338-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="ea338-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ea338-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea338-107">Приложение: &lt; приложение&gt;</span><span class="sxs-lookup"><span data-stu-id="ea338-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea338-108">Имя и версия (необязательно) блокируемого приложения.</span><span class="sxs-lookup"><span data-stu-id="ea338-108">The name and version (optional) of the application to lock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea338-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="ea338-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea338-110">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="ea338-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea338-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="ea338-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea338-112">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ea338-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea338-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="ea338-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea338-114">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="ea338-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ea338-115">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="ea338-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea338-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="ea338-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea338-117">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="ea338-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ea338-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ea338-118">Related topics</span></span>


[<span data-ttu-id="ea338-119">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="ea338-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





