---
title: Диагностика ошибок системы с помощью средства анализа сбоев Crash Analyzer
description: Диагностика ошибок системы с помощью средства анализа сбоев Crash Analyzer
author: dansimp
ms.assetid: 7ebef49e-a294-4173-adb1-7e6994aa01ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d0f4b71bf267d65ec53dd1b3e23fd8a59190b0b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813109"
---
# <span data-ttu-id="0e7e9-103">Диагностика ошибок системы с помощью средства анализа сбоев Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="0e7e9-103">Diagnosing System Failures with Crash Analyzer</span></span>


<span data-ttu-id="0e7e9-104">**Анализатор сбоев** в наборе средств диагностики и восстановления Microsoft (DART) 10 позволяет отладить файл дампа памяти на компьютере с Windows и затем диагностировать все связанные ошибки компьютера.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-104">The **Crash Analyzer** in Microsoft Diagnostics and Recovery Toolset (DaRT) 10 lets you debug a memory dump file on a Windows-based computer and then diagnose any related computer errors.</span></span> <span data-ttu-id="0e7e9-105">**Анализатор сбоев** использует инструменты отладки Microsoft для Windows для проверки файла дампа памяти драйвера, который привел к сбою компьютера.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-105">The **Crash Analyzer** uses the Microsoft Debugging Tools for Windows to examine a memory dump file for the driver that caused the computer to fail.</span></span> <span data-ttu-id="0e7e9-106">Вы можете запустить анализатор аварийного восстановления на компьютере с конечным пользователем или в автономном режиме на компьютере, отличном от компьютера конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-106">You can run the Crash Analyzer on an end-user computer or in stand-alone mode on a computer other than an end-user computer.</span></span>

## <span data-ttu-id="0e7e9-107">Запуск анализатора сбоев на компьютере с конечным пользователем</span><span class="sxs-lookup"><span data-stu-id="0e7e9-107">Run the Crash Analyzer on an end-user-computer</span></span>


<span data-ttu-id="0e7e9-108">Обычно вы запускаете **аварийный анализ** в окне **набора средств диагностики и восстановления** на компьютере конечного пользователя, на котором возникают проблемы.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-108">Typically, you run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing the problem.</span></span> <span data-ttu-id="0e7e9-109">**Анализатор сбоя** пытается найти инструменты отладки для Windows на компьютере с неполадками.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-109">The **Crash Analyzer** tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="0e7e9-110">Если диалоговое окно путь к каталогу не заполнено, необходимо указать расположение или перейти к расположению средств отладки для Windows (вы можете скачать файлы из Microsoft).</span><span class="sxs-lookup"><span data-stu-id="0e7e9-110">If the directory path dialog box is empty, you must enter the location, or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="0e7e9-111">Кроме того, необходимо указать путь к месту расположения файлов символов.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-111">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="0e7e9-112">Если вы включили инструменты отладки Microsoft для Windows и файлы символов при создании образа для восстановления DaRT 10, средства и файлы символов должны быть доступны при запуске **анализатора сбоев** на компьютере с неполадками.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-112">If you included the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT 10 recovery image, the Tools and symbol files should be available when you run the **Crash Analyzer** on the problem computer.</span></span> <span data-ttu-id="0e7e9-113">Если вы не включали их в образ восстановления DaRT или не можете получить их из-за проблем с размером диска или сетевым подключением, можно также запустить анализатор сбоев в автономном режиме на компьютере, отличном от компьютера конечного пользователя, как описано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-113">If you did not include them in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining them, you can alternatively run the Crash Analyzer in stand-alone mode on a computer other than the end user’s computer, as described in the following section.</span></span>

[<span data-ttu-id="0e7e9-114">Выполнение средства анализа сбоев Crash Analyzer на компьютере конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="0e7e9-114">How to Run the Crash Analyzer on an End-user Computer</span></span>](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-10.md)

## <a href="" id="run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-s-computer"></a><span data-ttu-id="0e7e9-115">Запуск анализатора сбоев в автономном режиме на компьютере, отличном от компьютера конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="0e7e9-115">Run the Crash Analyzer in stand-alone mode on a computer other than an end user’s computer</span></span>


<span data-ttu-id="0e7e9-116">Несмотря на то, что обычно запускается **Анализатор аварийного** восстановления на компьютере пользователя, на котором возникла проблема, вы также можете запустить анализатор сбоев в автономном режиме на компьютере, отличном от конечного компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-116">Although you typically run **Crash Analyzer** on the end-user computer that is experiencing the problem, you can also run the Crash Analyzer in stand-alone mode, on a computer other than an end-user computer.</span></span> <span data-ttu-id="0e7e9-117">Вы можете выбрать этот параметр, если вы не включали средства отладки Windows в образе восстановления DaRT, или если не удается получить доступ к средствам отладки.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-117">You might choose this option if you did not include the Windows Debugging Tools in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining the Debugging Tools.</span></span> <span data-ttu-id="0e7e9-118">В этом случае вы можете скопировать файл дампа с проблемного компьютера и проанализировать его на компьютере с установленной изолированной версией **анализатора сбоев** , например на компьютере агента службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-118">In this case, you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of **Crash Analyzer** installed, such as on a help desk agent’s computer.</span></span>

[<span data-ttu-id="0e7e9-119">Выполнение средства анализа сбоев Crash Analyzer в автономном режиме на компьютере, отличном от компьютера конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="0e7e9-119">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-10.md)

## <span data-ttu-id="0e7e9-120">Как убедиться, что анализатор сбоя может получить доступ к файлам символов</span><span class="sxs-lookup"><span data-stu-id="0e7e9-120">How to ensure that Crash Analyzer can access symbol files</span></span>


<span data-ttu-id="0e7e9-121">Чтобы отладить приложения, которые перестали отвечать, вам необходим доступ к файлу символов, отдельному от программы.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-121">To debug applications that have stopped responding, you need access to the symbol file, which is separate from the program.</span></span> <span data-ttu-id="0e7e9-122">Несмотря на то что файлы символов автоматически загружаются при запуске анализатора аварийного восстановления, может возникнуть ситуация, когда компьютер не имеет доступа к Интернету.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-122">Although symbol files are automatically downloaded when you run Crash Analyzer, there might be times when the problem computer does not have access to the Internet.</span></span> <span data-ttu-id="0e7e9-123">Есть несколько способов удостовериться в том, что вы гарантированно получили доступ к файлам символов.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-123">There are several ways to ensure that you have guaranteed access to symbol files.</span></span>

[<span data-ttu-id="0e7e9-124">Обеспечение доступа к файлам символов для средства анализа сбоев Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="0e7e9-124">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md)

## <span data-ttu-id="0e7e9-125">Другие ресурсы для диагностики сбоев системы с помощью анализатора сбоев</span><span class="sxs-lookup"><span data-stu-id="0e7e9-125">Other resources for diagnosing system failures with Crash Analyzer</span></span>


[<span data-ttu-id="0e7e9-126">Операции DaRT 10</span><span class="sxs-lookup"><span data-stu-id="0e7e9-126">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

 

 





