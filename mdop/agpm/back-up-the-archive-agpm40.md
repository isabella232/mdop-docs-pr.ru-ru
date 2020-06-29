---
title: Резервное копирование архива
description: Резервное копирование архива
author: dansimp
ms.assetid: 538d85eb-3596-4c1d-bbd7-26bc28857c28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c6888d61e126d603aefa4e818f1070c5a493ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819212"
---
# <span data-ttu-id="86bc9-103">Резервное копирование архива</span><span class="sxs-lookup"><span data-stu-id="86bc9-103">Back Up the Archive</span></span>


<span data-ttu-id="86bc9-104">Чтобы упростить восстановление архива для расширенного управления групповыми политиками (в случае аварии), администратор РАСШИРЕНного управления правами (Full Control) должен часто архивировать Архив.</span><span class="sxs-lookup"><span data-stu-id="86bc9-104">To help in the recovery of the archive for Advanced Group Policy Management (AGPM) if there is a disaster, an AGPM Administrator (Full Control) should back up the archive frequently.</span></span> <span data-ttu-id="86bc9-105">По умолчанию Архив создается в%ProgramData%\\Microsoft\\AGPM.</span><span class="sxs-lookup"><span data-stu-id="86bc9-105">By default, the archive is created in %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="86bc9-106">Однако вы можете указать другой путь во время настройки расширенного управления групповыми политиками (Майкрософт): сервер.</span><span class="sxs-lookup"><span data-stu-id="86bc9-106">However, you can specify a different path during the setup of Microsoft Advanced Group Policy Management - Server.</span></span>

<span data-ttu-id="86bc9-107">Для выполнения этой процедуры необходимо иметь учетную запись пользователя, у которой есть доступ к обоим серверам (в том числе с установленной службой РАСШИРЕНного доступа к данным) и к папке, содержащей архив.</span><span class="sxs-lookup"><span data-stu-id="86bc9-107">A user account that has access to both the AGPM Server—the computer on which the AGPM Service is installed—and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="86bc9-108">Создание резервной копии архива</span><span class="sxs-lookup"><span data-stu-id="86bc9-108">To back up the archive</span></span>**

1.  <span data-ttu-id="86bc9-109">Остановите службу РАСШИРЕНного.</span><span class="sxs-lookup"><span data-stu-id="86bc9-109">Stop the AGPM Service.</span></span> <span data-ttu-id="86bc9-110">Дополнительные сведения можно найти в разделе [Запуск и остановка службы расширенного](start-and-stop-the-agpm-service-agpm40.md)просмотра.</span><span class="sxs-lookup"><span data-stu-id="86bc9-110">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

2.  <span data-ttu-id="86bc9-111">Создайте резервную копию архивной папки с помощью проводника, xcopy, Windows Server® резервной копии или другого средства резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="86bc9-111">Back up the archive folder by using Windows Explorer, Xcopy, Windows Server® Backup, or another backup tool.</span></span> <span data-ttu-id="86bc9-112">Убедитесь в том, что вы хотите создать резервную копию скрытых, системных и только для чтения файлов.</span><span class="sxs-lookup"><span data-stu-id="86bc9-112">Make sure that you back up hidden, system, and read-only files.</span></span>

3.  <span data-ttu-id="86bc9-113">Храните архивную резервную копию в безопасном месте.</span><span class="sxs-lookup"><span data-stu-id="86bc9-113">Store the archive backup in a secure location.</span></span>

4.  <span data-ttu-id="86bc9-114">Перезапустите службу РАСШИРЕНного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="86bc9-114">Restart the AGPM Service.</span></span> <span data-ttu-id="86bc9-115">Дополнительные сведения можно найти в разделе [Запуск и остановка службы расширенного](start-and-stop-the-agpm-service-agpm40.md)просмотра.</span><span class="sxs-lookup"><span data-stu-id="86bc9-115">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

<span data-ttu-id="86bc9-116">**Примечание**  Если администратор РАСШИРЕНного администрирования не будет периодически архивировать Архив, объекты групповой политики (GPO) в архиве архивации не будут актуальными.</span><span class="sxs-lookup"><span data-stu-id="86bc9-116">**Note** If an AGPM Administrator backs up the archive infrequently, the Group Policy Objects (GPOs) in the archive backup will not be current.</span></span> <span data-ttu-id="86bc9-117">Чтобы лучше удостовериться в том, что резервная копия архивации актуальна, создайте резервную копию архива в рамках стратегии ежедневного резервного копирования вашей организации.</span><span class="sxs-lookup"><span data-stu-id="86bc9-117">To better ensure that the archive backup is current, back up the archive as part of your organization’s daily backup strategy.</span></span>

 

### <span data-ttu-id="86bc9-118">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="86bc9-118">Additional references</span></span>

-   [<span data-ttu-id="86bc9-119">Восстановление архива из резервной копии</span><span class="sxs-lookup"><span data-stu-id="86bc9-119">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

-   [<span data-ttu-id="86bc9-120">Перемещение сервера и архива AGPM</span><span class="sxs-lookup"><span data-stu-id="86bc9-120">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive-agpm40.md)

-   [<span data-ttu-id="86bc9-121">Управление архивами</span><span class="sxs-lookup"><span data-stu-id="86bc9-121">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





