---
title: PUBLISH PACKAGE (ОПУБЛИКОВАТЬ ПАКЕТ)
description: PUBLISH PACKAGE (ОПУБЛИКОВАТЬ ПАКЕТ)
author: dansimp
ms.assetid: a33e72dd-194f-4283-8e99-4584ab13de53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00b63389986f495d9405939245a50575bae453f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815812"
---
# <span data-ttu-id="7515d-103">PUBLISH PACKAGE (ОПУБЛИКОВАТЬ ПАКЕТ)</span><span class="sxs-lookup"><span data-stu-id="7515d-103">PUBLISH PACKAGE</span></span>


<span data-ttu-id="7515d-104">Публикует содержимое всего пакета.</span><span class="sxs-lookup"><span data-stu-id="7515d-104">Publishes the contents of an entire package.</span></span>

`SFTMIME PUBLISH PACKAGE:package-name /MANIFEST manifest-path [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7515d-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="7515d-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="7515d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7515d-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7515d-107">Пакет: &lt; имя пакета&gt;</span><span class="sxs-lookup"><span data-stu-id="7515d-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="7515d-108">Имя пакета, отображаемое пользователем, и понятное.</span><span class="sxs-lookup"><span data-stu-id="7515d-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7515d-109">&lt;Путь манифеста/manifest&gt;</span><span class="sxs-lookup"><span data-stu-id="7515d-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="7515d-110">Путь или URL-адрес файла манифеста, в котором перечислены приложения, включенные в пакет, и все сведения о его публикации.</span><span class="sxs-lookup"><span data-stu-id="7515d-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7515d-111">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="7515d-111">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="7515d-112">Если он указан, пакет будет доступен для всех пользователей на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="7515d-112">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7515d-113">/LOG</span><span class="sxs-lookup"><span data-stu-id="7515d-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="7515d-114">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="7515d-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7515d-115">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="7515d-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="7515d-116">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="7515d-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7515d-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="7515d-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="7515d-118">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="7515d-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7515d-119">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="7515d-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7515d-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="7515d-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="7515d-121">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="7515d-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7515d-122">**Важно!**  Пакет уже должен быть добавлен в клиент виртуализации приложений, а требуется файл манифеста.</span><span class="sxs-lookup"><span data-stu-id="7515d-122">**Important** The package must already have been added to the Application Virtualization Client, and the manifest file is required.</span></span>

<span data-ttu-id="7515d-123">Чтобы использовать **глобальный** параметр, команда "опубликовать пакет" должна быть запущена как локальный администратор; в противном случае требуются только разрешения **ManageTypes** и **PublishShortcut** .</span><span class="sxs-lookup"><span data-stu-id="7515d-123">To use the **GLOBAL** parameter, the PUBLISH PACKAGE command must be run as local Administrator; otherwise, only **ManageTypes** and **PublishShortcut** permissions are needed.</span></span>

<span data-ttu-id="7515d-124">Публикация без **глобального** параметра предоставляет пользователю доступ к приложениям в пакете и публикует типы файлов и ярлыки, указанные в манифесте, в профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="7515d-124">Publishing without the **GLOBAL** parameter grants the user access to the applications in the package and publishes the file types and shortcuts listed in the manifest to the user’s profile.</span></span>

<span data-ttu-id="7515d-125">Публикация с **глобальным** параметром добавляет типы файлов и ярлыки, указанные в манифесте, в профиль "все пользователи".</span><span class="sxs-lookup"><span data-stu-id="7515d-125">Publishing with the **GLOBAL** parameter adds the file types and shortcuts listed in the manifest to the “All Users” profile.</span></span>

<span data-ttu-id="7515d-126">Если пакет не является глобальным перед вызовом и используется **глобальный** параметр, пакет становится глобальным и доступен всем пользователям.</span><span class="sxs-lookup"><span data-stu-id="7515d-126">If the package is not global before the call and the **GLOBAL** parameter is used, the package is made global and available to all users.</span></span>

 

## <span data-ttu-id="7515d-127">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7515d-127">Related topics</span></span>


[<span data-ttu-id="7515d-128">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="7515d-128">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





