---
title: Планирование создания образа для восстановления DaRT 10
description: Планирование создания образа для восстановления DaRT 10
author: dansimp
ms.assetid: a0087d93-b88f-454b-81b2-3c7ce3718023
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 44cf052eaffd19645885618da9104e5b0a50cfd5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822979"
---
# <span data-ttu-id="702a9-103">Планирование создания образа для восстановления DaRT 10</span><span class="sxs-lookup"><span data-stu-id="702a9-103">Planning to Create the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="702a9-104">При планировании создания образа восстановления с помощью набора средств диагностики и восстановления Microsoft (DaRT)</span><span class="sxs-lookup"><span data-stu-id="702a9-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image.</span></span>

## <span data-ttu-id="702a9-105">Планирование создания образа для восстановления DaRT 10</span><span class="sxs-lookup"><span data-stu-id="702a9-105">Planning to create the DaRT 10 recovery image</span></span>


<span data-ttu-id="702a9-106">При создании изображения для восстановления DaRT необходимо решить, какие инструменты следует включить в изображение.</span><span class="sxs-lookup"><span data-stu-id="702a9-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="702a9-107">Чтобы принять решение, учитывайте, что конечные пользователи могут получить доступ к этим средствам.</span><span class="sxs-lookup"><span data-stu-id="702a9-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="702a9-108">Если инженеры службы поддержки будут использовать носители образа для восстановления на компьютерах конечных пользователей для диагностики проблем, возможно, потребуется установить все средства на образе восстановления.</span><span class="sxs-lookup"><span data-stu-id="702a9-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="702a9-109">Если вы планируете выявлять компьютеры конечных пользователей удаленно, вам может потребоваться отключить некоторые инструменты, такие как очистка диска и редактор реестра, а также включить другие инструменты, в том числе удаленное подключение.</span><span class="sxs-lookup"><span data-stu-id="702a9-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="702a9-110">При создании изображения для восстановления DaRT вы также можете указать, нужно ли включать дополнительные драйверы или файлы.</span><span class="sxs-lookup"><span data-stu-id="702a9-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="702a9-111">Определите расположение дополнительных драйверов или файлов, которые вы хотите включить в изображение для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="702a9-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="702a9-112">Дополнительные сведения о средствах DaRT можно найти в статье [Обзор средств на DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="702a9-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span> <span data-ttu-id="702a9-113">Дополнительные сведения о том, как создать защищенный образ восстановления, приведены в разделе [рекомендации по безопасности для DART 10](security-considerations-for-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="702a9-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 10](security-considerations-for-dart-10.md).</span></span>

## <span data-ttu-id="702a9-114">Предварительные условия для образа восстановления</span><span class="sxs-lookup"><span data-stu-id="702a9-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="702a9-115">Следующие элементы являются обязательными или рекомендуемыми для создания изображения для восстановления DaRT:</span><span class="sxs-lookup"><span data-stu-id="702a9-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="702a9-116">Предварительные</span><span class="sxs-lookup"><span data-stu-id="702a9-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="702a9-117">Сведения</span><span class="sxs-lookup"><span data-stu-id="702a9-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="702a9-118">Исходные файлы Windows 10</span><span class="sxs-lookup"><span data-stu-id="702a9-118">Windows 10 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="702a9-119">Требуется для создания изображения для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="702a9-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="702a9-120">Укажите путь к DVD-диску Windows 10 или исходным файлам Windows 10.</span><span class="sxs-lookup"><span data-stu-id="702a9-120">Provide the path of a Windows 10 DVD or of Windows 10 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="702a9-121">Средства отладки Windows для платформы</span><span class="sxs-lookup"><span data-stu-id="702a9-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="702a9-122">Требуется при запуске <strong> анализатора сбоев </strong> для определения причины сбоя компьютера.</span><span class="sxs-lookup"><span data-stu-id="702a9-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="702a9-123">Мы рекомендуем указать путь к средствам отладки Windows на момент создания изображения для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="702a9-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="702a9-124">Вы можете скачать инструменты для отладки Windows здесь: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)"> скачивание и установка средств отладки для Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="702a9-124">You can download the Windows Debugging Tools here: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="702a9-125">Необязательно: файлы символов Windows для работы с <strong> анализатором аварийного восстановления</span><span class="sxs-lookup"><span data-stu-id="702a9-125">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="702a9-126">Обычно отладочная информация хранится в файле символов, отдельном от программы.</span><span class="sxs-lookup"><span data-stu-id="702a9-126">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="702a9-127">При отладке приложения, которое перестало отвечать (например, если оно перестало работать), необходимо иметь доступ к сведениям о символах.</span><span class="sxs-lookup"><span data-stu-id="702a9-127">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="702a9-128">Дополнительные сведения можно найти <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)"> в разделе Диагностика сбоев системы с помощью анализатора сбоев </a> .</span><span class="sxs-lookup"><span data-stu-id="702a9-128">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="702a9-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="702a9-129">Related topics</span></span>

[<span data-ttu-id="702a9-130">Планирование развертывания DaRT 10</span><span class="sxs-lookup"><span data-stu-id="702a9-130">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 




