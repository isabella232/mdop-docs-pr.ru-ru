---
title: ADD PACKAGE (ДОБАВИТЬ ПАКЕТ)
description: ADD PACKAGE (ДОБАВИТЬ ПАКЕТ)
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822399"
---
# <span data-ttu-id="ba67f-103">ADD PACKAGE (ДОБАВИТЬ ПАКЕТ)</span><span class="sxs-lookup"><span data-stu-id="ba67f-103">ADD PACKAGE</span></span>


<span data-ttu-id="ba67f-104">Добавляет запись пакета.</span><span class="sxs-lookup"><span data-stu-id="ba67f-104">Adds a package record.</span></span> <span data-ttu-id="ba67f-105">Если пакет уже существует, эта команда обновит конфигурацию существующего пакета.</span><span class="sxs-lookup"><span data-stu-id="ba67f-105">If the package already exists, this command will update the configuration of the existing package.</span></span>

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ba67f-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="ba67f-106">Parameter</span></span></th>
<th align="left"><span data-ttu-id="ba67f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ba67f-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba67f-108">Пакет: &lt; имя пакета&gt;</span><span class="sxs-lookup"><span data-stu-id="ba67f-108">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-109">Имя пакета, отображаемое пользователем, и понятное.</span><span class="sxs-lookup"><span data-stu-id="ba67f-109">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba67f-110">&lt;Путь манифеста/manifest&gt;</span><span class="sxs-lookup"><span data-stu-id="ba67f-110">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-111">Путь к файлу манифеста, в котором перечислены приложения, включенные в пакет, и все сведения о его публикации.</span><span class="sxs-lookup"><span data-stu-id="ba67f-111">The path of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba67f-112">&lt;URL-адрес/OVERRIDEURL&gt;</span><span class="sxs-lookup"><span data-stu-id="ba67f-112">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-113">Расположение SFT-файла пакета.</span><span class="sxs-lookup"><span data-stu-id="ba67f-113">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba67f-114">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="ba67f-114">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-115">Фоновая загрузка выполняется после обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="ba67f-115">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba67f-116">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="ba67f-116">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-117">Фоновая загрузка выполняется, когда пользователь входит в систему.</span><span class="sxs-lookup"><span data-stu-id="ba67f-117">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba67f-118">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="ba67f-118">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-119">Фоновая загрузка выполняется после того, как пользователь запустит приложение из пакета.</span><span class="sxs-lookup"><span data-stu-id="ba67f-119">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba67f-120">Целевой объект/AUTOLOADTARGET</span><span class="sxs-lookup"><span data-stu-id="ba67f-120">/AUTOLOADTARGET target</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-121">Указывает, какие приложения из пакета будут выгружены.</span><span class="sxs-lookup"><span data-stu-id="ba67f-121">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba67f-122">НИЧЕГО</span><span class="sxs-lookup"><span data-stu-id="ba67f-122">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-123">Автозагрузка не будет выполнена, несмотря на наличие флагов/AUTOLOADONxxx.</span><span class="sxs-lookup"><span data-stu-id="ba67f-123">No autoloading will be performed, despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba67f-124">ВЕСЬ</span><span class="sxs-lookup"><span data-stu-id="ba67f-124">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-125">Если включен триггер autoload, все приложения в пакете будут загружены в кэш независимо от того, были ли они запущены ранее.</span><span class="sxs-lookup"><span data-stu-id="ba67f-125">If an autoload trigger is enabled, all applications in the package will be loaded into cache whether or not they have been previously started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba67f-126">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="ba67f-126">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-127">Если включен триггер autoload, пакет будет загружаться, если какое-либо приложение ранее было запущено пользователем.</span><span class="sxs-lookup"><span data-stu-id="ba67f-127">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba67f-128">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="ba67f-128">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-129">Если он указан, пакет будет доступен для всех пользователей на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="ba67f-129">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba67f-130">/LOG</span><span class="sxs-lookup"><span data-stu-id="ba67f-130">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-131">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="ba67f-131">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba67f-132">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="ba67f-132">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-133">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ba67f-133">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba67f-134">/GUI</span><span class="sxs-lookup"><span data-stu-id="ba67f-134">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-135">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="ba67f-135">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ba67f-136">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="ba67f-136">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba67f-137">/LOGU</span><span class="sxs-lookup"><span data-stu-id="ba67f-137">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba67f-138">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="ba67f-138">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ba67f-139">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ba67f-139">Related topics</span></span>


[<span data-ttu-id="ba67f-140">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="ba67f-140">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





