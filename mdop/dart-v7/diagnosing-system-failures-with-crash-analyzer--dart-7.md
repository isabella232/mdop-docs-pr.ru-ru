---
title: Диагностика ошибок системы с помощью средства анализа сбоев Crash Analyzer
description: Диагностика ошибок системы с помощью средства анализа сбоев Crash Analyzer
author: dansimp
ms.assetid: 170d40ef-4edb-4a32-a349-c285c0ea5e56
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c5f8b7e189de024d7ceb84f8cfc151dc82d56ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823469"
---
# <span data-ttu-id="8d8f5-103">Диагностика ошибок системы с помощью средства анализа сбоев Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="8d8f5-103">Diagnosing System Failures with Crash Analyzer</span></span>


<span data-ttu-id="8d8f5-104">Анализатор сбоев в средстве диагностики и восстановления Microsoft (DaRT) 7 позволяет отлаживать файл аварийной копии памяти на компьютере с Windows и затем диагностировать все связанные ошибки компьютера.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-104">The Crash Analyzer in Microsoft Diagnostics and Recovery Toolset (DaRT)7 lets you debug a crash dump file on a Windows-based computer and then diagnose any related computer errors.</span></span> <span data-ttu-id="8d8f5-105">Анализатор сбоев использует инструменты отладки Microsoft для Windows для проверки файла аварийного дампа для драйвера, который привел к сбою компьютера.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-105">The Crash Analyzer uses the Microsoft Debugging Tools for Windows to examine a crash dump file for the driver that caused the computer to fail.</span></span>

## <span data-ttu-id="8d8f5-106">Запуск анализатора сбоев на компьютере конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="8d8f5-106">Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="8d8f5-107">Обычно вы запускаете аварийный анализ в окне инструментария диагностики и восстановления на компьютере конечного пользователя, на котором возникли проблемы.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-107">Typically, you run Crash Analyzer from the Diagnostics and Recovery Toolset window on an end-user computer that has problems.</span></span> <span data-ttu-id="8d8f5-108">Анализатор сбоя пытается найти инструменты отладки для Windows на компьютере с неполадками.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-108">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="8d8f5-109">Если диалоговое окно путь к каталогу не заполнено, необходимо указать расположение или перейти к расположению средств отладки для Windows (вы можете скачать файлы из Microsoft).</span><span class="sxs-lookup"><span data-stu-id="8d8f5-109">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="8d8f5-110">Кроме того, необходимо указать путь к месту расположения файлов символов.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-110">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="8d8f5-111">Если вы включили инструменты для отладки Microsoft для Windows и файлы символов при создании образа восстановления DaRT, они должны быть доступны при запуске анализатора сбоев на компьютере с неполадками.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-111">If you included the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT recovery image, they should be available when you run the Crash Analyzer on the problem computer.</span></span>

[<span data-ttu-id="8d8f5-112">Выполнение средства анализа сбоев Crash Analyzer на компьютере конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="8d8f5-112">How to Run the Crash Analyzer on an End-user Computer</span></span>](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-7.md)

## <span data-ttu-id="8d8f5-113">Запуск анализатора сбоев в автономном режиме на компьютере, отличном от компьютера конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="8d8f5-113">Run the Crash Analyzer in stand-alone mode on a computer other than an end-user computer</span></span>


<span data-ttu-id="8d8f5-114">Анализатор сбоя пытается найти инструменты отладки для Windows на компьютере с неполадками.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-114">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="8d8f5-115">Если диалоговое окно путь к каталогу не заполнено, необходимо указать расположение или перейти к расположению средств отладки для Windows (вы можете скачать файлы из Microsoft).</span><span class="sxs-lookup"><span data-stu-id="8d8f5-115">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="8d8f5-116">Кроме того, необходимо указать путь к месту расположения файлов символов.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-116">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="8d8f5-117">Если вы не включали средства отладки Microsoft для Windows и файлы символов, созданные с помощью печатного образа для стрелок, или если вы не можете получить их из-за проблем с подключением к сети, вы можете скопировать файл дампа с проблемного компьютера и проанализировать его на компьютере, на котором установлен автономный анализатор аварийной версии. , например на компьютере администратора службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-117">If you did not include the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining them, then you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of Crash Analyzer installed, such as a helpdesk administrator’s computer.</span></span>

[<span data-ttu-id="8d8f5-118">Выполнение средства анализа сбоев Crash Analyzer в автономном режиме на компьютере, отличном от компьютера конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="8d8f5-118">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-7.md)

## <span data-ttu-id="8d8f5-119">Убедитесь в том, что анализатор аварийного восстановления может получать доступ к файлам символов.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-119">Ensure that Crash Analyzer can access symbol files</span></span>


<span data-ttu-id="8d8f5-120">Обычно отладочная информация хранится в файле символов, отдельном от исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-120">Typically, debugging information is stored in a symbol file that is separate from the executable.</span></span> <span data-ttu-id="8d8f5-121">При отладке приложения, которое перестало отвечать (например, если произошел сбой), необходимо иметь доступ к сведениям о символах.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-121">You must have access to the symbol information when you debug an application that has stopped responding, for example if it crashed.</span></span>

<span data-ttu-id="8d8f5-122">Файлы символов загружаются автоматически при запуске анализатора аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-122">Symbol files are automatically downloaded when you run Crash Analyzer.</span></span> <span data-ttu-id="8d8f5-123">Если у компьютера нет подключения к Интернету или в сети требуется, чтобы компьютер имел доступ к прокси-серверу HTTP, Загрузка файлов символов невозможна.</span><span class="sxs-lookup"><span data-stu-id="8d8f5-123">If the computer does not have an Internet connection or the network requires the computer to access an HTTP proxy server, the symbol files cannot be downloaded.</span></span>

[<span data-ttu-id="8d8f5-124">Обеспечение доступа к файлам символов для средства анализа сбоев Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="8d8f5-124">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md)

## <span data-ttu-id="8d8f5-125">Другие ресурсы для диагностики сбоев системы с помощью анализатора сбоев</span><span class="sxs-lookup"><span data-stu-id="8d8f5-125">Other resources for diagnosing system failures with Crash Analyzer</span></span>


[<span data-ttu-id="8d8f5-126">Операции DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="8d8f5-126">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





