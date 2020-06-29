---
title: CONFIGURE APP (НАСТРОИТЬ ПРИЛОЖЕНИЕ)
description: CONFIGURE APP (НАСТРОИТЬ ПРИЛОЖЕНИЕ)
author: dansimp
ms.assetid: fcfb4f86-8b7c-4208-bca3-955fd067079f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 42ff17e180df262deed3fe79674ad6fda6f0be4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819379"
---
# <span data-ttu-id="397e5-103">CONFIGURE APP (НАСТРОИТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="397e5-103">CONFIGURE APP</span></span>


<span data-ttu-id="397e5-104">Позволяет пользователю изменить значок, связанный с приложением, но не обновляет значок для существующих ярлыков или сопоставлений типов файлов.</span><span class="sxs-lookup"><span data-stu-id="397e5-104">Enables the user to change the icon associated with an application but does not update the icon on existing shortcuts or file type associations.</span></span>

`SFTMIME CONFIGURE APP:application /ICON icon-pathname                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="397e5-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="397e5-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="397e5-106">Описание</span><span class="sxs-lookup"><span data-stu-id="397e5-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="397e5-107">Приложение: &lt; приложение&gt;</span><span class="sxs-lookup"><span data-stu-id="397e5-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="397e5-108">Имя и версия (необязательно) приложения.</span><span class="sxs-lookup"><span data-stu-id="397e5-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="397e5-109">/ICON &lt; Icon (путь)&gt;</span><span class="sxs-lookup"><span data-stu-id="397e5-109">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="397e5-110">Путь или URL-адрес файла значка.</span><span class="sxs-lookup"><span data-stu-id="397e5-110">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="397e5-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="397e5-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="397e5-112">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="397e5-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="397e5-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="397e5-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="397e5-114">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="397e5-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="397e5-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="397e5-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="397e5-116">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="397e5-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="397e5-117">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="397e5-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="397e5-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="397e5-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="397e5-119">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="397e5-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="397e5-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="397e5-120">Related topics</span></span>


[<span data-ttu-id="397e5-121">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="397e5-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





