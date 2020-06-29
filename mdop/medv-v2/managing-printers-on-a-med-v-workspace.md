---
title: Управление принтерами в рабочей области MED-V
description: Управление принтерами в рабочей области MED-V
author: dansimp
ms.assetid: ba0a65ad-444f-4d18-95eb-8b9fa1a3ffba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bc7a62075c95e8816a425eff89ffb992f1185d04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826119"
---
# <span data-ttu-id="a8200-103">Управление принтерами в рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="a8200-103">Managing Printers on a MED-V Workspace</span></span>


<span data-ttu-id="a8200-104">В Microsoft Enterprise Virtualization (MED-V) 2,0, перенаправление принтеров обеспечивает конечные пользователи с одинаковым интерфейсом печати между виртуальной машиной MED-V и ведущим компьютером.</span><span class="sxs-lookup"><span data-stu-id="a8200-104">In Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, printer redirection provides end users with a consistent printing experience between the MED-V virtual machine and the host computer.</span></span>

<span data-ttu-id="a8200-105">В этом разделе приводятся сведения о том, как управлять печатью в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="a8200-105">This topic provides information about how to manage printing in a MED-V workspace.</span></span>

## <span data-ttu-id="a8200-106">Управление принтерами в рабочих областях MED-V</span><span class="sxs-lookup"><span data-stu-id="a8200-106">Managing Printers in MED-V Workspaces</span></span>


<span data-ttu-id="a8200-107">В большинстве случаев MED-V автоматически обрабатывает перенаправление принтера.</span><span class="sxs-lookup"><span data-stu-id="a8200-107">In most cases, MED-V handles printer redirection automatically.</span></span> <span data-ttu-id="a8200-108">После первого завершения настройки MED-V определяет все сетевые принтеры, установленные на узле, извлекает соответствующие драйверы с сетевого сервера печати и, если он найден, устанавливает соответствующие драйверы в рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="a8200-108">After first time setup finishes, MED-V identifies all network printers installed on the host, retrieves the corresponding drivers from the network print server, and if found, installs the relevant drivers in the MED-V workspace.</span></span> <span data-ttu-id="a8200-109">После того как все драйверы будут найдены и установлены, MED-V перезагружает рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="a8200-109">After all drivers are found and installed, MED-V reboots the MED-V workspace.</span></span> <span data-ttu-id="a8200-110">Только после перезапуска рабочей области MED-V принтеры узла будут представлены и доступны на гостевом компьютере (обычно через несколько минут).</span><span class="sxs-lookup"><span data-stu-id="a8200-110">Only after the MED-V workspace restarts, the host printers are present and available on the guest, typically in a few minutes.</span></span>

<span data-ttu-id="a8200-111">**Примечание**  Если в рабочей области для MED-V запущены приложения, пользователю будет предложено выполнить перезагрузку, чтобы продолжить, или отложить ее на более поздний срок.</span><span class="sxs-lookup"><span data-stu-id="a8200-111">**Note** If applications are running on the MED-V workspace, the end user is prompted to let the restart continue or postpone it until later.</span></span> <span data-ttu-id="a8200-112">Если приложение не запущено, перезагрузка выполняется автоматически и не отображается для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8200-112">If no applications are running, the restart is automatic and not shown to the end user.</span></span>

 

<span data-ttu-id="a8200-113">При каждом запуске MED-V выполняется проверка того, установлены ли на узле новые принтеры, и, если оно найдено, извлекает соответствующие драйверы с сетевого сервера печати и устанавливает их на гость.</span><span class="sxs-lookup"><span data-stu-id="a8200-113">Every time MED-V is re-started, it checks whether any new printers are installed on the host and, if found, retrieves the corresponding drivers from the network print server and installs them on the guest.</span></span> <span data-ttu-id="a8200-114">Затем MED-V перезапустит рабочую область MED-V точно так же, как при первом завершении настройки.</span><span class="sxs-lookup"><span data-stu-id="a8200-114">MED-V then restarts the MED-V workspace just as when first time setup was completed.</span></span>

<span data-ttu-id="a8200-115">**Важно!**  После того как на гостевой компьютере будут установлены необходимые драйверы, принтеры станут видны только на гостевой машине после перезапуска.</span><span class="sxs-lookup"><span data-stu-id="a8200-115">**Important** After the relevant drivers are installed on the guest, the printers only become visible on the guest after the restart occurs.</span></span>

 

<span data-ttu-id="a8200-116">Если вы в любой момент не можете найти или установить драйвер, его необходимо установить на гостевой машине вручную, чтобы обеспечить доступность сетевого принтера для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8200-116">If at any time a driver cannot be located or installed, it must be manually installed on the guest for the network printer to be available to the end user.</span></span>

<span data-ttu-id="a8200-117">Ниже приведены некоторые дополнительные рекомендации.</span><span class="sxs-lookup"><span data-stu-id="a8200-117">The following list offers some additional guidance:</span></span>

<span data-ttu-id="a8200-118">**Только сетевые принтеры управляются с помощью MED-V**.</span><span class="sxs-lookup"><span data-stu-id="a8200-118">**MED-V only manages network printers**.</span></span> <span data-ttu-id="a8200-119">Драйверы для принтеров, установленных локально на узле, не устанавливаются автоматически на гостевой машине.</span><span class="sxs-lookup"><span data-stu-id="a8200-119">Drivers for printers that are installed locally on the host are not automatically installed on the guest.</span></span>

<span data-ttu-id="a8200-120">**При обнаружении на сервере печати MED-V устанавливаются только драйверы принтера**.</span><span class="sxs-lookup"><span data-stu-id="a8200-120">**MED-V only installs printer drivers if found on the print server**.</span></span> <span data-ttu-id="a8200-121">В противном случае драйверы принтера должны быть установлены вручную.</span><span class="sxs-lookup"><span data-stu-id="a8200-121">If not found, printer drivers must be manually installed.</span></span>

<span data-ttu-id="a8200-122">**Принтеры, установленные вручную на гостевом компьютере, недоступны для узла**.</span><span class="sxs-lookup"><span data-stu-id="a8200-122">**Printers manually installed on the guest are not accessible to the host**.</span></span> <span data-ttu-id="a8200-123">По умолчанию MED-V поддерживает перенаправление принтеров только от гостя на узел.</span><span class="sxs-lookup"><span data-stu-id="a8200-123">By default, MED-V only supports printer redirection from the guest to the host.</span></span>

<span data-ttu-id="a8200-124">**Предупреждение**  Если принтер установлен вручную на гостевом компьютере, а этот принтер позже установлен на нем, то в результате этот принтер устанавливается дважды на гостевой машине.</span><span class="sxs-lookup"><span data-stu-id="a8200-124">**Warning** If a printer is manually installed on the guest, and the same printer is later installed on the host, the result is that the printer is installed two times in the guest.</span></span> <span data-ttu-id="a8200-125">Чтобы избежать такой ситуации, рекомендуется управлять перенаправлением принтеров одним способом: отключите перенаправление и установите принтеры вручную на гостевой или включите перенаправление и не устанавливайте принтеры вручную на гостевой машине.</span><span class="sxs-lookup"><span data-stu-id="a8200-125">To avoid this situation, a MED-V best practice is to manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

 

## <span data-ttu-id="a8200-126">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a8200-126">Related topics</span></span>


[<span data-ttu-id="a8200-127">Управление параметрами рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="a8200-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





