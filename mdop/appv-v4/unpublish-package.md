---
title: UNPUBLISH PACKAGE (ОТМЕНИТЬ ПУБЛИКАЦИЮ ПАКЕТА)
description: UNPUBLISH PACKAGE (ОТМЕНИТЬ ПУБЛИКАЦИЮ ПАКЕТА)
author: dansimp
ms.assetid: 1651427c-72a5-4701-bb57-71e14a7a3803
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7704fb3ed03be4864a837767d9e890d28b63f175
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815132"
---
# <span data-ttu-id="99421-103">UNPUBLISH PACKAGE (ОТМЕНИТЬ ПУБЛИКАЦИЮ ПАКЕТА)</span><span class="sxs-lookup"><span data-stu-id="99421-103">UNPUBLISH PACKAGE</span></span>


<span data-ttu-id="99421-104">Позволяет удалить сочетания клавиш и типы файлов для всего пакета.</span><span class="sxs-lookup"><span data-stu-id="99421-104">Enables you to remove the shortcuts and file types for an entire package.</span></span>

`SFTMIME UNPUBLISH PACKAGE:package-name [/CLEAR] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="99421-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="99421-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="99421-106">Описание</span><span class="sxs-lookup"><span data-stu-id="99421-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="99421-107">Пакет: &lt; имя пакета&gt;</span><span class="sxs-lookup"><span data-stu-id="99421-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="99421-108">Имя пакета.</span><span class="sxs-lookup"><span data-stu-id="99421-108">The name of the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="99421-109">/CLEAR</span><span class="sxs-lookup"><span data-stu-id="99421-109">/CLEAR</span></span></p></td>
<td align="left"><p><span data-ttu-id="99421-110">Если параметр указан, параметры пользователя также будут удалены.</span><span class="sxs-lookup"><span data-stu-id="99421-110">If present, user settings will also be removed.</span></span> <span data-ttu-id="99421-111">(Дополнительные сведения можно найти в разделе важное примечание ниже в этой статье.)</span><span class="sxs-lookup"><span data-stu-id="99421-111">(For more information, see the Important note later in this topic.)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="99421-112">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="99421-112">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="99421-113">Если он указан, пакет будет отменен для всех пользователей на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="99421-113">If present, the package will be unpublished for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="99421-114">/LOG</span><span class="sxs-lookup"><span data-stu-id="99421-114">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="99421-115">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="99421-115">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="99421-116">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="99421-116">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="99421-117">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="99421-117">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="99421-118">/GUI</span><span class="sxs-lookup"><span data-stu-id="99421-118">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="99421-119">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="99421-119">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="99421-120">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="99421-120">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="99421-121">/LOGU</span><span class="sxs-lookup"><span data-stu-id="99421-121">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="99421-122">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="99421-122">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="99421-123">**Важно!**  Прежде чем можно будет выполнить команду **отмены публикации пакета** , пакет должен быть уже добавлен в клиент Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="99421-123">**Important** Before you can run the **UNPUBLISH PACKAGE** command, the package must already have been added to the Application Virtualization Client.</span></span>

<span data-ttu-id="99421-124">Чтобы использовать **глобальную**программу, **отменить публикацию** , необходимо запустить ее от имени локального администратора. в противном случае требуется только разрешение **ClearApp** .</span><span class="sxs-lookup"><span data-stu-id="99421-124">To use **GLOBAL**, **UNPUBLISH PACKAGE** must be run as local Administrator; otherwise, only **ClearApp** permission is needed.</span></span>

<span data-ttu-id="99421-125">С помощью команды отменить **публикацию** в **глобальном шаблоне** удаляются все глобальные типы файлов и сочетания клавиш для пакета.</span><span class="sxs-lookup"><span data-stu-id="99421-125">Using **UNPUBLISH PACKAGE** with **GLOBAL** removes any global file types and shortcuts for the package.</span></span> <span data-ttu-id="99421-126">**Очистка** неприменима.</span><span class="sxs-lookup"><span data-stu-id="99421-126">**CLEAR** is not applicable.</span></span>

<span data-ttu-id="99421-127">Использование команды " **отменить публикацию** " без **глобального** удаления сочетаний клавиш и типов файлов для пакета и, если задано значение **clear** , приводит к удалению пользовательских настроек и остановке фоновой загрузки в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="99421-127">Using **UNPUBLISH PACKAGE** without **GLOBAL** removes the user shortcuts and file types for the package and, if **CLEAR** is set, also removes user settings and stops background loads under the user’s context.</span></span>

<span data-ttu-id="99421-128">**Пакет отмены публикации** работает в приложениях с тем же именем пакета или GUID, который использовался в качестве идентификатора источника для **добавления**, **изменения**и **публикации пакета**.</span><span class="sxs-lookup"><span data-stu-id="99421-128">**UNPUBLISH PACKAGE** works on applications from the same package name or GUID that was used as the source ID for **ADD**, **EDIT**, and **PUBLISH PACKAGE**.</span></span>

<span data-ttu-id="99421-129">Команда отменить **публикацию** всегда очищает все параметры пользователя, ярлыки и типы файлов независимо от использования переключателя/Clear.</span><span class="sxs-lookup"><span data-stu-id="99421-129">**UNPUBLISH PACKAGE** always clears all the user settings, shortcuts, and file types regardless of the use of the /CLEAR switch.</span></span>

 

## <span data-ttu-id="99421-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="99421-130">Related topics</span></span>


[<span data-ttu-id="99421-131">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="99421-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





