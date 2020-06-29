---
title: Изменение уровней создания отчетов журналов и сброс файлов журналов
description: Изменение уровней создания отчетов журналов и сброс файлов журналов
author: dansimp
ms.assetid: 9561d6fb-b35c-491b-a355-000064583194
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7307dee0030d9c03a8107d9d0ceef2086a94df07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818049"
---
# <span data-ttu-id="f5c44-103">Изменение уровней создания отчетов журналов и сброс файлов журналов</span><span class="sxs-lookup"><span data-stu-id="f5c44-103">How to Change the Log Reporting Levels and Reset the Log Files</span></span>


<span data-ttu-id="f5c44-104">С помощью описанной ниже процедуры можно изменить уровень ведения отчета журнала с узла **Application Virtualization** в консоли управления Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f5c44-104">You can use the following procedure to change the log reporting level from the **Application Virtualization** node in the Application Virtualization Management Console.</span></span> <span data-ttu-id="f5c44-105">Если файл журнала достигнет максимального размера (значение по умолчанию — 256 МБ), сброс будет принудительным, когда происходит следующая запись в журнал.</span><span class="sxs-lookup"><span data-stu-id="f5c44-105">When the log file reaches the maximum size (default is 256 MB), a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="f5c44-106">Сброс приводит к созданию нового файла журнала, а старый файл переименовывается в качестве резервной копии.</span><span class="sxs-lookup"><span data-stu-id="f5c44-106">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span>

**<span data-ttu-id="f5c44-107">Изменение уровня ведения журнала</span><span class="sxs-lookup"><span data-stu-id="f5c44-107">To change the log reporting level</span></span>**

1.  <span data-ttu-id="f5c44-108">Щелкните правой кнопкой мыши узел **Application Virtualization** и во всплывающем меню выберите пункт **свойства** .</span><span class="sxs-lookup"><span data-stu-id="f5c44-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="f5c44-109">На вкладке **Общие** в диалоговом окне **свойства** в раскрывающемся списке **Log Level (журнал** ) выберите необходимый уровень ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="f5c44-109">On the **General** tab in the **Properties** dialog box, from the **Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="f5c44-110">**Примечание**  Если вы выбрали **подробный** уровень ведения журнала, файлы журнала будут значительно увеличиваться очень быстро.</span><span class="sxs-lookup"><span data-stu-id="f5c44-110">**Note** If you choose **Verbose** as the logging level, the log files will grow large very quickly.</span></span> <span data-ttu-id="f5c44-111">Это может препятствовать работе клиента, поэтому рекомендуется использовать этот уровень ведения журнала только для диагностики конкретных проблем.</span><span class="sxs-lookup"><span data-stu-id="f5c44-111">This might inhibit client performance, so best practice is to use this log level only for diagnosing specific problems.</span></span>

     

3.  <span data-ttu-id="f5c44-112">На вкладке **Общие** в диалоговом окне **свойства** в раскрывающемся списке **системный журнал** выберите необходимый уровень ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="f5c44-112">On the **General** tab in the **Properties** dialog box, from the **System Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="f5c44-113">**Примечание**  Параметр **уровня системного журнала** определяет уровень сообщений, отправляемых в журнал событий системы.</span><span class="sxs-lookup"><span data-stu-id="f5c44-113">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="f5c44-114">Журнальные сообщения идентичны сообщениям, которые регистрируются в журнале событий клиента, но хранятся в другом расположении.</span><span class="sxs-lookup"><span data-stu-id="f5c44-114">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location.</span></span>

     

4.  <span data-ttu-id="f5c44-115">Нажмите кнопку **ОК** или **Применить** , чтобы изменить параметр.</span><span class="sxs-lookup"><span data-stu-id="f5c44-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="f5c44-116">Сброс файла журнала</span><span class="sxs-lookup"><span data-stu-id="f5c44-116">To reset the log file</span></span>**

1.  <span data-ttu-id="f5c44-117">Щелкните правой кнопкой мыши узел **Application Virtualization** и во всплывающем меню выберите пункт **свойства** .</span><span class="sxs-lookup"><span data-stu-id="f5c44-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="f5c44-118">На вкладке **Общие** в диалоговом окне **Свойства** нажмите кнопку **сброс журнала** , чтобы создать резервную копию текущего файла журнала и сразу же начните новый файл журнала.</span><span class="sxs-lookup"><span data-stu-id="f5c44-118">On the **General** tab in the **Properties** dialog box, click **Reset Log** to back up the current log file and immediately start a new log file.</span></span> <span data-ttu-id="f5c44-119">Файлы журнала резервного копирования хранятся в той же папке.</span><span class="sxs-lookup"><span data-stu-id="f5c44-119">The backup log files are stored in the same folder.</span></span>

3.  <span data-ttu-id="f5c44-120">Нажмите кнопку **ОК** или **Применить** , чтобы изменить параметр.</span><span class="sxs-lookup"><span data-stu-id="f5c44-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="f5c44-121">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f5c44-121">Related topics</span></span>


[<span data-ttu-id="f5c44-122">Настройка клиента в консоли управления клиентом Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f5c44-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

[<span data-ttu-id="f5c44-123">Разрешения на доступ пользователей в клиенте Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f5c44-123">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





