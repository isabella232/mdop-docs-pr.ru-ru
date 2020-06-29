---
title: CONFIGURE TYPE (НАСТРОИТЬ ТИП)
description: CONFIGURE TYPE (НАСТРОИТЬ ТИП)
author: dansimp
ms.assetid: 2caf9433-5449-486f-ab94-83ee8e44d7f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b70cdd1b27eba0109183f1eb9cfb42f08b3f341
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821939"
---
# <span data-ttu-id="4f91b-103">CONFIGURE TYPE (НАСТРОИТЬ ТИП)</span><span class="sxs-lookup"><span data-stu-id="4f91b-103">CONFIGURE TYPE</span></span>


<span data-ttu-id="4f91b-104">Позволяет пользователю изменять параметры сопоставления типов файлов.</span><span class="sxs-lookup"><span data-stu-id="4f91b-104">Enables the user to change settings for a file type association.</span></span>

`SFTMIME CONFIGURE TYPE:file-extension [/GLOBAL] [/APP application]                 [/ICON icon-pathname] [/DESCRIPTION type-desc]                 [/CONTENT-TYPE content-type] [/PERCEIVED-TYPE perceived-type]                 [/PROGID progid] [/CONFIRMOPEN {YES|NO}]                 [/SHOWEXT {YES|NO}] [/NEWMENU {YES|NO}]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4f91b-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="4f91b-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="4f91b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4f91b-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f91b-107">Тип: &lt; расширение файла&gt;</span><span class="sxs-lookup"><span data-stu-id="4f91b-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-108">Расширение имени файла, которое нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="4f91b-108">The file name extension to be configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f91b-109">&lt;Приложение/App&gt;</span><span class="sxs-lookup"><span data-stu-id="4f91b-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-110">Имя и версия (необязательно) приложения, которым нужно сопоставить этот тип файлов.</span><span class="sxs-lookup"><span data-stu-id="4f91b-110">The name and version (optional) of the application to associate this file type with.</span></span> <span data-ttu-id="4f91b-111">Не может быть указан с PROGID.</span><span class="sxs-lookup"><span data-stu-id="4f91b-111">Cannot be specified with PROGID.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f91b-112">/ICON &lt; Icon (путь)&gt;</span><span class="sxs-lookup"><span data-stu-id="4f91b-112">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-113">Путь или URL-адрес файла значка.</span><span class="sxs-lookup"><span data-stu-id="4f91b-113">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f91b-114">&lt;Тип/Description — DESC&gt;</span><span class="sxs-lookup"><span data-stu-id="4f91b-114">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-115">Удобное для пользователя имя типа файлов.</span><span class="sxs-lookup"><span data-stu-id="4f91b-115">The user-friendly name for the file type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f91b-116">&lt;Тип содержимого/Content-Type&gt;</span><span class="sxs-lookup"><span data-stu-id="4f91b-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-117">Тип содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="4f91b-117">The content type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f91b-118">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="4f91b-118">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-119">Если задано значение, это означает, что необходимо изменить связь, которая применяется ко всем пользователям, а не для конкретного пользователя.</span><span class="sxs-lookup"><span data-stu-id="4f91b-119">If present, indicates that the association that applies to all users should be edited, not the user-specific one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f91b-120">/PERCEIVED-TYPE &lt; распознанный тип&gt;</span><span class="sxs-lookup"><span data-stu-id="4f91b-120">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-121">Воспринимаемый тип файла.</span><span class="sxs-lookup"><span data-stu-id="4f91b-121">The perceived type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f91b-122">&lt;Идентификатор ProgID/ProgID&gt;</span><span class="sxs-lookup"><span data-stu-id="4f91b-122">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-123">Указывает, что расширение должно быть связано с другим типом файла.</span><span class="sxs-lookup"><span data-stu-id="4f91b-123">Indicates that the extension should be associated with a different file type.</span></span> <span data-ttu-id="4f91b-124">Предыдущий тип файлов не удаляется.</span><span class="sxs-lookup"><span data-stu-id="4f91b-124">The previous file type is not deleted.</span></span> <span data-ttu-id="4f91b-125">Не может быть указан с помощью приложения, ЗНАЧКа, описания, CONFIRMOPEN или SHOWEXT.</span><span class="sxs-lookup"><span data-stu-id="4f91b-125">Cannot be specified with APP, ICON, DESCRIPTION, CONFIRMOPEN, or SHOWEXT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f91b-126">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="4f91b-126">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-127">Указывает, должны ли пользователи загружать файл этого типа получать запросы на открытие или сохранение файла.</span><span class="sxs-lookup"><span data-stu-id="4f91b-127">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f91b-128">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="4f91b-128">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-129">Указывает, должно ли расширение файла всегда отображаться, даже если пользователь запрашивает, чтобы все расширения были скрыты.</span><span class="sxs-lookup"><span data-stu-id="4f91b-129">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f91b-130">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="4f91b-130">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-131">Указывает, следует ли добавить запись в меню "создать" <strong> оболочки </strong> .</span><span class="sxs-lookup"><span data-stu-id="4f91b-131">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f91b-132">/LOG</span><span class="sxs-lookup"><span data-stu-id="4f91b-132">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-133">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="4f91b-133">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f91b-134">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="4f91b-134">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-135">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="4f91b-135">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f91b-136">/GUI</span><span class="sxs-lookup"><span data-stu-id="4f91b-136">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-137">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="4f91b-137">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4f91b-138">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="4f91b-138">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f91b-139">/LOGU</span><span class="sxs-lookup"><span data-stu-id="4f91b-139">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f91b-140">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="4f91b-140">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4f91b-141">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4f91b-141">Related topics</span></span>


[<span data-ttu-id="4f91b-142">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="4f91b-142">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





