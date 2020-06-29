---
title: Выполнение средства анализа сбоев Crash Analyzer на компьютере конечного пользователя
description: Выполнение средства анализа сбоев Crash Analyzer на компьютере конечного пользователя
author: dansimp
ms.assetid: 40af4ead-6588-4a81-8eaa-3dc00c397e1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 943e3956609ae7e24deaca4313036445802a8f7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823839"
---
# <span data-ttu-id="6da86-103">Выполнение средства анализа сбоев Crash Analyzer на компьютере конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="6da86-103">How to Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="6da86-104">Обычно вы запускаете средство диагностики и восстановления Microsoft (DaRT) 7 Crash Analyzer из окна инструментария средств диагностики и восстановления на компьютере конечного пользователя, на котором возникли проблемы.</span><span class="sxs-lookup"><span data-stu-id="6da86-104">Typically, you run Microsoft Diagnostics and Recovery Toolset (DaRT)7 Crash Analyzer from the Diagnostics and Recovery Toolset window on an end-user computer that has problems.</span></span> <span data-ttu-id="6da86-105">Анализатор сбоя пытается найти инструменты отладки для Windows на компьютере с неполадками.</span><span class="sxs-lookup"><span data-stu-id="6da86-105">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="6da86-106">Если диалоговое окно путь к каталогу не заполнено, необходимо указать расположение или перейти к расположению средств отладки для Windows (вы можете скачать файлы из Microsoft).</span><span class="sxs-lookup"><span data-stu-id="6da86-106">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="6da86-107">Кроме того, необходимо указать путь к месту расположения файлов символов.</span><span class="sxs-lookup"><span data-stu-id="6da86-107">You must also provide a path to where the symbol files are located.</span></span>

**<span data-ttu-id="6da86-108">Открытие и запуск анализатора сбоев на компьютере конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="6da86-108">To open and run the Crash Analyzer on an end-user computer</span></span>**

1.  <span data-ttu-id="6da86-109">В окне **инструментов Диагностика и восстановление** на компьютере конечного пользователя нажмите кнопку **аварийный анализ**.</span><span class="sxs-lookup"><span data-stu-id="6da86-109">On the **Diagnostics and Recovery Toolset** window on an end-user computer, click **Crash Analyzer**.</span></span>

2.  <span data-ttu-id="6da86-110">Введите необходимые сведения для указанных ниже параметров.</span><span class="sxs-lookup"><span data-stu-id="6da86-110">Provide the required information for the following:</span></span>

    -   <span data-ttu-id="6da86-111">Средства отладки Microsoft для Windows</span><span class="sxs-lookup"><span data-stu-id="6da86-111">Microsoft Debugging Tools for Windows</span></span>

    -   <span data-ttu-id="6da86-112">Файлы символов</span><span class="sxs-lookup"><span data-stu-id="6da86-112">Symbol files</span></span>

        <span data-ttu-id="6da86-113">Дополнительные сведения о файлах символов можно найти в разделе [как убедиться, что анализатор аварийного восстановления может получать доступ к файлам символов](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="6da86-113">For more information about symbol files, see, [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span></span>

    -   <span data-ttu-id="6da86-114">Файл аварийной копии памяти</span><span class="sxs-lookup"><span data-stu-id="6da86-114">A crash dump file</span></span>

        <span data-ttu-id="6da86-115">Чтобы определить расположение файла аварийного дампа, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6da86-115">Follow these steps to determine the location of the crash dump file:</span></span>

        1.  <span data-ttu-id="6da86-116">Откройте окно " **Свойства системы** ".</span><span class="sxs-lookup"><span data-stu-id="6da86-116">Open the **System Properties** window.</span></span>

            <span data-ttu-id="6da86-117">Нажмите кнопку **Пуск**, введите sysdm.cpl и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="6da86-117">Click **Start**, type sysdm.cpl, and then press Enter.</span></span>

        2.  <span data-ttu-id="6da86-118">Перейдите на вкладку **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="6da86-118">Click the **Advanced** tab.</span></span>

        3.  <span data-ttu-id="6da86-119">В области **Загрузка и восстановление** нажмите кнопку **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="6da86-119">In the **Startup and Recovery** area, click **Settings**.</span></span>

        <span data-ttu-id="6da86-120">**Примечание**  Если у вас нет доступа к окну " **Свойства системы** ", вы можете выполнить поиск файлов дампа на компьютере конечного пользователя с помощью средства **поиска** в DART.</span><span class="sxs-lookup"><span data-stu-id="6da86-120">**Note** If you do not have access to the **System Properties** window, you can search for dump files on the end-user computer by using the **Search** tool in DaRT.</span></span>

         

3.  <span data-ttu-id="6da86-121">**Анализатор сбоев** проверит файл аварийного дампа и сообщит о возможетм сбое.</span><span class="sxs-lookup"><span data-stu-id="6da86-121">The **Crash Analyzer** scans the crash dump file and reports a probable cause of the crash.</span></span> <span data-ttu-id="6da86-122">Вы можете просмотреть дополнительные сведения о сбоях, такие как конкретное сообщение об ошибке и описание, драйверы, загруженные на момент сбоя, и полные результаты анализа.</span><span class="sxs-lookup"><span data-stu-id="6da86-122">You can view more information about the crash, such as the specific crash message and description, the drivers loaded at the time of the crash, and the full output of the analysis.</span></span>

4.  <span data-ttu-id="6da86-123">Решите подходящую стратегию решения проблемы.</span><span class="sxs-lookup"><span data-stu-id="6da86-123">Decide upon an appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="6da86-124">Для этого может потребоваться отключить или обновить драйвер устройства, который вызвал сбой, с помощью узла **службы и драйверы** средства **управления компьютером** для DART.</span><span class="sxs-lookup"><span data-stu-id="6da86-124">This may require disabling or updating the device driver that caused the crash by using the **Services and Drivers** node of the **Computer Management** tool in DaRT.</span></span>

## <span data-ttu-id="6da86-125">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="6da86-125">Related topics</span></span>


[<span data-ttu-id="6da86-126">Диагностика ошибок системы с помощью средства анализа сбоев Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="6da86-126">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





