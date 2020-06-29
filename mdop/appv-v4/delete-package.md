---
title: DELETE PACKAGE (УДАЛИТЬ ПАКЕТ)
description: DELETE PACKAGE (УДАЛИТЬ ПАКЕТ)
author: dansimp
ms.assetid: 8f7a4598-610d-490e-a224-426acce01a9f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0051967ca308e88d143b8116330f5d770d6086d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821699"
---
# <span data-ttu-id="3af13-103">DELETE PACKAGE (УДАЛИТЬ ПАКЕТ)</span><span class="sxs-lookup"><span data-stu-id="3af13-103">DELETE PACKAGE</span></span>


<span data-ttu-id="3af13-104">Удаляет запись пакета и связанные с ней приложения.</span><span class="sxs-lookup"><span data-stu-id="3af13-104">Removes a package record and the applications associated with it.</span></span>

`SFTMIME DELETE PACKAGE:package-name                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3af13-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="3af13-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="3af13-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3af13-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3af13-107">Пакет: &lt; имя пакета&gt;</span><span class="sxs-lookup"><span data-stu-id="3af13-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="3af13-108">Имя удаляемого пакета.</span><span class="sxs-lookup"><span data-stu-id="3af13-108">The name of the package to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3af13-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="3af13-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="3af13-110">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="3af13-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3af13-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="3af13-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3af13-112">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="3af13-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3af13-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="3af13-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="3af13-114">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="3af13-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3af13-115">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="3af13-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3af13-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="3af13-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="3af13-117">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="3af13-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3af13-118">**Важно!**  Команда удалить пакет всегда выполняет глобальное удаление пакета и удаляет только глобальные типы файлов и сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="3af13-118">**Important** The DELETE PACKAGE command always performs a global delete of the package and deletes only global file types and shortcuts.</span></span>

<span data-ttu-id="3af13-119">Если пакет является глобальным, эту команду необходимо запустить от имени локального администратора; в противном случае требуется только разрешение **DeleteApp** .</span><span class="sxs-lookup"><span data-stu-id="3af13-119">If the package is global, this command must be run as local Administrator; otherwise, only **DeleteApp** permission is needed.</span></span>

 

## <span data-ttu-id="3af13-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3af13-120">Related topics</span></span>


[<span data-ttu-id="3af13-121">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="3af13-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





