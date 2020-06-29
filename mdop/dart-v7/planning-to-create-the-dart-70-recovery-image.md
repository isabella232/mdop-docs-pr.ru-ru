---
title: Планирование создания образа для восстановления DaRT 7.0
description: Планирование создания образа для восстановления DaRT 7.0
author: dansimp
ms.assetid: e5d49bee-ae4e-467b-9976-c1203f6355f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c370d2a69ec8ccea217696045e64e9a0ae724815
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821332"
---
# <span data-ttu-id="1017e-103">Планирование создания образа для восстановления DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="1017e-103">Planning to Create the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="1017e-104">При планировании создания образа восстановления для набора средств диагностики и восстановления Microsoft (DaRT) 7 используется информация, описанная в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="1017e-104">Use the information in this section when you plan for creating the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="1017e-105">Планирование создания образа для восстановления DaRT 7</span><span class="sxs-lookup"><span data-stu-id="1017e-105">Planning to Create the DaRT 7 Recovery Image</span></span>


<span data-ttu-id="1017e-106">При создании изображения для восстановления DaRT необходимо решить, какие инструменты следует включить в изображение.</span><span class="sxs-lookup"><span data-stu-id="1017e-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="1017e-107">Когда вы принимаете это решение, помните, что конечные пользователи могут иногда получить доступ к различным средствам DaRT.</span><span class="sxs-lookup"><span data-stu-id="1017e-107">When you make that decision, remember that end users might have access occasionally to the various DaRT tools.</span></span> <span data-ttu-id="1017e-108">Дополнительные сведения о средствах DaRT можно найти в статье [Обзор средств на dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="1017e-108">For more information about the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span> <span data-ttu-id="1017e-109">Дополнительные сведения о том, как создать защищенный образ восстановления, приведены в разделе [рекомендации по обеспечению безопасности для DaRT 7,0](security-considerations-for-dart-70-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="1017e-109">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 7.0](security-considerations-for-dart-70-dart-7.md).</span></span>

<span data-ttu-id="1017e-110">При создании изображения для восстановления DaRT вы также можете указать, нужно ли включать дополнительные драйверы или файлы.</span><span class="sxs-lookup"><span data-stu-id="1017e-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="1017e-111">Определите расположение дополнительных драйверов или файлов, которые вы хотите включить в изображение для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="1017e-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

## <span data-ttu-id="1017e-112">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="1017e-112">Prerequisites</span></span>


<span data-ttu-id="1017e-113">Следующие элементы являются обязательными или рекомендуемыми для создания изображения для восстановления DaRT:</span><span class="sxs-lookup"><span data-stu-id="1017e-113">The following items are required or recommended for creating the DaRT recovery image:</span></span>

-   <span data-ttu-id="1017e-114">Исходные файлы Windows 7</span><span class="sxs-lookup"><span data-stu-id="1017e-114">Windows 7 source files</span></span>

    <span data-ttu-id="1017e-115">Необходимо указать путь к установочным файлам Windows 7 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1017e-115">You must provide the path of a Windows 7 DVD or of Windows 7 source files.</span></span> <span data-ttu-id="1017e-116">Исходные файлы Windows 7 необходимы для создания образа для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="1017e-116">Windows 7 source files are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="1017e-117">Средства отладки Windows для платформы</span><span class="sxs-lookup"><span data-stu-id="1017e-117">Windows Debugging Tools for your platform</span></span>

    <span data-ttu-id="1017e-118">Средства отладки Windows являются обязательными при запуске **анализатора отказов** , чтобы определить причину сбоя компьютера.</span><span class="sxs-lookup"><span data-stu-id="1017e-118">Windows Debugging Tools are required when you run **Crash Analyzer** to determine the cause of a computer crash.</span></span> <span data-ttu-id="1017e-119">Мы рекомендуем указать путь к средствам отладки Windows на момент создания изображения для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="1017e-119">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="1017e-120">При необходимости вы можете скачать инструменты для отладки Windows здесь: [скачивание и установка средств отладки для Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span><span class="sxs-lookup"><span data-stu-id="1017e-120">If it is necessary, you can download the Windows Debugging Tools here: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

-   <span data-ttu-id="1017e-121">Необязательно: **автономные определения системных параметров очистки**</span><span class="sxs-lookup"><span data-stu-id="1017e-121">Optional: **Standalone System Sweeper** definitions</span></span>

    <span data-ttu-id="1017e-122">Последние определения для **автономного средства очистки системы** требуются при запуске этого инструмента.</span><span class="sxs-lookup"><span data-stu-id="1017e-122">The latest definitions for the **Standalone System Sweeper** are required when you run this tool.</span></span> <span data-ttu-id="1017e-123">Несмотря на то, что вы можете скачать определения при запуске **автономного системного чистильщика**, мы рекомендуем загрузить последние определения на момент создания изображения для восстановления DART.</span><span class="sxs-lookup"><span data-stu-id="1017e-123">Although you can download the definitions when you run **Standalone System Sweeper**, we recommend that you download the latest definitions at the time you create the DaRT recovery image.</span></span> <span data-ttu-id="1017e-124">Таким образом, вы можете по-прежнему запускать это средство с самыми последними определениями, даже если у проблемного компьютера нет сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="1017e-124">In this manner, you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span>

-   <span data-ttu-id="1017e-125">Необязательно: файлы символов Windows для работы с **анализатором аварийного** восстановления</span><span class="sxs-lookup"><span data-stu-id="1017e-125">Optional: Windows symbols files for use with **Crash Analyzer**</span></span>

    <span data-ttu-id="1017e-126">Обычно отладочная информация хранится в файле символов, отдельном от исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="1017e-126">Typically, debugging information is stored in a symbol file that is separate from the executable.</span></span> <span data-ttu-id="1017e-127">При отладке приложения, которое перестало отвечать (например, если произошел сбой), необходимо иметь доступ к сведениям о символах.</span><span class="sxs-lookup"><span data-stu-id="1017e-127">You must have access to the symbol information when you debug an application that has stopped responding, for example if it crashed.</span></span> <span data-ttu-id="1017e-128">Дополнительные сведения можно найти [в разделе Диагностика сбоев системы с помощью анализатора сбоев](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="1017e-128">For more information, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span></span>

## <span data-ttu-id="1017e-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1017e-129">Related topics</span></span>


[<span data-ttu-id="1017e-130">Планирование развертывания DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="1017e-130">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





