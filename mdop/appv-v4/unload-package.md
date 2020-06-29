---
title: UNLOAD PACKAGE (ВЫГРУЗИТЬ ПАКЕТ)
description: UNLOAD PACKAGE (ВЫГРУЗИТЬ ПАКЕТ)
author: dansimp
ms.assetid: a076eb5a-ce3d-49e4-ac7a-4d4df10e3477
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fbee040f97bf5675ace7e873741a4270a993a911
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815149"
---
# <span data-ttu-id="c0780-103">UNLOAD PACKAGE (ВЫГРУЗИТЬ ПАКЕТ)</span><span class="sxs-lookup"><span data-stu-id="c0780-103">UNLOAD PACKAGE</span></span>


<span data-ttu-id="c0780-104">Выгрузка пакета из кэша файловой системы.</span><span class="sxs-lookup"><span data-stu-id="c0780-104">Unloads the package from the file system cache.</span></span>

`SFTMIME UNLOAD PACKAGE:package-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0780-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="c0780-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="c0780-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c0780-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0780-107">Пакет: &lt; имя пакета&gt;</span><span class="sxs-lookup"><span data-stu-id="c0780-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0780-108">Имя пакета для выгрузки.</span><span class="sxs-lookup"><span data-stu-id="c0780-108">The name of the package to unload.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0780-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="c0780-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0780-110">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="c0780-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0780-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="c0780-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0780-112">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="c0780-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0780-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="c0780-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0780-114">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="c0780-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c0780-115">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="c0780-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0780-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="c0780-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0780-117">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="c0780-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c0780-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c0780-118">Related topics</span></span>


[<span data-ttu-id="c0780-119">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="c0780-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





