---
title: PUBLISH APP (ОПУБЛИКОВАТЬ ПРИЛОЖЕНИЕ)
description: PUBLISH APP (ОПУБЛИКОВАТЬ ПРИЛОЖЕНИЕ)
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815819"
---
# <span data-ttu-id="d35e5-103">PUBLISH APP (ОПУБЛИКОВАТЬ ПРИЛОЖЕНИЕ)</span><span class="sxs-lookup"><span data-stu-id="d35e5-103">PUBLISH APP</span></span>


<span data-ttu-id="d35e5-104">Публикация ярлыка приложения в меню "Пуск", рабочем столе или другом указанном месте.</span><span class="sxs-lookup"><span data-stu-id="d35e5-104">Publishes an application shortcut to the user's Start menu, desktop, or other specified location.</span></span>

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d35e5-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="d35e5-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="d35e5-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d35e5-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d35e5-107">Приложение: &lt; приложение&gt;</span><span class="sxs-lookup"><span data-stu-id="d35e5-107">APPLICATION:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d35e5-108">Имя и версия (необязательно) приложения.</span><span class="sxs-lookup"><span data-stu-id="d35e5-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d35e5-109">/DESKTOP</span><span class="sxs-lookup"><span data-stu-id="d35e5-109">/DESKTOP</span></span></p></td>
<td align="left"><p><span data-ttu-id="d35e5-110">Публикация ярлыка на рабочем столе пользователя.</span><span class="sxs-lookup"><span data-stu-id="d35e5-110">Publishes a shortcut to the user's desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d35e5-111">/START</span><span class="sxs-lookup"><span data-stu-id="d35e5-111">/START</span></span></p></td>
<td align="left"><p><span data-ttu-id="d35e5-112">Публикация ярлыка в папке приложения Application Virtualization в папке программы в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="d35e5-112">Publishes a shortcut to the Application Virtualization Applications folder in the Programs folder of the Start menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d35e5-113">/TARGET &lt; Target-Path&gt;</span><span class="sxs-lookup"><span data-stu-id="d35e5-113">/TARGET &lt;target-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d35e5-114">Абсолютный путь к папке, в которой нужно опубликовать ярлык.</span><span class="sxs-lookup"><span data-stu-id="d35e5-114">The absolute path where the shortcut should be published.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d35e5-115">/ICON &lt; Icon (путь)&gt;</span><span class="sxs-lookup"><span data-stu-id="d35e5-115">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d35e5-116">Путь или URL-адрес файла значка.</span><span class="sxs-lookup"><span data-stu-id="d35e5-116">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d35e5-117">&lt;Отображаемое имя/Display&gt;</span><span class="sxs-lookup"><span data-stu-id="d35e5-117">/DISPLAY &lt;display-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d35e5-118">Отображаемое имя ярлыка.</span><span class="sxs-lookup"><span data-stu-id="d35e5-118">The display name for the shortcut.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d35e5-119">/ARGS &lt; Command-args&gt;</span><span class="sxs-lookup"><span data-stu-id="d35e5-119">/ARGS &lt;command-args&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d35e5-120">Параметры, передаваемые приложению.</span><span class="sxs-lookup"><span data-stu-id="d35e5-120">Parameters to be passed to the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d35e5-121">/LOG</span><span class="sxs-lookup"><span data-stu-id="d35e5-121">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="d35e5-122">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="d35e5-122">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d35e5-123">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="d35e5-123">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="d35e5-124">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="d35e5-124">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d35e5-125">/GUI</span><span class="sxs-lookup"><span data-stu-id="d35e5-125">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="d35e5-126">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="d35e5-126">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d35e5-127">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="d35e5-127">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d35e5-128">/LOGU</span><span class="sxs-lookup"><span data-stu-id="d35e5-128">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="d35e5-129">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="d35e5-129">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d35e5-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d35e5-130">Related topics</span></span>


[<span data-ttu-id="d35e5-131">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="d35e5-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





