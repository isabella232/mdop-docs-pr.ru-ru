---
title: Вкладка "Сервер AGPM"
description: Вкладка "Сервер AGPM"
author: dansimp
ms.assetid: a6689437-233e-4f33-a0d6-f7d432c96c00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7ffaa3f55d4ae1c2a59287d9dc302aec3dd00aed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819282"
---
# <span data-ttu-id="b9789-103">Вкладка "Сервер AGPM"</span><span class="sxs-lookup"><span data-stu-id="b9789-103">AGPM Server Tab</span></span>


<span data-ttu-id="b9789-104">С помощью вкладки **сервера расширенного управления групповыми политиками** в области " **изменение** " можно выбрать сервер политики доменных имен, указав полное имя компьютера и порт, а также удалить старые версии объектов групповой политики (GPO) из архива для экономии места на диске сервера расширенного управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="b9789-104">The **AGPM Server** tab on the **Change Control** pane enables you to select an AGPM Server by entering a fully-qualified computer name and port, and to delete older versions of Group Policy Objects (GPOs) from the archive to conserve disk space on the AGPM Server.</span></span>

## <span data-ttu-id="b9789-105">Указание сервера РАСШИРЕНного</span><span class="sxs-lookup"><span data-stu-id="b9789-105">Specifying the AGPM Server</span></span>


<span data-ttu-id="b9789-106">Выбранный сервер РАСШИРЕНного доступа определяет, какой из них будет отображаться на вкладке " **содержимое** " и к какому расположению будут применены параметры **делегирования домена** .</span><span class="sxs-lookup"><span data-stu-id="b9789-106">The AGPM Server selected determines which archive is displayed for you on the **Contents** tab and to which location the **Domain Delegation** settings are applied.</span></span> <span data-ttu-id="b9789-107">Портом по умолчанию для расширенного управления групповыми политиками является порт 4600.</span><span class="sxs-lookup"><span data-stu-id="b9789-107">The default port for Advanced Group Policy Management (AGPM) is port 4600.</span></span>

<span data-ttu-id="b9789-108">Если соединение с сервером РАСШИРЕНной конфигурации настроено с помощью параметров административных шаблонов, параметры на этой вкладке для настройки подключения будут недоступны.</span><span class="sxs-lookup"><span data-stu-id="b9789-108">If the AGPM Server connection is centrally configured using Administrative template settings, the options on this tab for configuring the connection are unavailable.</span></span> <span data-ttu-id="b9789-109">Дополнительные сведения можно найти в разделе [Настройка подключений к серверам с расширенным](configure-agpm-server-connections-agpm40.md)протоколом.</span><span class="sxs-lookup"><span data-stu-id="b9789-109">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

## <span data-ttu-id="b9789-110">Удаление старых версий GPO</span><span class="sxs-lookup"><span data-stu-id="b9789-110">Deleting old GPO versions</span></span>


<span data-ttu-id="b9789-111">По умолчанию все версии всех управляемых объектов групповой политики сохраняются в архиве.</span><span class="sxs-lookup"><span data-stu-id="b9789-111">By default, all versions of every controlled GPO are retained in the archive.</span></span> <span data-ttu-id="b9789-112">Однако вы можете настроить службу расширенного управления групповыми политиками, чтобы ограничить количество версий, сохраненных для каждого объекта групповой политики, и автоматически удалить самую старую версию при превышении этого ограничения.</span><span class="sxs-lookup"><span data-stu-id="b9789-112">However, you can configure the AGPM Service to limit the number of versions retained for each GPO and automatically delete the oldest version when that limit is exceeded.</span></span> <span data-ttu-id="b9789-113">Только версии объектов групповой политики, отображаемые на вкладке " **уникальные версии** " в окне **журнала** , предельное число.</span><span class="sxs-lookup"><span data-stu-id="b9789-113">Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

<span data-ttu-id="b9789-114">**Примечание**  Максимальное число уникальных версий, которые нужно хранить для каждого объекта групповой политики, не включает текущую версию, поэтому при вводе 0 сохраняется только текущая версия.</span><span class="sxs-lookup"><span data-stu-id="b9789-114">**Note** The maximum number of unique versions to store for each GPO does not include the current version, so entering 0 retains only the current version.</span></span> <span data-ttu-id="b9789-115">Предельное значение должно быть не более 999 версий.</span><span class="sxs-lookup"><span data-stu-id="b9789-115">The limit must be no greater than 999 versions.</span></span>

<span data-ttu-id="b9789-116">При удалении версии GPO запись этой версии сохраняется в истории объекта групповой политики, но сама версия GPO удаляется из архива.</span><span class="sxs-lookup"><span data-stu-id="b9789-116">When a GPO version is deleted, a record of that version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span> <span data-ttu-id="b9789-117">Вы можете запретить удаление версии GPO, пометив ее в истории как неудаляемую.</span><span class="sxs-lookup"><span data-stu-id="b9789-117">You can prevent a GPO version from being deleted by marking it in the history as not deletable.</span></span>

 

### <span data-ttu-id="b9789-118">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="b9789-118">Additional references</span></span>

-   [<span data-ttu-id="b9789-119">Пользовательский интерфейс: расширенное управление групповыми политиками</span><span class="sxs-lookup"><span data-stu-id="b9789-119">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="b9789-120">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="b9789-120">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

-   [<span data-ttu-id="b9789-121">Выполнение задач рецензента</span><span class="sxs-lookup"><span data-stu-id="b9789-121">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





