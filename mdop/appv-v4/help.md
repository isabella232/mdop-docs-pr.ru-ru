---
title: HELP (СПРАВКА)
description: HELP (СПРАВКА)
author: dansimp
ms.assetid: 0ddb5f18-0c0a-45ea-b7c7-2d4749e3d35d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 395e6199529ccbe708aa7d1ac6673ea6f9494ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821462"
---
# <span data-ttu-id="bc113-103">HELP (СПРАВКА)</span><span class="sxs-lookup"><span data-stu-id="bc113-103">HELP</span></span>


<span data-ttu-id="bc113-104">Отображает сведения о различных командах SFTMIME, которые можно использовать в Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="bc113-104">Displays information about the various SFTMIME commands that can be used in Application Virtualization (App-V).</span></span>

## <span data-ttu-id="bc113-105">HELP (СПРАВКА)</span><span class="sxs-lookup"><span data-stu-id="bc113-105">HELP</span></span>


`SFTMIME [/? | /HELP [VERB:<verb>]]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc113-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="bc113-106">Parameter</span></span></th>
<th align="left"><span data-ttu-id="bc113-107">Описание</span><span class="sxs-lookup"><span data-stu-id="bc113-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc113-108">/?,/HELP</span><span class="sxs-lookup"><span data-stu-id="bc113-108">/?, /HELP</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-109">Выводит сведения об использовании.</span><span class="sxs-lookup"><span data-stu-id="bc113-109">Displays usage information.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc113-110">соответствующ</span><span class="sxs-lookup"><span data-stu-id="bc113-110">verb</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-111">Команда, которую необходимо выполнить, например "Добавить", "Обновить", "Справка" или "Удалить".</span><span class="sxs-lookup"><span data-stu-id="bc113-111">The command to run, such as ADD, REFRESH, HELP or REMOVE.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc113-112">объект</span><span class="sxs-lookup"><span data-stu-id="bc113-112">object</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-113">Назначение команды (например, &quot; приложение Application: по умолчанию).&quot;</span><span class="sxs-lookup"><span data-stu-id="bc113-113">What the command applies to, such as APP:&quot;Default Application.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc113-114">параметры</span><span class="sxs-lookup"><span data-stu-id="bc113-114">parameters</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-115">Необязательные параметры для заданных команды и объекта.</span><span class="sxs-lookup"><span data-stu-id="bc113-115">Optional parameters for the specified verb and object.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc113-116">/LOG</span><span class="sxs-lookup"><span data-stu-id="bc113-116">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-117">Вывод журнала на указанный путь.</span><span class="sxs-lookup"><span data-stu-id="bc113-117">Log output to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc113-118">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="bc113-118">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-119">Выводит результаты в активном окне консоли (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="bc113-119">Displays output in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc113-120">/GUI</span><span class="sxs-lookup"><span data-stu-id="bc113-120">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-121">Выводит ошибки в диалоговом окне (недопустимый для запросов).</span><span class="sxs-lookup"><span data-stu-id="bc113-121">Displays errors in a dialog box (not valid for queries).</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="bc113-122">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="bc113-122">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc113-123">/LOGU</span><span class="sxs-lookup"><span data-stu-id="bc113-123">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-124">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="bc113-124">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="bc113-125">Поддерживаются команды, описанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="bc113-125">The verbs described in the following table are supported.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc113-126">ADD</span><span class="sxs-lookup"><span data-stu-id="bc113-126">ADD</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-127">Добавляет новое приложение, пакет, сопоставление типов файлов или сервер публикаций в клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="bc113-127">Adds a new application, package, file type association, or publishing server to the App-V Client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc113-128">СТРОИЛ</span><span class="sxs-lookup"><span data-stu-id="bc113-128">CONFIGURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-129">Изменение конфигурации приложения, пакета, сопоставления типа файла или сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="bc113-129">Changes the configuration of an application, a package, a file type association, or a publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc113-130">DELETE</span><span class="sxs-lookup"><span data-stu-id="bc113-130">DELETE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-131">Удаляет приложения, пакеты, сопоставления типов файлов или серверы.</span><span class="sxs-lookup"><span data-stu-id="bc113-131">Removes applications, packages, file type associations, or servers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc113-132">ЗАГРУЗИТЬ</span><span class="sxs-lookup"><span data-stu-id="bc113-132">LOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-133">Загружает пакет в кэш файловой системы.</span><span class="sxs-lookup"><span data-stu-id="bc113-133">Loads a package into the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc113-134">ЧИНИТ</span><span class="sxs-lookup"><span data-stu-id="bc113-134">REPAIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-135">Сброс личных параметров для приложения.</span><span class="sxs-lookup"><span data-stu-id="bc113-135">Resets your personal settings for an application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc113-136">Обновлен</span><span class="sxs-lookup"><span data-stu-id="bc113-136">REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-137">Запускает обновление сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="bc113-137">Triggers a publishing server refresh.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc113-138">ПУБЛИКОВАТЬ</span><span class="sxs-lookup"><span data-stu-id="bc113-138">PUBLISH</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-139">Публикует ярлык приложения в меню "Пуск", рабочем столе или другом указанном месте, а также может использоваться для публикации контента всего пакета.</span><span class="sxs-lookup"><span data-stu-id="bc113-139">Publishes an application shortcut to the user's Start menu, desktop, or other specified location, or can be used to publish the contents of an entire package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc113-140">Отмена публикации</span><span class="sxs-lookup"><span data-stu-id="bc113-140">UNPUBLISH</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-141">Удаление ярлыков и типов файлов для всего пакета.</span><span class="sxs-lookup"><span data-stu-id="bc113-141">Removes the shortcuts and file types for an entire package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc113-142">ЗАПРОСА</span><span class="sxs-lookup"><span data-stu-id="bc113-142">QUERY</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-143">Получает текущий список приложений, пакетов, сопоставлений типов файлов или серверов публикаций.</span><span class="sxs-lookup"><span data-stu-id="bc113-143">Gets a current list of applications, packages, file type associations, or publishing servers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc113-144">Сброс</span><span class="sxs-lookup"><span data-stu-id="bc113-144">CLEAR</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-145">Удаление личных настроек и настольных конфигураций для одного или нескольких приложений.</span><span class="sxs-lookup"><span data-stu-id="bc113-145">Removes your personal settings and desktop configurations for one or more applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc113-146">ГРУЖАТЬ</span><span class="sxs-lookup"><span data-stu-id="bc113-146">UNLOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-147">Выгрузка пакета из кэша файловой системы.</span><span class="sxs-lookup"><span data-stu-id="bc113-147">Unloads a package from the file system cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc113-148">БЛОКИРОВКИ</span><span class="sxs-lookup"><span data-stu-id="bc113-148">LOCK</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-149">Блокирует приложение, указанное в кэше файловой системы.</span><span class="sxs-lookup"><span data-stu-id="bc113-149">Locks the application specified in the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc113-150">Креп</span><span class="sxs-lookup"><span data-stu-id="bc113-150">UNLOCK</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc113-151">Разблокирует приложение, указанное в кэше файловой системы.</span><span class="sxs-lookup"><span data-stu-id="bc113-151">Unlocks the application specified in the file system cache.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="bc113-152">Для получения дополнительных сведений об описанных выше действиях используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bc113-152">For more information about the preceding actions, use the following command:</span></span>

`SFTMIME /HELP VERB:verb`

<span data-ttu-id="bc113-153">Например, следующая команда выведет сведения о команде ADD:</span><span class="sxs-lookup"><span data-stu-id="bc113-153">For example, the following command will display information for the ADD verb:</span></span>

`SFTMIME /HELP VERB:ADD`

## <span data-ttu-id="bc113-154">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="bc113-154">Related topics</span></span>


[<span data-ttu-id="bc113-155">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="bc113-155">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





