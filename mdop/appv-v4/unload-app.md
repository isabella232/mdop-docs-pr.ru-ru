---
title: UNLOAD APP (ВЫГРУЗИТЬ ПРИЛОЖЕНИЕ)
description: UNLOAD APP (ВЫГРУЗИТЬ ПРИЛОЖЕНИЕ)
author: dansimp
ms.assetid: f0d729ae-8772-498b-be11-1a4b35499c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1ae30f5b8c788f8763c2c2b9d1c1956182750d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815152"
---
# <span data-ttu-id="103d0-103">UNLOAD APP (ВЫГРУЗИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="103d0-103">UNLOAD APP</span></span>


<span data-ttu-id="103d0-104">Выгружает приложение и все другие приложения из пакета из кэша файловой системы.</span><span class="sxs-lookup"><span data-stu-id="103d0-104">Unloads the application and all other applications in the package from the file system cache.</span></span>

`SFTMIME UNLOAD APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="103d0-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="103d0-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="103d0-106">Описание</span><span class="sxs-lookup"><span data-stu-id="103d0-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="103d0-107">Приложение: &lt; приложение&gt;</span><span class="sxs-lookup"><span data-stu-id="103d0-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="103d0-108">Имя и версия (необязательно) выгружаемый приложение.</span><span class="sxs-lookup"><span data-stu-id="103d0-108">The name and version (optional) of the application to unload.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="103d0-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="103d0-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="103d0-110">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="103d0-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="103d0-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="103d0-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="103d0-112">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="103d0-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="103d0-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="103d0-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="103d0-114">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="103d0-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="103d0-115">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="103d0-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="103d0-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="103d0-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="103d0-117">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="103d0-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="103d0-118">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="103d0-118">Related topics</span></span>


[<span data-ttu-id="103d0-119">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="103d0-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





