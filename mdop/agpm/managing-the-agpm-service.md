---
title: Управление службой AGPM
description: Управление службой AGPM
author: dansimp
ms.assetid: 331f64d2-1236-4711-81b4-1b92f019bfa5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3247be846487ba6d80f30a55654b20b3db96e219
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820572"
---
# <span data-ttu-id="3368a-103">Управление службой AGPM</span><span class="sxs-lookup"><span data-stu-id="3368a-103">Managing the AGPM Service</span></span>


<span data-ttu-id="3368a-104">Служба управления групповыми политиками — это служба Windows, которая выступает в качестве прокси-сервера, управляет доступом клиентов к объектам групповой политики (GPO) в архивной и рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="3368a-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="3368a-105">Для этого используется расширенное делегирование управления групповыми политиками и обеспечивается улучшенный уровень безопасности.</span><span class="sxs-lookup"><span data-stu-id="3368a-105">It enforces Advanced Group Policy Management (AGPM) delegation and provides an enhanced level of security.</span></span> <span data-ttu-id="3368a-106">Служба расширенного управления групповыми политиками размещается на сервере, на котором установлен компонент Advanced Group Policy Management (Майкрософт) — сервер.</span><span class="sxs-lookup"><span data-stu-id="3368a-106">The AGPM Service is hosted on the server on which the Microsoft Advanced Group Policy Management - Server is installed.</span></span>

<span data-ttu-id="3368a-107">**Внимание!**  Не изменяйте параметры службы РАСШИРЕНного **управления правами с помощью средств администрирования** и **служб** в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="3368a-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="3368a-108">Это может привести к невозможности запуска службы РАСШИРЕНного настольных служб.</span><span class="sxs-lookup"><span data-stu-id="3368a-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

-   [<span data-ttu-id="3368a-109">Запуск и остановка службы AGPM</span><span class="sxs-lookup"><span data-stu-id="3368a-109">Start and Stop the AGPM Service</span></span>](start-and-stop-the-agpm-service.md)

-   [<span data-ttu-id="3368a-110">Изменение пути к архиву</span><span class="sxs-lookup"><span data-stu-id="3368a-110">Modify the Archive Path</span></span>](modify-the-archive-path.md)

-   [<span data-ttu-id="3368a-111">Изменение учетной записи службы AGPM</span><span class="sxs-lookup"><span data-stu-id="3368a-111">Modify the AGPM Service Account</span></span>](modify-the-agpm-service-account.md)

-   [<span data-ttu-id="3368a-112">Изменения порта, который прослушивает служба AGPM</span><span class="sxs-lookup"><span data-stu-id="3368a-112">Modify the Port on Which the AGPM Service Listens</span></span>](modify-the-port-on-which-the-agpm-service-listens.md)

 

 





