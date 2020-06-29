---
title: DELETE APP (УДАЛИТЬ ПРИЛОЖЕНИЕ)
description: DELETE APP (УДАЛИТЬ ПРИЛОЖЕНИЕ)
author: dansimp
ms.assetid: 2f89c0c0-373b-4389-a26d-67b3f9712957
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c27c70ef3227ebaf6b16bcb1fbb4b4e65b7cb7f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821719"
---
# <span data-ttu-id="16e36-103">DELETE APP (УДАЛИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="16e36-103">DELETE APP</span></span>


<span data-ttu-id="16e36-104">Удаляет запись приложения из кэша файловой системы, чтобы сделать ее более невидимой.</span><span class="sxs-lookup"><span data-stu-id="16e36-104">Removes an application record from the file system cache to make it no longer visible.</span></span> <span data-ttu-id="16e36-105">Ярлыки пользователей и сопоставления типов файлов скрыты, но не удаляются.</span><span class="sxs-lookup"><span data-stu-id="16e36-105">Users’ shortcuts and file type associations are hidden but not deleted.</span></span> <span data-ttu-id="16e36-106">Пользовательские параметры не удаляются.</span><span class="sxs-lookup"><span data-stu-id="16e36-106">No user settings are removed.</span></span>

`SFTMIME DELETE APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="16e36-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="16e36-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="16e36-108">Описание</span><span class="sxs-lookup"><span data-stu-id="16e36-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16e36-109">Приложение: &lt; приложение&gt;</span><span class="sxs-lookup"><span data-stu-id="16e36-109">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="16e36-110">Имя и версия (необязательно) приложения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="16e36-110">The name and version (optional) of the application to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16e36-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="16e36-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="16e36-112">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="16e36-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16e36-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="16e36-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="16e36-114">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="16e36-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16e36-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="16e36-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="16e36-116">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="16e36-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="16e36-117">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="16e36-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16e36-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="16e36-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="16e36-119">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="16e36-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="16e36-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="16e36-120">Related topics</span></span>


[<span data-ttu-id="16e36-121">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="16e36-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





