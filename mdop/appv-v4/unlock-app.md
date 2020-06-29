---
title: UNLOCK APP (РАЗБЛОКИРОВАТЬ ПРИЛОЖЕНИЕ)
description: UNLOCK APP (РАЗБЛОКИРОВАТЬ ПРИЛОЖЕНИЕ)
author: dansimp
ms.assetid: 91fc8ceb-b4f5-4a06-8193-05189f830943
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2ea47191450014856b4a9823728e3e275c7fb4cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815142"
---
# <span data-ttu-id="ad3ab-103">UNLOCK APP (РАЗБЛОКИРОВАТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="ad3ab-103">UNLOCK APP</span></span>


<span data-ttu-id="ad3ab-104">Разблокирует приложение, указанное в кэше файловой системы.</span><span class="sxs-lookup"><span data-stu-id="ad3ab-104">Unlocks the application specified in the file system cache.</span></span>

`SFTMIME UNLOCK APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad3ab-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="ad3ab-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="ad3ab-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ad3ab-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad3ab-107">Приложение: &lt; приложение&gt;</span><span class="sxs-lookup"><span data-stu-id="ad3ab-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad3ab-108">Имя и версия (необязательно) приложения, которые нужно разблокировать.</span><span class="sxs-lookup"><span data-stu-id="ad3ab-108">The name and version (optional) of the application to unlock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad3ab-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="ad3ab-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad3ab-110">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="ad3ab-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad3ab-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="ad3ab-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad3ab-112">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ad3ab-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad3ab-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="ad3ab-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad3ab-114">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="ad3ab-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ad3ab-115">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="ad3ab-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad3ab-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="ad3ab-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad3ab-117">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="ad3ab-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ad3ab-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ad3ab-118">Related topics</span></span>


[<span data-ttu-id="ad3ab-119">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="ad3ab-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





