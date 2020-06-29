---
title: Управление службой AGPM
description: Управление службой AGPM
author: dansimp
ms.assetid: 48ca02aa-6acf-403b-afd4-66ae8a953246
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cba6890986efdc6dbaec7cee8ebbec38903ca524
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820562"
---
# <span data-ttu-id="83879-103">Управление службой AGPM</span><span class="sxs-lookup"><span data-stu-id="83879-103">Managing the AGPM Service</span></span>


<span data-ttu-id="83879-104">Служба управления групповыми политиками — это служба Windows, которая выступает в качестве прокси-сервера, управляет доступом клиентов к объектам групповой политики (GPO) в архивной и рабочей среде домена.</span><span class="sxs-lookup"><span data-stu-id="83879-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment of the domain.</span></span> <span data-ttu-id="83879-105">Для этого используется расширенное делегирование управления групповыми политиками и обеспечивается улучшенный уровень безопасности.</span><span class="sxs-lookup"><span data-stu-id="83879-105">It enforces Advanced Group Policy Management (AGPM) delegation and provides an enhanced level of security.</span></span> <span data-ttu-id="83879-106">Служба расширенного управления групповыми политиками размещается на сервере, на котором установлен компонент Advanced Group Policy Management (Майкрософт) — сервер.</span><span class="sxs-lookup"><span data-stu-id="83879-106">The AGPM Service is hosted on the server on which the Microsoft Advanced Group Policy Management - Server is installed.</span></span>

<span data-ttu-id="83879-107">**Внимание!**  Не изменяйте параметры службы РАСШИРЕНного **управления правами с помощью средств администрирования** и **служб** в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="83879-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="83879-108">Это может привести к невозможности запуска службы РАСШИРЕНного настольных служб.</span><span class="sxs-lookup"><span data-stu-id="83879-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

-   [<span data-ttu-id="83879-109">Запуск и остановка службы AGPM</span><span class="sxs-lookup"><span data-stu-id="83879-109">Start and Stop the AGPM Service</span></span>](start-and-stop-the-agpm-service-agpm40.md)

-   [<span data-ttu-id="83879-110">Изменение службы AGPM</span><span class="sxs-lookup"><span data-stu-id="83879-110">Modify the AGPM Service</span></span>](modify-the-agpm-service-agpm40.md)

### <span data-ttu-id="83879-111">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="83879-111">Additional references</span></span>

-   [<span data-ttu-id="83879-112">Перемещение сервера и архива AGPM</span><span class="sxs-lookup"><span data-stu-id="83879-112">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive-agpm40.md)

-   [<span data-ttu-id="83879-113">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="83879-113">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





