---
title: CLEAR APP (ОЧИСТИТЬ ПРИЛОЖЕНИЕ)
description: CLEAR APP (ОЧИСТИТЬ ПРИЛОЖЕНИЕ)
author: dansimp
ms.assetid: c2e63031-5941-45e4-9863-127231cfa25b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26f2363bf15bd33d0da3fee48319b215e6791db9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821992"
---
# <span data-ttu-id="d5131-103">CLEAR APP (ОЧИСТИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="d5131-103">CLEAR APP</span></span>


<span data-ttu-id="d5131-104">Очищает параметры текущего пользователя и конфигурации публикации для приложения.</span><span class="sxs-lookup"><span data-stu-id="d5131-104">Clears the current user's settings and publishing configurations for an application.</span></span>

`SFTMIME CLEAR APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d5131-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="d5131-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="d5131-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d5131-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5131-107">Приложение: &lt; приложение&gt;</span><span class="sxs-lookup"><span data-stu-id="d5131-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5131-108">Имя и версия (необязательно) приложения.</span><span class="sxs-lookup"><span data-stu-id="d5131-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d5131-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="d5131-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5131-110">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="d5131-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5131-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="d5131-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5131-112">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="d5131-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d5131-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="d5131-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5131-114">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="d5131-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d5131-115">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="d5131-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5131-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="d5131-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5131-117">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="d5131-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d5131-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d5131-118">Related topics</span></span>


[<span data-ttu-id="d5131-119">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="d5131-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





