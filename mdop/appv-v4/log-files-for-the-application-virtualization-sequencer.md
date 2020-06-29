---
title: Файлы журнала программы Application Virtualization Sequencer
description: Файлы журнала программы Application Virtualization Sequencer
author: dansimp
ms.assetid: 1a296544-eab4-46f9-82ce-3136f8b578af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8cdf9dbc78ccdd03df5903ef4d42990099a2c53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816219"
---
# <span data-ttu-id="c61c3-103">Файлы журнала программы Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="c61c3-103">Log Files for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="c61c3-104">Файлы журнала для секвенсора Application Virtualization (App-V) содержат подробные сведения о последовательности приложений, и они могут быть полезны при проверке функциональности или при устранении проблем.</span><span class="sxs-lookup"><span data-stu-id="c61c3-104">The log files for the Application Virtualization (App-V) Sequencer provide detailed information about sequencing applications, and they can be helpful when you are verifying functionality or when you are troubleshooting issues.</span></span>

<span data-ttu-id="c61c3-105">В таблице ниже приведены сведения о файлах журнала и их расположениях по умолчанию, которые создаются при использовании секвенсора.</span><span class="sxs-lookup"><span data-stu-id="c61c3-105">The following table provides information about the log files and their default locations, which are created when using the Sequencer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c61c3-106">Имя файла журнала</span><span class="sxs-lookup"><span data-stu-id="c61c3-106">Log File Name</span></span></th>
<th align="left"><span data-ttu-id="c61c3-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c61c3-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c61c3-108">sft-seq-log.txt</span><span class="sxs-lookup"><span data-stu-id="c61c3-108">sft-seq-log.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c61c3-109">Общие сведения о том, как поочередно приложит приложение.</span><span class="sxs-lookup"><span data-stu-id="c61c3-109">Provides general information about sequencing an application.</span></span> <span data-ttu-id="c61c3-110">Используйте этот журнал в качестве отправной точки для устранения ошибок программы Sequencer.</span><span class="sxs-lookup"><span data-stu-id="c61c3-110">Use this log as a starting point for troubleshooting Sequencer errors.</span></span></p>
<p><span data-ttu-id="c61c3-111">Расположение файла журнала: <em> %WINDIR%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="c61c3-111">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="c61c3-112">[Значение маркера шаблона] Расположение файла журнала App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [значение маркера шаблона]</span><span class="sxs-lookup"><span data-stu-id="c61c3-112">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c61c3-113">sftbt.txt</span><span class="sxs-lookup"><span data-stu-id="c61c3-113">sftbt.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c61c3-114">Содержит сведения о задачах перезапуска компьютера, происходящих во время имитации перезапуска секвенсора.</span><span class="sxs-lookup"><span data-stu-id="c61c3-114">Provides information about computer restart tasks that occur during the Sequencer’s simulated restart.</span></span></p>
<p><span data-ttu-id="c61c3-115">Расположение файла журнала: <em> %WINDIR%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="c61c3-115">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="c61c3-116">[Значение маркера шаблона] Расположение файла журнала App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [значение маркера шаблона]</span><span class="sxs-lookup"><span data-stu-id="c61c3-116">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c61c3-117">SftCallBack.txt</span><span class="sxs-lookup"><span data-stu-id="c61c3-117">SftCallBack.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c61c3-118">Общие сведения о процессах, используемых при упорядочении.</span><span class="sxs-lookup"><span data-stu-id="c61c3-118">Provides general information about processes used during sequencing.</span></span></p>
<p><span data-ttu-id="c61c3-119">Расположение файла журнала: <em> %WINDIR%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="c61c3-119">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="c61c3-120">[Значение маркера шаблона] Расположение файла журнала App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [значение маркера шаблона]</span><span class="sxs-lookup"><span data-stu-id="c61c3-120">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c61c3-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c61c3-121">Related topics</span></span>


[<span data-ttu-id="c61c3-122">Справка по программе Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="c61c3-122">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

 

 





