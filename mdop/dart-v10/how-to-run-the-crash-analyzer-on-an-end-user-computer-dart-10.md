---
title: Выполнение средства анализа сбоев Crash Analyzer на компьютере конечного пользователя
description: Выполнение средства анализа сбоев Crash Analyzer на компьютере конечного пользователя
author: dansimp
ms.assetid: 10334800-ff8e-43ac-a9c2-d28807473ec2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4abf1ba2ae1a0cb1dfb129c1f5a26e11f5045290
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822669"
---
# <span data-ttu-id="3ec50-103">Выполнение средства анализа сбоев Crash Analyzer на компьютере конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="3ec50-103">How to Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="3ec50-104">Чтобы запустить **Анализатор аварийного** восстановления из окна **инструментов Диагностика и восстановление** на компьютере конечного пользователя, на котором возникли проблемы, необходимо установить средства отладки Microsoft для Windows и файлы символов.</span><span class="sxs-lookup"><span data-stu-id="3ec50-104">To run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing problems, you must have the Microsoft Debugging Tools for Windows and the symbol files installed.</span></span> <span data-ttu-id="3ec50-105">Для загрузки средств отладки Windows ознакомьтесь со [средствами отладки для Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="3ec50-105">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span>

**<span data-ttu-id="3ec50-106">Запуск анализатора сбоев на компьютере конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="3ec50-106">To run the Crash Analyzer on an end-user computer</span></span>**

1.  <span data-ttu-id="3ec50-107">В окне **инструментов Диагностика и восстановление** на компьютере конечного пользователя нажмите кнопку **аварийный анализ**.</span><span class="sxs-lookup"><span data-stu-id="3ec50-107">On the **Diagnostics and Recovery Toolset** window on an end-user computer, click **Crash Analyzer**.</span></span>

2.  <span data-ttu-id="3ec50-108">Укажите необходимые сведения о средствах отладки Microsoft для Windows.</span><span class="sxs-lookup"><span data-stu-id="3ec50-108">Provide the required information for the Microsoft Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="3ec50-109">Укажите необходимые сведения для файлов символов.</span><span class="sxs-lookup"><span data-stu-id="3ec50-109">Provide the required information for the symbol files.</span></span> <span data-ttu-id="3ec50-110">Дополнительные сведения о файлах символов [можно найти в разделе как убедиться, что анализатор аварийного восстановления может получать доступ к файлам символов](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="3ec50-110">For more information about symbol files, see [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md).</span></span>

4.  <span data-ttu-id="3ec50-111">Введите необходимые сведения для файла дампа памяти.</span><span class="sxs-lookup"><span data-stu-id="3ec50-111">Provide the required information for a memory dump file.</span></span> <span data-ttu-id="3ec50-112">Чтобы определить расположение файла дампа памяти, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3ec50-112">To determine the location of the memory dump file:</span></span>

    1.  <span data-ttu-id="3ec50-113">Откройте окно " **Свойства системы** ".</span><span class="sxs-lookup"><span data-stu-id="3ec50-113">Open the **System Properties** window.</span></span>

    2.  <span data-ttu-id="3ec50-114">Нажмите кнопку **Пуск**, введите **sysdm.cpl**и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="3ec50-114">Click **Start**, type **sysdm.cpl**, and then press **Enter**.</span></span>

    3.  <span data-ttu-id="3ec50-115">Перейдите на вкладку **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="3ec50-115">Click the **Advanced** tab.</span></span>

    4.  <span data-ttu-id="3ec50-116">В области **Загрузка и восстановление** нажмите кнопку **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="3ec50-116">In the **Startup and Recovery** area, click **Settings**.</span></span>

        <span data-ttu-id="3ec50-117">Если у вас нет доступа к окну " **Свойства системы** ", вы можете выполнить поиск файлов дампа на компьютере конечного пользователя с помощью средства **поиска** в Microsoft Diagnostics и средств восстановления (DART) 10.</span><span class="sxs-lookup"><span data-stu-id="3ec50-117">If you do not have access to the **System Properties** window, you can search for dump files on the end-user computer by using the **Search** tool in Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span></span>

    <span data-ttu-id="3ec50-118">**Анализатор сбоев** проверит файл дампа памяти и сообщит о причинах возникновения проблемы.</span><span class="sxs-lookup"><span data-stu-id="3ec50-118">The **Crash Analyzer** scans the memory dump file and reports a probable cause of the problem.</span></span> <span data-ttu-id="3ec50-119">Вы можете просмотреть дополнительные сведения об ошибке, например конкретное сообщение дампа памяти и описание, драйверы, загруженные на момент сбоя, и полные результаты анализа.</span><span class="sxs-lookup"><span data-stu-id="3ec50-119">You can view more information about the failure, such as the specific memory dump message and description, the drivers loaded at the time of the failure, and the full output of the analysis.</span></span>

5.  <span data-ttu-id="3ec50-120">Определите подходящую стратегию решения проблемы.</span><span class="sxs-lookup"><span data-stu-id="3ec50-120">Identify the appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="3ec50-121">Для стратегии может потребоваться отключить или обновить драйвер устройства, который вызвал ошибку, с помощью узла **службы и драйверы** средства **управления компьютером** в DART 10.</span><span class="sxs-lookup"><span data-stu-id="3ec50-121">The strategy may require disabling or updating the device driver that caused the failure by using the **Services and Drivers** node of the **Computer Management** tool in DaRT 10.</span></span>

## <span data-ttu-id="3ec50-122">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3ec50-122">Related topics</span></span>


[<span data-ttu-id="3ec50-123">Диагностика ошибок системы с помощью средства анализа сбоев Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="3ec50-123">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer-dart-10.md)

[<span data-ttu-id="3ec50-124">Операции DaRT 10</span><span class="sxs-lookup"><span data-stu-id="3ec50-124">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

 

 





