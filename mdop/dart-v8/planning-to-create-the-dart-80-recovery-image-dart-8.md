---
title: Планирование создания образа для восстановления DaRT 8.0
description: Планирование создания образа для восстановления DaRT 8.0
author: dansimp
ms.assetid: cfd0e1e2-c379-4460-b545-3f7be9f33583
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1d1dc7dc5b3776638523a282d9216b80d4ce9ce1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824809"
---
# <span data-ttu-id="42b65-103">Планирование создания образа для восстановления DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="42b65-103">Planning to Create the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="42b65-104">При планировании создания образа восстановления для набора средств диагностики и восстановления Microsoft (DaRT) 8,0 вы можете использовать сведения из этого раздела.</span><span class="sxs-lookup"><span data-stu-id="42b65-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image.</span></span>

## <span data-ttu-id="42b65-105">Планирование создания образа для восстановления DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="42b65-105">Planning to create the DaRT 8.0 recovery image</span></span>


<span data-ttu-id="42b65-106">При создании изображения для восстановления DaRT необходимо решить, какие инструменты следует включить в изображение.</span><span class="sxs-lookup"><span data-stu-id="42b65-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="42b65-107">Чтобы принять решение, учитывайте, что конечные пользователи могут получить доступ к этим средствам.</span><span class="sxs-lookup"><span data-stu-id="42b65-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="42b65-108">Если инженеры службы поддержки будут использовать носители образа для восстановления на компьютерах конечных пользователей для диагностики проблем, возможно, потребуется установить все средства на образе восстановления.</span><span class="sxs-lookup"><span data-stu-id="42b65-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="42b65-109">Если вы планируете выявлять компьютеры конечных пользователей удаленно, вам может потребоваться отключить некоторые инструменты, такие как очистка диска и редактор реестра, а также включить другие инструменты, в том числе удаленное подключение.</span><span class="sxs-lookup"><span data-stu-id="42b65-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="42b65-110">При создании изображения для восстановления DaRT вы также можете указать, нужно ли включать дополнительные драйверы или файлы.</span><span class="sxs-lookup"><span data-stu-id="42b65-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="42b65-111">Определите расположение дополнительных драйверов или файлов, которые вы хотите включить в изображение для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="42b65-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="42b65-112">Дополнительные сведения о средствах DaRT можно найти в статье [Обзор средств на dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="42b65-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span> <span data-ttu-id="42b65-113">Дополнительные сведения о том, как создать защищенный образ восстановления, приведены в разделе [рекомендации по обеспечению безопасности для DaRT 8,0](security-considerations-for-dart-80--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="42b65-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 8.0](security-considerations-for-dart-80--dart-8.md).</span></span>

## <span data-ttu-id="42b65-114">Предварительные условия для образа восстановления</span><span class="sxs-lookup"><span data-stu-id="42b65-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="42b65-115">Следующие элементы являются обязательными или рекомендуемыми для создания изображения для восстановления DaRT:</span><span class="sxs-lookup"><span data-stu-id="42b65-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="42b65-116">Предварительные</span><span class="sxs-lookup"><span data-stu-id="42b65-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="42b65-117">Сведения</span><span class="sxs-lookup"><span data-stu-id="42b65-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42b65-118">Исходные файлы Windows 8</span><span class="sxs-lookup"><span data-stu-id="42b65-118">Windows 8 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="42b65-119">Требуется для создания изображения для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="42b65-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="42b65-120">Укажите путь к DVD-диску Windows 8 или исходным файлам Windows 8.</span><span class="sxs-lookup"><span data-stu-id="42b65-120">Provide the path of a Windows 8 DVD or of Windows 8 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42b65-121">Средства отладки Windows для платформы</span><span class="sxs-lookup"><span data-stu-id="42b65-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="42b65-122">Требуется при запуске <strong> анализатора сбоев </strong> для определения причины сбоя компьютера.</span><span class="sxs-lookup"><span data-stu-id="42b65-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="42b65-123">Мы рекомендуем указать путь к средствам отладки Windows на момент создания изображения для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="42b65-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="42b65-124">Вы можете скачать инструменты для отладки Windows здесь: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)"> скачивание и установка средств отладки для Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="42b65-124">You can download the Windows Debugging Tools here: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42b65-125">Необязательно <strong> : </strong> определения защитника</span><span class="sxs-lookup"><span data-stu-id="42b65-125">Optional: <strong>Defender</strong> definitions</span></span></p></td>
<td align="left"><p><span data-ttu-id="42b65-126"><strong> </strong> При запуске защитника требуются последние определения для защитника <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="42b65-126">The latest definitions for <strong>Defender</strong> are required when you run <strong>Defender</strong>.</span></span> <span data-ttu-id="42b65-127">Несмотря на то, что вы можете скачать определения при запуске <strong> защитника </strong> , мы рекомендуем вам загрузить последние определения на момент создания образа для восстановления DaRT, чтобы можно было запустить средство с самыми последними определениями, даже если на компьютере с неполадкой не установлено сетевое подключение.</span><span class="sxs-lookup"><span data-stu-id="42b65-127">Although you can download the definitions when you run <strong>Defender</strong>, we recommend that you download the latest definitions at the time you create the DaRT recovery image so that you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42b65-128">Необязательно: файлы символов Windows для работы с <strong> анализатором аварийного восстановления</span><span class="sxs-lookup"><span data-stu-id="42b65-128">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="42b65-129">Обычно отладочная информация хранится в файле символов, отдельном от программы.</span><span class="sxs-lookup"><span data-stu-id="42b65-129">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="42b65-130">При отладке приложения, которое перестало отвечать (например, если оно перестало работать), необходимо иметь доступ к сведениям о символах.</span><span class="sxs-lookup"><span data-stu-id="42b65-130">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="42b65-131">Дополнительные сведения можно найти <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)"> в разделе Диагностика сбоев системы с помощью анализатора сбоев </a> .</span><span class="sxs-lookup"><span data-stu-id="42b65-131">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="42b65-132">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="42b65-132">Related topics</span></span>


[<span data-ttu-id="42b65-133">Планирование развертывания DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="42b65-133">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





