---
title: Управление архивами
description: Управление архивами
author: dansimp
ms.assetid: b11a3d71-74ea-4dd7-b243-6f2880b7af2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 682d720b4095dbfa6a7cc4d868109f57c4f54641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820559"
---
# <span data-ttu-id="d1105-103">Управление архивами</span><span class="sxs-lookup"><span data-stu-id="d1105-103">Managing the Archive</span></span>


<span data-ttu-id="d1105-104">В расширенном управлении групповыми политиками (расширенный доступ) вы можете управлять доступом к архиву, а также ограничивать количество версий объектов групповой политики (GPO), которые хранятся в архиве.</span><span class="sxs-lookup"><span data-stu-id="d1105-104">In Advanced Group Policy Management (AGPM), as an AGPM Administrator (Full Control), you manage access to the archive and have the option to limit the number of versions of each Group Policy Object (GPO) stored in the archive.</span></span> <span data-ttu-id="d1105-105">Вы можете делегировать доступ к объектам групповой политики в архиве на уровне домена или GPO.</span><span class="sxs-lookup"><span data-stu-id="d1105-105">You can delegate access to GPOs in the archive at the domain level or GPO level.</span></span> <span data-ttu-id="d1105-106">Кроме того, вы можете создать резервную копию архива, чтобы восстановить его при возникновении аварии.</span><span class="sxs-lookup"><span data-stu-id="d1105-106">Additionally, you can back up the archive so that you may be able to recover it if a disaster occurs.</span></span>

<span data-ttu-id="d1105-107">Как администратор РАСШИРЕНного администрирования группы, вы можете экспортировать в файл объект групповой политики, скопировать его в другой лес и затем импортировать этот объект в домен в этом лесу.</span><span class="sxs-lookup"><span data-stu-id="d1105-107">As an AGPM Administrator, you can export a GPO to a file, copy the file to another forest, and then import the GPO into a domain in that forest.</span></span> <span data-ttu-id="d1105-108">В отличие от редактора, вы можете импортировать параметры политики из резервной копии GPO прямо в новый управляемый объект групповой политики при его создании.</span><span class="sxs-lookup"><span data-stu-id="d1105-108">Unlike an Editor, you can import policy settings from a GPO backup directly into a new controlled GPO when you create it.</span></span> <span data-ttu-id="d1105-109">Сведения о том, как экспортировать объект групповой политики, приведены [в разделе Экспорт объекта групповой политики в файл](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="d1105-109">For information about how to export a GPO, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

-   [<span data-ttu-id="d1105-110">Предоставление доступа на уровне домена к архиву</span><span class="sxs-lookup"><span data-stu-id="d1105-110">Delegate Domain-Level Access to the Archive</span></span>](delegate-domain-level-access-to-the-archive-agpm40.md)

-   [<span data-ttu-id="d1105-111">Передача прав доступа для отдельного объекта групповой политики в архиве</span><span class="sxs-lookup"><span data-stu-id="d1105-111">Delegate Access to an Individual GPO in the Archive</span></span>](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md)

-   [<span data-ttu-id="d1105-112">Ограничение хранимых версий объекта групповой политики</span><span class="sxs-lookup"><span data-stu-id="d1105-112">Limit the GPO Versions Stored</span></span>](limit-the-gpo-versions-stored-agpm40.md)

-   [<span data-ttu-id="d1105-113">Импорт объекта групповой политики из файла</span><span class="sxs-lookup"><span data-stu-id="d1105-113">Import a GPO from a File</span></span>](import-a-gpo-from-a-file-agpmadmin.md)

-   [<span data-ttu-id="d1105-114">Резервное копирование архива</span><span class="sxs-lookup"><span data-stu-id="d1105-114">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="d1105-115">Восстановление архива из резервной копии</span><span class="sxs-lookup"><span data-stu-id="d1105-115">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

### <span data-ttu-id="d1105-116">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="d1105-116">Additional references</span></span>

-   <span data-ttu-id="d1105-117">Сведения о делегировании доступа к объектам групповой политики в рабочей среде можно найти в разделе [Передача доступа в производственную среду](delegate-access-to-the-production-environment-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="d1105-117">For information about how to delegate access to GPOs in the production environment, see [Delegate Access to the Production Environment](delegate-access-to-the-production-environment-agpm40.md).</span></span>

-   <span data-ttu-id="d1105-118">Сведения о том, как переместить Архив, приведены в разделе [Перемещение сервера расширенного использования и архива](move-the-agpm-server-and-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="d1105-118">For information about how to move the archive, see [Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md).</span></span>

-   [<span data-ttu-id="d1105-119">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="d1105-119">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





