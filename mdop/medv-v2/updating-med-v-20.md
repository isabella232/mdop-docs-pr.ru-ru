---
title: Обновление MED-V 2.0
description: Обновление MED-V 2.0
author: dansimp
ms.assetid: beea2f54-42d7-4a17-98e0-d243a8562265
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 62e8987ec511783422b8dd336dd4f3be2008c9b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823732"
---
# <span data-ttu-id="a3678-103">Обновление MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="a3678-103">Updating MED-V 2.0</span></span>


<span data-ttu-id="a3678-104">Обеспечьте безопасность системы, применяя соответствующие обновления для системы безопасности для Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="a3678-104">Help secure your system by applying the appropriate security updates for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="a3678-105">Обновление MED-V</span><span class="sxs-lookup"><span data-stu-id="a3678-105">Updating MED-V</span></span>


<span data-ttu-id="a3678-106">Вы можете обновить версию MED-V в интерактивном режиме, конечным пользователем или автоматически, используя электронную систему распространения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="a3678-106">You can update MED-V interactively, by the end user, or silently by using an electronic software distribution system.</span></span> <span data-ttu-id="a3678-107">Установка агента узла MED-V обновляет агент узла MED-v, а затем при необходимости обновляет рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="a3678-107">Installation of the MED-V Host Agent upgrades the MED-V Host Agent and then updates the MED-V workspace if required.</span></span> <span data-ttu-id="a3678-108">Агент узла MED-V и гостевой агент постоянно синхронизируются. Если приложение запускается из рабочей области MED-V во время обновления агента узла MED-v, для его завершения требуется перезагрузка главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="a3678-108">The MED-V Host Agent and Guest Agent keep in sync. If applications are running from the MED-V workspace while the MED-V Host Agent is being updated, a restart of the host computer is required to complete the update.</span></span> <span data-ttu-id="a3678-109">Если ни одно приложение не запущено, MED-V запускается автоматически и обновление завершается без перезапуска главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="a3678-109">If no applications are running, MED-V is restarted automatically and the upgrade is completed without a restart of the host computer.</span></span>

<span data-ttu-id="a3678-110">Если вы обновляете MED-V с помощью электронной системы распространения программного обеспечения, вы можете управлять поведением при перезапуске.</span><span class="sxs-lookup"><span data-stu-id="a3678-110">If you are updating MED-V by using an electronic software distribution system, you can control the restart behavior.</span></span> <span data-ttu-id="a3678-111">Чтобы сделать это, не загружайте перезагрузку, введя **reboot = "REALLYSUPPRESS"** в командной строке при установке MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="a3678-111">To do this, suppress the restart by typing **REBOOT=”ReallySuppress”** at the command prompt when installing MED-V\_HostAgent\_Setup.exe.</span></span> <span data-ttu-id="a3678-112">Затем настройте электронную систему распространения программного обеспечения, чтобы захватить код возврата 3010 (который сигнализирует, что требуется перезагрузка), и выполните действие Set restart.</span><span class="sxs-lookup"><span data-stu-id="a3678-112">Then, configure the electronic software distribution system to capture the 3010 return code (which signals that a restart is required) and perform the set restart behavior.</span></span>

## <span data-ttu-id="a3678-113">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a3678-113">Related topics</span></span>


[<span data-ttu-id="a3678-114">Технический справочник по MED-V</span><span class="sxs-lookup"><span data-stu-id="a3678-114">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





