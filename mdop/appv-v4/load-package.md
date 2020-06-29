---
title: LOAD PACKAGE (ЗАГРУЗИТЬ ПАКЕТ)
description: LOAD PACKAGE (ЗАГРУЗИТЬ ПАКЕТ)
author: dansimp
ms.assetid: eb19116d-e5d0-445c-b2f0-3116a09384d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 938aa92696c8530c91d9a7acaac42408de534edc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816239"
---
# <span data-ttu-id="84ba3-103">LOAD PACKAGE (ЗАГРУЗИТЬ ПАКЕТ)</span><span class="sxs-lookup"><span data-stu-id="84ba3-103">LOAD PACKAGE</span></span>


<span data-ttu-id="84ba3-104">Загружает заданный пакет в кэш файловой системы.</span><span class="sxs-lookup"><span data-stu-id="84ba3-104">Loads the specified package into the file system cache.</span></span>

`SFTMIME LOAD PACKAGE:package-name [/SFTPATH sft-pathname]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84ba3-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="84ba3-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="84ba3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="84ba3-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84ba3-107">Пакет: &lt; имя пакета&gt;</span><span class="sxs-lookup"><span data-stu-id="84ba3-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="84ba3-108">Имя загружаемого пакета.</span><span class="sxs-lookup"><span data-stu-id="84ba3-108">The name of the package to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84ba3-109">/SFTPATH &lt; SFT — PathName&gt;</span><span class="sxs-lookup"><span data-stu-id="84ba3-109">/SFTPATH &lt;sft-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="84ba3-110">Указывает путь к SFT – файлу для загрузки.</span><span class="sxs-lookup"><span data-stu-id="84ba3-110">If specified, the path to an SFT file to load from.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84ba3-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="84ba3-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="84ba3-112">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="84ba3-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84ba3-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="84ba3-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="84ba3-114">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="84ba3-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84ba3-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="84ba3-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="84ba3-116">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="84ba3-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="84ba3-117">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="84ba3-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84ba3-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="84ba3-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="84ba3-119">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="84ba3-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="84ba3-120">**Примечание**  Если не указано ни одного SFTPATH, клиент загрузит пакет, используя путь, который он использует, на основании файла OSD, значения раздела реестра ApplicationSourceRoot или параметра OverrideURL.</span><span class="sxs-lookup"><span data-stu-id="84ba3-120">**Note** If no SFTPATH is specified, the client will load the package by using the path it has been configured to use, based on the OSD file, the ApplicationSourceRoot registry key value, or the OverrideURL setting.</span></span>

<span data-ttu-id="84ba3-121">Команда **загрузить пакет** выполняет синхронную загрузку и не будет завершена до полной загрузки пакета или до тех пор, пока не встретится условие ошибки.</span><span class="sxs-lookup"><span data-stu-id="84ba3-121">The **LOAD PACKAGE** command performs a synchronous load and will not be complete until the package is fully loaded or until it encounters an error condition.</span></span>

 

## <span data-ttu-id="84ba3-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="84ba3-122">Related topics</span></span>


[<span data-ttu-id="84ba3-123">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="84ba3-123">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





