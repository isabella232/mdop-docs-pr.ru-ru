---
title: CONFIGURE PACKAGE (НАСТРОИТЬ ПАКЕТ)
description: CONFIGURE PACKAGE (НАСТРОИТЬ ПАКЕТ)
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819349"
---
# <span data-ttu-id="8fcc1-103">CONFIGURE PACKAGE (НАСТРОИТЬ ПАКЕТ)</span><span class="sxs-lookup"><span data-stu-id="8fcc1-103">CONFIGURE PACKAGE</span></span>


<span data-ttu-id="8fcc1-104">Позволяет пользователю изменить файл манифеста пакета, источник пакетов, типы триггеров загрузки или целевой объект загрузки для пакета.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-104">Enables the user to change a package manifest file, package source, load trigger types, or load target for a package.</span></span>

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8fcc1-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="8fcc1-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="8fcc1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8fcc1-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fcc1-107">Пакет: &lt; имя пакета&gt;</span><span class="sxs-lookup"><span data-stu-id="8fcc1-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-108">Имя пакета, отображаемое пользователем, и понятное.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8fcc1-109">&lt;Путь манифеста/manifest&gt;</span><span class="sxs-lookup"><span data-stu-id="8fcc1-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-110">Путь или URL-адрес файла манифеста, в котором перечислены приложения, включенные в пакет, и все сведения о его публикации.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fcc1-111">&lt;URL-адрес/OVERRIDEURL&gt;</span><span class="sxs-lookup"><span data-stu-id="8fcc1-111">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-112">Расположение SFT-файла пакета.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-112">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8fcc1-113">/AUTOLOADNEVER</span><span class="sxs-lookup"><span data-stu-id="8fcc1-113">/AUTOLOADNEVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-114">Фоновая загрузка выключена для пакета.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-114">Background loading is turned off for the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fcc1-115">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="8fcc1-115">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-116">Фоновая загрузка выполняется после обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-116">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8fcc1-117">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="8fcc1-117">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-118">Фоновая загрузка выполняется, когда пользователь входит в систему.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-118">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fcc1-119">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="8fcc1-119">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-120">Фоновая загрузка выполняется после того, как пользователь запустит приложение из пакета.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-120">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8fcc1-121">&lt;Целевой объект/AUTOLOADTARGET&gt;</span><span class="sxs-lookup"><span data-stu-id="8fcc1-121">/AUTOLOADTARGET &lt;target&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-122">Указывает, какие приложения из пакета будут выгружены.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-122">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fcc1-123">НИЧЕГО</span><span class="sxs-lookup"><span data-stu-id="8fcc1-123">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-124">Ни один из автонагрузок не будет выполнен, несмотря на наличие флагов/AUTOLOADONxxx.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-124">No autoloading will be performed despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8fcc1-125">ВЕСЬ</span><span class="sxs-lookup"><span data-stu-id="8fcc1-125">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-126">Если включен триггер autoload, все приложения в пакете будут загружены в кэш независимо от того, были ли они запущены.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-126">If an autoload trigger is enabled, all applications in the package will be loaded into cache regardless of whether they have ever been launched.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fcc1-127">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="8fcc1-127">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-128">Если включен триггер autoload, пакет будет загружаться, если какое-либо приложение ранее было запущено пользователем.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-128">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8fcc1-129">/LOG</span><span class="sxs-lookup"><span data-stu-id="8fcc1-129">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-130">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-130">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fcc1-131">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="8fcc1-131">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-132">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="8fcc1-132">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8fcc1-133">/GUI</span><span class="sxs-lookup"><span data-stu-id="8fcc1-133">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-134">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="8fcc1-134">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8fcc1-135">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-135">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fcc1-136">/LOGU</span><span class="sxs-lookup"><span data-stu-id="8fcc1-136">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-137">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-137">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8fcc1-138">Для версии 4.6 SP2 была добавлена следующая опция.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-138">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fcc1-139">[/NO-UPDATE-FTA-SHORTCUT {TRUE | FALSE} {/GLOBAL}]</span><span class="sxs-lookup"><span data-stu-id="8fcc1-139">[/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-140">Если задано значение "TRUE", для пакета создается параметр для одного пользователя или глобально, если указан флаг/GLOBAL.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-140">If set to TRUE, a registry value is created for the package, either per user, or globally if the /GLOBAL flag is specified.</span></span></p>
<p><span data-ttu-id="8fcc1-141">Если для параметра установлено значение FALSE, значение реестра удаляется, а также переустанавливаются сопоставления типов файлов (FTA) для пакета.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-141">If set to FALSE, the registry value is removed and the file type associations (FTA) for the package are reinstalled.</span></span></p>
<p><span data-ttu-id="8fcc1-142">Если не указано, происходит обычное поведение публикации по FTA и сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-142">If not specified, normal FTA and shortcut publishing behavior occurs.</span></span> <span data-ttu-id="8fcc1-143">Если вы выполняете последующие операции обновления публикации в клиенте App-V 4,6 SP2, сочетания клавиш и FTAs для пакетов, для которых задан этот параметр реестра, не будут изменены, а сочетания клавиш и FTAs не будут регистрироваться при запуске системы или входе пользователя в систему, если не установить флажок.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-143">If you perform any subsequent publishing refresh operations on the App-V 4.6 SP2 client, the shortcuts and FTAs for packages that have this registry value set will not be changed, and the shortcuts and FTAs will not be registered at system startup or user login unless you reset the flag.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8fcc1-144">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="8fcc1-144">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fcc1-145">Работает совместно с флагом/NO-UPDATE-FTA-SHORTCUT.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-145">Works in conjunction with the /NO-UPDATE-FTA-SHORTCUT flag.</span></span> <span data-ttu-id="8fcc1-146">Если присутствует флаг/GLOBAL, это означает, что для этого пакета будет создано значение реестра для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-146">If the /GLOBAL flag is present, it indicates that a registry value will be created for that package for all users.</span></span> <span data-ttu-id="8fcc1-147">По умолчанию значение реестра создается только для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-147">By default, the registry value is created only for this user.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8fcc1-148">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8fcc1-148">Related topics</span></span>


[<span data-ttu-id="8fcc1-149">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="8fcc1-149">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





