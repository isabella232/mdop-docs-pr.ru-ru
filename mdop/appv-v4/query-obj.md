---
title: QUERY OBJ (ЗАПРОСИТЬ ОБЪЕКТ)
description: QUERY OBJ (ЗАПРОСИТЬ ОБЪЕКТ)
author: dansimp
ms.assetid: 55abf0d1-c779-4172-8357-552ab010933b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328e9feb96c70080531cbbc666d8ff1b86045ba5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815739"
---
# <span data-ttu-id="f1fe9-103">QUERY OBJ (ЗАПРОСИТЬ ОБЪЕКТ)</span><span class="sxs-lookup"><span data-stu-id="f1fe9-103">QUERY OBJ</span></span>


<span data-ttu-id="f1fe9-104">Возвращает список текущих приложений, пакетов, сопоставлений типов файлов или серверов публикаций с разделением табуляцией.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-104">Returns a tab-delimited list of current applications, packages, file type associations, or publishing servers.</span></span>

`SFTMIME QUERY OBJ:{APP|PACKAGE|TYPE|SERVER} [/SHORT] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE ]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f1fe9-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="f1fe9-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="f1fe9-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f1fe9-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1fe9-107">·</span><span class="sxs-lookup"><span data-stu-id="f1fe9-107">APP</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1fe9-108">Возвращает список приложений.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-108">Returns a list of applications.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1fe9-109">УПАКОВАТЬ</span><span class="sxs-lookup"><span data-stu-id="f1fe9-109">PACKAGE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1fe9-110">Возвращает список пакетов.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-110">Returns a list of packages.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1fe9-111">TYPE</span><span class="sxs-lookup"><span data-stu-id="f1fe9-111">TYPE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1fe9-112">Возвращает список сопоставлений типов файлов.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-112">Returns a list of file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1fe9-113">SERVER</span><span class="sxs-lookup"><span data-stu-id="f1fe9-113">SERVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1fe9-114">Возвращает список серверов публикации.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-114">Returns a list of publishing servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1fe9-115">/SHORT</span><span class="sxs-lookup"><span data-stu-id="f1fe9-115">/SHORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1fe9-116">Без отображения полных свойств каждый из них возвращает список имен приложений, пакетов, ассоциаций и имен серверов.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-116">Without displaying the full properties of each, returns a list of application names, packages, associations, or server names.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1fe9-117">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="f1fe9-117">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1fe9-118">Для приложений возвращаются все известные приложения, а не только те из них, к которым у текущего пользователя есть доступ.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-118">For applications, returns all known applications instead of only the ones the current user has access to.</span></span> <span data-ttu-id="f1fe9-119">Для пакетов возвращает все известные пакеты, а не только те из них, к которым у текущего пользователя есть доступ.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-119">For packages, returns all known packages instead of only the ones the current user has access to.</span></span> <span data-ttu-id="f1fe9-120">Для ассоциаций — возвращает только те связи, которые применяются ко всем пользователям, а не к определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-120">For associations, returns only associations that apply to all users, not user-specific ones.</span></span> <span data-ttu-id="f1fe9-121">Недопустимый для серверов.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-121">Not valid for servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1fe9-122">/LOG</span><span class="sxs-lookup"><span data-stu-id="f1fe9-122">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1fe9-123">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-123">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1fe9-124">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="f1fe9-124">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1fe9-125">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="f1fe9-125">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f1fe9-126">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-126">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1fe9-127">/LOGU</span><span class="sxs-lookup"><span data-stu-id="f1fe9-127">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1fe9-128">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-128">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f1fe9-129">**Примечание**  В версии 4,6 для вывода запроса SFTMIME был добавлен новый столбец: приложение \ [/GLOBAL\].</span><span class="sxs-lookup"><span data-stu-id="f1fe9-129">**Note** In version 4.6, a new column has been added to the output of SFTMIME QUERY OBJ:APP \[/GLOBAL\].</span></span> <span data-ttu-id="f1fe9-130">Последний столбец выходных данных — это числовое значение, указывающее на то, опубликовано ли приложение.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-130">The last column of the output is a numeric value that indicates whether an application is published or not.</span></span>

<span data-ttu-id="f1fe9-131">ОПУБЛИКОВАНО = 1 означает, что приложение было опубликовано обновлением сервера публикаций, которое можно установить с помощью файла установщика Windows (. MSI) или, запустив SFTMIME ADD PACKAGE, настройте команду PACKAGE или PUBLISHing Package с помощью манифеста пакета.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-131">PUBLISHED=1 means the application was published by a Publishing Server refresh, by installing the application by using a Windows Installer file (.MSI), or by running an SFTMIME ADD PACKAGE, CONFIGURE PACKAGE or PUBLISH PACKAGE command by using a package manifest.</span></span>

<span data-ttu-id="f1fe9-132">ОПУБЛИКОВАНО = 0 означает, что приложение не было опубликовано или уже не Опубликовано в результате выполнения операции очистки или выполнения команды SFTMIME отменить публикацию.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-132">PUBLISHED=0 means the application has not been published or it is no longer published as a result of performing a Clear operation or running an SFTMIME UNPUBLISH command.</span></span>

<span data-ttu-id="f1fe9-133">Если вы используете параметр/GLOBAL, ОПУБЛИКОВАНное состояние будет равно 1 для приложений, которые были опубликованы глобально, а 0 для приложений, опубликованных в контекстах пользователя.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-133">If you use the /GLOBAL parameter, the PUBLISHED state will be 1 for applications that were published globally and 0 for those applications that were published under user contexts.</span></span> <span data-ttu-id="f1fe9-134">Если параметр/GLOBAL не задан, для приложений, опубликованных в контексте пользователя, выполняющего команду, возвращается состояние 1, а для тех приложений, которые публикуются глобально, возвращается состояние 0.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-134">Without the /GLOBAL parameter, a PUBLISHED state of 1 is returned for applications published in the context of the user running the command, and a state of 0 is returned for those applications that are published globally.</span></span>

 

<span data-ttu-id="f1fe9-135">С помощью команды SFTMIME QUERY можно запрашивать сведения обо всех указанных выше объектах — приложениях, пакетах, ассоциациях типов файлов и серверах.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-135">The SFTMIME QUERY OBJ command can be used to query for information on all of the objects shown above—applications, packages, file type associations, and servers.</span></span><span data-ttu-id="f1fe9-136">Чтобы показать, как можно использовать команду "SFTMIME QUERY" OBJ в обычных задачах операций, в следующем примере показан процесс, который следует выполнить, если вы хотели бы задать значение параметра OVERRIDEURL для определенного пакета, чтобы указать новый путь к содержимому пакета.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-136">To show how you might use the SFTMIME QUERY OBJ command in your normal operations tasks, the following example demonstrates the process you would follow if you wanted to set the OVERRIDEURL parameter value for a specific package to specify a new path to the package content.</span></span> 

1.  <span data-ttu-id="f1fe9-137">Чтобы найти пакет, который требуется настроить, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f1fe9-137">To find the package that you want to configure, run the following command:</span></span>

    `SFTMIME QUERY OBJ:PACKAGE`

    <span data-ttu-id="f1fe9-138">Эта команда возвращает каждое обнаруженное имя пакета как идентификатор GUID в первом столбце вывода (например, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}).</span><span class="sxs-lookup"><span data-stu-id="f1fe9-138">This command returns each discovered package name as a GUID in the first column of output—for example, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.</span></span>

2.  <span data-ttu-id="f1fe9-139">Чтобы задать значение параметра OVERRIDEURL, используйте команду " [настроить пакет](configure-package.md) " SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-139">To set the OVERRIDEURL parameter value, you use the SFTMIME [CONFIGURE PACKAGE](configure-package.md) command.</span></span> <span data-ttu-id="f1fe9-140">Например, чтобы задать для этого пакета значение *\\\\server\\share\\mypackage.SFT*, используйте команду SFTMIME configure Package и назначьте ей выделенный идентификатор GUID пакета из выходных данных команды SFTMIME Query на этапе 1, за которой следует параметр OVERRIDEURL и его новое значение, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-140">For example, to set the OVERRIDEURL value for this package to a value of *\\\\server\\share\\mypackage.sft*, use the SFTMIME CONFIGURE PACKAGE command and give it the selected package GUID from the output of the SFTMIME QUERY OBJ command in step 1, followed by the OVERRIDEURL parameter and its new value, as follows:</span></span>

    `SFTMIME CONFIGURE PACKAGE:"{AF78ABE1-57D4-4297-89DE-C308684AEDD6}" /OVERRIDEURL "\\\\server\\share\\mypackage.sft "`

<span data-ttu-id="f1fe9-141">Для версии 4.6 SP2 была добавлена следующая опция.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-141">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1fe9-142">/NO-UPDATE-FTA-SHORTCUT</span><span class="sxs-lookup"><span data-stu-id="f1fe9-142">/NO-UPDATE-FTA-SHORTCUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1fe9-143">Указывает текущее состояние флага/NO-UPDATE-FTA-SHORTCUT.</span><span class="sxs-lookup"><span data-stu-id="f1fe9-143">Indicates the current state of the /NO-UPDATE-FTA-SHORTCUT flag.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f1fe9-144">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f1fe9-144">Related topics</span></span>


[<span data-ttu-id="f1fe9-145">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="f1fe9-145">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





