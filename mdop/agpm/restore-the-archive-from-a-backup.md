---
title: Восстановление архива из резервной копии
description: Восстановление архива из резервной копии
author: dansimp
ms.assetid: 49666337-d72c-4e44-99e4-9eb59b2355a9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b00d2e5e612e2ac43f965e4adf6175e2fd159007
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818362"
---
# <span data-ttu-id="fe991-103">Восстановление архива из резервной копии</span><span class="sxs-lookup"><span data-stu-id="fe991-103">Restore the Archive from a Backup</span></span>


<span data-ttu-id="fe991-104">В случае аварийного восстановления и повреждения архива для расширенного управления групповыми политиками (расширенный доступ) Администратор РАСШИРЕНного доступа (Full Control) может восстановить архив из резервной копии, подготовленной заранее, и импортировать данные из рабочей среды в любые объекты групповой политики (GPO), которых нет в архиве, или для которых версия в рабочей среде больше текущих, чем в архиве.</span><span class="sxs-lookup"><span data-stu-id="fe991-104">If a disaster occurs and the archive for Advanced Group Policy Management (AGPM) is damaged or destroyed, an AGPM Administrator (Full Control) can restore the archive from a backup copy prepared in advance and then import from the production environment any Group Policy Objects (GPOs) that are not in the archive or for which the version in production is more current than that in the archive.</span></span> <span data-ttu-id="fe991-105">Сведения о том, как восстановить архив архивации на другом сервере, можно найти в разделе [Перемещение сервера расширенного использования и архива](move-the-agpm-server-and-the-archive.md).</span><span class="sxs-lookup"><span data-stu-id="fe991-105">For information about how to restore an archive backup to a different server, see [Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive.md).</span></span>

<span data-ttu-id="fe991-106">Для выполнения этой процедуры требуется учетная запись пользователя, имеющая доступ к серверу РАСШИРЕНного доступа (компьютеру, на котором установлена служба РАСШИРЕНного доступа к данным) и папке, содержащей архив.</span><span class="sxs-lookup"><span data-stu-id="fe991-106">A user account that has access to the AGPM Server (the computer on which the AGPM Service is installed) and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="fe991-107">Восстановление архива из резервной копии</span><span class="sxs-lookup"><span data-stu-id="fe991-107">To restore the archive from a backup</span></span>**

1.  <span data-ttu-id="fe991-108">Остановите службу РАСШИРЕНного.</span><span class="sxs-lookup"><span data-stu-id="fe991-108">Stop the AGPM Service.</span></span> <span data-ttu-id="fe991-109">Дополнительные сведения можно найти в разделе [Запуск и остановка службы расширенного](start-and-stop-the-agpm-service-agpm30ops.md)просмотра.</span><span class="sxs-lookup"><span data-stu-id="fe991-109">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

2.  <span data-ttu-id="fe991-110">Удалите существующий архив.</span><span class="sxs-lookup"><span data-stu-id="fe991-110">Remove the existing archive.</span></span> <span data-ttu-id="fe991-111">По умолчанию папкой "Архив" является%ProgramData%\\Microsoft\\AGPM, но администратор РАСШИРЕНного управления групповыми политиками (Microsoft) может ввести другое расположение во время настройки.</span><span class="sxs-lookup"><span data-stu-id="fe991-111">By default, the archive folder is %ProgramData%\\Microsoft\\AGPM, however the AGPM Administrator who installed Microsoft Advanced Group Policy Management - Server may have entered a different location during setup.</span></span>

3.  <span data-ttu-id="fe991-112">Чтобы создать папку архива, настройте путь к архиву, учетную запись службы, а также владельца архива и прослушивающий порт.</span><span class="sxs-lookup"><span data-stu-id="fe991-112">Re-create the archive folder by configuring the archive path, AGPM Service Account, Archive Owner, and listening port.</span></span> <span data-ttu-id="fe991-113">Использование тех же значений, которые использовались при первоначальной установке, не требуется.</span><span class="sxs-lookup"><span data-stu-id="fe991-113">Using the same values as used during the original installation is not necessary.</span></span> <span data-ttu-id="fe991-114">Дополнительные сведения можно найти в разделе [изменение службы расширенного редактирования](modify-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="fe991-114">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md).</span></span>

4.  <span data-ttu-id="fe991-115">Скопируйте содержимое резервной копии архива в папку "Архив", скопировав вложенные папки и файлы, чтобы они унаследовали разрешения папки "архивы" для каждой подпапки и файла.</span><span class="sxs-lookup"><span data-stu-id="fe991-115">Copy the contents of the archive backup to the archive folder, copying the subfolders and files to make sure that each subfolder and file inherits the permissions of the archive folder.</span></span> <span data-ttu-id="fe991-116">Будьте внимательны, чтобы перезаписать папку архива.</span><span class="sxs-lookup"><span data-stu-id="fe991-116">Be careful not to overwrite the archive folder.</span></span>

5.  <span data-ttu-id="fe991-117">Если вы не уверены в том, что объект групповой политики в резервной копии является более актуальным, чем копия этого GPO, создайте отчет о разнице и сравните их настройки.</span><span class="sxs-lookup"><span data-stu-id="fe991-117">If you not sure about whether a GPO in the archive backup is more current than the copy of that GPO in production, generate a difference report and compare their settings.</span></span> <span data-ttu-id="fe991-118">Дополнительные сведения можно найти в разделе [Определение различий между GPO, версиями объектов групповой политики или шаблонами](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="fe991-118">For more information, see [Identify Differences Between GPOs, GPO Versions, or Templates](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md).</span></span>

6.  <span data-ttu-id="fe991-119">Перезапустите службу РАСШИРЕНного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="fe991-119">Restart the AGPM Service.</span></span> <span data-ttu-id="fe991-120">Дополнительные сведения можно найти в разделе [Запуск и остановка службы расширенного](start-and-stop-the-agpm-service-agpm30ops.md)просмотра.</span><span class="sxs-lookup"><span data-stu-id="fe991-120">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

### <span data-ttu-id="fe991-121">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="fe991-121">Additional references</span></span>

-   [<span data-ttu-id="fe991-122">Резервное копирование архива</span><span class="sxs-lookup"><span data-stu-id="fe991-122">Back Up the Archive</span></span>](back-up-the-archive.md)

-   [<span data-ttu-id="fe991-123">Перемещение сервера и архива AGPM</span><span class="sxs-lookup"><span data-stu-id="fe991-123">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive.md)

-   [<span data-ttu-id="fe991-124">Управление архивами</span><span class="sxs-lookup"><span data-stu-id="fe991-124">Managing the Archive</span></span>](managing-the-archive.md)

 

 





