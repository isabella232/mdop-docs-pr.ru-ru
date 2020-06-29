---
title: Выполнение средства анализа сбоев Crash Analyzer в автономном режиме на компьютере, отличном от компьютера конечного пользователя
description: Выполнение средства анализа сбоев Crash Analyzer в автономном режиме на компьютере, отличном от компьютера конечного пользователя
author: dansimp
ms.assetid: 881d573f-2f18-4c5f-838e-2f5320179f94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6f398c56b7c631145388541b71229d69c16bf6f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822789"
---
# <span data-ttu-id="d8d79-103">Выполнение средства анализа сбоев Crash Analyzer в автономном режиме на компьютере, отличном от компьютера конечного пользователя</span><span class="sxs-lookup"><span data-stu-id="d8d79-103">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>


<span data-ttu-id="d8d79-104">Если вам не удается получить доступ к средствам отладки Microsoft для Windows или файлам символов на компьютере пользователя, вы можете скопировать файл дампа с проблемного компьютера и проанализировать его на компьютере с установленной изолированной версией анализатора сбоев, например на компьютере администратора службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="d8d79-104">If you cannot access the Microsoft Debugging Tools for Windows or the symbol files on the end-user computer, you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of Crash Analyzer installed, such as a helpdesk administrator’s computer.</span></span>

**<span data-ttu-id="d8d79-105">Запуск анализатора сбоев в изолированном режиме</span><span class="sxs-lookup"><span data-stu-id="d8d79-105">To run the Crash Analyzer in stand-alone mode</span></span>**

1.  <span data-ttu-id="d8d79-106">На компьютере с установленным DaRT7 нажмите кнопку **запустить**  /  **все программы**  /  **Microsoft DaRT 7**.</span><span class="sxs-lookup"><span data-stu-id="d8d79-106">On a computer with DaRT7 installed, click **Start** / **All Programs** / **Microsoft DaRT 7**.</span></span>

2.  <span data-ttu-id="d8d79-107">Введите необходимые сведения для указанных ниже параметров.</span><span class="sxs-lookup"><span data-stu-id="d8d79-107">Provide the required information for the following:</span></span>

    -   <span data-ttu-id="d8d79-108">Средства отладки Microsoft для Windows</span><span class="sxs-lookup"><span data-stu-id="d8d79-108">Microsoft Debugging Tools for Windows</span></span>

    -   <span data-ttu-id="d8d79-109">Файлы символов</span><span class="sxs-lookup"><span data-stu-id="d8d79-109">Symbol files</span></span>

        <span data-ttu-id="d8d79-110">Дополнительные сведения о файлах символов можно найти в разделе [как убедиться, что анализатор аварийного восстановления может получать доступ к файлам символов](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="d8d79-110">For more information about symbol files, see, [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span></span>

    -   <span data-ttu-id="d8d79-111">Файл аварийной копии памяти</span><span class="sxs-lookup"><span data-stu-id="d8d79-111">A crash dump file</span></span>

        <span data-ttu-id="d8d79-112">**Примечание**  С помощью средства поиска в DaRT7 найдите скопированный файл аварийной копии памяти.</span><span class="sxs-lookup"><span data-stu-id="d8d79-112">**Note** Use the Search tool in DaRT7 to locate the copied crash dump file.</span></span>

         

3.  <span data-ttu-id="d8d79-113">**Анализатор сбоев** проверит файл аварийного дампа и сообщит о возможетм сбое.</span><span class="sxs-lookup"><span data-stu-id="d8d79-113">The **Crash Analyzer** scans the crash dump file and reports a probable cause of the crash.</span></span> <span data-ttu-id="d8d79-114">Вы можете просмотреть дополнительные сведения о сбоях, такие как конкретное сообщение об ошибке и описание, драйверы, загруженные на момент сбоя, и полные результаты анализа.</span><span class="sxs-lookup"><span data-stu-id="d8d79-114">You can view more information about the crash, such as the specific crash message and description, the drivers loaded at the time of the crash, and the full output of the analysis.</span></span>

4.  <span data-ttu-id="d8d79-115">Решите подходящую стратегию решения проблемы.</span><span class="sxs-lookup"><span data-stu-id="d8d79-115">Decide upon an appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="d8d79-116">Для этого может потребоваться отключить или обновить драйвер устройства, который вызвал сбой, с помощью узла **службы и драйверы** средства **управления компьютером** для DART.</span><span class="sxs-lookup"><span data-stu-id="d8d79-116">This may require disabling or updating the device driver that caused the crash by using the **Services and Drivers** node of the **Computer Management** tool in DaRT.</span></span>

## <span data-ttu-id="d8d79-117">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d8d79-117">Related topics</span></span>


[<span data-ttu-id="d8d79-118">Диагностика ошибок системы с помощью средства анализа сбоев Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="d8d79-118">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





