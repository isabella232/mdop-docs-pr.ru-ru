---
title: ADD TYPE (ДОБАВИТЬ ТИП)
description: ADD TYPE (ДОБАВИТЬ ТИП)
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822382"
---
# <span data-ttu-id="44c16-103">ADD TYPE (ДОБАВИТЬ ТИП)</span><span class="sxs-lookup"><span data-stu-id="44c16-103">ADD TYPE</span></span>


<span data-ttu-id="44c16-104">Добавляет указанную ассоциацию типов файлов.</span><span class="sxs-lookup"><span data-stu-id="44c16-104">Adds the specified file type association.</span></span>

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="44c16-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="44c16-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="44c16-106">Описание</span><span class="sxs-lookup"><span data-stu-id="44c16-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44c16-107">Тип: &lt; расширение файла&gt;</span><span class="sxs-lookup"><span data-stu-id="44c16-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-108">Расширение имени файла, которое будет сопоставлено указанному приложению.</span><span class="sxs-lookup"><span data-stu-id="44c16-108">The file name extension that will be associated with the application specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44c16-109">&lt;Приложение/App&gt;</span><span class="sxs-lookup"><span data-stu-id="44c16-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-110">Имя и версия (необязательно) приложения.</span><span class="sxs-lookup"><span data-stu-id="44c16-110">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44c16-111">/ICON &lt; Icon (путь)&gt;</span><span class="sxs-lookup"><span data-stu-id="44c16-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-112">Путь или URL-адрес файла значка.</span><span class="sxs-lookup"><span data-stu-id="44c16-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44c16-113">&lt;Тип/Description — DESC&gt;</span><span class="sxs-lookup"><span data-stu-id="44c16-113">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-114">Удобное для пользователя имя типа файлов.</span><span class="sxs-lookup"><span data-stu-id="44c16-114">The user-friendly name for the file type.</span></span> <span data-ttu-id="44c16-115">По умолчанию — &quot; файл расширения.&quot;</span><span class="sxs-lookup"><span data-stu-id="44c16-115">Defaults to &quot;EXTENSION File.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44c16-116">&lt;Тип содержимого/Content-Type&gt;</span><span class="sxs-lookup"><span data-stu-id="44c16-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-117">Тип содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="44c16-117">The content type of the file.</span></span> <span data-ttu-id="44c16-118">По умолчанию &quot; — расширение Application/Softricity.&quot;</span><span class="sxs-lookup"><span data-stu-id="44c16-118">Defaults to &quot;application/softricity-extension.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44c16-119">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="44c16-119">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-120">Если он указан, пакет будет доступен для всех пользователей на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="44c16-120">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44c16-121">/PERCEIVED-TYPE &lt; распознанный тип&gt;</span><span class="sxs-lookup"><span data-stu-id="44c16-121">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-122">Воспринимаемый тип файла.</span><span class="sxs-lookup"><span data-stu-id="44c16-122">The perceived type of the file.</span></span> <span data-ttu-id="44c16-123">Значение по умолчанию — Nothing.</span><span class="sxs-lookup"><span data-stu-id="44c16-123">Defaults to nothing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44c16-124">&lt;Идентификатор ProgID/ProgID&gt;</span><span class="sxs-lookup"><span data-stu-id="44c16-124">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-125">Программный идентификатор для типа файла.</span><span class="sxs-lookup"><span data-stu-id="44c16-125">The programmatic identifier for the file type.</span></span> <span data-ttu-id="44c16-126">По умолчанию — приложение virt. расширение. File.</span><span class="sxs-lookup"><span data-stu-id="44c16-126">Defaults to App Virt.extension.File.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44c16-127">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="44c16-127">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-128">Указывает, должны ли пользователи загружать файл этого типа получать запросы на открытие или сохранение файла.</span><span class="sxs-lookup"><span data-stu-id="44c16-128">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span> <span data-ttu-id="44c16-129">По умолчанию используется значение Да.</span><span class="sxs-lookup"><span data-stu-id="44c16-129">Defaults to YES.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44c16-130">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="44c16-130">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-131">Указывает, должно ли расширение файла всегда отображаться, даже если пользователь запрашивает, чтобы все расширения были скрыты.</span><span class="sxs-lookup"><span data-stu-id="44c16-131">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span> <span data-ttu-id="44c16-132">По умолчанию — нет.</span><span class="sxs-lookup"><span data-stu-id="44c16-132">Defaults to NO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44c16-133">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="44c16-133">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-134">Указывает, следует ли добавить запись в меню "создать" <strong> оболочки </strong> .</span><span class="sxs-lookup"><span data-stu-id="44c16-134">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span> <span data-ttu-id="44c16-135">По умолчанию — нет.</span><span class="sxs-lookup"><span data-stu-id="44c16-135">Defaults to NO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44c16-136">/LOG</span><span class="sxs-lookup"><span data-stu-id="44c16-136">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-137">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="44c16-137">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44c16-138">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="44c16-138">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-139">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="44c16-139">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44c16-140">/GUI</span><span class="sxs-lookup"><span data-stu-id="44c16-140">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-141">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="44c16-141">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="44c16-142">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="44c16-142">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44c16-143">/LOGU</span><span class="sxs-lookup"><span data-stu-id="44c16-143">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="44c16-144">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="44c16-144">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="44c16-145">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="44c16-145">Related topics</span></span>


[<span data-ttu-id="44c16-146">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="44c16-146">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





