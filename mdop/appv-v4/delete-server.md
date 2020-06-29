---
title: DELETE SERVER (УДАЛИТЬ СЕРВЕР)
description: DELETE SERVER (УДАЛИТЬ СЕРВЕР)
author: dansimp
ms.assetid: 4c929639-1c1d-47c3-9225-cc4d7a8736f0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92af31a818174fb4b0e82a11c918af2484ac2bce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821692"
---
# <span data-ttu-id="5d052-103">DELETE SERVER (УДАЛИТЬ СЕРВЕР)</span><span class="sxs-lookup"><span data-stu-id="5d052-103">DELETE SERVER</span></span>


<span data-ttu-id="5d052-104">Удаляет сервер публикаций.</span><span class="sxs-lookup"><span data-stu-id="5d052-104">Removes a publishing server.</span></span>

<span data-ttu-id="5d052-105">**Примечание**  Эта команда не удаляет все приложения и пакеты, опубликованные клиентом сервером.</span><span class="sxs-lookup"><span data-stu-id="5d052-105">**Note** This command does not remove any applications or packages published to the client by the server.</span></span> <span data-ttu-id="5d052-106">Для каждого приложения используйте команду SFTMIME **clear App** , а затем команду **удалить пакет** , чтобы полностью удалить эти приложения и пакеты из клиента.</span><span class="sxs-lookup"><span data-stu-id="5d052-106">For each application, use the SFTMIME **CLEAR APP** command followed by the **DELETE PACKAGE** command to completely remove those applications and packages from the client.</span></span>

 

`SFTMIME DELETE SERVER:server-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5d052-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="5d052-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="5d052-108">Описание</span><span class="sxs-lookup"><span data-stu-id="5d052-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5d052-109">СЕРВЕР: &lt; имя сервера&gt;</span><span class="sxs-lookup"><span data-stu-id="5d052-109">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d052-110">Отображаемое имя сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="5d052-110">The display name of the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5d052-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="5d052-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d052-112">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="5d052-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5d052-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="5d052-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d052-114">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="5d052-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5d052-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="5d052-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d052-116">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="5d052-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="5d052-117">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="5d052-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5d052-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="5d052-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="5d052-119">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="5d052-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5d052-120">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5d052-120">Related topics</span></span>


[<span data-ttu-id="5d052-121">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="5d052-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





